## `mongo:4-nanoserver-1809`

```console
$ docker pull mongo@sha256:2e24e19ce2b093faec1281817ff84f1d50d1d33f2fea0e118db96fff744c29cf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.3046; amd64

### `mongo:4-nanoserver-1809` - windows version 10.0.17763.3046; amd64

```console
$ docker pull mongo@sha256:cc2aed3a1a2a9129e6d04f5e45fbae2d793c37a58e6cffc9b062b291ebb5c37c
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **345.1 MB (345074164 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fbc86a766a1f06dd046b51ae3ee4b4467e29f3ae5711589b31612147c049f2e1`
-	Default Command: `["mongod","--bind_ip_all"]`
-	`SHELL`: `["cmd","\/S","\/C"]`

```dockerfile
# Thu, 09 Jun 2022 19:20:11 GMT
RUN Apply image 10.0.17763.3046
# Wed, 15 Jun 2022 13:18:02 GMT
SHELL [cmd /S /C]
# Wed, 15 Jun 2022 21:09:01 GMT
USER ContainerAdministrator
# Wed, 15 Jun 2022 21:09:31 GMT
RUN setx /m PATH "C:\mongodb\bin;%PATH%"
# Wed, 15 Jun 2022 21:09:32 GMT
USER ContainerUser
# Wed, 15 Jun 2022 21:09:33 GMT
COPY multi:9a4a91c322ba6325a22891e3a40eb7306a49c53e11d5828931f2326770a3f548 in C:\Windows\System32\ 
# Wed, 15 Jun 2022 21:15:38 GMT
ENV MONGO_VERSION=4.4.14
# Wed, 15 Jun 2022 21:16:03 GMT
COPY dir:5db4d92801abb4c6b6f16e80c283eda3a5fdc6431914dfb8699f556acea891c1 in C:\mongodb 
# Wed, 15 Jun 2022 21:16:18 GMT
RUN mongo --version && mongod --version
# Wed, 15 Jun 2022 21:16:19 GMT
VOLUME [C:\data\db C:\data\configdb]
# Wed, 15 Jun 2022 21:16:20 GMT
EXPOSE 27017
# Wed, 15 Jun 2022 21:16:21 GMT
CMD ["mongod" "--bind_ip_all"]
```

-	Layers:
	-	`sha256:d555a7e4de4dd775379d5c43c1419374bff7908670dc7444be5e8e8f386f3d26`  
		Size: 103.2 MB (103153235 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:1ec2e0a40359897e8d5f91d9806e952d9783f2bc30dd279b63a217ee6985ef3c`  
		Last Modified: Wed, 15 Jun 2022 14:07:45 GMT  
		Size: 1.2 KB (1164 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d19bba12342216b396550bee0fd1ec81490efee021917ee03cd358c63f84ba8`  
		Last Modified: Wed, 15 Jun 2022 21:54:02 GMT  
		Size: 1.2 KB (1187 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1482fe090238b0a466d117555441f2f20f684020b14f8c6ab297c5e213d39b5e`  
		Last Modified: Wed, 15 Jun 2022 21:53:57 GMT  
		Size: 70.5 KB (70534 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb8a70e7a7c337b61c46d7d53947831d7a343ec9b3afc2f1ac6909de090c0e88`  
		Last Modified: Wed, 15 Jun 2022 21:53:56 GMT  
		Size: 1.2 KB (1165 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5d7c468f9b42d6946f0bee90ae8ef2b05161d9e5f7f6de932d1e31ae7a9728dc`  
		Last Modified: Wed, 15 Jun 2022 21:53:48 GMT  
		Size: 263.5 KB (263496 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a43bc191f9795894f8120276f3951c4e2a7b60223827e2212e1b5585e8654956`  
		Last Modified: Wed, 15 Jun 2022 22:05:30 GMT  
		Size: 1.2 KB (1178 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a4edad4578563bb6d488e73df31d3f1ffb95d8d97096bb1ba9e3002725bdb8ac`  
		Last Modified: Wed, 15 Jun 2022 22:06:15 GMT  
		Size: 241.5 MB (241502321 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3bcb2674f37712ba369d220b2b2f4a740550bb953e202e71daa5192313073178`  
		Last Modified: Wed, 15 Jun 2022 22:05:27 GMT  
		Size: 76.4 KB (76386 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6e8ff006b2815babd4c15de129ed6949d0260177d2474cbcc4e4ef21015d7747`  
		Last Modified: Wed, 15 Jun 2022 22:05:27 GMT  
		Size: 1.2 KB (1168 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ab0fc1841075c90c2e10e37e16071ea1743b01c92a22de4396fef481f8193b62`  
		Last Modified: Wed, 15 Jun 2022 22:05:27 GMT  
		Size: 1.2 KB (1161 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c2347e7dda916034e6a039e1ff9e816c65d0065cbab8ea1d423674fa205f169c`  
		Last Modified: Wed, 15 Jun 2022 22:05:27 GMT  
		Size: 1.2 KB (1169 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
