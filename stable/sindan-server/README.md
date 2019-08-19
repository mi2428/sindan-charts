```yaml
apiVersion: v1
kind: PersistentVolume
metadata:
  name: mysql-pv
spec:
  storageClassName: mysql
  capacity:
    storage: 4Gi
  persistentVolumeReclaimPolicy: Recycle
  accessModes:
    - ReadWriteOnce
  hostPath:
    path: "/mnt/kubernetes/pv/sindan-mysql"
```

```yaml
apiVersion: v1
kind: PersistentVolume
metadata:
  name: mysql-backup-pv
spec:
  storageClassName: mysql-backup
  capacity:
    storage: 4Gi
  persistentVolumeReclaimPolicy: Recycle
  accessModes:
    - ReadWriteOnce
  hostPath:
    path: "/mnt/kubernetes/pv/sindan-mysql-backup"
```
