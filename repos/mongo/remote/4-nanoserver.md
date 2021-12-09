## `mongo:4-nanoserver`

```console
$ docker pull mongo@sha256:182a87098845957150f1a7671a5d2a8a06878f01481525ca6d58fa7796ba7db4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.20348.350; amd64
	-	windows version 10.0.17763.2300; amd64

### `mongo:4-nanoserver` - windows version 10.0.20348.350; amd64

```console
$ docker pull mongo@sha256:14c4836003107cee1f4529d9331a0068bd2cb72dd8a5667f766a5b8c4eafe377
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **350.2 MB (350194849 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:67f1879619da3580683d8b9ce99bf2c632787d562d289f745ac7e374c709d3ff`
-	Default Command: `["mongod","--bind_ip_all"]`
-	`SHELL`: `["cmd","\/S","\/C"]`

```dockerfile
# Wed, 03 Nov 2021 08:13:55 GMT
RUN Apply image ltsc2022-amd64
# Wed, 10 Nov 2021 13:37:46 GMT
SHELL [cmd /S /C]
# Thu, 09 Dec 2021 02:17:56 GMT
USER ContainerAdministrator
# Thu, 09 Dec 2021 02:18:10 GMT
RUN setx /m PATH "C:\mongodb\bin;%PATH%"
# Thu, 09 Dec 2021 02:18:11 GMT
USER ContainerUser
# Thu, 09 Dec 2021 02:18:12 GMT
COPY multi:0196f9e96f60ad3e2b92fd0773f8d0fe3a8235e1eefbb9ef1a1f0d672e6a711c in C:\Windows\System32\ 
# Thu, 09 Dec 2021 02:24:28 GMT
ENV MONGO_VERSION=4.4.10
# Thu, 09 Dec 2021 02:24:54 GMT
COPY dir:38b7137ed0744364da7d2052947e6bc819b65de66682c9d7639e51a11bc90cfa in C:\mongodb 
# Thu, 09 Dec 2021 02:25:11 GMT
RUN mongo --version && mongod --version
# Thu, 09 Dec 2021 02:25:12 GMT
VOLUME [C:\data\db C:\data\configdb]
# Thu, 09 Dec 2021 02:25:13 GMT
EXPOSE 27017
# Thu, 09 Dec 2021 02:25:14 GMT
CMD ["mongod" "--bind_ip_all"]
```

-	Layers:
	-	`sha256:83b9a19f898e6e25b6ee7e787da89582a8528b2defb5682f45364d04b35a278d`  
		Size: 117.1 MB (117116823 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:10d992a589a3ae9381768ac49d33610737b9d4229b1e142eb81c933bc18bab3d`  
		Last Modified: Wed, 10 Nov 2021 14:06:44 GMT  
		Size: 1.2 KB (1159 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:98bccafd0fd699b4f42034a1a80968e4dd05c63c2d0e6a3e3dd8bbc66716e3f8`  
		Last Modified: Thu, 09 Dec 2021 03:24:22 GMT  
		Size: 1.2 KB (1164 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c14f097a17e5aa88d89296d1cc3bd1dad6c43a2701815519f26d90da3980d6c8`  
		Last Modified: Thu, 09 Dec 2021 03:24:20 GMT  
		Size: 85.9 KB (85936 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3ab7b7ae956bad8e7cc44d93558d1d763ef3b49265647c521beaf6e92125f16e`  
		Last Modified: Thu, 09 Dec 2021 03:24:20 GMT  
		Size: 1.2 KB (1152 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dbc33fb039b33b94c48e470c6b2ba97ef5774a05338d436454c045476ae3eee0`  
		Last Modified: Thu, 09 Dec 2021 03:24:20 GMT  
		Size: 274.1 KB (274093 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:213caf07573be1adcdf33caa0fd1dafe44dd9ec0c4d9ede63fef4e6f17f29d52`  
		Last Modified: Thu, 09 Dec 2021 03:35:15 GMT  
		Size: 1.2 KB (1175 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:330338d33a643b12a167d04fd7bd23d54f56e15b538adc8e9e8a4c7b988af45f`  
		Last Modified: Thu, 09 Dec 2021 03:39:14 GMT  
		Size: 232.7 MB (232655390 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:97f2bdc3d670413e2ee6bb63b21abee783ebc418e1ebd7bb0ced21238640dc9d`  
		Last Modified: Thu, 09 Dec 2021 03:35:13 GMT  
		Size: 54.5 KB (54471 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9bb447a3a55228c59801e3cb3a2c5776d9fe5e3fced7ee79c705851bbb52f094`  
		Last Modified: Thu, 09 Dec 2021 03:35:13 GMT  
		Size: 1.2 KB (1156 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a52c907b9b4801fbe1f6c01c2bd72713b61641fe2819339dc97c4cc108e68578`  
		Last Modified: Thu, 09 Dec 2021 03:35:13 GMT  
		Size: 1.2 KB (1167 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eb11ac9ee4a668a43031b16e80f84d79e60ef8c2b279efb8fba998501d6da10e`  
		Last Modified: Thu, 09 Dec 2021 03:35:13 GMT  
		Size: 1.2 KB (1163 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mongo:4-nanoserver` - windows version 10.0.17763.2300; amd64

```console
$ docker pull mongo@sha256:5d95585db4e3aa894ade70b922cd01aa05925bbfc8c8f9f4aa87082acc63f2bf
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **335.8 MB (335840005 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a334f2bb1f617be587b6259c0bec0a64628835efd5a4e6d8fa239ed05a2e1416`
-	Default Command: `["mongod","--bind_ip_all"]`
-	`SHELL`: `["cmd","\/S","\/C"]`

```dockerfile
# Thu, 04 Nov 2021 00:06:50 GMT
RUN Apply image 1809-amd64
# Wed, 10 Nov 2021 13:41:43 GMT
SHELL [cmd /S /C]
# Wed, 10 Nov 2021 19:14:13 GMT
USER ContainerAdministrator
# Wed, 10 Nov 2021 19:14:28 GMT
RUN setx /m PATH "C:\mongodb\bin;%PATH%"
# Wed, 10 Nov 2021 19:14:29 GMT
USER ContainerUser
# Wed, 10 Nov 2021 19:14:30 GMT
COPY multi:0196f9e96f60ad3e2b92fd0773f8d0fe3a8235e1eefbb9ef1a1f0d672e6a711c in C:\Windows\System32\ 
# Wed, 10 Nov 2021 19:20:06 GMT
ENV MONGO_VERSION=4.4.10
# Wed, 10 Nov 2021 19:20:26 GMT
COPY dir:38b7137ed0744364da7d2052947e6bc819b65de66682c9d7639e51a11bc90cfa in C:\mongodb 
# Wed, 10 Nov 2021 19:20:42 GMT
RUN mongo --version && mongod --version
# Wed, 10 Nov 2021 19:20:43 GMT
VOLUME [C:\data\db C:\data\configdb]
# Wed, 10 Nov 2021 19:20:44 GMT
EXPOSE 27017
# Wed, 10 Nov 2021 19:20:45 GMT
CMD ["mongod" "--bind_ip_all"]
```

-	Layers:
	-	`sha256:b9dc943b4e8df8f472d444248152fa0920172ec630a60ada316e1603600dd1c7`  
		Size: 102.8 MB (102782944 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:9fe7a02124d29cd21b5f6d5ea22a1ba3de09099c347d1d0c0e2d89e650ddee00`  
		Last Modified: Wed, 10 Nov 2021 14:07:31 GMT  
		Size: 1.1 KB (1144 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f7a0459f3f99e74f05a8457e55c1f306a65f91eb620f2b335f36b49ce70f8d2f`  
		Last Modified: Wed, 10 Nov 2021 19:40:59 GMT  
		Size: 1.2 KB (1156 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a90c3faaf1ec3abe7f2c84c50d3e74483cba21bd14918c5273cd7577764bf12c`  
		Last Modified: Wed, 10 Nov 2021 19:40:57 GMT  
		Size: 72.1 KB (72092 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:90b354c743ddd6e6dab3fde4cc72bf3fbf21fd4f2f69d57bdb71b204ddbe92c5`  
		Last Modified: Wed, 10 Nov 2021 19:40:57 GMT  
		Size: 1.1 KB (1118 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc81adde81af5d22a9d13bbc929d2143462e050a3c821a78a755b210b322b993`  
		Last Modified: Wed, 10 Nov 2021 19:40:57 GMT  
		Size: 274.1 KB (274065 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:25cf1a1440e8b247508cd979761280f90e4f83abbcfb1b07c185d78c4cf6a1ed`  
		Last Modified: Wed, 10 Nov 2021 19:48:14 GMT  
		Size: 1.2 KB (1160 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db2f862013ab4a7f9bf2dc94f469ad5bf48e98b5f831c638ada3caf26bcba8c5`  
		Last Modified: Wed, 10 Nov 2021 19:48:52 GMT  
		Size: 232.7 MB (232655417 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:375b41ec133fc2034ddb993f5f249bc7c736548d17453157ef55ab0f4865cfe6`  
		Last Modified: Wed, 10 Nov 2021 19:48:11 GMT  
		Size: 47.4 KB (47435 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4452af2b7da334e44a86c0441b0fdcc3cbac3c6c9db5aa91ab7e3af39c43051d`  
		Last Modified: Wed, 10 Nov 2021 19:48:11 GMT  
		Size: 1.1 KB (1136 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a2a74c166c82942f7dacf9bf301378a113ce0950025c4e870cee8b0cc1981c55`  
		Last Modified: Wed, 10 Nov 2021 19:48:11 GMT  
		Size: 1.2 KB (1171 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:98788e7c1d14a7e325bcb72812b505608f493521bc965db638a61839227e9dac`  
		Last Modified: Wed, 10 Nov 2021 19:48:11 GMT  
		Size: 1.2 KB (1167 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
