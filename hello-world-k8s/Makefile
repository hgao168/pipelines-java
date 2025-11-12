# Makefile

.PHONY: build run deploy clean

build:
	docker build -t hello-world-k8s .

run:
	docker run -p 3000:3000 hello-world-k8s

deploy:
	kubectl apply -f k8s/deployment.yaml
	kubectl apply -f k8s/service.yaml
	kubectl apply -f k8s/ingress.yaml

clean:
	docker rmi hello-world-k8s || true
	kubectl delete -f k8s/deployment.yaml || true
	kubectl delete -f k8s/service.yaml || true
	kubectl delete -f k8s/ingress.yaml || true