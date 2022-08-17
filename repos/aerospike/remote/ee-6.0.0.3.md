## `aerospike:ee-6.0.0.3`

```console
$ docker pull aerospike@sha256:bd3095ca6a66a71e186554a0dcf22207ee6ba9a02709b94f2ea014c9005c3853
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `aerospike:ee-6.0.0.3` - linux; amd64

```console
$ docker pull aerospike@sha256:5821f239b5e9fc57d0ad328ad1ae5c02465fbc686f97d85bdf445950dca65271
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **104.3 MB (104263409 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7364e7040efed5fe31857d90a8e0a441b316f593a0cf5abe2a8ddf972a95c3af`
-	Entrypoint: `["\/usr\/bin\/as-tini-static","-r","SIGUSR1","-t","SIGTERM","--","\/entrypoint.sh"]`
-	Default Command: `["asd"]`

```dockerfile
# Tue, 02 Aug 2022 01:20:24 GMT
ADD file:81dbfe4f9df4d280f7580380c0c5c93ba71fedba17b3072d2b7b4bce127f88a9 in / 
# Tue, 02 Aug 2022 01:20:24 GMT
CMD ["bash"]
# Tue, 16 Aug 2022 22:19:18 GMT
ENV AEROSPIKE_VERSION=6.0.0.3
# Tue, 16 Aug 2022 22:19:18 GMT
ENV AEROSPIKE_SHA256=ad2ecced7bd1a62af43788c2a31d27c3521c48b9065cdb2234d6ead8aa8c0422
# Tue, 16 Aug 2022 22:19:18 GMT
ENV AS_TINI_SHA256=d1f6826dd70cdd88dde3d5a20d8ed248883a3bc2caba3071c8a3a9b0e0de5940
# Tue, 16 Aug 2022 22:19:40 GMT
RUN apt-get update -y   && apt-get install -y iproute2 procps wget python python3 python3-distutils lua5.2 gettext-base libldap-dev libcurl4-openssl-dev   && wget https://github.com/aerospike/tini/releases/download/1.0.1/as-tini-static -O /usr/bin/as-tini-static   && echo "$AS_TINI_SHA256 /usr/bin/as-tini-static" | sha256sum -c -   && chmod +x /usr/bin/as-tini-static   && wget "https://download.aerospike.com/artifacts/aerospike-server-enterprise/${AEROSPIKE_VERSION}/aerospike-server-enterprise-${AEROSPIKE_VERSION}-debian10.tgz" -O aerospike-server.tgz   && echo "$AEROSPIKE_SHA256 *aerospike-server.tgz" | sha256sum -c -   && mkdir aerospike   && tar xzf aerospike-server.tgz --strip-components=1 -C aerospike   && dpkg -i aerospike/aerospike-server-*.deb   && dpkg -i aerospike/aerospike-tools-*.deb   && mkdir -p /var/log/aerospike/   && mkdir -p /var/run/aerospike/   && rm -rf aerospike-server.tgz aerospike /var/lib/apt/lists/*   && rm -rf /opt/aerospike/lib/java   && dpkg -r wget ca-certificates openssl xz-utils  && dpkg --purge wget ca-certificates openssl xz-utils  && apt-get purge -y   && apt autoremove -y   && find /usr/bin/ -lname '/opt/aerospike/bin/*' -delete   && find /opt/aerospike/bin/ -user aerospike -group aerospike -exec chown root:root {} +   && mv /opt/aerospike/bin/* /usr/bin/   && rm -rf /opt/aerospike/bin
# Tue, 16 Aug 2022 22:19:41 GMT
COPY file:f56e2e33c0b4bb66affff75053eaed44661e723b8b33d3ef3c10e305b506c350 in /etc/aerospike/aerospike.template.conf 
# Tue, 16 Aug 2022 22:19:41 GMT
COPY file:697e2123680798e87da7a3f98d1d70e76ffec66f0e1aafa90ff25047a11cca52 in /entrypoint.sh 
# Tue, 16 Aug 2022 22:19:41 GMT
EXPOSE 3000 3001 3002
# Tue, 16 Aug 2022 22:19:41 GMT
ENTRYPOINT ["/usr/bin/as-tini-static" "-r" "SIGUSR1" "-t" "SIGTERM" "--" "/entrypoint.sh"]
# Tue, 16 Aug 2022 22:19:41 GMT
CMD ["asd"]
```

-	Layers:
	-	`sha256:751ef25978b2971e15496369695ba51ed5b1b9aaca7e37b18a173d754d1ca820`  
		Last Modified: Tue, 02 Aug 2022 01:25:00 GMT  
		Size: 27.1 MB (27140083 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0937189fde642eff71608b4e421c3813176ecad280e30bdc76bf18d67d47556a`  
		Last Modified: Tue, 16 Aug 2022 22:20:31 GMT  
		Size: 77.1 MB (77121443 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9933709a547cf3c030de79fb03a66769f12bccfbe0e52ded94204859830ccbeb`  
		Last Modified: Tue, 16 Aug 2022 22:20:31 GMT  
		Size: 1.0 KB (1043 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0bc82dd8fbbbe4398453bca16155d3b61d06786d831fa00764ffcd4daa078412`  
		Last Modified: Tue, 16 Aug 2022 22:20:30 GMT  
		Size: 840.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
