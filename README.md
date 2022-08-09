# 요구사항 분석

- 목록 화면에서 영화의 제목과 이미지 하나, 영화 리뷰의 평점/리뷰 개수를 출력
- 영화 조회 화면에서 영화와 영화의 이미지들, 리뷰의 평균점수/리뷰 개수를 같이 출력
- 조회 화면에서 회원은 자신이 기록한 리뷰의 내용을 수정/삭제 할 수 있다.
- 리뷰에 대한 정보에는 화의 이메일이나 닉네임과 같은 정보를 같이 출력
- 업로드된 확장자가 이미지만 가능하도록 검사
- 동일한 이름의 파일이 업로드 되면 기존 파일을 덮어쓰는 문제
- 업로드된 파일을 저장하는 폴더의 용량
- 업로드된 파일을 저장하고 섬네일 라이브러리를 활용해서 섬네일 파일을 만들어 준다
- 영화(Movie)의 등록과 수정에는 파일 업로드 기능을 활용해서 영화 포스터 등을 등록
- 회원(Member)은 기존 회원들이 존재한다고 자정하고 데이터베이스에 존재하는 회원들을 이용
- 회원은 특정한 영화 조회 페이지에서 평점과 자신의 감상을 리뷰로 기록

# API 규격서

| 방식 | URL | 설명 |
| --- | --- | --- |
| GET | /reviews/영화번호/all | 해당 영화의 모든 리뷰 반환 |
| POST | /reviews/영화번호 | 새로운 리뷰 등록 |
| PUT | /reviews/영화번호/영화리뷰번호 | 리뷰 수정 |
| DELETE | /reviews/영화번호/영화리뷰번호 | 리뷰 삭제 |
| POST | /movie/register | 새로운 영화 등록 |
| GET | /movie/list | 영화 리스트 |
| GET | /movie/read | 영화 읽기 |
| GET | /movie/modify | 영화 수정 |

# 엔티티 관계도
![image](https://user-images.githubusercontent.com/109207727/183556299-6eb7e884-0e54-4021-933a-82fadfb4bc04.png)

# GIT TREE
Master 브랜치와 Dev 브랜치, Feature 브랜치로 나누었다.

Feature -> Dev -> Master 순으로 Pull Request 하였다. 

이후 Master → Feature로 이어갔다
![image](https://user-images.githubusercontent.com/109207727/183556011-f33199ea-4ec9-4b8a-b525-c39a5bd4d690.png)

# 소개

## 1.영화 리스트
![image](https://user-images.githubusercontent.com/109207727/183557060-63e3b649-bd88-41cb-b1bf-13fbef6002bf.png)

## 2. 영화등록
![image](https://user-images.githubusercontent.com/109207727/183556551-837a6f24-fa84-43d4-a5ee-0ce9caddedbc.png)

## 3. 영화리뷰 등록
![image](https://user-images.githubusercontent.com/109207727/183556656-e78f57e4-c4ae-4489-85a9-0a82579c2e16.png)


## 4. 리뷰 수정 / 삭제
![image](https://user-images.githubusercontent.com/109207727/183556729-bffee153-a45e-47cb-b65c-8eedccd3a6d7.png)

## 5. 썸네일 클릭 시 원본 이미지 출력
![image](https://user-images.githubusercontent.com/109207727/183557330-2a86a905-1676-4df7-87ee-2fcc8d6f9f33.png)
