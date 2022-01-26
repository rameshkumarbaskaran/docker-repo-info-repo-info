## `aerospike:ee-5.7.0.10`

```console
$ docker pull aerospike@sha256:9c962abbcbbb74f76310c8444c21226a74bbea3cb3005a1aa05c6c1a8d3e87ac
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `aerospike:ee-5.7.0.10` - linux; amd64

```console
$ docker pull aerospike@sha256:e0310b9e10bb0664a632a04533198e07c2375bd24c0ff469cb394aa2512eeb39
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **83.9 MB (83904138 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ee80ee1197db98423e03c56f7012039a3d5057c7001e2c258ce9ea27ba4b7e6f`
-	Entrypoint: `["\/usr\/bin\/as-tini-static","-r","SIGUSR1","-t","SIGTERM","--","\/entrypoint.sh"]`
-	Default Command: `["asd"]`

```dockerfile
# Wed, 26 Jan 2022 01:40:59 GMT
ADD file:c51141702f568a28a7e3e7a2748f5ead5754e32d7b1cf7ebc8f4326273d05206 in / 
# Wed, 26 Jan 2022 01:40:59 GMT
CMD ["bash"]
# Wed, 26 Jan 2022 02:08:18 GMT
ENV AEROSPIKE_VERSION=5.7.0.10
# Wed, 26 Jan 2022 02:08:19 GMT
ENV AEROSPIKE_SHA256=736bc5779412088d72a76d95192bfa34e3332fc33357cb5c413a71fbb7ee634c
# Wed, 26 Jan 2022 02:08:19 GMT
ENV AS_TINI_SHA256=d1f6826dd70cdd88dde3d5a20d8ed248883a3bc2caba3071c8a3a9b0e0de5940
# Wed, 26 Jan 2022 02:08:41 GMT
RUN apt-get update -y   && apt-get install -y iproute2 procps wget python python3 python3-distutils lua5.2 gettext-base libldap-dev libcurl4-openssl-dev   && wget https://github.com/aerospike/tini/releases/download/1.0.1/as-tini-static -O /usr/bin/as-tini-static   && echo "$AS_TINI_SHA256 /usr/bin/as-tini-static" | sha256sum -c -   && chmod +x /usr/bin/as-tini-static   && wget "https://www.aerospike.com/enterprise/download/server/${AEROSPIKE_VERSION}/artifact/debian10" -O aerospike-server.tgz   && echo "$AEROSPIKE_SHA256 *aerospike-server.tgz" | sha256sum -c -   && mkdir aerospike   && tar xzf aerospike-server.tgz --strip-components=1 -C aerospike   && dpkg -i aerospike/aerospike-server-*.deb   && dpkg -i aerospike/aerospike-tools-*.deb   && mkdir -p /var/log/aerospike/   && mkdir -p /var/run/aerospike/   && rm -rf aerospike-server.tgz aerospike /var/lib/apt/lists/*   && rm -rf /opt/aerospike/lib/java   && dpkg -r wget ca-certificates openssl xz-utils  && dpkg --purge wget ca-certificates openssl xz-utils  && apt-get purge -y   && apt autoremove -y   && find /usr/bin/ -lname '/opt/aerospike/bin/*' -delete   && find /opt/aerospike/bin/ -user aerospike -group aerospike -exec chown root:root {} +   && mv /opt/aerospike/bin/* /usr/bin/   && rm -rf /opt/aerospike/bin
# Wed, 26 Jan 2022 02:08:41 GMT
COPY file:7d75174e09b209cf7f56b715636c2b8e08dd083d548e8cdc8517cabd512600b5 in /etc/aerospike/aerospike.template.conf 
# Wed, 26 Jan 2022 02:08:42 GMT
COPY file:31b6a51a1d9d91f22433472f07f6ddfe3cea3bb07f460dd69c4187bc7fd20fdf in /entrypoint.sh 
# Wed, 26 Jan 2022 02:08:42 GMT
EXPOSE 3000 3001 3002
# Wed, 26 Jan 2022 02:08:42 GMT
ENTRYPOINT ["/usr/bin/as-tini-static" "-r" "SIGUSR1" "-t" "SIGTERM" "--" "/entrypoint.sh"]
# Wed, 26 Jan 2022 02:08:42 GMT
CMD ["asd"]
```

-	Layers:
	-	`sha256:6552179c3509e3c4314b4065e0d2790563d01cd474e2fdd58be4d46acd48af6a`  
		Last Modified: Wed, 26 Jan 2022 01:47:31 GMT  
		Size: 27.2 MB (27153731 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c01d0d8de92d7f44e81599a75c10c2250944d5c99a9d9beb7fc33402ad3fb215`  
		Last Modified: Wed, 26 Jan 2022 02:09:25 GMT  
		Size: 56.7 MB (56748326 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c895237e9c3bfa91ff7ae84c795d974fd5125d44c27616d2b3c93a8db31ee9a9`  
		Last Modified: Wed, 26 Jan 2022 02:09:17 GMT  
		Size: 1.2 KB (1173 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:387f888840ae005f11c7b2140cb7c82a98087ea879319d447d976b96a32064d4`  
		Last Modified: Wed, 26 Jan 2022 02:09:17 GMT  
		Size: 908.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
