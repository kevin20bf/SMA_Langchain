# SMA LangChain — Agents IA avec LangGraph & Groq

Projet d'apprentissage des agents IA avec LangChain, LangGraph et le modèle Llama 3 via Groq.

## Concepts abordés

- Création d'agents avec `create_agent`
- Sélection dynamique de modèle via middleware
- Mémoire conversationnelle avec `InMemorySaver`
- Utilisation d'outils (tools) : météo, infos employé, recherche web
- Recherche web en temps réel avec Tavily

## Stack technique

- [LangChain](https://python.langchain.com/) — framework d'orchestration
- [LangGraph](https://langchain-ai.github.io/langgraph/) — moteur d'agents
- [Groq](https://console.groq.com/) — inférence rapide (Llama 3.3 70B / Llama 3.1 8B)
- [Tavily](https://tavily.com/) — recherche web pour agents

## Installation

```bash
# Cloner le projet
git clone <url-du-repo>
cd SMA_Langchain

# Installer les dépendances avec uv
uv sync
```

## Configuration

Crée un fichier `.env` à la racine :

```env
GROQ_API_KEY=ta_cle_groq
TAVILY_API_Key=ta_cle_tavily
```

- Clé Groq : [console.groq.com/keys](https://console.groq.com/keys)
- Clé Tavily : [app.tavily.com](https://app.tavily.com)

## Utilisation

Ouvre `sma.ipynb` dans VS Code ou Jupyter et exécute les cellules dans l'ordre.

## Structure du notebook

| Section | Description |
|---------|-------------|
| Agent basique | Premier agent avec prompt système |
| Sélection dynamique | Choix du modèle selon le contexte (`test` vs `prod`) |
| Mémoire | Agent avec historique de conversation par thread |
| Tools | Agent avec outils météo et RH |
| Recherche web | Agent avec Tavily pour les actualités |
