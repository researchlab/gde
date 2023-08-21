## 设计规范

主要是包裹第三方, 能剥离出相应的逻辑的, 就以${第三方主要名称}_${业务名称}.go 命名文件, 如
- rabbitmq_conn.go
- rabbitmq_publisher.go
- rabbitmq_consumer.go
- rabbitmq_conn_test.go
- rabbitmq_publisher_test.go
- rabbitmq_consumer_test.go
- example_rabbitmq_publiser_test.go
- example_rabbitmq_consumer_test.go

如果不能剥离业务的, 可以直接用${第三方主要名称}.go, 如
- rabbitmq.go
- rabbitmq_test.go
- example_rabbitmq_test.go

如果是共用的业务, 则统一用 ${第三方主要名称}_utils.go 命名文件, 如
- rabbitmq_utils.go

如果多个包裹都需要用到, 则直接命名为utils.go 
