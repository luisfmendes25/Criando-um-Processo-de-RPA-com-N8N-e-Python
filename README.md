# 🤖 Criando um Processo de RPA com N8N e Python

## 🎯 Objetivo do Projeto
Este projeto prático faz parte do bootcamp da DIO e tem como objetivo construir um **Assistente de Investimentos automatizado**, utilizando automação de processos robóticos (RPA) para orquestrar a coleta de dados, análise via Inteligência Artificial e envio de relatórios.

## 🛠️ Tecnologias Utilizadas
* **n8n:** Orquestração do fluxo de trabalho (Nodes: Webhook, HTTP Request, Merge, Code).
* **Python (Google Colab):** Desenvolvimento da lógica inicial do MVP e processamento de dados.
* **LLM (Inteligência Artificial):** Agente de IA para interpretar os dados e gerar um briefing inteligente.
* **Gmail:** Nó utilizado para automatizar o disparo do e-mail final.

## ⚙️ Arquitetura do Fluxo de Automação
O workflow no n8n foi desenhado seguindo estas etapas principais:
1. **Gatilho (Webhook):** Inicia o processo recebendo as requisições externas.
2. **Coleta e Tratamento de Dados (HTTP Request + Merge + Code):** Realiza chamadas de APIs para buscar dados, mescla as informações necessárias e roda pequenos scripts (Code) para adequar o formato (JSON).
3. **Análise com Agente de IA:** Os dados estruturados são enviados para o modelo de linguagem (LLM), que atua como o assistente, gerando um texto explicativo (Briefing) sobre o cenário de investimentos.
4. **Disparo de E-mail:** O texto gerado pela IA é formatado e enviado automaticamente via Gmail para o usuário final.

## 💡 Principais Aprendizados
* Como estruturar Webhooks para conectar ferramentas externas ao n8n.
* Manipulação de requisições HTTP e unificação de ramificações usando o nó `Merge`.
* Injeção de lógica customizada com o nó `Code`.
* Criação de agentes de IA integrados a fluxos de comunicação (Gmail).
