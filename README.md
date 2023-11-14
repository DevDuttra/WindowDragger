# WindowDragger

## Visão Geral
O **WindowDragger** é um trecho de código em C# projetado para habilitar a funcionalidade personalizada de arrastar janelas com um efeito estendido de vidro Aero no Windows. Este código permite criar um formulário do Windows com uma barra de título personalizada (neste caso, um painel chamado **PanelMove**) que os usuários podem arrastar para reposicionar o formulário.

## Recursos
**Arrastar com Barra de Título Personalizada**: O código fornece a capacidade de mover a janela clicando e arrastando um painel designado (**PanelMove**), simulando o comportamento de arrastar uma barra de título de janela nativa.

**Efeito de Vidro Aero:** Quando a composição do Gerenciador de Janelas de Desktop (DWM) está ativada (tema Aero), o código estende o efeito de vidro Aero para a área do cliente do formulário, proporcionando uma aparência visualmente atraente.

**Bordas Redondas e Sombra:** O código utiliza a função **CreateRoundRectRgn** para criar uma região de forma oval (bordas redondas) para o formulário. Além disso, quando o Aero está desativado, uma sombra é adicionada ao formulário para um efeito visual mais agradável.

## Uso
Para usar o **WindowDragger** em seu projeto C#:

Copie o código fornecido para a parte relevante do seu projeto.
Certifique-se de que o painel que você deseja usar como barra de título tenha o nome PanelMove.
O código lidará automaticamente com o arrasto da janela quando o usuário interagir com o painel designado.
Requisitos
Sistema Operacional Windows: O código depende das funções da API DWM e é projetado para sistemas operacionais Windows (Vista e posterior) que suportam os efeitos de vidro Aero.

## Explicação do Código
O código usa P/Invoke para chamar funções da API DWM para efeitos de vidro Aero.
A propriedade **CreateParams** é substituída para habilitar um efeito de sombra se o Aero não estiver ativado.
O método **WndProc** é substituído para lidar com a personalização do desenho quando o Aero está ativado.
Os métodos **PanelMove_MouseDown**, PanelMove_MouseMove e PanelMove_MouseUp implementam a funcionalidade de arrastar.

## Licença
Este código é fornecido sob a *Licença MIT*, permitindo flexibilidade para usar e modificar o código em seus projetos.

## Notas
Certifique-se de que o framework de destino do projeto suporta as funcionalidades usadas no código.
Teste a aplicação em uma máquina com suporte ao tema Aero para efeitos visuais ideais.
Sinta-se à vontade para personalizar o código conforme suas necessidades específicas, e contribuições são bem-vindas!
