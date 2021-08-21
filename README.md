#This is to demonstrate deployment using kubernetes:

- A simple node app "simple express" is deployed as internal service
- A reverse proxy which forwards requests to simple express is deployed as external service

# How to deploy:
- kubectl apply -f deployment/simple-express-deploy.yml
- kubectl apply -f deployment/simple-express-svc.yml
- kubectl apply -f deployment/reverse-proxy-deploy.yml
- kubectl apply -f deployment/reverse-proxy-svc.yml

# How to test

- curl http://<external-ip-simple-reverse-proxy-service>/api/
> "Hello!"  should be output

