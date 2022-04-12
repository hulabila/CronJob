# Running a JAR as Kubernetes Cron Job

## Build and Deploy

### Build

Go to the terminal and go the root folder of this project and run the following command:

```bash
make
```

### Deploy
1. Put your mail credentials into the `deployment/secret-env.yaml` file.
2. Run the following commands to deploy the CronJob.
```bash
kubectl apply -f deployment/secret-env.yaml
kubectl apply -f deployment/secret-cer.yaml
kubectl apply -f deployment/cronjob.yaml
```

will run the job periodically.


## Procedure
- create java project
- create a docker image out of the java project 
- push the docker image into any image registry. I am using DockerHub here. 
- use the docker image to run the kubernetes cron job


## Future improvements
- passing arguments from the kubernetes cron job to the java application
- saving any file to persistent storage form the java application 
