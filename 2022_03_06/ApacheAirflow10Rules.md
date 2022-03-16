# Title: ApacheAirflow10Rules
## Source: https://towardsdatascience.com/apache-airflow-in-2022-10-rules-to-make-it-work-b5ed130a51ad 
## Summary: 

The 10 rules:
1. Airflow is an orchestration framework, not an execution framework (you should use only operators that trigger computation out of Airflow)
1. Avoid the PythonOperator for your jobs (only run very very simple code, use an operator like a KubernetesPodOperator , EmrCreateJobFlowOperator etc.)
1. Check the existing operators before creating one
1. Do not install any custom dependency in your Airflow deployment (only allowed dependencies are apache-airflow-providers-XXX)
1. Airflow is NOT a data lineage solution
1. Airflow is NOT a data storage solution
1. Do not put secrets in Airflow variables or connections
1. Do not deploy together the different elements of Airflow (if you go for manual deployment then you must isolate the airflow_scheduler, the airflow_webserver and airflow_workers so you can scale them depending your use-cases)
1. LocalExecutor and KubernetesExecutor are not easy

## Tags: #airflow #tips #10tips #apacheairflow #tips&tricks 

