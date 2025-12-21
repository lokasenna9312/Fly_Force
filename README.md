# Fly Force
My 1st product by Unity. A space shooting game.

Korean Announcement
------------------------------------------------------------
Written by Myself.

[ 조작법 ]
------------------------------------------------------------
캐릭터 이동 : 방향키 또는 WASD
공격 : 왼쪽 Shift 또는 마우스 왼쪽 버튼
실드 : 왼쪽 Ctrl 또는 마우스 가운데 버튼
폭탄 : Spacebar 또는 마우스 오른쪽 버튼
조이스틱으로도 조작할 수 있도록 코드는 짜놨는데, 테스트는 아직 안 해봤습니다.

[ 시스템 ]
------------------------------------------------------------
1. 보스 출현
   - 보스가 없는 상태에서 5번의 웨이브가 진행되면 보스가 출현합니다.

2. 잔기 시스템
   - 2개의 잔기를 갖고 게임을 시작합니다.
   - 보스를 격추햇을 때 잔기가 2개보다 적다면 1개의 잔기가 추가됩니다.

3. 실드 원리
   - 실드는 실드 키를 다시 눌러서 수동으로 해제하지 않으면 3초간 지속됩니다.
   - 실드가 작동중일 때는 공격하거나 아이템을 얻을 수 없습니다.
   - 실드에 의해 격추된 적은 점수를 제공하지 않습니다.
   - 리스폰 시에도 1초간 실드가 작동됩니다. 이것도 수동으로 해제할 수 있습니다.

4. 감점 상황
   - 실드를 작동시킬 때.
   - 총알이나 폭탄이 아무런 적도 맞히지 못하고 화면에서 사라질 때.

[ 저작권 공지 ]
------------------------------------------------------------

0. 본 게임은 자유 소스로 개발한 Lokasenna의 저작물임을 밝히며, CC BY SA 4.0 저작권을 설정합니다.

1. 본 게임은 인프런의 게이머TV님이 업로드하신 ["2. 유니티가 어려운 입문자를 위한 입문용 게임 제작" 강의](https://www.inflearn.com/course/%EA%B2%8C%EC%9D%B4%EB%A8%B8tv-%EC%9C%A0%EB%8B%88%ED%8B%B0-%EC%9E%85%EB%AC%B8-%EA%B2%8C%EC%9E%84%EC%A0%9C%EC%9E%91/dashboard)와, 구글 제미나이 AI와의 질문답변을 통해 제작한 게임입니다.


2. 에셋 습득처
 - 실드 관련 효과음 : [Unity Asset Store의 Retro Sci-Fi Pack](https://assetstore.unity.com/packages/audio/sound-fx/retro-sci-fi-pack-61781) 중 다음의 2개 파일
    - /Compressed/Medium swell 03.ogg
    - /Compressed/Medium swell 01.ogg
 - 게이머TV님이 위 강의에서 제공해주신 에셋들 : 그림 애셋은 게이머TV님이 직접 만드신 거라고 합니다.
 - Open Game Art의 에너지 실드 사진 : https://opengameart.org/content/shield-effect
 - 아이템 획득 사운드 : https://freesound.org/people/GabrielAraujo/sounds/242501/
 - 폭발음 : https://freesound.org/people/bareform/sounds/218721/
 - 적 기체 탄환 피격음 : https://freesound.org/people/Rudmer_Rotteveel/sounds/336005/
 - 재가공된 소스
     - [Laser by Daleonfire](https://freesound.org/people/Daleonfire/sounds/376694/) 사운드 소스
     - [Laser Machine Gun by Sonically](https://freesound.org/people/sonically_sound/sounds/612875/) 사운드 소스
     - [Explosion2](https://freesound.org/people/steveygos93/sounds/80401/) 사운드 소스
 - 게임 화면 BGM : https://freemusicarchive.org/music/8bit_Betty/too_bleep_to_bloop/hc152_04_spooky_loop_by_8bit_betty/

3. 직접 작성한 요소
 - 실드의 작동에 관련된 코드
 - 총알이 자신이 가진 공격력이 다 소진될 때까지 적을 관통하는 요소
 - 폭탄이나 기본 무장으로 적을 한 마리도 맞추지 못할 경우 감점되는 요소
 - 보스의 애니메이션에 관련된 컨트롤러 코딩
 - Stage No. 출력 (보스를 격퇴할 때마다 1씩 올라갑니다.)
 - HighScore 리셋, 현재 점수가 HighScore보다 높을 때 표시하는 기능
 - 클래스 캡슐화
 - 일반공격의 레벨과 대미지를 별개의 변수로 관리하기
 - 격추된 플레이어가 행동을 하지 못하게 만들기
 - 플레이어의 탄환이 화면에서 모두 사라져야 게임오버 화면이 나오게 만들기
 - 격추된 플레이어의 기체가 관성에 의해서 격추 직전의 운동 상태를 유지하게 만들기

English Announcement
------------------------------------------------------------
Translated and Formatted by Google Gemini.

[ CONTROLS ]
------------------------------------------------------------
- Movement : Arrow Keys or W, A, S, D
- Attack   : Left Shift or Left Button of Mouse 
- Shield   : Left Ctrl or Middle Button of Mouse 
- Bomb     : Spacebar or Right Button of Mouse 
Not tested yet if this game is playable with JoyStick despite I coded to make it be able to.

[ GAME SYSTEM ]
------------------------------------------------------------
1. Boss Encounter
   The boss appears after surviving 5 waves while no boss is 
   currently on the map.

2. Life System
   - You start the game with 2 lives.
   - If you have fewer than 2 lives after defeating a boss, 
     1 extra life is granted.

3. Shield Mechanics
   - The shield lasts for 3 seconds unless manually deactivated 
     by pressing the shield key again.
   - While the shield is active, you cannot attack or pick up items.
   - Defeating enemies with the shield will not grant points.
   - Shield will be active for 1 second when respawned. It can be turned off manually too.

4. Points Deduction
   - When the shield is activated.
   - When a bullet or bomb leaves the screen without hitting any enemies.


[ COPYRIGHT & CREDITS ]
------------------------------------------------------------
0. License
   This game is an original work by Lokasenna9312, developed 
   using open-source resources, and is licensed under 
   CC BY-SA 4.0.

1. Credits
   This project was created through the following resources:
   - Lecture: ["Entry-level Game Production for Beginners"](https://www.inflearn.com/course/%EA%B2%8C%EC%9D%B4%EB%A8%B8tv-%EC%9C%A0%EB%8B%88%ED%8B%B0-%EC%9E%85%EB%AC%B8-%EA%B2%8C%EC%9E%84%EC%A0%9C%EC%9E%91/)
     by GamerTV (Inflearn)     
   - Technical Assistance: Q&A with Google Gemini AI.

2. Asset Sources
   - Shield SFX: These 2 files below in [Retro Sci-Fi Pack (Unity Asset Store)](https://assetstore.unity.com/packages/audio/sound-fx/retro-sci-fi-pack-61781) are used.
       - /Compressed/Medium swell 03.ogg
       - /Compressed/Medium swell 01.ogg
   - Game Sprites: Provided by GamerTV (Original art by GamerTV).
   - Shield Sprite: [Energy Shield Effect (OpenGameArt)](https://opengameart.org/content/shield-effect)
   - Item Pickup SFX: https://freesound.org/people/GabrielAraujo/sounds/242501/
   - Explosion SFX: https://freesound.org/people/bareform/sounds/218721/
   - Enemy Hit SFX: https://freesound.org/people/Rudmer_Rotteveel/sounds/336005/
   - Remixed SFX Sources:
     * Laser by Daleonfire: https://freesound.org/people/Daleonfire/sounds/376694/
     * Laser Machine Gun by Sonically: https://freesound.org/people/sonically_sound/sounds/612875/
     * Explosion2 by steveygos93: https://freesound.org/people/steveygos93/sounds/80401/
   - In-game BGM: [Spooky Loop by 8bit Betty](https://freemusicarchive.org/music/8bit_Betty/too_bleep_to_bloop/hc152_04_spooky_loop_by_8bit_betty/)


[ ORIGINAL IMPLEMENTATION (CUSTOM CODE) ]
------------------------------------------------------------
The following features were personally developed and implemented:
- Shield mechanics and state logic.
- Piercing bullet system (bullets penetrate based on damage capacity).
- Score penalty system for missed shots and bomb usage.
- Boss animation controller coding.
- Stage tracking system (increments after boss defeat).
- High Score system (reset functionality and new high score display).
- Class encapsulation and code refactoring.
- Independent variable management for attack levels and damage.
- To make fallen player not be available to do actions.
- To make GameOver scene only occurs when all of player's bullet are vanished from game scene.
- To make the dead player's vessel move by inertia maintaining its pre-destruction momentum.
