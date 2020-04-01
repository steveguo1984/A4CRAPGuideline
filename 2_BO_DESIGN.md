# How to design a RAP Object
This document try to find a way to help you make decision and avoid issues in the future when you design RAP Objects.
## When should I create RAP Objects with parent - child relationship 
Technicaly, if B is A's child object, you can not create B without A, and when A is deleted, the releated record in B is being deleted as well.
So when design the object, if B it self has business meaning even there is no A record exist, you should create them as 2 different root object. If B's meaning is totally rely on A, you should create B as a sub object of A.
There is no best practice of how many layer's you should have, all dependent on the business meaning.
## When to use Business Object Projection , when to just create a normal CDS view and select from a Business Object 
Compare to just write some select statement on business object view, business projection provide not only a different perspective of reading and query data but also consuming the CRUD logic / custom action. 
So if you want to create a perspective of how to write / operate the business object, you should create a business object projection, if only for reading and reporting, just create a normal CDS view
## What do I need to create , for a Business Object, by default, to get best flexibility and consistense in the long run ?

## What can / should I do / not to do when define CDS for  Business Object
## What can / should I do / not to do when define CDS for  Business Object Projection
## What can / should I do / not to do when define association
## What can / should I do / not to do when define CDS view for reporting purpose
## What can / should I do / not to do when define CDS view for value help purpose
## Naming Convension?

