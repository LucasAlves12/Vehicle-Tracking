# Vehicle-Tracking
Este repositório contém um projeto de detecção e rastreamento de veículos em uma rodovia, com a capacidade de diferenciar carros de motos. O código foi adaptado de um exemplo pronto para atender a essa necessidade específica.

## Descrição do Projeto
O objetivo deste projeto é detectar e rastrear veículos em um vídeo de uma rodovia, contando e diferenciando carros de motos. Para isso, utilizamos técnicas de processamento de imagem e visão computacional.

## Funcionalidades
- Detecção de Objetos: Utilizamos um detector de objetos para identificar veículos no vídeo.
- Rastreamento de Objetos: Implementamos um rastreador para acompanhar os veículos detectados ao longo dos frames do vídeo.
- Classificação de Veículos: Diferenciamos carros de motos com base nas dimensões (altura e largura) dos objetos detectados.
- Estabilização de Vídeo: Aplicamos técnicas de estabilização para reduzir os efeitos de movimentos da câmera.

![tracking](https://github.com/user-attachments/assets/b05af617-91f0-4c64-b0d4-ab218c67f0e3)

# Método Utilizado
## Detecção de Objetos
A detecção de objetos é realizada utilizando um detector de fundo (BackgroundSubtractor). A região de interesse (ROI) é extraída do frame e processada para obter uma máscara binária que destaca os veículos.

## Rastreamento de Objetos
Utilizamos um rastreador para acompanhar os veículos detectados ao longo dos frames. O rastreador atualiza as posições dos veículos e mantém um ID único para cada um.

## Classificação de Veículos
Para diferenciar carros de motos, utilizamos as dimensões dos objetos detectados:

- Motos: Objetos com área menor que um determinado limiar.
- Carros: Objetos com área maior que o limiar.

## Estabilização de Vídeo
Para lidar com movimentos da câmera, aplicamos técnicas de estabilização de vídeo utilizando fluxo óptico. Isso ajuda a reduzir os efeitos de tremores e movimentos bruscos da câmera.

# Problemas Encontrados
Apesar das melhorias implementadas, o código ainda enfrenta alguns desafios:

- Perda de Efetividade com Movimentos da Câmera: Quando a câmera se move, a detecção de objetos perde precisão, resultando em falhas no rastreamento.
- Classificação Imperfeita: A classificação de veículos com base nas dimensões pode não ser precisa em todos os casos, especialmente quando os veículos estão em diferentes ângulos ou distâncias da câmera.

Sugestões e apontamentos para melhorias são muito bem-vindas 

### Créditos
A base de códigos e arquivos utilizados nesse projeto, foram tiradas do canal no Youtube chamado: "Pysource". O vídeo em questão apresenta um modelo de código de "Objetct Tracking" onde o autor utiliza a biblioteca OpenCV do python para desenvolver o aplicativo. Esse repositório contem uma versão adaptada do vídeo, baseada em necessidades e aplicações específicas.

Segue o link para o vídeo:

<https://www.youtube.com/watch?v=O3b8lVF93jU&list=WL&index=5>
