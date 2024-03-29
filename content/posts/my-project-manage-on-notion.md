---
title: "내가 Notion으로 프로젝트 관리하는 방법"
date: 2022-02-24T19:35:45+09:00
draft: false
---

혼자서 프로젝트 거리로 괜찮은게 생기면 틈틈이 만드는 편이라 지금까지 생겼다가 죽은 프로젝트들이 많다. (그 중엔 제대로 된게 하나도 없다..) 혼자하는 프로젝트라도 다른 일을 하면서 진행하다 보면 어디까지 했는지 놓치기도 자주하고, 하다보면 이런저런 생각나는 것도 많아서 평소 일하는 스타일과 비슷하게 관리하면 어떨까라는 생각으로 노션을 이용해 관리하고 있다.

최근 몇개 프로젝트는 노션으로 정리하면서 해봤는데, 그러면서 만든 구조를 적어두려 한다.

- Project : 만들고 싶은거
- Todo : 해야할거
- Run : 단기목표 관리용

전 회사에서 사용했던 노션 구조를 많이 참고해서 만들었다. 처음에는 Project랑 Todo만 사용하다가 쌓이는 백로그와 완성을 위해서 해야하는 일들을 구분하기 위해서 Run이라는 단위를 만들었다. (애자일 스프린트같은?)

## Project

프로젝트에는 전체적인 그림을 그려두는 곳으로 사용한다. 어떤걸 만드는 프로젝트인지, 어떤 목표로 만드는지 적고 어떤 순서로 진행할지 간략히 쓰는 용으로 쓴다.

![Untitled](/my-project-manage-on-notion/project.png)

### Status

- Building : 구상 단계
- On going : 진행 단계
- Pending : 멈춤
- Drop : 접음

4가지 상태로 나눠서 관리하고 있다. 지금까지 완성해서 제대로된 서비스가 된 프로젝트가 없었는데 만약 서비스하는 프로젝트가 생긴다면 `Serving` 이라는 상태를 추가할 것 같다.

### Todo

Project에 종속되는 할 일들을 담는 곳 이다. Project에서 끄적인 내용들을 유형, 상태, 우선순위, 일정을 사용해서 구체적이고 세분화해서 관리한다.

![Untitled](/my-project-manage-on-notion/todo.png)

![Untitled](/my-project-manage-on-notion/todo-detail.png)

### 유형

- 작업 : Coding. 노동.
- 버그 : 이슈처리
- 검토 : 구글링하기

새롭게 만들 것들은 `작업` 으로 등록하고, 그 외 이슈관련된 것들은 `버그` 로 등록해서 분리되어 있도록 했다. `검토` 는 작업 진행 전에 광범위하게 리서치가 필요한 경우, 내용들을 정리하는 문서 역할을 느낌으로 사용했다.

### 상태

- 시작 전
- 진행 중
- 완료
- 취소

일반적인 할일 상태들

### 우선순위

- 우선순위 1~5

`우선순위 1`이 제일 급한 건이다. 할일이 많이 쌓였을 때 어떤걸 먼저 해야할지 나누는 용으로 사용된다.

### 일정

혼자하는 진행하기 때문에 일정은 그리 중요하지 않지만 너무 늘어지는 것 같아 추가해서 사용했다. 하지만 효과는 없었다..

## Run

프로젝트에 종속되게 되고, 단기간에 이루고자 하는 목표를 위해서 진행해야하는 할 일들을 묶는 역할을 하게된다. 

![Untitled](/my-project-manage-on-notion/run.png)

### Status

- Building : 구상 단계
- On Going : 진행 중
- Finish : 달성
- Pending : 보류
- Canceled : 접음

`Project`와 비슷한 구성의 `Status`를 가지도록 했다. 프로젝트의 프로젝트가 되는 개념이고, 프로젝트 발전 스텝을 구분 짓는 역할을 위해 만들었다.