# Módulo iugu Cartão para WHMCS

[![versão](https://img.shields.io/github/v/release/gofas/gofasiugucartao?label=vers%C3%A3o&color=005071&style=flat-square)](https://github.com/gofas/gofasiugucartao/releases/latest)
[![downloads](https://img.shields.io/endpoint?url=https%3A%2F%2Fgofas.net%2Fwp-json%2Fgofas%2Fv1%2Fbadge%2Fgofasiugucartao&style=flat-square)](https://github.com/gofas/gofasiugucartao/releases/latest)
[![abrir issue](https://img.shields.io/badge/suporte-abrir%20issue-ff8700?style=flat-square)](https://gofas.net/?p=12349/#new-post)

Processa pagamentos à vista e parcelados via API da iugu, usando a interface nativa de cartão de crédito do WHMCS, sem armazenar os dados do cartão no seu servidor. Desenvolvido pela Gofas Software, é 100% gratuito e de código aberto.

## Sumário

- [Download](#download)
- [Funcionalidades](#funcionalidades)
- [Requisitos](#requisitos)
- [Instalação](#instalação)
- [Configuração](#configuração)
- [Informações importantes](#informações-importantes)
- [Suporte](#suporte)
- [Licença](#licença)

## Download

**[Baixar a versão mais recente](https://github.com/gofas/gofasiugucartao/releases/latest/download/gofasiugucartao.zip)**

## Funcionalidades

- **Checkout nativo** de cartão de crédito do WHMCS
- **Pagamentos à vista ou parcelados**, com valor mínimo e número máximo de parcelas configuráveis
- **Não armazena dados de cartão** no seu servidor
- **Valor mínimo** da fatura para permitir pagamento com cartão
- **Suporte a produção e a testes (sandbox)**
- **Logs de diagnóstico** configuráveis
- **Aviso de atualização** e verificação de versão na própria tela de configuração do módulo

## Requisitos

- WHMCS >= 7.9
- PHP >= 8.1
- Conta iugu com API habilitada (ID da conta e tokens de produção e de testes)

## Instalação

1. Baixe o arquivo pelo link de download e descompacte. Será criada a pasta `gofasiugucartao`.
2. Copie a pasta `modules` de dentro de `gofasiugucartao` para a raiz da instalação do WHMCS, mesclando com as pastas existentes.
3. Ative o módulo em `Opções > Pagamentos > Portais para Pagamentos > aba All Payment Gateways`, clicando em "Gofas iugu - Cartão".
4. Informe o ID da conta e os tokens da API.

## Configuração

### Opções do módulo

<img src="https://raw.githubusercontent.com/gofas/gofasiugucartao/master/docs/img/tela-configuracoes-modulo-1.1.0.png" alt="Tela de configuracoes do modulo" width="640">

- **ID da Conta na iugu**: identificador da sua conta iugu.
- **API token produção**: token de produção da sua conta iugu.
- **API token teste**: token de testes da sua conta iugu.
- **Sandbox**: alterna entre o ambiente de testes e produção.
- **Salvar Logs**: grava informações de diagnóstico em `Utilitários > Logs > Log de Módulo`.
- **Valor mínimo**: valor mínimo da fatura para permitir pagamento com cartão.
- **Permitir Parcelamento**: exibe as opções de parcelamento na fatura quando aplicável.
- **Valor mínimo para parcelamento**: valor mínimo da fatura para permitir parcelamento.
- **Máximo de parcelas**: número máximo de parcelas oferecidas ao cliente.
- **Enviar estatísticas de uso (opcional)**: controla o envio identificado das estatísticas de confirmação de pagamento. Desmarcado, as confirmações continuam sendo contabilizadas de forma anônima.

## Informações importantes

- A tarifa do cartão é paga separadamente à iugu, conforme o plano da sua conta.
- Sempre faça backup antes de mudar algo no seu sistema.

## Suporte

[Abrir issue](https://gofas.net/?p=12349/#new-post) no fórum do módulo.

## Licença

O código deste módulo é público para transparência e auditoria. Isso não transfere a titularidade nem concede licença livre de uso: o software é de propriedade da Gofas Software, protegido pela Lei 9.609/98 e pelos tratados de direitos autorais.

Trechos do [contrato de licença de uso](https://gofas.net/contrato-de-venda-de-licenca-de-uso-de-software/) que se aplicam diretamente a este repositório:

- **Não redistribuir**: é proibido o aluguel, o arrendamento, o empréstimo, a cessão e o licenciamento do software a terceiros, total ou parcial, assim como o fornecimento de serviços de hospedagem comercial do software (Cláusula 10ª, §3º).
- **Não modificar**: é vedado qualquer procedimento que implique engenharia reversa, descompilação, desmontagem, tradução, adaptação ou modificação do software, bem como qualquer alteração não autorizada de suas funcionalidades (Cláusula 10ª, §2º).
- **Módulo alterado perde o suporte**: a Gofas não se responsabiliza por defeitos decorrentes de alteração do software, de operação por pessoas não autorizadas ou da integração com softwares de terceiros (Cláusula 10ª, §7º). O suporte é uma cortesia e não é garantido pela licença (Cláusula 7ª, §1º).
