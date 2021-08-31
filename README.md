# ppm-kintana-fndload-example

DISCLAIMER OF WARRANTY 
This example of PPM workflows, object types, validaitons, special commands is provided as a courtesy, free of charge, "AS-IS" by Micro Focus International plc ("Micro Focus"). Micro Focus shall have no obligation to maintain or support these changes. Micro Focus MAKES NO EXPRESS OR IMPLIED WARRANTY OF ANY KIND REGARDING THESE INSTRUCTIONS. Micro Focus SHALL NOT BE LIABLE FOR ANY DIRECT, INDIRECT, SPECIAL, INCIDENTAL OR CONSEQUENTIAL DAMAGES, WHETHER BASED ON CONTRACT, TORT OR ANY OTHER LEGAL THEORY, IN CONNECTION WITH OR ARISING OUT OF THE FURNISHING, PERFORMANCE OR USE OF THESE INSTRUCTIONS.

Please note : This example describes a PPM/Kintana Object Type and supporting objects calling Oracle's FNDLOAD and other utilities.   All Oracle utlities are subject to Oracle's terms of use.

<b>Oracle knowledge References :</b>

https://blogs.oracle.com/prajkumar/oracle-fndload-scripts [1]<BR>
https://docs.oracle.com/cd/E26401_01/doc.122/e22961.pdf [2]<BR>
https://docs.oracle.com/cd/E18727_01/doc.121/e12148/T531058T531061.htm [3]<BR>
https://docs.oracle.com/cd/E26401_01/doc.122/e22954/T202991T531065.htm [4]<BR>

Please send feedback or questions: to christopher.hangl@microfocus.com

<b>FAQ:</b>

1. Is there exports of the entities?  No, we are not providing exports of the enities types.  If you want to use a variation of this example, please create and manage your own custom entites.
  
<b>Background:</b>
  
This example has been created for Micro Focus PPM/Kintana to assist in their migration of Oracle's AOL objec types.  Most customer's have created their own object types, to perform these activity.  This is one of the reason it has yet to be added OOTB.  
  
|custom kintana type |   link to details                                           | summary                       |
|--------------------|-------------------------------------------------------------|-------------------------------|
|special command     | <a href='./sc_knta_download/README.md'>sc_knta_download</a> | used to call FNDLOAD DOWNLOAD |
|special command     | <a href='./sc_knta_set_fs_source_base_path/README.md'>sc_knta_set_fs_source_base_path</a> | sc_knta_set_fs_source_base_path  |
|special command     | <a href='./sc_knta_upload/README.md'>sc_knta_upload</a>     | used to call FNDLOAD UPLOAD   |
|special command     | <a href='./sc_knta_transfer_content_to_dest/README.md'>sc_knta_transfer_content_to_dest</a>| sc_knta_transfer_content_to_dest|  
|special command     | <a href='./sc_knta_set_fs_dest_base_path/README.md'>sc_knta_set_fs_dest_base_path</a>| sc_knta_set_fs_dest_base_path|
|special command     | <a href='./sc_knta_default_filename/README.md'>sc_knta_default_filename</a>| sc_knta_default_filename|
|validation          | <a href='./validation_EBSAPPLY/README.md'>validation EBSAPPLY</a>| validation EBSAPPLY|
|validation          | <a href='./validation_KNTA - Responsibilities/README.md'>validation KNTA - Responsibilities</a>| validation KNTA - Responsibilities|
|validation          | <a href='./validation_KNTA - Oracle Applicaitons/README.md'>validation_KNTA - Oracle Applicaitons</a>| validation_KNTA - Oracle Applicaitons|
|user data          | <a href='./environment_user_data/README.md'>environment_user_data</a>| environment user data|
|object type          | <a href='./object_type_KNTALOADResponsiblity/README.md'>KNTALOAD Responsiblity</a>| KNTALOAD Responsiblity|




Also including example testing with ADOP

|custom kintana type |   link to details                                           | summary                       |
|--------------------|-------------------------------------------------------------|-------------------------------|
|workflow            | <a href='./ADOP/KNTA-ORACLE ADOP Patch Deployment Subworkflow/README.md'>KNTA-ORACLE ADOP Patch Deployment Subworkflow</a> | KNTA-ORACLE ADOP Patch Deployment Subworkflow |
|workflow step       |
|workflow step      |
|workflow step     |
|workflow step      |
|workflow step       |
