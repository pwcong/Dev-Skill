# GitLab CI

GitLab CI 官方文档在这里[GitLab CI](https://docs.gitlab.com/ee/ci/)

### 0x00 准备

推荐区分开`GitLab服务器`与`Runners服务器`

* GitLab服务器部署GitLab服务
* Runners服务器安装GitLabRunner服务，安装帮助在这里[GitLabRunner](https://docs.gitlab.com/runner/install/)

### 0x01 获取Token

GitLab使用root账户登录，进入页面`admin/runners`获取`registration token`

### 0x02 注册Runner

在Runners服务器中使用0x01步骤获取到的token注册runner，命令如下：

```shell
gitlab-ci-multi-runner register
```

### 0x03 编写CI Job

新建仓库，并在仓库根目录下新建文件`.gitlab-ci.yml`，示例如下：

```yml
stages:
  - test
  - build
  - deploy

test:
  stage: test
  script:
    - yarn test

build:
  stage: build
  script:
    - yarn build

deploy:
  stage: deploy
  script:
    - yarn deploy
```

### 0x04 查看结果

到对应仓库CI页面查看