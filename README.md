# TextSummarizer
인턴 개인과제를 위해 만든 텍스트 요약 알고리즘입니다.<br>Textrank와 PMI 기법을 활용한 추출요약 방식을 사용했습니다.<br>Textrank, PMI에 관한 설명, 오픈소스코드는 [해당 링크](https://bab2min.tistory.com/552)를 참조하시면 됩니다.<br>
해당링크의 오픈소스코드를 변형하고 새로운 알고리즘을 추가하여 만들었습니다.
<br>

# Key Point 
코드 안에 다양한 파라미터가 존재합니다.<br>
(형태소 추가 단어, window, coef, 불용어사전, 품사 선택 등등)<br>
단어를 추가하고 파라미터 값을 변경할 때마다 결과 값이 달라지므로 최적의 값을 찾아서 사용해야 합니다.<br>
또한 정제된 텍스트 일수록 요약 결과가 좋습니다~!<br>
아직 부족한 점이 많은 코드라 보완해나가겠습니다~

# Requirement
python3.5<br>
Konlpy<br>
customized_konlpy<br>
networkx<br>

# Algorithm flow

![flow1](https://user-images.githubusercontent.com/43260218/46671897-f95d8980-cc10-11e8-9e17-ba0ac6335ece.PNG)

# Usage

sent라는 변수에 텍스트 원문([ex 1400자 영화리뷰](https://blog.naver.com/nachthimmel/221326960131))을 입력하고 word+summary.ipynb 파일을 돌리면<br>
1. 핵심단어<br>
‘로맨틱 코미디’, ‘영화 주인공’, ‘달리 신선’, ‘여주’, ‘설정’, ‘무슬림’, ‘생활’, ‘결혼’, ‘포스터’, ‘갈등’, ‘없다’
2. 요약문<br>
포스터와 달리 몹시 세련되다, 로맨틱 코미디와 달리 신선한 점이 많다, 로맨틱 코미디 영화 주인공의 직업이 코미디언이다. 배우가 생활에서 치는 드립도 억지스럽게 느껴지지 않다, 파키스탄 무슬림의 결혼 문화도 상당히 신선하다, 파키스탄 무슬림이라는 하나의 설정은 여러가지 갈등을 보이다, 하나 흔한 전개가 없다.
<br>
이와 같은 형태로 핵심단어, 요약문이 추출됩니다.
