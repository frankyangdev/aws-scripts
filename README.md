# aws-scripts
scripts for AWS back-end management
This repository for AWS scripts with Python Boto3 to do regular EC2 EBS backup and other common instance operation

1. ec2-ebs-delete-snapshos.py
This script has been tested and will delete ebs snapshot over 15 days old.

This script is written with Python and applied in lamda function and set triggerged schedule cronjob in cloudwatch.
i.e Schedule Cron expression 55 18 28 * ? *  every 28 days to delete snapshots of older 15 days  

2. ec2-ebs-snapshot-backup.py
This script has been tested and will create ebs snapshot according to tags' value I have set in ebs volume, only create snapshots for those tags with Key = Backup and Value = Yes
This script is written with Python and applied in lamda function and set triggerged schedule cronjob in cloudwatch.

i.e Schedule Cron expression 55 16 */10 * ? *  every 10 days to create ebs snapshots






