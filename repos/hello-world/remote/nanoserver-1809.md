## `hello-world:nanoserver-1809`

```console
$ docker pull hello-world@sha256:521c2ecb5cf4e97152ea72449a05d5594764cc5d16711aabe25fd80ab847d010
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.4131; amd64

### `hello-world:nanoserver-1809` - windows version 10.0.17763.4131; amd64

```console
$ docker pull hello-world@sha256:222fd58970d97d818081fee49fa57821d0acad88697639692e5cd0bd26f9f174
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **106.7 MB (106687219 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:04b63a3baea853aac4d28ea13c9fcea23eadc7d948b41997d55ca78e61a5675f`
-	Default Command: `["cmd","\/C","type C:\\hello.txt"]`

```dockerfile
# Sat, 11 Mar 2023 10:09:02 GMT
RUN Apply image 10.0.17763.4131
# Thu, 16 Mar 2023 02:54:10 GMT
RUN cmd /S /C #(nop) COPY file:994f63bc3cea8285310afa5f4677df29bf99dd4cd1881c7e381100a9e794ba71 in C: 
# Thu, 16 Mar 2023 02:54:11 GMT
RUN cmd /S /C #(nop)  CMD ["cmd" "/C" "type C:\\hello.txt"]
```

-	Layers:
	-	`sha256:95eb2f0f3287f5ec687287cc244924aafc74c7ada3121d43f54223487f3f2d8d`  
		Last Modified: Thu, 16 Mar 2023 01:43:14 GMT  
		Size: 106.7 MB (106684240 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:285b306a8caaa9cc04c39708af1068f83c88903fbe9cef0efe0f43f75c088636`  
		Last Modified: Thu, 16 Mar 2023 02:54:34 GMT  
		Size: 1.9 KB (1860 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b2e3ab839ded2a87c69c52b021e5647d6eb7202012349c2f36ea1e27c319a191`  
		Last Modified: Thu, 16 Mar 2023 02:54:33 GMT  
		Size: 1.1 KB (1119 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
