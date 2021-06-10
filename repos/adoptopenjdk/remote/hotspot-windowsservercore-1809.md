## `adoptopenjdk:hotspot-windowsservercore-1809`

```console
$ docker pull adoptopenjdk@sha256:87a36e2b7c0a7f270e6b226367c97e97107f8f633bd74279618484d955087b33
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.17763.1999; amd64

### `adoptopenjdk:hotspot-windowsservercore-1809` - windows version 10.0.17763.1999; amd64

```console
$ docker pull adoptopenjdk@sha256:110f6365eb3fcf33f03755d03eb0821d6cd06eb773d5629e0a9e5ad01bf3f71a
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 GB (3019546532 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:00bfdac14868ecc19d7cd12224d0598cc43e58df2b51550db51f01c50de372e7`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 07 May 2020 05:09:25 GMT
RUN Apply image 1809-RTM-amd64
# Sun, 06 Jun 2021 04:28:43 GMT
RUN Install update 1809-amd64
# Wed, 09 Jun 2021 12:10:31 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 09 Jun 2021 18:16:32 GMT
ENV JAVA_VERSION=jdk-16.0.1+9
# Wed, 09 Jun 2021 18:18:04 GMT
RUN Write-Host ('Downloading https://github.com/AdoptOpenJDK/openjdk16-binaries/releases/download/jdk-16.0.1%2B9/OpenJDK16U-jdk_x64_windows_hotspot_16.0.1_9.msi ...');     curl.exe -LfsSo openjdk.msi https://github.com/AdoptOpenJDK/openjdk16-binaries/releases/download/jdk-16.0.1%2B9/OpenJDK16U-jdk_x64_windows_hotspot_16.0.1_9.msi ;     Write-Host ('Verifying sha256 (dc898ec3574e08a90f67fa75808954462749c874ab22c860ded6de051bcc7499) ...');     if ((Get-FileHash openjdk.msi -Algorithm sha256).Hash -ne 'dc898ec3574e08a90f67fa75808954462749c874ab22c860ded6de051bcc7499') {             Write-Host 'FAILED!';             exit 1;     };         New-Item -ItemType Directory -Path C:\temp | Out-Null;         Write-Host 'Installing using MSI ...';     $proc = Start-Process -FilePath "msiexec.exe" -ArgumentList '/i', 'openjdk.msi', '/L*V', 'C:\temp\OpenJDK.log',     '/quiet', 'ADDLOCAL=FeatureEnvironment,FeatureJarFileRunWith,FeatureJavaHome' -Wait -Passthru;     $proc.WaitForExit() ;     if ($proc.ExitCode -ne 0) {             Write-Host 'FAILED installing MSI!' ;             exit 1;     };         Remove-Item -Path C:\temp -Recurse | Out-Null;     Write-Host 'Removing openjdk.msi ...';     Remove-Item openjdk.msi -Force
# Wed, 09 Jun 2021 18:18:07 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:4612f6d0b889cad0ed0292fae3a0b0c8a9e49aff6dea8eb049b2386d9b07986f`  
		Size: 1.7 GB (1718332879 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:639bb6bb2beb4cfdcacb9f0844344448fe26494665d5fe78a494419f86fbb18f`  
		Size: 923.3 MB (923252167 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:7863ef96846d497ea06fe442ea13dcecaf5c248ce238c69800475281a4fa848e`  
		Last Modified: Wed, 09 Jun 2021 12:20:41 GMT  
		Size: 1.4 KB (1431 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8ec063507933c81f52e50bc85dddbc5035b5e91d9551d2f7e3054de1ec65a153`  
		Last Modified: Wed, 09 Jun 2021 19:29:40 GMT  
		Size: 1.4 KB (1441 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5109189b881971c75ef6a62ef2c89796bbee7bcb6703ef81cfe3efbb114296ad`  
		Last Modified: Wed, 09 Jun 2021 19:30:15 GMT  
		Size: 378.0 MB (377957184 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f166de1b9b59e339bccd0699e502a0930759abd5b9f4c64ae18f8ded7f5d4316`  
		Last Modified: Wed, 09 Jun 2021 19:29:41 GMT  
		Size: 1.4 KB (1430 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
