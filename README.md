# AI-playing-tag
# AI 술래잡기

---

## Motivation / 개발 이유
* English: This project was inspired by Unity-based AI Tag simulation videos. I wanted to see if I could recreate complex intelligent behaviors and evolutionary logic using pure JavaScript and HTML5 Canvas in a web environment.
* 한국어: 유튜브에서 유니티(Unity)로 제작된 AI 술래잡기 영상을 보고, 자바스크립트만으로도 저런 복잡한 지능형 로직과 진화 시스템을 간단하게 구현해볼 수 있지 않을까 하는 궁금증에서 시작되었습니다.

---

## Tech Stack / 기술 스택
* Language: JavaScript (ES6+) - Handles core AI logic, physics, and game loop.
* Graphics: HTML5 Canvas API - 2D graphic rendering.
* Design: CSS3 - UI design and animations.
* Environment: Web Browser - Runs instantly on Chrome, Edge, etc., without installation.

---

## Main Algorithms / 주요 알고리즘

### 1. Steering Behaviors (조향 행동)
* Seek: Target-oriented acceleration. / 목표를 향해 가속.
* Flee: Moving away from threats. / 술래로부터 도망.
* Avoidance: Detecting and bypassing obstacles using sensors. / 장애물을 감지하고 회피함.

### 2. Genetic Algorithm (유전 알고리즘)
* DNA Inheritance: Top 5 longest-surviving individuals pass their stats to the next generation.
* Mutation: New generations evolve with slight variations in speed and vision based on their parents' DNA.
* 진화 로직: 우수한 개체의 DNA를 복제하고 변이를 통해 더 최적화된 다음 세대를 생성함.

### 3. Ray-casting (레이캐스팅)
* Intelligent sensor technology using invisible lasers to detect walls in advance.
* 보이지 않는 레이저를 쏴서 전방의 장애물을 미리 감지하는 지능형 센서 기술.

---

## Chaser Logic (술래 조건) - 2025.12.31 Update

* Targeting: Automatically tracks the nearest living evader. / 살아있는 도망자 중 가장 가까운 개체를 추격.
* Experience System (XP): Levels up per catch; permanent speed increase of 0.05 per level.
* Fatigue: Speed decreases over time during chase; resets to 0 upon catching a target.
* Deadlock Prevention: Recalculates path if stuck in obstacles for over 40 frames.
* Special States:
    * Respawn: Respawns as a powerful Lv.10 unit if the chaser count drops below 4.
    * Berserk: Activated when only 1 evader remains. Speed increases to 7.5 and destroys barricades.
    * Weakness: Speed drops to 25% of normal when entering the central Mud Zone.

---

## Evader Logic (도망자 조건)

* Energy: Consumed over time; the unit dies if energy reaches 0. / 에너지가 없으면 굶어 죽음.
* Dash: 1.8x speed boost when the chaser is within 80px. / 술래 접근 시 에너지를 소모해 가속.
* Flocking: Moving with allies provides a psychological speed boost up to 2.5. / 동료와 모여 있을 때 속도 상승.
* Cooperation:
    * Chaser Hunting: If 3+ evaders gather near the chaser (80px), they can eliminate the chaser.
    * Revival: Revives 1 dead ally for every 12 food items collected by the group.
* Defense:
    * Barricade: Deploys walls when the chaser is nearby (Prohibited in Mud Zone).
    * Hide: Tends to hide behind obstacles to avoid the chaser's line of sight.

---

## How to Run / 실행 방법
1. Clone the repository / 저장소 클론:
   ```bash
   git clone [https://github.com/Dangel165/AI-playing-tag.git](https://github.com/Dangel165/AI-playing-tag.git)
