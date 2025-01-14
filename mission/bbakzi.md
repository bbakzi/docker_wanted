# I. 사전 미션
## 컨테이너 기술이란 무엇입니까? (100자 이내로 요약)
### What?  
컨테이너는 애플리케이션과 필요한 모든 파일을 하나의 런타임 환경으로 묶는 데 사용하는 기술입니다. 단일 구성 단위로서 컨테이너는 모든 컨텍스트의 모든 운영 체제에서 쉽게 이동 및 실행할 수 있습니다.
### Why?  
컨테이너를 사용하여 사용자는 호환되지 않는 환경으로 인해 발생하는 충돌을 방지하고 시스템 전반에서 일관된 성능을 얻을 수 있습니다. 개발자는 디버깅 또는 다양한 서버 환경에 대한 다시 쓰기가 아닌 애플리케이션 자체에 집중할 수 있습니다. 또한 운영 체제가 없어 개발자가 클러스터에 컨테이너를 효율적으로 구축할 수 있으며 개별 컨테이너에 복잡한 애플리케이션의 단일 구성 요소가 포함됩니다. 구성요소를 개별 컨테이너에 분류하여 개발자들은 전체 애플리케이션을 다시 작업하지 않고 개별 구성요소를 업데이트할 수 있습니다.
### GoodPoint! 
(크기, 속도, 이동성, 모듈성, 자급자족, 비용)  컨테이너를 사용하면 소프트웨어를 격리하고 다른 운영 체제, 하드웨어, 네트워크, 스토리지 시스템 및 보안 정책에서 독립적으로 작업할 수 있습니다. 컨테이너 기반 애플리케이션을 개발, 테스트 및 생산 환경 전반에서 원활하게 전환할 수 있습니다. 운영 체제가 컨테이너에 포함되어 있지 않기 때문에 각 컨테이너는 최소한의 컴퓨팅 리소스를 사용하여 설치가 단순하고 간편합니다.

## 도커란 무엇입니까? (100자 이내로 요약)
### WHAT? 
Go 언어로 작성된 리눅스 컨테이너 기반으로 특정한 서비스를 패키징하고 배포하는데 유용한 오픈소스 가상화 플랫폼이다.
### WHY? 
1. 애플리케이션 독립성을 가진다. 호스트 OS, 다른 컨테이너와도 독립된 공간을 보장받아 충돌이 발생하지 않는다.

2. 컨테이너 내부에 작업 후 배포하려 한다면 도커 이미지로 만들어서 운영서버에 전달만 하면 된다.

3. 마이크로 서비스 구조로 변화가 쉽다. 컨테이너 하나당 하나의 기능을 제공하는 모듈로 만드는 등 조정이 가능하다.

   다시 말해, Docker을 사용하면 환경에 구애받지 않고 애플리케이션을 신속하게 배포, 확장할 수 있다.

## 도커 파일, 도커 이미지, 도커 컨테이너의 개념은 무엇이고, 서로 어떤 관계입니까?
### 도커이미지, 컨테이너란?
Docker Image란 컨테이너를 실행할 수 있는 실행파일, 설정 값들을 가지고 있는 것으로, 더 이상 의존성 파일을 컴파일하거나 이것저것 설치할 필요가 없는 상태의 파일을 의미한다.
### 도커 이미지의 생성 방식
도커 이미지는 기존 이미지에 추가적인 구성이 필요할 때 다시 다운로드하는 방법이 아닌 기존이미지에 레이어를 추가하여 구성을 올려주는 방식으로 생성된다.
### 이미지와 컨테이너의 차이
간단하게 설명하면 도커 이미지는 설계서, 컨테이너는 설계서로 만들어진 상품이다. 게다가 이미지가 중간에 바꾸게 되더라도 기존 컨테이너는 더 이상 이미지에 영향을 받지 않는다.
### 도커컨테이너의 정리 및 특징
정의 : 다시 말해 Docker container란 이미지를 실행한 상태로 응용프로그램의 종속성과 함께 응용프로그램 자체를 패키징 Or 캡슐화하여 격리된 공간에서 프로세스를 동작시키는 기술이다.
특징
1. 컨테이너는 이미지 레이어에 읽기/쓰기 레이어를 추가하는 것으로 생성됨
2. 종료되었다고 해도 삭제되지 않음 -> 읽기/쓰기 레이어 보존
3. 컨테이너를 삭제한 것은 생성파일이 사라지는 것
4. 한 서버는 여러 개의 컨테이너를 가져도 상관없으며 독립적으로 실행
5. 컨테이너는 커널 공간과 호스트 os자원을 공유
   
# II. 실전 미션

## 도커 설치하기


![docker complate](https://github.com/bbakzi/docker_wanted/assets/128371819/af82c157-0af4-4a97-8ef4-9e97cf103653)
