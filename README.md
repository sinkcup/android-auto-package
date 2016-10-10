# Android 持续集成自动打包（gradle）

首先把项目代码放到github上，然后开始配置持续集成，步骤如下：

## Android项目使用daocloud持续集成自动打包并上传至七牛云存储

注册登录daocloud.io——》代码构建——》创建新项目——》“设置代码源”时选择你的Android项目，打开“持续集成”——》创建成功。

代码构建选择项目——》设置——》“流程定义”选择“云端流程定义”。

代码构建选择项目——》流程定义——》“持续集成”，打开项目代码里的daocloud.yml，逐行贴到网页上，把七牛的key和sercet填到网页上（不要放到代码里）。

下次提交代码时，即可自动打包上传。

## 使用travis-ci持续集成

把本项目中的`.travis.yml`拷贝到你的Android项目中。

开源项目使用免费的travis-ci.org，私有项目使用收费的travis-ci.com，用github账号登录——》Add New Repository——》选择你的Android项目——》创建成功。

选择项目——》More options——》Settings，填写七牛的key、secret和bucket。
