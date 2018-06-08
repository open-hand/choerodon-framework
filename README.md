# choerodon-framework

Choerodon Framework is a Microservices development framework based on Spring Cloud. You can use it as your parent's dependence in your service pom. And you can also use the dependency of Spring boot and Spring cloud.

## Modules

There are a number of modules in Choerodon Framework, here is a quick overview:

- [go-register-server](https://github.com/choerodon/go-register-server ) - The microservice registration center is implemented in the Golang, by tightly integrating the Kubernetes, the microservice registration is implemented by monitoring the state changes of the Kubernetes pod, and pull the interface in the Spring Cloud eureka client service list.
- [api-gateway](https://github.com/choerodon/api-gateway ) - Choerodon's gateway service is responsible for routing requests to real services. 
- [register-server](https://github.com/choerodon/go-register-server )  - The microservice registration is implemented by monitoring the state changes of the k8s pod, and pull the interface in the spring cloud eureka client service list.
- [config-server](https://github.com/choerodon/config-server ) - Choerodon's configuration service is the configuration center for unified management of service configuration files.
- [manager-service](https://github.com/choerodon/manager-service ) - This service is the management center of the choerodon microservices framework. Its main functions include configuration management, route management, and swagger management.
- [gateway-helper](https://github.com/choerodon/gateway-helper ) - Authenticating and limiting the requests from api-gateway, create JWT and return to api-gateway.
- [oauth-server](https://github.com/choerodon/oauth-server ) - This service is the authorized authentication center of the choerodon microservices framework and is mainly responsible for user privilege and authorization.
- [eureka-server](https://github.com/choerodon/eureka-server ) - Locally initiated registration services. Eureka registration center, for local testing only, please using go-register-server if you are online. The API send the message of server starting to "register-server" topic of kafka, after receiving the message, manager-service do the corresponding processing, such as refresh permissions.
- [iam-service](https://github.com/choerodon/iam-service ) - With management functions of user, role, permission, organization, project, password policy, fast code, client, menu, icon, multi-language , and support for importing third-party users through LDAP.
- [event-store-service](https://github.com/choerodon/event-store-service ) - Choerodon Event-store-service for data consistency support. It is necessary to cooperate with choerodon-starter-event-producer and choerodon-starter-event-consumer to implement data consistency. Currently, the message queue kafka is supported.
- [file-service](https://github.com/choerodon/file-service ) - Choerodon file-service is built on minio server, we can use minio client to upload and delete files.
- [hystrix-turbine](https://github.com/choerodon/hystrix-turbine ) - The Hystrix turbine integrates each service's data of Hystrix Dashboard. The use of Hystrix Turbine is very simple and requires only the introduction of appropriate dependencies, annotations and configurations.
- [hystrix-dashboard](https://github.com/choerodon/hystrix-dashboard ) - The Hystrix Dashboard is a dashboard component of Hystrix. It is mainly used to monitor Hystrix's index information in real time. Information fed back through the interface can quickly discover problems in the system.

## Dependencies

* Spring Boot: 1.5.3.RELEASE
* Spring Cloud: Dalston.SR4

## Links

* [Change Log](./CHANGELOG.zh-CN.md)

## Reporting Issues
If you find any shortcomings or bugs, please describe them in the  [issue](https://github.com/choerodon/choerodon/issues/new?template=issue_template.md).

## How to Contribute
Pull requests are welcome! [Follow](https://github.com/choerodon/choerodon/blob/master/CONTRIBUTING.md) to know for more information on how to contribute.

## Note

If you get a wrong prompt after use choerodon framework, like ` Failed to execute goal org.maven.plugins ... `

You can use the command to skip this mistake. ` mvn package -Dgpg.skip -Dmaven.source.skip=true -Dmaven.javadoc.skip=true `

We'll fix it and release it as soon as possible.
