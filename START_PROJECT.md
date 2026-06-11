1. Start Docker Desktop

2. minikube start

3. kubectl get pods

4. Recreate backend secret if needed

kubectl create secret generic backend-secret \
--from-literal=JWT_SECRET=my-secret

5. kubectl get svc

6. Access application