# 플러그인

플러그인은 여러분이 XE를 확장할 수 있는 유일한 방법입니다. XE에 새로운 기능을 추가하거나 기본 기능을 변경하려고 할 때, 또는 테마나 스킨과 같은 컴포넌트를 XE에 추가하고 싶을 때, 플러그인을 사용하십시오.

XE는 오픈소스프로그램으로 자유롭게 코어 소스코드를 수정하여 사용할수 있지만, 업데이트 되는 소스코드를 계속 적용하려면 소스코드의 수정을 피해야 합니다. 대신 플러그인을 사용하면 XE 소스코드의 수정을 피할 수 있습니다. 또한 플러그인을 다른 XE 사용자들과 공유할 수도 있습니다.

각 플러그인은 고유한 이름을 가지는 하나의 디렉토리로 구성되며, `/plugins` 디렉토리에 등록됩니다.

## 번들 플러그인

XE는 사용자들이 자주 사용할 만한 플러그인을 XE에 포함하여 배포하고 있습니다.

* Together (기본 번들 테마 플러그인)
* banner (기본 번들 테마 의존성 플러그인, 배너 플러그인)
* board (게시판 기능 플러그인)
* ckeditor (에디터 기능 플러그인)
* claim (신고 기능 플러그인)
* comment (댓글 기능 플러그인)
* news\_client ( XE3 의 새로운 소식을 알려주는 위젯 플러그인)
* page (심플 페이지 번들 플러그인)
* widget\_page (위젯 페이지를 구성하는데에 필요한 플러그인, 위젯 플러그인)

## 플러그인 상태

각 플러그인은 활성화 또는 비활성화 상태를 가집니다. 어떤 플러그인을 `/plugins` 디렉토리에 추가한다고 해도 처음에는 비활성화 상태이기 때문에 바로 작동되지 않습니다. 플러그인을 활성화\(activate\)시켜야 비로소 플러그인이 작동합니다. 플러그인을 활성화시키려면 사이트 관리자 &gt; 플러그인 &gt; 플러그인 목록에서 원하는 플러그인을 활성화시키십시오.

## 개발 모드 플러그인

XE 자료실을 통해 설치하지 않은 플러그인을 `개발 모드 플러그인`이라고 합니다.

사이트관리자는 XE 자료실을 통해 다른 개발자들이 배포한 플러그인을 다운로드 받을 수 있습니다. 물론, 다른 개발자의 플러그인 소스코드를 `/plugins`에 직접 추가하여 사용할 수도 있으며, 여러분이 직접 생성한 플러그인을 추가하여 사용할 수도 있습니다.

XE 자료실을 통해 설치하지 않은 플러그인은 터미널에서 반드시 플러그인 디렉토리로 이동후 `composer update` 명령을 실행해주어야 합니다. 이 명령을 실행하면, 플러그인 디렉토리에 `vendor` 디렉토리가 생성됩니다. 따라서 개발모드 플러그인은 `vendor` 디렉토리를 가집니다.

> 직접 설치한 플러그인에서 `composer update`를 실행하지 않으면 autoload가 등록되지 않아 제대로 작동하지 않을 수 있습니다. 또 XE에서는 자료실을 통해 설치한 플러그인으로 인식하여 오작동을 일으킬 수 있습니다.
