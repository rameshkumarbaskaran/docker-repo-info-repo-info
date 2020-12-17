## `jobber:latest`

```console
$ docker pull jobber@sha256:b11ff35e0e2ba30c7c140a4d1d917286f5a4a0dca14a9e78650001acfa03bd48
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `jobber:latest` - linux; amd64

```console
$ docker pull jobber@sha256:ccc43476869b96a7f9ce403e40a9bab10cb81a569db046f572a4e77d2328e6aa
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.8 MB (11762002 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aadc2d0e4e7206a067b628daa623c3ff442be7a40b01159bdbdf2a41a01c527a`
-	Default Command: `["\/usr\/libexec\/jobberrunner","-u","\/var\/jobber\/1000\/cmd.sock","\/home\/jobberuser\/.jobber"]`

```dockerfile
# Thu, 17 Dec 2020 00:19:49 GMT
ADD file:8ed80010e443da19d72546bcee9a35e0a8d244c72052b1994610bf5939d479c2 in / 
# Thu, 17 Dec 2020 00:19:49 GMT
CMD ["/bin/sh"]
# Thu, 17 Dec 2020 13:51:43 GMT
ENV USERID=1000
# Thu, 17 Dec 2020 13:51:45 GMT
RUN addgroup jobberuser &&     adduser -S -u "${USERID}" -G jobberuser jobberuser &&     mkdir -p "/var/jobber/${USERID}" &&     chown -R jobberuser:jobberuser "/var/jobber/${USERID}"
# Thu, 17 Dec 2020 13:51:45 GMT
ENV JOBBER_VERSION=1.4.4
# Thu, 17 Dec 2020 13:51:45 GMT
ENV JOBBER_SHA256=ec09b2efafff69c91fba2124bf28607209e1c9b50ed834ff444a9d40798aa8d3
# Thu, 17 Dec 2020 13:51:47 GMT
RUN wget -O /tmp/jobber.apk "https://github.com/dshearer/jobber/releases/download/v${JOBBER_VERSION}/jobber-${JOBBER_VERSION}-r0.apk" &&     echo -n "Actual checksum: " && sha256sum /tmp/jobber.apk &&     echo "${JOBBER_SHA256} */tmp/jobber.apk" | sha256sum -c &&     apk add --no-network --no-scripts --allow-untrusted /tmp/jobber.apk &&     rm /tmp/jobber.apk
# Thu, 17 Dec 2020 13:51:47 GMT
COPY --chown=jobberuser:jobberuserfile:c7cc6d32091e7beeac78efd9fe855e36a106902c1177df0f9f6bd2bbe3b8d518 in /home/jobberuser/.jobber 
# Thu, 17 Dec 2020 13:51:48 GMT
RUN chmod 0600 /home/jobberuser/.jobber
# Thu, 17 Dec 2020 13:51:48 GMT
USER jobberuser
# Thu, 17 Dec 2020 13:51:49 GMT
CMD ["/usr/libexec/jobberrunner" "-u" "/var/jobber/1000/cmd.sock" "/home/jobberuser/.jobber"]
```

-	Layers:
	-	`sha256:0a6724ff3fcd51338afdfdc2b1d4ffd04569818e31efad957213d67c29b45101`  
		Last Modified: Thu, 17 Dec 2020 00:20:26 GMT  
		Size: 2.8 MB (2814864 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ea66016a8f87f326b8c184fed4bd82fcadbad2e193d61eae7e5e453578e39b37`  
		Last Modified: Thu, 17 Dec 2020 13:52:00 GMT  
		Size: 1.3 KB (1281 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:63c38b7f79fe3611e6fcb4f5d701082a7ee8a3afbed2a4a4ec90e853a98938b4`  
		Last Modified: Thu, 17 Dec 2020 13:52:04 GMT  
		Size: 8.9 MB (8945388 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:87f3915d04665b6d2814099beaf160e811f4d5555db42d40ab963018f711821a`  
		Last Modified: Thu, 17 Dec 2020 13:52:00 GMT  
		Size: 235.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7b2169cb5b5d09c70d9c5928632015a1c35251256761bc077cc126ae3d1ce15a`  
		Last Modified: Thu, 17 Dec 2020 13:52:02 GMT  
		Size: 234.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
