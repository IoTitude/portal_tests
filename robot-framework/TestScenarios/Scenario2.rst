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
       
   Try To Login
    Invalid Login
    
   Successful Login
    Valid Login
      
  To Kamulist
    Navigate To Kamulist 
    
  Set Version
    Click Element    //a[@href='/kamulist/00-00-00-00-00-01']
    Click Element    //option[contains(.,'0.4.4')]
    Click Element    //option[contains(.,'0.4.4')]
    
  Check Version
    Navigate To Kamulist
    
  Resize and Download
    Navigate To Status
    Navigate To Download
    
  Logout and Close
    Logout
    Sleep    1
    Close Browser
