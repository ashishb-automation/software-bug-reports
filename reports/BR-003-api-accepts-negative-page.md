# BR-003: Products API accepts a negative page number

| Field | Value |
| --- | --- |
| Area | Product API |
| Severity | Medium |
| Priority | Medium |
| Type | API validation |
| Frequency | 5 of 5 attempts |
| Status | Ready for triage |

## Request

```http
GET /api/products?page=-1&limit=20
Accept: application/json
```

## Expected result

The API should return `400 Bad Request` with a stable validation error explaining that `page` must be zero or greater.

## Actual result

The API returns `200 OK` and the same first-page records returned for `page=0`.

## Impact

Invalid client input is silently accepted. This can hide integration defects, produce duplicate records during pagination and make API behaviour harder for consumers to reason about.

## Severity and priority reasoning

**Medium severity:** data is not modified, but the paging contract is inconsistent and can create duplicate processing.

**Medium priority:** address with the next API validation work and add a contract test to prevent regression.

## Evidence

```json
{
  "request": { "page": -1, "limit": 20 },
  "status": 200,
  "returnedPage": 0,
  "itemCount": 20
}
```

Sensitive headers and tokens are intentionally excluded. Save the full sanitized request and response as `evidence/BR-003/negative-page-response.json`.

## Retest criteria

Check `page=-1`, a large negative integer, text, decimal and omitted values. Confirm the error schema, HTTP status and API documentation agree.
