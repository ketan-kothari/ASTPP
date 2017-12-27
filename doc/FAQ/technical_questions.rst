=========
Technical Questions
=========

  1. What databases are supported in ASTPP ?
      It supports only MySQL (PostgreSQL support will be added in future release).
   
   
  2. What payment gateways are supported in ASTPP ?
      Paypal only for now.


  3. Does ASTPP support Multi-language ?
      No


  4. Does ASTPP current version support callshop?
      No. It will be included in future releases. To get more information you can contact us at sales@inextrix.com.


  5. How can I update my source from to keep it update to date?
      ASTPP provides update.sh script with its source just run that script to update your source.


  6. When I go to login page, rather WEBUI I get long list of php contents.
      Enable short_open_tag in php.ini and then restart apache.


  7. Why I am not able to register extensions after installation?
      Make sure you have configured your IP in Sip Profile and your registration request is reaching to server.


  8. How to verify if ASTPP and FreeSWITCH communicating properly?
      Default sip profile must be loaded in FreeSWITCH


  9. While login I am getting “Unable to connect to your database server using the provided settings” error.
      Please check your database credentials. ASTPP uses /var/lib/astpp/astpp-config.conf file for database connection.


  10. How can I do IP Authentication for my customers?
       Configure your customer IP under Customers -> IP Settings


  11. Does CDRs report will show all data ?
       No, CDRs report will only record of current day. If you want to see record of previous days record then you need 
       to search.
       
       
  12. How to connect freeswitch fs_cli console from linux server ?
      #fs_cli or fs_cli -p123456 (if you have set even_socket password)


  13. How to change event socket password in freeswitch ?
        Open below file and replace your password with “ClueCon”.
        File path : /usr/local/freeswitch/conf/autoload_configs/event_socket.conf.xml
        Go to fs_cli console and reload it. freeswitch> reload mod_event_socket
        
  14. If we are getting origination rates not found error in fs_cli console then what to do ?
      [WARNING] mod_dptools.c:1724 Accountcode 2457848300. Dialed number (3318555801802)  origination rates not found!!
        Add origination rate for prefix 33 and select rategroup which assigned to customer.
        
  15.If we are getting origination rates not found error in fs_cli console then what to do ?
     [WARNING] mod_dptools.c:1724 Accountcode 2457848300. Dialed number (3318555801802) termination rates not found!!
       Add termination rate for prefix 33 and select trunk which selected in rate group
       Or select approprie trunk in rategroup which assigned to customer.
