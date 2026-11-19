## API

| Método | URL | O que recebe | Resposta |
|---|---|---|---|
| GET | /api/cartas | Tipo opcional | 200 - Lista de cartas |
| GET | /api/cartas/aleatoria | Nada | 200 - Carta aleatória |
| POST | /api/cartas | name, type, attack | 201 - Carta criada; 400 - Dados inválidos |


### Pergunta 3

Quando acrescentas uma carta, o Network tab mostra dois pedidos para `/api/cartas`. Qual é o primeiro, quem o manda e porque é que, antes do pacote CORS, o `console.log` da rota POST nunca aparecia no terminal?

O primeiro pedido é o OPTIONS, enviado automaticamente pelo browser antes do POST. Serve para verificar se o servidor permite este tipo de comunicação. Antes de instalar o CORS, o servidor não respondia corretamente a essa verificação. Por isso, o POST não chegava a ser executado e o console.log da rota não aparecia no terminal.

### Pergunta 4

Nas três versões da aula (só setCards, POST sem ficheiro, POST com cartas.json), onde vivia a carta nova e o que a apagava?

Na primeira versão, a carta ficava apenas no estado do React e desaparecia ao atualizar a página. Na segunda versão, ficava no array do servidor e desaparecia quando o servidor era reiniciado. Na terceira versão, ficava guardada no ficheiro cartas.json e continuava disponível mesmo depois de reiniciar o servidor.

## Autor

Gabriel Sousa

Curso: Técnico de Gestão e Programação de Sistemas Informáticos
