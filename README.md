# atwrap

A wrapper for common functions for accessing data on an airtable.com database.  All queries return promises.

## installation

```
npm i -s atwrap
```

## Usage

```
import Atwrap from 'atwrap'
const at = new Atwrap({apiKey: 'key9sdfkjisrfoi', databaseRef: 'appOIjFOIJJFioj'}) // faked data
```
note: you may create multiple instances for different databases, but only if they share the same api key.
Find your api key and database ref ID on the interactive docs page on airtable.com

## Interface list

```
const record = await at.getSingleRecordFrom({tableName, id})

const allRecords = await at.getAllRecordsFrom(tableName)

const matchedRecords = await at.getAllMatchedRecordsFrom({tableName, column, value})

const queryResult = await at.getRecordsSelect({tableName, select})

```
