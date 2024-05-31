# Salesforce Interview Question Answer

## Table of Content


## Batchable Apex
#### What is Batch Apex?
The Batch class executes every transaction, by breaking down large sets of data into small chunks and providing us with the additional benefit of a governor limit.

It provides us with a higher SOQL query limit. It implements a Database.Batchable interface.

Database.Batchable Interface has three methods that we have to implement:

Start – We collected the records either with a Database.QueryLocator or Iterable to pass them in the execute.<br/>
Execute – We performed the logic on the collected data. It will run multiple times according to the batch size.<br/>
Finish – We can do any post activities like sending emails.<br/>

Syntax: 
```apex
global class BatchDemo implements Database.Batchable <sObject> {
    global (Database.QueryLocator or Iterable<sobject>)
        start(Database.BatchableContext bc) {
        //query on object;
        //return Database.getQueryLocator(query);
    }
    global void execute(Database.batchableContext bc, List <SObject> scope) {
        //execute logic
    }
    global void finish(Database.BatchableContext bc) {
        //job such as sending email or any post activities
    }
}
```
