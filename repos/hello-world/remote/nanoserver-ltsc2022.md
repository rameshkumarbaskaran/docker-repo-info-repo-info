## `hello-world:nanoserver-ltsc2022`

```console
$ docker pull hello-world@sha256:d171f6d0737dca64527c042b5c877cd1d397a4c504e1ad9ccd60ef355f965213
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.1607; amd64

### `hello-world:nanoserver-ltsc2022` - windows version 10.0.20348.1607; amd64

```console
$ docker pull hello-world@sha256:f5094c800af671abfc125480b44bd223bdb54d0d2b065de6f9f8e9cdf25dead8
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **122.2 MB (122174756 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6eb663712d0b9dd755690f9a9339d8f82f565f9e1502aad7e9cc50f5e054b1b1`
-	Default Command: `["cmd","\/C","type C:\\hello.txt"]`

```dockerfile
# Fri, 10 Mar 2023 06:31:34 GMT
RUN Apply image 10.0.20348.1607
# Thu, 16 Mar 2023 02:54:00 GMT
RUN cmd /S /C #(nop) COPY file:ac9f104fd739943f22886335a779468d86b20ac43fd3168171f6b23fc28882b9 in C: 
# Thu, 16 Mar 2023 02:54:01 GMT
RUN cmd /S /C #(nop)  CMD ["cmd" "/C" "type C:\\hello.txt"]
```

-	Layers:
	-	`sha256:7abf0a70d48bf65f3d985f5780d4bdaece36f1f4bb8be10d5a6aacce33dacc75`  
		Last Modified: Thu, 16 Mar 2023 01:54:24 GMT  
		Size: 122.2 MB (122171731 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:63bea342840d705357efe1b72927dcbeaf97949d81b30efc809a1c3f498fd51e`  
		Last Modified: Thu, 16 Mar 2023 02:54:28 GMT  
		Size: 1.9 KB (1853 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ba5cd160e3372d85f317c2a4f399b0ae30b5253cdce9abcdab20f9fda0344d3`  
		Last Modified: Thu, 16 Mar 2023 02:54:28 GMT  
		Size: 1.2 KB (1172 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
