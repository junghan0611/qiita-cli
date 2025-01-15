[!Qiita CLI](https://qiita-image-store.s3.ap-northeast-1.amazonaws.com/0/88/92b6e4ce-4803-b06e-2d56-e7a9507c612f.png)

## Qiita CLI, Qiita Preview에 오신 것을 환영합니다!

Qiita CLI는 손 안의 환경에서 기사 작성, 미리보기, 투고를 할 수 있는 도구입니다. Qiita CLI를 사용하면 평소 사용하던 편집기 등을 사용하여 쉽게 기사를 작성하고 게시할 수 있습니다.

## 이용 전

Qiita CLI, Qiita Preview를 이용하시면 [이용약관](https://qiita.com/terms), [개인정보보호정책](https://qiita.com/privacy)에 동의한 것으로 간주합니다.

이 기사 링크도 참고하세요

-   [커뮤니티 가이드라인](https://help.qiita.com/ja/articles/qiita-community-guideline)
-   [좋은 기사를 쓰기 위한 가이드라인](https://help.qiita.com/ja/articles/qiita-article-guideline)
-   [Markdown 표기법 치트시트](https://qiita.com/Qiita/items/c686397e4a0f4f11683d)

#### 스타의 부탁

조금이라도 관심이 생기거나 실제로 사용해보고 Qiita CLI가 유용하다고 느끼셨다면 GitHub 리포지토리에 별을 달아주시면 감사하겠습니다. 별을 달아주시면 개발 동기부여가 되고, 더 좋은 도구를 여러분께 제공할 수 있는 힘이 됩니다.

#### 기사 투고 요청 📝 기사 투고 부탁

Qiita CLI를 사용하여 기사를 작성할 수 있다면, Qiita에 꼭 투고해 보세요. 게시된 기사는 많은 사람들에게 도움이 되고, 지식이 공유될 수 있는 기회가 될 것입니다. 어떤 사소한 내용이라도 괜찮으니, 부담 없이 글을 올려주세요🙇♂️

[Qiita CLI 관련 기사](https://qiita.com/search?sort=created&q=%22Qiita+CLI%22)

#### 👉🏻 질문 및 피드백에 대해

더 많은 피드백을 받으면 여러분에게 도움이 되는 기능을 계속 추가할 수 있습니다.

-   자주 묻는 질문 등을 기재하고 있습니다 → [FAQ](https://github.com/junghan0611/qiita-cli/tree/main#FAQ)
-   문제나 의견이 있으시면 [Qiita Discussions](https://github.com/increments/qiita-discussions/discussions)에 올려주시기 바랍니다.

## Qiita CLI 도입 방법

### 1\. 사전 준비

Qiita CLI를 사용하려면 `Node.js 18.18.0` 이상이 필요합니다.  
Node.js를 처음 사용하는 경우 Node.js를 설치해야 합니다.

### 2\. Qiita CLI 설치하기

Qiita의 콘텐츠를 관리하고자 하는 디렉토리에서 다음 명령을 실행합니다.

```shell
npm install @qiita/qiita-cli --save-dev
```

아래 명령어로 버전이 표시되면 설치가 완료된 것입니다.

### 3\. Qiita CLI 업데이트하기

Qiita CLI를 업데이트하려면 다음 명령을 실행합니다.

```shell
npm install @qiita/qiita-cli@latest
```

## Qiita CLI 설정 방법

### init 명령 실행하기

아래 명령어를 실행하면 된다,

-   .lord
-   GitHub Actions의 워크플로우 파일
    -   'GitHub에서 문서 관리하기' 항목 참조
-   사용자 설정 파일(qiita.config.json)
    -   '사용자 설정 파일에 대하여' 항목 참조

가 생성됩니다.

### Qiita 토큰 발행하기

아래 흐름에 따라 토큰을 발행해 주세요.

-   [https://qiita.com/settings/tokens/new](https://qiita.com/settings/tokens/new?read_qiita=1&write_qiita=1&description=qiita-cli) 에 로그인한 상태로 접속합니다.
    -   토큰의 권한은 'read\_qiita'와 'write\_qiita'를 설정합니다.

발행한 토큰은 `Qiita CLI 로그인`, `GitHub에서 글 관리하기`에서 사용합니다.

### Qiita CLI 로그인

아래 명령어를 통해 발행한 토큰을 등록합니다.

```shell
発行したトークンを入力: トークンを入力しEnterキーを押す
Hi ユーザー名!
```

토큰을 등록하면 Qiita의 계정과 연동되어 기사 검색, 게시, 업데이트가 가능해진다.

## Qiita Preview 실행(미리보기 화면 표시)

본문 작성은 브라우저에서 미리보기를 통해 확인할 수 있습니다.  
브라우저에서 미리 보기를 하려면 아래 명령어를 실행합니다. 명령어 실행 시, Qiita에 게시하고 있는 글이 다운로드됩니다.

명령어를 실행하면 Qiita Preview(미리보기 화면)에 접속할 수 있습니다.  
미리보기 화면의 기본 URL은 [http://localhost:8888](http://localhost:8888/) 입니다.

### 기사 파일 배치에 대하여

1개의 글의 내용은 하나의 markdown 파일(◯◯.md)로 관리합니다.  
기사 파일은 `public` 디렉터리 내에 포함되어야 합니다.

```shell
.
└─ public
   ├── newArticle001.md
   └── newArticle002.md
```

## Qiita CLI로 기사 관리하기

### 기사 작성

Qiita Preview의 '새 글 작성' 버튼 또는 아래 명령어로 새 글을 작성할 수 있습니다.

```shell
npx qiita new 記事のファイルのベース名
```

기사 파일의 기본 이름은 자유롭게 변경할 수 있습니다.

> 기사 파일명을 `newArticle001.md`로 하려면 `newArticle001`로 한다.
> 
> 예): `$ npx qiita new newArticle001`

작성된 기사 파일의 내용은 다음과 같습니다.

```yaml
---
title: newArticle001 # 記事のタイトル
tags:
  - "" # タグ（ブロックスタイルで複数タグを追加できます）
private: false # true: 限定共有記事 / false: 公開記事
updated_at: "" # 記事を投稿した際に自動的に記事の更新日時に変わります
id: null # 記事を投稿した際に自動的に記事のUUIDに変わります
organization_url_name: null # 関連付けるOrganizationのURL名
slide: false # true: スライドモードON / false: スライドモードOFF
ignorePublish: false # true: `publish`コマンドにおいて無視されます（Qiitaに投稿されません） / false: `publish`コマンドで処理されます（Qiitaに投稿されます）
---
# new article body
```

파일 상단에는 `---` 사이에 기사 설정(Front Matter)이 포함되어 있습니다.  
여기에 글의 제목(title)과 태그(tags) 등을 yaml 형식으로 지정합니다.

### 기사 게시 및 업데이트

Qiita Preview의 '글 올리기' 버튼 또는 아래 명령어로 글을 올리거나 업데이트할 수 있습니다.

```shell
npx qiita publish 記事のファイルのベース名
```

아래 명령어로 모든 글을 반영할 수 있습니다.

`--force` 옵션을 사용하여 기사 파일의 내용을 Qiita에 강제로 반영한다.

```shell
npx qiita publish 記事ファイルのベース名 --force
# -f は --force のエイリアスとして使用できます。
npx qiita publish 記事ファイルのベース名 -f
```

### 기사 삭제

Qiita CLI, Qiita Preview에서 글을 삭제할 수 없습니다.  
`public` 디렉토리에서 markdown 파일을 삭제해도 Qiita에서는 삭제되지 않습니다.

[Qiita](https://qiita.com/)에서 글을 삭제할 수 있습니다.

## GitHub에서 기사 관리하기

### GitHub 설정 정보

아래 흐름에 따라 설정하면 GitHub의 특정 브랜치에 커밋한 시점에 글을 게시하고 업데이트할 수 있습니다.

1.  GitHub에 리포지토리를 생성합니다.
2.  [https://github.com/\[username\]/\[repository name\]/settings/secrets/actions](https://github.com/%5B%E3%83%A6%E3%83%BC%E3%82%B6%E3%83%BC%E5%90%8D%5D/%5B%E3%83%AA%E3%83%9D%E3%82%B8%E3%83%88%E3%83%AA%E5%90%8D%5D/settings/secrets/actions)에서 시크릿에 `QIITA_TOKEN` >라는 이름으로 발행한 Qiita 토큰을 저장한다.
3.  qiita init을 실행한 디렉토리 전체를 생성한 리포지토리에 푸시합니다.

기본값은 `main` 또는 `master` 브랜치에 커밋이 있을 경우 자동으로 Qiita에 글 게시 및 업데이트가 이루어집니다.  
처리 실행 조건은 `.github/workflows/publish.yml`에서 변경할 수 있다.

## Qiita CLI의 명령어, 옵션에 대하여

### 도움말

간단한 도움말을 볼 수 있습니다.

### pull

기사 파일을 Qiita와 동기화합니다.  
Qiita에서 업데이트를 진행하여 수작업으로 변경하지 않은 기사 파일만 동기화됩니다.

`--force` 옵션을 사용하여 Qiita 상의 내용을 강제적으로 기사 파일에 반영합니다.

```shell
npx qiita pull --force
# -f は --force のエイリアスとして使用できます。
npx qiita pull -f
```

### 버전

Qiita CLI의 버전을 확인할 수 있습니다.

## 사용자 설정 파일에 대하여

`npx qiita init` 명령어로 생성되는 `qiita.config.json`에 대해 설명한다.  
이 파일을 이용하여 Qiita CLI를 설정할 수 있습니다.  
설정할 수 있는 옵션은 다음과 같습니다.

-   includePrivate: qiita.com에서 다운로드하여 저장하는 글에 공유 제한 글을 포함시킬지 여부를 선택할 수 있습니다. 기본값은 `false`입니다.
-   host: `qiita preview` 명령에서 사용할 호스트를 지정할 수 있다. 기본값은 `localhost`이다.
-   port: `qiita preview` 명령에서 사용할 포트를 지정할 수 있습니다. 기본값은 `8888`이다.

## 옵션

### \--자격 증명 <credential\_dir>

Qiita CLI의 인증 정보(`credentials.json`)를 저장할 디렉토리를 지정할 수 있습니다. 기본적으로 `$XDG_CONFIG_HOME/qiita-cli` 또는 `$HOME/.config/qiita-cli`로 설정되어 있다.

```shell
npx qiita login --credential ./my_conf/
npx qiita preview --credential ./my_conf/
```

### \--config <config\_dir>

Qiita CLI의 설정 정보(`qiita.config.json`)를 배치할 디렉토리를 지정할 수 있습니다.

기본적으로 현재 디렉터리로 설정되어 있습니다.

(예)

```shell
npx qiita login --config ./my_conf/
npx qiita preview --config ./my_conf/
```

### \--root <root\_dir>

기사 파일이 다운로드될 디렉토리를 지정할 수 있습니다.  
기본적으로 현재 디렉터리로 설정되어 있습니다.

(예)

```shell
npx qiita preview --root ./my_articles/
npx qiita publish c732657828b83976db47 --root ./my_articles/
```

### \--버버

상세한 로그를 출력할 수 있습니다.

```shell
npx qiita login --verbose
npx qiita preview --verbose
```

## 자주 묻는 질문

### 제한적 공유 포스팅을 어떻게 해야 할지 모르겠어요.

[사용자 설정 파일](https://github.com/junghan0611/qiita-cli/tree/main#%E3%83%A6%E3%83%BC%E3%82%B6%E3%83%BC%E8%A8%AD%E5%AE%9A%E3%83%95%E3%82%A1%E3%82%A4%E3%83%AB%E3%81%AB%E3%81%A4%E3%81%84%E3%81%A6)에서 아래와 같이 지정합니다.  
`includePrivate: true` (기본값은 `false`입니다).  
qiita.com에서 다운로드하여 저장하는 글에 공유 제한 기사를 포함시킬지 여부를 선택할 수 있습니다.

[기사 파일](https://github.com/junghan0611/qiita-cli/tree/main#%E8%A8%98%E4%BA%8B%E3%81%AE%E4%BD%9C%E6%88%90)에서 아래와 같이 지정합니다.  
`비공개: true` (비공개: 거짓 #참: 제한된 공유 노트 / 거짓: 공개 노트)

### 오류가 발생하여 해결되지 않음

현재 오류 내용이 제대로 표시되지 않을 수 있습니다.

오류를 해결할 수 없는 경우, 이쪽의 Discussions도 참고해 보세요🙇.  
[increments/qiita-discussions#561](https://github.com/increments/qiita-discussions/discussions/561)

## 문제 및 의견은 Discussions로 보내주세요.

문제나 의견이 있으시면 [Qiita Discussions](https://github.com/increments/qiita-discussions/discussions)로 문의해 주시기 바랍니다.
