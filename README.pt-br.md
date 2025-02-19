# FreeSomeSpace
Um script shell que interage com usuário para excluir `node_modules` de projetos não utilizados.  

# Delete `node_modules` Script 🗑️

Um script poderoso e interativo para ajudar você a encontrar e excluir diretórios `node_modules`, liberando espaço valioso no disco do seu Mac. Perfeito para desenvolvedores que trabalham com vários projetos! 🚀  

---

## Features ✨

- **Seleção Interativa**: Usa `fzf` (fuzzy finder) para selecionar facilmente quais diretórios `node_modules` deletar.  
- **Exclusão Segura**: Solicita confirmação antes de excluir cada diretório—evitando exclusões acidentais!  
- **Suporte Multi-Projeto**: Funciona em vários projetos dentro de um diretório específico.  
- **Verificação de Dependências**: Verifica automaticamente e instala dependências ausentes (como `fzf`).  
- **Fácil de Usar**: Projetado com instruções claras e prompts intuitivos.  

---

## Pré-requisitos 📋  

- **MacOS**: O script foi montado para MacOS.  
- **Homebrew**: Necessário para instalar dependências ausentes (como `fzf`).    

---

## Instalação 🛠️  

### 1. Baixar o Script  
Faça o download do script para o local desejado usando `curl`:  
```bash
curl -O https://raw.githubusercontent.com/erivanstdio/FreeSomeSpace/main/delete_node_modules.sh
```

### 2. Tornar o Script Executável  

Execute o seguinte comando para permitir a execução do script:  


```bash
chmod +x delete_node_modules.sh
```


### 3. (Opcional) Adicionar o Script ao PATH  

Para executar o script de qualquer lugar, mova-o para um diretório no seu PATH, como `/usr/local/bin` ou `~/bin`:  

```bash
mkdir -p ~/bin
mv delete_node_modules.sh ~/bin/delete_node_modules
```

Depois, adicione `~/bin` ao seu PATH, inserindo a seguinte linha no arquivo de configuração do seu shell (`~/.zshrc` ou `~/.bashrc`):  

```bash
export PATH="$HOME/bin:$PATH"
```

Recarregue a configuração do shell:  

```bash
source ~/.zshrc  # or ~/.bashrc
```

---

## Uso 🚀  

### Uso Básico  

Execute o script no diretório atual:  

```bash
delete_node_modules
```

### Especificar um Diretório  

Para buscar `node_modules` em um diretório específico, use a opção `--dir`:  

```bash
delete_node_modules --dir /path/to/your/directory
```

### Ajuda  

Para ver a mensagem de ajuda, use a opção `--help`:  

```bash
delete_node_modules --help
```
---

## Como Funciona ⚙️  

- O script procura todos os diretórios `node_modules` a partir do diretório especificado (ou do diretório atual, se nenhum for indicado).  
- Exibe o tamanho de cada diretório `node_modules`.  
- Permite selecionar interativamente quais diretórios deseja excluir usando `fzf`.  
- Solicita confirmação antes de excluir cada diretório selecionado.  

---

## Exemplo de Uso 📂  

### Passo 1: Navegar até o Diretório dos Projetos  

```bash
cd /path/to/your/projects
```
### Passo 2: Executar o Script

```bash
delete_node_modules
```

### Passo 3: Selecionar Diretórios para Excluir  

- Use as setas do teclado para navegar pela lista de diretórios `node_modules`.  
- Pressione **Tab** para selecionar vários diretórios.  
- Pressione **Enter** para confirmar sua seleção.  

### Passo 4: Confirmar a Exclusão  

Para cada diretório selecionado, o script pedirá uma confirmação antes de excluir.  
Digite `y` para excluir ou `n` para pular.  

---

## Solução de Problemas 🛠️  

### O Script Não Está Executável  

Se aparecer um erro como **Permissão negada**, certifique-se de que o script é executável:  

```bash
chmod +x delete_node_modules.sh
```

### Dependências Ausentes  

Se o script relatar dependências ausentes (como `fzf`), instale-as usando Homebrew:  

```bash
brew install fzf
```

### Script Não Encontrado  

Se aparecer um erro como **comando não encontrado: delete_node_modules**, verifique se o script está no seu PATH:  

```bash
echo $PATH
```

Se `~/bin` não estiver listado, adicione-o ao seu PATH conforme descrito na seção **Instalação**.  

---

## Licença 📜  

Este script é fornecido sob a Licença MIT. Sinta-se à vontade para usar, modificar e distribuí-lo conforme necessário.  

---

## Autor 👨‍💻  

**Erivan Brunno**  
GitHub: [erivanstio](https://github.com/erivanstio)  
E-mail: erivanstdio@gmail.com  

---

## Feedback 💬  

Se tiver dúvidas, sugestões ou encontrar problemas, abra uma issue no GitHub ou entre em contato diretamente. Seu feedback é muito bem-vindo! 🙌  
