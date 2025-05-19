## 📌 Organização dos Estudos com Git

Durante meus estudos de programação, percebi que uma ótima forma de manter tudo organizado é utilizando branches no Git para separar cada tópico desenvolvido durante o curso. 💡

## 🚀 Estrutura de Branches

Para cada novo tópico, crio uma branch separada a partir da `main`, garantindo que cada conceito fique bem organizado e isolado:

```sh
git checkout -b 04_primeirosPassosComSpringBoot  # Cria e troca para a nova branch
```

Isso cria uma nova branch chamada `04_primeirosPassosComSpringBoot` baseada na `main`.

## 🔄 Mantendo a Branch Atualizada

Se houver atualizações na main que preciso na branch do tópico, posso utilizá-las da seguinte forma:

```sh
# Atualizar a branch com as mudanças da main
git rebase main  # Mantém um histórico mais limpo e linear
# ou
git merge main   # Mantém o histórico de commits original
```

⚠️ _Dica:_ O `git rebase` é ideal para manter um histórico mais linear, mas deve ser usado com cuidado, especialmente em branches compartilhadas, pois altera o histórico de commits.
<br>

Após as alterações, envio a branch para o repositório remoto:

```sh
git push -u origin 04_primeirosPassosComSpringBoot
```

## ✅ Benefícios desta abordagem:

- Cada tópico tem sua própria branch
- A `main` mantém sempre a versão consolidada
- Posso voltar a qualquer tópico sem misturar conteúdos
- Aprendo `Git` de forma prática

📌 _Dica Extra:_ Nomear as branches com um prefixo numérico (01, 02, etc.) ajuda a manter a ordem cronológica dos tópicos!
