Lab 2.2: Initial Configuration and First Run of f5 WAF Tester
========================================================

2.2.1 - Create a configuration file for the first time by going to directory /home/f5student/.local/bin, and executing:

.. code-block:: bash

      ./f5-waf-tester –init

This will run you through a wizard where you will populate:

	[BIG-IP] Host []: 10.1.1.4
		This is the management IP of the Big-IP that is securing your application.

	[BIG-IP] Username []: admin
		Username of an account that can log into the Big-IP. (Can be a guest account)

	[BIG-IP] Password []: f5DEMOs4u!
		Password that is tied to the username above.

	ASM Policy Name []: /secops_testing/waf_juiceshop_secops_testing
		Name of the policy that is tied to the virtual server of the application you are testing.

	Virtual Server URL []: http://10.1.10.120 
		URL of the virtual server that services the application you are testing. 

For this lab take the defaults for the rest of the prompts (See Appendix A for an explanation of the other features).  If you want to see the configuration file, it can be found here: /home/f5student/.local/lib/python2.7/site-packages/f5_waf_tester/config/config.json 
You can also get there by typing:

.. code-block:: bash

	cat ~/.local/lib/python2.7/site-packages/f5_waf_tester/config/config.json

2.2.2 - You can now run the tool by issuing:

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

    		"fail": 39, 

    		"pass": 9

