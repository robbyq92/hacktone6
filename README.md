#006:Argo CD

De cara a mejorar el cluster de Kubernetes de la compañía, en el que ya se han ido desplegando aplicaciones y configurando la monitorización, el CTO decide que el siguiente paso será apostar por el framework GitOps. De esta manera, los cambios que se realice en el cluster estarán almacenados en un repositorio git y su despliegue se hará de forma automatizada, evitando asi el trabajo manual.

Para poder implementar este framework se apuesta por el uso de la herramienta Argo CD.
Objetivos:
```
•	Instalar Argo CD.
•	Almacenar la aplicación de prueba https://github.com/cloudogu/hello-k8s en un repo git personal.
•	Utilizando Argo CD desplegar la aplicación desde este git.
•	Configurar el despliegue automático de la aplicación ante cualquier cambio realizado en el repositorio Git.
•	Una vez configurado, realizar un cambio a la aplicación, ver que se despliega correctamente y realizar un roll-back a la versión previa al cambio desde Argo CD.
```
Bonus Track:
```
•	Probar a realizar desde Argo CD despliegues complejos del tipo: Canary deployment o Blue-Green deployment.
Tips:
•	GitOps framework
•	Argo CD Installation
```


## Pasos:

Instalar el argocd 
https://argo-cd.readthedocs.io/en/stable/

```
kubectl create namespace argocd
kubectl apply -n argocd -f https://raw.githubusercontent.com/argoproj/argo-cd/stable/manifests/install.yaml
```

![image](https://github.com/robbyq92/hacktone6/assets/49034238/65799741-9ebf-428c-9061-0146486a1653)


Clonamos repositorio
```
https://github.com/robbyq92/hello-k8s-hack6.git
```

Creamos un nuevo proyecto en argocd y lo añadimos ahí vía https:
![image](https://github.com/robbyq92/hacktone6/assets/49034238/a7a25ec7-9cf5-4d19-88e4-8a7f596afe37)

añadimos el repositorio:
![image](https://github.com/robbyq92/hacktone6/assets/49034238/6caf9af2-0734-4e9c-af5f-e1943121461c)
![image](https://github.com/robbyq92/hacktone6/assets/49034238/2df3e794-06eb-4c19-975d-c7409aee981c)

Añadimos una nueva app
![image](https://github.com/robbyq92/hacktone6/assets/49034238/41f1a522-b3c5-40a0-8566-cda8eca5036d)
![image](https://github.com/robbyq92/hacktone6/assets/49034238/c2250ee0-b828-49cf-b329-4e13525f8ade)





