# Airflow - OpenMetadata Integration

1. Get Source Code
    github airflow, openmetadata source code download
    OpenMetadata 1.3.4-release
    Airflow 2.7.3

2. setup python venv  

    ```shell
    python3.10 -m venv venv
    source venv/bin/activate
    ```

3. airflow  
    move to source root of airflow. and...  

    1) install require pkg  

        ```shell
        pip install . 
        ```

    2) set env `AIRFLOW_HOME`  

        ```shell
        export AIRFLOW_HOME=${PWD}/ROOT
        ```

4. open-metadata  
    move to source root of open-metadata pkg install and generate code from json  

    1) install require pkg  

        ```shell
        pip install datamodel_code_generator antlr4
        # and antlr4 command run
        antlr4
        # will be download ANTLR4 
        ```

    2) generate code by make  

        ```shell
        make generate
        ```

airflow users create -u admin -p admin -r Admin -f yeem -l junbum -e jblim0125@gmail.com