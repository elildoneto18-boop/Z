# O celular de Diogo — ARG de terror psicológico

Projeto estático em HTML, CSS e JavaScript, preparado para GitHub Pages. **O aparelho pertence a Diogo. Elildo é o contato investigado.**

## Executar
Abra `index.html` no navegador ou use um servidor estático local (por exemplo, Live Server no VS Code).

## Publicar no GitHub Pages
1. Crie um repositório e envie todos os arquivos e a pasta `assets/` para a raiz.
2. Abra **Settings → Pages**.
3. Selecione a branch principal e `/ (root)` e salve.
4. Aguarde o link de publicação.

## Onde editar
No `script.js`:
- `CONFIG.lockPattern`: sequência de pontos do padrão. O padrão em Z atual é `[0,1,2,4,6,7,8]` (grade numerada da esquerda para a direita e de cima para baixo, começando em zero).
- `CONFIG.archivePassword`: permanece `null` para deixar as conversas arquivadas inacessíveis. Quando escolher uma senha, substitua `null` por uma string. Isso é uma mecânica narrativa, não segurança real, pois o JavaScript fica visível ao jogador.
- `MESSAGES`: mensagens, datas e horários da conversa com Elildo.
- `CALLS`: histórico de chamadas perdidas e atendidas.

## Áudio secreto do discador
Ao digitar `67` no teclado da emergência, o jogo reproduz `assets/audio/emergency-67.mp3`. O arquivo de áudio enviado foi incluído diretamente no projeto. A reprodução depende do suporte do navegador ao formato Opus.

## Imagens
`assets/images/profile-elildo.jpg` é usada como foto de perfil do contato Elildo. `home-wallpaper.jpg` e `lockscreen-wallpaper.jpg` são os papéis de parede de referência. `chat-reference.jpg` e `calls-reference.jpg` ficam disponíveis para novas personalizações.

## Recursos
- Desbloqueio por padrão desenhado em formato de quadrado (canto superior esquerdo → superior direito → inferior direito → inferior esquerdo).
- Tela inicial inspirada em Android/Samsung.
- WhatsApp fictício com ícones redesenhados em CSS, abas e menu.
- Lista principal com apenas Elildo como conversa.
- Mensagens, separadores de datas, indicadores de leitura, chamadas e áudio com falha intencional.
- Histórico de ligações com detalhes de cada registro.
- Configurações simplificadas e área arquivada bloqueada enquanto a senha não for definida.
- Ligação de emergência simulada: discar 190 e tocar em ligar inicia falas em português com voz sintetizada pelo navegador; nenhuma chamada real é feita.
- Layout responsivo, navegação local e caminhos relativos.

## Limitações
Mensagens e chamadas são fictícias. O áudio não carrega nem reproduz gravação real. Não há chamadas reais, backend ou salvamento de progresso. O conteúdo das conversas arquivadas ainda deve ser criado quando a senha narrativa for definida.


## Ligação de emergência simulada
Na tela de desenho do padrão, toque em “Ligação de emergência”. No discador, digite `190` e toque no botão verde. O navegador tentará sintetizar a fala “Polícia, qual é o seu problema? Senhor? Olá?” usando `SpeechSynthesis`; o resultado depende das vozes disponíveis no dispositivo. Isso é apenas uma cena do ARG e não contata os serviços de emergência.
