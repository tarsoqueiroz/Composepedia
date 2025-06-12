# 🐳 Composepedia

**A enciclopédia de stacks Docker Compose.**  

Um repositório organizado com exemplos, templates e configurações reutilizáveis para diversos serviços e stacks baseados em Docker Compose.

---

## 📚 Visão Geral

Este repositório tem como objetivo:

- Centralizar configurações Docker Compose para diferentes aplicações e serviços.
- Servir como referência rápida para desenvolvedores e equipes de infraestrutura.
- Facilitar a criação e personalização de ambientes locais ou de teste.
- Promover boas práticas na organização e uso de `docker-compose`.

---

## 🧭 Estrutura do Repositório

```plaintext
/
├── databases/ (breve)
│   ├── postgres/
│   ├── mysql/
│   └── mongo/
├── dev-tools/
│   ├── nginx/ (breve)
│   ├── redis/ (breve)
│   └── n8n/
├── monitoring/ (breve)
│   ├── prometheus-grafana/
│   └── uptime-kuma/
├── full-stacks/ (breve)
│   ├── nextjs-postgres/
│   └── laravel-mysql/
├── 
└── README.md
```

---

## 🚀 Como usar

1. **Clone o repositório:**

```bash
   git clone https://github.com/seu-usuario/composepedia.git
   cd composepedia
```

2. **Escolha o serviço ou stack desejado:**

```bash
   cd databases/postgres
```

3. **Suba o serviço:**

```bash
   docker-compose up -d
```

---

## 📦 Exemplos incluídos

| Categoria      | Exemplos                           |
|----------------|------------------------------------|
| **Databases**  | PostgreSQL, MySQL, MongoDB         |
| **Dev Tools**  | Redis, Nginx, Traefik              |
| **Monitoring** | Prometheus + Grafana, Uptime Kuma  |
| **Full Stacks**| Next.js + PostgreSQL, Laravel + MySQL |

---

<!--
## 🙌 Contribuindo

Quer adicionar um novo serviço ou stack?

Veja o arquivo [`CONTRIBUTING.md`](./CONTRIBUTING.md) com as instruções para padronizar nomes de pastas, estrutura dos arquivos e boas práticas.

---
-->

## 📄 Licença

Este projeto está licenciado sob a [MIT License](LICENSE).
