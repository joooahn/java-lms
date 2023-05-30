# 학습 관리 시스템(Learning Management System)
## 진행 방법
* 학습 관리 시스템의 수강신청 요구사항을 파악한다.
* 요구사항에 대한 구현을 완료한 후 자신의 github 아이디에 해당하는 브랜치에 Pull Request(이하 PR)를 통해 코드 리뷰 요청을 한다.
* 코드 리뷰 피드백에 대한 개선 작업을 하고 다시 PUSH한다.
* 모든 피드백을 완료하면 다음 단계를 도전하고 앞의 과정을 반복한다.

## 온라인 코드 리뷰 과정
* [텍스트와 이미지로 살펴보는 온라인 코드 리뷰 과정](https://github.com/next-step/nextstep-docs/tree/master/codereview)

## Step 1
-[x] 질문 데이터를 완전히 삭제하는 것이 아니라 데이터의 상태를 삭제 상태(deleted - boolean type)로 변경한다.
-[x] 로그인 사용자와 질문한 사람이 같은 경우 삭제 가능하다.
-[x] 답변이 없는 경우 삭제가 가능하다.
-[x] 질문자와 답변글의 모든 답변자 같은 경우 삭제가 가능하다.
-[x] 질문을 삭제할 때 답변 또한 삭제해야 하며, 답변의 삭제 또한 삭제 상태(deleted)를 변경 한다.
-[x] 질문자와 답변자가 다른 경우 답변을 삭제 할 수 없다.
-[x] 질문과 답변 삭제 이력에 대한 정보를 DeleteHistory를 활용해 남긴다.

## Step 2
-[x] 과정(Course)은 기수 단위로 여러 개의 강의(Session)를 가질 수 있다.
-[x] 강의는 시작일과 종료일을 가진다.
-[x] 강의는 강의 커버 이미지 정보를 가진다.
-[x] 강의는 무료 강의와 유료 강의로 나뉜다.
-[x] 강의 상태는 준비중, 모집중, 종료 3가지 상태를 가진다.
-[x] 강의 수강신청은 강의 상태가 모집중일 때만 가능하다.
-[x] 강의는 강의 최대 수강 인원을 초과할 수 없다.

## Step 3
-[x] 앞 단계에서 구현한 도메인 모델을 DB 테이블과 매핑하고, 데이터를 저장한다.
- 