1. Bug
Run Docker with Linux Container
  - Error in running docker command in terminal -> go Power shell -> run cmd:  "C:\Program Files\Docker\Docker\DockerCli.exe" -SwitchDaemon
  - Using right click in Docker app -> Run docker with Linux container -> will see error
    set "experimental": true in Setting
    https://docs.microsoft.com/en-us/windows/wsl/install-win10#step-4---download-the-linux-kernel-update-package
Can't find `/app/dist /usr/share/nginx/html`
  because new react doesn't have `dist` -> using `build`

2. Some command
  docker container ls
  docker rm -f
  docker images 

3. Learn
Run first docker
  npm run docker:build (from docker build)
  npm run docker:run (from docker run)

Pushing to docker hub with using tag
  docker build -t react-docker-example .
  docker images -> get id of docker image
  docker tag [id] hieptqsocial/reactdockerexample:v1
  docker push hieptqsocial/reactdockerexample:v1
  -> now it is dockerhub
b                                                                                                                                                                                                                                                                                                                                                         
docker run -d --publish 8888:5000 reactdockerexample

aws ecr get-login-password --region ap-southeast-2 | docker login --username AWS --password-stdin 189705706301.dkr.ecr.ap-southeast-2.amazonaws.com
docker build -t react-docker-example .
docker tag react-docker-example:latest 189705706301.dkr.ecr.ap-southeast-2.amazonaws.com/react-docker-example:latest
docker push 189705706301.dkr.ecr.ap-southeast-2.amazonaws.com/react-docker-example:latest

SUCCESS deploy react docker app to ECS | https://www.linkedin.com/pulse/deploy-your-react-app-ecsfargate-sourav-sutradhar/?trk=read_related_article-card_title
-> error in 
VPC when config load balancer


pipeline
arn:aws:iam::189705706301:role/service-role/codebuild-react-docker-example-service-role
AWSCodePipelineServiceRole-ap-southeast-2-react-docker-deploy-p