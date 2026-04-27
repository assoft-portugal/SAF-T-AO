# SAF-T AO

[English](README.md) | [Português](README.pt-AO.md)

[![GitHub All Releases](https://img.shields.io/github/downloads/assoft-portugal/SAF-T-AO/total)](https://github.com/assoft-portugal/SAF-T-AO/releases)
[![GitHub issues](https://img.shields.io/github/issues-raw/assoft-portugal/SAF-T-AO)](https://github.com/assoft-portugal/SAF-T-AO/issues)
[![GitHub tag (latest SemVer)](https://img.shields.io/github/v/tag/assoft-portugal/SAF-T-AO)](https://github.com/assoft-portugal/SAF-T-AO/releases)
[![License](https://img.shields.io/badge/license-MIT-blue.svg)](https://github.com/assoft-portugal/SAF-T-AO/blob/master/LICENSE)
[![Discussion](https://img.shields.io/badge/discusion-telegram-blue)](https://t.me/saftao)

XSD Oficial do Governo de Angola para uso no SAF-T AO. O propósito deste esquema é padronizar o formato dos dados relacionados com impostos, facilitando a auditoria e a conformidade com os regulamentos fiscais angolanos.

> O Standard Audit File for Tax Purposes (SAF-T) é um ficheiro XML normalizado utilizado para exportar a informação contabilística de uma empresa para as autoridades fiscais. O ficheiro contém dados contabilísticos que podem ser exportados de um sistema contabilístico original para um período de tempo específico.
>
> O ficheiro SAF-T baseia-se numa diretiva da Organização para a Cooperação e Desenvolvimento Económico (OCDE).
>
> [Oracle, JD Edwards EnterpriseOne Applications OECD Standard Audit File for Tax Purposes (SAF-T) Localizations Implementation Guide](https://docs.oracle.com/cd/E16582_01/doc.91/e97460/ch_eu_saft_xml.htm#EOAST109).

## Implementação do IVA em Angola

A [legislação](Resources/Legislation/README.md) do IVA entrou em vigor em outubro de 2019. O prazo aplica-se a soluções de faturação de software, ficheiro SAF-T e regras de faturação:

- As soluções de software devem seguir os requisitos do novo sistema jurídico para processar documentos de venda, faturas e outros documentos financeiros de acordo com o quadro jurídico. Esta regra aplica-se a todos os sujeitos do regime de IVA.
- Os criadores de software devem candidatar-se a um programa de certificação de software pelo governo, que é obrigatório.
- A partir de 1 de janeiro de 2020, é obrigatório produzir um ficheiro SAF-T mensal e enviá-lo para as autoridades fiscais do governo.
- A partir de 1 de janeiro de 2020, todos os contribuintes com um volume de negócios anual superior a 50.000.000 AKZ serão obrigados a produzir os ficheiros SAF-T acima referidos e a utilizar software certificado.

## Estrutura do Esquema

O esquema XML está organizado nos seguintes elementos principais:

- **AuditFile**: O elemento raiz que contém todos os dados do ficheiro de auditoria.
- **Header**: Metadados sobre o ficheiro de auditoria.
- **MasterFiles**: Ficheiros de dados mestres, tais como contas do razão geral, clientes, fornecedores, produtos e tabelas de impostos.
- **GeneralLedgerEntries**: Entradas do razão geral.
- **SourceDocuments**: Documentos de origem, tais como faturas de venda, faturas de compra e movimentação de mercadorias.

## Validação XML

### Unix

- [xmllint](http://xmlsoft.org/xmllint.html)

### Windows

- [XmlPad](https://xmlpad-mobile.com/) com uma interface gráfica de utilizador
- [Test-XML](https://www.powershellgallery.com/packages/Test-XML/1.0) com [PowerShell](https://docs.microsoft.com/en-us/powershell/)

### Instalando o xmllint

```bash
sudo apt install libxml2-utils
```

### Validação XML contra XSD

```bash
xmllint -schema schema.xsd file.xml --noout
```

## Contribuidores

Este projeto existe graças a todas as pessoas que contribuem. [[Contribuir]](CONTRIBUTING.md).

<a href="https://github.com/assoft-portugal/SAF-T-AO/graphs/contributors">
  <img src="https://contrib.rocks/image?repo=assoft-portugal/SAF-T-AO" />
</a>
