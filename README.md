# [AR] 건축 AR 시뮬레이션 프로그램


</br>

## :memo: 목차

- [프로젝트 개요](#프로젝트-개요)
- [핵심 기술 구현](#핵심-기술-구현)
- [시연 영상](#시연-영상)
- [회고록](#회고록)
- [참고자료](#참고자료)

</br>

# 프로젝트 개요

|제목|건축 AR 시뮬레이션 프로그램|
|:------:|---|
|장르 | AR 산업|
|개발기간 | 10|
|개발도구 |Unity (2022.3.2f1), Vuforia|
|사용언어 |C#|
|플랫폼 |모바일|
|팀원 |4명|
|기획의도| - 카메라로 인식한 2D 도면에 해당하는 3D 모델링을 AR로 출력 <br> -  UGUI를 활용하여 부분별 살펴보기, 단면도 보기, 공정별 보기 기능이 가능한 테블릿 전용 건축 AR 시뮬레이션 프로그램 제작

</br>

# 핵심 기술 구현

### :ballot_box_with_check: 2D 도면 인식 후 해당 3D 모델링 생성
- Vuforia plugin을 활용하여 이미지 타겟팅으로 도면별 3D 모델링 띄우기 가능

### :ballot_box_with_check: UI 토글 및 버튼, 공정 슬라이더 기능 구현
- 원하는 부분만 볼 수 있도록 UI 토글을 활용하여 모델링별 활성화 제어 기능
- Reset / Delete /Phase(공정) 버튼과 토글 활성화 기능이 상호작용하도록 설계하여 원클릭 전체 제어 기능
- Phase 버튼을 키면 슬라이더를 활용하여 공정 단계별(1~4단계) 이미지 확인 가능

### :ballot_box_with_check: ResourceManager로 공유되는 리소스 관리
- 버튼과 토글, 슬라이더 스크립트에서 함께 공유하는 게임 오브젝트와 UI 오브젝트를 싱글톤으로 만든 ResourceManager에서 관리하여 중복 코드를 줄이고 유지 보수의 용이성을 높임.

</br>

# 시연 영상

- 영상 링크: https://www.youtube.com/watch?v=JlwMx1OHJJU&feature=youtu.be

</br>
# 회고록

