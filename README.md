## KH정보교육원 수료
### 작성자 : 김태욱
### 교육기간 2019년 08월 16일 ~ 2020년 01월 23일


#

# Riot Games의 Rest API를 활용한 "fifteenGG" 프로젝트

- 챔피언 공략페이지를 담당하였습니다.
- 게임 빅데이터를 활용하기 위한 Rest API를 사용하여 데이터를 수집했습니다.
- 빅데이터를 기반으로 통계수치화 및 시각화 하였습니다.

![개발일정15gg](https://user-images.githubusercontent.com/53084458/82660573-9265da80-9c65-11ea-9fec-b4365a025c15.jpg)



### 2019년 12월 23일 ~ 2020년 1월 23일.

#

![사용 툴](https://user-images.githubusercontent.com/53084458/83226348-c3da2b00-a1bc-11ea-8263-09bcc5800b0c.jpg)

### - 사용 언어 : JAVA, JavaScript
### - 툴 : Spring, Oracle
### - 서버 : apache Tomcat > JSP
### - 홈페이지는 HTML기반이며 디자인은 css, 부트스트랩4 사용
### - 사용 API : Riot Games의 Rest API 사용
### - 라이브러리 : gson, Jquery, myBaits
### - 형상관리 : github

#

## DB 설계

![db1](https://user-images.githubusercontent.com/53084458/83225697-4eba2600-a1bb-11ea-8c0b-ec5aaf935ebf.jpg)
![db](https://user-images.githubusercontent.com/53084458/83225703-511c8000-a1bb-11ea-918d-e007cb946542.jpg)




#


# 담당페이지 설명 및 시연자료
## fifteenGG 프로젝트에서 
### 1. 챔피언 공략 페이지,
### 2. 소환사의 최근 KDA 및 최근 동향 부분,
### 3. 통계 페이지를 담당 구현하였습니다.

#

## 1. 챔피언 공략 게시판
### "챔피언 공략 게시판"은 각 라인별 챔피언 동향과 챔피언에 맞는 공략 페이지 이동 ,
### 최근 업데이트 뉴스 , 각 라인별 상위 티어별 통계로 구성되어 있습니다.
 - 원하는 챔피언의 공략을 빠르게 보기 쉽게 라인별로 챔피언들을 나눠주었습니다.
 - 최신 패치노트 , 현재 라인별로 1티어부터 2티어까지 나누어 롤의 추세를 빠르게 확인 가능합니다.
 
###

#

#

### Jquery를 사용하여 라인별 챔피언 , 통계를 구현하였습니다.
![3](https://user-images.githubusercontent.com/58212906/84868171-3dc44c80-b0b7-11ea-871f-b1886a901d78.jpg)
#
![2](https://user-images.githubusercontent.com/58212906/84870365-30f52800-b0ba-11ea-8364-675cb26b887c.jpg)





## 공략 페이지 시연입니다.

![ezgif com-video-to-gif](https://user-images.githubusercontent.com/58212906/84868652-fee2c680-b0b7-11ea-9b03-a9b4bee1d187.gif)




### 패치노트는 라이엇 홈페이지로 이동합니다.
- 라이엇 홈페이지 패치노트 페이지로 이동을 하여 보다 자세히 볼 수 있습니다.


##
# 소환사 전적 페이지

![4](https://user-images.githubusercontent.com/58212906/84870409-423e3480-b0ba-11ea-89bd-57a75ef1e037.jpg)

#

![5](https://user-images.githubusercontent.com/58212906/84870028-bdebb180-b0b9-11ea-91dc-c6c9265aed00.jpg)



#

## Riot(Rest) API 파싱하기

![파싱1](https://user-images.githubusercontent.com/53084458/82916416-f9102e80-9fac-11ea-8532-2aacafcc7c17.jpg)

- Rest API로부터 받아온 json형식의 DATA를 gson을 사용 클래스매핑하여 파싱하였습니다.

#

![파싱2](https://user-images.githubusercontent.com/53084458/82916408-f6153e00-9fac-11ea-8c42-41b3a7b03d45.jpg)
![파싱쿼리](https://user-images.githubusercontent.com/53084458/82919320-d4b65100-9fb0-11ea-9ef9-8087c285a4a2.jpg)

- 파싱된 DATA는 vo->Service->DAO->Mapper.xml->INSERT 쿼리를 통하여 저장됩니다.

#

![파싱DB](https://user-images.githubusercontent.com/53084458/82916414-f8779800-9fac-11ea-9bf9-fcc6cd9c0225.jpg)

- 위 과정을 통하여 저장되는 테이블입니다.

#


#


## 3. 승률 통계 페이지입니다.
### - Chart.js를 활용하여 DATA를 시각화 하였습니다.


## 파싱한 DATA를 사용 승률을 계산한 쿼리입니다.

![승률통계쿼리](https://user-images.githubusercontent.com/53084458/82923319-ba32a680-9fb5-11ea-8fc7-a039c6402c97.jpg)

## Chart.js 코드입니다.

![chartjs보완](https://user-images.githubusercontent.com/53084458/82922967-409ab880-9fb5-11ea-8da8-74e204a4ba39.jpg)

- canvas태그를 사용해 id를 정해주고 기본적인 사이즈를 설정합니다.

#

<img width="714" alt="차트제이에스" src="https://user-images.githubusercontent.com/53084458/82663588-e7f0b600-9c6a-11ea-932f-93ed55163bd0.png">

- 해당 id를 호출해 어떤 그래프타입을 사용할 것인지, 크기와 색상등 세부적인 css를 설정합니다.

#

![3 승률통계](https://user-images.githubusercontent.com/53084458/82663581-e626f280-9c6a-11ea-8241-04d5136341e6.jpg)

- 승률에 대해 그래프로 표현하여 숫자를 보다 확인하기 쉽게 사용자 중점으로 표현 하였습니다. 

## fifteen.GG                           END

#
#
#

# 첫번째 프로젝트 "Rang"

#### 여행을 공유하여 나의 여행을 다른사람들과 소통, 함께할 일행구하기 그리고
#### 다른사람의 여행을 참고하여 나의 여행을 디자인할 수 있는 플랫폼을 목적으로 진행하였습니다.

### 일정

![세미프로젝트 타임라인](https://user-images.githubusercontent.com/53084458/82647471-35f8c000-9c51-11ea-97e1-7bd58b5e0ec7.jpg)

### 2019년 11월 4일 ~ 2019년 12월 20일.

#

![개발도구](https://user-images.githubusercontent.com/53084458/83231038-d0af4c80-a1c5-11ea-8817-e8000e8bd063.jpg)

### - 사용 언어 : JAVA, JavaScript
### - 툴 : eclipse, Oracle
### - 서버 : apache Tomcat > servlet
### - HTML기반의 홈페이지, css, 부트스트랩4 사용
### - 사용 API : google Map
### - 형상관리 : github

#

## DB 설계
![랑DB설계](https://user-images.githubusercontent.com/53084458/83231044-d147e300-a1c5-11ea-8e13-b24e7a09faac.jpg)


#

## 담당페이지 : 마이페이지 , 검색기능 
### SNS 방식의 스타일로 젊은 사람들에게 친근하게 다가갈 수 있으며 ,
### 너랑나랑 게시판으로 함께 여행할 친구를 구할 수 있습니다.

#



![11](https://user-images.githubusercontent.com/58212906/84873077-a9111d00-b0bd-11ea-9c6d-59b7fd05ef2f.jpg)


![12](https://user-images.githubusercontent.com/58212906/84873114-b928fc80-b0bd-11ea-9c3b-984d6901bc34.jpg)

### 마이페이지는 크게 자기 자신, 상대방 마이페이지로 구성되어 있습니다.
### 회원의 정보 수정 및 자신의 팔로우, 팔로워, 게시글 수 , 목록 등을 확인할 수 있습니다.

#

![13](https://user-images.githubusercontent.com/58212906/84873440-36547180-b0be-11ea-9b6d-12849a6f2535.jpg)

![14](https://user-images.githubusercontent.com/58212906/84873551-5f750200-b0be-11ea-8bb0-c2a625beb0b9.jpg)

### 검색기능(닉네임 or 태그)을 통하여 원하는 나라의 게시글이나 상대방의 마이페이지로 들어갈 수 있습니다.

![15](https://user-images.githubusercontent.com/58212906/84873555-613ec580-b0be-11ea-8e0b-cac1c3588c29.jpg)

![16](https://user-images.githubusercontent.com/58212906/84873557-626ff280-b0be-11ea-9047-aa9eeddb2821.jpg)

![17](https://user-images.githubusercontent.com/58212906/84873560-64d24c80-b0be-11ea-847d-1eb80315bddd.jpg)


### 또한 상대방의 마이페이지로 이동하여 팔로우 및 언팔로우 , 상대방의 게시글들을 볼 수 있습니다.



![5조 랑ppt 최종 (1)_64](https://user-images.githubusercontent.com/53084458/83231034-cf7e1f80-a1c5-11ea-9d34-e588c471b300.png)




