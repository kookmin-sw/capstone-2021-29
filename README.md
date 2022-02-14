# 블랙박스 데이터를 이용한 사고 영상 검출

**팀페이지 주소** -> https://kookmin-sw.github.io/capstone-2021-29

### 1. 프로잭트 소개

![socar](image/socar_image.jpg)  

저희의 프로젝트 목표는 블랙박스 데이터를 이용하여 사고 여부를 판단하는 것입니다.  

블랙박스 데이터는 Normal과 Event 영상으로 나뉩니다.  
Event 영상은 블랙박스가 자체적으로 이벤트, 즉 사고를 감지하여 데이터를 처리한 영상입니다.
Normal 영상은 이벤트가 없는 일반적인 주행 또는 정차된 블랙박스 영상입니다.

하지만 Normal 영상에서도 다양한 사고가 발생하고 있습니다.  
특히, 차의 후면 또는 휠 등 블랙박스에 찍힐 수 없는 부분이 어딘가에 긁히거나 부딪치는 사고입니다.

이러한 사고의 경우에는 사용자가 직접 신고해야 하지만, 모른척 넘어가는 사용자들이 있습니다.  
나중에 다른 사용자가 이를 발견하고 신고하게 되면 어떤 사용자에 의한 사고인지 모르기 때문에 쏘카에서 수리 비용을 전액 부담해야합니다.  

저희 프로젝트는 블랙박스의 영상 데이터와 메타 데이터를 이용하여 이러한 사고들을 검출하는 것입니다.

### 2. 팀 소개

```markdown
담당 교수님: 이재구

E-mail: jaekoo@kookmin.ac.kr
```

```markdown
조영완

학번: 20181694  
E-mail: jyy1551@kookmin.ac.kr
역할 : 메타 데이터를 이용한 사고 검출 모델 개발
Github : https://github.com/whduddhks
```

```markdown
조익현

학번: 20181695  
E-mail: 8982679@kookmin.ac.kr
역할 : 영상, 메타 데이터를 합친 모델 개발
Github : https://github.com/childyouth
```

### 3. 개발  

개발 방법은 2가지로 나누었습니다.  
영상 데이터의 경우, 데이터가 블러처리 되거나 환경에 따라 영향을 많이 받습니다.  
따라서, 1차적으로 메타 데이터만을 이용하여 사고를 검출하는 방법을 선택했고  
영상과 메타 데이터를 한번에 이용하는 모델 개발 방법을 선택했습니다.


### 4. 시연영상 (유튜브)
[![시연](http://img.youtube.com/vi/UQWx4GgbSds/0.jpg)](https://youtu.be/UQWx4GgbSds) 

**메타 데이터 이용**
1. 머신러닝 - decision tree, Random Forest
2. 딥러닝 - 1d cnn, rnn

**영상+메타 데이터 이용**
1. VGG16 / Resnet + lstm
