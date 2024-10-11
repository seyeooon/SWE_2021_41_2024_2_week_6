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
This code is a function that checks whether a given number is a 'Happy Number'.

>#### `summ(n)` function
>- **Role**: A function that returns the sum of the squares of the digits of number `n`.
>- **Description**: 
>   - `n % 10` retrieves the last digit and squares it before adding it to the sum.
>   - `n = int(n / 10)`removes the last digit and repeats the process.


>#### `isHappy(n)` function
>- **Role**: A function that checks if the number `n` is a 'Happy Number'.
>- **Description**: 
>   - It repeatedly calls `summ(n)` to get the sum of the squares of the digits.
>   - If the sum is 1, it returns `True`; if it's 4, it returns `False`.


>#### Example
>```python
>isHappy(2)  # Returns False


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
> * **Description**: This command reads the `/etc/os-release` file inside the `ossp-container` to print the operating system information. From the output, it can be seen that the container is running Ubuntu 24.04.1 LTS.

>```bash
>docker exec ossp-container git --version
>```
> * **Output**:
>   ```bash
>   git version 2.43.0
>   ```
> * **Description**: his command checks the version of Git installed inside the `ossp-container`. The output shows that Git version 2.43.0 is installed.

>```bash
>docker exec ossp-container python3 --version
>```
> * **Output**:
>   ```bash
>   Python 3.12.3
>   ```
> * **Description**: This command checks the version of Python 3 installed inside the `ossp-container`. The output shows that Python version 3.12.3 is installed.

>```bash
>docker inspect --format="{{.HostConfig.Binds}}" ossp-container
>```
> * **Output**:
>   ```bash
>   [/Users/seyeonpark/desktop:/mnt/ossp_container_dir]
>   ```
> * **Description**: This command checks the bind mount configuration between the `ossp-container` and the host system. The output shows that the host directory `/Users/seyeonpark/desktop` is mounted to `/mnt/ossp_container_dir` inside the container.
