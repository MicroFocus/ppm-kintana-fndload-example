
Validation : validation_KNTA - Responsibilities
Description: validation_KNTA - Responsibilities
  
<img src="./validation_KNTA - Responsibilities.PNG" width=800/>

Commands:<BR>
<table>
<tr><td>Command</td><td><b>Get Responsibilities</b></td></tr>
<tr><td>Condition</td><td><pre>'[SOURCE_ENV.ENV.ENVIRONMENT_NAME]' NOT LIKE 'SCM_%'</pre></td></tr>
<tr><td>Description</td><td></td></tr>
<tr><td>Timeout(s)</td><td>90</td></tr>
<tr><td>Enabled?</td><td>Yes</td></tr>
<tr><td>Steps</td>
<td><pre>

ksc_connect_source_server
. [SOURCE_ENV.ENV.SERVER_BASE_PATH]/EBSapps.env [P.P_DOWNLOAD_FROM]
echo $RUN_BASE | awk -F/ '{print $(NF)}'
ksc_set FS_EDITION_RUN="[EXEC.OUTPUT]"
echo $RUN_BASE
ksc_set FS_RUN_BASE="[EXEC.OUTPUT]"

ksc_set [QUERY_STRING]="[EXEC.OUTPUT]"
export driver=validationGetResponsiblities.sql
```#set colsep "#@#"```
```echo 'set colsep "#@#"' > $driver```
echo 'set trimspool on' > $driver
echo 'set heading off' >> $driver
echo 'set headsep off' >> $driver
echo 'set termout off' >> $driver
echo 'spool [SYS.USER_ID]RESP.txt' >> $driver
echo "select fr.responsibility_name, fr.description from fnd_responsibility_vl fr, fnd_application_vl fa where fr.application_id = fa.application_id and fa.application_short_name ='[VP.P_APP_SHORT_NAME]';" >> $driver
echo "spool off" >> $driver
echo 'exit;' >> $driver

cat $driver

sqlplus [SOURCE_ENV.DB_USERNAME]/[SOURCE_ENV.DB_PASSWORD]@[SOURCE_ENV.DB_CONNECT_STRING] @$driver

ksc_capture_output cat  [SYS.USER_ID]RESP.txt

ksc_exit


</pre></td></tr>
</table>
<br>

<table>
<tr><td>Command</td><td><b>Get Responsiblity from SCM</b></td></tr>
<tr><td>Condition</td><td><pre>'[SOURCE_ENV.ENV.ENVIRONMENT_NAME]' LIKE 'SCM_%'</pre></td></tr>
<tr><td>Description</td><td></td></tr>
<tr><td>Timeout(s)</td><td>90</td></tr>
<tr><td>Enabled?</td><td>Yes</td></tr>
<tr><td>Steps</td>
<td><pre>

ksc_connect_source_server

ksc_capture_output echo [P.P_SING_RESP]

ksc_exit

</pre></td></tr>
</table>