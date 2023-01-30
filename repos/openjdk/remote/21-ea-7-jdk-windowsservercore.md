## `openjdk:21-ea-7-jdk-windowsservercore`

```console
$ docker pull openjdk@sha256:f69dd9df432738edd3db790abd60d9e89a4a4dbdd46e287c8e55289606320831
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.20348.1487; amd64
	-	windows version 10.0.17763.3887; amd64

### `openjdk:21-ea-7-jdk-windowsservercore` - windows version 10.0.20348.1487; amd64

```console
$ docker pull openjdk@sha256:8a4556ff179f5ab4647b7f920703c6f687d2561bbfdcbf1fb8914668594003f9
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.6 GB (1581876272 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:afaa47bfd6bcdc3303972f5e14c0e1257486f1c9ff7ad19d771ac98f112006aa`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Jan 2023 23:47:40 GMT
RUN Apply image 10.0.20348.1487
# Thu, 12 Jan 2023 01:40:34 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 12 Jan 2023 05:07:34 GMT
RUN Write-Host 'Enabling TLS 1.2 (https://githubengineering.com/crypto-removal-notice/) ...'; 	$tls12RegBase = 'HKLM:\\SYSTEM\CurrentControlSet\Control\SecurityProviders\SCHANNEL\Protocols\TLS 1.2'; 	if (Test-Path $tls12RegBase) { throw ('"{0}" already exists!' -f $tls12RegBase) }; 	New-Item -Path ('{0}/Client' -f $tls12RegBase) -Force; 	New-Item -Path ('{0}/Server' -f $tls12RegBase) -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	Write-Host 'Complete.'
# Thu, 12 Jan 2023 05:07:35 GMT
ENV JAVA_HOME=C:\openjdk-21
# Thu, 12 Jan 2023 05:07:57 GMT
RUN $newPath = ('{0}\bin;{1}' -f $env:JAVA_HOME, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	setx /M PATH $newPath; 	Write-Host 'Complete.'
# Mon, 30 Jan 2023 19:16:14 GMT
ENV JAVA_VERSION=21-ea+7
# Mon, 30 Jan 2023 19:16:16 GMT
ENV JAVA_URL=https://download.java.net/java/early_access/jdk21/7/GPL/openjdk-21-ea+7_windows-x64_bin.zip
# Mon, 30 Jan 2023 19:16:17 GMT
ENV JAVA_SHA256=5a2689afd238ad9016a4f205b48d6e2aea38b9622f64f9c962cceee06bd04ecb
# Mon, 30 Jan 2023 19:17:20 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JAVA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JAVA_URL -OutFile 'openjdk.zip'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $env:JAVA_SHA256); 	if ((Get-FileHash openjdk.zip -Algorithm sha256).Hash -ne $env:JAVA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	New-Item -ItemType Directory -Path C:\temp | Out-Null; 	Expand-Archive openjdk.zip -DestinationPath C:\temp; 	Move-Item -Path C:\temp\* -Destination $env:JAVA_HOME; 	Remove-Item C:\temp; 		Write-Host 'Removing ...'; 	Remove-Item openjdk.zip -Force; 		Write-Host 'Verifying install ...'; 	Write-Host '  javac --version'; javac --version; 	Write-Host '  java --version'; java --version; 		Write-Host 'Complete.'
# Mon, 30 Jan 2023 19:17:22 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:1a65b089bc835b0c3700397b1935e97cf469b0891bb4de3942c8dfbe4b672d47`  
		Last Modified: Thu, 12 Jan 2023 02:33:52 GMT  
		Size: 1.4 GB (1386029089 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa41f3a43cc9e40e953b9cfe1530c27eed49cf79cdae96e9dfc39b04a1b75ecf`  
		Last Modified: Thu, 12 Jan 2023 02:29:45 GMT  
		Size: 1.4 KB (1427 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6aa8e5b91e3c425a756945d0dec251c1595992592fd0dcf4df0ec0a7962717eb`  
		Last Modified: Thu, 12 Jan 2023 05:22:24 GMT  
		Size: 614.6 KB (614563 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6284573ed998f0926754c8fd5dc7faff95102e54cf06b0d280cd07428b048e11`  
		Last Modified: Thu, 12 Jan 2023 05:22:23 GMT  
		Size: 1.4 KB (1389 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fee2720203565dd5e40979d2f76187379d7c05254dd58609d0f974f653b1db40`  
		Last Modified: Thu, 12 Jan 2023 05:22:24 GMT  
		Size: 552.5 KB (552462 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a24dc1f826d4ee38379bbf6318745f66cf8ae02a1028d3696a6d4f5dc5aa7ad8`  
		Last Modified: Mon, 30 Jan 2023 19:26:38 GMT  
		Size: 1.3 KB (1317 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:00d1e1c9ddec76feb9006c16ed9d34d337713e2042f1ad3fc486b5a973d329be`  
		Last Modified: Mon, 30 Jan 2023 19:26:38 GMT  
		Size: 1.3 KB (1339 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ccf2fcf69a835bd99f97dbaf9c3375b4f79b1e9395af562dfb0539ab00490ea`  
		Last Modified: Mon, 30 Jan 2023 19:26:38 GMT  
		Size: 1.3 KB (1316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ceabe7a6c1808be256396e5b906b219aaa2e783812b755fafbc830e72c8ff6a`  
		Last Modified: Mon, 30 Jan 2023 19:27:02 GMT  
		Size: 194.7 MB (194672087 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:29b75656a32fd08c24ef440446afbc36e17e4406c2365b2e67d2b28d9022e75d`  
		Last Modified: Mon, 30 Jan 2023 19:26:38 GMT  
		Size: 1.3 KB (1283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `openjdk:21-ea-7-jdk-windowsservercore` - windows version 10.0.17763.3887; amd64

```console
$ docker pull openjdk@sha256:91007447805e5a1e51ea4bc7adea40b321b5c4f1e5810a623f27ea91be811fd0
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.9 GB (1903102545 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0836e4a285e6ea19613cb68b4bdf5946c317b6f5746638cf27e64e5ba3f5305e`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sat, 07 Jan 2023 05:37:58 GMT
RUN Apply image 10.0.17763.3887
# Thu, 12 Jan 2023 01:43:02 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 12 Jan 2023 05:09:35 GMT
RUN Write-Host 'Enabling TLS 1.2 (https://githubengineering.com/crypto-removal-notice/) ...'; 	$tls12RegBase = 'HKLM:\\SYSTEM\CurrentControlSet\Control\SecurityProviders\SCHANNEL\Protocols\TLS 1.2'; 	if (Test-Path $tls12RegBase) { throw ('"{0}" already exists!' -f $tls12RegBase) }; 	New-Item -Path ('{0}/Client' -f $tls12RegBase) -Force; 	New-Item -Path ('{0}/Server' -f $tls12RegBase) -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	Write-Host 'Complete.'
# Thu, 12 Jan 2023 05:09:36 GMT
ENV JAVA_HOME=C:\openjdk-21
# Thu, 12 Jan 2023 05:10:00 GMT
RUN $newPath = ('{0}\bin;{1}' -f $env:JAVA_HOME, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	setx /M PATH $newPath; 	Write-Host 'Complete.'
# Mon, 30 Jan 2023 19:17:34 GMT
ENV JAVA_VERSION=21-ea+7
# Mon, 30 Jan 2023 19:17:35 GMT
ENV JAVA_URL=https://download.java.net/java/early_access/jdk21/7/GPL/openjdk-21-ea+7_windows-x64_bin.zip
# Mon, 30 Jan 2023 19:17:36 GMT
ENV JAVA_SHA256=5a2689afd238ad9016a4f205b48d6e2aea38b9622f64f9c962cceee06bd04ecb
# Mon, 30 Jan 2023 19:18:51 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JAVA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JAVA_URL -OutFile 'openjdk.zip'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $env:JAVA_SHA256); 	if ((Get-FileHash openjdk.zip -Algorithm sha256).Hash -ne $env:JAVA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	New-Item -ItemType Directory -Path C:\temp | Out-Null; 	Expand-Archive openjdk.zip -DestinationPath C:\temp; 	Move-Item -Path C:\temp\* -Destination $env:JAVA_HOME; 	Remove-Item C:\temp; 		Write-Host 'Removing ...'; 	Remove-Item openjdk.zip -Force; 		Write-Host 'Verifying install ...'; 	Write-Host '  javac --version'; javac --version; 	Write-Host '  java --version'; java --version; 		Write-Host 'Complete.'
# Mon, 30 Jan 2023 19:18:53 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:6e222c5ada69382aa2b4fe30b23ae56c7e3ada92712109d20f3edd457a6120b6`  
		Last Modified: Thu, 12 Jan 2023 02:40:02 GMT  
		Size: 1.7 GB (1707943932 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:691d210e0841eeceff800f3b441be6db4bc689728f1bb771ce88f839d06f57d0`  
		Last Modified: Thu, 12 Jan 2023 02:34:04 GMT  
		Size: 1.4 KB (1433 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b1fe1d317f0927d209417077d671ba0fb8e3b7ff9c583727da819f0d16252e80`  
		Last Modified: Thu, 12 Jan 2023 05:23:04 GMT  
		Size: 367.5 KB (367453 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f6807e3d75deac242f3cfe460728c148c2f68e1d8366ad3f0358a3c9237042b6`  
		Last Modified: Thu, 12 Jan 2023 05:23:04 GMT  
		Size: 1.4 KB (1396 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ebbe0b64cf9fa2560a38a4c1a75582463f16f8e35e9776b14d87cd13167e4281`  
		Last Modified: Thu, 12 Jan 2023 05:23:04 GMT  
		Size: 320.0 KB (320032 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d96ae69a96d28380ec7f365e2d0adafd09cc2978544b8eb13b68326446e666d3`  
		Last Modified: Mon, 30 Jan 2023 19:27:19 GMT  
		Size: 1.3 KB (1320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8e63de4ee3afec3d8aa7f112dbca6788a32ef5a4fdbcb5249c1b96693fb3540a`  
		Last Modified: Mon, 30 Jan 2023 19:27:19 GMT  
		Size: 1.3 KB (1311 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ad65860f84d10690f5b2d381f5f59de772b8166960ddc06e7726658787f590d7`  
		Last Modified: Mon, 30 Jan 2023 19:27:19 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ed721d6d51aea5eb5fc419c21751cec90313fed43c0f6fe70ac65fbe8cb8754`  
		Last Modified: Mon, 30 Jan 2023 19:27:43 GMT  
		Size: 194.5 MB (194463093 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e67de36a0bc7df29368ba7c7d4b4da9d93cf3552e514d557bafaf303f2787920`  
		Last Modified: Mon, 30 Jan 2023 19:27:19 GMT  
		Size: 1.3 KB (1281 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
