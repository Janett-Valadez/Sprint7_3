# 🚀 Demo CI/CD con Streamlit y Render

Este proyecto muestra cómo crear, ejecutar y desplegar una aplicación sencilla de **Streamlit** usando **Render**.
Este es un nuevo cambio para mostrar

---

## 📌 1. Crear el ambiente con Conda
Primero, asegúrate de tener [Anaconda](https://www.anaconda.com/download) o [Miniconda](https://docs.conda.io/en/latest/miniconda.html) instalado.  
Luego, en tu terminal:

```bash
conda create -n streamlit-demo-webinar
conda activate streamlit-demo-webinar
```

Instala los paquetes desde `requirements.txt`:

```bash
pip install -r requirements.txt
```

---

## 📌 2. Ejecutar la app localmente
Para probar que tu aplicación funciona antes de desplegarla:

```bash
streamlit run app.py
```

Esto abrirá la aplicación en tu navegador en:  
👉 [http://localhost:8501](http://localhost:8501)

---

## 📌 3. Despliegue en Render
1. Accede a tu cuenta en [Render](https://render.com/) y abre el **Dashboard**  

2. Crea un **nuevo servicio web** enlazado a tu repositorio de GitHub  

3. Configura tu servicio web:
   - **Build Command**  
     ```bash
     pip install --upgrade pip && pip install -r requirements.txt
     ```
   - **Start Command**  
     ```bash
     streamlit run app.py
     ```

4. Despliega y espera que el build termine correctamente  

5. Comprueba tu aplicación en:  
   ```
   https://<APP_NAME>.onrender.com/
   ```

⚠️ **Notas importantes**:
- Puede tardar unos minutos en estar disponible la primera vez.  
- En el plan gratuito, las apps entran en “sleep mode” si están inactivas. Solo necesitas recargar la página para despertarlas.  
- Si actualizas el repositorio de GitHub, en Render puedes forzar el despliegue manual en:  
  **Manual Deploy → Latest Commit**

---


¡Listo! Ahora tienes tu primera aplicación desplegada con **Streamlit + Render** 🚀




