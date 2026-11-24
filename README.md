# Inspetor de Meta Tags e Open Graph

[![Inspetor Meta Tags](https://img.shields.io/badge/TAVARDT-Meta%20Tags-5b3cf5.svg)](https://tools.tavardt.com/br/verificador-meta-tags/)
[![Python](https://img.shields.io/badge/Python-3.8%2B-blue.svg)](https://www.python.org/)
[![License: MIT](https://img.shields.io/badge/License-MIT-green.svg)](LICENSE)

Auditoria de metadados HTML, analise de comprimento de titulos e meta descricoes, pre-visualizacao de cards sociais e checagem de diretivas de indexacao.

Desenvolvido e mantido pela divisao de engenharia de busca e experiencia do usuario da **TAVARDT**.

***

## Capacidades de Auditoria de Metadados e Redes Sociais

* **Inspecao de Titulos e Descricoes**: Analise de extensao recomendada da tag title (30 a 60 caracteres) e meta description (120 a 160 caracteres).
* **Validacao de Protocolo Open Graph**: Auditoria completa de tags og:title, og:description, og:image, og:url e og:type para compartilhamento no WhatsApp, Facebook e LinkedIn.
* **Integracao com Twitter Cards**: Checagem de definicoes twitter:card, twitter:title, twitter:description e twitter:image.
* **Controle de Indexabilidade**: Rastreio de diretivas meta robots (noindex, nofollow) e verificacao de tag canonica.
* **Pontuacao de Qualidade de Snippet**: Indice tecnico de 0 a 100 com recomendacoes diretas de redacao e formatacao de metadados.

***

## Instalacao e Execucao

Requer Python 3.8 ou superior sem dependencias externas adicionais.

```bash
git clone https://github.com/TAVARDT-Brasil/meta-tags-inspector-br.git
cd meta-tags-inspector-br
python meta_inspector.py exemplo.com.br
```

Para gerar a saida em formato estruturado JSON:

```bash
python meta_inspector.py exemplo.com.br -json
```

***

## Diagnostico Completo na Web

Para pre-visualizacao visual de snippets e teste em tempo real:

* **Inspetor de Meta Tags Oficial**
* **[Portal Corporativo TAVARDT](https://ag.tavardt.com/br/)**

***

## Consultoria em Otimizacao e SEO Tecnico

Para projetos de aprimoramento de visibilidade organica e conformidade com Boas Praticas de SEO Tecnico e Compartilhamento Social, contate a equipe da **TAVARDT**.

***

## Links Úteis

* **Portal Corporativo:** https://ag.tavardt.com/br/
* **Suíte de Diagnósticos:** https://tools.tavardt.com/br/
* **Contato Técnico:** https://ag.tavardt.com/br/contato/

***

### Licença
Distribuído sob a Licença MIT. Consulte o arquivo [LICENSE](LICENSE) para obter detalhes completos.

***

© 2026 TAVARDT. Todos os direitos reservados.
