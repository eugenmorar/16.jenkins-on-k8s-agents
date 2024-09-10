1.Create Jenkins Namespace
 kubectl config set-context --namespace jenkins

2.Create Persistent Volume
 /var/jenkins_home

3.Create a StatefullSet

4.Initial Admin Password
 kubectl port-forward pod/jenkins-0 8080:8080

5.Create a StorageClass to Retain

6.Disable Executors

7.Install Plugins
 Kubernetes
 BlueOcean

8.Create Cluster Role for Jenkins Admin
 cluster_admin role for an actual service account

9.Add Pod Template
 jenkins url: http://jenkins:8080 (jenkins svc)
 jenkins tunnel: http://jenkins:50000 (jenkins agent)

10.Create Service for svc and agent
 kubectl logs -l jenkins_slaves_label