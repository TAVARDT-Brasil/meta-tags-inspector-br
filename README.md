# Inspetor de Meta Tags e Open Graph

[![Inspetor Meta Tags](https://img.shields.io/badge/TAVARDT-Meta%20Tags-5b3cf5.svg)](https://tools.tavardt.com/br/verificador-meta-tags/)
[![Python](https://img.shields.io/badge/Python-3.8%2B-blue.svg)](https://www.python.org/)
[![License: MIT](https://img.shields.io/badge/License-MIT-green.svg)](LICENSE)

O **TAVARDT Inspetor de Meta Tags e Open Graph** oferece validação automatizada de metadados HTML, diretivas do protocolo Open Graph, links canônicos e qualidade de snippets de busca no Brasil.

***

## Arquitetura de Metadados e Matriz Diagnóstica

Rastreadores de busca e plataformas sociais dependem de cabeçalhos estruturados para indexar documentos e exibir cards visuais de compartilhamento. Falhas nas meta tags causam perda de tráfego orgânico, visualizações corrompidas e baixa taxa de cliques.

Esta ferramenta audita limites de caracteres em títulos, tamanho da meta descrição, tags sociais e canônicas a partir de uma pontuação base de 100 pontos sem dependências externas.

O motor analítico avalia as tags do cabeçalho HTML frente às normas dos motores de busca e especificações sociais:

<table>
  <thead>
    <tr>
      <th>Tag do Cabeçalho</th><th>Critério de Validação</th><th>Dedução</th><th>Impacto em SEO e Redes Sociais</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td><strong>Elemento Title</strong></td><td>Exige presença de <code>&lt;title&gt;</code>. Ideal: 30-60 caracteres. Penalizado se &lt;20 caracteres (-10 pts) ou &gt;70 caracteres (-10 pts). Ausente: -25 pts.</td><td>Até -25 pts</td><td>Principal fator de posicionamento orgânico e título clicável nas buscas.</td>
    </tr>
    <tr>
      <td><strong>Meta Description</strong></td><td>Exige <code>&lt;meta name='description'&gt;</code>. Ideal: 120-160 caracteres. Penalizado se &lt;70 caracteres (-10 pts) ou &gt;175 caracteres (-10 pts). Ausente: -20 pts.</td><td>Até -20 pts</td><td>Resumo decisivo para atração de cliques orgânicos na SERP.</td>
    </tr>
    <tr>
      <td><strong>Protocolo Open Graph</strong></td><td>Valida cinco propriedades obrigatórias: <code>og:title</code>, <code>og:description</code>, <code>og:image</code>, <code>og:url</code> e <code>og:type</code>.</td><td>-5 pts por tag ausente (Máx -25 pts)</td><td>Gera prévias visuais ricas no WhatsApp, LinkedIn, Facebook e Slack.</td>
    </tr>
    <tr>
      <td><strong>Link Canônico</strong></td><td>Exige presença de <code>&lt;link rel='canonical'&gt;</code> com URL de destino absoluta e canônica.</td><td>-10 pts</td><td>Evita problemas de canibalização e consolida sinais de indexação.</td>
    </tr>
    <tr>
      <td><strong>Falha de Conexão</strong></td><td>Tempo limite de requisição esgotado ou erro de handshake TLS/HTTP.</td><td>Pontuação zerada (0 pts)</td><td>Inacessibilidade do servidor impedindo a extração do cabeçalho HTML.</td>
    </tr>
  </tbody>
</table>

### Escala de Qualidade e Níveis de Status

O utilitário gera uma pontuação de conformidade classificando a maturidade dos metadados:

* <strong>85 a 100 (OPTIMAL)</strong>: Metadados perfeitamente estruturados; title, description, canônico e Open Graph 100% conformes.
* <strong>65 a 84 (ACCEPTABLE)</strong>: Configuração funcional com pequenos desvios de comprimento ou ausência pontual de tags sociais.
* <strong>0 a 64 (DEFICIENT)</strong>: Ausência crítica de tags centrais de indexação, prejudicando o ranqueamento e o compartilhamento.

***

## Instalação e Execução

Construído estritamente com a biblioteca padrão do Python 3.8+, sem qualquer dependência externa.

```bash
git clone https://github.com/TAVARDT-Brasil/meta-tags-inspector-br.git
cd meta-tags-inspector-br
```

### Execução Padrão via CLI

```bash
python meta_inspector.py exemplo.com.br
```

### Saída Estruturada para Pipelines em JSON

```bash
python meta_inspector.py exemplo.com.br -j
```

### Configuração de Timeout Personalizado

```bash
python meta_inspector.py exemplo.com.br -j -t 15
```

***

## Conformidade e Boas Práticas Digitais no Brasil

A correta identificação de metadados apoia as diretrizes brasileiras de governança e integridade digital da informação. Metadados consistentes protegem marcas contra fraudes em cards sociais e preservam a integridade institucional.

Recomenda-se incorporar a validação automatizada de cabeçalhos nos processos contínuos de deploy para garantir indexabilidade consistente.

***

## Perguntas Frequentes Técnicas

### Qual é o comprimento ideal de caracteres para a tag title?

O inspetor recomenda títulos entre 30 e 60 caracteres. Títulos com menos de 20 caracteres sofrem dedução de 10 pontos por oferecerem sinais fracos de relevância, enquanto títulos com mais de 70 caracteres perdem 10 pontos pelo risco iminente de truncamento no Google. A ausência total deduz 25 pontos.

### Como o validador avalia a meta description?

O sistema verifica se o resumo está entre 120 e 160 caracteres. Textos com menos de 70 ou mais de 175 caracteres sofrem penalização de 10 pontos. A ausência completa da tag description deduz 20 pontos.

### Quais propriedades Open Graph são exigidas pelo validador?

O analisador verifica cinco tags centrais: <code>og:title</code>, <code>og:description</code>, <code>og:image</code>, <code>og:url</code> e <code>og:type</code>. Cada tag não encontrada acarreta uma penalidade de 5 pontos, totalizando até 25 pontos de dedução.

### Por que a tag canonical é indispensável no SEO técnico?

A tag <code>&lt;link rel="canonical"&gt;</code> informa aos rastreadores qual é a versão oficial da página, consolidando autoridade e evitando canibalização por conteúdo duplicado. Sua omissão resulta em perda de 10 pontos.

### O que significam as faixas de status e pontuação de qualidade?

Uma pontuação de 85 a 100 pontos representa status OPTIMAL. Entre 65 e 84 pontos classifica-se como ACCEPTABLE, indicando pequenos ajustes necessários, e abaixo de 65 pontos o status é DEFICIENT, exigindo intervenção imediata nas tags essenciais.

***

## Resposta a Incidentes e Consultoria Técnica

Para auditorias aprofundadas de SEO técnico, estruturação de metadados e governança de aplicações web, consulte os especialistas da **TAVARDT**.

***

## Links Úteis

* **Portal Corporativo:** https://ag.tavardt.com/br/
* **Suíte de Diagnósticos:** https://tools.tavardt.com/br/
* **Contato Técnico:** https://ag.tavardt.com/br/contato/

***

### Licença
Distribuído sob a Licença MIT.

***

© 2026 TAVARDT. Todos os direitos reservados.
