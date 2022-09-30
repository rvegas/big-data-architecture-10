## BIG DATA ARCHITECTURE IX

En este módulo las clases estan distribuidas utilizando notebooks de Python 
alojados en Google Colaboratory.


## Solucion Posible a la practica:
  

## Links importantes

- Link a la práctica: [practica](https://docs.google.com/document/d/15GgimXmPYFlNCdjoilp-9z6Q0HCjK0LQfmiG5FjIE9A/edit#heading=h.gjdgxs)


## Trabajando en Docker con Windows
  
Recomendado bajarse/comprar windows 10 Pro para trabajar de manera más cómoda con docker 
y otras cosas, podéis conseguirlo [aquí](https://www.amazon.es/Windows-Pro-Bits-Electr%C3%B3nico-Instrucciones/dp/B07QKJT53N/ref=sr_1_3?__mk_es_ES=%C3%85M%C3%85%C5%BD%C3%95%C3%91&keywords=windows+10+pro&qid=1575994695&sr=8-3): 
  
### Si trabajas en Windows, te recomiendo instalar el subsistema de Ubuntu:
  
- https://blogs.msdn.microsoft.com/commandline/2016/04/06/bash-on-ubuntu-on-windows-download-now-3/
  
- https://docs.microsoft.com/es-es/windows/wsl/install-win10
  
### Si tenéis problemas con docker en ciertas versiones de Windows, se recomienda lo siguiente en orden:

- Habilitar "Switch to Linux containers" en Docker (en logo de docker->"Cambiar a contenedores Linux")
  
- Habilitar los features experimentales de docker (en logo de docker->opciones->avanzado)
  
- Trabajar con un Powershell con permisos de administrador (Click derecho sobre el logo y ejecutar como Administrador)
  
#### Si llegarais a tener el problema con docker en el que no se ejecutan los contenedores y no salen errores:
  
- Intentad lo comentado en este issue de github: https://github.com/microsoft/WSL/issues/4694#issuecomment-556095344

- Editad `C:/Users/XXX/.wslconfig` y colocad dentro (donde XXX es vuestro usuario de windows):  
```
[wsl2]
kernelCommandLine = vsyscall=emulate
```
  
## Conseguir Datasets:
  
- https://kaggle.com  
- https://public.opendatasoft.com
  
    
## Libros y Articulos recomendados
  
### Libros

- Top Tier
  -  [The pragmatic programmer](https://www.amazon.es/Pragmatic-Programmer-journey-mastery-Anniversary/dp/0135957052)
  -  [Clean Architecture](https://www.amazon.es/Arquitectura-limpia-especialistas-estructura-Especiales/dp/8441539901)
  -  [Architecting Modern Data Platforms](https://www.amazon.es/Architecting-Modern-Data-Platforms-Enterprise-ebook/dp/B07L9JDXM8)

- Intermedio
  -  [Hadoop: The definitive guide](https://www.amazon.es/Hadoop-Definitive-Guide-Tom-White/dp/1491901632/ref=sr_1_1?__mk_es_ES=%C3%85M%C3%85%C5%BD%C3%95%C3%91&keywords=hadoop&qid=1576859032&sr=8-1)
  -  [Hadoop: The definitive guide online](https://www.oreilly.com/library/view/hadoop-the-definitive/9781491901687/ch04.html)
  -  [Python Machine Learning](https://www.amazon.es/Python-machine-learning-Mirjalili-Vahid/dp/8426727204/ref=sr_1_1?__mk_es_ES=%C3%85M%C3%85%C5%BD%C3%95%C3%91&crid=O3KR2N81PQR0&keywords=sebastian+raschka&qid=1576858947&sprefix=sebastian+ra%2Caps%2C175&sr=8-1)


### Articulos / blogs
  
- https://www.slideshare.net/mcsrivas/design-scale-and-performance-of-maprs-distribution-for-hadoop
- https://hadoop.apache.org/docs/r1.2.1/hdfs_design.html
- https://www.todaysoftmag.com/article/1358/hadoop-mapreduce-deep-diving-and-tuning
- https://tdwi.org/articles/2017/10/16/arch-all-data-lake-manifesto-10-best-practices.aspx
- https://stackoverflow.com/questions/22769129/differences-between-hadoop-jar-and-yarn-jar
- https://www.reddit.com/r/bigdata/
- https://datafloq.com/
- https://www.dataversity.net/category/data-topics/big-data/ 
  

### Certificaciones Cloud
  
- Recomendado para estudiar:
  - https://www.linuxacademy.com
  - https://www.qwiklabs.com/
- Mejor certificacion para empezar:
  - https://aws.amazon.com/certification/certified-cloud-practitioner/
- Segundo nivel:
  - https://cloud.google.com/certification/cloud-engineer
  - https://aws.amazon.com/es/certification/certified-solutions-architect-associate/
- Tercer nivel:
  - https://cloud.google.com/certification/cloud-architect
  - https://aws.amazon.com/certification/certified-solutions-architect-professional/
- Reto para sacarse la GCP Cloud Engineer y ganar 100$ de premio en la google store:
  - https://cloud.google.com/blog/topics/training-certifications/get-google-cloud-certified-in-3-months
  

## Notebooks

Los notebooks en orden de cada sesión estan aquí, **OJO**: Cada clase utilizaremos 
material externo como Google Collaboratory para facilitar las clases, así como 
repositorios y presentaciones powerpoint alojadas fuera de gitlab. 
Este README se irá actualizando con la información que vayamos cubriendo cada día.
  
  
### DIA 1
  
- INTRO: [Mapa de conceptos y calendario]  
https://colab.research.google.com/drive/12_Af6n5KmpnWuj_Ni_DnVqkYsLFXTo9q
- ARQUITECTURA: [Intro a Arquitectura]
https://colab.research.google.com/drive/1_LTnLRG5EANOdct-uJx6g3lVAl6PdYS2?usp=sharing  
- DATA 1: [Intro a Datos]  
https://colab.research.google.com/drive/1-FpEbJ-6ZzsiYoVFXqOwl56LTC53s9Va  
- CRAWLING: [Usando scrapy para obtener datos]  
https://colab.research.google.com/drive/1VDcjf-Tk69ZuNbx0hJdh_H6ZyccoRzsb  
  
  
### DIA 2
  
- SCRAPING: [Usando python requests para llamar a APIs]  
https://colab.research.google.com/drive/1lGfM-2fj1aa7bOIDFlYWOfdtXduuxXuv  
- CLOUD 1: [Intro Rapida]  
https://colab.research.google.com/drive/1h6YStd7B0_SsGyFoI5JRca7LzLTeLzBF  
- Bases de datos Cloud:  
https://colab.research.google.com/drive/1o0X2dpDMJT6vv6aj9uef7obUMDkr3CiH  
  
  
### DIA 3
  
- Bases de Datos 1: [NoSQL vs SQL]  
**PRESENTACION**: https://docs.google.com/presentation/d/1cHlnB-CumQhPT52phFLtdqp-NL2P3yI372wLoc0l3pA  
**PRACTICA**: https://colab.research.google.com/drive/1GJz8sMerq_wfl574NZUEsa-xugv7FQ7r?usp=sharing 


### DIA 4
  
- Elastic Search:    
- Elastic y Kibana en la nube: https://colab.research.google.com/drive/1so11jurzTD2W5BRlz-Ozc5PoT28A94Wn  
  
    
### DIA 5 

- Elastic Search:    
**PRESENTACION**: https://docs.google.com/presentation/d/1NdtGyWRCsxyp6T__wLriMJDx3l61AVgaORV9nBdd2sA  
**PRACTICA**: https://colab.research.google.com/drive/1LcRwty_B3tn6LlabR2_kRvarB_5yiPBX  
  
- HADOOP: [Datalakes]  
https://colab.research.google.com/drive/1eC-oD_E_D-S1Y94nvtkSqJtMsUmc7w-y  
  
  
   
### DIA 6

- HADOOP 1: [HADOOP (HDFS)]  [registry.hub.docker.com/rvegas/hadoop-cluster:0.0.3]
https://colab.research.google.com/drive/1kfHF8HpDv2py33-ByDlz4yjWfRMWJkJB
- HADOOP 2: [YARN (YARN + colas)]  
https://colab.research.google.com/drive/14a_jUJwFG1AjBFr1zZY-w_nUjk9mreDG?usp=sharing    
- CLOUD 1: [Intro Rapida]  
https://colab.research.google.com/drive/1h6YStd7B0_SsGyFoI5JRca7LzLTeLzBF  
  
### DIA 7  

- CLOUD 2: [Montar un Hadoop en la nube]  
https://colab.research.google.com/drive/1C4vZpQmiw4ZimIIa7Hx4qbbTlZmtUMGN    
- CLOUD 3: [Dataproc - Jobs]  
https://colab.research.google.com/drive/1-h60zR9Jmk1l2Z5tb4yE-gQBGmu3F9jb
- HIVE: [Intro a HIVE]  
https://colab.research.google.com/drive/1ZdQ4gUvFBKvr6RJDbFMfBUJZJRWFNLit  
- HIVE II: [HIVE + Python + Cloud]  
https://colab.research.google.com/drive/1OqdMecXdqnDa6J2FR0DOqRqzB2pSzdS5  
 
  
### DIA 8

- ElasticSearch - HADOOP: [Conector de elastic con hadoop]  
https://colab.research.google.com/drive/1HQxHHbJjej4Cp1tRhOEzQSQ9uW5PlJ5q?  
- KAFKA: [Kafka en Google Cloud Market]  
https://colab.research.google.com/drive/1zM7ytX7ja-6TwX8iCefggXI7CfgIRvfD  
- Herramientas de Integracion en Cloud  
- Snippets de Codigo/Scripts de apoyo:  
https://colab.research.google.com/drive/1yDaYE_7cEj5qTdPOP5CuQu6PnRyJWaL_?usp=sharing  
  

### Notebooks Extra  
  
  
- RabbitMq: [Intro - si da tiempo]  
https://colab.research.google.com/drive/11LtyOF5PIkNETz19hrSFI0Q6-MOtBPAg  
  
- Folium: [Mapas]  
https://colab.research.google.com/drive/1So3FTlgF1n-qvXnbqOriZLU4ucNEFJII  

- Bases de Datos Structured Data: [Redis]  
https://docs.google.com/presentation/d/1nVbQc0CkWxbRGxRSrmfGm-yrEBLoDeKjY85UVG57eWw/edit?usp=sharing
- Link de ejercicios: [aqui](/databases_elastic_redis)  


  
