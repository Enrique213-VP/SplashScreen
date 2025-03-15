# 🚀 Splash Screen en Android con Kotlin

Bienvenido a este proyecto donde implementamos una **Splash Screen** moderna en Android usando Kotlin. 🎨

✅ Animación de inicio ✨  
✅ Integración con lottie para las animaciones 🎭  
✅ Transición fluida a la pantalla principal 📲  

---

## 🎬 Demo en Video

📺 **Mira el video en acción:** 

[![Ver Video](https://img.shields.io/badge/Ver%20Video-%F0%9F%94%B4-red?style=for-the-badge)](https://www.youtube.com/watch?v=OLK0VfMi6Ws&ab_channel=Svape)

---

## 📌 Tecnologías Utilizadas

- 📱 Android SplashScreen API
- ⚙️ Kotlin
- 🎨 Material Design
- 🚀 Lottie

---

## 🚀 Configuración del Proyecto

1. **Clona este repositorio**
   ```bash
   git clone https://github.com/Enrique213-VP/SplashScreen.git
   ```

2. **Injeccion del Splash en tu `SplashScreenActivity.kt`**
   ```xml
    private fun showScreen() {
        object : CountDownTimer(3000, 1000) {
            override fun onTick(millisUntilFinished: Long) {

            }

            override fun onFinish() {
                val intent = Intent(applicationContext, MainActivity::class.java)
                startActivity(intent)
                finish()
            }

        }.start()
    }
   ```

3. **Clase predeterminada en `MainActivity.kt`**
   ```kotlin
   class MainActivity : AppCompatActivity() {
    override fun onCreate(savedInstanceState: Bundle?) {
        super.onCreate(savedInstanceState)
        enableEdgeToEdge()
        setContentView(R.layout.activity_main)
        ViewCompat.setOnApplyWindowInsetsListener(findViewById(R.id.main)) { v, insets ->
            val systemBars = insets.getInsets(WindowInsetsCompat.Type.systemBars())
            v.setPadding(systemBars.left, systemBars.top, systemBars.right, systemBars.bottom)
            insets
        }
    }
   ```

4. **Ejecuta el proyecto en Android Studio** y disfruta de la animación de inicio. 🚀

---

## 📩 Contacto
Si tienes alguna duda o sugerencia, no dudes en contactarme.

📧 Email: [sevargas](sevargas213@outlook.com)  
🐙 GitHub: [Svape](https://github.com/Enrique213-VP)  
🔗 LinkedIn: [Sergio](https://www.linkedin.com/in/svap/)

---

💡 **¡Dale ⭐ al repo si te fue útil!** 🎉

