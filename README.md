# VLibras Widget Integration

Este repositório fornece um widget de acessibilidade baseado no VLibras para tradução de texto em português para Libras (Língua Brasileira de Sinais), permitindo maior inclusão e acessibilidade digital.

## Demonstração
Confira o widget em ação: [VLibras Widget](https://data-ju.github.io/vLibras/vlibras-widget.html)

## Recursos
- **Tradução em tempo real**: Converte texto em português para Libras.
- **Compatível com diferentes plataformas**: Pode ser integrado em sites e aplicativos.
- **Personalizável**: Fácil de adaptar ao design do seu site ou aplicação.

## Como Usar
### 1. Adicionar o widget ao seu projeto
Inclua o seguinte código em seu arquivo HTML para integrar o VLibras:

```
html
<div vw class="enabled">
    <div vw-access-button class="active"></div>
    <div vw-plugin-wrapper>
        <div class="vw-plugin-top-wrapper"></div>
    </div>
</div>
<script src="https://vlibras.gov.br/app/vlibras-plugin.js"></script>
<script>
    new window.VLibras.Widget('https://vlibras.gov.br/app');
</script>
```

### 2. Personalização
Para personalizar o comportamento ou aparência do widget, siga as orientações abaixo:

## Posicionamento do botão de acessibilidade:
Utilize CSS para ajustar a posição do botão conforme necessário. Por exemplo:

```
[vw-access-button] {
    bottom: 20px;
    right: 20px;
    position: fixed;
}
```

## Idiomas:
Certifique-se de que o conteúdo do seu site esteja em português, pois o VLibras foi projetado para traduzir exclusivamente textos nesta língua.

## Elementos específicos:
 Caso queira focar a tradução em apenas uma parte da página, ajuste a lógica para carregar o widget somente nessas áreas.

### 3. Testar o Widget

Após integrar o código, teste o widget em seu ambiente de desenvolvimento.

Verifique o carregamento correto dos scripts do VLibras e teste a interação para garantir a funcionalidade.

## Requisitos
- Navegadores compatíveis com JavaScript (versões modernas do Chrome, Firefox, Edge, ou Safari).
- Conexão com a internet para carregar o script hospedado do VLibras.

## Exemplos de Uso
Veja a seguir um exemplo de como o VLibras pode ser integrado em um site de forma simples e funcional:

```
<!DOCTYPE html>
<html lang="pt-BR">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Exemplo VLibras</title>
</head>
<body>
    <h1>Bem-vindo ao nosso site!</h1>
    <p>Este site utiliza o VLibras para acessibilidade.</p>

    <!-- Integração do widget -->
    <div vw class="enabled">
        <div vw-access-button class="active"></div>
        <div vw-plugin-wrapper>
            <div class="vw-plugin-top-wrapper"></div>
        </div>
    </div>
    <script src="https://vlibras.gov.br/app/vlibras-plugin.js"></script>
    <script>
        new window.VLibras.Widget('https://vlibras.gov.br/app');
    </script>
</body>
</html>
```

## Integração com o Power BI
Para integrar esse recurso com o Power BI, você pode fazer seua própria versão do código ou utilizar a versão disponibilizada.

Realizei algumas tentativas de utilizar o widget diretamente no Power BI, porém, por restrições de acesso do próprio visual, não é possível. Portanto, minha solução foi a de utilizar um site externo já hospedado para configuração do visual.

Você deve utilizar o visual HTML Content e criar uma medida como o exemplo abaixo:

```
Libras_Player = "<!DOCTYPE html>
<html>
<head>
  <meta name='viewport' content='width=device-width, initial-scale=1.0'>
  <style>
    iframe {
      width: 100%;
      height: 500px;
      border: none;
    }
  </style>
</head>
<body>
  <!-- Embed VLibras Widget -->
  <iframe 
    src='https://data-ju.github.io/vLibras/vlibras-widget.html' 
    title='VLibras Widget'
  ></iframe>
</body>
</html>
"
```

Caso queira utilizar seu próprio site, altere a URL "https://data-ju.github.io/vLibras/vlibras-widget.html" para sua própria versão do Github Pages ou site hospedado que contenha o Widget.

**Lembre-se de trocar todas suas aspas duplas (") por aspas simples (') ou duas aspas duplas (""), para evitar problemas de interpretação no DAX do Power BI.

## Contribuindo
Contribuições são sempre bem-vindas! Caso tenha sugestões ou encontre problemas, sinta-se à vontade para abrir uma issue ou enviar um pull request.

## Licença
Este projeto utiliza o VLibras, respeitando os termos de uso. Verifique as diretrizes antes de implementar em ambientes comerciais.

## Contato
Se precisar de suporte ou tiver sugestões, entre em contato:

- Autor: Julia Azevedo

- Linkedin: https://www.linkedin.com/in/javlira/
