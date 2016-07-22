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
       
   Invalid Login
    Input Text    //input[@name='username']    ${InvalidUser}
    Input Text    //input[@name='password']    ${InvalidPassword}
    Click Element    //button[contains(.,'login')]
       
   Valid Login
    Input Text    //input[@name='username']    ${ValidUser}
    Input Text    //input[@name='password']    ${ValidPassword}
    Click Element    //button[contains(.,'login')]
      
   Navigate To Kamulist
    Click Element    //a[@href='/kamulist']
    
  Set Version
    Click Element    //a[@href='/kamulist/00-00-00-00-00-01']
    Click Element    //option[contains(.,'0.4.4')]
    Click Element    //option[contains(.,'0.4.4')]
    
  Check Version
    Click Element    //a[@href='/kamulist']
    
  Resize
    Click Element    //a[@href='/status']
    Set Window Size    ${440}    ${700}
    Click Element    //a[@href='/download']
    Click Element    //option[contains(.,'2016')]
    Click Element    //option[contains(.,'July')]
    
  Logout and Close
    Click Element    //a[contains(.,'Logout')]
    Sleep    1
    Close Browser
