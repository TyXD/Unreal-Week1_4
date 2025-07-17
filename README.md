# 사전캠프 4일차 TIL
## 3D 게임 개발이 처음이어도 언리얼 블루프린트로 쉽게 배우는 3D 게임 개발 5주차 과제
### 숙제 설명
10분간 플레이할 수 있는 게임으로 만들기

지금까지 학습한 내용을 바탕으로 플레이가 가능한 게임을 만들 수 있게 되었습니다.

이번에는 이 게임을 조금 더 **게임같게** 만들어봅시다.

내가 구현한 발판, 장애물, AI 캐릭터를 더 다양하게 직접 배치하여 난이도 높은 게임으로 만들어보세요!

필수숙제

1. 내 언리얼 게임 프로젝트에서 작업하던 레벨에 **발판**을 추가해주세요.

> **발판의 위치와 개수를 더 다양하게 배치하여** 더 많은 발판을 밟아야 클리어 할 수 있도록 구성해보세요.

> **추가한 동작이 실제로 동작하는지** 시뮬레이션을 통해 확인하며 변경해보세요.

2. 내 언리얼 게임 프로젝트에서 작업하던 레벨에 **장애물**을 추가해주세요.

> **장애물을 이쯤 넣으면 게임의 난이도가 올라가겠지..?** 를 생각하며 장애물을 추가합니다.

> **너무 많은 장애물은 오히려 게임을 피곤하게 만들겠죠?** 적절하게 배치해봅시다.

3. 내 언리얼 게임 프로젝트에서 작업하던 레벨에 **AI 캐릭터**를 추가해주세요.

> AI 캐릭터를 더 배치하는 것으로 **발판에 오르는 것과 동시에 적에게서 벗어나는 챌린지를** 줄 수 있습니다.

> **AI 캐릭터도 너무 많으면** 게임이 어려워지니 시뮬레이션으로 적절하게 조절해보세요.

### 결과 이미지

<img width="720" height="353" alt="Image" src="https://github.com/user-attachments/assets/98a5ced4-2a65-41ee-a56e-56c6a1680abd" />

<img width="720" height="364" alt="Image" src="https://github.com/user-attachments/assets/ed0bbede-7266-41b5-aacf-427ac1564e56" />

<img width="719" height="343" alt="Image" src="https://github.com/user-attachments/assets/a57946fc-80b2-4cae-aab3-19103373e863" />

<img width="720" height="352" alt="Image" src="https://github.com/user-attachments/assets/77ce1cd2-69f4-4268-a5fe-301da0b722e1" />

<img width="720" height="425" alt="Image" src="https://github.com/user-attachments/assets/00243aeb-7eff-4c00-aec2-909c6dfd2264" />

<img width="719" height="367" alt="Image" src="https://github.com/user-attachments/assets/caeed1f2-92bd-4247-bab0-3dca2d9573bd" />

<img width="720" height="448" alt="Image" src="https://github.com/user-attachments/assets/945c7acd-2902-4f72-bf58-fa24e83500f6" />

<img width="720" height="371" alt="Image" src="https://github.com/user-attachments/assets/3df4e10a-f533-4dae-b07f-2bed96599733" />

## 3D 게임 개발이 처음이어도 언리얼 블루프린트로 쉽게 배우는 3D 게임 개발 6주차 
## UMG의 제작 및 연동

### 1. 언리얼 엔진에서 UI 제작
언리얼 엔진에서는 **언리얼 모션 그래픽 UI 디자이너**를 사용해서 UI를 구현이 가능하다.

<img width="720" height="411" alt="Image" src="https://github.com/user-attachments/assets/863d10b1-3a50-401d-bc9a-bb3aa7945a32" />


우선 콘텐츠 브라우저에서 블루프린트 클래스 생성을 들어가서 **UserWidget** 블루프린트 클래스를 선택하여 UI를 만들어 준다.

<img width="720" height="425" alt="Image" src="https://github.com/user-attachments/assets/c7e01142-2896-4b8c-809c-854300ed6685" />

그 후 UI 구성 창에서 **캔버스**를 추가해야 한다. **캔버스 패널**은 UserWidget에서 UI를 그릴 수 있는 실제 캔버스 역할을 한다.

<img width="693" height="720" alt="Image" src="https://github.com/user-attachments/assets/7f1db09e-8392-4313-810e-1c2fa66b357b" />

**앵커**는 UI 정렬 방식으로, UI의 위치를 조절하는 기준점이다다.

예를 들어 앵커를 가운데로 설정하면 포지션 0,0 위치는 중앙을 기준으로 설정된다. 

텍스트를 변경하는 예시로 "안녕하세요"를 입력하면 해당 텍스트가 표시됩니다. 폰트도 마찬가지로 바꿔줄 수 있다.


<img width="720" height="437" alt="Image" src="https://github.com/user-attachments/assets/7e8ba00e-c80e-4cde-abd0-481a23112a14" />

**이미지**의 경우 브러시에서 텍스쳐 에셋을 선택하여 이미지 모양을 바꾸어 줄 수 있다.

<img width="688" height="720" alt="Image" src="https://github.com/user-attachments/assets/a18d7e40-9362-4029-a24d-ccf7ef1e894b" />

또한 Z순서를 조절하여 구현 순서를 변경하여 UI가 겹칠 때 먼저 겹쳐질 순서를 정할 수 있다.

<img width="688" height="720" alt="Image" src="https://github.com/user-attachments/assets/a18d7e40-9362-4029-a24d-ccf7ef1e894b" />

**버튼**의 경우 버튼을 UI에 추가한다. 버튼에 이벤트를 연결하려면 **변수** 설정이 필요한데, 이는 디테일 패널 오른쪽 상단의 변수 여부의 체크로 해 줄 수 있다.

변수를 설정한 후, **그래프** 탭에서 버튼을 끌어와 버튼에 관련된 이벤트를 설정할 수 있다.

<img width="720" height="401" alt="Image" src="https://github.com/user-attachments/assets/adf34d58-053e-49a7-966c-6c92ff745567" />

예를 들어, **Assign On Click** 이벤트를 사용하면 **버튼 클릭 시** 특정 동작을 실행할 수 있다.

예시에서는 버튼으로 **캐릭터 점프**를 동작하게 구현하였다

### 2. 제작한 UI를 게임 화면에 연동하기

<img width="720" height="427" alt="Image" src="https://github.com/user-attachments/assets/91b2df1d-8093-4b94-9de3-13b02d44e406" />

위젯을 화면에 붙이는 방법은 CreateWidget을 통해 내가 만든 UI 블루프린트 클래스를 인스턴스화하고 

**Add to Viewport**를 연결해 화면에 나타내면 된다.

다음과 같이 이미 인스턴스가 되어있고 변수에 할당되어 있을 때에는 추가만 가능하게 Branch를 사용해서 인스턴스화를 건너뛰게 하면 효율적이다.

<img width="720" height="416" alt="Image" src="https://github.com/user-attachments/assets/18aadaaa-1477-4b23-a737-6fa5d4ab6335" />

반대로 화면에서 제거할 때에는 **Remove from Parent함수**에 내가 만든 위젯을 불러오면 된다.

<img width="720" height="475" alt="Image" src="https://github.com/user-attachments/assets/de352328-02e1-4acb-98b9-8be6b813ba15" />

이후 위에서 인스턴스된 위젯을 플레이어 캐릭터에 연결해서 게임이 시작할 때 **자동으로 실행**하게 만들어 주면 된다.

## 학습하며 겪었던 문제점 & 에러

1번 과제를 실행중에 버튼의 스태틱 메시의 hit 판정이 안되어 Box collision을 추가하여 overlap 판정으로 바꾸었다.

UI를 공부하면서 Z순서를 잘못 적어서 이미지가 텍스트보다 먼저 출력되어 텍스트가 가려졌었다. 

## 내일 할 일

내일은 사전캠프에서 제공한 블루프린트 퀘스트 1-2를 수행하는걸 목표로 설정하였다.





