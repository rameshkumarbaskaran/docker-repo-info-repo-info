## `nats:scratch`

```console
$ docker pull nats@sha256:b1d817c7444c12e37b09ac305dd21d5dc54ee7cb75b2335fa3946a7204ead780
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `nats:scratch` - linux; amd64

```console
$ docker pull nats@sha256:d16e1e48c0ab845192603492b3d9c64445983a3dc5667ec2d581f2870424d68f
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5122711 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0ca39502494bbde906154629d4c0a6e88389a16bf77d69e274587dd1dc8afa4c`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Wed, 21 Jun 2023 00:17:34 GMT
COPY file:0c5b3273ac56fdd9a548c5562dc6cca434baed1b8b5486460a64f797a00263af in /nats-server 
# Wed, 21 Jun 2023 00:17:35 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Wed, 21 Jun 2023 00:17:35 GMT
EXPOSE 4222 6222 8222
# Wed, 21 Jun 2023 00:17:35 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Wed, 21 Jun 2023 00:17:35 GMT
ENTRYPOINT ["/nats-server"]
# Wed, 21 Jun 2023 00:17:35 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:41d97cbbc06ca3db7712fe594a3002518a211924b7a2a273d85c1aa8c1197696`  
		Last Modified: Wed, 21 Jun 2023 00:18:12 GMT  
		Size: 5.1 MB (5122205 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0e2a4ef06e2a4e8f39e43fb44106a50476193b933ecaab0a1d6e582794dd5577`  
		Last Modified: Wed, 21 Jun 2023 00:18:11 GMT  
		Size: 506.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:scratch` - linux; arm variant v6

```console
$ docker pull nats@sha256:6fd7bfb33bbf19e7ccb75c6ac3fcdc072b6120923fdb4e96e29492a5e7b89289
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.9 MB (4890101 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:18d7fa51b81b0dcfb6ee49a1b74a5881dbf8163021afff101d2002b70686142a`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 13 Jul 2023 21:49:27 GMT
COPY file:b5f9cb21b49e06d0ef4d044cf5d2fa6f64bbabb0cfb73701be4fa9d1e7c16c56 in /nats-server 
# Thu, 13 Jul 2023 21:49:27 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Thu, 13 Jul 2023 21:49:27 GMT
EXPOSE 4222 6222 8222
# Thu, 13 Jul 2023 21:49:27 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 13 Jul 2023 21:49:27 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 13 Jul 2023 21:49:27 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:505fc4baba759223316e40a0109c61f162bb1d1acafb25bbc8e92b684cd58c5e`  
		Last Modified: Thu, 13 Jul 2023 21:50:07 GMT  
		Size: 4.9 MB (4889594 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1bc06a01182930b7a494867f205f3a02b099200299bffa49031f3085b8952f64`  
		Last Modified: Thu, 13 Jul 2023 21:50:06 GMT  
		Size: 507.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:scratch` - linux; arm variant v7

```console
$ docker pull nats@sha256:55d0a97fd6b8545229214515f0b602829800d5945d91f12186e2abc4c905cfae
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.9 MB (4876601 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6b98d9a7220cafc3414a842dc2edf402cd1530aa26574de19cfb6f21408a19b4`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Wed, 21 Jun 2023 00:09:33 GMT
COPY file:01958cf912dc4ee20e8b0fb70a3d0de3d63643774adc3ae0be935d8d09c97dab in /nats-server 
# Wed, 21 Jun 2023 00:09:33 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Wed, 21 Jun 2023 00:09:33 GMT
EXPOSE 4222 6222 8222
# Wed, 21 Jun 2023 00:09:33 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Wed, 21 Jun 2023 00:09:33 GMT
ENTRYPOINT ["/nats-server"]
# Wed, 21 Jun 2023 00:09:33 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:da6bffc650385dc011fd2a8b3128dbeca7a7660e2871df1f81f75ba119957e35`  
		Last Modified: Wed, 21 Jun 2023 00:10:13 GMT  
		Size: 4.9 MB (4876094 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a780e691c52c3e5da4018a474c8645c2bdf15a579f4aa28abdc9df5bb929ff41`  
		Last Modified: Wed, 21 Jun 2023 00:10:11 GMT  
		Size: 507.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:scratch` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:3ab6dcfe06a1eee538235ba74c29c53d8fb2d46b7d053aee64b7f6d138ffced8
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.7 MB (4688245 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6bdf6eb10bb37d0efe11e788b04e433ccad9c0838b26bd4dfb8e84d03c3df4fa`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Wed, 21 Jun 2023 00:15:37 GMT
COPY file:6dc04ecbe26e2f3419cc32efecbab24e08c4e5e1159cf103444ed8297e83dfd6 in /nats-server 
# Wed, 21 Jun 2023 00:15:37 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Wed, 21 Jun 2023 00:15:38 GMT
EXPOSE 4222 6222 8222
# Wed, 21 Jun 2023 00:15:38 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Wed, 21 Jun 2023 00:15:38 GMT
ENTRYPOINT ["/nats-server"]
# Wed, 21 Jun 2023 00:15:38 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:719bc06bdd9bd4c4c08d2f3030227de063dc2c6cfdbd8c4dee82757a9b32422d`  
		Last Modified: Wed, 21 Jun 2023 00:16:14 GMT  
		Size: 4.7 MB (4687741 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d8744977fbb1df9e2d0b8b2fd74ea3514e265be3ab31e4147897a9ec1c2274af`  
		Last Modified: Wed, 21 Jun 2023 00:16:13 GMT  
		Size: 504.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
