### 250617
## python repository 배포 방법 (pip)
### 먼저 repository 최상단에 다음과 같이 있어야 한다.
```
[package_name]/
LICENSE
pyproject.toml
README.md
requirements.txt
setup.cfg
```
### <br/>

### requirments.txt를 만든다.
```
pip freeze > requirements.txt
```
### <br/>

### pyproject.toml 수정
#### 여기서 dependencies는 requirments.txt의 내용을 그대로 복사해서 쓰면 된다.
- \[package_name\] = "\[package_name\].\[script_name\]:main"은 수정해야 한다.
```
[build-system]
requires = ["setuptools>=61.0"]
build-backend = "setuptools.build_meta"

[project]
name = "dofp"
version = "0.1.0"
description = "test"
authors = [
  { name="Theragenbio", email="test@test.com" }
]
readme = "README.md"
license = {file = "LICENSE"}
requires-python = ">=3.7"
dependencies = [
  "certifi==2025.4.26",
  "charset-normalizer==3.4.2",
  "idna==3.10",
  "numpy==2.0.2",
  "pandas==2.2.3",
  "pysam==0.21.0",
  "python-dateutil==2.9.0.post0",
  "pytz==2025.2",
  "PyYAML==6.0.2",
  "requests==2.32.4",
  "six==1.17.0",
  "tqdm==4.66.1",
  "tzdata==2025.2",
  "urllib3==2.4.0"
]

[project.scripts]
[package_name] = "[package_name].[script_name]:main"
```
### <br/>

### setup.cfg
```
[metadata]
name = test
version = 0.1.0
author = test
author_email = contact@test.com
description = test package
long_description = file: README.md
long_description_content_type = text/markdown
license = Proprietary
license_files = LICENSE
url = https://github.com/username/repo.git
classifiers =
    Programming Language :: Python :: 3
    License :: Other/Proprietary License
    Operating System :: POSIX :: Linux

[options]
packages = find:
python_requires = >=3.7
```
### <br/>

### LICENSE 파일은 chatgpt한테 EULA, MIT 등 원하는 걸로 대충 포맷 만들어달라고 하면 만들어준다.
```
End-User License Agreement (EULA)

This End-User License Agreement ("Agreement") is a legal agreement between you and me.
```
### <br/>

### 그리고 \[package_name\]/ 폴더에는 다음과 같이 되어 있어야 한다.
#### pyproject.toml 에서 main.main 함수를 인식하려면 \[package_name\].main:main"이 되어야 한다.
```
__init__.py
main.py
나머지 ...
```
### <br/>

### local 설치
#### 최상단 경로에서 실행
```
pip install build
python -m build
```
#### <br/>

### 그러면 dist 폴더가 하나 생긴다.
#### * dofp는 내가 진행하는 프로젝트 이름이다. 이름은 설정에 따라 바뀐다.
```
dist/
├── dofp-0.1.0-py3-none-any.whl
├── dofp-0.1.0.tar.gz
```
#### <br/>

### 패키지 설치
```
pip install dist/dofp-0.1.0-py3-none-any.whl

# 또는 강제 재설치
pip install --force-reinstall dist/dofp-0.1.0-py3-none-any.whl
```
### <br/>

### 이렇게 하면 pyproject.toml 에 \[package_name\]/으로 적은 이름으로 명령어를 치면 실행 가능하다.
### 물론 import도 됨
