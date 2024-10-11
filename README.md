# SWE_2021_41_2024_2_week_6
---
## Week 4 Assignment
 * https://github.com/seyeooon/SWE_2021_41_2024_2_week_4

```python
def summ(n) :
    x = 0
    while n // 1 != 0 :
        x += (n % 10) ** 2
        n = int(n / 10)
    return (x)


def isHappy(n) :
  while 1 :
      n = summ(n)
      if n == 1 :
          return True
          break
      elif n == 4 :
          return False
          break

isHappy(2)
```
### - Description of the code
이 코드는 주어진 숫자가 '행복한 수(Happy Number)'인지 확인하는 함수이다.

>#### `summ(n)` 함수
>- **Role**: 숫자 `n`의 각 자릿수를 제곱한 후 그 합을 반환하는 함수이다.
>- **Description**: 
>   - `n % 10`으로 마지막 자릿수를 가져오고, 이를 제곱하여 합산한다.
>   - `n = int(n / 10)`으로 마지막 자릿수를 제거한 후 반복한다.


>#### `isHappy(n)` 함수
>- **Role**: 숫자 `n`이 '행복한 수'인지 확인하는 함수이다.
>- **Description**: 
>   - `summ(n)`을 반복 호출하여 자릿수 제곱합을 구한다.
>   - 제곱합이 1이면 `True`, 4이면 `False`를 반환한다.


>#### Example
>```python
>isHappy(2)  # False 반환


---
## Week 5 Assignment
>```bash
>docker exec ossp-container cat /etc/os-release
>```
> * **Output**:
>   ```bash
>   PRETTY_NAME="Ubuntu 24.04.1 LTS"
>   NAME="Ubuntu"
>   VERSION_ID="24.04"
>   VERSION="24.04.1 LTS (Noble Numbat)"
>   UBUNTU_CODENAME=noble
>   ```
> * **Description**: `ossp-container` 컨테이너 안에서 `/etc/os-release` 파일을 읽어, 컨테이너가 실행 중인 운영체제의 정보를 출력하는 명령어이다. 위 출력에서 컨테이너는 Ubuntu 24.04.1 LTS를 실행 중임을 확인할 수 있다.

>```bash
>docker exec ossp-container git --version
>```
> * **Output**:
>   ```bash
>   git version 2.43.0
>   ```
> * **Description**: `ossp-container` 컨테이너 안에 설치된 Git의 버전을 확인하는 명령어이다. 출력 결과로 Git 2.43.0 버전이 설치되어 있음을 알 수 있다.

>```bash
>docker exec ossp-container python3 --version
>```
> * **Output**:
>   ```bash
>   Python 3.12.3
>   ```
> * **Description**: `ossp-container` 컨테이너 안에 설치된 Python 3의 버전을 확인하는 명령어이다. 출력 결과로 Python 3.12.3 버전이 설치되어 있음을 알 수 있다.

>```bash
>docker inspect --format="{{.HostConfig.Binds}}" ossp-container
>```
> * **Output**:
>   ```bash
>   [/Users/seyeonpark/desktop:/mnt/ossp_container_dir]
>   ```
> * **Description**: 이 명령어는 `ossp-container` 컨테이너와 호스트 시스템 간의 바인드 마운트 설정을 확인한다. 출력 결과는 호스트의 `/Users/seyeonpark/desktop` 디렉토리가 컨테이너의 `/mnt/ossp_container_dir` 디렉토리와 연결되어 있음을 의미한다.
