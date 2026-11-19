# Diário de Ignição

Lê o PDF do **Relatório de percurso** do rastreador e mostra só o que interessa: quando cada veículo **ligou** e **desligou**, com data, hora, coordenada e endereço.

## Como usar

1. Abra o site (GitHub Pages deste repositório).
2. Clique em **Abrir PDF** ou arraste o arquivo para a página. Dá para selecionar **vários PDFs de uma vez** (um por carro, ou partes do mesmo carro).
3. Veja os usos (ligou → desligou) ou os eventos, filtre por dia e baixe a planilha (.csv).

- O PDF é lido **no próprio navegador**: o arquivo não é enviado para nenhum servidor.
- PDF com texto embutido é lido em segundos, mesmo com mais de 1000 páginas.
- PDF em imagem (escaneado/impresso) é lido por OCR, com dupla leitura de cada evento.
- Arquivo de frota (vários veículos no mesmo PDF) ou vários PDFs abertos juntos são separados por placa, com planilha da frota inteira. PDFs do mesmo carro são juntados em ordem de data e hora, sem contar registro repetido.
- **Viagens repetidas entre carros**: com dois ou mais carros abertos, lista os dias em que carros diferentes foram para a mesma cidade (a cidade onde desligaram), com horários, se estiveram lá ao mesmo tempo, mapa com os trajetos e planilha. A cidade-base da frota fica de fora, com opção de incluir.
- **Ver trajeto**: em cada uso, abre um mapa com o caminho feito do ponto A (ligou) ao ponto B (desligou), pelas posições do relatório, e um botão para abrir o trajeto no Google Maps.

## Arquivos

- `index.html`: a aplicação.
- `lib/`: leitor de PDF (pdf.js 3.11.174), OCR (tesseract.js 5.1.1, com dados de português e inglês) mapa (Leaflet 1.9.4, com fundo do OpenStreetMap) e lista de municípios do IBGE (`municipios.txt`, de github.com/kelvins/municipios-brasileiros, licença MIT).
