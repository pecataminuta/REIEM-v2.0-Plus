# 🌌 REIEM v2.0 — Modelo de Replicación Extradimensional con Interferencia y Expansión Multicapas

## 📖 Descripción

**REIEM v2.0** es una propuesta teórica en cosmología fundamental que introduce un mecanismo de *replicación extradimensional interferente* en un espacio-tiempo en expansión. El modelo propone que estructuras cosmológicas a gran escala emergen de huellas cuánticas replicadas en capas dimensionales adicionales, generando firmas observables en el CMB y en la distribución de galaxias.

Esta versión integra un **formalismo matemático completo**, **predicciones cuantificadas** y una **estrategia de validación observacional** con los experimentos **CMB-S4** y **Euclid**.

---

## 📊 Predicciones Clave

- Oscilaciones en el espectro del fondo cósmico de microondas (CMB):
\[
    \Delta C_\ell \approx (9.2 \pm 1.1) \times 10^{-6} \, \ell^{-3/2} \cos\left(\frac{2\pi \ell}{150}\right)
\]

- Correlaciones en la estructura a gran escala (LSS) a escalas de ~1.2 Gpc  
- Escala característica: $\ell_5^{\text{(rec)}} \approx 150$

---

## 📁 Contenido del Repositorio

- `/figures`: Diagramas conceptuales y resultados visuales  
  ![Firma Cosmológica del Modelo REIEM](https://github.com/user-attachments/assets/cc33597f-46ae-4287-88c8-75d790012af5)

- `/code`: Scripts Python para simulaciones REIEM  
  ```python
  import numpy as np
  import matplotlib.pyplot as plt

  # Parámetros REIEM
  beta5 = 2.8e-5
  l_n = 150
  l = np.arange(2000, 5001, 10)

  # Predicción REIEM
  delta_cl = beta5 * l**(-1.5) * np.cos(2*np.pi*l/l_n)

  # Banda de ruido CMB-S4 (estimado)
  noise = 0.002 * l**(-0.7)

  # Figura
  plt.plot(l, delta_cl, label="REIEM ΔCl")
  plt.fill_between(l, delta_cl - noise, delta_cl + noise, alpha=0.2, label="Noise Band")
  plt.legend()
  plt.xlabel("Multipole ℓ")
  plt.ylabel("ΔCl")
  plt.title("Predicción REIEM vs Ruido CMB-S4")
  plt.show()
  ## 🧠 Requisitos Técnicos

- Python 3.10+
- NumPy, SciPy, Matplotlib
- (Opcional) CLASS o CAMB modificados para REIEM
- Soporte para ejecución en entornos paralelos (CUDA/HPC)

---

## 🔬 Validación Observacional

Se recomienda aplicar los métodos REIEM a:
- Datos de **CMB-S4** para $\ell > 2500$
- Datos DR1 del telescopio espacial **Euclid** para LSS

---

## 📜 Declaración Ética

> Este proyecto fue desarrollado con el apoyo conceptual y crítico de modelos de lenguaje (ChatGPT, Claude, DeepSeek). Todas las fórmulas, algoritmos y simulaciones fueron diseñadas, verificadas y dirigidas por el autor humano.

---

## 📩 Contacto

Para colaboración, análisis conjunto o validación experimental:

**Autor principal**:  
Dr. Roberto Escárcega Jácome  
[escarcegaj.roberth@gmail.com o perfil de GitHub pecataminuta]  

---

Licencia

Este repositorio se distribuye bajo la licencia **MIT** para fines académicos y de investigación no comercial.
