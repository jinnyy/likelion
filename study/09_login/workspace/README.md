## Likelion at Yonsei Univ. --Study Session #09
##### - Scaffold & Devise
<br>

#### References
- https://rubykr.github.io/rails_guides/getting_started.html#Getting-Up-and-Running-Quickly-with-Scaffolding
- https://github.com/plataformatec/devise
- http://guides.rubyonrails.org/action_controller_overview.html

#### Environment
- Ruby 2.3.4
- Rails 4.2.5

<hr>
<br>


## Scaffold
- scaffold is a tool which automatically implements CRUD function.
- 스캐폴드는 CRUD 기능을 자동으로 만들어 주는 툴입니다.

<br>

터미널에 아래와 같이 입력합니다.
```
$ rails generate scaffold Post name:string title:string content:text
```
or
```
$ rails g scaffold Post name:string title:string content:text
```
스캐폴드가 Post라는 모델에 string 타입인 name과 title, text 타입인 content를 만들어줍니다.

rails g scaffold [모델이름] [속성]:[타입] [속성]:[타입] 형태

<br>

아래와 같이 입력해서 db 정보를 마이그레이트해줍니다.
```
$ rails db:migrate
```
or
```
$ rake db:migrate
```
<br>
scaffold가 생성해준 view의 index를 첫 페이지로 지정하고 싶다면

route 파일에 아래 입력
```
root 'posts#index'
```

<br>
<br>

## Devise
- 로그인 기능을 간편하게 구현해주는 gem

<br>

###### Gem 설치
Gemfile에 아래 내용 추가
```
gem 'devise'
```
이후 터미널 창에서
```
$ bundle install
```
<br>

###### 모델 생성 및 실행
USER라는 모델을 생성한다.
```
$ rails generate devise USER
```
or
```
$ rails g devise USER
```


이후

루비가 최신 버전인 경우
```
$ rails db:migrate
```
루비가 최신 버전이 아닌 경우 (c9의 default 환경)
```
$ rake db:migrate
```

여기까지 완료하면 devise gem을 사용하기 위한 환경 설정이 완료됩니다!

<br>


```

```
