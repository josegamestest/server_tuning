Este documento e uma vercao portugues descrevendo o funcionamento do mod<br>
Documentação por: José Anastácio (josegamestest)<br>
Site: https://www.josegamestest.com.br/<br>
Youtube: https://www.youtube.com/c/josegamestest<br>

# Server tuning #
Este mod cria uma experiência de administração mais interativa,<br>
permitindo aos administradores ajustar as configurações de servidor cruciais diretamente no jogo.<br>
Implementa um sistema de ajuste dinâmico de várias configurações de servidor no jogo Minetest, <br>
permitindo que os administradores otimizem o desempenho do servidor em tempo real. <br>
Cada configuração é associada a uma função específica e é ajustável através de um menu acessível no jogo. 

### Descrição detalhada de cada configuração e sua função no jogo: ###
### Configurações de Ajuste Dinâmico no Menu do Servidor: ###

    BSD (Max Block Send Distance):
        Controla a distância máxima que os blocos podem ser enviados a outros jogadores.
        Ajustável através do menu para otimizar a transmissão de dados entre jogadores.

    Sbspc (Max Simultaneous Block Sends Per Client):
        Define o número máximo de envios simultâneos de blocos que um cliente pode realizar.
        Ajustável para otimizar a carga de dados entre o servidor e os clientes.

    Bgd (Max Block Generate Distance):
        Limita a distância máxima a partir da qual blocos podem ser gerados.
        Ajustável para controlar a geração de novos blocos no mundo do jogo.

    Chunk (Chunksize):
        Especifica o tamanho dos "chunks" (pedaços) no jogo.
        Ajustável para otimizar o desempenho e a eficiência na manipulação de terreno.

    Active_br (Active Block Range):
        Define a distância a partir da qual blocos são considerados ativos e processados.
        Ajustável para otimizar o desempenho em termos de processamento de blocos no ambiente do jogador.

    Active_osrb (Active Object Send Range Blocks):
        Controla a distância de envio de objetos ativos (por exemplo, jogadores e mobs).
        Ajustável para otimizar a transmissão de dados de objetos ativos entre os jogadores.

    Item_entity_ttl (Item Entity Time To Live):
        Determina a quantidade total de tempo que as entidades de item permanecem no jogo.
        Ajustável para controlar a persistência de itens caídos no chão.

    Liquid_loop_max (Liquid Loop Maximum):
        Define o número máximo de iterações no loop de atualização de líquidos.
        Ajustável para otimizar a simulação e atualização de líquidos no jogo.

    Liquid_update (Liquid Update):
        Controla a taxa de atualização para simulação de líquidos.
        Ajustável para equilibrar a precisão da simulação com a carga no servidor.

Funções Associadas a Configurações:<br>
    recalculate_bsd() - Atualiza e aplica alterações na configuração BSD.<br>
    recalculate_sbspc() - Atualiza e aplica alterações na configuração Sbspc.<br>
    recalculate_bgd() - Atualiza e aplica alterações na configuração Bgd.<br>
    recalculate_chunk() - Atualiza e aplica alterações na configuração Chunk.<br>
    recalculate_br() - Atualiza e aplica alterações na configuração Active_br.<br>
    recalculate_osrb() - Atualiza e aplica alterações na configuração Active_osrb.<br>
    recalculate_ttl() - Atualiza e aplica alterações na configuração Item_entity_ttl.<br>
    recalculate_loop() - Atualiza e aplica alterações na configuração Liquid_loop_max.<br>
    recalculate_liquid() - Atualiza e aplica alterações na configuração Liquid_update.<br>

Interações com Jogadores:<br>
    minetest.register_on_joinplayer() - Registra uma função para ser chamada quando um jogador entra no jogo.<br>
    minetest.register_on_leaveplayer() - Registra uma função para ser chamada quando um jogador deixa o jogo.<br>
    minetest.register_on_player_receive_fields() - Registra uma função para processar campos recebidos de um formulário no jogo.<br>

Comandos de Chat:<br>
    /server - Comando de chat que exibe informações e abre o menu do servidor para jogadores com a permissão 'server'.

