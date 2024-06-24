## Phenotyping using a Plate Reader
작성자 : 유지현 
날짜 : 2024-06-23


### 실험 목표

-   MPH-based Genetic Enzyme Screening System (GESS)의 activity를 예측하는 simple binary classification CNN model을 제작함.
-   이 model의 예측성을 검증하기 위한 MPH mutant를 제작하였고, multi-label microplate reader를 통해서 EPN과 pNP가 있는 환경에서 Fluorescence analysis를 한다.

### 참고 논문

-   https://www.nature.com/articles/s41467-018-07488-0
-   https://pubs.acs.org/doi/10.1021/sb400112u

### Wild type GESS를 이용한 Standard activity 확인

#### Streaking
1. deep freezer에서 Stock을 꺼낸다.
2. stock을 녹이지 않은 상태에서 loop로 얼음을 살짝 긁어낸다. 
3. 항생제가 처리된 Petri plate(no colony)의 약 1/4정도되는 곳을 바깥에서 안쪽 방향으로 지그재그로 loop를 부드럽게 spread 시켜줍니다.
4. streak의 첫 번째 위치에 loop를 두고, plate의 또다른 1/4되는 곳으로 inculum을 부드럽게 이동시키며 지그재그 모양을 만듭니다.
5. 마지막 streak는 지그재그 모양을 넓혀 tail을 만들어 picking하기 용이하게 만들어 줍니다.
6. 37℃ incubator에서 overnight(16h)동안 배양한다.

#### Seed culture
1. 14mL conical tube에 2ml LB medium와 2μL Chloramphenicol(34μg/ml)을 넣는다.
2. 키워두었던 streaking plate에서 single colony를 1개씩 loop를 이용해 tube에 옮겨준다.
3. 37℃ 200rpm incubator에서 8h동안 키워준다.
4. Spectrophotometer를 이용해 OD600을 측정한다.

#### main culture
1. 14mL conical tube에 2ml LB Broth와 2μL chloramphenicol을 넣는다. 
2. 키워두었던 culture에서 2μL씩 tube에 옮겨준다.-> 1% (v/v) of the seed culture
3. 농도별로 EPN,pNP을 넣어준다. 
- 0uM, 0.1uM,1uM,10uM,100uM,1M
4. 37℃ 200rpm overnight로 키운다.(16H)

#### Fluorescence analysis
1. conical tube에서 200ul씩 따서 black wall clear bottom 96 well plate에 넣는다.
2. Multi-label microplate reader를 이용해 RFU를 측정한다.
(at excitation and emission wavelengths of 485 and 535 nm, respectively)
-Multimode reader Infinite® 200 PRO
-THE SPARK® MULTIMODE MICROPLATE READE
-Victor V, Perkin-Elmer, Waltham, MA

### 8종의 MPH_GESS mutant를 이용한 activity 확인