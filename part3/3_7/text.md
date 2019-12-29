# Kubernetes

Kubernetes is a tool for organizing multiple containers. It offers a wide range of tools that aid in scaling, deploying and operating clusters of containers. Most cloud services offer kubernetes support and thus, kubernetes has become the standard tool for managing large, container based applications.

Kubernetes installation is not the easiest of tasks and requires planning. Installing kubernetes is a manual process and configurations differ from project to project. Working with kubernetes requires knowledge of its own interface as kubernetes is incompatible with Docker CLI. The learning curve can be quite steep.

Another popular tool for organizing multi-container applications is called Docker Swarm. Docker Swarm is built into Docker and is said to offer a “just works” experience with little effort. Docker Swarm integrates with Docker CLI and makes deploying multi-host container environments a bit easier than Kubernetes. 

Kubernetes is designed to work best with large clusters and Docker Swarm offers a simpler experience but lacks some features to manage very complex applications and clusters. Kubernetes should be used when an application has grown to the point where it has hundreds of containers. For smaller projects, the extra work and effort required to configure kubernetes might not be very beneficial if the same end result can be achieved with a simpler tool, such as Docker Swarm.
