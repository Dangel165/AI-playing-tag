# AI-playing-tag
# AI 술래잡기 

🚀 What's New in v2.0

### 🧬 Dual AI System
- **DNA Mode**: Traditional genetic algorithm with predefined behaviors
- **Neural Network Mode**: Deep learning agents that evolve their own strategies
- **Real-time switching**: Compare AI approaches in the same environment

### 🎮 Enhanced Game Mechanics
- **Balanced Combat**: 25 Runners vs 4 Chasers with unique abilities
- **Dynamic Environment**: Obstacles, mud zones, and destructible barricades
- **Victory Conditions**: Time-based survival or elimination-based wins
- **Game State Management**: Proper win/loss detection with auto-restart

### 🔧 Major Bug Fixes
- **Boundary Wrapping**: Agents no longer disappear at screen edges
- **Anti-Clustering**: Neural agents maintain proper spacing
- **Stuck Prevention**: Advanced pathfinding and escape mechanisms
- **Real-time Fitness**: Live performance tracking for neural networks
- **Barricade Cooldown**: Strategic building with 2-second limitations

---

## Motivation / 개발 이유
* English: This project was inspired by Unity-based AI Tag simulation videos. I wanted to see if I could recreate it using pure JavaScript.
* 한국어: 유니티 AI 술래잡기 동영상을 보다가 한번 간단하게 만들어보고 싶어서 만들었습니다.

---

## Tech Stack / 기술 스택
* Language: JavaScript (ES6+)
* Graphics: HTML5 Canvas API
* Design: CSS3
* Environment: Web Browser

---

## Main Algorithms / 주요 알고리즘
* Steering Behaviors: Seek(추격), Flee(도망), Avoidance(장애물 회피)
* Genetic Algorithm: 상위 5마리 DNA 복제 및 변이 진화
* Ray-casting: 장애물 감지 센서 기술
* Flocking: 도망자 간 분산(Separation) 로직

---

## Chaser Logic (술래 조건) - 2025.12.31 Update
* Targeting: 가장 가까운 도망자 추격
* XP System: 포획 시 레벨업 및 속도 +0.05 상승
* Fatigue: 추격 시 속도 저하, 포획 시 초기화
* Deadlock Prevention: 40프레임 이상 끼일 경우 경로 재탐색
* Special States:
    * Respawn: 술래 사망 후 인원 4명 미만 시 Lv.10으로 부활
    * Berserk: 최후의 1인 생존 시 속도 7.5 상승 및 바리케이드 파괴
    * Weakness: 중앙 Mud Zone 진입 시 속도 25%로 감소

---

## Evader Logic (도망자 조건)
* Energy: 초당 일정량 소모, 0이 되면 사망
* Dash: 술래 근처(80px) 시 에너지를 소모해 속도 1.8배 상승
* Flocking: 동료와 모여 있을 때 속도 최대 2.5 추가 상승
* Cooperation:
    * 술래 사냥: 3마리 이상 근처(80px) 시 술래 제거 가능
    * 동료 부활: 전체 먹은 음식 12개당 죽은 동료 1명 부활
* Defense:
    * Barricade: 술래 근처 시 설치 (Mud Zone 내부 설치 금지)
    * Hide: 장애물 뒤로 은신 시도

---

## How to Run / 실행 방법
1. Clone the repository:
   ```bash
   git clone [https://github.com/Dangel165/AI-playing-tag.git](https://github.com/Dangel165/AI-playing-tag.git)
