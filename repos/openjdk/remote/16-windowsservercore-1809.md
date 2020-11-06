## `openjdk:16-windowsservercore-1809`

```console
$ docker pull openjdk@sha256:bd58bf5b1f59494ffead7b3578d9ad54cd5cbbd009965b41b638ec5a2d1b71af
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.17763.1518; amd64

### `openjdk:16-windowsservercore-1809` - windows version 10.0.17763.1518; amd64

```console
$ docker pull openjdk@sha256:f57e71872f6308e399da2864e43236e3caa87f7c1746243b9e53516f0a36784d
```

-	Docker Version: 19.03.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 GB (2567078527 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:be250edaabe02d092cd093d8db90b2b72200a4789d40a482be65ecdc8f028bb5`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 07 May 2020 05:09:25 GMT
RUN Apply image 1809-RTM-amd64
# Thu, 01 Oct 2020 02:26:38 GMT
RUN Install update 1809-amd64
# Wed, 14 Oct 2020 12:27:02 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 14 Oct 2020 17:38:17 GMT
RUN Write-Host 'Enabling TLS 1.2 (https://githubengineering.com/crypto-removal-notice/) ...'; 	$tls12RegBase = 'HKLM:\\SYSTEM\CurrentControlSet\Control\SecurityProviders\SCHANNEL\Protocols\TLS 1.2'; 	if (Test-Path $tls12RegBase) { throw ('"{0}" already exists!' -f $tls12RegBase) }; 	New-Item -Path ('{0}/Client' -f $tls12RegBase) -Force; 	New-Item -Path ('{0}/Server' -f $tls12RegBase) -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force
# Wed, 14 Oct 2020 17:38:18 GMT
ENV JAVA_HOME=C:\openjdk-16
# Wed, 14 Oct 2020 17:38:40 GMT
RUN $newPath = ('{0}\bin;{1}' -f $env:JAVA_HOME, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	setx /M PATH $newPath
# Fri, 06 Nov 2020 18:15:44 GMT
ENV JAVA_VERSION=16-ea+23
# Fri, 06 Nov 2020 18:15:45 GMT
ENV JAVA_URL=https://download.java.net/java/early_access/jdk16/23/GPL/openjdk-16-ea+23_windows-x64_bin.zip
# Fri, 06 Nov 2020 18:15:46 GMT
ENV JAVA_SHA256=43cfcadc298b570dd697c74e67886ebcaad569357e4c38d24e5d0ebaded77fb6
# Fri, 06 Nov 2020 18:17:35 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JAVA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JAVA_URL -OutFile 'openjdk.zip'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $env:JAVA_SHA256); 	if ((Get-FileHash openjdk.zip -Algorithm sha256).Hash -ne $env:JAVA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	New-Item -ItemType Directory -Path C:\temp | Out-Null; 	Expand-Archive openjdk.zip -DestinationPath C:\temp; 	Move-Item -Path C:\temp\* -Destination $env:JAVA_HOME; 	Remove-Item C:\temp; 		Write-Host 'Removing ...'; 	Remove-Item openjdk.zip -Force; 		Write-Host 'Verifying install ...'; 	Write-Host '  javac --version'; javac --version; 	Write-Host '  java --version'; java --version; 		Write-Host 'Complete.'
# Fri, 06 Nov 2020 18:17:37 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:4612f6d0b889cad0ed0292fae3a0b0c8a9e49aff6dea8eb049b2386d9b07986f`  
		Size: 1.7 GB (1718332879 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:406ffb8432a757e84f7594e85c676620dec6955e0475ac271aa4dd5c0531190d`  
		Size: 655.8 MB (655757265 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:5e61fff845eda39f31bdf5d797254fdf656ee79d8c294c1713007864bc4c2535`  
		Last Modified: Wed, 14 Oct 2020 12:50:32 GMT  
		Size: 1.1 KB (1130 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6b5f8e5825cfa7b4f8c5a50657da7a44c0547d90306b4fa11bbf82021b684262`  
		Last Modified: Wed, 14 Oct 2020 18:26:50 GMT  
		Size: 9.2 MB (9230486 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:01e034563561e5379df3a00fd4da250e977243aacd8623dc768db3ef40497b87`  
		Last Modified: Wed, 14 Oct 2020 18:26:42 GMT  
		Size: 1.1 KB (1123 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:24997a5d1f99495d60fc79a47ec6d7bcf172f637b322078eccbc230cebf01c74`  
		Last Modified: Wed, 14 Oct 2020 18:26:42 GMT  
		Size: 307.8 KB (307821 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6a957802d7c07d39a76147b405edafa7966752e14c31229fc9fdd77b5834ab52`  
		Last Modified: Fri, 06 Nov 2020 18:25:28 GMT  
		Size: 1.1 KB (1129 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4d61b9aedc424ed7ec570370ab5e44b87769dc53dba7684dca8619583b09b64f`  
		Last Modified: Fri, 06 Nov 2020 18:25:29 GMT  
		Size: 1.1 KB (1135 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d34cc117757ad48c5d9ef700a1fa86ddfa449743b9388d31f38f9ec51e73b19`  
		Last Modified: Fri, 06 Nov 2020 18:25:30 GMT  
		Size: 1.2 KB (1161 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:66c9751f4facc9c4e50cca92fa43a10f26428e51442a1f5b969c4e67ba575154`  
		Last Modified: Fri, 06 Nov 2020 18:25:50 GMT  
		Size: 183.4 MB (183443265 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f99eb695f0451e1b566be5d8c2f5d7e184efa6afc214a94a14d96edb71e1e4b`  
		Last Modified: Fri, 06 Nov 2020 18:25:34 GMT  
		Size: 1.1 KB (1133 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
