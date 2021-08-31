# ppm-kintana-fndload-example

DISCLAIMER OF WARRANTY 
This example of PPM workflows, object types, validaitons, special commands is provided as a courtesy, free of charge, "AS-IS" by Micro Focus International plc ("Micro Focus"). Micro Focus shall have no obligation to maintain or support these changes. Micro Focus MAKES NO EXPRESS OR IMPLIED WARRANTY OF ANY KIND REGARDING THESE INSTRUCTIONS. Micro Focus SHALL NOT BE LIABLE FOR ANY DIRECT, INDIRECT, SPECIAL, INCIDENTAL OR CONSEQUENTIAL DAMAGES, WHETHER BASED ON CONTRACT, TORT OR ANY OTHER LEGAL THEORY, IN CONNECTION WITH OR ARISING OUT OF THE FURNISHING, PERFORMANCE OR USE OF THESE INSTRUCTIONS.

Please note : This example describes a PPM/Kintana Object Type and supporting objects calling Oracle's FNDLOAD and other utilities.   All Oracle utlities are subject to Oracle's terms of use.

Oracle knowledge References :

https://blogs.oracle.com/prajkumar/oracle-fndload-scripts [1]<BR>
https://docs.oracle.com/cd/E26401_01/doc.122/e22961.pdf [2]<BR>
https://docs.oracle.com/cd/E18727_01/doc.121/e12148/T531058T531061.htm [3]<BR>
https://docs.oracle.com/cd/E26401_01/doc.122/e22954/T202991T531065.htm [4]<BR>

  
Background:
  
This example has been created for Micro Focus PPM/Kintana to assist in their migration of Oracle's AOL objec types.  Most customer's have created their own object types, to perform these activity.  This is one of the reason it has yet to be added OOTB.  
  
custom type     |   link to details                                           | summary  
special command | <a href='./sc_knta_download/README.md'>sc_knta_download</a> | used to call FNDLOAD DOWNLOAD
special command | <a href='./sc_knta_upload/README.md'>sc_knta_download</a>   | used to call FNDLOAD UPLOAD
  
