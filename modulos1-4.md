## 🎯 Módulo 1: Conceitos Básicos de Git e GitHub

- Git é um sistema de controle de versões distribuído  
- GitHub é uma plataforma para hospedar repositórios remotos  
- Branch, commit, merge e remoto são conceitos fundamentais  

---

## 🔍 Módulo 2: Cenários de União de Repositórios

1. Mesclar o conteúdo de dois históricos distintos  
2. Importar repositório B dentro de A como subdiretório  
3. Manter B independente dentro de A via submódulo  

---

## 🛠️ Módulo 3: Preparação e Backup

- Confirme permissão de leitura/escrita em ambos repositórios  
- Clone cada repositório em pastas separadas  
- Opcional: compactar ou criar tags de backup para emergências  

---

## 🔗 Módulo 4: Mesclagem Direta de Repositórios

1. **Clone o repositório A (_destino_)**  
   ```bash
   > git clone https://github.com/usuario/repositorio-A.git
   > mcd repositorio-A

2. **Adicione o repositório B como remoto**

```bash
> git remote add repoB https://github.com/usuario/repositorio-B.git
```
- Busque o histórico de B

```bash
> git fetch repoB
```
- Mescle a branch principal de B em A


```bash
git merge repoB/main --allow-unrelated-histories
```
- Resolva conflitos, _commit e push_

```bash
> git add .
> git commit -m "Mescla repositório B em A"
> git push origin main
```
