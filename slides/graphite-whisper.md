## Whisper

- Whisper is essentially directories and files on a disk and some python scripts
- Whisper requires size and resolution of database files to be specified in advance
- Schemas are immutable, but Whisper can reindex from one archive into a new schema
- Reindexing or even just renaming all the time is not at all practical (source: my personal experience)

Note:
> Whisper is a fixed-size database, similar in design and purpose to RRD (round-robin-database). It provides fast, reliable storage of numeric data over time. Whisper allows for higher resolution (seconds per point) of recent data to degrade into lower resolutions for long-term retention of historical data.

> ... an archive with 1 data point every 60 seconds can have a lower-resolution archive following it with a resolution of 1 data point every 300 seconds because 60 cleanly divides 300. In contrast, a 180 second precision (3 minutes) could not be followed by a 600 second precision (10 minutes) because the ratio of points to be propagated from the first archive to the next would be 3 1/3 and Whisper will not do partial point interpolation.

> Whisper databases contain one or more archives, each with a specific data resolution and retention (defined in number of points or max timestamp age). Archives are ordered from the highest-resolution and shortest retention archive to the lowest-resolution and longest retention period archive.

Semantics of Null:
- Each data point is stored with its timestamp
- The timestamps are used during data retrieval to check the validity of the data point
- All time-slots within an archive take up space whether or not a value is stored
