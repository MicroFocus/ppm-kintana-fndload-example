
Validation : KNTA-CLONE-PATCH
Description: KNTA-CLONE-PATCH
  
<img src="./KNTA-CLONE-PATCH.PNG" width=800/>


<br>
<table>
<tr><td>Command</td><td><b>Transfer content to destination patch file location</b></td></tr>
<tr><td>Condition</td><td><pre></pre></td></tr>
<tr><td>Description</td><td></td></tr>
<tr><td>Timeout(s)</td><td>360</td></tr>
<tr><td>Enabled?</td><td>Yes</td></tr>
<tr><td>Steps</td>
<td><pre>

ksc_connect_dest_server
ksc_simple_respond "[WFI.P.ADOP_CLONE_CMD]" -hide "Enter the APPS password:" "[DEST_ENV.ENV.AC.OA_APPS_PASSWORD]" -hide "Enter the SYSTEM password:" "[DEST_ENV.ENV.AC.OA_SYSTEM_PASSWORD]" -hide "Enter the WLSADMIN password:" passwordorPasswordToken
ksc_set MY_EXIT_CODE="[EXEC.EXIT_CODE]"
ksc_exit

sc_knta_check_adop_status ADOP_COMMAND="[WFI.P.ADOP_CLONE_CMD]"

</pre></td></tr>
</table>