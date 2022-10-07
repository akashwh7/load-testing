# load-testing

Load testing using K6

K6 documentation: https://k6.io/docs/

Run the script: k6 run -u 1000 -d 1m script.js --insecure-skip-tls-verify 

LoadImpact: docker run --rm loadimpact/loadgentest-wrk -c 600 -t 600 -d 1m http://URLorIP

where, c = Connections, t = Threads, d = Duration (in s=seconds, m=mins, h=hours), u = number of virtual users

Load testing using shell script:
# Make 100 requests to a http/s target URL/IP:
# for i in $(seq 1 100); do curl -s -o /dev/null "<http://URL/IP>"; done
# To get HPA details: kubectl get hpa
