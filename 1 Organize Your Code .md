# Orgnize Your Code
You have 2 stregty of orgnizing your code in ABAP Cloud
1. Single Repository Stregty
This approach works if your development team running in a traditional mode, that ABAP developers are orgnized by functional area, and have a clear sepraration between develop team and operation team.

You orgnize your ABAP code just like what you have done on ABAP on premise, that all the developers develop application in a big code repository which contain all your ABAP Code.
You create one namespace or develop without namespace ( using Y* or Z* objects ).
You have a package structure defined globally, as well as naming convension.
There should be a team centrally managing the transport for the whole system.

1. Container Based Stregty
This approach works when you working in a agile way, and have a morden devops concept. That you have different product team work on different products, and each taem manage their own development, operation and deployment themselves. And the dependency between products are only on exceptional case and clearly defined. 
What you need to do?
  1. Apply namespcae for each of your product, to elimite nameing conflict 
  1. Create a software component instead of package for each product because one software component is mapping to one code repository
  1. It is critical to have namespace shorter than 6 charaters, otherwise it will be really difficult to naming table and authfield
  1. It is good to run 1, or 10 products on same abap cloud instance, but don't run too much. Because now there is no limition to restrict which software component developer can work on, and each software will occupai a transport layer. Think about if you have 50+ products, everytime you create TR, you need to select the right transport layer for your product. So it is good to develop at least medium size product in ABAP Cloud, if you just want creat app with 1-5 screens and within 20 tables, or just want to have a very simple use case, consider use a shared software component, or consider using CAP instead of ABAP. The more complexy transactional logic you have in your product, the more benefit you get from ABAP Cloud.
