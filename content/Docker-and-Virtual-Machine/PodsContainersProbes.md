# My LFD259 Notes

# readinessProbe
Oftentimes, our application may have to initialize or be configured prior to being ready to accept traffic. As we scale up our application, we may have containers in various states of creation. Rather than communicate with a client prior to being fully ready, we can use a readinessProbe. The container will not accept traffic until the probe returns a healthy state.

With the exec statement, the container is not considered ready until a command returns a zero exit code. As long as the return is non-zero, the container is considered not ready and the probe will keep trying.

Another type of probe uses an HTTP GET request (httpGet). Using a defined header to a particular port and path, the container is not considered healthy until the web server returns a code 200-399. Any other code indicates failure, and the probe will try again.

The TCP Socket probe (tcpSocket) will attempt to open a socket on a predetermined port, and keep trying based on periodSeconds. Once the port can be opened, the container is considered healthy.

# livenessProbe
Just as we want to wait for a container to be ready for traffic, we also want to make sure it stays in a healthy state. Some applications may not have built-in checking, so we can use livenessProbes to continually check the health of a container. If the container is found to fail a probe, it is terminated. If under a controller, a replacement would be spawned.

# startupProbe
Becoming beta recently, we can also use the startupProbe. This probe is useful for testing an application which takes a long time to start.

If kubelet uses a startupProbe, it will disable liveness and readiness checks until the application passes the test. The duration until the container is considered failed is failureThreshold times periodSeconds. For example, if your periodSeconds was set to five seconds, and your failureThreshold was set to ten, kubelet would check the application every five seconds until it succeeds, or is considered failed after a total of 50 seconds. If you set the periodSeconds to 60 seconds, kubelet would keep testing for 300 seconds, or five minutes, before considering the container failed.