# Flow MCP: Native Google Flow AI Integration

This repository contains the configuration and guides to run and connect the Google Flow MCP server remotely.

---

## 📂 Files in this Repository
* **`docker-compose.yml`** — Configuration to run the Flow API & MCP server container.

---

## 🚀 1. Deploying the Server (On Any PC)

To start the server:
1. Ensure **Docker** is running.
2. Run this command in the repository folder:
   ```bash
   docker-compose up -d
   ```
3. Load Chrome and verify that your **Flow Chrome Extension** is connected.

*Note: If you deploy on another PC with a different Cloudflare subdomain, update the `PUBLIC_BASE_URL` in `docker-compose.yml` before starting.*

---

## 🔌 2. Connecting to Cursor / Desktop Apps (SSE Transport)

To connect your IDE or desktop app (like Cursor) to the server over the internet:

Open Cursor Settings (`Cmd + ,`) -> **Models** -> **MCP** -> **Add New MCP Server**:
* **Name**: `flow`
* **Type**: `SSE`
* **URL**: `https://flow.chatbulky.com/sse`

---

## 🌐 3. Connecting to ChatGPT Web (Chrome)

For browser-based ChatGPT (Web):
1. Add a Custom Connector/MCP tool in your ChatGPT Web interface.
2. Select **SSE** transport type.
3. Use the URL:
   ```text
   https://flow.chatbulky.com/sse
   ```
4. Set Authentication to **None** (Disable OAuth).
