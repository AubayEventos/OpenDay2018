# OpenDay2018

## Informações

Deverá ser feita uma aplicação de consola que nos permita fazer a gestão das salas. 
Esta deverá ter um menu que permita ao utilizador operar nela.

![appConsole](https://github.com/AubayEventos/OpenDay2018/images/menuprincipal.png)

## Tipos de Dados 
###### Sala de Entrevista: Representa uma sala onde são feitas entrevistas

| Campo           | Tipo               | Descrição |
| :-------------- | :----------------- | :---------- |
| Id              | Texto              | Identificador da Sala |
| Nome            | Texto              | Nome da Sala |
| Marcação        | Lista de Marcações | Uma lista que contém todas as marcações desta sala |
| Disponibilidade | Hash Table         | Uma hash table de key/value que contém como key os dias da semana e como value as horas para esse dia |
| Quadro-Branco   | Boolean            | Indica se aquela sala tem um quadro-branco |

###### Sala de Reuniões: Representa uma sala onde são feitas reuniões.

| Campo     | Tipo     | Descrição |
| :-------- | :--------- | :---------- |
| Id   | Texto       | Identificador da Sala |
| Nome  |  Texto      | Nome da Sala |
| Marcação | Lista de Marcações | Uma lista que contém todas as marcações desta sala |
| Disponibilidade | Hash Table | Uma hash table de key/value que contém como key os dias da semana e como value as horas para esse dia |
| Videoconferência | Boolean | Indica se aquela sala tem suporte para videoconferência |
| NOcupantes | Número | Indica quantos ocupantes é que aquela sala suporta |

###### Marcação: Representa uma marcação de uma determinada sala.

| Campo | Tipo | Descrição |
| :-------- | :--------| :--------|
| Id | Texto | Identificador da Marcação |
| IdSala | Texto | Identificador da Sala a marcar |
| NomeResponsável | Texto | Nome da pessoa responsável pela marcação |
| DataInício | Data | Data e Hora do início da marcação |
| DataFim | Data | Data e Hora de fim da marcação |
| NomeOcupantes | Lista de Texto | Nome de todos os ocupantes desta marcação

###### Disponibilidade: Representa a disponibilidade de uma sala ao longo da semana
 
| Campo | Tipo | Descrição |
| :-------- | :--------| :--------|
| DiaSemana | Texto | Dias da Semana que a sala está disponível para reserva |
| HorasInicioFim | Array de Números | Indica o início e o fim das horas naquele dia de semana |

Não é necessário levar em conta dias especiais, como feriados.

Esta disponibilidade é constante e não se irá alterar ao longo do tempo.

## Funcionalidades: 
Será necessário implementar as seguintes funcionalidades:

- Adicionar uma Sala
  - Poderá ser adicionada uma sala de reuniões ou uma sala de entrevista.
- Reservar uma Sala
  - Qualquer sala poderá ser reservada, desde que esteja disponível no tempo indicado
- Cancelar uma Reserva
  - Não é necessário manter tracking das reservas canceladas, bastando apenas apagar o registo da memória.
- Mostrar as Reservas
  - Esta opção deverá permitir mostrar tanto as reservas para um determinado dia ou mostrar as reservas para uma determinada sala.
 