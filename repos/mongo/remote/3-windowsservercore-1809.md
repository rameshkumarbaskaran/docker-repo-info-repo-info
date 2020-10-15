## `mongo:3-windowsservercore-1809`

```console
$ docker pull mongo@sha256:c57a92116796c8ea9166fcd99b44b581fca3d6daf6caa3c8bea06c238083d98e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.17763.1518; amd64

### `mongo:3-windowsservercore-1809` - windows version 10.0.17763.1518; amd64

```console
$ docker pull mongo@sha256:b8fefcddbb21895882a3482395682ef472c52db6ba6eb096740c55bcca6828d8
```

-	Docker Version: 19.03.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 GB (3069087808 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:29ab4912c4fd77cd0395d2cd593e631bd8e6c28c10524af7140e31c60f21262f`
-	Default Command: `["mongod","--bind_ip_all"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Thu, 07 May 2020 05:09:25 GMT
RUN Apply image 1809-RTM-amd64
# Thu, 01 Oct 2020 02:26:38 GMT
RUN Install update 1809-amd64
# Wed, 14 Oct 2020 12:58:33 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Wed, 14 Oct 2020 21:47:31 GMT
ENV MONGO_VERSION=3.6.20
# Wed, 14 Oct 2020 21:47:31 GMT
ENV MONGO_DOWNLOAD_URL=https://fastdl.mongodb.org/win32/mongodb-win32-x86_64-2008plus-ssl-3.6.20-signed.msi
# Wed, 14 Oct 2020 21:47:32 GMT
ENV MONGO_DOWNLOAD_SHA256=341d1163c192488596e01219b50c14c9113ad0c305b0aef73f271d9746e44aa1
# Wed, 14 Oct 2020 22:11:52 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:MONGO_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	(New-Object System.Net.WebClient).DownloadFile($env:MONGO_DOWNLOAD_URL, 'mongo.msi'); 		if ($env:MONGO_DOWNLOAD_SHA256) { 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:MONGO_DOWNLOAD_SHA256); 		if ((Get-FileHash mongo.msi -Algorithm sha256).Hash -ne $env:MONGO_DOWNLOAD_SHA256) { 			Write-Host 'FAILED!'; 			exit 1; 		}; 	}; 		Write-Host 'Installing ...'; 	Start-Process msiexec -Wait 		-ArgumentList @( 			'/i', 			'mongo.msi', 			'/quiet', 			'/qn', 			'INSTALLLOCATION=C:\mongodb', 			'ADDLOCAL=all' 		); 	$env:PATH = 'C:\mongodb\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ...'; 	Write-Host '  mongo --version'; mongo --version; 	Write-Host '  mongod --version'; mongod --version; 		Write-Host 'Removing ...'; 	Remove-Item C:\windows\installer\*.msi -Force; 	Remove-Item mongo.msi -Force; 		Write-Host 'Complete.';
# Wed, 14 Oct 2020 22:11:54 GMT
VOLUME [C:\data\db C:\data\configdb]
# Wed, 14 Oct 2020 22:11:55 GMT
EXPOSE 27017
# Wed, 14 Oct 2020 22:11:56 GMT
CMD ["mongod" "--bind_ip_all"]
```

-	Layers:
	-	`sha256:4612f6d0b889cad0ed0292fae3a0b0c8a9e49aff6dea8eb049b2386d9b07986f`  
		Size: 1.7 GB (1718332879 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:406ffb8432a757e84f7594e85c676620dec6955e0475ac271aa4dd5c0531190d`  
		Size: 655.8 MB (655757265 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:d839ec6fa74e5e869036dfd823e95452a7afcde18ac997af483c88c21b92ad8c`  
		Last Modified: Wed, 14 Oct 2020 16:02:33 GMT  
		Size: 1.1 KB (1129 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:24247f3bb51d1d4e86da74443bc2c07ab23d165aa6e07f2a5a2d99cf05c7e09f`  
		Last Modified: Wed, 14 Oct 2020 23:57:46 GMT  
		Size: 1.2 KB (1154 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ad14823774a10cba45ad99901994ea512b74289f543aad2974750f173ca9bee0`  
		Last Modified: Wed, 14 Oct 2020 23:57:47 GMT  
		Size: 1.1 KB (1123 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:082fab4a2a46a94445439e0ffbca86e7d33ca34a8471e9912ba73b5677f59305`  
		Last Modified: Wed, 14 Oct 2020 23:57:44 GMT  
		Size: 1.1 KB (1149 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:322ee7b70d12bd5de38d86cec245f4e621040b3ab8f19193a78ffe5b16895f9c`  
		Last Modified: Thu, 15 Oct 2020 00:04:56 GMT  
		Size: 695.0 MB (694989660 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a07f92a202efa518a36564623a29e77f98156933bad8ae7cd1aa620c26135d22`  
		Last Modified: Wed, 14 Oct 2020 23:57:44 GMT  
		Size: 1.2 KB (1177 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e53e24915deaffd8e1fe632ebb6ccee3d6189366052f323b4739dcfc5af05978`  
		Last Modified: Wed, 14 Oct 2020 23:57:43 GMT  
		Size: 1.1 KB (1135 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:651fa935973ca4316c01b23f45eb6a2dacb626bd8df8ff766a1483ee06a1c327`  
		Last Modified: Wed, 14 Oct 2020 23:57:44 GMT  
		Size: 1.1 KB (1137 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
