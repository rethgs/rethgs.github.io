---
date: 2018-06-08 12:00:00 +0900
title: 순수 지킬에 대하여
excerpt: 테마 없이 지킬 사용하기 - 1 - 순수 지킬 시작
---
## 준비
* 지킬은 ruby 기반으로 실행되기 때문에 다음을 미리 설치
* 미리 설치를 했을 수도 있으므로 버전 확인
'''
$ jekyll -v
'''
* -v 는 버전 확인
  * --version과 같다
* 설치 가이드: http://jekyllrb-ko.github.io/docs/installation/

## 일단 실행
* 깃헙에서 빈 저장소 하나 생성 후 로컬에 동기화
* 놀랍게도 바로 실행은 됨
  * 그러나 설정한 것이 아무 것도 없으므로, 비어 있는 디렉토리만 보임
* 지킬 실행
'''
$ jekyll serve
'''

## 권장 인덱스 파일: index.html
* index.html이나 index.md를 일단 생성
  * 두 파일이 모두 있으면, index.md가 우선시됨
* index.html
  * 시작에 ---를 이용해 yml 문법으로 표시를 해두면, 지킬이 컴파일을 해줌
  * 없으면 파일을 그대로 사용하기 때문에, 지킬이 제공하는 기능을 사용할 수 없음
* index.md
  * 반드시 ---를 이용해 지킬 파일임을 명시해야 함
* 페이지 작성 가이드: https://jekyllrb-ko.github.io/docs/posts/

## 권장 설정 파일: \_config.yml
* 설정 파일을 만들어 관리하는 것을 추천
  * 기본 설정 파일: \_config.yml
* 실행할 때마다 플래그 옵션을 지정하여 사용하는 것도 가능
* 기본 설정 파일 대신에 다른 설정 파일(심지어 여러 개) 지정 가능
* 처음에는 없어도 되고, 빈 파일도 괜찮음
* 실행 가이드: https://jekyllrb-ko.github.io/docs/configuration/

## 권장 favicon 파일: favicon.ico
* favicon에 대해서는 별도로 다룰 예정
* 일단은 기본 폴더에 favicon.ico가 있으면 보기 좋음

## 권장 깃 설정 파일: .gitignore
'''
\_site
.jekyll-metadata
'''
* \_site
  * 컴파일된 홈페이지가 저장되는 곳이라 보통 굳이 깃에 올릴 필요가 없음
  * 다만 일부 플러그인의 경우 깃헙 페이지에서 자동으로 처리가 안 될 때 \_site를 이용해서,
    로컬에서 컴파일 후 이 폴더를 깃에 일부러 포함시켜야 함
* .jekyll-metadata
  * 빌드를 효율적으로 하기 위해서 지킬 내부적으로 사용됨
* 구조 가이드: https://jekyllrb-ko.github.io/docs/structure/
