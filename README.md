![move](https://user-images.githubusercontent.com/55978194/85254186-a8500080-b49a-11ea-8c0e-bc4b806491f6.gif)

# 한국어
https://youtu.be/1ElgyAAYoH4   
슈팅게임 유튜브 주소   

https://youtu.be/1ElgyAAYoH4  
シューティングゲームのYouTubeアドレス

Project name : RL-of-shooting-game-with-PyGame
=============
## Project プロジェクトの紹介
1. ファイゲームでシューティングゲームを制作
2. シューティングゲームをRL(強化学習)で学習
3. RLが適用されたゲームをプレイ

Project information
=============
## Requirement
1. PyGame
2. anaconda
3. tensorflow
4. numpy

Environment
=============
![1](https://user-images.githubusercontent.com/55978194/84865962-0b652000-b0b4-11ea-94d9-1e5f6f18d941.png)
1. 10×10配列を作った後、この配列でパイゲームを使って視覚的に制作
2. 0は Map 1は Agent 2は Enemy

Agent
=============
![sprite1](https://user-images.githubusercontent.com/55978194/84870916-dc05e180-b0ba-11ea-8329-0762be789882.png)
1. Environmentと相互作用をしながら上下二つのActionを選択
2. Actionを選択後、EnemyとぶつからなければRewardを1獲得
3. もしEnemyとぶつかったら Rewardを-30させてから Reset

Enemy 
=============
![enemy1](https://user-images.githubusercontent.com/55978194/84871944-26d42900-b0bc-11ea-9339-ce9ddcd60064.png)
1. Enviromentでは2に表現され、1に表現されるAgentとぶつかったらRewardを-30させてからReset

State, Step
=============
![me](https://user-images.githubusercontent.com/55978194/84872705-3011c580-b0bd-11ea-8f35-6fe8cbefac4c.png) ![you](https://user-images.githubusercontent.com/55978194/84873052-9bf42e00-b0bd-11ea-8ce1-c7dca765a945.png)
1. MySpriteクラスで臨時環境(board上のAgentの位置を表示)を作り出す。
2. EnemyクラスでMySpriteで作り出した臨時環境を使って完璧なNextState{board上のAgent(1)とEnemy(2)}を作り出す。
![temp](https://user-images.githubusercontent.com/55978194/84873200-dc53ac00-b0bd-11ea-98bf-feed537a8dcb.png)

Deep Q network
=============
![ss](https://user-images.githubusercontent.com/55978194/84881793-50e01800-b0c9-11ea-9d72-e6ba3aa60383.png)
1. ネットワークを構成後、Predict、Update関数生成

Replay Memory
=============
1. Agentをすぐに学習させずに一定量を保存しておいて一度に学習。

Target, Main network
=============
1. Target networkとMainnetworkを分離して学習した後、コピー

Step count
=============
![s](https://user-images.githubusercontent.com/55978194/84881456-d7482a00-b0c8-11ea-8d77-62337c35ff88.png)
1. AgentがStepを300以上したらPyGameで画面に出力
2. Stepが600以上ならゲーム開始
* * *   
* * *   
* * *
# 한국어
Project name : RL-of-shooting-game-with-PyGame
=============
## 프로젝트 소개   
1. 파이게임으로 슈팅게임을 제작
2. 슈팅 게임을 RL(강화학습)으로 학습
3. 강화학습이 적용된 게임을 플레이

Project information
=============
## Requirement
1. PyGame
2. anaconda
3. tensorflow
4. numpy

Environment
=============
![1](https://user-images.githubusercontent.com/55978194/84865962-0b652000-b0b4-11ea-94d9-1e5f6f18d941.png)
1. 10 X 10 배열을 만든 후 이 배열을 가지고 파이게임을 사용하여 시각적으로 제작
2. 0은 Map 1은 Agent 2는 Enemy

Agent
=============
![sprite1](https://user-images.githubusercontent.com/55978194/84870916-dc05e180-b0ba-11ea-8329-0762be789882.png)
1. Environment와 상호작용을 하며 위아래 둘 중 하나의 Action을 선택
2. Action 선택 후 Enemy와 부딪히지 않는다면 Reward를 1 획득
3. 만약 Enemy와 부딪혔다면 Reward를 -30 시킨 후 Reset

Enemy 
=============
![enemy1](https://user-images.githubusercontent.com/55978194/84871944-26d42900-b0bc-11ea-9339-ce9ddcd60064.png)
1. Enviroment에선 2로 표현되며 1로 표현되는 Agent와 부딪혔다면 Reward를 -30 시킨 후 Reset

State, Step
=============
![me](https://user-images.githubusercontent.com/55978194/84872705-3011c580-b0bd-11ea-8f35-6fe8cbefac4c.png) ![you](https://user-images.githubusercontent.com/55978194/84873052-9bf42e00-b0bd-11ea-8ce1-c7dca765a945.png)
1. MySprite 클래스에서 임시환경(board상의 Agent의 위치를 표시)를 만들어냄
2. Enemy 클래스에서 MySprite에서 만들어낸 임시 환경을 사용하여 완벽한 NextState{board상의 Agent(1)와 Enemy(2)}를 만들어냄
![temp](https://user-images.githubusercontent.com/55978194/84873200-dc53ac00-b0bd-11ea-98bf-feed537a8dcb.png)

Deep Q network
=============
![ss](https://user-images.githubusercontent.com/55978194/84881793-50e01800-b0c9-11ea-9d72-e6ba3aa60383.png)
1. Network를 구성 후 Predict, Update 함수 생성

Replay Memory
=============
1. Agent를 즉시 학습 시키지 않고 일정량 저장해 두었다가 한 번에 학습.

Target, Main network
=============
1. Target network와 Main network를 분리하여 학습한 후 복사

Step count
=============
![s](https://user-images.githubusercontent.com/55978194/84881456-d7482a00-b0c8-11ea-8d77-62337c35ff88.png)
1. Agent가 Step을 300 이상 했다면 PyGame으로 화면에 출력 
2. Step이 600 이상이면 게임 시작   
* * *   
* * *   
* * *
# English
https://youtu.be/1ElgyAAYoH4   
YouTube Address of Shooting Game   

Project name : RL-of-shooting-game-with-PyGame
==============
## Introduction to the
1. Produce shooting game with pie games
2. Learning reinforcement learning
3. Play the game

Project information
=============
## Requirement
1. PyGame
2. anaconda
3. tensorflow
4. numpy

Environment
=============
![1](https://user-images.githubusercontent.com/55978194/84865962-0b652000-b0b4-11ea-94d9-1e5f6f18d941.png)
1. Create a 10 X 10 array, then use this array to create visual with PyGame.
2. 0 is a map, 1 is an agent, and 2 is an enemy.

Agent
=============
![sprite1](https://user-images.githubusercontent.com/55978194/84870916-dc05e180-b0ba-11ea-8329-0762be789882.png)
1. Interact with Environment and select an action from either up or down
2. Select Action and get 1 Reward if you haven't bumped into Enemy
3. If you bumped into Enemy, -30 Rewards and then Reset

Enemy 
=============
![enemy1](https://user-images.githubusercontent.com/55978194/84871944-26d42900-b0bc-11ea-9339-ce9ddcd60064.png)
1. In Environment, it is expressed as 2, and if it encounters an agent, the reward is -30 and then reset.

State, Step
=============
![me](https://user-images.githubusercontent.com/55978194/84872705-3011c580-b0bd-11ea-8f35-6fe8cbefac4c.png) ![you](https://user-images.githubusercontent.com/55978194/84873052-9bf42e00-b0bd-11ea-8ce1-c7dca765a945.png)
1. Creating a Temporary Environment in MySprite Class
2. Create NextState using a temporary environment created by MySprite in the Enemy class
![temp](https://user-images.githubusercontent.com/55978194/84873200-dc53ac00-b0bd-11ea-98bf-feed537a8dcb.png)

Deep Q network
=============
![ss](https://user-images.githubusercontent.com/55978194/84881793-50e01800-b0c9-11ea-9d72-e6ba3aa60383.png)
1. Create a Predict, Update function after configuring the network

Replay Memory
=============
1. Save a certain amount of agent and learn them all at once

Target, Main network
=============
1. Create a Target network and the Main network separately and then paste the Target network into the Main network after learning it.

Step count
=============
![s](https://user-images.githubusercontent.com/55978194/84881456-d7482a00-b0c8-11ea-8d77-62337c35ff88.png)
1. Output on screen with PyGame if agent step is 300 or more 
2. Start the game if Step is over 600 

