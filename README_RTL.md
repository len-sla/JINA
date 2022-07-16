

## 1.  Getting data set for presentation of multimodal capability
---
There are multiple ready to use sets of data vaailable though to personalise a bit the presentation I decided to scrap quickly( to get pictures internet with the help of bing engine

it is enough to install download library


```
!pip install bing-image-downloader
from bing_image_downloader import downloader
```
simple funcion

```
query_string='RTL, jobs'
downloader.download(query_string, limit=350, output_dir='rtl', adult_filter_off=True, force_replace=False, timeout=60, verbose=True)
```
was also placed in Colab form to be more universal





---
## 2.  Crossmodal JINA framework in action.

Embedings are calculated and Streamlit front end used to give search text or picture and present result sall this with the help of k8s in docker KIND




![RTL](rtl.gif)

Of course if there would be some extra metadata to those pictures  finetunig could be done and level of confidence will be much higher. <b>
    
Direction  taken by Han Xiao in my opinion is very promisinge.Especially coupled with microservices Strealite, Weaviate and k8s

 ---
## 3.  [Using TTS to generate voice comments as a wave/mp3 file where  input  is text file](https://github.com/len-sla/JINA/blob/main/tts-input_txt_file.ipynb).
    
---


_readme and notebook were prepared in dockerised JupyterLAB_ <b>

```
    docker run --name jupyter_lab  --rm -v $(pwd):/home/jovyan/work  --user "$(id -u):$(id -g)" -p 8888:8888 jupyter/scipy-notebook
```

_Created by:_ [lencz.sla@gmail.com]

