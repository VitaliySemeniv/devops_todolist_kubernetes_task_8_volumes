# Validation Guide

Цей гайд показує, **як перевірити**, що застосунок розгорнуто, томи та файли змонтовані коректно, і як отримати доступ до додатку.
> **Примітка:** розгортання виконується скриптом `./bootstrap.sh`. У цьому файлі немає команд деплою — лише перевірки.

---

## 1) Перевірити стан Namespace/ресурсів
```bash
kubectl get ns mateapp
kubectl -n mateapp get cm,secret
kubectl get pv
kubectl -n mateapp get pvc
kubectl -n mateapp get deploy,pods
