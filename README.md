
### Building mysql docker image 
```docker build -t my_db -f Dockerfile_mysql . ```

### Building application docker image 
```docker build -t my_app -f Dockerfile . ```

### Running mysql
```docker run -d -e MYSQL_ROOT_PASSWORD=pw  mydb```





### Running the AP container
```
docker run -d --name app -p 81:81 \
-e DBHOST=172.17.0.2 \
-e DBPORT=3306 \
-e DBPWD=pw
-e APP_COLOR=blue \
-e ENVIRONMENT=prod \
-e IMAGEURL='s3://s3-bucket-for-final-project/bg.jpg' \
-e AWS_ACCESS_KEY_ID=<Key> \
-e AWS_SECRET_ACCESS_KEY=<key> \
-e AWS_SESSION_TOKEN="<>" \
-e GROUPNAME=group6 \
app
```
### Run the application, make sure it is visible in in browser


##### Update key in the repo and Push to ECR
