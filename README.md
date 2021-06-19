# 2021_1_jong_seol
1학기 종설 프로젝트

패션 이미지의 상/하의에서 패션 속성을 각 16개씩 총 32개의 패션속성을 인식하는 딥러닝 모델 구현

( 딥러닝 모델 : efficient net b4 & fc layer )

입력데이터 : 874개

- Optimizer : AdamW , Scheduler : CosineAnnealing Warmup Restart 

( ref : ICLR 2019 발표된 “DECOUPLED WEIGHT DECAY REGULARIZATION” 

- 클래스간 불균형 : Over sampling 

( 부족한 클래스의 이미지는 중복으로 학습함 )

- Data Augmentation & TTA ( test time augmentation ) 사용

( DA : 기본적인 회전,상하좌우반전을 이용, TTA : inference시, DA에 적용했던 동일한 augmentation을 적용하여 여러개의 예측치의 평균을 내서 robust 하면서 높은 성능을 내기 위해 사용 )

