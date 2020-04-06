__R에서 패키지 설치할 때 생기는 문제와 해결 방법 ("failed to create lock directory")__

------

R을 사용하다 보면 간혹 패키지 설치 시 다음과 같은 메시지가 뜨면서 패키지 설치가 진행되지 않는 것을 보게 됩니다.

`failed to create lock directory`

이 때 R 사용자 라이브러리 (패키지가 설치되는 폴더)에 가보면 `00LOCK`이라는 폴더가 생성되어 있는 것을 볼 수 있습니다.

문제 해결을 위해 다음 2가지 방법을 이용할 수 있습니다.

## 1. 패키지 설치 시 옵션을 설정하는 방법

`install.packages("NameOfThePackageToInstall", dependencies = TRUE, INSTALL_opts = '--no-lock')`

즉 패키지 설치 시 `INSTALL_opts = '--no-lock'` 옵션을 더해주는 것입니다.
([출처: stackoverflow, R install.packages returns “failed to create lock directory”](https://stackoverflow.com/questions/14382209/r-install-packages-returns-failed-to-create-lock-directory)

## 2. `00LOCK` 폴더 지우기

간단한 방법으로는 R 사용자 라이브러리 폴더에 가서 `00LOCK`이라고 되어 있는 폴더를 지우는 것입니다.
폴더를 지우고 나면 패키지가 잘 설치되는 것을 볼 수 있습니다. 

다만 `00LOCK` 폴더가 반복적으로 생성될 경우에는 앞의 1번과 같은 방법을 이용하는 것을 추천드립니다.

