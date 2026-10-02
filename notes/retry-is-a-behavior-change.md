# A retry is a behavior change

Retries are often introduced as an availability fix. They also change the shape of failure: one user action can become several calls, a delayed write, or a duplicate event.

Before adding a retry, define the timeout, which failures are transient, the backoff, the maximum attempt count, and the idempotency boundary. Then decide what the caller sees while the system is still trying.

The useful default is not “retry everything.” It is “make the failure class and duplicate behavior explicit.”
