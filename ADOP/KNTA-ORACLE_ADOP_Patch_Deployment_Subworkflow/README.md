
Validation : KNTA-ORACLE ADOP Patch Deployment Subworkflow
Description: KNTA-ORACLE ADOP Patch Deployment Subworkflow
  
<img src="./KNTA-ORACLE ADOP Patch Deployment Subworkflow_layout.PNG" width=800/>
<img src="./KNTA-ORACLE ADOP Patch Deployment Subworkflow.PNG" width=800/>

Parameters

|Prompt|   Token                                          | Description                       | Default Value|
|--------------------|--------------------------------|-----------------------------|-------------------------------|
|CLEANUP_MODE|CLEANUP_MODE|After executing abort, full mode clean up should be run|full|
|ADOP_STATUS_CMD|ADOP_STATUS_CMD|adop status command used.|adop -status|
|ADOP_PREPARE_CMD|ADOP_PREPARE_CMD|adop prepare command used.|adop phase=prepare|
|ADOP_CLEANUP_CMD|ADOP_CLEANUP_CMD|adop cleanup command used.|adop phase=cleanup cleanup_mode=full|
|ADOP_ABORT_CMD|ADOP_ABORT_CMD|adop command used to abort the current patching cycle.|adop phase=abort|
|ADOP_CLONE_COMMAND|ADOP_CLONE_COMMAND|s_clone phase synchronizes the patch file system with the run file system.  options: force=no (default), yes|adop phase=fs_clone|
|ADOP_APPLY_CMD|ADOP_APPLY_CMD|adop apply command used.|adop phase=apply|
|ADOP_FINALIZE_CMD|ADOP_FINALIZE_CMD|adop finalize command used.|adop phase=finalize|
|ADOP_CUTOVER_CMD|ADOP_CUTOVER_CMD||adop phase=cutover cm_wait=5|