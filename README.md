# Rowy Hooks

Cloud run instance for managing webhooks on Rowy

## Deployment

### Bash script
```
./deploy.sh --project [YOUR_PROJECT_ID]
```

### Cloudbuild

It assumes existing `service account` responsible for `rowy-hooks`

    rowy-hooks@${PROJECT_ID}.iam.gserviceaccount.com

with several permissions:
    
    - datastore.user // access to firestore
    - storage.objectAdmin // access to storage
    - secretmanager.secretAccessor // access to secrets for actionScripts
    - logging.logWriter // access to cloud logs
