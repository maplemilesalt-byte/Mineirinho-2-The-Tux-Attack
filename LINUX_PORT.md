# Linux Port

## Objetivo

Levar o Mineirinho Ultra Adventures 2 para Linux preservando o comportamento do jogo original.

A prioridade nesta etapa é **portar**, não melhorar a lógica do jogo.

## Situação atual

O código decompilado é código C# de um projeto Unity baseado em Mono.

Isso significa que a maior parte dos scripts não precisa de uma reescrita específica para Linux. O principal trabalho é recuperar/usar o projeto Unity, suas cenas, prefabs, materiais, texturas, áudio, configurações e demais assets e então gerar um build Linux.

## Ordem do port

1. Recuperar a estrutura do projeto Unity.
2. Identificar a versão exata do Unity usada pelo jogo.
3. Reunir os scripts C# decompilados.
4. Recuperar as cenas e referências dos componentes.
5. Corrigir apenas problemas necessários para o código compilar no projeto recuperado.
6. Configurar o target Linux x86_64.
7. Testar o jogo no Linux.
8. Comparar o comportamento com a versão original.
9. Só depois começar melhorias.

## Regras desta etapa

- Não alterar a lógica original sem necessidade.
- Não trocar nomes de classes, métodos ou tags sem necessidade.
- Não otimizar código ainda.
- Não adicionar funcionalidades novas ainda.
- Registrar separadamente qualquer alteração necessária para o Linux.

## Primeira barreira

Os scripts sozinhos não formam um projeto Unity completo. Para produzir um executável Linux fiel, ainda são necessários os assets e a estrutura do projeto.

Portanto, o próximo passo técnico é reconstruir/recuperar essa estrutura antes de tentar transformar os scripts em um executável.

## Fases futuras

### Port original

Código e comportamento equivalentes ao original, com apenas as alterações necessárias para o build Linux.

### Melhorias

Depois que o port original estiver funcionando, mudanças de qualidade, correções e melhorias serão feitas separadamente.
