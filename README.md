Repositório baseado no exemplo de [/wrigleyster/arch-pkgs](https://github.com/wrigleyster/arch-pkgs).

[![Na medida do permitido por lei, Alexandre Magno renunciou a todos os direitos de autor e direitos conexos (ou próximos) sobre o conjunto de projetos de empacotamento "/alexandre-mbm/arch-pkgs". Este trabalho é publicado a partir de: Brasil.](http://i.creativecommons.org/p/mark/1.0/88x31.png)](http://creativecommons.org/publicdomain/zero/1.0/deed.pt_BR)

Para contribuir com este repositório, faça _fork_ e [_pull requests_](../../pulls).

Para contribuir em algum dos pacotes, clone o repositório do AUR 4 (submodule deste repositório), trabalhe em novo _branch_, e ao final prepare um [**patch**](https://ariejan.net/2009/10/26/how-to-create-and-apply-a-patch-with-git/), anexando o arquivo em [_issue_](../../issues).

Instruções para instalação de pacotes podem ser encontradas no [wiki](../../wiki).

# aliases

É uma ferramenta que facilita geração e teste de pacotes definidos neste repositório. [Licença MIT](http://pt.wikipedia.org/wiki/Licen%C3%A7a_MIT).

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
A propósito, quando se tem um Makefile, como é o caso em nosso pacote inkblot, o desenvolvedor empacotador, após compilar com sucesso, deverá procurar os _makedepends_ para incluir no PKGBUILD, assim:
```console
$ cd nomedopacote/
$ pkgfindflags				# lista candidatos a makedepends
```
Já esta outra popular consulta é provida por pacote de mesmo nome, "pkgfile":
```console
$ pkgfile NOMEDEARQUIVO		# lista pacotes contendo o arquivo
```
Isso é tudo que vocẽ precisa saber para gerenciar as definições de empacotamento versionadas nos subdiretórios deste respositório.

# subaur4

É uma ferramenta que converte um diretório de pacote em _submodule_ Git com repositório em formato adequado para emprego no AUR 4. Um script sob [Licença MIT](http://pt.wikipedia.org/wiki/Licen%C3%A7a_MIT).

Com um `git status` limpo, e sabendo que o diretório ainda não é _submodule_, faça:

```console
$ bash subaur4 NOMEDEPACOTE/    # isso faz commit dentro e fora do submodule, exibindo relatório
```

