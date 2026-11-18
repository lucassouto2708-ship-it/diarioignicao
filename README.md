# Diário de Ignição

Lê o PDF do **Relatório de percurso** do rastreador e mostra só o que interessa: quando cada veículo **ligou** e **desligou**, com data, hora, coordenada e endereço.

## Como usar

1. Abra o site (GitHub Pages deste repositório).
2. Clique em **Abrir PDF** ou arraste o arquivo para a página.
3. Veja os usos (ligou → desligou) ou os eventos, filtre por dia e baixe a planilha (.csv).

- O PDF é lido **no próprio navegador**: o arquivo não é enviado para nenhum servidor.
- PDF com texto embutido é lido em segundos, mesmo com mais de 1000 páginas.
- PDF em imagem (escaneado/impresso) é lido por OCR, com dupla leitura de cada evento.
- Arquivo de frota (vários veículos no mesmo PDF) é separado por placa, com planilha da frota inteira.

## Arquivos

- `index.html`: a aplicação.
- `lib/`: leitor de PDF (pdf.js 3.11.174) e OCR (tesseract.js 5.1.1, com dados de português e inglês).
