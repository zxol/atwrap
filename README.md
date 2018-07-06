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
const record = await at.get.single({tableName, id})

const allRecords = await at.get.all(tableName)

const matchedRecords = await at.get.find({tableName, column, value})
const matchedRecords = await at.get.match({tableName, column, value})
const matchedRecords = await at.get.findAll({tableName, column, value})

const queryResult = await at.get.select({tableName, select})

const newRecord = await at.insert({tableName, data})
const newRecord = await at.add({tableName, data})
const newRecord = await at.create({tableName, data})

const updatedRecord = await at.update({tableName, id, data})
const updatedRecord = await at.set({tableName, id, data})

const deletedRecord = await at.delete({tableName, id})
const deletedRecord = await at.remove({tableName, id})
const deletedRecord = await at.destroy({tableName, id})


```
