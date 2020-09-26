LUT는 무엇일까?

LUT (Look-Up Table)는 특정 RGB 이미지 값을 소스 이미지로 가져와 해당 소스 이미지의 색조, 채도 및 밝기 값을 변경하여 새 RGB 값으로 수정하는 수학적으로 정확한 방법입니다.

LUT는 과학적으로 정확할 수 있습니다 (예 : sRGB 색 공간에서 DCI P3 색 공간으로 이동).

LUT는 또한 Bleach Bypass Look과 같은 소스 이미지에 특정 'Look'을 적용하기 위해 창의적으로 사용될 수 있습니다.

[What is a LUT (and how do you use a LUT for color correction)?](https://mixinglight.com/color-grading-tutorials/understanding-luts/)

<img width="904" alt="스크린샷 2020-09-21 오후 5 46 49" src="https://user-images.githubusercontent.com/34304514/93747947-6f0e6480-fc32-11ea-9e14-1d51104a5a24.png">

Technical LUTs – These types of LUTs are designed to transform an image from one color space / gamut to another. The end goal is to have the same image look perceptually identical on two different viewing devices. For instance: A plasma display and the output of your inkjet printer (technically, this is the goal of ACES – an in-development color space that covers the human visual spectrum – but conceptually the end-goal is the same).
Creative LUTs – These types of LUTs can be generated in software, allowing – for instance – completely different grading apps to share looks between them.
The problem occurs when we assume a Creative LUT is actually a Technical LUT. And there’s a broad type of common color correction LUT where this incorrect assumption happens regularly:

Camera LUTs – A good example of this kind of LUT is the ARRI Alexa Rec 709 LUT, designed to be applied to footage recorded to ARRI’s flat Log-C recording setting. This type of LUT is really a merging of Technical and Creative LUTs. A Camera LUT seems like it’s operating with Mathematical precision. And you’d think Camera LUTs should work precisely the same way every time you use them. But they don’t. Why?Because of…Exposure. As the amount of light hitting the sensor changes – and the relationship between the darkest shadows and brightest highlights change – so does the effect of a LUT on that image.The end result: A Camera LUT is a creative tool designed with a specific purpose in mind. But what it’s NOT designed to do is take every image recorded by that camera and make it perfect every time. It’s just not possible. Professionals new to LUTs often find this is a hard concept to internalize.


LUT는 위와 같이 이미지 보정의 끝단에 위치합니다.

LUT를 적용하는 방법

1. Gamma값 조절하기

2. 사용자가 정한 Gamma값을 적용하기 

