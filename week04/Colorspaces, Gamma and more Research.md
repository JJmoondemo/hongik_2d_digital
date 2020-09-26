* color space는 무엇인가?

색상이 들어있는 공간을 뜻한다.

색 공간(色空間, color space)은 색 표시계(color system)를 3차원으로 표현한 공간 개념이다. 색 표시계의 모든 색들은 이 색 공간에서 3차원 좌표로 나타낸다.

CIE lab color spacec

CIE 1976 L * a * b * 색상 공간 (CIELAB이라고도 함)은 물체 색상 측정에 가장 많이 사용되는 색상 공간 중 하나입니다.

1976 년 CIE에서 컬러 커뮤니케이션을 위해 정의했으며 오늘날 많은 산업에서 컬러 제어 및 관리를 위해 널리 채택되고 있습니다.

세상에 굉장히 다양한 color space가 있다.

R,G,B = X,Y,Z로 치환을 할 수 있다.

* YUV 

3D로 모델링한다고 했을 때 UV를 많이 쓴다. 

Y = Luminance & U-V

YCbCr /YPbPr

YCbCr= digital color codes

YPbPr= analog color codes

component video cable = YPbPr

![화면 캡처 2020-09-21 093454](https://user-images.githubusercontent.com/34304514/93725905-d5bd5f00-fbed-11ea-8d61-d6f1486d3676.png)

* ACES color

"Academy Color Encoding System" Acacdemy 시상식의 그 Academy, 영화 제작에 기여하는 이런 것을 개발 배포 공급한다.

카메라마다 color space가 다르다. canon - C log 등등

영화를 촬영할 때 하나의 카메라만 쓰는 것이 아니다. 그래서 촬영, 편집, CG작업등을 할 때 ACES를 기반으로 color space를 제한하는게 좋다.

* color space가 달라지면 예뻐진다..? (ACES < SRGB?)

nope color space 범위가 넓은 ACES가 dynamic range도 더 넓고 풍부한 표현에 있어서 더 좋다. 효과적으로

* ACES Color space가 왜 유명한가?

포토샵으로 작업하고 JPG, PNG파일등으로 저장한다면 sRGB로 대부분 저장이 된다. - 단점은 색상을 표현할 수 있는 단위가 매우 좁다.

JPG는 손실 압출방식(8bit). 디테일한 작업을 위해서는 JPG는 쓰지 않는게 좋을 것 같다.

* 왜 color space에 대해 알고 있어야할까?

SRGB의 한계점을 이해하고 이 color space에 대해 연구가 진행되고 발전이 되고 있는데 폭넓은 color space를 쓰면서 풍부하게 표현할 수 있도록 하는 것이 목표이다.

* Dynamic range

 in photography describes the ratio between the maximum and minimum measurable light intensities
 
 * Gamma / Linear work flow
 
 감마 보정(감마 교정)은 비디오 카메라, 컴퓨터 그래픽 등에서 비선형 전달 함수(nonlinear transfer function)를 사용하여 빛의 강도(intensity) 신호를 비선형적으로 변형하는 것을 말한다. 일반적으로 감마 보정(gamma correction)이란 용어가 널리 쓰이나, 대부분의 경우 감마 부호화(gamma encoding)란 표현이 더 적절하다.

디스플레이 등의 특성에 따라 감마 값을 미세하게 조정하는 것은 감마 조정이며, 감마 보정과는 다른 개념이다
 
 sRGB가 표준으로 채택되면서 감마 2.2를 대부분 쓴다.
 
 SRGB사진들은 대부분 조금씩 감마가 밝게 설정된다. 
 
내가 설정했던 것보다 밝게 나와 어둡게나와 할 때 포토샵에서 해결방법은? "CURVE" 사용해서 적정 감마 곡선(노출)을 조절

누크 마야등에서도 color space지정해줄 수 있는게 있다.

* color-correction

포토샵에서 curves 위로 올리면 밝아지는 이유?

수치를 일일이 조절하지 않아도 밝게/어둡게 만들 수 있기 때문입니다.

RGB (0.5,0.5,0.5)에서 RGB (0.75,0.75,0.75)로 수치가 변한다.

RGB값이 0,0,0이면 black 1,1,1이면 흰색 (additive) 1,0,0이면 빨간색 0,1,0이면 초록색 0,0,1 파란색

위에 것들이 매우 기초적인 color correction 작업이다.

curves는 양 옆이 고정되고 가운데만 움직이는 것 (계속 호의 모습을 하고 있다. linear랑)

brightness를 올리면 RGB 자체 linear를 위 아래로 움직이는 것

이를 통해 어떻게 포토샵은 연산되는지 알 수 있다.



LUT는 무엇일까?

LUT (Look-Up Table)는 특정 RGB 이미지 값을 소스 이미지로 가져와 해당 소스 이미지의 색조, 채도 및 밝기 값을 변경하여 새 RGB 값으로 수정하는 수학적으로 정확한 방법입니다.

LUT는 과학적으로 정확할 수 있습니다 (예 : sRGB 색 공간에서 DCI P3 색 공간으로 이동).

LUT는 또한 Bleach Bypass Look과 같은 소스 이미지에 특정 'Look'을 적용하기 위해 창의적으로 사용될 수 있습니다.

LUT 또는 대조 테이블을 사용하면 비디오 콘텐츠에 다양한 룩을 쉽게 적용할 수 있습니다. RAW 또는 로그 콘텐츠를 촬영할 때 자주 사용되는데, 처음에는 그냥 밋밋하게 보이지만 포스트 프로덕션 창의성을 위한 많은 양의 정보가 포함되어 있습니다.  

서로 다른 텔레비전 표준 간의 변환(예: S-Log3에서 Rec-709로)에 사용되는 “테크니컬” LUT가 있으며, 거의 무한대의 다양한 시각적 모양과 스타일을 만드는 데 사용할 수 있는 크리에이티브 LUT가 있습니다.

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
