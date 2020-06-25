apiVersion: extensions/v1beta1
kind: Deployment
metadata:
  name: elk
spec:
  replicas: 1
  template:
    metadata:
      labels:
        app: elk
    spec:
      containers:
        - name: elk
          image: sebp/elk
          ports:
            - containerPort: 5601

---
apiVersion: v1
kind: Service
metadata:
  name: 'elk-service '
  labels:
    name: 'elk-service '
spec:
  ports:
    - port: 5601
      targetPort: 5601
      protocol: TCP
      name: '5601'
  selector:
    app: elk
  type: LoadBalancer 
 
