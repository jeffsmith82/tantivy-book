# types

Tantivy has a very strict schema. The schema defines information about the fields your index contains, that is, for each field:

* the field name (may only contain letters [a-zA-Z], number [0-9], and _)
* the type of the field (currently only text and u64 are supported)
* how the field should be indexed / stored.

This very last point is critical as it will enable / disable some of the functionality for your index.

Tantivy's schema is stored within the meta.json file at the root of your directory.

* u64
* i64
* date
* text
* facet
* bytes


* FAST
* INDEXED
* STORED
* STRING
* TEXT