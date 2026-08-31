# Versões do Als Copilot

Este repositório tem **um arquivo só**: `versoes.json`, o anúncio de qual é a versão mais
recente do Als Copilot.

## Por que ele é público

Cada instalação do Als Copilot consulta este arquivo de hora em hora para saber se saiu versão
nova. Ler não pode depender de senha: uma credencial vencida faria a instalação parar de
receber avisos **em silêncio** — e o cliente ficaria para trás sem ninguém perceber.

Aqui não há código nem segredo nenhum. Só o número da versão e o resumo do que mudou, escrito
para o usuário ler.

**As imagens da aplicação continuam privadas.** Elas são o produto; isto é só o aviso.

## Quem escreve

O comando `scripts/publicar.sh`, do repositório principal. Não editar à mão.

## O formato

```json
{
  "atual": {
    "versao": "1.3.0",
    "novidades": "O que mudou, em português de gente.",
    "obrigatoria": false,
    "publicada_em": "2026-08-31"
  },
  "anteriores": []
}
```

- **`versao`** — maior.menor.correção. É por ela que a instalação sabe se está atrasada.
- **`novidades`** — o texto que aparece no aviso, dentro do sistema. Máximo 500 caracteres.
- **`obrigatoria`** — deixa o aviso mais enfático. **Nunca atualiza sozinho**: quem aperta o
  botão é sempre uma pessoa.
- **`anteriores`** — o histórico. Serve para o aviso sumir da tela de quem pulou versões.
