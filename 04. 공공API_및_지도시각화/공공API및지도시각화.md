# 공공 API 및 지도 시각화

참고: 

[Folium](http://python-visualization.github.io/folium/)

[Rest API](https://meetup.toast.com/posts/92)





## 1. Folium 지도 시각화





### 로컬에서 Folium 설치

https://anaconda.org/conda-forge/folium 

```
conda activate base

conda install -c conda-forge folium

y 후 conda deactivate
```





XML: eXtensible Markup Language

JSON: JavaScript Object Notation



지도 생성

```
map = folium.Map(location=[37.541, 126.986], zoom_start=11)
# 서울의 중심
```

```
map.save("seoulmap.html") 	# 지도 저장
```

```
tiles='Stamen Toner' 	# 타일 형태
tiles= 'Stamen Terrain'
```



마커 설치

```
folium.Marker(
    location=[37.55636876124751, 126.99153389155929],    # 위도 경도
    popup="서울 시청",
    tooltip='서울특별시, tooltip'
).add_to(map)
```



Circle Maker

```
folium.CircleMarker(
    ridius=50,
    location=[37.577, 126.988],    # 위도 경도
    popup="서울 시청",
    tooltip='서울특별시',
    color="#3186cc",
    fill=False,
).add_to(map)
```



로컬 파일을 Colab에 업로드

```
from google.colab import files
uploaded = files.upload()
uploaded.keys()
```

```
filename = list(uploaded.keys())[0]
# 리스트로 업로드
```



Choropleth maps(단계구분도)









## 2. 공공API 다운로드

```
다운로드 받고
키 생성하고 devU01TX0FVVEgyMDIxMDgxNjEwMTEzODExMTUyODM=
roadapikey.txt 생성
gitignore에 파일 이름 추가 # 키 노출 안 되게 하기 위함
```

