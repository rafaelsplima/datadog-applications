
# Datadog Power User

Repositorio com material de apoio do curso Datadog Power User


## Informações para rodar ambiente:

1 - MINIKUBE:

minikube stop   #Parar
minikube delete #Limpar

1.1 minikube start --driver=docker  #START

minikube dashboard - # Verificar status

2 - SUBINDO AGENT:
helm install datadog -f values.yaml --set datadog.apiKey=bff83accd780b0a80a4efe161fa76a01 datadog/datadog

3 - IMAGEM:
3.1 eval $(minikube docker-env)
3.2 minikube docker-env
3.3 docker build . -t dotnet-api:1.0.0 --no-cache # Fazer o build da imagem


4 - DEPLOY KUBERNETS:
kubectl apply -f dotnet-todoapi.yaml

5 - STATUS POD | STATUS LOGS:
kubectl get pods
kubectl logs

6 - EXPOR SERVIÇO:
minikube tunnel

7 - Popular API:
./populate.sh



## Documentação
##### [Traces](https://docs.datadoghq.com/tracing/setup_overview/)

##### [Requisitos de compatibilidade](https://docs.datadoghq.com/tracing/setup_overview/compatibility_requirements/)

##### [APM Kubernets](https://docs.datadoghq.com/agent/kubernetes/apm/?tab=helm)

##### [Instrumentalização .NET](https://github.com/DataDog/dd-trace-dotnet/releases)

##### [Unified Service Tagging](https://docs.datadoghq.com/getting_started/tagging/unified_service_tagging/?tab=kubernetes)

##### [Runtime Metrics](https://docs.datadoghq.com/tracing/runtime_metrics/)

##### [Service Page](https://docs.datadoghq.com/tracing/visualization/service/)

##### [Facets](https://docs.datadoghq.com/tracing/trace_explorer/query_syntax/)

##### [Trace Ingerido x Trace Indexado](https://docs.datadoghq.com/tracing/trace_explorer/?tab=listview#tracing-without-limits-recommended)

##### [Criando uma métrica a partir do trace/span](https://docs.datadoghq.com/tracing/generate_metrics/)

##### [Instrumentando aplicação Python](https://docs.datadoghq.com/tracing/setup_overview/setup/python/?tab=containers)

##### [Instrumentando aplicação Java](https://docs.datadoghq.com/tracing/setup_overview/setup/java/?tab=containers)

##### [Instrumentando aplicações host-based: IIS](https://docs.datadoghq.com/tracing/setup_overview/setup/dotnet-core/?tab=jsonfile#internet-information-services-iis)