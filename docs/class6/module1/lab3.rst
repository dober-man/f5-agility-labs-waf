Lab 1.3: Deploying to secops testing environment 
=========================================

1.3.1 review as3 declaration 
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~


1.3.2 deploy using AS3 
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

1.3.3 review the created items on the bigip
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

**Step 4:** Now that we have a template created, we’re now done with the BIG-IP for now and are moving onto Postman.  
Postman will be interacting with our BIG-IP via AS3 making API calls.  
Launch Postman from the Linux desktop icon shown below:

        .. image:: images/10-module1.png

    **4a.** Once Postman is open, we need to import the collection (series of declarations we’ll be using on our BIG-IP) from GitHub.  To do so, click on ‘Import’ on the top left of Postman and select ‘Import From Link’ option.  Paste the following into the field where you enter the URL and click ‘Import’

        https://gitlab.com/f5-examples/udf_waf_cicd/-/raw/master/WAF_342_postman_collection.json?inline=false 

        .. image:: images/11-module1.png

        With the collection imported, on the left-hand pane of Postman, you’ll see the collection titled ‘WAF_342’ with several declarations under it:

        .. image:: images/12-module1.png

        The first collection does a simple GET request against the lab BIG-IP to ensure that AS3 is installed and running.  
        It will also show you the version of AS3. 

        Click on the selection ‘check if AS3 is ready’ and click ‘Send’.  You should see the BIG IP report back with the following:

        .. image:: images/13-module1.png

        This validates that AS3 is running and responded with version 3.16.0

**Step 5:** We’re now going to make an AS3 declaration to the BIG-IP.  To view the JSON declaration, click on the declaration titled ‘as3 with_declarative_waf_and_vs’ and select ‘Body’ and ‘raw” as shown below:

    .. image:: images/14-module1.png

    In this declaration, we’re going to be creating a new Virtual Server on the BIG-IP, creating an ASM policy by referencing the template created earlier and applying it to the new Virtual Server. This virtual server front-ends a pool member that is running OWASP’s Juice Shop application that has all of the OWASP top 10 vulnerabilities.  

    Also note that the declaration is calling an external URL hosted on Gitlab and is our WAF JSON declaration that will be creating all of the configuration items mentioned above.  If you’d like, you can view the JSON declaration by using the bookmark bar in FireFox on the Linux Desktop and clicking on the ‘WAF_342’ Bookmark folder and clicking on ‘Gitlab’.  The following screen appears:

        .. image:: images/15-module1.png

    **5a.** Click on ‘waf_labs / waf_cicd’ and at the bottom of the page you’ll see ‘waf_policy.json’.  Click on that to view the JSON file:

        **Note in the top section you’ll see the name “owasptop10’.  This refers to the template we created on the BIG-IP to build the ASM policy and matches the name of the template we created in the BIG-IP.

        .. image:: images/16-module1.png

    **5b.** Return to Postman and run the declaration titled ‘as3_with_declarative_waf_VS_create’ by clicking ‘Send’ on the far right of the screen.  If it finished successfully, you’ll see the following response from the BIG-IP in Postman.

        .. image:: images/17-module1.png

    **5c.** Validate that the ASM policy has been created via the previous step by logging into the BIG-IP with the following credentials.  

        Username:	admin
		Password:	f5DEMOs4u!

		Once logged in, go to: 

            Security  ››  Application Security : Security Policies : Policies List
	
            There you’ll see the policy titled ‘waf_juiceshop_secops_testing’ under the newly created ‘secops_testing’ partition:

                .. image:: images/18-module1.png

            This declaration also created a VS on the BIG-IP called ‘juiceshop_secops_testing’ with the security policy ‘waf_juiceshop_secops_testing’ WAF policy applied.

                .. image:: images/18-module1.png

**Review of Module 1**

In this module we reviewed how to manually create an ASM template in the BIG-IP to use for various automation tasks.  The first task was to create the template with a base configuration with a few settings like blocking a geo location, and modifying HTTP protocol compliance settings.
We then used Visual Studio Code to review some pre-configured JSON files that we imported into the BIG-IP to create ASM policies for us.  This moved us further along the automation path by importing files to the BIG-IP for ASM policy creation rather than building them manually in the 
BIG-IP.  

Next we used Postman to interact with the BIG-IP and push our ASM JSON files calling AS3 on the BIG-IP to fully automate the creation of ASM policies.  

