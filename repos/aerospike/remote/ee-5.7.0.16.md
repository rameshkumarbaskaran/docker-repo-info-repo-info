## `aerospike:ee-5.7.0.16`

```console
$ docker pull aerospike@sha256:3fa61de4a6abc8076348f0ce88c2cfdde9065f4dc1dc953d18deee49e85537a0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `aerospike:ee-5.7.0.16` - linux; amd64

```console
$ docker pull aerospike@sha256:fe6851b50e2226f530acfad4edfa176c6e9228d937beaf13922af2b2bd6318aa
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **83.9 MB (83924935 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ab2174d17f9c1fa40c802d3f7f8690dcbc340815834ca0381bb35b05ddf83905`
-	Entrypoint: `["\/usr\/bin\/as-tini-static","-r","SIGUSR1","-t","SIGTERM","--","\/entrypoint.sh"]`
-	Default Command: `["asd"]`

```dockerfile
# Tue, 29 Mar 2022 00:22:38 GMT
ADD file:59187422476c57db46e60f894a4cfd0f243e80230ef9ea75b2d8dd4925d59df3 in / 
# Tue, 29 Mar 2022 00:22:38 GMT
CMD ["bash"]
# Tue, 05 Apr 2022 17:46:19 GMT
ENV AEROSPIKE_VERSION=5.7.0.16
# Tue, 05 Apr 2022 17:46:20 GMT
ENV AEROSPIKE_SHA256=0cf6b82692f3d8414fdade36645f8d2380ce9371bd3a6b6201471fd506864d88
# Tue, 05 Apr 2022 17:46:20 GMT
ENV AS_TINI_SHA256=d1f6826dd70cdd88dde3d5a20d8ed248883a3bc2caba3071c8a3a9b0e0de5940
# Tue, 05 Apr 2022 17:46:40 GMT
RUN apt-get update -y   && apt-get install -y iproute2 procps wget python python3 python3-distutils lua5.2 gettext-base libldap-dev libcurl4-openssl-dev   && wget https://github.com/aerospike/tini/releases/download/1.0.1/as-tini-static -O /usr/bin/as-tini-static   && echo "$AS_TINI_SHA256 /usr/bin/as-tini-static" | sha256sum -c -   && chmod +x /usr/bin/as-tini-static   && wget "https://download.aerospike.com/artifacts/aerospike-server-enterprise/${AEROSPIKE_VERSION}/aerospike-server-enterprise-${AEROSPIKE_VERSION}-debian10.tgz" -O aerospike-server.tgz   && echo "$AEROSPIKE_SHA256 *aerospike-server.tgz" | sha256sum -c -   && mkdir aerospike   && tar xzf aerospike-server.tgz --strip-components=1 -C aerospike   && dpkg -i aerospike/aerospike-server-*.deb   && dpkg -i aerospike/aerospike-tools-*.deb   && mkdir -p /var/log/aerospike/   && mkdir -p /var/run/aerospike/   && rm -rf aerospike-server.tgz aerospike /var/lib/apt/lists/*   && rm -rf /opt/aerospike/lib/java   && dpkg -r wget ca-certificates openssl xz-utils  && dpkg --purge wget ca-certificates openssl xz-utils  && apt-get purge -y   && apt autoremove -y   && find /usr/bin/ -lname '/opt/aerospike/bin/*' -delete   && find /opt/aerospike/bin/ -user aerospike -group aerospike -exec chown root:root {} +   && mv /opt/aerospike/bin/* /usr/bin/   && rm -rf /opt/aerospike/bin
# Tue, 05 Apr 2022 17:46:40 GMT
COPY file:7d75174e09b209cf7f56b715636c2b8e08dd083d548e8cdc8517cabd512600b5 in /etc/aerospike/aerospike.template.conf 
# Tue, 05 Apr 2022 17:46:41 GMT
COPY file:31b6a51a1d9d91f22433472f07f6ddfe3cea3bb07f460dd69c4187bc7fd20fdf in /entrypoint.sh 
# Tue, 05 Apr 2022 17:46:41 GMT
EXPOSE 3000 3001 3002
# Tue, 05 Apr 2022 17:46:41 GMT
ENTRYPOINT ["/usr/bin/as-tini-static" "-r" "SIGUSR1" "-t" "SIGTERM" "--" "/entrypoint.sh"]
# Tue, 05 Apr 2022 17:46:41 GMT
CMD ["asd"]
```

-	Layers:
	-	`sha256:f003217c5aaebdfee0b9a448fbabd995e5f0159f5b231460c0ecc21baf171953`  
		Last Modified: Tue, 29 Mar 2022 00:28:02 GMT  
		Size: 27.2 MB (27151970 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a443d40e8854d4e5fe77314a6aff905b2fb91da835ecacc211384f8332c9f8cd`  
		Last Modified: Tue, 05 Apr 2022 17:47:21 GMT  
		Size: 56.8 MB (56770887 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ab490dc80e69436fd84d682e368307b77a84094e3da01ba69cd6a85f3fd163c2`  
		Last Modified: Tue, 05 Apr 2022 17:47:13 GMT  
		Size: 1.2 KB (1170 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:90327c4f16512650c0cc555290e21018ab40e2c7e2b3285b853a1318a718c7c1`  
		Last Modified: Tue, 05 Apr 2022 17:47:13 GMT  
		Size: 908.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
