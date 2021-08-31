
Validation : validation_KNTA - Oracle Applicaitons
Description: validation_KNTA - Oracle Applicaitons
  
<img src="./validation_KNTA - Oracle Applicaitons.PNG" width=800/>

Commands:<BR>
<table>
<tr><td>Command</td><td><b>Get Application List</b></td></tr>
<tr><td>Condition</td><td></td></tr>
<tr><td>Description</td><td></td></tr>
<tr><td>Timeout(s)</td><td>90</td></tr>
<tr><td>Enabled?</td><td>Yes</td></tr>
<tr><td>Steps</td>
<td><pre>

sc_knta_run_sql QUERY_STRING="select fa.application_short_name, fa.application_short_name, fa.application_name, fa.basepath  from fnd_application_vl fa" & " where fa.application_short_name like UPPER(" & "'" & "[PKG.PKGL.P_APP_SHORT_NAME]" & "') order by fa.application_name" DELIMITER="#!#" ENV_NAME="[SOURCE_ENV.ENVIRONMENT_NAME]" FILENAMEPATH="[AS.PKG_TRANSFER_PATH][SYS.USER_ID]APP.txt"
ksc_capture_output cat [AS.PKG_TRANSFER_PATH][SYS.USER_ID]APP.txt


</pre></td></tr>
</table>
