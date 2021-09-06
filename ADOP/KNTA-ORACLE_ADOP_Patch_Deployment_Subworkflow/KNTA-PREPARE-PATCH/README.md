
Validation : KNTA-PREPARE-PATCH
Description: KNTA-PREPARE-PATCH
  
<img src="./KNTA-PREPARE-PATCH.PNG" width=800/>


<br>
<table>
<tr><td>Command</td><td><b>adop check status</b></td></tr>
<tr><td>Condition</td><td><pre></pre></td></tr>
<tr><td>Description</td><td></td></tr>
<tr><td>Timeout(s)</td><td>90</td></tr>
<tr><td>Enabled?</td><td>Yes</td></tr>
<tr><td>Steps</td>
<td><pre>

ksc_connect_dest_server
ksc_simple_respond "[WFI.P.ADOP_STATUS_CMD]" -hide "Enter the APPS password:" "[DEST_ENV.ENV.AC.OA_APPS_PASSWORD]"
ksc_exit
sc_knta_check_adop_status ADOP_COMMAND="[WFI.P.ADOP_STATUS_CMD]"

</pre></td></tr>
</table>
<br>
<table>
<tr><td>Command</td><td><b>adop prepare</b></td></tr>
<tr><td>Condition</td><td><pre></pre></td></tr>
<tr><td>Description</td><td></td></tr>
<tr><td>Timeout(s)</td><td>1800</td></tr>
<tr><td>Enabled?</td><td>Yes</td></tr>
<tr><td>Steps</td>
<td><pre>

ksc_connect_dest_server
```#verify it is in the expected status```
```#if it has already been set to Prepare assume can continue transtition```
ksc_simple_respond "[WFI.P.ADOP_PREPARE_CMD]" -hide "Enter the APPS password:" "[DEST_ENV.ENV.AC.OA_APPS_PASSWORD]" -hide "Enter the SYSTEM password:" "[DEST_ENV.ENV.AC.OA_SYSTEM_PASSWORD]" -hide "Enter the WLSADMIN password:" PasswordorPasswordToken
ksc_set MY_EXIT_CODE="[EXEC.EXIT_CODE]"
ksc_exit

sc_knta_check_adop_status ADOP_COMMAND="[WFI.P.ADOP_PREPARE_CMD]"

</pre></td></tr>
</table>