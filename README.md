# :books: 온라인 도서 대여, 반납 서비스 <br> (online book rental service)

* 회원가입 기능
  + 회원만 해당 서비스를 이용할 수 있다. 모든 사용자는 회원 가입시 user 권한을 지닌다.
  + 회원가입시 아이디와 패스워드를 입력받으며, 아이디는 primary key로 설정된다.

* 로그인 기능
  + 사용자는 아이디와 패스워드를 이용해 로그일 할 수 있다. 회원가입시 입력한 아이디, 패스워드와 일치해야 한다.

* 도서 CRUD 기능
  + 신규 도서 추가, 기존 도서 정보 수정 (ISBN, 도서명, 저자, 출간일, 출판사), 기존 도서 삭제
  + 도서 검색의 경우 고유 ISBN 번호, 도서명, 저자, 출판사로 검색 가능.

* 도서 대여 기능
  + 개별 도서별로 status가 있어 대여 진행중 여부 확인. 이미 대여중이라면 대여 불가.
  + 도서 대여 기간 설정. (7, 14, 30일) 최대 30일.

* 도서 반납 기능
  + 대여 중 상태인 도서가 반납되었을 경우, 고유번호 (ISBN) 일치여부 확인 후 status를 대여가능으로 변경
  + 도서 대여 기간이 만료되었을 시 자동 만료처리. 만료일자 기준 익일 00시 만료.

* 만료 처리 기능
  + 만료 된 이후 회원이 더이상 해당 도서자료에 접근할 수 없도록 block 처리 진행. (spring-batch)

* 선호 카테고리 설정 기능
  + 도서 장르/카테고리 중 본인이 선호하는 카테고리를 설정.
  + 카테고리ID와 카테고리명으로 구성되어

* 카테고리 별 베스트셀러 TOP 10 조회 기능
  + 설정한 카테고리 별 베스트셀러 TOP 10 정보 확인.
 
* 해당 정보는 Rent Book Restful API 활용
  + (https://github.com/mamenesia/rent-book)

 # ERD
 
![ERD - Online Bookstore](https://github.com/tldnjs0911/CodeRivewStudy/assets/129709961/0d903a2e-1593-42ab-a1b6-8b57501b1785)
