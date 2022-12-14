# DataAnalysis
데이터 시각화 코드 및 데이터 분석 실습 코드 모음

1. meta visualization 이라는 이름의 코드들은 각각 서로 다른 데이터를 시각화하는 코드이다.
  1) 해당 코드를 colab 환경으로 옮긴다.
  2) 제공된 csv 파일을 구글 드라이브로 옮긴다. 코드 실행 전에 구글 드라이브를 mount한다.
  3) csv 파일과 코드의 이름을 보고 1이 붙어있는 것, 2가 붙어있는 것, 숫자가 붙어있지 않은 것을 매칭시켜서 실행한다.
    1metavisualization.ipynb에는 sequences_1.csv파일을 연결하면 된다.
    
  ![image](https://user-images.githubusercontent.com/101084413/206541966-23e5c0dd-7c95-44de-8986-93db820494da.png)
  데이터 시각화한 것들을 시간대 순서대로 나열하면 이렇게 나온다. 이건 백신 출현 이전의 데이터들만 러프하게 처리한 것이고 시간대를 좀더 작게 쪼개서 데이터 시각화를 하면서 시계열적 특성이 드러나도록 데이터들을 만들어 시계열 딥러닝 RNN 모델에 학습시켜 그 다음의 특성이 예측되도록 하는 모델을 만들려고 한다.


<hitmap 제작>
1.	Korea_map
코로나19 발생 초기, 한국의 데이터를 바탕으로 Heat Map을 제작해 보았습니다.
1)	Dashboard1.ipynb : 구글 코랩 환경에서 코드를 실행할 수 있습니다. 지도 시각화 패키지인 ‘follium’을 이용하여 한국의 지도 위에 감염자 수를 열분포 형태로 나타냈습니다. 빨간색에 가까울수록 더 많은 확진자가 발생한 건데요, 이를 보면 당시에 수도권과 대구, 부산 지역에 확진자가 밀집해 있었음을 확인할 수 있습니다.
![image](https://user-images.githubusercontent.com/101084413/206717243-38892c55-2558-42ff-afcb-4c4aa80ce27f.png)
  
2)	Keg_Korcase.csv: 2020년 1월부터 6월까지의 한국의 코로나 확진 데이터입니다. 코랩에 이 파일을 업로드 해놓고 데이터 분석을 진행하면 됩니다.
![image](https://user-images.githubusercontent.com/101084413/206717284-db26d800-3538-49d3-a86a-dd046b94bf26.png)
  

3)	Map.html:
 
제작한 히트맵을 html파일로 내보내 로컬에서 코드 없이도 확인할 수 있게 하였습니다.
![image](https://user-images.githubusercontent.com/101084413/206717340-c8ecfca0-fff1-4a5f-9f20-862d1ba898ee.png)  

2.	World_map
API를 이용하여 해외의 코로나19 데이터를 가져와서 4개국의 코로나 바이러스 발생 현황을 Heat Map으로 만들어 분석해 보았습니다.
1)	Covid_world_map.ipynb : 구글 코랩 환경에서 코드를 작성했으며, Python의 folium, plotly.express 패키지를 사용하여 시각화를 진행했습니다. 지도위에 데이터를 표현하여 각 나라별 위치와 환자 수를 직관적으로 파악할 수 있게 하였습니다.
![image](https://user-images.githubusercontent.com/101084413/206717386-df9f9772-1e67-41b5-9401-49bf7d5de122.png)

 
2)	World_Countries__Generalized_.geojson : 나라별 데이터를 엑셀 파일에 저장한 것입니다. 요소 기술을 검증하기 위해 이스라엘, 아랍에미리트, 영국, 미국의 4개국에 한정하여 데이터를 분석하였습니다. 
 ![image](https://user-images.githubusercontent.com/101084413/206717406-47efdf7b-1c85-4796-aa46-9900a53c9fca.png)

 
3)	folium 세계지도에 확진자 수 시각화_2022-12-02.html : 결과 맵을 html 파일로 저장한 것입니다. 지도를 움직여 해당 나라의 위치를 파악하고 그 위에 마우스를 올리면 확진자수 윈도우가 뜹니다. 색깔에 따라 발생량을 파악할 수도 있습니다.
![image](https://user-images.githubusercontent.com/101084413/206717443-d852c8c9-3504-4dcf-bc15-164ec67a3339.png)

 

