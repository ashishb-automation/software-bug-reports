# Severity and Priority Guide

Severity describes impact. Priority describes urgency. They are related, but they are not interchangeable.

## Severity

| Level | Practical meaning | Example |
| --- | --- | --- |
| Critical | System unavailable, security exposure, unrecoverable corruption or no safe workaround | Payment captured twice |
| High | Core workflow blocked or major data inconsistency | Eligible users cannot complete checkout |
| Medium | Feature behaves incorrectly but a reasonable workaround exists | Filters reset after pagination |
| Low | Limited inconvenience or presentation problem | Non-blocking alignment issue |

## Priority

| Level | When to use it |
| --- | --- |
| Urgent | Stop current release or start immediate incident work |
| High | Fix before the next relevant release |
| Medium | Schedule with normal product work |
| Low | Address when capacity allows |

## Rating questions

Before assigning severity, ask:

1. How many users or systems are affected?
2. Is a core workflow blocked?
3. Is data, money, privacy or security at risk?
4. Is there a safe and realistic workaround?
5. Does the problem recover without support intervention?

Priority should also consider release timing, contractual obligations, accessibility commitments, frequency and business exposure.
