##

Messages are sent to and received from `_____`. `_____` store messages until the receiving application is available to receive and process them.

%

Messages are sent to and received from **queues**. **Queues** store messages until the receiving application is available to receive and process them.

##

`_____` in queues are ordered and timestamped on arrival. Once accepted by the broker, the `_____` is always held durably in triple-redundant storage, spread across availability zones if the namespace is zone-enabled. Service Bus keeps `_____` in memory or volatile storage until they've been reported by the client as accepted.

%

**Messages** in queues are ordered and timestamped on arrival. Once accepted by the broker, the **message** is always held durably in triple-redundant storage, spread across availability zones if the namespace is zone-enabled. Service Bus keeps **messages** in memory or volatile storage until they've been reported by the client as accepted.

##

Messages are delivered in `_____` mode, only delivering messages when requested. Unlike the busy-polling model of some other cloud queues, the `_____` operation can be long-lived and only complete once a message is available.

%

Messages are delivered in **pull** mode, only delivering messages when requested. Unlike the busy-polling model of some other cloud queues, the **pull** operation can be long-lived and only complete once a message is available.

##

You can use `_____` to send and receive messages. While a queue is often used for point-to-point communication, `_____` are useful in publish/subscribe scenarios.

%

You can use **topics** to send and receive messages. While a queue is often used for point-to-point communication, **topics** are useful in publish/subscribe scenarios.

##

Topics can have multiple, independent `_____`, which attach to the topic and otherwise work exactly like queues from the receiver side. A `_____` to a topic can receive a copy of each message sent to that topic. `_____` are named entities. `_____` are durable by default, but can be configured to expire and then be automatically deleted. Via the Java Message Service (JMS) API, Service Bus Premium also allows you to create volatile `_____` that exist for the duration of the connection.

%

Topics can have multiple, independent **subscriptions**, which attach to the topic and otherwise work exactly like queues from the receiver side. A **subscriber** to a topic can receive a copy of each message sent to that topic. **Subscriptions** are named entities. **Subscriptions** are durable by default, but can be configured to expire and then be automatically deleted. Via the Java Message Service (JMS) API, Service Bus Premium also allows you to create volatile **subscriptions** that exist for the duration of the connection.

##

You can define rules on a subscription. A subscription rule has a filter to define a condition for the message to be copied into the subscription and an optional action that can modify message metadata.

This feature is useful in the following scenarios:

- `_____`
- `_____`

%

- You don't want a subscription to receive all messages sent to a topic
- You want to mark up messages with extra metadata when they pass through a subscription

##

A `_____` is a container for all messaging components (queues and topics). Multiple queues and topics can be in a single `_____`, and `_____` often serve as application containers.

%

A **namespace** is a container for all messaging components (queues and topics). Multiple queues and topics can be in a single **namespace**, and **namespaces** often serve as application containers.

##

A namespace can be compared to a `_____` in the terminology of other brokers, but the concepts aren't directly equivalent.

%

A namespace can be compared to a **server** in the terminology of other brokers, but the concepts aren't directly equivalent.

##

A Service Bus namespace is your own capacity slice of a large cluster made up of dozens of all-active virtual machines. It may optionally span three Azure availability zones. So, you get all the availability and robustness benefits of running the message broker at enormous scale. And, you don't need to worry about underlying complexities. Service Bus is `_____` messaging.

%

A Service Bus namespace is your own capacity slice of a large cluster made up of dozens of all-active virtual machines. It may optionally span three Azure availability zones. So, you get all the availability and robustness benefits of running the message broker at enormous scale. And, you don't need to worry about underlying complexities. Service Bus is **serverless** messaging.

##

To realize a first-in, first-out (FIFO) guarantee in Service Bus, use sessions. `_____` enable joint and ordered handling of unbounded sequences of related messages.

%

To realize a first-in, first-out (FIFO) guarantee in Service Bus, use sessions. **Message sessions** enable joint and ordered handling of unbounded sequences of related messages.

##

The `_____` feature enables you to chain a queue or subscription to another queue or topic that is part of the same namespace. When `_____` is enabled, Service Bus automatically removes messages that are placed in the first queue or subscription (source) and puts them in the second queue or topic (destination).

%

The **auto-forwarding** feature enables you to chain a queue or subscription to another queue or topic that is part of the same namespace. When **auto-forwarding** is enabled, Service Bus automatically removes messages that are placed in the first queue or subscription (source) and puts them in the second queue or topic (destination).

##

Service Bus supports a `_____` (`_____`) to hold messages that cannot be delivered to any receiver, or messages that cannot be processed. You can then remove messages from the `_____` and inspect them.

%

Service Bus supports a **dead-letter queue** (**DLQ**) to hold messages that cannot be delivered to any receiver, or messages that cannot be processed. You can then remove messages from the **DLQ** and inspect them.

##

You can submit messages to a queue or topic for `_____` processing. For example, to schedule a job to become available for processing by a system at a certain time.

%

You can submit messages to a queue or topic for **delayed** processing. For example, to schedule a job to become available for processing by a system at a certain time.

##

When a queue or subscription client receives a message that it's willing to process, but for which processing isn't currently possible because of special circumstances within the application, the entity can defer `_____` of the message to a later point. The message remains in the queue or subscription, but it's set aside.

%

When a queue or subscription client receives a message that it's willing to process, but for which processing isn't currently possible because of special circumstances within the application, the entity can defer **retrieval** of the message to a later point. The message remains in the queue or subscription, but it's set aside.

##

A `_____` groups two or more operations together into an execution scope. Service Bus supports grouping operations against a single messaging entity (queue, topic, subscription) within the scope of a `_____`.

%

A **transaction** groups two or more operations together into an execution scope. Service Bus supports grouping operations against a single messaging entity (queue, topic, subscription) within the scope of a **transaction**.

##

Subscribers can define which messages they want to receive from a topic. These messages are specified in the form of one or more `_____` subscription rules. For each matching rule condition, the subscription produces a copy of the message, which may be differently annotated for each matching rule.

%

Subscribers can define which messages they want to receive from a topic. These messages are specified in the form of one or more **named** subscription rules. For each matching rule condition, the subscription produces a copy of the message, which may be differently annotated for each matching rule.

##

`_____` enables you to specify an idle interval after which the queue is automatically deleted. The interval is reset when there is traffic on the queue. The minimum duration is 5 minutes.

%

**Auto-delete on idle** enables you to specify an idle interval after which the queue is automatically deleted. The interval is reset when there is traffic on the queue. The minimum duration is 5 minutes.

##

If an error occurs that causes the client to have any doubt about the outcome of a send operation, `_____` takes the doubt out of these situations by enabling the sender to resend the same message, and the queue or topic discards any duplicate copies.

%

If an error occurs that causes the client to have any doubt about the outcome of a send operation, **duplicate detection** takes the doubt out of these situations by enabling the sender to resend the same message, and the queue or topic discards any duplicate copies.

##

Service Bus supports security protocols such as

- `_____`
- `_____`
- `_____`

%

- Shared Access Signatures (SAS)
- Role Based Access Control (RBAC)
- and Managed identities for Azure resources

##

When Azure regions or datacenters experience downtime, `_____` enables data processing to continue operating in a different region or datacenter.

%

When Azure regions or datacenters experience downtime, **Geo-disaster recovery** enables data processing to continue operating in a different region or datacenter.

##

Service Bus supports standard `_____` and `_____` protocols.

%

Service Bus supports standard **Advanced Message Queuing Protocol (AMQP) 1.0** and **HTTP/REST** protocols.
