Module 1: ASM Policy Template Creation on BIG-IP
===================================================
Expected time to complete: **1 hours**


For this module we’re going to be using a combination of the F5 TMUI (GUI) and Postman to make API calls to the F5 via AS3.  
AS3 stands for Application Services 3 Extension.  AS3 is a flexible, low-overhead mechanism for managing application-specific configurations on a BIG-IP system. 
AS3 uses a declarative model, meaning you provide a JSON declaration rather than a set of imperative commands. 
The declaration represents the configuration which AS3 is responsible for creating on a BIG-IP system.  To learn more about AS3, you can visit: 

https://clouddocs.f5.com/products/extensions/f5-appsvcs-extension/latest/

Step 1: Log into the Linux Client via RDP using the following credentials:

	Username:	f5student

	Password: 	f5DEMOs4u!


.. image:: images/1-module1.png

Step 2: We’re going to be working in the BIG-IP to create an ASM template with some specific settings applied that we can use on our VS.  
Once the template is created, we’ll use AS3 and Postman to add an ASM policy to a VS based on our template to show how to add automation of ASM policies to applications.  



    2a: Log into the BIG-IP by opening the FireFox browser in the Linux client and selecting the browser bookmark titled ‘bigip01’ using the following credentials:

        Username:	admin
    
        Password:	f5DEMOs4u!

        .. image:: images/2-module1.png

    2b:  Let’s create an ASM policy template that we’ll reference later, by navigating to:
		
		Security  ››  Application Security : Security Policies : Policies List

        a.	Click ‘Create’

        .. image:: images/3-module1.png

    2c.	Name the policy ‘waf_Protected’ and set the following settings:

        Policy Template:                                    Rapid Deployment Policy

        Enforcement Mode:	                                Blocking

        Auto-Added Signature Accuracy:	                    Medium

        Signature Staging:                                  Enabled

        Enforcement Readiness Period:	                    7

        Policy is Case Sensitive:	                        Disabled

        Differentiate between HTTP/WS and HTTPS/WSS URLs	Disabled

        .. image:: images/4-module1.png

            Click ‘Save’ to save the policy

        2d.	Navigate to:  Security  ››  Application Security : Geolocation Enforcement

            c.	We’re going to create a Geo enforcement on this policy to block North Korea form accessing out site.  
                From the ‘Allowed Geolocations’ on the right, find ‘Korea, Democratic People’s Republic of’ and bring it to the left window titled ‘Disallowed Geolocations’:

                .. image:: images/5-module1.png

.. toctree::
   :maxdepth: 1
   :glob:

   lab*/lab*
   review

