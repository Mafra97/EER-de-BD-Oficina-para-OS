# EER-de-BD-Oficina-para-OS
Exercicio de desenvolvimento de um EER de BD para OS em uma oficina mecânica

Este projeto consiste no desenvolvimento do esquema conceitual e lógico de um sistema para controle e gerenciamento de ordens de serviço em uma oficina mecânica

Decisões de Projeto e Complementações

Status da Ordem de Serviço:

Implementei um campo status na tabela ordem_servico com os valores: 'Aberta', 'Em andamento', 'Concluída' e 'Cancelada'

Isso permite melhor acompanhamento do fluxo de trabalho, não especificado na narrativa original

Tabela de Preços de Referência:

Criei uma entidade separada tabela_referencia para armazenar os valores padrão de mão-de-obra

Isso permite atualizações de preços sem afetar ordens de serviço já existentes

Especialização dos Mecânicos:

Adicionei o campo especialidade na tabela mecanico

Permite designar mecânicos específicos para tipos de serviço, melhorando a eficiência

Valor Total Dinâmico:

O campo valor_total em ordem_servico será calculado automaticamente

Soma dos valores dos serviços (com base na tabela de referência) mais peças utilizadas

Controle de Peças:

Adicionei o campo quantidade na tabela peca

Permite registrar quantas unidades de cada peça foram utilizadas na OS

Relacionamento Equipe-Veículo:

Estabeleci relação 1:1 entre veículo e equipe

Considerando que uma equipe atende um veículo por vez, mas poderia ser ajustado para N:N se necessário

Justificativas

As decisões tomadas buscam:

Complementar informações não explicitadas na narrativa

Garantir a normalização do banco de dados

Permitir escalabilidade do sistema

Facilitar a manutenção e atualização dos dados

Melhorar a experiência do usuário final

O esquema está pronto para implementação e pode ser adaptado conforme necessidades específicas da oficina.
