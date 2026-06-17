# RAG Colab Demo

This repository contains a single Google Colab-ready notebook that implements a Retrieval-Augmented Generation (RAG) pipeline with a native Colab `ipywidgets` UI. Users can upload a PDF, select a domain (Media, Law, Telecom, General), and either ask questions or generate a structured summary.

Files:
- [RAG_Colab_Notebook.ipynb](RAG_Colab_Notebook.ipynb) - The Colab notebook (run cell 1, then cell 2).
- [.env.example](.env.example) - Example environment toggles.
- [requirements.txt](requirements.txt) - Python dependencies for local testing.
- [.gitignore](.gitignore) - Useful ignores for local development.

Quick start (open in Google Colab):

1. Clone the repo locally (or open directly from GitHub in Colab):

```bash
git clone <your-repo-url>
cd <repo-folder>
```

2. Open the notebook in Colab:

- Option A: Upload `RAG_Colab_Notebook.ipynb` in Colab (File -> Upload notebook).
- Option B: Use Colab's GitHub integration: `https://colab.research.google.com/github/<owner>/<repo>/blob/main/RAG_Colab_Notebook.ipynb`

3. Run the first cell to install dependencies. If you want to use Ollama locally inside the Colab VM, click the "Install & Run Ollama" button in the UI (this may or may not succeed depending on the Colab environment). For most users, choose the OpenAI backend.

4. In the Configuration panel, set Backend to `OpenAI (Cloud)` and paste your OpenAI API key into the `OpenAI Key` field, or choose `Ollama (Local)` if you have Ollama running.

5. Upload a PDF, choose a domain, then click `Ask` or `Generate Summary`.

.env usage (optional):
- The notebook writes a `.env` file automatically, but you can create one yourself from `.env.example` and edit keys locally.

Push to GitHub (if you want to check in from your machine):

```bash
git init
git add .
git commit -m "Add Colab RAG notebook and README"
git remote add origin <your-git-remote-url>
git push -u origin main
```

Replace `<your-git-remote-url>` with your repository's remote URL.

Security notes:
- Do not commit your `.env` or API keys. Add keys locally or use Colab UI to paste them.
- The `.gitignore` includes `.env` by default.

If you want, I can help generate a GitHub repo and provide the exact commands to push these files from this machine (I cannot push automatically without your remote credentials).