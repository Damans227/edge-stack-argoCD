# Deploying Ambassador Edge Stack using ArgoCD - GitOps Approach

1. Download the edge stack deployment templates from these links given below:

    - [https://www.getambassador.io/yaml/aes-crds.yaml](https://www.getambassador.io/yaml/aes-crds.yaml)
    - [https://www.getambassador.io/yaml/aes.yaml](https://www.getambassador.io/yaml/aes.yaml)

2) Push **aes-crds.yaml** and **aes.yaml** filesto the github repo, for example:


    ![img1](https://raw.githubusercontent.com/Damans227/edge-stack-argoCD/main/assets/img/Screen%20Shot%202021-08-10%20at%207.30.33%20PM.png)

3) Deploy argoCD in your k8s cluster using the instructions given in this document:

    - [https://argoproj.github.io/argo-cd/getting\_started/](https://argoproj.github.io/argo-cd/getting_started/)

4) Create an APP in the argoCD using UI, you can also use CLI, it&#39;s just a matter of preference. I find using the UI much easier:

    ![img2](https://raw.githubusercontent.com/Damans227/edge-stack-argoCD/main/assets/img/Screen%20Shot%202021-08-10%20at%207.32.31%20PM.png)

5) If the app has been created correctly, the ambassador pods will be deployed and app health will show healthy in argoCD:

    ![img3](https://raw.githubusercontent.com/Damans227/edge-stack-argoCD/main/assets/img/Screen%20Shot%202021-08-10%20at%207.33.33%20PM.png)

6) Once the argoCD shows the edge stack running successfully, you can deploy a sample mapping to test the edge stack. You can do this by following the instructions given on this link below  **starting from step number 2:** 

  - [https://www.getambassador.io/docs/edge-stack/latest/tutorials/getting-started/](https://www.getambassador.io/docs/edge-stack/latest/tutorials/getting-started/)
    
