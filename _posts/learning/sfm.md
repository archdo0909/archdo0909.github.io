  ---
  layout: archive
  permalink: /docs/learning/  
  title: "Structure from Motion의 이해"
  author_profile: true
  ---


##Structure from Motion(sfm)의 이해

OpenCV를 활용한 sfm에 대해서 논의하고자 함.

###Structure from Motion의 개념

먼저, stero 카메라와 sfm에 의한 3차원 재구성에 대한 차별점을 이해하고 가고자 한다. 
3차원 재구성에 있어, 스테레오 카메라와 같은 다수의 카메라가 사전에 calibrated 된 장치가 아닌 한대의 카메라를 가지고 카메라 사이의 "움직임"을 추정하고자 함. Sfm의 시스템을 구성하는 첫번째 단계는 카메라 간의 움직임을 찾는 것이고, OpenCV의 [findFundamentalMat](https://docs.opencv.org/2.4/modules/calib3d/doc/camera_calibration_and_3d_reconstruction.html#Mat%20findFundamentalMat(InputArray%20points1,%20InputArray%20points2,%20int%20method,%20double%20param1,%20double%20param2,%20OutputArray%20mask) 및 [findEssentialMat](https://docs.opencv.org/3.4/d9/d0c/group__calib3d.html) 함수는 카메라의 모션을 획득하는데 도움이 되는 몇 가지의 방법 중 하나이다.

[Reference Links](https://hub.packtpub.com/exploring-structure-motion-using-opencv/)