https://youtu.be/1ElgyAAYoH4 슈팅게임 유튜브 주소

# Project name : RL-of-shooting-game-with-PyGame
## 프로젝트 소개
1. 파이게임으로 슈팅게임을 제작
2. 슈팅 게임을 RL(강화학습)으로 학습
3. 강화학습이 적용된 게임을 플레이

# Project information
## Requirement
1. PyGame
2. anaconda
3. tensorflow
4. numpy

# Environment
![1](https://user-images.githubusercontent.com/55978194/84865962-0b652000-b0b4-11ea-94d9-1e5f6f18d941.png)
1. 10 X 10 배열을 사용하여 구축 후 이 배열을 가지고 파이게임을 사용하여 시각적으로 제작
2. 0은 맵 1은 Agent 2는 적

# Agent
![sprite1](https://user-images.githubusercontent.com/55978194/84870916-dc05e180-b0ba-11ea-8329-0762be789882.png)
1. Environment와 상호작용을 하며 위아래 둘 중 하나의 Action을 선택
2. Action 선택 후 Enemy과 부딪히지 않았다면 Reward를 1 획득
3. 만약 Enemy와 부딪혔다면 Reward를 -10 시킨 후 Reset

# Enemy 
![enemy1](https://user-images.githubusercontent.com/55978194/84871944-26d42900-b0bc-11ea-9339-ce9ddcd60064.png)
1. Enviroment에선 2로 표현되며 1인 Agent와 부딪혔다면 Reward를 -1 시킨 후 Reset

# State
![me](https://user-images.githubusercontent.com/55978194/84872705-3011c580-b0bd-11ea-8f35-6fe8cbefac4c.png) ![you](https://user-images.githubusercontent.com/55978194/84873052-9bf42e00-b0bd-11ea-8ce1-c7dca765a945.png)
1. Agent에서 임시 환경을 만들어 낸 후 Enemy에서 완벽한 NextState를 만들어냄
![temp](https://user-images.githubusercontent.com/55978194/84873200-dc53ac00-b0bd-11ea-98bf-feed537a8dcb.png)



