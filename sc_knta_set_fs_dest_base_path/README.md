
Special Command : sc_knta_set_fs_dest_base_path 
Description: sets the DEST BASE_PATH based on active filesystem
  
<img src="./sc_knta_set_fs_dest_base_path_parameters.PNG" width=800/>
Parameter Name    Default Token

<BR>

<img src="./sc_knta_set_fs_dest_base_path_commands.PNG" width=800/>

Commands:

Command: <b>set fs base path</b> <BR>
Steps:
```
echo '<font color="blue">*********************************<br><b>Special Command: sc_knta_set_fs_dest_base_path</b><br>The <b>[P.P_EBSAPPLY]</b> file system is on <b>[FS_EDITION_RUN]</b>.<br>Environment: [WFS.DEST_ENVIRONMENT_NAME]<br>App code: [P.P_APP_SHORT_NAME]<br>*********************************</font>'
```
<BR>
Command: <b>fs1 check</b><BR>
Condition: <pre>'[FS_EDITION_RUN]'='fs1'</pre><BR>
Description: FS1 check <BR>

Steps:
```
ksc_set P_APP_ACTUAL_FS_DEST_BASE_PATH=[ENV="[WFS.DEST_ENVIRONMENT_NAME]".APP="[P.P_APP_SHORT_NAME]".UD.FS1]
echo 'Setting the FS PATH to : '[P_APP_ACTUAL_FS_DEST_BASE_PATH]
```

<BR>
Command: <b>fs2 check</b><BR>
Condition: <pre>'[FS_EDITION_RUN]'='fs2'</pre><BR>
Description: FS2 check <BR>

Steps:
```
ksc_set P_APP_ACTUAL_FS_DEST_BASE_PATH=[ENV="[WFS.DEST_ENVIRONMENT_NAME]".APP="[P.P_APP_SHORT_NAME]".UD.FS2]
echo 'Setting the FS PATH to : '[P_APP_ACTUAL_FS_DEST_BASE_PATH]
```