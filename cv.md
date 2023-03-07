
### Igor Prokhorchuk

#### Full Stack web developer

--- 


Contacts:

- phone: [+38(063) 992 65 65](tel:+38(063)9926565)
- email: [igor.prokhorchuk@yahoo.com](mailto:igor.prokhorchuk@yahoo.com)
- Github: [IgorProkhorchuk](https://github.com/IgorProkhorchuk)
- Discord: [IgorProkhorchuk](https://discord.com/channels/igorprokhorchuk#1619)
- LinkedIn: [Igor Prokhorchuk](https://www.linkedin.com/in/igorprohorchuk/)

##### Summary:

 Results-driven person with a solid technical background and experience in automation of logistics and supply chain processes. Being always on cutting edge of the IT technologies I set up my goal to change the field from project management in production to Web development, software engineering & cloud technologies. With a big passion to study I'm building my hard skills brick by brick in order to become a full stack guru.

| Hard skills: | Soft skills: |
| :----------- | :----------: |
| Linux, Bash, Python | Work from scratch  |
| IaC (Terraform, Ansible) | Analytical thinking |
| CI/CD (GitHub Actions, Jenkins) | Business planning |
| Cloud platforms: GCP & AWS | Time Management |
| MySQL | Lean & Kanban methodology |
| Networking, VPN | Leadership & motivation |
| Docker | |

###### Code example:

`#!/bin/bash
if [ $# -ne 2 ]; then
  echo "Usage: $0 source_directory backup_directory"
  exit 1
fi
source_dir="$1"
backup_dir="$2"
log_file="backup.log"
timestamp=$(date +"%Y-%m-%d %T")
rsync_command="rsync -avh --delete --log-file=$log_file $source_dir $backup_dir"
$rsync_command
new_files=$(grep "^>f" $log_file)
deleted_files=$(grep "^<f" $log_file)
if [ -n "$new_files" ]; then
  echo "$timestamp: Added files:" >> $log_file
  echo "$new_files" >> $log_file
fi
if [ -n "$deleted_files" ]; then
  echo "$timestamp: Deleted files:" >> $log_file
  echo "$deleted_files" >> $log_file
fi
crontab -l > mycron
echo "* * * * * $0 $source_dir $backup_dir" >> mycron
crontab mycron
rm mycron`

### Experience

####Project manager, __Aptiv__
a global technology company, automotive industry 
December 2020 to present time (2 years, 2 months) 

Work from scratch – from empty premises to a working manufacturing plant. Implemented SOP,  Lean manufacturing, WMS system (DCIx) for logistic department. Work on continuous  delivery with the new SOPs and features in order to improve mateerial flow and reduce
mistakes.


### Education

__National technical university "Kharkiv polytechnical institute"__
- International economy, Master's degree.

##### Courses:
- AWS Cloud practitioner, AWS, 
- Cloudskillboost, Google,
- IT Fundamentals,  EPAM.
- JavaScript/Front-end, RSSChool - in process

##### Activities & interests

- TRIZ theory
- Lean philosophy
- Foreign literature in origin
- Running & World cycling

##### Additional information:
English - __B2__ ([certificate](https://www.efset.org/cert/UrgDgR))