# endfield-factory-calculator

<p align="left">
  <b>🇰🇷 한국어</b> | <a href="#en"><b>🇺🇸 English</b></a>
</p>

---

## <a id="ko"></a> 🇰🇷 KO - 한국어 버전

《명일방주: 엔드필드(Arknights: Endfield)》의 통합 공업 시스템(AIC) 및 공장 자동화 콘텐츠를 위한 공용 데이터베이스 저장소입니다. 

본 프로젝트는 자원 레시피, 장비 효율, 생산 공식을 구조화된 데이터(JSON)로 관리하며, 라이트 유저용 AI 가이드(Gems)와 하드코어 유저용 시뮬레이터 웹앱의 핵심 데이터 백엔드로 활용됩니다.

### 🛠️ 투 트랙 프로젝트 에코시스템

본 데이터셋은 다음 두 가지 서비스의 심장 역할을 수행합니다.

1. **라이트 유저용 AI 챗봇 (Gemini Gems)**
   - **명칭:** `E.A.I.C.O.S`
   - **역할:** 자연어 질의응답을 통한 실시간 레시피 확인 및 가벼운 병목 현상 가이드 제공.
2. **하드코어 유저용 시뮬레이터 (자체 웹앱)**
   - **호스팅:** Cloudflare Pages (정적 웹앱)
   - **역할:** 시간 가속(배속) 스트레스 테스트, 가상 그리드 배치 빌더, 실시간 물류 정체 연산.

### 📂 데이터 구조

모든 데이터는 효율적인 관리와 확장성을 위해 3개의 JSON 파일로 분할 관리됩니다.

* `data/items.json`: 인게임 내 모든 자원/아이템의 한·영 명칭, 등급(Tier), 카테고리 및 아이콘 이미지 URL 매핑 데이터.
* `data/machines.json`: 채굴기, 용해로, 조립기 등 가공 장비의 소모 전력, 기본 가속 비율 데이터.
* `data/recipes.json`: 기계 ID와 자원 ID를 연계하여 1회 작동 시간(Cycle Time), 입력(Input), 출력(Output) 자원 수량을 정의한 제작 공식 데이터.

### 🤝 기여 방법

이 프로젝트는 전 세계 엔드필드 공장장들의 집단지성으로 유지됩니다. 
인게임 패치로 인해 수치가 변경되었거나, 오타 및 데이터 누락을 발견하셨다면 언제든 **Issue**를 생성하거나 **Pull Request (PR)**를 보내주세요!

1. 본 저장소를 Fork 합니다.
2. `data/` 폴더 내의 JSON 파일을 수정합니다.
3. 변경 사항을 Commit 후 PR을 제출해 주시면 검토 후 메인 데이터에 반영됩니다.

### ⚠️ 안내 및 면책 조항

이 툴은 《명일방주: 엔드필드》를 사랑하는 팬이 개인적인 연구와 학습, 그리고 즐거운 공장 설계를 돕기 위해 만든 비영리 목적의 팬메이드 공간입니다. 따라서 개발사인 Hypergryph 및 글로벌 배급사인 Gryphline과는 아무런 공식 제휴나 연관 관계가 없습니다.

시뮬레이터 특성상 정기적인 인게임 패치나 눈에 보이지 않는 미세한 변수 때문에 실제 게임 내 결과와는 다소 오차가 발생할 수 있습니다. 어디까지나 공장 효율을 고민하실 때 방향을 잡는 참고용 가이드로 가볍게 활용해 주시길 부탁드리며, 본 툴의 계산 결과를 신뢰하고 활용하는 과정에서 발생하는 계정 문제나 손해에 대해 제작자는 법적인 책임을 지지 않습니다.

게임 내 자원 이름과 이미지 등 모든 리소스의 저작권은 원저작권자에게 귀속되며, 상업적 이용은 절대 금지합니다. 향후 공식 퍼블리셔의 삭제 요청이나 이의 제기가 있을 경우 본 저장소와 툴은 예고 없이 즉시 수정되거나 배포가 중단될 수 있습니다.

---

## <a id="en"></a> 🇺🇸 EN - English Version

<p align="left">
  <a href="#ko"><b>🇰🇷 한국어</b></a> | <b>🇺🇸 English</b>
</p>

This is a public database repository dedicated to the Automated Industrial Complex (AIC) and factory automation content in *Arknights: Endfield*.

This project manages resource recipes, machine efficiencies, and production formulas as structured data (JSON), serving as the core data backend for both the light-user AI guide (Gems) and the hardcore-user simulator web app.

### 🛠️ Two-Track Project Ecosystem

This dataset serves as the heart of the following two services:

1. **AI Chatbot for Light Users (Gemini Gems)**
   - **Name:** `E.A.I.C.O.S`
   - **Role:** Provides real-time recipe checks and light bottleneck guidance through natural language Q&A.
2. **Simulator for Hardcore Users (Self-hosted Web App)**
   - **Hosting:** Cloudflare Pages (Static Web App)
   - **Role:** Offers time-acceleration (speed-up) stress testing, a virtual grid layout builder, and real-time logistics congestion calculation.

### 📂 Data Structure (Data Directory)

All data is split into three JSON files for efficient management and scalability.

* `data/items.json`: Mapping data for Korean/English names, Tiers, categories, and icon image URLs for all in-game resources/items.
* `data/machines.json`: Data on power consumption and base acceleration ratios for processing equipment like miners, smelters, and assemblers.
* `data/recipes.json`: Production formula data linking machine IDs and resource IDs, defining cycle times, input resources, and output resource quantities.

### 🤝 Contribution

This project is maintained by the collective intelligence of Endfield factory managers worldwide. If you notice any value changes due to in-game patches, typos, or missing data, feel free to create an **Issue** or submit a **Pull Request (PR)**!

1. Fork this repository.
2. Modify the JSON files in the `data/` folder.
3. Commit your changes and submit a PR. It will be reviewed and merged into the main data.

### ⚠️ Disclaimer & Guidelines

This is an unofficial, non-profit fan-made tool created purely out of passion to help players plan their factories in Arknights: Endfield. It is not affiliated with, endorsed by, or officially connected to Hypergryph or Gryphline.

Please note that due to regular in-game updates, patches, and hidden variables, calculation and simulation results may not perfectly match the actual gameplay. We kindly ask you to use this tool as a general guide and reference only. The creator assumes no legal responsibility for any direct or indirect issues or game account damages arising from the use of this data.

All intellectual property, resource icons, and names belong to their respective owners, Hypergryph and Gryphline. Commercial use is strictly prohibited. We fully respect these rights, and this repository will be promptly modified or removed without prior notice upon request from the official publisher.

---

## 📄 라이선스 (License)

This project is licensed under the [MIT License](LICENSE).
