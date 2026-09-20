# 🧸 Doudou – enseignant d'informatique virtuel (9ème année)

Chatbot + quiz **بالتونسي** (dialecte tunisien par défaut, avec français et anglais) sur : carte **BBC micro:bit**, **Internet des Objets (IoT)**, **MIT App Inventor**.

## Fichiers
- `app.py` : l'application (Gradio + Gemini)
- `requirements.txt` : les bibliothèques à installer

## Variables d'environnement
| Nom | Rôle |
|---|---|
| `GEMINI_API_KEY` | (obligatoire) clé gratuite créée sur https://aistudio.google.com/api-keys |
| `MOT_DE_PASSE` | (optionnelle) protège l'accès ; identifiant : `eleves` |
| `PYTHON_VERSION` | (conseillée sur Render) `3.12.3` |

## Lancer en local (test)
```bash
pip install -r requirements.txt
export GEMINI_API_KEY="ta_cle"      # Windows : set GEMINI_API_KEY=ta_cle
python app.py                       # puis ouvre http://localhost:7860
```

## Déployer gratuitement sur Render
- Type : **Web Service** (Python) – Instance : **Free**
- Build Command : `pip install -r requirements.txt`
- Start Command : `python app.py`
- Ajoute les variables d'environnement ci-dessus.

⚠️ Sur l'offre gratuite, le service s'endort après ~15 min sans visite : le premier chargement prend environ 1 minute.
Le quota gratuit de Gemini est **partagé par tous les élèves**. Ne demande pas d'informations personnelles aux élèves.
