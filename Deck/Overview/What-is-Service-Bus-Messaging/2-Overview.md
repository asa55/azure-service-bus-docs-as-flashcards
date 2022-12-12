##

Data is transferred between different applications and services using

%

messages

##

A message is a container decorated with metadata, and contains data. The data can be any kind of information, including structured data encoded with the common formats such as the following ones:

- `_____`
- `_____`
- `_____`
- `_____`

%

- JSON
- XML
- Apache Avro
- Plain Text

##

Some common messaging scenarios are:

- `_____`
- `_____`
- `_____`
- `_____`
- `_____`
- `_____`

%

- Messaging
- Decouple applications
- Load balancing
- Topics and subscriptions
- Transactions
- Message sessions

##

"Transfer business data, such as sales or purchase orders, journals, or inventory movements."

describes the common messaging scenario called

%

"Messaging"

##

"Improve reliability and scalability of applications and services. Producer and consumer don't have to be online or readily available at the same time. The load is leveled such that traffic spikes don't overtax a service."

describes the common messaging scenario called

%

"Decouple applications"

##

"Allow for multiple competing consumers to read from a queue at the same time, each safely obtaining exclusive ownership to specific messages."

describes the common messaging scenario called

%

"Load balancing"

##

"Enable 1:n relationships between publishers and subscribers, allowing subscribers to select particular messages from a published message stream."

describes the common messaging scenario called

%

"Topics and subscriptions"

##

"Allows you to do several operations, all in the scope of an atomic transaction."

describes the common messaging scenario called

%

"Transactions"

##

The following operations can be done in the scope of a transaction:

- `_____`
- `_____`
- `_____`

%

- Obtain a message from one queue
- Post results of processing to one or more different queues
- Move the input message from the original queue

##

For the common messaging scenario called "Transactions", the results become visible to downstream consumers only upon `_____`, including the `_____` settlement of input message, allowing for once-only processing semantics. This transaction model is a robust foundation for the compensating transactions pattern in the greater solution context.

%

For the common messaging scenario called "Transactions", the results become visible to downstream consumers only upon **success**, including the **successful** settlement of input message, allowing for once-only processing semantics. This transaction model is a robust foundation for the compensating transactions pattern in the greater solution context.

##

"Implement high-scale coordination of workflows and multiplexed transfers that require strict message ordering or message deferral."

describes the common messaging scenario called

%

"Message sessions"

##

Service Bus concepts are similar other message brokers like

%

Apache ActiveMQ

##

Azure Service Bus is a `_____`-as-a-service (`_____`) offering

%

Azure Service Bus is a **Platform**-as-a-service (**PaaS**) offering

##

Azure Service Bus takes care of the following chores for you:

- Worrying about hardware `_____`
- Keeping the operating systems or the products `_____`
- Placing `_____` and managing `_____` space
- Handling `_____`
- `_____` to a reserve machine

%

- Worrying about hardware **failures**
- Keeping the operating systems or the products **patched**
- Placing **logs** and managing **disk** space
- Handling **backups**
- **Failing over** to a reserve machine
