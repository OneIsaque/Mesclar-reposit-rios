## 📂 Módulo 5: Importação como Subdiretório com `git subtree`

- Mantém o histórico de B organizado em uma pasta única  
- Comando para adicionar B dentro de A com “squash”  
  ```bash
  > git subtree add --prefix=repositorio-B \
    https://github.com/usuario/repositorio-B.git main --squash
  ```

---

## 📦 Módulo 6: Integração com `git submodule`

- Mantém B como projeto separado dentro de A  
- Fluxo básico de criação  
  ```bash
  > git submodule add https://github.com/usuario/repositorio-B.git repositorio-B
  > git commit -m "Adiciona repoB como submódulo"
  ```

- Para atualizar submódulo  
  ```bash
  > git submodule update --remote
  ```

---

## 🚀 Módulo 7: Fluxos Práticos e Exemplos

| Situação                             | Comando Principal                                                                  | Quando Usar                       |
|--------------------------------------|------------------------------------------------------------------------------------|-----------------------------------|
| Mesclar dois projetos independente   | `git merge --allow-unrelated-histories`                                            | Quando precisa unificar tudo      |
| Importar como subdiretório mantendo histórico | `git subtree add --prefix=pasta ... --squash`                                     | Ao organizar projetos dentro de um|
| Manter dependência separada          | `git submodule add ...`                                                            | Se B deve evoluir fora de A       |

---

