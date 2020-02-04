Appendix B: Matrix of all f5 WAF Tester Attacks
--------------------------------------------------------------

.. list-table::
   :widths: 20 20 20 20 20 20
   :header-rows: 1

   * - **Test ID**
     - **Attack Type**
     - **Name**
     - **System**
     - **Type**
     - **Signature ID**
   * - 100000001
     - XSS
     - HTML Tag Injection - script
     - All Systems
     - Signature
     - 200000097
   * - 
     -
     -
     - signature	
     - 200001088
   * - 
     -
     -
     - Signature	
     - 200000099
   * - 100000002		
     - HTML Attribute Injection - onmouseover	
     - All Systems	
     - Signature	
     - 200101163
   * - 
     -
     -
     - signature	
     - 200101162
   * - 
     -
     -
     - Signature	
     - 200101164
100000003		JavaScript Injection - eval	All Systems	signature	200001406
				signature	200001405
				signature	200001404
100000004	SQL Injection	SQL-Injection - integer field UNION	General Database	signature	200002554
				signature	200002611
				signature	200002495
100000005		Blind SQL-Injection	General Database	signature	200002546
				signature	200002045
				signature	200001404
100000006		Authentication Bypass SQL Injection	General Database	signature	200002836
				signature	200002835
				signature	200002837
100000007	NoSQL Injection	MongoDB Injection - db.getCollectionNames()	MongoDB	signature	200002784
				signature	200002783
				signature	200002785
100000008	Command Execution	Linux Command Execution - uname()	Unix/Linux	signature	200003412
				signature	200003921
				signature	200100315
100000009		Windows Command Exeuction - powershell	Microsoft Windows	signature	200003574
				signature	200003573
				signature	200003575
100000010	Path Traversal	Path Traversal	All Systems	signature	200003055
				signature	200003054
				evasion	Directory traversals
100000011	Predictable Resource Location	Predictable Resource Location	All Systems	signature	200001404
100000012	HTTP Protocol Compliance	Null in request	All Systems	violation	HTTP protocol compliance failed
100000013	Detection Evasion	Alternative Datastream Access	Microsoft Windows	signature	200001404
100000014	Insecure Deserialization	Insecure Deserialization - node.js	node.js	signature	200004283
				signature	200004282
				signature	200004284
100000015	Insecure Deserialization	Insecure Deserialization - PHP	PHP	signature	200004189
				signature	200004188
				signature	200004190
100000016	Information Leakage	Illegal Method TRACE	All systems	violation	Illegal Method
100000017	JSON Parser Attack	Malformed JSON	All systems	violation	Malformed JSON data
100000018	XML Parser Attack	Malformed XML	All systems	violation	Malformed XML data
100000019	HTTP Parser Attack	Cookie not RFC-compliant	All systems	violation	Cookie not RFC-compliant
100000020					
100000021		Wrong HTTP Protocol Version	All systems	violation	HTTP protocol compliance failed
100000022	HTTP Request Smuggling	HTTP Desync Attack Attempt	All systems	signature	200018061
100000023	Server Side Request Forgery	SSRF attempt (AWS Metadata Server)	All systems	signature	200018040
100000024	Server Side Request Forgery	SSRF attempt - Local network IP range 10.x.x.x	All systems	signature	200020201
