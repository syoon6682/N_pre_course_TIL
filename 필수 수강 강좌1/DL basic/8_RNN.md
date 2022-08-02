# RNN

: sequential한 입력에 대한 처리



### Sequential Model

: sequential data = 순차적인 데이터

: 문제 : 입력의 처음과 끝을 알 수 없다, 몇 개의 데이터가 들어올지도 모름

: 고려해야 하는 정보가 점점 늘어남



-> 해결하기 위해 제시된 모델: **Markov model (first-order autoregressive model)**

h : hidden state (output)



### Recurrent Neural Network (RNN)

: 모델이 자기자신으로 들어옴 -> 그러면서 과거를 반영시킴



단점

: short-term dependencies - 조금만 기간이 멀어져도 영향력이 떨어짐 -> 최근 정보만 주로 반영 -> 이걸 해결한 것이 LSTM(Long Short Term Memory)

-> 그래서 ReLU를 잘 안씀..



### LSTM

: 교재보고 flow 잘 기억하기..

: 컨베이어 벨트 같이 생각! -> 넘어오고 조작하고 넘겨주고

- Forget Gate

   : 어떤 정보를 버릴지

- Input Gate

  : 어떤 정보를 저장해서 cell state에 넘겨줄지

- Update cell

  : cell state 업데이트

- Output Gate

  : updated cell을 Output으로 보냄



### GRU (Gated Recurrent Unit)

: gate가 2개 (reset gate & update gate)

: no cell state, just hidden state

-> 그러나 대부분의 RNN은 transformer에 대체되었다...

: 헷갈리면 강의 한번 더 보기





