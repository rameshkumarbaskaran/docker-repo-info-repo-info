## `fsharp:netcore`

```console
$ docker pull fsharp@sha256:338e3165d3f949dc4456bfafccb059eb779d65dcdccf17957ebe9f38126c3951
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `fsharp:netcore` - linux; amd64

```console
$ docker pull fsharp@sha256:afd213519955896709e418d94265266a07e3f04c6865d0c4c7129d1e9f90e763
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **323.7 MB (323681564 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c0bb968af12efda715c13ad474c6d4821cd501520abff2a03b284ffc332caa32`
-	Default Command: `["dotnet","fsi"]`

```dockerfile
# Thu, 16 Apr 2020 03:22:36 GMT
ADD file:865f9041e12eb341f0a394764ddc11db49cbc8b91d4fb57c6fb1960b68b1bb41 in / 
# Thu, 16 Apr 2020 03:22:36 GMT
CMD ["bash"]
# Thu, 16 Apr 2020 04:35:35 GMT
LABEL maintainer=Dave Curylo <dave@curylo.org>, Steve Desmond <steve@stevedesmond.ca>
# Thu, 16 Apr 2020 04:35:35 GMT
ENV MONO_THREADS_PER_CPU=50
# Thu, 16 Apr 2020 04:47:54 GMT
RUN MONO_VERSION=6.8.0.105 &&     FSHARP_VERSION=10.2.3 &&     FSHARP_BASENAME=fsharp-$FSHARP_VERSION &&     FSHARP_ARCHIVE=$FSHARP_VERSION.tar.gz &&     FSHARP_ARCHIVE_URL=https://github.com/fsharp/fsharp/archive/$FSHARP_VERSION.tar.gz &&     export GNUPGHOME="$(mktemp -d)" &&     apt-get update && apt-get --no-install-recommends install -y gnupg dirmngr ca-certificates apt-transport-https &&     apt-key adv --batch --keyserver hkp://p80.pool.sks-keyservers.net:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF &&     echo "deb https://download.mono-project.com/repo/debian stable-buster/snapshots/$MONO_VERSION main" | tee /etc/apt/sources.list.d/mono-official-stable.list &&     apt-get update -y &&     apt-get --no-install-recommends install -y pkg-config make nuget mono-devel msbuild ca-certificates-mono locales &&     rm -rf /var/lib/apt/lists/* &&     echo 'en_US.UTF-8 UTF-8' > /etc/locale.gen && /usr/sbin/locale-gen &&     mkdir -p /tmp/src &&     cd /tmp/src &&     printf "namespace a { class b { public static void Main(string[] args) { new System.Net.WebClient().DownloadFile(\"%s\", \"%s\");}}}" $FSHARP_ARCHIVE_URL $FSHARP_ARCHIVE > download-fsharp.cs &&     mcs download-fsharp.cs && mono download-fsharp.exe && rm download-fsharp.exe download-fsharp.cs &&     tar xf $FSHARP_ARCHIVE &&     cd $FSHARP_BASENAME &&     make &&     make install &&     cd ~ &&     rm -rf /tmp/src /tmp/NuGetScratch ~/.nuget ~/.config ~/.local "$GNUPGHOME" &&     apt-get purge -y make gnupg dirmngr &&     apt-get clean
# Thu, 16 Apr 2020 04:47:54 GMT
WORKDIR /root
# Thu, 16 Apr 2020 04:47:54 GMT
CMD ["fsharpi"]
# Thu, 16 Apr 2020 05:03:46 GMT
LABEL maintainer=Dave Curylo <dave@curylo.org>, Steve Desmond <steve@stevedesmond.ca>
# Thu, 16 Apr 2020 05:03:46 GMT
ENV FrameworkPathOverride=/usr/lib/mono/4.7.2-api/
# Thu, 16 Apr 2020 05:03:46 GMT
ENV NUGET_XMLDOC_MODE=skip DOTNET_RUNNING_IN_CONTAINER=true DOTNET_USE_POLLING_FILE_WATCHER=true
# Thu, 16 Apr 2020 05:03:57 GMT
RUN apt-get update &&     apt-get --no-install-recommends install -y     curl     libunwind8     gettext     apt-transport-https     libc6     libcurl4     libgcc1     libgssapi-krb5-2     libicu63     liblttng-ust0     libssl1.1     libstdc++6     libunwind8     libuuid1     zlib1g &&     rm -rf /var/lib/apt/lists/*
# Thu, 16 Apr 2020 05:04:20 GMT
RUN DOTNET_SDK_VERSION=3.1.102 &&     DOTNET_SDK_DOWNLOAD_URL=https://dotnetcli.blob.core.windows.net/dotnet/Sdk/$DOTNET_SDK_VERSION/dotnet-sdk-$DOTNET_SDK_VERSION-linux-x64.tar.gz &&     DOTNET_SDK_DOWNLOAD_SHA=9cacdc9700468a915e6fa51a3e5539b3519dd35b13e7f9d6c4dd0077e298baac0e50ad1880181df6781ef1dc64a232e9f78ad8e4494022987d12812c4ca15f29 &&     curl -SL $DOTNET_SDK_DOWNLOAD_URL --output dotnet.tar.gz &&     echo "$DOTNET_SDK_DOWNLOAD_SHA dotnet.tar.gz" | sha512sum -c - &&     mkdir -p /usr/share/dotnet &&     tar -zxf dotnet.tar.gz -C /usr/share/dotnet &&     rm dotnet.tar.gz &&     ln -s /usr/share/dotnet/dotnet /usr/bin/dotnet
# Thu, 16 Apr 2020 05:04:23 GMT
RUN mkdir warmup &&     cd warmup &&     dotnet new &&     cd - &&     rm -rf warmup /tmp/NuGetScratch
# Thu, 16 Apr 2020 05:04:24 GMT
WORKDIR /root
# Thu, 16 Apr 2020 05:04:24 GMT
CMD ["dotnet" "fsi"]
```

-	Layers:
	-	`sha256:123275d6e508d282237a22fefa5aef822b719a06496444ea89efa65da523fc4b`  
		Last Modified: Thu, 16 Apr 2020 03:31:44 GMT  
		Size: 27.1 MB (27098147 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f6025c7b2cd48a671e18960f1c43599827ca765d3957ebd1c26ddbfcfaf4b831`  
		Last Modified: Thu, 16 Apr 2020 05:06:15 GMT  
		Size: 159.5 MB (159520483 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8fb5b7d2547039f15892438861b7c2a551e4fabe963486bb7f759d44442418f0`  
		Last Modified: Thu, 16 Apr 2020 05:07:01 GMT  
		Size: 17.2 MB (17202198 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:249525f146ecdc124ca194ee5ce57c3e8af9023607bd5640032f7678dd65638f`  
		Last Modified: Thu, 16 Apr 2020 05:07:19 GMT  
		Size: 115.9 MB (115919109 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e6aacf4edd95c1964c6926cca05431ab7681b2bea7541972470ed5ee6ceab8eb`  
		Last Modified: Thu, 16 Apr 2020 05:06:58 GMT  
		Size: 3.9 MB (3941627 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
