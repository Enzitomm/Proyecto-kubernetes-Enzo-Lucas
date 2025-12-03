# Proyecto Kubernetes - Enzo Golbano & Lucas Sosa

Este proyecto consiste en el despliegue de una aplicación web estática utilizando una imagen Docker personalizada basada en **NGINX**, ejecutada dentro de un cluster **Kubernetes** local montado con **Minikube**.

El objetivo es practicar el flujo completo:

1. Crear una imagen Docker personalizada.
2. Correrla en un cluster Kubernetes local.
3. Exponer el servicio mediante un `Service` de tipo `NodePort`.

---

## 👥 Autores

- **Enzo Golbano**
- **Lucas Sosa**

Materia: **Redes II**  
Carrera: **Analista en Sistemas**  
Institución: **Universidad Champagnat**  
Profesor: **José Scattareggia**

---

## 🧰 Tecnologías utilizadas

| Herramienta      | Función                                      |
|------------------|----------------------------------------------|
| Docker Desktop   | Creación y manejo de imágenes de contenedores|
| Kubernetes       | Orquestación del contenedor                  |
| Minikube         | Cluster Kubernetes local                     |
| kubectl          | Administración del cluster                   |
| PowerShell / WSL2| Consola y compatibilidad en Windows          |
| NGINX            | Servidor web para la página estática         |

---

## 📂 Estructura del proyecto

```text
Proyecto-kubernetes-Enzo-Lucas/
├─ app/
│  └─ index.html          # Página estática que muestra el mensaje del proyecto
├─ k8s/
│  ├─ deployment.yaml     # Deployment de Kubernetes
│  └─ service.yaml        # Service de tipo NodePort
├─ Dockerfile             # Definición de la imagen Docker basada en NGINX
└─ README.md              # Documentación del proyecto

🎯 ¿QUÉ HACÉS ENTONCES?
Cada vez que quieras abrir el proyecto:

1️⃣ Iniciar minikube (si no está iniciado):

minikube start --driver=docker

2️⃣ Abrir el servicio:

minikube service miweb-service

3️⃣ Dejar esa terminal abierta (si la cerrás, se cierra el túnel).





🔥Cada vez que cambies el index.html:
Comandos:
        minikube docker-env   (activar daemon)
        docker build -t miweb:1.0 .
        minikube kubectl -- rollout restart deployment miweb
        minikube service miweb-service