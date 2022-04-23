# Kurbnets-news-site
# repository created to practice use of the basic elements of a kubernetes

<h3>the system used to show the examples was developed by alura courses and the examples and concepts cited are based on the content presented in the course of the alura, knowledge of the author and research in documentation. I hope they help anyone who's reading. : )</h3>


***************

<h3>Requirements:</h3>


<ul>
  <li>Linux operating system. For this example is being used the Ubuntu 20.4 LTS</a></li>
  <li>Vitualbox</li>
  <li>Must have <a href="https://docs.docker.com/engine/install/centos/">Docker</a> installed</li> 
</ul>

*****************
<h3> Basic Concepts</h3>

it is interesting to know some basic concepts to understand how the project examples work, such as:
<h4>pod:</h4> element that will own the containers that are running in the application
<h4>configmap:</h4> componete responsible for mapping environment variavies between different kubernetes services
<h4> nodes:</h4> Collection of resources to support u or more pods
<h4> SVC or services:</h4> are used to expose pod ports to achieve internal communication etre the services or external as well


************
<h3>config project<h3>
  
  <h5>instale o minikube:<h5>
  
        curl -LO https://storage.googleapis.com/minikube/releases/latest/minikube-linux-amd64
  
        sudo install minikube-linux-amd64 /usr/local/bin/minikube
  <h5>start minikube:<h5>
        
        minikube start –vm-driver=virtualbox
    
 if you use the kubectl get node will already see the kubernets cluster up and running:
        
        kubectl get nodes
    
 
 ![image](https://user-images.githubusercontent.com/38367700/164945484-f2219688-d5c4-46d6-99cd-ce08a3f3e5e2.png)

Now apply the manifests:
    
          
    
      kubectl apply -f site_noticias/porta-noticias.yaml
      kubectl apply -f site_noticias/site-noticias.yaml
      kubectl apply -f site_noticias/db/db-noticias.yaml
      kubectl apply -f site_noticias/configMap/db-configmap.yaml
      kubectl apply -f site_noticias/configMap/portal-configmap.yaml
      kubectl apply -f site_noticias/configMap/sistema-configmap.yaml
    
