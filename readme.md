# Módulo iugu Cartão para WHMCS

[![versão](https://img.shields.io/github/v/release/gofas/gofasiugucartao?label=vers%C3%A3o&color=005071&style=flat-square)](https://github.com/gofas/gofasiugucartao/releases/latest)
[![downloads](https://img.shields.io/github/downloads/gofas/gofasiugucartao/total?label=downloads&color=005071&style=flat-square)](https://github.com/gofas/gofasiugucartao/releases/latest)
[![licença](https://img.shields.io/badge/licen%C3%A7a-propriet%C3%A1ria-005071?style=flat-square)](https://gofas.net/contrato-de-venda-de-licenca-de-uso-de-software/)
[![suporte](https://img.shields.io/badge/suporte-f%C3%B3rum%20gratuito-ff8700?style=flat-square)](https://gofas.net/foruns/)

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

O download é contabilizado no site pelo contador de instalações do módulo.

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

Fórum de suporte gratuito: https://gofas.net/foruns/

## Licença

Software proprietário da Gofas Software. O código é público apenas para transparência e consulta; isso não concede licença de uso, modificação ou redistribuição. É vedado modificar, redistribuir, sublicenciar ou realizar engenharia reversa sem autorização prévia por escrito. Veja [LICENSE](LICENSE) e o contrato completo em https://gofas.net/contrato-de-venda-de-licenca-de-uso-de-software/.
