# operator helloworld

## 本项目目的

- 快速启动一个新的operator, 供新入手operator的同事快速上手operator
- 仅包含最基本的代码功能, 以便于使用者将注意力集中于operator本身


## 使用方法

- helloworld为完整的工程项目, 在x86平台上已完成编译
- 将helloworld目录完整的拷贝到个人目录, 按以下操作快速上手operator


### 操作指南

1. 以下操作都需进去helloworld根目录后执行
2. 启动operator: 
   1. 执行make run
   2. 在linux终端将直接运行operator, 日志为标准控制台输出
3. 启动测试用的k8s的实例guestbook
   1. 执行  kubectl apply -f config/samples/
4. operator业务逻辑修改
   1. 文件 controllers/guestbook_controller.go
   2. 函数 Reconcile 中, 添加业务逻辑
   3. 测试用的 Reconcile 仅包含一条日志输出