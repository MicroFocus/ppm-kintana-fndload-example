
Special Command : sc_knta_transfer_content_to_dest 
Description: sc_knta_transfer_content_to_dest
  
<img src="./sc_knta_transfer_content_to_dest_parameters.PNG" width=800/>
Parameter Name    Default Token
<pre>
FILESYSTEM              [FILESYSTEM]
</pre>

<img src="./sc_knta_transfer_content_to_dest_commands.PNG" width=800/>

Commands:

<table>
<tr><td>Command</td><td><b>Special command sc_knta_transfer_content_to_dest</b></td></tr>
<tr><td>Condition</td><td></td></tr>
<tr><td>Description</td><td></td></tr>
<tr><td>Enabled?</td><td>Yes</td></tr>
<tr><td>Steps</td>
<td><pre>

```ksc_comment '<font color="blue">*********************************<br><b>Special Command: sc_knta_transfer_content_to_dest</b><br>DEST File System: [FILESYSTEM]<br>Environment: [WFS.DEST_ENVIRONMENT_NAME]<br>App code: [P.P_APP_SHORT_NAME]<br>copying content bundle<br>*********************************</font>'```

</pre></td></tr>
</table>

<BR>

<table>
<tr><td>Command</td><td><b>transfer content to dest</b></td></tr>
<tr><td>Condition</td><td></td></tr>
<tr><td>Description</td><td></td></tr>
<tr><td>Enabled?</td><td>Yes</td></tr>
<tr><td>Steps</td>
<td><pre>

ksc_connect_dest_server
```# use token passed for the path to EBSapps.env.  ```
. [DEST_ENV.ENV.SERVER_BASE_PATH]/EBSapps.env [FILESYSTEM]
echo $RUN_BASE | awk -F/ '{print $(NF)}'
ksc_set FS_EDITION_RUN="[EXEC.OUTPUT]"
echo $RUN_BASE
ksc_set FS_RUN_BASE="[EXEC.OUTPUT]"

sc_knta_set_fs_dest_base_path

ksc_exit

```ksc_comment '<font color="blue">copying content bundle from <b>[AS.BASE_URL][AS.PKG_TRANSFER_PATH][P.P_FILENAME]</b> to [DEST_ENV.SERVER_NAME] [P_APP_ACTUAL_FS_DEST_BASE_PATH]</font>'```
ksc_copy_server_server FILE_TYPE="BIN" SUB_PATH="" DEST_BASE_PATH="[P_APP_ACTUAL_FS_DEST_BASE_PATH]" SOURCE_BASE_PATH="[AS.PKG_TRANSFER_PATH]" FILENAME="[P.P_FILENAME]" SOURCE_ENV="[AS.SERVER_ENV_NAME]"
</pre></td></tr>
</table>