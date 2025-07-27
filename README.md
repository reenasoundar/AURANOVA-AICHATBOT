# 🤖 AI Chatbot using Gradio and Django

This project is an **AI-powered chatbot** built using **transformer models** in Python. The chatbot interface is served via **Gradio** and runs on **Google Colab**, while the frontend is optionally integrated with a Django-based web interface including **Login/Register** functionality.

---

## 📁 Project Structure
myproject/ ├── accounts/ # Django app (handles views, templates, user auth) │ ├── templates/ │ │ ├── login.html │ │ ├── register.html │ │ └── home.html │ ├── views.py │ └── ... ├── myproject/ # Django project settings │ ├── settings.py │ ├── urls.py │ └── ... ├── db.sqlite3 # Django database ├── manage.py # Django management script ├── colab_model_training.ipynb # Google Colab notebook (model training + Gradio) └── README.md </pre>




---

## 🚀 How to Run This Project

### 🔗 Step 1: Run the Chatbot on Colab

1. Open the Colab notebook [`chatbot_notebook.ipynb`](#) in Google Colab.
2. Click on **Runtime > Run all**.
3. At the end of execution, you'll get a **Gradio link** like:  
   `https://xxxx.gradio.live`
4. Copy this link — you'll use it in your Django project.

---

### 🧠 What’s Inside the Colab Notebook?

- Imports required transformer libraries
- Loads tokenizer & model (e.g., SQLCODER 7B, LLaMA, Falcon, etc.)
- Fine-tunes or loads pre-trained weights
- Wraps everything with a **Gradio chatbot interface**

---

### 🛠️ Step 2: Setup Django Integration (Optional)

1. In `views.py` (inside Django project):
   ```python
   from django.shortcuts import redirect
   def chatbot_view(request):
       return redirect("https://xxxx.gradio.live")  # Paste your Gradio link here
run your django server 
you will get a link like http://127.0.0.1:8000/
