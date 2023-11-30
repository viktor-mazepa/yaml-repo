# YAML Examples

|NAME|PROMPT|DESCRIPTION|EXAMPLE|
|------------|------------|---------|---------|
|Create pod| k ai "create pod for europe-central2-docker.pkg.dev/devops2023-405122/dev-repo/devops-demo2:v2.0.0 with port 8080, port name http and labels app:demo run:demo"|Generates YAML to create POD with port 8080 and specific labels| [app.yml](/yaml/app.yaml)|
|Add liveness probe|add livenes probe  with get request to / and port 8080 | Generates YAML to create pod with liveness probe for pod demo via GET reuest to port 8080| [app-livenessProbe.yml](/yaml/app-livenessProbe.yaml)|
|Add readiness probe|add readiness proby to /ready and port 8080|Generates YAML to create pod with readiness probe for pod demo via GET reuest to port 8080 and path /ready|[app-readinessProbe.yml](/yaml/app-readinessProbe.yaml)|
|Add volume mount|add volume mount /data to local folder /home/data|Generates YAML to create pod with volume mount from local folder /home/data to folder /data in POD|[app-readinessProbe.yml](/yaml/app-volumeMounts.yaml)|
|Create CronJob| k ai "create cronjob that write 'Hello Cron Job' into terminal each 15 seconds"| Generates YAML to create CronJob that writes 'Hello Cron Job' into terminal each 15 seconds| [app-cronjob.yml](/yaml/app-cronjob.yaml)|
|Create Job| kubectl-ai "create job to make postgres database copy each month to local folder /home/db-archive"| Generates YAML to create Job that perform database backup|[app-job.yml](/yaml/app-job.yaml)|
|Create multicontainer POD|kubectl-ai "create pod with two contaniners: nginx with mount folder in pod /html to host folder /home/html/ and port http 8080; postgresql with mount folder /db-data to host folder /home/db-data"|Generates YAML to create POD with two containers|[app-multicontainer.yml](/yaml/app-multicontainer.yaml)|
|Create POD with resources|k ai "create pod for europe-central2-docker.pkg.dev/devops2023-405122/dev-repo/devops-demo2:v2.0.0 with port 8080, port name http and labels app:demo run:demo and required resources"| Generates YAML to create POD with resources| [app-resources.yaml](/yaml/app-resources.yaml)|
|Create secret env POD| k ai "create pod wikth redis image to secret with secretKeyRef with name mysecret and value password"|enerates YAML to create POD that uses a Redis image and uses secrets to configure environment variables| [app-secret-env.yaml](/yaml/app-secret-env.yaml)|