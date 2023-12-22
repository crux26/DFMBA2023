# 현재 설치된 라이브러리 목록을 파일로 만들기
pip list --format=freeze > requirements.txt

# 라이브러리 목록을 이용하여 설치하기
pip install -r requirements.txt
# (== conda create env -f /my/YAML/file.yml)


# venv 생성하고 activate 하기
# 서로 다른 파이썬 및 라이브러리 버전을 사용할 경우, 가상 환경을 통해 작업 환경 분리 가능
# 실질적으로는 특정 폴더 내에 파이썬 및 라이브러리를 다시 설치하는 것

# virtual environment 생성
> python -m venv /path/to/new/virtual/environment

# 혹은 현재 path 아래에 생성
> python -m venv .

# path 아래에 생성된 Scripts 폴더 내의 activate.bat 파일 실행
> %CD%/Scripts/activate.bat (CMD)
> .\activate.bat (PS)

# 나올 때는 deactivate
> deactivate

# 가상환경 삭제는 해당 폴더를 직접 삭제하면 됨

#######################################
# 혹은 conda venv를 통해서도 생성할 수 있음
> conda create -n ENV_NAME python=VERSION

# venv 목록을 다음으로 확인 가능
> conda env list

# 가상환경 (비)활성화
> conda (de)activate ENV_NAME

# 가상환경 삭제
> conda remove -n ENV_NAME --all