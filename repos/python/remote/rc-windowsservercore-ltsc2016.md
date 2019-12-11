## `python:rc-windowsservercore-ltsc2016`

```console
$ docker pull python@sha256:898f9ec3989847a0682977fedeb1d40fd797cdc1d42896ed3a01e37bbe9892b4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.14393.3384; amd64

### `python:rc-windowsservercore-ltsc2016` - windows version 10.0.14393.3384; amd64

```console
$ docker pull python@sha256:b3debc92436be01086f0363a17c7bdfae620d30fb9afb53e30baaa91f163695e
```

-	Docker Version: 18.03.1-ee-4
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 GB (5790142737 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aaeeb7d967df2e912cf82574bae0bf55285552ab2ca2db594c60299a1b2d9ba0`
-	Default Command: `["python"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sat, 19 Nov 2016 17:05:00 GMT
RUN Apply image 1607-RTM-amd64
# Wed, 27 Nov 2019 14:43:00 GMT
RUN Install update ltsc2016-amd64
# Wed, 11 Dec 2019 00:35:49 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 11 Dec 2019 00:35:50 GMT
ENV PYTHON_VERSION=3.9.0a1
# Wed, 11 Dec 2019 00:35:51 GMT
ENV PYTHON_RELEASE=3.9.0
# Wed, 11 Dec 2019 00:39:19 GMT
RUN $url = ('https://www.python.org/ftp/python/{0}/python-{1}-amd64.exe' -f $env:PYTHON_RELEASE, $env:PYTHON_VERSION); 	Write-Host ('Downloading {0} ...' -f $url); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $url -OutFile 'python.exe'; 		Write-Host 'Installing ...'; 	Start-Process python.exe -Wait 		-ArgumentList @( 			'/quiet', 			'InstallAllUsers=1', 			'TargetDir=C:\Python', 			'PrependPath=1', 			'Shortcuts=0', 			'Include_doc=0', 			'Include_pip=0', 			'Include_test=0' 		); 		$env:PATH = [Environment]::GetEnvironmentVariable('PATH', [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ...'; 	Write-Host '  python --version'; python --version; 		Write-Host 'Removing ...'; 	Remove-Item python.exe -Force; 		Write-Host 'Complete.'
# Wed, 11 Dec 2019 00:39:21 GMT
ENV PYTHON_PIP_VERSION=19.3.1
# Wed, 11 Dec 2019 00:39:22 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/ffe826207a010164265d9cc807978e3604d18ca0/get-pip.py
# Wed, 11 Dec 2019 00:39:24 GMT
ENV PYTHON_GET_PIP_SHA256=b86f36cc4345ae87bfd4f10ef6b2dbfa7a872fbff70608a1e43944d283fd0eee
# Wed, 11 Dec 2019 00:41:20 GMT
RUN Write-Host ('Downloading get-pip.py ({0}) ...' -f $env:PYTHON_GET_PIP_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:PYTHON_GET_PIP_URL -OutFile 'get-pip.py'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $env:PYTHON_GET_PIP_SHA256); 	if ((Get-FileHash 'get-pip.py' -Algorithm sha256).Hash -ne $env:PYTHON_GET_PIP_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host ('Installing pip=={0} ...' -f $env:PYTHON_PIP_VERSION); 	python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		('pip=={0}' -f $env:PYTHON_PIP_VERSION) 	; 	Remove-Item get-pip.py -Force; 		Write-Host 'Verifying pip install ...'; 	pip --version; 		Write-Host 'Complete.'
# Wed, 11 Dec 2019 00:41:22 GMT
CMD ["python"]
```

-	Layers:
	-	`sha256:3889bb8d808bbae6fa5a33e07093e65c31371bcf9e4c38c21be6b9af52ad1548`  
		Last Modified: Tue, 18 Sep 2018 20:20:50 GMT  
		Size: 4.1 GB (4069985900 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:55d044e60c8959ce88aee467913bb11827c1ec057a2fd108a293e274dbd74f1d`  
		Size: 1.7 GB (1652717978 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:530e4240d4261ce165890648d1df6230dc4f9ce5df2e6cf9f0d5876694c3d4f0`  
		Last Modified: Wed, 11 Dec 2019 01:14:39 GMT  
		Size: 1.2 KB (1208 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:235d3b8c04f464cb5e6fb61245bd9c50d0ae7ed0ffa73f794e87dc24b508b385`  
		Last Modified: Wed, 11 Dec 2019 01:14:38 GMT  
		Size: 1.2 KB (1210 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1220b0b922564594fbbfe7e85e1b5f5bdbdc0d58c24c3fc35abbf7b1d0a2f8e8`  
		Last Modified: Wed, 11 Dec 2019 01:14:38 GMT  
		Size: 1.2 KB (1154 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:56a6d7e3d8a78bbec5dfaf9c6c5caf6bc36843c6b16465476b4e78a0802c60e4`  
		Last Modified: Wed, 11 Dec 2019 01:15:05 GMT  
		Size: 57.1 MB (57100872 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:76f30c14ac574a444257d8f3383e496a4909b6feb115e3e3df4f1767b59e030a`  
		Last Modified: Wed, 11 Dec 2019 01:14:35 GMT  
		Size: 1.2 KB (1186 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:27a4adddbba8685df6370571160c0a328db3d538a349584002640a1cbe0d6bc5`  
		Last Modified: Wed, 11 Dec 2019 01:14:35 GMT  
		Size: 1.2 KB (1184 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ab6e0deaadf72eda596e21e25810f723da02fbbf2a7ae72ebc3aeca3a1b08345`  
		Last Modified: Wed, 11 Dec 2019 01:14:35 GMT  
		Size: 1.2 KB (1180 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:013438b915e2eeeaed16e0aa3d04c6dc672e69ad56dff1726cbabac5fb010560`  
		Last Modified: Wed, 11 Dec 2019 01:14:47 GMT  
		Size: 10.3 MB (10329680 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf7e51fa4e4cd5d3c1158dfad527110067987ba9f109d3d4ac732c93a0818819`  
		Last Modified: Wed, 11 Dec 2019 01:14:34 GMT  
		Size: 1.2 KB (1185 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
