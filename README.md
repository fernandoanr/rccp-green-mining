# RCCP Green Mining

Calculadora de planejamento agregado de capacidade para Centros de Coleta, Transporte e Hub.

**Site:** https://fernandoanr.github.io/rccp-green-mining/

## Organização

- `index.html`: página de entrada e metadados de compartilhamento.
- `rccp/index.html`: interface, cenários e layout de impressão.
- `rccp/rccp-model.js`: motor de cálculo.
- `rccp/rccp-baseline.js`: parâmetros e cenário-base.
- `rccp/arrival-profile-2025.js`: perfil de chegadas.
- `rccp/support.js`: suporte de renderização.
- `rccp/green-mining-logo.png`: identidade visual.
- `og.png` e `favicon.svg`: recursos de compartilhamento e ícone.
- `tests/`: testes do motor.

## Uso

Os cálculos são executados no navegador. Os cenários salvos ficam somente no navegador e não são enviados ao repositório. Use a importação e exportação de JSON para transportar um cenário.

Para executar localmente, sirva esta pasta por HTTP e abra o endereço informado:

```sh
python3 -m http.server 8000
```

## Verificação

```sh
node --test tests/rccp-model.test.cjs
```

## Publicação

O GitHub Pages publica a raiz da branch `main`. A interface e o motor utilizam caminhos relativos, compatíveis com o endereço do projeto.

A ferramenta compara carga e capacidade agregadas; não representa filas, horários de partida nem sequência de rotas.
