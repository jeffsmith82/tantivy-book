# Basic concepts of tantivy

Tantivy is a full-text search index written in rust that is designed as a library to make it easy to add searching functionality into your applications.

## Index

As we have said Tantivy is a full-text search index and this is the top level of tantivy. Each index is stored in it's own directory. This can be either in memory (RAM) or on disk. We will show you how to do both and why you would pick one other the other.

## Documents

Each index will be made up of one or more documents that you insert into the index. A document could be something like an email.

## Fields

Each document is made up of one or more fields. An email may be made up of multiple fields like 'from', 'to', 'subject', 'body' and 'Date received'. You can them search on these fields and it will return the ID of the document it was inserted into the index as.

## Types

There are multiple types that you can define your fields as in tantivy. For instance you would define the subject of our email as type "TEXT". You also have the ability to tell tantivy to store the whole content of the subject so it returns it with your results. This will increase the space required to store the index.

## Schema

When building a tantivy index we have to define our schema for the index. This means defining all the fileds and their types for all the documents you intend to insert into the index. If you need to add something to the schema later you have to delete and recreate your index from stratch with the new Schema.

## Query

When searching with tantivy you need to create a query that you give to an index searcher. There are multiple differnt types of query types in tantivy. We will learn about them later in teh book.

## Terms

terms are the individual parts of a query. For instance this query contains 2 terms which are split by the operator AND.

```subject:"invoice" AND body:"Microsoft"```