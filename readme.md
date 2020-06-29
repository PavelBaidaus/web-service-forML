docker exec -it d5be66b4fc79 bash

docker exec -it flask-hello_flask_1 python train_model.py

curl --header "Content-Type: application/json" \
  --request POST \
  --data '{"flower":"1, 2, 3, 7"}' \
  http://localhost:5000/iris_post

  curl -H "Content-Type: application/json" -X POST -d '{"flower":"1, 2, 3, 7"}' http://localhost:5000/iris_post

  Invoke-WebRequest "http://localhost:5000/iris_post" -Content-Type "application/json" -body @{"flower" = "1, 2, 3, 7"}

  Invoke-WebRequest "http://localhost:5000/iris_post" -Headers @{"Content-Type" = "application/json"} -body @{"flower":"1, 2, 3, 7"}

  curl  --data-binary '{"flower" = "1, 2, 3, 7"}' -H @{ "content-type" = "application/json"} http://localhost:5000/iris_post

  curl -X POST "http://localhost:5000/iris_post" -H "accept: application/json" -H "Content-Type: application/json" -d '{"flower" = "1, 2, 3, 7"}'


  curl -X POST -H "Content-Type: application/json" -d "{ \"flower\": \"1, 2, 3, 7\" }" http://localhost:5000/iris_post

  curl -XPOST localhost:5000/iris_post -d "{"flower":"1, 2, 3, 7"}"

  curl -X POST localhost:5000/iris_post -d "{\"flower\":\"1, 2, 3, 7\"}" | python -mjson.tool