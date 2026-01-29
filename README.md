<<<<<<< HEAD
# quiz-app-helm
=======
# quiz-app-chart

Helm chart per il deploy di quiz-app (frontend, backend, database MongoDB) su Kubernetes.

## Struttura
- **Namespace**: parametrico
- **Backend**: Node.js, parametrico (immagine, env, porta)
- **Frontend**: React, parametrico (immagine, env, porta)
- **Database**: MongoDB, PVC, StorageClass parametrico
- **Ingress**: ALB parametrico
- **Secret**: mongo-uri parametrico

## Installazione

```sh
helm install quiz-app ./quiz-app-chart -n <namespace> --create-namespace
```

## Parametri principali (`values.yaml`)
- `namespace`: Namespace di deploy
- `backend.*`: Immagine, env, porta backend
- `frontend.*`: Immagine, env, porta frontend
- `database.*`: Immagine, storage, porta database
- `ingress.*`: Host, className, annotazioni ALB
- `secret.mongoUri`: Stringa connessione MongoDB

## Note
- Adatto a CD/ArgoCD
- Personalizza i parametri in `values.yaml` secondo ambiente
>>>>>>> 648aa3f (Initial commit: add Helm chart)
