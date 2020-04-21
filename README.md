
Dependencies:

* python
* curl

```
$ ./gs
Checking for python...
Checking for curl...

    Bash script for getting started with Enroute Standalone API Gateway.

    Uses curl to make REST calls to program locally running Enroute Standalone API Gateway

    Run Enroute first -

        sudo docker run --net=host saarasio/enroute-gw:v0.3.0

    Then use this script to program it.

    Usage: ./gs [option]

     options:

         create-http        - create service, route, upstream
         send-http-traffic  - use this option to send http traffic

         create-https       - create service, secret, route, upstream
         send-https-traffic - use this option to send https traffic

         create-grpc        - create service, route, upstream for grpc
         send-grpc-traffic  - sends grpc traffic (grpc_client_server -role client -host 127.0.0.1 -port 8080 -id 3)

         start-server       - Runs server using python (python -m SimpleHTTPServer 50051)
         start-server-grpc  - Runs server using grpc_client_server (grpc_client_server -role server -host 127.0.0.1 -port 50053)

         show
         delete

      Example:

        ./gs create-https
        ./gs delete
        ./gs show
        
        
