**WAKTAVERSE dashboard** 에서 이용하기 위해 학습시킨 자연어처리(이진분류) 모델 입니다.

### 데이터

>* 한국어 단발성 대화 
* [한국어 악성댓글 데이터](https://github.com/ZIZUN/korean-malicious-comments-dataset) 
욕설이 들어갔거나, 강한 혐오표현, 비난
* [욕설 감지 데이터셋](https://github.com/2runo/Curse-detection-data) 
단순 욕설, 인종 차별적인 말, 정치적 갈등을 조장하는 말, 성적·성차별적인 말, 타인을 비하하는 말, 그 외에 불쾌감을 주거나 욕설로 판단되는 말 
* youtube comment 를수집하여 일부 라벨링

### 전처리, tokenizer 모델
일부 인터넷 용어들 사전을 따로 만들어주기위해 커스텀하기 쉬운 ckonlpy로 선정 
* ckonlpy

### 학습모델
*  LSTM, LSTM+Attention, Bilstm, Bilstm + Attention

### 데이터 결합
> 어차피 해당 댓글이 clean(긍정적)인지, 부정적인지 이진분류 하는데에 초점을 맞췄기 때문에, '부정'중에 좀 더 세부적으로 라벨링('인종차별','성별혐오','단순악플' 등)이 되어있는 데이터들을 모두 '부정'으로 합쳐주었습니다. 긍정으로 라벨링된 데이터가 약 2만개 더 많습니다.

sentiment 긍정(1) : 125585
sentiment 부정(0) : 104299

![](https://velog.velcdn.com/images/liveandletlive/post/28675be5-44ad-4b54-9a6f-1a20a9de1bae/image.png)

### 전처리
> 딥러닝을 이용한 [자연어 처리 입문](https://wikidocs.net/book/2155)의 내용을 바탕으로 진행하였습니다.

### 모델요약

