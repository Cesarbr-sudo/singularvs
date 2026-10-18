*[Read in English](CONTRIBUTORS.md)*

# Contribuidores

## Como este projeto foi feito

**Singularvs** e um experimento de desenvolvimento humano-IA. A ideia, a direcao criativa, as decisoes de design, os testes e a validacao final foram conduzidos por um ser humano. Grande parte do codigo foi escrita em colaboracao com um modelo de linguagem. E um exemplo de **vibecoding**: programar guiado por intuicao, curiosidade e conversa, em vez de especificacao formal.


## Autor e direcao criativa

**Cesar** -- Concepcao, direcao de design, arquitetura de ideias, testes, feedback iterativo e validacao.

Responsavel por:

- A visao do projeto: um demake 2D do SpaceEngine com metodologia procedural estilo Elite (1984).

- Todas as decisoes de escopo, prioridades e o que cortar.

- Descricao dos bugs, comportamento esperado e sugestoes de melhoria em cada ciclo.

- Testes manuais em navegador e verificacao de cada patch.

- Curadoria de fontes cientificas e de referencias externas.

- A escolha da licenca MIT e a decisao de publicar em dominio aberto.


## Desenvolvimento em colaboracao com IA

### DeepSeek

Modelo de linguagem da DeepSeek que **escreveu a maior parte do codigo-fonte** deste projeto em colaboracao direta com o autor.

- Geracao do codigo a partir de descricoes em linguagem natural.

- Proposicao de algoritmos (geracao procedural de galaxias, sistemas estelares, planetas, tectonica, biologia).

- Refatoracoes, correcao de bugs e implementacao de patches incrementais.

- Sugestoes de arquitetura e organizacao do codigo.

- Revisao do proprio codigo em ciclos subsequentes.

De acordo com os Termos de Uso da DeepSeek (Secao 4.2), todos os direitos sobre os *Outputs* (o codigo gerado) sao atribuidos ao usuario, e o uso para desenvolvimento de produtos derivados e explicitamente permitido.


### Refinamento iterativo (v1.2)

Entre v1.1 e v1.2, dez patches incrementais foram aplicados em sessao separada de desenvolvimento:

- Correcao do parsing de semente hex + reset completo de estado em `setSeedFromText`.
- Threshold de tidal locking recalibrado (0.45 -> 0.20) para manter Mercurio/Venus destravados em estrelas tipo Sol.
- Selecao robusta de gamepad por score (prefere `mapping='standard'`), tolerante a reconexao de teclado 2.4G.
- Scheduler de musica ignora AudioContext suspenso (silencia warnings de autoplay).
- Espirais barradas forcadas a 2 bracos; pitch e largura da barra sincronizados entre arte e densidade.
- Gasosos redimensionados de 2-5 para 12-27 raios terrestres (faixa Netuno a Jupiter).
- Raio de exploracao escalado para 2.5x o raio da galaxia (A1) para proporcoes coerentes entre mapa e mundo.
- Sistemas multiplos agora usam **arvore binaria** (A-B, C-D orbita AB, etc.) em vez de cadeia linear.
- Atribuicao de orbita P-type usa threshold de separacao interna (correcao de regressao).
- `orbitTarget` default para todos os planetas (orfaos = 0), threshold de ICEGIANT relaxado.

Estes refinamentos foram realizados sob direcao e validacao do autor, com assistencia de IA para geracao de codigo e diagnostico de bugs.

## Referencias e inspiracoes

Projetos e obras que influenciaram conceitualmente o Singularvs, sem contribuicao de codigo ou assets:

- **SpaceEngine** (Vladimir Romanyuk / CosmoGraphic) -- inspiracao conceitual e estetica.

- **Elite** (David Braben e Ian Bell, 1984) -- inspiracao na filosofia procedural.

- **Kurzgesagt - In a Nutshell** -- referencias cientificas conceituais.


## Nota sobre geracao de codigo por IA

Este projeto e transparente quanto ao uso de IA. Parte substancial do codigo foi gerada por modelos de linguagem sob supervisao, direcao e teste humanos. A licenca MIT e concedida pelo autor humano do projeto, que tem o direito de faze-lo conforme os termos das ferramentas utilizadas.

