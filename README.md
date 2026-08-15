# How seq2seq Works

seq2seq(Sutskever·Vinyals·Le, 2014)의 동작 원리를 브라우저에서 직접 실험하며 배우는 인터랙티브 교육 자료입니다. 모든 데모가 외부 라이브러리 없이 브라우저에서 직접 실행됩니다.

**🔗 데모: https://dev-jonghoonpark.github.io/how-seq2seq-works/**

『Sutskever's List』 4장(RNN)과 5장(어텐션) 사이의 다리로 읽는 것을 권합니다.

## 내용

| 절 | 주제 | 인터랙티브 데모 |
|---|---|---|
| §1 | 인코더–디코더 구조 | 번역 과정 스텝별 애니메이션 (은닉 상태 → 문맥 벡터 c → 자기회귀 생성) |
| §2 | 고정 길이 병목 | 문장 길이 압축 시각화 · 문장 길이 vs BLEU 차트 (Bahdanau 2015 재구성) |
| §3 | 입력 역순 트릭 | 단어 간 의존 거리 측정기 — 평균은 같은데 왜 도움이 되는가 |
| §4 | 미니 seq2seq | **브라우저에서 직접 학습하는 LSTM 인코더–디코더** — 순방향 vs 역순 입력 A/B 실험, 길이별 정확도, 직접 디코딩 |
| §5 | 빔 서치 | 방금 학습한 모델의 실제 확률로 전개하는 빔 서치 시각화 |
| §6 | 유산 | 병목 → 어텐션 → 트랜스포머로 이어지는 계보 + 이해도 퀴즈 6문제 |

§4의 미니 seq2seq는 LSTM 인코더–디코더의 순전파·역전파(BPTT)를 순수 JavaScript로 직접 구현한 것으로, 복사 과제(copy task)를 통해 논문의 입력 역순 트릭 효과가 페이지 안에서 실제로 재현됩니다.

## 원전

- Ilya Sutskever, Oriol Vinyals, Quoc V. Le, [Sequence to Sequence Learning with Neural Networks](https://arxiv.org/abs/1409.3215) (NeurIPS 2014)
- Kyunghyun Cho et al., [Learning Phrase Representations using RNN Encoder–Decoder](https://arxiv.org/abs/1406.1078) (2014)
- Dzmitry Bahdanau, Kyunghyun Cho, Yoshua Bengio, [Neural Machine Translation by Jointly Learning to Align and Translate](https://arxiv.org/abs/1409.0473) (2015)

## 함께 보기

- [how-ai-works](https://github.com/dev-jonghoonpark/how-ai-works) — 이 시리즈의 전체 목록
