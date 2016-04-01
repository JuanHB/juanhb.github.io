---
layout: post
title:  "Usando UI-Router com multiplas views"
date:   2016-03-11 19:13:57 -0300
#categories: AngularJS UI-Router  
tags: [AngularJS, UI-Router]
---

Como montar rotas em um projeto grande e que possui mais de um página? Como ter várias áreas de conteudo dinamico em um mesmo arquivo?

{% highlight yaml %}
tl:dr; - UI Router é bom, use em todos os projetos, aqui está como fazer,
         pule direto para ...
{% endhighlight %}

tl:dr;? ---->>> [nem li, nem lerei][nl-nl]{:target="_blank"} ou [too long, didn't read][tl-dr]{:target="_blank"}

Para montar uma estrutura de layouts modulares e com conteudo dinamico usando apenas o sistema nativo de rotas do AngularJS é dificil, porque originalmente o AngularJS é feito para o desenvolvimento de SPAs (Single Page Application), onde tudo ocorre em uma mesma página e sem alteração da url conforme o usuário vai navegando na aplicação.

É aí que entra o [UI Router][ui-router-repo]{:target="_blank"}, um módulo open source, criado e mantido gratuitamente por uma crescente comunidade de desenvolvedores.

Entre as muitas utilidades do UI Router, está a de permitir o uso de multiplas áreas de conteudo dinamico (view) em um mesmo arquivo de layout, com isso, é possivel combinar mudança da URL com mudança de conteudo para mais de uma view no mesmo arquivo, baseado na mudança de state.

Para entender:

- `state`: State (estado) é a rota ou url em que o usuário se encontra;
- `view`: Diretiva que carrega conteudo dinâmico configurado no `state`;
- `layout`: Arquivo com áreas de conteudo dinamico, o esqueleto da aplicação.

Assim, quando o usuário navega na aplicação podemos dizer que ele está navegando entre os diversos estados de html que foi configurado em cada rota.

## Instalando o UI-Router

Pode ser pelo Bower `bower install ui-router` ou por download direto no [repo][ui-router-repo].
Claro, existem outras formas de instalar, use a que você achar mais fácil.

## Preparando o projeto

Um bom guia de estilo para AngularJS é o [desenvolvido pelo John Papa][john-papa-a1], Google Expert Developer que trabalha com AngularJS desde o começo, o guia é mais do que testado e é muito maduro, [ele também é traduzido para o português][john-papa-a1-ptbr], o que deixa tudo mais fácil.

Eu criei um [projeto básico usando o Angular Material e o AngularJS][juanhb-multi-view-ui-router], ele segue uma estrutura sólida e de fácil compreensão, e pode ser usado como modelo para aplicações grandes e pequenas, mas nesse guia vamos nos focar na configuração dos estados e views. 




[nl-nl]: /images/posts/2016-03-11/nlnl.jpg
[tl-dr]: /images/posts/2016-03-11/tldr.gif
[ui-router-repo]: https://github.com/angular-ui/ui-router
[john-papa-a1]: https://github.com/johnpapa/angular-styleguide/tree/master/a1
[john-papa-a1-ptbr]: https://github.com/johnpapa/angular-styleguide/blob/master/a1/i18n/pt-BR.md
[juanhb-multi-view-ui-router]: https://github.com/JuanHB/multi-view-ui-router
