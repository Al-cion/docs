---
$title: Validar o HTML para AMP 
---

Sempre que você criar uma página AMP, será preciso confirmar que o HTML para AMP está correto. Há [vários métodos possíveis para validar suas páginas AMP](/pt_br/docs/fundamentals/validate.html).  Neste tutorial, ativaremos o validador de AMP usando o modo de desenvolvedor.  Para isso, adicione o seguinte identificador de fragmentos ao seu URL e atualize a página:

```text
#development=1
```

Exemplo:

```text
http://localhost:8000/pets.html#development=1 
```

Abra o [DevTools Console](https://developer.chrome.com/devtools/docs/console) no Chrome (ou no navegador que você preferir) e verifique se há erros de AMP. Talvez seja preciso atualizar o navegador para ver as mensagens de validação. Se a página não tiver erros, esta mensagem será exibida:

```text
AMP validation successful.
```

<div class="prev-next-buttons">
  <a class="button prev-button" href="/pt_br/docs/design/getting_started/create_bookend.html"><span class="arrow-prev">Anterior</span></a>
  <a class="button next-button" href="/pt_br/docs/design/getting_started/congratulations.html"><span class="arrow-next">Próxima</span></a>
</div>
 
