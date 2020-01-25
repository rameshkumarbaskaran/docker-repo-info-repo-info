## `hylang:0-python3.7-windowsservercore-ltsc2016`

```console
$ docker pull hylang@sha256:b3d34dd8a927fed1dffa95148316d092d2e7c41b103b5770d50cb22e55a7d0a7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.14393.3443; amd64

### `hylang:0-python3.7-windowsservercore-ltsc2016` - windows version 10.0.14393.3443; amd64

```console
$ docker pull hylang@sha256:2fcc9c710921f9a7b2c7d1faf59fc6b7abcb6b8e85f967e8fd95daf469f980d3
```

-	Docker Version: 18.03.1-ee-4
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 GB (5797320075 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9ac1df2eb8416d59dc63ff812c8c6a98db38215a9e52a34c31eb56bfd296ac55`
-	Default Command: `["hy"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sat, 19 Nov 2016 17:05:00 GMT
RUN Apply image 1607-RTM-amd64
# Thu, 02 Jan 2020 15:48:00 GMT
RUN Install update ltsc2016-amd64
# Tue, 14 Jan 2020 23:50:17 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 15 Jan 2020 18:15:45 GMT
ENV PYTHON_VERSION=3.7.6
# Wed, 15 Jan 2020 18:15:46 GMT
ENV PYTHON_RELEASE=3.7.6
# Wed, 15 Jan 2020 18:18:51 GMT
RUN $url = ('https://www.python.org/ftp/python/{0}/python-{1}-amd64.exe' -f $env:PYTHON_RELEASE, $env:PYTHON_VERSION); 	Write-Host ('Downloading {0} ...' -f $url); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $url -OutFile 'python.exe'; 		Write-Host 'Installing ...'; 	Start-Process python.exe -Wait 		-ArgumentList @( 			'/quiet', 			'InstallAllUsers=1', 			'TargetDir=C:\Python', 			'PrependPath=1', 			'Shortcuts=0', 			'Include_doc=0', 			'Include_pip=0', 			'Include_test=0' 		); 		$env:PATH = [Environment]::GetEnvironmentVariable('PATH', [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ...'; 	Write-Host '  python --version'; python --version; 		Write-Host 'Removing ...'; 	Remove-Item python.exe -Force; 		Write-Host 'Complete.'
# Sat, 25 Jan 2020 02:30:50 GMT
ENV PYTHON_PIP_VERSION=20.0.2
# Sat, 25 Jan 2020 02:30:52 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/42ad3426cb1ef05863521d7988d5f7fec0c99560/get-pip.py
# Sat, 25 Jan 2020 02:30:53 GMT
ENV PYTHON_GET_PIP_SHA256=da288fc002d0bb2b90f6fbabc91048c1fa18d567ad067ee713c6e331d3a32b45
# Sat, 25 Jan 2020 02:32:40 GMT
RUN Write-Host ('Downloading get-pip.py ({0}) ...' -f $env:PYTHON_GET_PIP_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:PYTHON_GET_PIP_URL -OutFile 'get-pip.py'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $env:PYTHON_GET_PIP_SHA256); 	if ((Get-FileHash 'get-pip.py' -Algorithm sha256).Hash -ne $env:PYTHON_GET_PIP_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host ('Installing pip=={0} ...' -f $env:PYTHON_PIP_VERSION); 	python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		('pip=={0}' -f $env:PYTHON_PIP_VERSION) 	; 	Remove-Item get-pip.py -Force; 		Write-Host 'Verifying pip install ...'; 	pip --version; 		Write-Host 'Complete.'
# Sat, 25 Jan 2020 02:32:41 GMT
CMD ["python"]
# Sat, 25 Jan 2020 05:07:02 GMT
ENV HY_VERSION=0.17.0
# Sat, 25 Jan 2020 05:08:18 GMT
RUN pip install --no-cache-dir ('hy == {0}' -f $env:HY_VERSION)
# Sat, 25 Jan 2020 05:08:19 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:3889bb8d808bbae6fa5a33e07093e65c31371bcf9e4c38c21be6b9af52ad1548`  
		Last Modified: Tue, 18 Sep 2018 20:20:50 GMT  
		Size: 4.1 GB (4069985900 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:31f9df80631e7b5d379647ee7701ff50e009bd2c03b30a67a0a8e7bba4a26f94`  
		Size: 1.7 GB (1654613376 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:f1c8c4c99f36cfcf87884a9382011e93fb05fa4002d8f4eca62a43e744db8e95`  
		Last Modified: Wed, 15 Jan 2020 01:46:47 GMT  
		Size: 1.2 KB (1208 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:231d068bc7d6ef0d45f3e7928dd8b7316314a79ba961211f403ff4e6af443363`  
		Last Modified: Wed, 15 Jan 2020 18:41:29 GMT  
		Size: 1.2 KB (1210 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a2e6bbf0d2465c626c795a3b859649cabcb07f76f3615f1c6357318a4d51b7e0`  
		Last Modified: Wed, 15 Jan 2020 18:41:28 GMT  
		Size: 1.2 KB (1206 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5eced260e8a270d4df19d1b0e46006c2bd30aa312ff93f9c5e8c9870d92a88b5`  
		Last Modified: Wed, 15 Jan 2020 18:41:59 GMT  
		Size: 56.1 MB (56149516 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4a1e551f40b29cc9febe7710ec872cc14345e63e6aebc6f466826b95716eaae4`  
		Last Modified: Sat, 25 Jan 2020 03:13:25 GMT  
		Size: 1.2 KB (1180 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4d9a12c654e0b0160fe019872b92cf204a5e5c3e6ad764ceb2b419e65ff1b071`  
		Last Modified: Sat, 25 Jan 2020 03:13:25 GMT  
		Size: 1.2 KB (1184 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5e7d5d5904a2f4fa53692b59c1354b5e9d3719a808a620fed17ee55d2c71d019`  
		Last Modified: Sat, 25 Jan 2020 03:13:25 GMT  
		Size: 1.2 KB (1186 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f3dc0c58e4962af366a122d849b8d3b9975be7d076b6d755ea652c43a0186d63`  
		Last Modified: Sat, 25 Jan 2020 03:13:33 GMT  
		Size: 10.4 MB (10373318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5e56c47e9e359ab5eb6e376735228ccba9f5041177803a6d50693217bfa6893e`  
		Last Modified: Sat, 25 Jan 2020 03:13:25 GMT  
		Size: 1.2 KB (1193 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:276f224d8fd2a8915b74109eb246d1cd250d0567a7b686f0c28e061b181aca4a`  
		Last Modified: Sat, 25 Jan 2020 05:13:06 GMT  
		Size: 1.2 KB (1177 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7a3f6b27c554374d49ed0a58aaab5fae2b31a8780718126fde570196b4250eaa`  
		Last Modified: Sat, 25 Jan 2020 05:13:08 GMT  
		Size: 6.2 MB (6187238 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:52053f3678f26581963c594563084db63f16dee9b04bf00f443c7dc59e190694`  
		Last Modified: Sat, 25 Jan 2020 05:13:05 GMT  
		Size: 1.2 KB (1183 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
