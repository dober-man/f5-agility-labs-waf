Module 1: ASM Policy Template Creation on BIG-IP
===================================================

**Intro**

For this module we’re going to be using a combination of the F5 TMUI (GUI) and Postman to make API calls to the F5 via AS3.  
AS3 stands for Application Services 3 Extension.  AS3 is a flexible, low-overhead mechanism for managing application-specific configurations on a BIG-IP system. 
AS3 uses a declarative model, meaning you provide a JSON declaration rather than a set of imperative commands. 
The declaration represents the configuration which AS3 is responsible for creating on a BIG-IP system.  To learn more about AS3, you can visit: 

https://clouddocs.f5.com/products/extensions/f5-appsvcs-extension/latest/

**In this lab, we will cover the following:**

- Creation of an AWAF base policy (lab1) 
- Creating a template from a base policy (lab2)
- Deploying to a 'secops testing' environemnt (lab3) 


.. toctree::
   :maxdepth: 1
   :glob:

   lab*
   review

