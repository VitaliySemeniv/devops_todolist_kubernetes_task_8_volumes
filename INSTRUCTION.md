kubectl create namespace mateapp || true
kubectl -n mateapp apply -f .infrastructure/confgiMap.yml
kubectl -n mateapp apply -f .infrastructure/secret.yml
kubectl apply -f .infrastructure/pv.yml
kubectl -n mateapp apply -f .infrastructure/pvc.yml
kubectl -n mateapp apply -f .infrastructure/deployment.yml
kubectl -n mateapp rollout status deploy/todoapp
