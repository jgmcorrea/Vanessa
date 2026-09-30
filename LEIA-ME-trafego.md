# Site Vanessa Bollmann — instruções para publicação

Domínio: vanessabollmann.com.br

## 1. Estrutura dos arquivos

Tudo sobe na raiz do domínio, mantendo as pastas como estão:

```
index.html                        site principal (abre no endereço do domínio)
leitura-12-casas.html             landing da leitura das 12 casas (R$ 350)
diagnostico-empresa.html          landing do diagnóstico de empresa (R$ 350)
ebook-mulheres-em-travessia.html  landing do ebook (R$ 44)
ebook-o-retorno-para-si.html      landing do ebook (R$ 44)
termos.html                       termos, entrega e privacidade
img/                              fotos, capas e páginas internas dos ebooks
og/                               imagens de compartilhamento (WhatsApp, redes)
audio/                            áudio de apresentação da Vanessa
```

Os links entre as páginas são relativos. Se algum arquivo for para uma subpasta, os links quebram.

## 2. O que precisa ser feito antes de rodar anúncio

### 2.1 Pixel do Meta
Em todas as seis páginas existe o trecho do pixel com o texto `SEU_PIXEL_ID`.
Trocar pelo ID real do pixel. Aparece duas vezes por página (script e noscript).

Já estão programados três eventos, além do PageView:
- `Contact` — clique em qualquer botão de WhatsApp
- `InitiateCheckout` — clique em "Quero o ebook"
- `AbriuMandala` (custom) — abertura das mandalas gratuitas

### 2.2 Links de checkout da Eduzz
Os dois ebooks serão vendidos pela Eduzz. Hoje os botões ainda apontam para o WhatsApp.
Assim que os links de checkout existirem, substituir nos botões "Quero o ebook · R$ 44"
nas páginas index.html, ebook-mulheres-em-travessia.html e ebook-o-retorno-para-si.html.

### 2.3 Certificado e HTTPS
Confirmar que o site abre em https e que http redireciona para https.

## 3. Verificações depois de publicar

- [ ] index.html abre no endereço do domínio, sem /index.html
- [ ] As seis páginas abrem e as imagens aparecem (pasta img no lugar certo)
- [ ] O áudio da seção "A minha travessia" toca no celular
- [ ] As mandalas gratuitas abrem e mostram a mensagem (index, e as duas landings de ebook)
- [ ] A mandala das 12 casas gera a roda e o botão envia para o WhatsApp
- [ ] Botão flutuante de WhatsApp aparece em todas as páginas
- [ ] O carrossel "Folheie algumas páginas" arrasta no celular
- [ ] Link do rodapé para termos.html funciona em todas as páginas
- [ ] Mandar o link no WhatsApp e conferir se aparece a imagem de preview
- [ ] Testar em Android e iPhone

## 4. Observações técnicas

- Páginas são HTML estático, sem banco de dados e sem back-end
- As mandalas rodam no navegador e guardam uma tiragem por dia no localStorage
- O formulário de contato do site não envia e-mail: ele monta a mensagem e abre o WhatsApp
- Peso: index.html com 104 KB, demais páginas entre 30 e 50 KB, imagens somam cerca de 600 KB

## 5. Contato

Vanessa Bollmann
WhatsApp (47) 99118-8982
vanessabollmann1982@gmail.com
