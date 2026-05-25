# XNB Editor — by Nox Games

**Editor visual de arquivos `.xnb` direto no navegador, sem instalação, 100% gratuito.**

---

## O que é o XNB Editor?

O XNB Editor é uma ferramenta web desenvolvida pela **Nox Games** para abrir, visualizar, editar e reempacotar arquivos no formato `.xnb` — o formato de assets usado por jogos feitos com **XNA Framework** e **MonoGame** (como Stardew Valley, por exemplo).

Tudo funciona diretamente no navegador: nenhum dado é enviado a servidores. O processamento é 100% local.

---

## Funcionalidades

### 📂 Carregamento de Arquivos
- Arraste e solte um ou mais arquivos `.xnb` diretamente na interface.
- Ou clique em **"Selecionar Arquivos"** para abrir o explorador de arquivos.
- Suporte a múltiplos arquivos ao mesmo tempo.
- Cada arquivo carregado aparece como um card expansível com informações detalhadas.

---

### 🖼 Texturas (Texture2D)
Para arquivos `.xnb` que contêm imagens/texturas:

- **Visualização em tempo real** da textura com fundo xadrez (para transparência).
- Exibe informações técnicas: largura, altura, formato de pixel, quantidade de mipmaps.
- **Substituir Imagem** — importe qualquer imagem (PNG, JPG etc.) para substituir a textura original. A imagem é automaticamente redimensionada para caber nas dimensões originais.
- **Exportar como PNG** — salva a textura atual como um arquivo `.png` no seu computador.
- Conversão automática de BGRA (formato XNA) para RGBA (formato web) e vice-versa.

---

### 📄 XML (XElement)
Para arquivos `.xnb` que contêm dados XML:

- **Editor de texto completo** com área de edição redimensionável.
- Exibe o XML original formatado e editável diretamente no navegador.
- **Validação de XML** em tempo real: erros de sintaxe são detectados antes de salvar.
- **Salvar Alterações** — reempacota o XML editado de volta ao formato `.xnb` com tamanho corrigido automaticamente.
- **Resetar** — desfaz todas as edições e volta ao conteúdo original.
- **Exportar como .xml** — salva o conteúdo como arquivo `.xml` separado.
- Informações técnicas: TypeID, Reader Type, número de linhas e tamanho em bytes.

---

### 📝 Strings (StringReader)
Para arquivos `.xnb` que contêm texto puro:

- Editor de texto para visualizar e modificar o conteúdo da string.
- **Salvar Alterações** — reempacota o texto editado de volta ao `.xnb`.
- **Resetar** — volta ao texto original.
- **Exportar como .txt** — salva o conteúdo como arquivo de texto.
- Exibe número de linhas e tamanho do arquivo.

---

### ❓ Tipos Desconhecidos (Raw Binary)
Para arquivos `.xnb` com tipos não reconhecidos nativamente:

- Exibe informações técnicas completas: plataforma, versão, flags, tamanho total, tamanho do header, tamanho do payload e lista de todos os readers presentes no arquivo.
- Mostra os primeiros 48 bytes do payload em hexadecimal para diagnóstico.
- **Extrair Payload (.bin)** — exporta o conteúdo binário bruto (sem o cabeçalho XNB) para edição externa com hex editor ou outras ferramentas.
- **Importar Payload (.bin)** — reimporta um `.bin` editado externamente e reempacota com o cabeçalho original e tamanho corrigido.
- **Baixar XNB Original** — baixa o arquivo sem modificações.

---

### ⬇ Download em Massa
- Após editar um ou mais arquivos, uma **barra de download** aparece automaticamente.
- **Baixar Todos** — faz o download de todos os arquivos carregados (modificados ou não) de uma vez.
- **Limpar** — remove todos os arquivos da sessão e reseta a interface.
- Indicador visual de quantos arquivos foram modificados.

---

## Interface e Design

- Tema escuro com visual cyberpunk/tech em tons de azul neon.
- Animação de partículas flutuantes no cabeçalho.
- Cards expansíveis por arquivo com badge de status (Texture2D, XElement, String, Modificado).
- Notificações em toast (mensagens de confirmação ou erro no canto da tela).
- Totalmente responsivo — funciona em desktop e mobile.
- Fonte **JetBrains Mono** para o código e **Syne** para os títulos.

---

## Limitações

- Arquivos `.xnb` **comprimidos (LZX)** não são suportados. É necessário descompactar antes de usar o editor.
- A substituição de texturas mantém as dimensões originais (largura × altura) do arquivo.
- Desenvolvido para XNA 4.0 / MonoGame (versão 5 do formato XNB).

---

## Tecnologias Utilizadas

- HTML5, CSS3 e JavaScript puro (sem frameworks ou dependências externas).
- Canvas API para renderização de texturas.
- FileReader API e ArrayBuffer para leitura e escrita de binários.
- DOMParser para validação de XML.
- Processamento 100% no lado do cliente (client-side).

---

## Licença

MIT License — Copyright (c) 2026 Nox Games  
Livre para usar, modificar e distribuir com atribuição.
