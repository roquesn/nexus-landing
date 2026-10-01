# Nexus Proteção Veicular — landing page

Página única da Nexus: apresenta a empresa, chama o cliente para cotar pelo WhatsApp e convida novos consultores.

## Arquivos

- `index.html` — a página inteira (HTML, CSS e JavaScript no mesmo arquivo).
- `assets/favicon.svg` — ícone da aba do navegador.
- `assets/nexus-simbolo.svg` — símbolo do logo (quadrado azul com o N).
- `assets/nexus-logo-claro.svg` / `nexus-logo-escuro.svg` — logo completo para fundo claro e fundo escuro.

Para ver a página, abra o `index.html` no navegador.

## Fotos

As fotos da página são de banco de imagens gratuito (Unsplash, licença de uso livre, inclusive comercial) e são carregadas direto do Unsplash, por link. Servem de marcação até a Nexus ter fotos próprias.

| Onde aparece | Foto | Autor no Unsplash |
| --- | --- | --- |
| Topo, "Carros" | `photo-1651446404130-104e68e2f39a` | Russian Supreme |
| Topo, "Motos" | `photo-1683183191390-c6e1a70ea99e` | LouisMoto |
| Topo, "Caminhões" | `photo-1790364757239-2bd1ab3b5f31` | Arlind Photography |
| Como a Nexus trabalha | `photo-1756142007128-f431ede241cc` | Samsung Memory US |
| Seja consultor | `photo-1758521961483-30f5908b9c93` | Vitaly Gariev |
| Fechamento | `photo-1760068670115-6d4e415b0c7a` | Leonardo Iribe |

Para trocar por uma foto própria: salve o arquivo em `assets/img/` e, na tag `<img>` correspondente, troque o `src` pelo caminho do arquivo (por exemplo `assets/img/clientes.jpg`) e apague os atributos `srcset` e `sizes`.

## Depoimentos

As seções "Depoimentos de clientes" e "Depoimentos de colaboradores" estão com cartões de modelo, marcados com a etiqueta "Exemplo". Para publicar um depoimento real, em cada cartão (`<li class="depo">`):

1. Troque o texto do `<p class="depo-text">` pelo relato da pessoa.
2. Troque o nome e a linha de baixo (veículo e cidade, ou função e cidade).
3. Apague a linha `<span class="tag">Exemplo</span>`.
4. Se tiver foto, troque o `<span class="avatar">…</span>` por `<img class="avatar" src="assets/img/nome.jpg" alt="">`.

Quando todos os cartões forem reais, apague também o aviso "Estes cartões são modelos…" de cada seção. Publique só depoimentos de pessoas reais e com autorização delas.

## O que editar com mais frequência

| O quê | Onde, no `index.html` |
| --- | --- |
| Número do WhatsApp | Procure por `5534993008884` (links) e `99300-8884` (texto) e substitua todos |
| Nomes das parceiras | Seção `<!-- PARCEIRAS -->`, texto do hero e seção `<!-- CONSULTOR -->` |
| Coberturas | Seção `<!-- COBERTURAS -->` |
| Depoimentos | Seções `<!-- DEPOIMENTOS DE CLIENTES -->` e `<!-- CONSULTOR + DEPOIMENTOS DE COLABORADORES -->` |
| Perguntas frequentes | Seção `<!-- DÚVIDAS -->` |
| Cores | Bloco `:root` no início do `<style>` (tema claro) e os dois blocos de tema escuro logo abaixo |

## Publicar de graça no GitHub Pages

1. Crie o repositório e envie os arquivos (no PowerShell, dentro desta pasta):

   ```powershell
   git init -b main
   git add .
   git commit -m "Landing page da Nexus"
   git remote add origin https://github.com/SEU-USUARIO/nexus-landing.git
   git push -u origin main
   ```

   Antes do `git remote add`, crie um repositório vazio e público chamado `nexus-landing` em github.com/new.

2. No GitHub, abra o repositório e vá em **Settings → Pages**. Em **Source** escolha **Deploy from a branch**, selecione **main** e **/(root)** e salve.

3. Em um ou dois minutos o site fica em `https://SEU-USUARIO.github.io/nexus-landing/`.

A cada `git push` o site é atualizado sozinho.

## Observações

- A pasta `Imagens/` (referências de design) está no `.gitignore` e não vai para o repositório.
- As fontes vêm do Google Fonts e as fotos do Unsplash, então a página precisa de internet para aparecer completa.
