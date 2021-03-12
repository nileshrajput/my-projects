
import requests
from bs4 import BeautifulSoup

r = requests.get('https://prefeitura.pbh.gov.br/saude/licitacao/pregao-eletronico-151-2020')
print(r)
soup = BeautifulSoup(r.text, 'html.parser')

publication_date=soup.select("span.col-sm-6.lbl-licitacao")
print(publication_date)

objectt=soup.select("span p")
print(objectt)

link=soup.select("div.field.field--name-field-icone.field--type-image.field--label-hidden.field__item")
print(link)
