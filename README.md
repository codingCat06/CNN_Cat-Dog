# CNN_Cat-Dog
## 변경 사항 및 성찰
### 1. summary를 통해 분석해보니 Dense 부분의 parameter 가 300만이 나와서 Conv2D Layer 1개 더 쌓았으며 실행 비용, 과적합 방지

### 2. train 의 정확도가 60% 정도로 낮아짐. 모델의 복잡도를 올리고자 input data 크기를 64 -> 128 로 늘리고 64->128 Conv2D 를 하나 더 쌓음. train과 valid 정확도가 80%까지 상승함.

### 3. train / valid 곡선을 분석해보니 과적합이 일어나지 않지만 성능적으로 좋지 못한 결과(80%)가 아쉬워서 Dropout 수치를 낮췄더니 train / valid 수치 모두 상승함 (85%). 곡선을 통해 아직 일반화도 좋은 성능을 보임.

