.. default-role:: code

============
Scenario 2
============

Browser: Firefox


.. contents:: Table of contents
   :local:
   :depth: 2

=================
Scenario 2 Tests
=================



.. code:: robotframework

   *** Settings ***
   Resource 		resources.txt



.. code:: robotframework

   *** Test Cases ***
   Open Portal
       Open browser To Login Page
       
.. code:: robotframework

   *** Test Cases ***
   Try To Login
    Invalid Login
    
.. code:: robotframework

   *** Test Cases ***
   Successful Login
    Valid Login
      
.. code:: robotframework

   *** Test Cases ***
  To Kamulist
    Navigate To Kamulist 
    
.. code:: robotframework

   *** Test Cases ***
  Set Version
    Click Element    //a[@href='/kamulist/00-00-00-00-00-01']
    Click Element    //option[contains(.,'0.4.4')]
    Click Element    //option[contains(.,'0.4.4')]
    
    
.. code:: robotframework

   *** Test Cases ***
  Check Version
    Navigate To Kamulist
    
.. code:: robotframework

   *** Test Cases ***
  Resize and Download
    Navigate To Status
    Navigate To Download
    
    
.. code:: robotframework

   *** Test Cases ***
  Logout and Close
    Logout
    Sleep    1
    Close Browser
