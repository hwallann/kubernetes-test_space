cd gomhdsu

docker run --name=pmmysql -e MYSQL_DATABASE=$DSU_MYSQL_DATABASE -e MYSQL_ROOT_PASSWORD=$DSU_MYSQL_PASSWORD -e MYSQL_ROOT_HOST="%" -d mysql/mysql-server:5.7

sudo docker build -f './build/docker/Dockerfile' . -t hwallann/dsud:0.1.0

sudo docker build -f './build/docker/Dockerfile' . -t hwallann/dsud:0.1.0 --build-arg cred_path=config/pmsys.pem --build-arg tmp=$(cp /home/ablab/vsts/work/_temp/pmsys.pem config/) --no-cache

https://docs.bitnami.com/kubernetes/how-to/deploy-go-application-kubernetes-helm/


sudo docker build -f './build/docker/Dockerfile' . -t hwallann/dsud:0.1.0 --build-arg MYSQL_DATABASE=$DSU_MYSQL_DATABASE --build-arg MYSQL_ROOT_PASSWORD=$DSU_MYSQL_PASSWORD --build-arg MYSQL_ROOT_HOST="%"

docker push hwallann/dsud:0.1.0

$ kubectl run dsud-k --image=hwallann/dsud:0.1.0 --port=8080 --generator=run-pod/v1 --image-pull-policy=Always

$ kubectl run dsud-k --image=hwallann/dsud:0.1.0 --generator=run-pod/v1 --port=8080

$ kubectl expose pod dsud-k --type=NodePort --name=example-service-dsud
$ kubectl describe services example-service-dsud
$ minikube service list
$ kubectl delete services example-service-dsud
$ kubectl delete deployment dsud-k
$ kubectl delete pod dsud-k
