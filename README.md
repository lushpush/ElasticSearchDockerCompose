# Elastic Search 
    To start docker-compose follow folling steps 

    1. Create docker volumes esdata1 and esdata2 
    > docker volume create esdata1 
    > docker volume create esdata2

    2. Docker up 
    > docker-compose up

    3. Check cluster is running/health
    > curl http://127.0.0.1:9200/_cat/health

    
    4. To destroy docker 
    > docker-compose down 
    > docker-compose down -v ( Warn: destroy volume to)


