---
title: "Android 휴대폰으로 홈 서버 만들기"
date: 2022-02-26T10:24:02+09:00
draft: false
---

집에서 추가적인 비용없이 가지고 놀 서버가 있으면 좋겠다는 생각을 하고 있다가 전에 사용하던 Android 휴대폰으로 만들어보기로 했다.

일단 로컬에 Docker로 사용하던 Postgresql을 옮기는걸 목표로 셋팅해봤다.

# 사용기기

- Sharp Aquos S3
- 퀄컴 스냅드래곤 630 SDM630 Platform (2.2 GHz)
- 4 GB LPDDR4X SDRAM, 64 GB
- Android 10

# Termux

`F-Droid`를 이용해서 `Termux` 를 설치해주면 Linux 환경을 사용할 수 있게된다.

- [https://medium.com/junior-dev/how-to-re-purpose-your-old-android-phone-by-running-linux-on-it-1310df46b3fe](https://medium.com/junior-dev/how-to-re-purpose-your-old-android-phone-by-running-linux-on-it-1310df46b3fe)

이 페이지를 따라서 ssh server 셋팅까지만 따라했다. 여기서 셋팅하는 Ubuntu에서는 제대로 셋팅되는게 하나도 없어서 포기했다.

# Postgresql

`Termux` 앱에서 계속 타이핑하긴 힘드니 셋팅해둔 ssh로 접근해서 계속 셋팅을 해줬다.

```bash
pkg install postgresql
```

- [https://gist.github.com/nairacalm/c0b392cf15e8a656ffeb3b62a116d129](https://gist.github.com/nairacalm/c0b392cf15e8a656ffeb3b62a116d129)

설치 후 위 링크를 따라서 계정과 DB를 만들어주었다. 이 상태로 데스크탑에서 접근해도 외부 접속이 막힌 상태라 변경해줘야 한다.

- [https://www.bigbinary.com/blog/configure-postgresql-to-allow-remote-connection](https://www.bigbinary.com/blog/configure-postgresql-to-allow-remote-connection)

`postgresql.conf`와 `pg_hba.conf`를 수정 후 `Postgresql`를 재시작해주면 외부 접근이 가능해졌다.

# 그리고..

이제 서버가 되었으니 IP를 고정시켜 두었다. 일단은 Postgresql 서버로만 사용하고 있는데 나중엔 cron도 몇개 셋팅해서 돌려볼 예정이다.

Postgresql 데이터 이전하면서 확인해보니 속도도 나쁘지 않은것 같다. 초당 10만 로우 정도는 insert되는 것 같았다. 소프트웨어 적인 불편함이 좀 있을 수 있지만 집에서 남는 안드로이드 폰이 라즈베리파이보다 가성비가 좋을 것다.(배터리 내장으로 정전 사태에도 안전할듯)

Docker를 Termux 위에 사용방법이 있는데 느린것 같아 아직은 잘 모르겠다. Docker로 돌아가는 서버가 필요한 상황이면 AWS를 사용하는게 정신건강에 좋을 것 같다..

### Refs

- [https://f-droid.org](https://f-droid.org/)
- [https://medium.com/junior-dev/how-to-re-purpose-your-old-android-phone-by-running-linux-on-it-1310df46b3fe](https://medium.com/junior-dev/how-to-re-purpose-your-old-android-phone-by-running-linux-on-it-1310df46b3fe)
- [https://gist.github.com/nairacalm/c0b392cf15e8a656ffeb3b62a116d129](https://gist.github.com/nairacalm/c0b392cf15e8a656ffeb3b62a116d129)
- [https://www.bigbinary.com/blog/configure-postgresql-to-allow-remote-connection](https://www.bigbinary.com/blog/configure-postgresql-to-allow-remote-connection)