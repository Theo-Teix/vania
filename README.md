# Vânia Alonso, nutrição clínica e esportiva funcional

Página da nutricionista Vânia Alonso (@vania.nutri), com 22 anos de atendimento, on-line e presencial em São Paulo. É uma nova versão do site atual (vanianutri.com.br), com o mesmo conteúdo e design novo.

Versão 1 (16/11/2026), conceito "a flor que abre":
- a flor de cinco pétalas do logo dela, redesenhada em SVG (pétalas verdes e contorno laranja), atravessa a página: ela se desenha na abertura, gira na escolha das áreas, preenche as etapas do PNI e aparece inteira no final;
- "Por onde você quer começar?": ao tocar uma das cinco áreas (saúde da mulher, estética e emagrecimento, gestação e infância, controle de doenças, performance), a flor gira, o painel troca e os botões de agendar passam a levar aquele assunto no WhatsApp;
- seção própria para o Personal Diet em domicílio, o percurso do PNI, atendimento on-line, depoimentos do site atual, quem sou e o final.

HTML, CSS e JavaScript puros, sem build. Todos os botões de agendamento abrem o WhatsApp.

## Estrutura

```
index.html                  página completa (estilos, scripts e a flor dentro do arquivo)
img/vania-abertura.jpg      abertura (camisa listrada, parede de folhas; post do Instagram)
img/comida-legumes.jpg      faixa "Saúde não é só o que você coloca no prato" (post das receitas)
img/casa-cozinha.jpg        em casa: preparando legumes (capa de vídeo do Instagram)
img/casa-treino.jpg         em casa: treino com corda (capa de vídeo do Instagram)
img/vania-folhas.jpg        atendimento on-line
img/vania-cafe.jpg          quem sou
img/favicon.png             ícone da aba (flor)
img/apple-touch-icon.png    ícone ao salvar na tela do celular
vercel.json                 configuração da Vercel (URLs limpas)
```

Todas as fotos são da Vânia (Instagram e fotos enviadas). Nenhuma foi gerada por IA.

## Publicar

1. Crie um repositório no GitHub (ex.: `Vania_Alonso`) e envie os arquivos desta pasta para a raiz dele.
   Importante: **arraste a pasta `img` inteira** para a área de upload. O botão "choose your files" não envia pastas.
2. Na Vercel, clique em **Add New → Project**, importe o repositório e mantenha:
   - Project Name: `nutri-vaniaalonso`
   - Framework Preset: **Other**
   - Build Command: vazio
   - Output Directory: vazio (raiz)
3. Clique em **Deploy**. O site fica em https://nutri-vaniaalonso.vercel.app/ e cada novo commit publica a atualização sozinho.

Se usar outro nome de projeto, troque o endereço em `canonical`, `og:url` e `og:image` no `<head>` do `index.html`.

## Atualizar o site já publicado

Envie o `index.html` novo para o repositório. A pasta `img` só precisa subir de novo quando alguma imagem mudar. Ao trocar uma imagem mantendo o mesmo nome, aumente o `?v=1` nos links (por exemplo `?v=2`).

## Editar conteúdo

- WhatsApp: variável `numero` no fim do `index.html` (hoje 5511983819390) e o número exibido no rodapé e no passo 1 do on-line.
- Mensagem padrão: atributo `data-wa` de cada botão. A mensagem de cada área fica na lista `areas` do script.
- Áreas: os painéis `.pn` (textos) e a lista `areas` no script, na mesma ordem.
- Cores: variáveis no início do `<style>` (`--floresta`, `--musgo`, `--creme`, `--linho`, `--folha`, `--laranja`).

## A confirmar com a cliente

- Fotos em alta resolução das capas de vídeo (cozinha e treino) e da foto do café; as atuais ficam um pouco moles em telas de alta densidade.
- CRN (não está publicado no site nem no Instagram).
- Se vende consulta avulsa além do PNI.
- A flor do logo foi redesenhada em SVG a partir do logo atual; conferir e, se possível, receber o arquivo original.
- Endereço e horários: não estão publicados; a página mostra só "São Paulo · on-line, presencial".
- O site atual tem um segundo WhatsApp no menu de contato, (11) 99717-7493; a página usa o (11) 98381-9390.
- A nota "4,9" do site atual ficou de fora por não ter fonte; ela não tem perfil no Google Maps.
