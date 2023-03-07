
# Igor Prokhorchuk

## Full Stack web developer

--- 


#### Contacts:

- phone: [+38(063) 992 65 65](tel:+38(063)9926565)
- email: [igor.prokhorchuk@yahoo.com](mailto:igor.prokhorchuk@yahoo.com)
- Github: [IgorProkhorchuk](https://github.com/IgorProkhorchuk)
- Discord: [IgorProkhorchuk](https://discord.com/channels/igorprokhorchuk#1619)
- LinkedIn: [Igor Prokhorchuk](https://www.linkedin.com/in/igorprohorchuk/)

### <div align="center">Summary:</div>

 Results-driven person with a solid technical background and experience in automation of logistics and supply chain processes. Being always on cutting edge of the IT technologies I set up my goal to change the field from project management in production to Web development, software engineering & cloud technologies. With a big passion to study I'm building my hard skills brick by brick in order to become a full stack guru.

 ---

| Hard skills: | Soft skills: |
| :----------- | :----------- |
| Linux, Bash, Python | Work from scratch  |
| IaC (Terraform, Ansible) | Analytical thinking |
| CI/CD (GitHub Actions, Jenkins) | Business planning |
| Cloud platforms: GCP & AWS | Time Management |
| MySQL | Lean & Kanban methodology |
| Networking, VPN | Leadership & motivation |
| Docker | |

---

###### Code example:

```
import requests
import csv
import openpyxl
from bs4 import BeautifulSoup
from urllib.parse import urljoin

# Create user agent

headers = {
  'User-Agent': 'Mozilla/5.0 (Windows NT 10.0; rv:91.0) Gecko/20100101 Firefox/91.0'
}

# target url

URL = "https://fayni-recepty.com.ua/recepty/pershi-stravy/"
first_dishes_name = []
print(URL)

# Going throw all pages

while True:
  site_page = requests.get(URL, headers=headers)
  soup = BeautifulSoup(site_page.content, "html.parser")

  first_dishes = soup.find_all("h2", class_="entry-title")
  for dish in first_dishes:
    dish_name = dish.a.text
    first_dishes_name.append(dish_name)

  next_page = soup.select_one('a.next')

  if next_page:
    next_url = next_page.get('href')
    URL = urljoin(URL, next_url)
  else:
    break

# Create and write results into .csv file

with open('pershi-stravy.csv', 'w', newline='') as csv_file:
  csv_writer = csv.writer(csv_file)
  csv_writer.writerow(['name'])

# Create and write results into .xlsx file

excel_file = openpyxl.Workbook()
excel_writer = excel_file.active
excel_writer['A1'] = 'name'

for first_dish in first_dishes_name:
  excel_writer.append([first_dish])

excel_file.save('ershi-stravy.xlsx')
```

---


### Experience

#### Project manager, __Aptiv__

_a global technology company, automotive industry_

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