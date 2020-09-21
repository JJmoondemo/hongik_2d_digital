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

RGB값이 000이면 black 111이면 흰색 (additive)

1,0,0이면 빨간색 0,1,0이면 초록색 0,0,1 파란색

