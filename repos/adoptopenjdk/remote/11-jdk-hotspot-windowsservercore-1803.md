## `adoptopenjdk:11-jdk-hotspot-windowsservercore-1803`

```console
$ docker pull adoptopenjdk@sha256:7ccb76b63dacfcbd946588391b6b8a226e3988f086255538d5ef55a5ac62f052
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.17134.1184; amd64

### `adoptopenjdk:11-jdk-hotspot-windowsservercore-1803` - windows version 10.0.17134.1184; amd64

```console
$ docker pull adoptopenjdk@sha256:100d6e425c91210d533b6ba5b873ec5ec8806ca3bc7d42e9a0d903533519a213
```

-	Docker Version: 18.03.1-ee-4
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 GB (2731935133 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d731f59ffed2ec3493b2132d78c233cfde242aa431dd9919668b3377a13356c8`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 12 Apr 2018 09:20:54 GMT
RUN Apply image 1803-RTM-amd64
# Wed, 04 Dec 2019 15:21:18 GMT
RUN Install update 1803-amd64
# Wed, 11 Dec 2019 20:25:21 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 11 Dec 2019 20:40:29 GMT
ENV JAVA_VERSION=jdk-11.0.5+10
# Wed, 11 Dec 2019 20:43:22 GMT
RUN Write-Host ('Downloading https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.5%2B10/OpenJDK11U-jdk_x64_windows_hotspot_11.0.5_10.msi ...');         [Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12;         wget https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.5%2B10/OpenJDK11U-jdk_x64_windows_hotspot_11.0.5_10.msi -O 'openjdk.msi';         Write-Host ('Verifying sha256 (692b95374e860daac705ae6c1c351d07a6f5105a1909de68680d556db4f4f426) ...');         if ((Get-FileHash openjdk.msi -Algorithm sha256).Hash -ne '692b95374e860daac705ae6c1c351d07a6f5105a1909de68680d556db4f4f426') {                 Write-Host 'FAILED!';                 exit 1;         };                 New-Item -ItemType Directory -Path C:\temp | Out-Null;                 Write-Host 'Installing using MSI ...';         Start-Process -FilePath "msiexec.exe" -ArgumentList '/i', 'openjdk.msi', '/L*V', 'C:\temp\OpenJDK.log',         '/quiet', 'ADDLOCAL=FeatureEnvironment,FeatureJarFileRunWith,FeatureJavaHome' -Wait -Passthru;         Write-Host 'Removing openjdk.msi ...';         Remove-Item openjdk.msi -Force;         Remove-Item -Path C:\temp -Recurse | Out-Null;
# Wed, 11 Dec 2019 20:43:24 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:d9e8b01179bfc94a5bdb1810fbd76b999aa52016001ace2d3a4c4bc7065a9601`  
		Last Modified: Tue, 18 Sep 2018 22:43:55 GMT  
		Size: 1.7 GB (1659688273 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:d117323cd539488e5ef3bef575a41fa714d83119b0da1896607d96ec2a5e3b52`  
		Size: 696.9 MB (696873564 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:76b68c2d6c99fac63a7998081753df26697a83f71d1138943905bde6cb959583`  
		Last Modified: Wed, 11 Dec 2019 22:12:46 GMT  
		Size: 1.1 KB (1141 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8910e7a0ae7cd57d5a29fc540a4121f7d98a0c670b11c2f9fca893ab1a6d1ed7`  
		Last Modified: Wed, 11 Dec 2019 22:17:46 GMT  
		Size: 1.2 KB (1186 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:84377e411b55e7d366c5c1f5aefe1605cb8d8301b144cd4546e06ab7ab18f23c`  
		Last Modified: Wed, 11 Dec 2019 22:18:24 GMT  
		Size: 375.4 MB (375369796 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6a97490f0a15b665ec7f391e285021d15ce66fbd24a65175c2fe487c633211e4`  
		Last Modified: Wed, 11 Dec 2019 22:17:45 GMT  
		Size: 1.2 KB (1173 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
