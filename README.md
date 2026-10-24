# chajajwo-meals-data

서울대 식단 스냅샷. GitHub Actions가 하루 한 번(한국 시간 06:30) 학교 식단 페이지를 읽어 `meals.json`을 갱신합니다.

- 기간: 오늘 기준 과거 30일 ~ 앞으로 14일. 학교가 아직 올리지 않은 날짜는 비어 있습니다.
- 앱 주소: `https://raw.githubusercontent.com/myunlee133-beep/chajajwo-meals-data/main/meals.json`
- 형식: `schemaVersion 1`. `menus[].date`가 `null`이면 매일 같은 고정 메뉴입니다.
- 크롤러: `src/chajwo_meals`, 스냅샷 생성: `scripts/build_snapshot.py`. 로컬 실행: `python scripts/build_snapshot.py meals.json`
