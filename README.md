# Config-NGINX-Load-Balancer
1.cd /etc/nginx/conf.d

2.touch lb1.conf

3.nano lb1.conf

4.Edit lb1.conf

    upstream myserver {

      server (ip address) ;
  
      server (ip address) ;
  
      server (ip address) ;
  
    }

    server{

      location / {
  
      proxy_pass http://myserver;
    
      }
  
    }

5.nginx -s reload

6.curl http://(ip address)

