## the setup of ingress supporting TLS certificate

### ingressclass
controlplane $ k -n ingress-nginx get svc ingress-nginx-controller
NAME                       TYPE       CLUSTER-IP      EXTERNAL-IP   PORT(S)                      AGE
ingress-nginx-controller   NodePort   10.111.232.20   <none>        80:30080/TCP,443:30443/TCP   18m

controlplane $ k -n ingress-nginx get ingressclass
NAME    CONTROLLER             PARAMETERS   AGE
nginx   k8s.io/ingress-nginx   <none>       18m


### TLS certs via openssl

openssl req -x509 -nodes -days 365 -newkey rsa:2048 -keyout cert.key -out cert.crt -subj "/CN=world.universe.mine/O=world.universe.mine"

controlplane $ ls -al cert*
-rw-r--r-- 1 root root 1220 Dec 28 16:43 cert.crt
-rw------- 1 root root 1708 Dec 28 16:43 cert.key



### Secret to reference TLS certs
k -n world create secret tls ingress --cert=/root/cert.crt --key=/root/cert.key

### Ingress to reference TLS certs via Secret

  spec:
    ingressClassName: nginx
    rules:
    - host: world.universe.mine
      http:
        paths:
        - backend:
            service:
              name: europe
              port:
                number: 80
          path: /europe
          pathType: Prefix
        - backend:
            service:
              name: asia
              port:
                number: 80
          path: /asia
          pathType: Prefix
    tls:
    - hosts:
      - world.universe.mine
      secretName: ingress
      
