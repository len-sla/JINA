

## 1.  [Getting data set for presentation of multimodal capability](https://github.com/len-sla/JINA/blob/main/cornelsen-jina.ipynb)
---
There are multiple ready to use sets of data available though to personalise a bit for  the presentation purpose I decided to scrap quickly( getting search results  for the word "Cornelsen" with bing help)

it is enough to install  library


```
!pip install bing-image-downloader
from bing_image_downloader import downloader
```
simple funcion

```
query_string='Cornelsen Verlag  company profile people media data science'
downloader.download(query_string, limit=350, output_dir='cornelsen', adult_filter_off=True, force_replace=False, timeout=60, verbose=True)
```
was also placed in Colab form to be more universal





---
## 2.  Crossmodal JINA framework in action.

Embedings are calculated and Streamlit front end used to give search text or picture and present results all this with the help of k8s in docker




![Cornelsen](cornelsen-crossmodal.gif)

Of course if there would be some extra metadata to those pictures  finetunig could be done and level of confidence will be much higher. <b>
    
Direction  taken by Han Xiao in my opinion has future. Especially coupled with microservices Streamlite, Weaviate and other Python based frontends 

---


_readme and notebook were prepared in dockerised JupyterLab,  to prepare gif ffmpeg was used_ <b>

```
    docker run --name jupyter_lab  --rm -v $(pwd):/home/jovyan/work  --user "$(id -u):$(id -g)" -p 8888:8888 jupyter/scipy-notebook
```
---
## 3.  [Using TTS to generate voice comments as a wave file where is input text file](https://github.com/len-sla/JINA/blob/main/tts-input_txt_file.ipynb).
    
    
_Created by:_ [lencz.sla@gmail.com]

