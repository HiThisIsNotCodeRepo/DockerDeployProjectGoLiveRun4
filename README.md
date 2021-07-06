# DockerDeployProjectGoLiveRun4

## Prerequisite

```shell
# 1. Install Docker
# 2. Install Git
# 3. Clone Repo
git clone https://github.com/qinchenfeng/DockerDeployProjectGoLiveRun4.git
```

## Deploy App

```shell
# 1 Run MySQL container
docker run --name paotui_mysql -dp 3306:3306 magicpowerworld/paotui_back_end:20210706
# 1-1 Prepare database
go run .
# 2 Run Backend container
docker run --name paotui_back_end --net=host magicpowerworld/paotui_back_end:20210706
# 3 Run Frontend container
docker run --name paotui_front_end -p 80:80 -d magicpowerworld/paotui_front_end:20210706
```

## URL
www.paotui.sg