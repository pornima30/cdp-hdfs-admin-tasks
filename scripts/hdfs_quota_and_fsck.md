## HDFS Quota and Space Quota Management

```bash
# Upload large dataset
wget https://raw.githubusercontent.com/tbertinmahieux/MSongsDB/master/Tasks_Demos/CoverSongs/shs_dataset_test.txt
hdfs dfs -put shs_dataset_test.txt /data

# Set namespace quota
hdfs dfsadmin -setQuota 3 /data

# Set space quota
hdfs dfsadmin -setSpaceQuota 319520 /data

# Clear quotas
hdfs dfsadmin -clrQuota /data
hdfs dfsadmin -clrSpaceQuota /data

# View usage
hdfs dfs -count -q -h /data
