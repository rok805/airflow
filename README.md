# airflow
study airflow with exams


## airflow 설치하기 on MAC

* 1. pip, python 설치하기

```
    $brew install pip
    $brew install python
```    

* 2. airflow 설치

```
    $sudo -H pip install apache-airflow
```

* 3. DB 초기화

```
    $airflow db init
```


* 4. airflow 계정 생성

```
    $ airflow users create \
        --username admin \
        --firstname cheongrok \
        --lastname lee \
        --role Admin \ 
        --email rok805@zuminternet.com

```

* 5. web server UI 실행

```
    $ airflow webserver --port 8080
```
    이후 localhost:8080으로 web 접근. username이 아이디고 비밀번호는 4번 절차시 계성 생성할 때 입력한 것으로 로그인한다.
    
    example task가 많이 보이는데 이를 안보려면 airflow.cfg에서 load_examples = False로 수정한다.

    
* 6. airflow 스케쥴러 실행

```
    $ airflow scheduler
```

* 7. ~/airflow 에 dags 폴더 생성
    
```
    $ mkdir ~/airflow/dags
```

* 8. DAG 생성

```
    $touch tutorial.py
    tutorial.py의 내용은 참조사이트 1)의 tutorial.py와 동일
```

* 9. DAG 확인

```
    $airflow dags list
```

* 9. task 테스트

    command layout: command subcommand dag_id task_id date
    testing print_date
```
    $airflow test tutorial print_date 2015-06-01
```



참조사이트)
1) https://airflow.apache.org/docs/apache-airflow/1.10.14/tutorial.html
2) https://zzsza.github.io/data/2018/01/04/airflow-1/

