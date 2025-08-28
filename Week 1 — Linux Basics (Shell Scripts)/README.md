week-01-linux-basics/day01_file_ops.sh
#!/bin/bash
# Day 1: Linux File Operations Practice

mkdir -p cloud_project/{scripts,logs,data}
echo "Hello Generative AI World!" > cloud_project/data/sample.txt

echo "Directory structure created:"
ls -R cloud_project/


week-01-linux-basics/day02_grep_find.sh

#!/bin/bash
# Day 2: Grep & Find practice

echo -e "INFO Start\nERROR Something broke\nINFO End" > app.log

echo "Extract ERROR lines:"
grep "ERROR" app.log

echo "Find log files in current folder:"
find . -name "*.log"


week-01-linux-basics/day03_permissions.sh

#!/bin/bash
# Day 3: Permissions

touch secret.txt
chmod 600 secret.txt
ls -l secret.txt


week-01-linux-basics/day04_process_mgmt.sh

#!/bin/bash
# Day 4: Process Management

echo "Running background process..."
sleep 60 &
ps -ef | grep sleep


week-01-linux-basics/day05_networking.sh

#!/bin/bash
# Day 5: Networking Basics

ping -c 2 google.com
curl -I https://aws.amazon.com


week-01-linux-basics/day06_archive.sh

#!/bin/bash
# Day 6: Archiving

mkdir demo
echo "file1" > demo/f1.txt
echo "file2" > demo/f2.txt

tar -czvf demo.tar.gz demo/


week-01-linux-basics/day07_backup_to_s3.sh

#!/bin/bash
# Day 7: Backup to AWS S3

aws s3 mb s3://my-genai-practice-bucket-$(date +%s)
aws s3 cp demo.tar.gz s3://my-genai-practice-bucket-$(date +%s)/
