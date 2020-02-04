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
   * - 100000001
     - XSS
     - HTML Tag Injection - script
     - -
     - Signature
     - 200001088
   * - 100000001
     - XSS
     - HTML Tag Injection - script
     - All Systems
     - Signature
     - 200000099
   * - 100000002		
     - XSS
     - HTML Attribute Injection - onmouseover	
     - All Systems	
     - Signature	
     - 200101163
   * - 100000002		
     - XSS
     - HTML Attribute Injection - onmouseover	
     - All Systems	
     - Signature	
     - 200101162
   * - 100000002		
     - XSS
     - HTML Attribute Injection - onmouseover	
     - All Systems	
     - Signature	
     - 200101164
   * - 100000003		
     - XSS
     - HTML Attribute Injection - onmouseover	
     - All Systems	
     - Signature	
     - 200001406
   * - 100000003		
     - XSS
     - HTML Attribute Injection - onmouseover	
     - All Systems	
     - Signature	
     - 200001405
   * - 100000003		
     - XSS
     - HTML Attribute Injection - onmouseover	
     - All Systems	
     - Signature	
     - 200001404
   * - 100000004		
     - SQL Injection
     - SQL-Injection - integer field UNION
     - General Database	
     - Signature	
     - 200002554
   * - 100000004		
     - SQL Injection
     - SQL-Injection - integer field UNION
     - General Database	
     - Signature	
     - 200002611
   * - 100000004		
     - SQL Injection
     - SQL-Injection - integer field UNION
     - General Database	
     - Signature	
     - 200002495
   * - 100000005		
     - SQL Injection
     - Blind SQL-Injection
     - General Database	
     - Signature	
     - 200002546
   * - 100000005		
     - SQL Injection
     - Blind SQL-Injection
     - General Database	
     - Signature	
     - 200002045
   * - 100000005		
     - SQL Injection
     - Blind SQL-Injection
     - General Database	
     - Signature	
     - 200001404
   * - 100000006		
     - SQL Injection
     - Authentication Bypass SQL Injection
     - General Database	
     - Signature	
     - 200002836
   * - 100000006		
     - SQL Injection
     - Authentication Bypass SQL Injection
     - General Database	
     - Signature	
     - 200002835
   * - 100000006		
     - SQL Injection
     - Authentication Bypass SQL Injection
     - General Database	
     - Signature	
     - 200002837
   * - 100000007		
     - NoSQL Injection
     - MongoDB Injection - db.getCollectionNames()
     - MongoDB	
     - Signature	
     - 200002784
   * - 100000007		
     - NoSQL Injection
     - MongoDB Injection - db.getCollectionNames()
     - MongoDB	
     - Signature	
     - 200002783
   * - 100000007		
     - NoSQL Injection
     - MongoDB Injection - db.getCollectionNames()
     - MongoDB	
     - Signature	
     - 200002785
   * - 100000008	
     - Command Execution
     - Linux Command Execution - uname()
     - Unix/Linux	
     - Signature	
     - 200003412
   * - 100000008	
     - Command Execution
     - Linux Command Execution - uname()
     - Unix/Linux	
     - Signature	
     - 200003921
   * - 100000008	
     - Command Execution
     - Linux Command Execution - uname()
     - Unix/Linux	
     - Signature	
     - 200100315
   * - 100000009	
     - Command Execution
     - Windows Command Exeuction - powershell
     - Microsoft Windows	
     - Signature	
     - 200003574
   * - 100000009	
     - Command Execution
     - Windows Command Exeuction - powershell
     - Microsoft Windows	
     - Signature	
     - 200003573
   * - 100000009	
     - Command Execution
     - Windows Command Exeuction - powershell
     - Microsoft Windows	
     - Signature	
     - 200003575
   * - 100000010	
     - Path Traversal
     - Path Traversal
     - All Systems	
     - Signature	
     - 200003055
   * - 100000010	
     - Path Traversal
     - Path Traversal
     - All Systems	
     - Signature	
     - 200003054
   * - 100000011	
     - Predictable Resource Location
     - Predictable Resource Location
     - All Systems	
     - Signature	
     - 200001404
   * - 100000012	
     - HTTP Protocol Compliance
     - Null in request
     - All Systems	
     - Violation	
     - HTTP protocol compliance - Null in request
   * - 100000013	
     - Detection Evasion
     - Alternative Datastream Access
     - Microsoft Windows	
     - Signature	
     - 200001404
   * - 100000014	
     - Insecure Deserialization
     - Insecure Deserialization - node.js
     - node.js	
     - Signature	
     - 200004283
   * - 100000014	
     - Insecure Deserialization
     - Insecure Deserialization - node.js
     - node.js	
     - Signature	
     - 200004282
   * - 100000014	
     - Insecure Deserialization
     - Insecure Deserialization - node.js
     - node.js	
     - Signature	
     - 200004284
   * - 100000015	
     - Insecure Deserialization
     - Insecure Deserialization - PHP
     - PHP	
     - Signature	
     - 200004189
   * - 100000015	
     - Insecure Deserialization
     - Insecure Deserialization - PHP
     - PHP	
     - Signature	
     - 200004188
   * - 100000015	
     - Insecure Deserialization
     - Insecure Deserialization - PHP
     - PHP	
     - Signature	
     - 200004190
   * - 100000016	
     - Information Leakage
     - Illegal Method TRACE
     - All systems	
     - Violation	
     - Illegal Method
   * - 100000017	
     - JSON Parser Attack
     - Malformed JSON
     - All systems	
     - Violation	
     - Malformed JSON data
   * - 100000018	
     - XML Parser Attack
     - Malformed XML
     - All systems	
     - Violation	
     - Malformed XML data
   * - 100000019	
     - HTTP Parser Attack
     - Cookie not RFC-compliant
     - All systems	
     - Violation	
     - Cookies - not RFC-compliant
   * - 100000020	
     - HTTP Parser Attack
     - Cookie not RFC-compliant
     - All systems	
     - Violation	
     - Cookies - not RFC-compliant
   * - 100000021	
     - HTTP Parser Attack
     - Wrong HTTP Protocol Version
     - All systems	
     - Violation	
     - HTTP protocol compliance failed
   * - 100000022	
     - HTTP Request Smuggling
     - HTTP Desync Attack Attempt
     - All systems	
     - Signature	
     - 200018061
   * - 100000023	
     - Server Side Request Forgery
     - SSRF attempt (AWS Metadata Server)
     - All systems	
     - Signature	
     - 200018040
   * - 100000024	
     - Server Side Request Forgery
     - SSRF attempt - Local network IP range 10.x.x.x
     - All systems	
     - Signature	
     - 200020201

.. toctree::
   :maxdepth: 1
   :glob:

   lab1
   lab2
   lab3
   