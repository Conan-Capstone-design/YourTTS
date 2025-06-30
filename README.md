# YourTTS - 짱구, 케로로, 코난 음성 합성 프로젝트

이 프로젝트는 캐릭터 기반 음성 합성(TTS)을 위해 [`YourTTS`](https://github.com/coqui-ai/TTS.git) 모델을 기반으로 수정·학습한 프로젝트입니다.  
짱구, 케로로, 코난 3명의 캐릭터 음성을 한 명의 화자로 두고 한국어를 학습시킨 후, 각각 단일 화자 전용 모델로 재학습하여 총 3개의 캐릭터 TTS 모델을 생성했습니다.


<br/>

---



## 프로젝트 구조

### 1단계: 사전학습
- 짱구, 케로로, 코난 음성 데이터를 **동일 화자처럼 취급하여** 한국어를 학습하도록 사전 학습합니다.

### 2단계: 단일 캐릭터 전용 미세조정 (Fine-tuning)
- 1단계 모델을 기반으로, **각 캐릭터별로** 단일 화자 전용 모델을 파인튜닝하여 다음 3개 모델을 제작했습니다:
  - `yourtts-jjanggu`
  - `yourtts-keroro`
  - `yourtts-conan`

<br/>

---


## 학습 방법

### colab 환경 학습
아래의 ipnyb 파일을 따라가면 학습, 추론이 가능합니다. (코랩 유료환경 사용하였습니다.)

[`YourTTS_Keroro.ipynb`](https://github.com/Conan-Capstone-design/YourTTS/blob/main/yourTTS_keroro.ipynb)

<br/>

---


## 모델 다운로드 (Hugging Face)

| 캐릭터 | 모델 링크 |
|--------|-----------|
| 짱구   | [yourtts-jjanggu](https://huggingface.co/gahyunlee/YourTTS_characters/tree/main/conan) |
| 케로로 | [yourtts-keroro](ttps://huggingface.co/gahyunlee/YourTTS_characters/tree/main/keroro) |
| 코난   | [yourtts-conan](ttps://huggingface.co/gahyunlee/YourTTS_characters/tree/main/conan) |

( 사전학습한 모델   | [yourtts-pretrained](https://huggingface.co/Conan-Capstone-design/yourtts-conan) )

<br/>

---

## 참고 리포지터리

- [Original YourTTS](https://github.com/coqui-ai/TTS)
