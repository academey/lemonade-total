<!-- Improved compatibility of back to top link: See: https://github.com/othneildrew/Best-README-Template/pull/73 -->
<a name="readme-top"></a>
<!--
*** Thanks for checking out the Best-README-Template. If you have a suggestion
*** that would make this better, please fork the repo and create a pull request
*** or simply open an issue with the tag "enhancement".
*** Don't forget to give the project a star!
*** Thanks again! Now go create something AMAZING! :D
-->



<!-- PROJECT SHIELDS -->
<!--
*** I'm using markdown "reference style" links for readability.
*** Reference links are enclosed in brackets [ ] instead of parentheses ( ).
*** See the bottom of this document for the declaration of the reference variables
*** for contributors-url, forks-url, etc. This is an optional, concise syntax you may use.
*** https://www.markdownguide.org/basic-syntax/#reference-style-links
-->
[![Contributors][contributors-shield]][contributors-url]
[![Forks][forks-shield]][forks-url]
[![Stargazers][stars-shield]][stars-url]
[![Issues][issues-shield]][issues-url]
[![MIT License][license-shield]][license-url]



<!-- PROJECT LOGO -->
<br />
<div align="center">
  <a href="https://github.com/othneildrew/Best-README-Template">
    <img width="240" alt="image" src="https://github.com/othneildrew/Best-README-Template/assets/14977613/345e5e7e-ecea-4a66-a2bc-2c1ba6dbbe6a">
  </a>

  <h3 align="center">Lemonade nuxt.js & spring</h3>

  <p align="center">
    nuxt.js 와 spring을 기반으로 동작하는 웹 어플리케이션 제작 및 Docker 컨테이너 구성
  </p>
</div>

<!-- ABOUT THE PROJECT -->
## About The Project
<img width="600" alt="스크린샷 2024-01-02 오전 3 32 24" src="https://github.com/othneildrew/Best-README-Template/assets/14977613/6844810b-6041-47de-ae95-81a448a3f342">

로그인 및 게시글 CRUD 기능을 제공하는 웹어플리케이션입니다.

[서버 레포](https://github.com/academey/lemonade-api)
[웹 레포](https://github.com/academey/lemonade-web)

위의 레포들은 각각 github packages 에 이미지를 배포하고 있으며, 해당 레포(lemonade-total) 에서는 이를 nginx reverse proxing 설정과 레디스를 같이 띄워서 어플리케이션을 전체 구동시키는 역할을 하고 있습니다.


### Built With
- Nuxt
- Spring
- Spring Security
- Spring Validation
- h2
- Redis (세션관리를 위해 사용)
- nginx


<!-- GETTING STARTED -->
## Getting Started

로컬에서 해당 프로덕트를 실행하기 위한 설정입니다.

### Prerequisites
docker-compose 가 설치되어 있어야 합니다.

### Installation


1. 다음과 같이 hosts 파일 설정 
   ```sh
   sudo vi /private/etc/hosts

   ... 아래 설정 추가
   127.0.0.1       lemonade.api.com
   127.0.0.1       lemonade.web.com
   ```
2. docker 실행
    ```sh
   docker-compose up
   ```
3. http://lemonade.web.com 에 접속 후 테스트
<img width="400" alt="스크린샷 2024-01-02 오전 3 20 02" src="https://github.com/academey/lemonade-total/assets/14977613/b6e46369-0472-4184-b91d-71a07db2bfa3">

4. API 에 대해 테스트하고 싶다면 [Lemonade Postman](https://www.postman.com/blue-spaceship-2858/workspace/lemonade-api) 을 이용하는 것이 편리합니다.

<!-- USAGE EXAMPLES -->
## Usage
### 현재 서버에서 제공하는 기능들
1. 로그인 및 회원가입 (레디스 세션)
2. Post CRUD
3. 권한에 따른 제어

### 현재 웹에서 제공하는 기능들
1. 로그인 및 회원가입
2. Post Read
3. 권한에 따른 제어

<!-- ROADMAP -->
## Roadmap
- [ ] 웹에서 Post Popup 방식으로 리스트 화면에서 Update, Delete 기능 제공하기
- [ ] 웹 API 쪽 인터페이스 작업 추가 및 최적화
- [ ] Nginx 설정 최적화 (static resource 등등)
- [ ] Post List API 에 대한 캐싱


<!-- LICENSE -->

## 프로젝트에 대한 스크린샷
### 1. 로그인
<img width="300" alt="스크린샷 2024-01-02 오전 3 20 02" src="https://github.com/academey/lemonade-total/assets/14977613/09169b1b-77cf-43b8-bc5d-67280d8846de">

### 2. 회원가입
<img width="300" alt="스크린샷 2024-01-02 오전 3 20 06" src="https://github.com/academey/lemonade-total/assets/14977613/418001bf-3fc1-4a1f-a9fa-45d010cb5fd0">

### 3. 게시글 리스트
<img width="300" alt="스크린샷 2024-01-02 오전 3 20 16" src="https://github.com/academey/lemonade-total/assets/14977613/15ba4c8d-24d2-4f00-a48e-9927f66b7717">

### 4. 게시글 디테일 (남의 게시글일 때 수정, 삭제 버튼 미노출)
<img width="300" alt="스크린샷 2024-01-02 오전 3 20 26" src="https://github.com/academey/lemonade-total/assets/14977613/ae72c832-e1ce-4f05-a8f9-f4e9b2c35c55">

### 5. 게시글 디테일 (나의 게시글이거나 ADMIN일 때 수정, 삭제 버튼 노출)
<img width="300" alt="스크린샷 2024-01-02 오전 3 20 48" src="https://github.com/academey/lemonade-total/assets/14977613/f144900b-05a6-4e23-9f20-65989e480d1e">

### 6. reverse proxy 설정
<img width="500" alt="스크린샷 2024-01-02 오전 3 32 24" src="https://github.com/academey/lemonade-total/assets/14977613/3ab8a154-1ee4-45a9-944b-fd2a2ceb21d1">


## License

Distributed under the MIT License. See `LICENSE.txt` for more information.

<p align="right">(<a href="#readme-top">back to top</a>)</p>




<!-- MARKDOWN LINKS & IMAGES -->
<!-- https://www.markdownguide.org/basic-syntax/#reference-style-links -->
[contributors-shield]: https://img.shields.io/github/contributors/academey/lemonade-total.svg?style=for-the-badge
[contributors-url]: https://github.com/academey/lemonade-total/graphs/contributors
[forks-shield]: https://img.shields.io/github/forks/academey/lemonade-total.svg?style=for-the-badge
[forks-url]: https://github.com/academey/lemonade-total/network/members
[stars-shield]: https://img.shields.io/github/stars/academey/lemonade-total.svg?style=for-the-badge
[stars-url]: https://github.com/academey/lemonade-total/stargazers
[issues-shield]: https://img.shields.io/github/issues/academey/lemonade-total.svg?style=for-the-badge
[issues-url]: https://github.com/academey/lemonade-total/issues
[license-shield]: https://img.shields.io/github/license/academey/lemonade-total.svg?style=for-the-badge
[license-url]: https://github.com/academey/lemonade-total/blob/master/LICENSE.txt
