- [How does AWS SQS work?](#how-does-aws-sqs-work)
- [Explain Amazon SQS Visibility Timeout?](#explain-amazon-sqs-visibility-timeout)
- [Amazon S3 data consistency model?](#amazon-s3-data-consistency-model)
- [Consistency Model in AWS DynomoDB?](#consistency-model-in-aws-dynomodb)

### How does AWS SQS work?
There are three main parts in a distributed messaging system:
 - the components of your distributed system
 - your queue (distributed on Amazon SQS servers)
 - the messages in the queue.

In the following scenario, your system has several producers (components that send messages to the queue) and consumers (components that receive messages from the queue). The queue (which holds messages A through E) redundantly stores the messages across multiple Amazon SQS servers.

- A producer sends message A to a queue, and the message is distributed across the Amazon SQS servers redundantly.
- When a consumer is ready to process messages, it consumes messages from the queue, and message A is returned. While message A is being processed, it remains in the queue and isn't returned to subsequent receive requests for the duration of the visibility timeout.
- The consumer deletes message A from the queue to prevent the message from being received and processed again when the visibility timeout expires.

### Explain Amazon SQS Visibility Timeout?
When a consumer receives and processes a message from a queue, the message remains in the queue. Amazon SQS doesn't automatically delete the message. Because Amazon SQS is a distributed system, there's no guarantee that the consumer actually receives the message (for example, due to a connectivity issue, or due to an issue in the consumer application). Thus, the consumer must delete the message from the queue after receiving and processing it.
Immediately after a message is received, it remains in the queue. To prevent other consumers from processing the message again, Amazon SQS sets a visibility timeout, a period of time during which Amazon SQS prevents other consumers from receiving and processing the message. 

### Amazon S3 data consistency model?
Amazon S3 provides strong read-after-write consistency for PUT and DELETE requests of objects in your Amazon S3 bucket in all AWS Regions. This behavior applies to both writes to new objects as well as PUT requests that overwrite existing objects and DELETE requests. In addition, read operations on Amazon S3 Select, Amazon S3 access controls lists (ACLs), Amazon S3 Object Tags, and object metadata (for example, the HEAD object) are strongly consistent.

### Consistency Model in AWS DynomoDB?
A database consistency model determines the manner and timing in which a successful write or update is reflected in a subsequent read operation of that same value. Amazon DynamoDB lets you specify the desired consistency characteristics for each read request within an application. You can specify whether a read is eventually consistent or strongly consistent.
- The `eventual consistency` option is the default in Amazon DynamoDB and maximizes the read throughput. However, an eventually consistent read might not always reflect the results of a recently completed write. Consistency across all copies of data is usually reached within a second.
- A `strongly consistent` read in Amazon DynamoDB returns a result that reflects all writes that received a successful response prior to the read. To get a strongly consistent read result, you can specify optional parameters in a request. It takes more resources to process a strongly consistent read than an eventually consistent read.
