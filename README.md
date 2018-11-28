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

 5. Generate Data 
    movie dataset reside in sample/blog.json


    > you can create your own data set using following link, you may need to format documents and delete extra parenthesis, can be done easily using notepad++ or sed , use this code if you don't find the fork
    ` [
  {
    'repeat(100, 50)': {
      _id: '{{objectId()}}',
      title: 'Blog -Title {{lorem(3, "words")}}',
      author: {
        first: '{{firstName()}}',
        last: '{{surname()}}'
      },    
      
      comments: [
        {
          'repeat(0,5)': {            
            text: '{{lorem(10)}}',
            name: '{{firstName()}} {{surname()}}'
          }
        }
      ]	
    }
  }
]'

