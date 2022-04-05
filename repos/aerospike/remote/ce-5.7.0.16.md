## `aerospike:ce-5.7.0.16`

```console
$ docker pull aerospike@sha256:0c7e6cc1a62c8e761dc4c5bf061a7ad10bc1bb71a2ac38aaf50f4b3e607e268b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `aerospike:ce-5.7.0.16` - linux; amd64

```console
$ docker pull aerospike@sha256:23cb1a319a7b86c77946b894a6dc58774be1a107e5f7bf97fb4ca3d7714adc93
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **81.6 MB (81556806 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b84072fbce0254bea69b505b9e65335a0a99b0f7506513f6b48d41eae2b2bd08`
-	Entrypoint: `["\/usr\/bin\/dumb-init","--","\/entrypoint.sh"]`
-	Default Command: `["asd"]`

```dockerfile
# Tue, 29 Mar 2022 00:22:38 GMT
ADD file:59187422476c57db46e60f894a4cfd0f243e80230ef9ea75b2d8dd4925d59df3 in / 
# Tue, 29 Mar 2022 00:22:38 GMT
CMD ["bash"]
# Tue, 05 Apr 2022 17:46:19 GMT
ENV AEROSPIKE_VERSION=5.7.0.16
# Tue, 05 Apr 2022 17:46:43 GMT
ENV AEROSPIKE_SHA256=31d54cd60c48a365f761ba35f7e2914f36d6c1b09e6143bec3c7ce68fb1a4409
# Tue, 05 Apr 2022 17:47:01 GMT
RUN apt-get update -y   && apt-get install -y iproute2 procps dumb-init wget python python3 python3-distutils lua5.2 gettext-base libcurl4-openssl-dev    && wget "https://www.aerospike.com/artifacts/aerospike-server-community/${AEROSPIKE_VERSION}/aerospike-server-community-${AEROSPIKE_VERSION}-debian10.tgz" -O aerospike-server.tgz   && echo "$AEROSPIKE_SHA256 *aerospike-server.tgz" | sha256sum -c -   && mkdir aerospike   && tar xzf aerospike-server.tgz --strip-components=1 -C aerospike   && dpkg -i aerospike/aerospike-server-*.deb   && dpkg -i aerospike/aerospike-tools-*.deb   && mkdir -p /var/log/aerospike/   && mkdir -p /var/run/aerospike/   && rm -rf aerospike-server.tgz aerospike /var/lib/apt/lists/*   && rm -rf /opt/aerospike/lib/java   && dpkg -r wget ca-certificates openssl xz-utils  && dpkg --purge wget ca-certificates openssl xz-utils  && apt-get purge -y   && apt autoremove -y   && find /usr/bin/ -lname '/opt/aerospike/bin/*' -delete   && find /opt/aerospike/bin/ -user aerospike -group aerospike -exec chown root:root {} +   && mv /opt/aerospike/bin/* /usr/bin/   && rm -rf /opt/aerospike/bin
# Tue, 05 Apr 2022 17:47:02 GMT
COPY file:1897c4aae07efbc61bf2d8c2c7b0dfb0990174e11cc787eac71d5adf767abaed in /etc/aerospike/aerospike.template.conf 
# Tue, 05 Apr 2022 17:47:02 GMT
COPY file:e1d47057fdb4c34c118f7ba5898161c386b475cba70907a4ae483866cf07335b in /entrypoint.sh 
# Tue, 05 Apr 2022 17:47:02 GMT
EXPOSE 3000 3001 3002
# Tue, 05 Apr 2022 17:47:02 GMT
ENTRYPOINT ["/usr/bin/dumb-init" "--" "/entrypoint.sh"]
# Tue, 05 Apr 2022 17:47:02 GMT
CMD ["asd"]
```

-	Layers:
	-	`sha256:f003217c5aaebdfee0b9a448fbabd995e5f0159f5b231460c0ecc21baf171953`  
		Last Modified: Tue, 29 Mar 2022 00:28:02 GMT  
		Size: 27.2 MB (27151970 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a77411ab9e61591ac2e04bcc2dabbf59eab5ccfeb1b7372ec7352bfaa164f09`  
		Last Modified: Tue, 05 Apr 2022 17:47:38 GMT  
		Size: 54.4 MB (54402815 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:91054120f003f51a5b7189eed7313efaca72b2d31113741af156c2e42f727d01`  
		Last Modified: Tue, 05 Apr 2022 17:47:30 GMT  
		Size: 1.1 KB (1139 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7b0e7ee50d90d235ea2783ea5b0e557b050b0042754aac06757f5cbf4221a0ed`  
		Last Modified: Tue, 05 Apr 2022 17:47:30 GMT  
		Size: 882.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
