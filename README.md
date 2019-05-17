# sorting characters

이 알고리듬은 영상에서 어떠한 물체를 검출 했으면 그들의 좌표를 가지고 목적에 따라 sorting 해주는 것입니다.


기본적으로 다음의 기능이 구현되어 있습니다.

영상의 글자들 위치를 알고 있을 때 이들을 우종서의 서식으로 읽을 때의 순서로 소팅해 줄 수 있습니다.


아래와 같이 사용하시면 됩니다.

예시)
input_path = "/home/ihs/Documents/프로젝트사진파일"
output_path = "/home/ihs/Documents/프로젝트/numbering"
csv_path = "/home/ihs/Documents/프로젝트/boundingbox.csv"

input_path : 영상 파일들이 있는 폴더 경로 입니다
output_path : 처리된 영상을 내보낼 폴더 경로 입니다.
csv_path : bounding box 처리된 정보가 있는 폴더 입니다(기본적으로 csv 파일 형식이고 다음과 같은 형태로 되어있습니다.)


x       y       w       h
  10      10     10      10
  30      55     60      12
  .
  .
  .
  
  
  
만약 여러분이 자신만의 특별한 bbox 형식을 갖고 있다고 하여도 걱정하지 마십시오.

단지 class MakeListGT()의 내부 함수 get_gt_dict를 자신의 bbox 정보를 담고 있는 형식에 맞게 수정해주시면 되겠습니다
get_gt_dict 함수는 단지 csv 파일에서 각 영상에 해당하는 bbox 좌표들만 추출하여 딕셔너리 형태로 보관만 하는 함수입니다.

예시)
data { '영종일기' : [[x,y,w,h], [x,y,w,h], [x,y,w,h] ...] , '태종일기' : [[x,y,w,h], [x,y,w,h], [x,y,w,h] ...] }



Configuration

 python 3.x
 jupyter notebook
 matplotlib
 PIL
 math
 
그 외에 필요하다고 요구되는 library는 경고 문구에 따라 설치하시면 되겠습니다.

실행에 곤란함을 겪으신다면 dlrghks411@naver.com 으로 이메일을 주시면 됩니다.


적용 예

![
