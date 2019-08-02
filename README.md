# Serverless

Serverless, the serverless architecture, frees everyone from the server and only needs to focus on the business logic itself. Users only need to pay attention to data and business logic, no need to maintain the server, and do not need to care about the capacity and capacity of the system. Serverless is essentially a simpler and easier to use PaaS with two meanings:

An application or service that relies solely on cloud services to manage business logic and state, commonly referred to as BaaS (Backend as a Service)
Event-driven and short-time execution of an application or service whose main logic is done by the developer but managed by a third party (such as AWS Lambda), commonly referred to as FaaS (Function as a Service). At present, Serverless of the fire generally refers to FaaS.

Introducing serverless can bring significant benefits to application developers

- Users do not need to configure and manage the server
- User services do not need to be based on a specific framework or software library
- Easy to deploy, just upload the code to the serverless platform
- Fully automated horizontal scaling
- Event triggering, such as http request triggering, file update triggering, time triggering, message triggering, etc.
- Low cost, such as AWS Lambda charging by execution time and number of triggers, no need to pay when the code is not running

Of course, serverless is not a silver bullet, but it also has its own limitations.

- No state, any in-process or host state of the service cannot be used by subsequent calls, and need to manage state via external database or network storage
- There is usually a limit on the time of each function call, such as AWS Lambda limits each function to a maximum of 5 minutes
- Startup delays, especially in the case of inactive or bursty traffic
- Platform dependencies such as service discovery, monitoring, debugging, API Gateway, etc. all rely on the functionality provided by the serverless platform

## Open source framework

- OpenFaas: https://github.com/openfaas/faas
- Fission: https://github.com/fission/fission
- Kubeless: https://github.com/kubeless/kubeless
- OpenWhisk: https://github.com/apache/incubator-openwhisk
- Fn: https://fnproject.io/

## Commercial products

- AWS Lambda: http://docs.aws.amazon.com/lambda/latest/dg/welcome.html
- AWS Fargate: https://aws.amazon.com/cn/fargate/
- Azure Container Instance (ACI): https://azure.microsoft.com/en-us/services/container-instances/
- Azure Functions: https://azure.microsoft.com/en-us/services/functions/
- Google Cloud Functions: https://cloud.google.com/functions/
- Hyper: https://hyper.sh/
- Huawei CCI: https://www.huaweicloud.com/product/cci.html
- Aliyun Serverless Kubernetes: https://help.aliyun.com/document_detail/71480.html

Many commercial products can also be seamlessly integrated with Kubernetes, using commercial serverless products (such as ACI and Fargate, etc.) as Kubernetes clusters via [Virtual Kubelet] (https://github.com/virtual-kubelet/virtual-kubelet) An infinite Node is used, so there is no need to consider the number of Nodes.

![](images/virtual-kubelet.png)

## Reference Document

- [Awesome Serverless](https://github.com/anaibol/awesome-serverless)
- [AWS Lambda] (http://docs.aws.amazon.com/lambda/latest/dg/welcome.html)
- [Serverless Architectures] (https://martinfowler.com/articles/serverless.html)
- [TNS Guide to Serverless Technologies] (http://thenewstack.io/tns-guide-serverless-technologies-best-frameworks-platforms-tools/)
- [Serverless blogs and posts] (https://github.com/JustServerless/awesome-serverless)
