## Graphite Could be Problematic If:

- Your domain is best modeled categorically, not numerically
- The stats have many to many relationships to each other
- The number of categories, and relationships among categories, can't be determined in advance

Note:
- SubPub principal IDs and message types are like this
- Each subscription is owned by one principal, subscribing to one message type
- A Message Type may or may not be published, and if it does, it may be published
by any principal
- Some principals are related to each other, and others are not
- If I reported all stats to graphite, how could I query for delivery failures for all GRID message types?

