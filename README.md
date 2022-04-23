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
<h4>pod</h4>: element that will own the containers that are running in the application
configmap: componete responsible for mapping environment variavies between different kubernetes services
nodes: Collection of resources to support u or more pods
sVC or services: are used to expose pod ports to achieve internal communication etre the services or external as well
