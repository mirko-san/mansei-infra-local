https://github.com/mirko-san/mansei のローカル開発環境のインフラまわり

## Commands

### 各種 apply
```
kubectl apply -f src/deployment.yaml
```

```
kubectl apply -f src/service.yaml
```

```
kubectl apply -f src/ingress.yaml
```

### 確認

ingress リソース（？）の確認
`ADDRESS` 列のIPを後に使う
```
kubectl get ingresses
```

curl で確認
```
curl http://<ADDRESS>/index.html
curl http://<ADDRESS>/path1/index.html -H 'Host: foo.bar.com'
curl http://<ADDRESS>/path2/index.html -H 'Host: foo.bar.com'
```
