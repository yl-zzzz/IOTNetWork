# 지하철 승강장의 초미세먼지 농도
-MQTT 프로토콜을 사용하여 청량리역 승강장의 초미세먼지 농도를
 실시간으로 받아오는 프로젝트이다.
 
 # 1. 프로젝트의 필요성
 환경부와 한국환경공단에서 지하철 승강장의 초미세먼지 농도를 누리집과 모바일 애플리케이션으로 확인할 수 있다는 글을 보게 되었고,<br/>
 직접 사이트에 들어가서 확인해봤다. 전국 지하역사에 초미세먼지 자동측정기기 설치를 하고,<br/> 측정결과를 누리집과 모바일 애플리케이션을 구축해 확인할 수 있게 했다.<br/> 
 하지만 1시간 평균 또는 24시간 평균만 확인할 수 있어서 실시간의 데이터를 볼 수 없는 점이 아쉬웠다.<br/> 
 실시간으로 초미세먼지 농도를 확인할 수 있다면 kf가 높은 마스크를 챙긴다든지,<br/> 다른 교통수단을 이용할 수 있어서 실시간으로 확인하는 것이 더 좋을 것 같다는 생각에 이 프로젝트를 구상하게 됐다.
 
 # 2. 시스템 구조
 지하철역 이름, 초미세먼지 농도, 실시간 시간까지 볼 수 있는 모니터링 시스템의 시스템 구조를 보여준다.<br/> 본 시스템은 센서, MQTT Broker, Node. js, Mongo DB, MQTT Publisher, MQTT Subscriber, Web UI로 구성된다.
![image01](https://user-images.githubusercontent.com/71144019/122519454-70e44780-d04d-11eb-9634-3e273ed42622.png)

# 3. 프로젝트 과정
### 1. 공공 데이터 포털에서 실시간 데이터 발급 
### 2. MongoDB에 데이터 저장
### 3. Publish서버가 토픽 발행하고 Broker 서버로 전달
### 4. Subscriber가 토픽 구독하면 Broker 서버가 데이터 전달
### 5. html에 실시간 정보 출력
 
# 3. 결과 화면
