Repositório baseado no exemplo de [/wrigleyster/arch-pkgs](https://github.com/wrigleyster/arch-pkgs).

[![Na medida do permitido por lei, Alexandre Magno renunciou a todos os direitos de autor e direitos conexos (ou próximos) sobre o conjunto de projetos de empacotamento "/alexandre-mbm/arch-pkgs". Este trabalho é publicado a partir de: Brasil.](http://i.creativecommons.org/p/mark/1.0/88x31.png)](http://creativecommons.org/publicdomain/zero/1.0/deed.pt_BR)

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