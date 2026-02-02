import streamlit as st
import numpy as np
import matplotlib.pyplot as plt

# Título da aplicação
st.title("📈 Gráfico da Função de Segundo Grau")

st.write("Digite os valores dos coeficientes da função f(x) = ax² + bx + c")

# Entradas dos coeficientes
a = st.number_input("Coeficiente a (≠ 0)", value=1.0)
b = st.number_input("Coeficiente b", value=0.0)
c = st.number_input("Coeficiente c", value=0.0)

# Verificação se é função do 2º grau
if a == 0:
    st.error("O coeficiente 'a' deve ser diferente de zero para ser uma função do segundo grau.")
else:
    # Define a função quadrática
    def funcao_quadratica(x, a, b, c):
        return a * x**2 + b * x + c

    # Intervalo de x
    x_values = np.linspace(-10, 10, 400)
    y_values = funcao_quadratica(x_values, a, b, c)

    # Criação do gráfico
    fig, ax = plt.subplots(figsize=(9, 7))
    ax.plot(x_values, y_values, label=f'f(x) = {a}x² + {b}x + {c}')

    ax.set_title("Gráfico da Função de Segundo Grau")
    ax.set_xlabel("Eixo X")
    ax.set_ylabel("Eixo Y")
    ax.grid(True, linestyle='--', alpha=0.7)

    # Eixos cartesianos
    ax.axhline(0)
    ax.axvline(0)

    ax.legend()

    # Exibe o gráfico no Streamlit
    st.pyplot(fig)
