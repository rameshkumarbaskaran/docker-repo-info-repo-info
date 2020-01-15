## `adoptopenjdk:11-hotspot-windowsservercore-1803`

```console
$ docker pull adoptopenjdk@sha256:18f211516d89f87bbad1b5307f3b8eabd5da0bc479027b123bbad9e0277c4eb5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.17134.1246; amd64

### `adoptopenjdk:11-hotspot-windowsservercore-1803` - windows version 10.0.17134.1246; amd64

```console
$ docker pull adoptopenjdk@sha256:8f92a683e0053a9e8d054b90c40f8bb6279e341e99f7e8251a1c72ea75c98bb4
```

-	Docker Version: 18.03.1-ee-4
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 GB (2734311483 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2ead10edbd02b90aedb207b1f516af0a37ddca6aae46725749ecd25dfbce6c0f`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 12 Apr 2018 09:20:54 GMT
RUN Apply image 1803-RTM-amd64
# Wed, 08 Jan 2020 15:30:02 GMT
RUN Install update 1803-amd64
# Wed, 15 Jan 2020 18:58:01 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 15 Jan 2020 19:14:32 GMT
ENV JAVA_VERSION=jdk-11.0.5+10
# Wed, 15 Jan 2020 19:17:37 GMT
RUN Write-Host ('Downloading https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.5%2B10/OpenJDK11U-jdk_x64_windows_hotspot_11.0.5_10.msi ...');         [Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12;         wget https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.5%2B10/OpenJDK11U-jdk_x64_windows_hotspot_11.0.5_10.msi -O 'openjdk.msi';         Write-Host ('Verifying sha256 (692b95374e860daac705ae6c1c351d07a6f5105a1909de68680d556db4f4f426) ...');         if ((Get-FileHash openjdk.msi -Algorithm sha256).Hash -ne '692b95374e860daac705ae6c1c351d07a6f5105a1909de68680d556db4f4f426') {                 Write-Host 'FAILED!';                 exit 1;         };                 New-Item -ItemType Directory -Path C:\temp | Out-Null;                 Write-Host 'Installing using MSI ...';         Start-Process -FilePath "msiexec.exe" -ArgumentList '/i', 'openjdk.msi', '/L*V', 'C:\temp\OpenJDK.log',         '/quiet', 'ADDLOCAL=FeatureEnvironment,FeatureJarFileRunWith,FeatureJavaHome' -Wait -Passthru;         Write-Host 'Removing openjdk.msi ...';         Remove-Item openjdk.msi -Force;         Remove-Item -Path C:\temp -Recurse | Out-Null;
# Wed, 15 Jan 2020 19:17:40 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:d9e8b01179bfc94a5bdb1810fbd76b999aa52016001ace2d3a4c4bc7065a9601`  
		Last Modified: Tue, 18 Sep 2018 22:43:55 GMT  
		Size: 1.7 GB (1659688273 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:270ec3ad3fc7d52c0dd086b32f7751131c799e25cdcd4686cc33cbf2b607c34e`  
		Size: 699.2 MB (699246147 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:4b8ccd780af5210d26057ebca3a11489d01a7a0151f175a60af96d3719ce8bc9`  
		Last Modified: Wed, 15 Jan 2020 20:45:08 GMT  
		Size: 1.2 KB (1212 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:98c10173f75e43b342c7fb6d7e73a144d844d5669ef82d3d819453243a554553`  
		Last Modified: Wed, 15 Jan 2020 20:50:23 GMT  
		Size: 1.2 KB (1182 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b56b8313a42846e67ace5f4ebee2f31f67ec92f168c61f60a5343406314deb9c`  
		Last Modified: Wed, 15 Jan 2020 20:51:13 GMT  
		Size: 375.4 MB (375373472 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c3f615fb3469cd139948db5e4cef47d1b45182a46eb9785f325fcc3c09b1d98d`  
		Last Modified: Wed, 15 Jan 2020 20:50:23 GMT  
		Size: 1.2 KB (1197 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
