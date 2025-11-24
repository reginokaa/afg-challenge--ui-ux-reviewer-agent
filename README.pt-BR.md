# UI/UX Reviewer | Azure Frontier Girls Challenge

## 📘 Visão Geral
Este projeto fornece um assistente com IA capaz de revisar screenshots de sites, aplicativos, dashboards ou outras interfaces digitais.  
O agente analisa layout, hierarquia visual, usabilidade e possíveis problemas de acessibilidade, oferecendo sugestões claras e concisas de melhoria.

A avaliação é baseada no seguinte prompt:

```
Você é um assistente de design UI/UX. O usuário enviará screenshots de sites,
apps, dashboards ou interfaces. Você deve avaliar a imagem e então:

1. Analisar elementos de UI: botões, campos de texto, títulos, imagens, ícones pensando na experiência do usuário (ex.: tamanho dos elementos, cores, área clicável, design da página) – não liste os elementos. Você deve descrever brevemente sua avaliação.
2. Sugerir melhorias que considerar necessárias.

Sempre seja conciso e claro.
Para tópicos, use numeração sequencial.
```

---

## 🖼️ Como Capturar Screenshots de Alta Qualidade

Para garantir uma avaliação precisa de UI/UX, capture screenshots diretamente pelas ferramentas de desenvolvedor do navegador.  
Isso elimina barras do navegador, melhora a resolução e gera uma imagem limpa da interface renderizada.

### Passos

1. Abra o site ou aplicativo web que deseja avaliar.
2. Clique com o botão direito em qualquer lugar da página e selecione **Inspecionar** (ou pressione `F12`).
3. No painel **Elements/Elementos**, localize o elemento raiz `<html>`.
4. Clique com o botão direito no nó `<html>` e selecione:  
   - **Capture node screenshot** (Chrome), ou  
   - **Screenshot Node** (Firefox)  
5. O navegador salvará uma screenshot limpa, em alta resolução, da página renderizada.

Este método garante uma imagem:
- Sem barra de navegador  
- Sem barras de rolagem  
- Representando exatamente o layout renderizado pelo DOM  
- Com detalhes pixel-perfect para avaliação de UI/UX  

---

## 📤 Como Enviar a Screenshot para Avaliação

Siga os passos abaixo para enviar uma imagem ao agente de IA:

1. Abra a interface do Agente no **Azure AI Foundry**.
2. Clique no ícone **Upload/Anexar Arquivo** na área de entrada.
3. Selecione o arquivo `.png` ou `.jpg` da screenshot capturada.
4. Escreva uma mensagem como:
   - “Avalie esta interface, por favor.”  
   - ou “Quais melhorias de UX você sugere para esse layout?”  
5. Envie a mensagem.
6. O agente irá:
   1. Analisar a UI com base em heurísticas de UX.  
   2. Fornecer uma avaliação breve e objetiva (sem listar elementos).  
   3. Sugerir melhorias usando tópicos numerados.  

---

## 🧠 Como Funciona

1. Você envia uma screenshot.  
2. O agente envia a imagem para o **Azure AI Vision** para análise visual.  
3. O LLM interpreta a estrutura da interface conforme o prompt definido.  
4. O agente retorna uma avaliação de UI/UX e sugestões de melhoria.

---

## 🚀 Primeiros Passos

1. Clone ou baixe este projeto.  
2. Abra o workspace no Azure AI Foundry.  
3. Crie um Agente e cole o prompt fornecido.  
4. Adicione a ferramenta HTTP do Azure Vision para análise de imagens.  
5. Teste enviando uma screenshot e analisando a resposta do agente.

---

