# Project name

## Environment

+ Docker for dev
  - Ubuntu 16.04
  - Python2.7

```
docker build --rm -t python-dev .\conf\docker\python2.7
```
> 此路徑用於 Window 作業系統

+ Docker for app
  - Base on python-dev
  - Copy app and initial package

```
docker build --rm -t python-app .
```
> 此路徑用於 Window 作業系統

## Library

+ [numpy](http://www.numpy.org/)
+ [pytest](https://docs.pytest.org/en/latest/)
+ [pycodestyle](https://pypi.org/project/pycodestyle/)

## Script

#### 1、Install dependencies

```
pip install -r .pythonrc
```

#### 2、Setep command

```
python setup.py
```

#### 3、setup in docker

```
docker run -ti -v %cd%:/repo python-dev /bin/bash -l -c "python /repo/setup.py"
```

#### 4、RUN python-app

```
docker run -ti python-dev
```
> 確保 python-dev 已經存在，倘若要重新封裝則需執行 build 命令

```
docker run -ti -v %cd%:/repo python-dev
```
> 若需替換執行應用程式內容

## Reference
