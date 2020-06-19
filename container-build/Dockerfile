# Use the httpd-parent image as base
FROM quay.io/redhattraining/httpd-parent
LABEL io.openshift.expose-services="8080:http" \
	io.openshift.tags="apache.http" \
	io.k8s.description="A basic Apache HTTP Server image." \
	io.k8s.display-name="Apache HTTP Server" 
Run sed -i 's/^Listen 80/&80/' /etc/httpd/conf/httpd.conf && \
	chgrp -R 0 /var/log/httpd /var/run/httpd && \
	chmod -R 770 /var/log/httpd /var/run/httpd
user 1001
