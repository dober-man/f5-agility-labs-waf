Lab 2.2: Initial Configuration of f5 WAF Tester
========================================================

Create a configuration file for the first time by going to directory /home/f5student/.local/bin, and executing:

.. code-block:: bash

      ./f5-waf-tester –init

This will run you through a wizard where you will populate:

	[BIG-IP] Host []: - .. code-block:: bash 10.1.1.4
		This is the management IP of the Big-IP that is securing your application.

	[BIG-IP] Username []: .. code-block:: bash admin
		Username of an account that can log into the Big-IP. (Can be a guest account)

	[BIG-IP] Password []: .. code-block:: bash f5DEMOs4u!
		Password that is tied to the username above.

	ASM Policy Name []: .. code-block:: bash owasptop10_secops_test
		Name of the policy that is tied to the virtual server of the application you are testing.

	Virtual Server URL []: .. code-block:: bash http://10.1.10.150 
		URL of the virtual server that services the application you are testing. 

For this lab take the defaults for the rest of the prompts (See Appendix A for an explanation of the other features).  If you want to see the configuration file, it can be found here: /home/f5student/.local/lib/python2.7/site-packages/f5_waf_tester/config/config.json 
You can also get there by typing:

.. code-block:: bash

	cd ~/.local/lib/python2.7/site-packages/f5_waf_tester/config/config.json

2.	You can now run the tool by issuing:

.. code-block:: bash

	./f5-waf-tester

The results of the tests will be displayed on the CLI and also saved to "report.json" under the current folder. Test results will give you information of the attack type that was executed, name of the attack, what protection it was testing (signature, evasion, or violation) along with a pass or fail verdict. If the protection is a signature, it will show the signature ID; if an evasion, it will show the evasion name; if a violation, it will show the violation name.  If the attack passes, you will get the support ID of the block page.  If the attack fails, you will get information of why it failed so you can make policy changes.  At the end it will show the summary and provide total number of passed/failed tests:

Attack information:
      	"attack_type": "Insecure Deserialization", 
      	"name": "Insecure Deserialization - node.js", 
      	"results": {
        		"header": {
          			"expected_result": {
            				"type": "signature", 
            				"value": "200004283”
Failed test:
          	"pass": false, 
          	"reason": "ASM Policy is not in blocking mode", 
          	"support_id": ""
Passed test:
"pass": true, 
          	"reason": "", 
          	"support_id": "4469169378524397882"
Summary:
"summary": {
    		"fail": 30, 
    		"pass": 18

3.	Open the report and look to see what is failing.

	a.	One way to do this:

		i.	vi report.json

		ii.	 Search for the failed results by looking for the term “false”.

			1.	Type: /false

		iii.	Look to see why the attack was not blocked by looking for the term “reason”
	b.	Another way:

		Type

	.. code-block:: bash

		cat report.json | jq .details[] | jq '.results[] | .expected_result.value, .pass, .reason’
	
		ii.	look for a result of “false” and why it did not pass
4.	Modify Policy named owasptop10_secops_test (change staging, enable signatures).

	a.	Enable appropriate signatures

	b.	Turn Staging off

	c.	Enable appropriate violations

	d.	Enable appropriate evasions
5.	Run the f5 WAF tester again to make sure all attacks are stopped.
6.	Update the Security Template with the new settings.

	a.	Go to Security -> Options -> Application Security -> Advanced Configuration -> Policy Templates.

	b.	Click on owasptop10 template

	c.	Under the Template File line, choose “Use existing security policy” and select the policy you just modified.

	d.	Click Update.

	.. image:: images/policy-template.png

.. toctree::
   :maxdepth: 1
   :glob:

   lab1
   lab3
   lab4
