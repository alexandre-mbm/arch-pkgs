Repositório baseado no exemplo de [/wrigleyster/arch-pkgs](https://github.com/wrigleyster/arch-pkgs).

[![Na medida do permitido por lei, Alexandre Magno renunciou a todos os direitos de autor e direitos conexos (ou próximos) sobre o conjunto de projetos de empacotamento "/alexandre-mbm/arch-pkgs". Este trabalho é publicado a partir de: Brasil.](http://i.creativecommons.org/p/mark/1.0/88x31.png)](http://creativecommons.org/publicdomain/zero/1.0/deed.pt_BR)

# aliases

É uma ferramenta que facilita geração e teste de pacotes definidos neste repositório. Um script sob [Licença MIT](http://pt.wikipedia.org/wiki/Licen%C3%A7a_MIT). Se você for usá-lo, não precisa ler as demais seções deste documento, só esta.

Ative a ferramenta para o pacote de trabalho atual:
```console
$ DIRNAME=nomedopacote/; source aliases
```
Ela habilita os seguintes comandos:
```console
$ pkgnow		# informações de pacote atual
$ pkgmake		# constrói pacote atual
$ pkginstall   	# instala pacote atual
$ pkgtest     	# constrói e instala pacote atual
$ pkgremove   	# remove pacote atual, caso esteja instalado
$ pkgsource		# empacota fontes do pacote atual
$ pkgaur        # atualiza banco de dados e tenta instalar pacote atual a partir do AUR, com o yaourt
```

Inclusive uma consulta auxiliar:
```console
$ pkgmkdep NOMEDEPACOTE		# informa se é necessário declarar esse pacote em makedepends de PKGBUILD de pacote atual
```
Já esta outra popular consulta é provida por pacote de mesmo nome, "pkgfile":
```console
$ pkgfile NOMEDEARQUIVO		# lista pacotes contendo o arquivo
```
Isso é tudo que vocẽ precisa saber para gerenciar as definições de empacotamento versionadas nos subdiretórios deste respositório.

# Gerar para instalar

```console
$ cd nomedopacote/
$ makepkg
```
Para instalar a partir do arquivo:
```console
$ sudo pacman -U nomedopacote-versão-release-plataforma.pkg.tar.xz
```

# Gerar para AUR
```console
$ cd nomedopacote/
$ makepkg --source
```
Resultado para upload: `nomedopacote-versão-release-plataforma.src.tar.gz`

# Buscar
```console
$ sudo pacman -Ss chuteparanomedopacote
$ sudo yaourt -Ss chuteparanomedopacote
```

# Instalar
```console
$ sudo yaourt -S nomedopacote
```

# Remover
```console
$ sudo pacman -R nomedopacote
```

# Informações sobre pacote
```console
$ sudo pacman -Qi nomedopacote
```