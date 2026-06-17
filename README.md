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

3. Run the first cell to install dependencies. This notebook now uses an inline OpenAI key variable in Cell 1.

4. Open `RAG_Colab_Notebook.ipynb` in Colab, edit Cell 1 to set the `OPENAI_API_KEY` value to your OpenAI API key (replace the empty string), then run Cell 1 and Cell 2 in order.

5. Upload a PDF, choose a domain, then click `Ask` or `Generate Summary`.

Note on secrets:
- This notebook stores the OpenAI key inline in Cell 1 for simplicity when running in Colab. Do not commit your key to a public repository.
- For production usage, prefer managing secrets via environment variables or secret managers instead of inline keys.

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