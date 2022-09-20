# AZ messaging.

There are many ways to manage events in azure.

* Storage grid - Used for simple queueing, in order. Max msg size 64KB. No additional cost.
* Event grid - Event driven architectures. Max size 1 MB. **Great integration with other services.**\
* Event hub - Big data streaming. Max size  1MB. Low latency, designed for heavy load.
* Service bus - Advanced queueing solutions. Max size 256KB. Advance features and durability.s