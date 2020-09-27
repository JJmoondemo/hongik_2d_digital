# Color space

색 공간(色空間, color space)은 색 표시계(color system)를 3차원으로 표현한 공간 개념이다.
색 표시계의 모든 색들은 이 색 공간에서 3차원 좌표로 나타낸다.


# CIE lab color space

CIE 1976 L * a * b * 색상 공간은 물체 색상 측정에 가장 많이 사용되는 색상 공간 중 하나입니다. 
1976 년 CIE에서 컬러 커뮤니케이션을 위해 정의했으며 오늘날 많은 산업에서 컬러 제어 및 관리를 위해 널리 채택되고 있습니다.


# YUV 

빛의 삼원색을 표현하는 RGB와 달리 빛의 밝기를 나타내는 **휘도(Y)와 색상신호 2개(U, V)** 로 표현하는 방식이다. 일반적인 TV나 비디오 카메라에서 많이 사용되는 방식이며, 흑백을 표현하기 위한 흰색, 회색, 검정색을 표현하는데 사용된다.
3D로 모델링한다고 했을 때 UV를 많이 쓰는 것을 알 수 있다.
**Y = Luminance & U-V**




# YCbCr /YPbPr
> YCbCr는 digital color codes
YPbPr는 analog color codes

![화면 캡처 2020-09-21 093454](https://user-images.githubusercontent.com/34304514/93725905-d5bd5f00-fbed-11ea-8d61-d6f1486d3676.png)

    Component video cable = YPbPr




# ACES color

> "Academy Color Encoding System"

 Acacdemy 시상식의 그 Academy이다. Academy에서 영화 제작에 기여하는 이런 Color system을 개발,배포,공급한다.
카메라마다 color space가 다른 것을 알 수 있다. canon에서는 C log를 쓰는 등등
즉 영화를 촬영할 때 하나의 카메라만 쓰는 것이 아니다. 그래서 촬영, 편집, CG작업 등을 할 때 이 ACES를 기반으로 color space를 제한하는게 좋다.




### Color space가 달라지면 예뻐진다? (ACES < SRGB?)

> **Nope**
Color space 범위가 넓은 ACES가 Dynamic Range도 더 넓고,
풍부한 표현에 있어서 더 좋다. 




### ACES Color space가 왜 유명한가?

> 포토샵으로 작업하고 JPG, PNG파일등으로 저장한다면 sRGB로 대부분 저장이 된다.
이것의 단점은 색상을 표현할 수 있는 단위가 매우 좁다는 것이다.
JPG는 손실 압출방식(8bit). 디테일한 작업을 위해서는 JPG는 쓰지 않는게 좋을 것 같다.




# 왜 color space에 대해 알고 있어야할까?

SRGB의 한계점을 이해하고 이 color space에 대해 연구가 진행되고 발전이 되는 세상에서  폭넓은 Color space를 쓰면서 풍부하게 표현할 수 있도록 하는 것이 목표이다.




* Dynamic range
 > in photography describes the ratio between the maximum and minimum measurable light intensities
 
# Gamma / Linear work flow
 
 감마 보정(감마 교정)은 비디오 카메라, 컴퓨터 그래픽 등에서 비선형 전달 함수(nonlinear transfer function)를 사용하여 **빛의 강도(intensity) 신호를 비선형적으로 변형하는 것**을 말한다. 일반적으로 감마 보정(gamma correction)이란 용어가 널리 쓰이나, 대부분의 경우 감마 부호화(gamma encoding)란 표현이 더 적절하다. 디스플레이 등의 특성에 따라 감마 값을 미세하게 조정하는 것은 감마 조정이며, 감마 보정과는 다른 개념이다
 
* sRGB가 표준으로 채택되면서 감마 2.2를 대부분 쓴다.
 sRGB 사진들은 대부분 조금씩 감마가 밝게 설정된다. 
 
* **내가 설정했던 것보다 밝게/어둡게 나온다면,** 포토샵에서 해결방법은? 
"CURVE" 사용해서 적정 감마 곡선(노출)을 조절하는 것이다. 


# Color-correction

포토샵에서 curves 위로 올리면 밝아지는 이유?
수치를 일일이 조절하지 않아도 밝게/어둡게 만들 수 있기 때문입니다.
예를 들어, RGB (0.5,0.5,0.5)에서 RGB (0.75,0.75,0.75)로 수치가 변한다.
> RGB값이 
> 0,0,0이면 Black
1,1,1이면 White (additive)
1,0,0이면 Red
0,1,0이면 Green
0,0,1 Blue

위가 매우 기초적인 color correction 작업이다.
curves는 양 옆이 고정되고 가운데만 움직이는 것 (계속 호의 모습을 하고 있다. linear랑)
brightness를 올리면 RGB 자체 linear를 위 아래로 움직이는 것
이를 통해 어떻게 포토샵은 연산되는지 알 수 있다.






LUT는 무엇일까?

LUT (Look-Up Table)는 특정 RGB 이미지 값을 소스 이미지로 가져와 해당 소스 이미지의 색조, 채도 및 밝기 값을 변경하여 새 RGB 값으로 수정하는 수학적으로 정확한 방법입니다.

LUT는 과학적으로 정확할 수 있습니다 (예 : sRGB 색 공간에서 DCI P3 색 공간으로 이동).

LUT는 또한 Bleach Bypass Look과 같은 소스 이미지에 특정 'Look'을 적용하기 위해 창의적으로 사용될 수 있습니다.

LUT 또는 대조 테이블을 사용하면 비디오 콘텐츠에 다양한 룩을 쉽게 적용할 수 있습니다. RAW 또는 로그 콘텐츠를 촬영할 때 자주 사용되는데, 처음에는 그냥 밋밋하게 보이지만 포스트 프로덕션 창의성을 위한 많은 양의 정보가 포함되어 있습니다.  

서로 다른 텔레비전 표준 간의 변환(예: S-3에서 Rec-709로)에 사용되는 “테크니컬” LUT가 있으며, 거의 무한대의 다양한 시각적 모양과 스타일을 만드는 데 사용할 수 있는 크리에이티브 LUT가 있습니다.

[What is a LUT (and how do you use a LUT for color correction)?](https://mixinglight.com/color-grading-tutorials/understanding-luts/)

[LUT 라이브러리SONY](https://pro.sony/ko_KR/technology/professional-video-lut-look-up-table)


* LUT의 이점
LUT 또는 대조 테이블을 사용하면 비디오 콘텐츠에 다양한 룩을 쉽게 적용할 수 있습니다. RAW 또는 로그 콘텐츠를 촬영할 때 자주 사용되는데, 처음에는 그냥 밋밋하게 보이지만 포스트 프로덕션 창의성을 위한 많은 양의 정보가 포함되어 있습니다.  

서로 다른 텔레비전 표준 간의 변환(예: S-Log3에서 Rec-709로)에 사용되는 “테크니컬” LUT가 있으며, 거의 무한대의 다양한 시각적 모양과 스타일을 만드는 데 사용할 수 있는 크리에이티브 LUT가 있습니다.

<img width="904" alt="스크린샷 2020-09-21 오후 5 46 49" src="https://user-images.githubusercontent.com/34304514/93747947-6f0e6480-fc32-11ea-9e14-1d51104a5a24.png">


LUT는 위와 같이 이미지 보정의 끝단에 위치합니다.

LUT를 적용하는 방법

1. Gamma값 조절하기

2. 사용자가 정한 Gamma값을 적용하기 

LUT의 종류

[LUT의 종류]
 
1. 1D LUT
R, G, B의 채널은 각각 하나의 1차원의 배열을 지니고 있습니다. 다시 말해 1D LUT는 1차원이기 때문에 개념상 면이 아닌 선 혹은 곡선의 형태이며 R, G, B 채널당 각각 커브를 움직일 수 있습니다. 1D LUT의 특징은 Lift, Gamma, Gain, Contrast에 1:1로 매칭이 되고, Hue, Saturation의 보정 값은 1D LUT에 아무런 변화를 주지 못합니다. 이러한 결과로 인해 흔히들 1D LUT를 흔히 밝기 값만 보정한다고 해서 ‘휘도 곡선’이라고 표현하고 있습니다. 하지만 Lift, Gamma, Gain 들을 R, G, B 채널 당 따로 보정을 했을 경우에는 휘도 외에도 색상까지 보정되는 결과를 얻을 수 있으므로 단지 휘도 값만 조절한다고 한정 지을 순 없습니다. 하지만 대다수 1D LUT는 R, G, B채널의 값이 동일한 경우가 대다수 입니다.
 
 2. 3D LUT
3D LUT는 색상 채널의 모든 값 범위에 대한 색상 변환을 나타내는 각각의 축을 사용하여 선으로만 표현이 가능한 1D LUT와 달리 3차원 좌표계(3D Cube)로 시각화할 시킬 수 있습니다. R, G, B 각 축을 따라 있는 점의 개수는 LUT의 사이즈에 따라 다르게 생성됩니다. 그 점을 중심으로 각각의 색상 채널에 대한 색상 변환을 할 수 있으며, 점 과 점 사이는 보간법을 이용해 근사치 값으로 보정이 되므로 LUT의 사이즈가 클수록 좀 더 정밀하게 색상을 컨트롤 할 수 있습니다. 현재 우리가 LUT라고 통칭해서 부르고 많이 사용하는 LUT가 바로 3D LUT라고 보시면 됩니다.

LUT의 포맷

![LUT포맷](https://user-images.githubusercontent.com/34304514/94341400-f2b9be00-0043-11eb-925b-135cac9fb5d1.png)

LUT 만들기

LUT는 자신이 필요해 의해서 만들어 쓰는 것도 가능합니다. 만드는 방법은 무척이나 다양합니다. 후반 작업용 소프트웨어나 DI 툴, 이미지 편집 툴을 이용할 수도 있고 전문 LUT 제작 툴을 사용 할 수도 있습니다. 툴마다 다른 방법을 가지고는 있지만 일반적으로 색보정 하듯이 색보정을 한 후 단순히 그 정보값을 기반으로 LUT를 출력하는 단순한 방법 부터 일일이 변수를 주어서 값을 변화 시키는 방법까지 다양합니다.

[LUT, 원하는 룩으로 가는 지름길](http://keruluke.com/archived_web/kft/vol4/lookuptable/)


linear 

 컴퓨터 처리에 사용하기에 완벽한 의미가 있지만 우리 눈은 동일한 간격 사이에서 거의 동일한 양의 밝기 변화를 볼 것으로 기대하기 때문에 사람이 보는 데 적합하지 않습니다. 
 
 SRGB

linear의 문제를 해결하기 위해서 색상을 비선형으로 만드는 표준 인 sRGB라는 변환을 적용합니다 (그림 2). 곡선은 하단이 더 얕아서 더 어두운 값을 표시하고 상단이 더 가파르 기 때문에 더 적은 라이트 값을 가질 수 있습니다.
곡선은 하단이 더 얕아서 더 어두운 값을 표시하고 상단이 더 가파르 기 때문에 더 적은 라이트 값을 가질 수 있습니다.


Logospace

로그를 색상 공간 "아카이버"로 생각할 수 있습니다 (파일에 대해 zip 또는 rar가 수행하는 것과 동일한 방식). 선형 공간은 동일한 단계로 값을 증가시키는 반면 로그 색상 공간은 이미지의 흰색 및 검은 색 영역의 값을 압축하여 정보를 저장하는 데 필요한 공간을 최소화하기 때문입니다 (그림 4).
이 형식을 사용하면 16 비트 .tif와 같이보다 관리하기 쉬운 형식으로 그림을 그릴 수도 있습니다. 위의 비유를 따르면 16 비트 로그 파일이 클리핑없이 32 비트 선형 형식으로 "보관 해제"될 수 있기 때문입니다. 가장 일반적인 로그 형식은 ARRI Log 및 Cineon Dpx입니다.

언제
Log는 영화 제작자에게 놀라운 리소스입니다. 이제 소비자 용 카메라에 내장 된 저렴한 비용으로이를 얻을 수 있다는 사실 은 모든 저예산 영화 제작자 에게 놀라운 도구 일뿐 입니다.

왜 쓰나
카메라 센서 (또는 필름 네거티브)에서 가장 역동적 인 정보 범위를 유지하는 방법 입니다. 카메라가 보는 것을 로그로 인코딩 하여 이미지 노출 (스톱 단위로 측정)과 기록 된 이미지 간의 상관 관계 가 더 넓은 범위에서 완전히 일정하다는 것을 의미합니다 . 인간의 눈이나 비디오 화면을 위해 특별히 캡처하는 대신 가능한 한 많은 데이터를 저장  하기 때문에 표준 비디오 곡선보다 센서 정보 를 더 많이 사용합니다 . 이것은 포스트 프로덕션에서 작업 할 수있는 훨씬 더 많은 색상 데이터를 제공합니다.

what is main difference with sRGB,

대부분의 Photoshop 툴은 8비트 또는 16비트 모드에서만 제대로 작동하기 때문에 32비트 형식으로 제공되는 모든 또는 대부분의 정보를 유지하면서 이러한 모드에서 그림을 그릴 수 있는 방법을 찾아야 합니다. 그것을 해결하기 위해 위해 "로그"가 존재한다.

[색 공간 관리 : sRGB, 선형 및 로그](https://www.artstation.com/tiberius-viris/blog/3ZBO/color-space-management-srgb-linear-and-log)


[합성시 로그 및 색 공간 이해](https://www.rocketstock.com/blog/tips-for-log-color-space-compositing/)
