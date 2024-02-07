# M-quina_de_Galton.py
.
import numbers as np
import matplotlib.pyplot as plt

def simular_maquina_galton(canicas, niveles):
    contadores = [0] * (niveles + 1)

#Iniciar contadores para cada contenedor 
    for _ in range(canicas):
        nivel = 0

#Comenzar en el nivel superior 
        for _ in range(niveles):

#Realizar 12 decisiones de izquierda o derecha
            if np.random.rand() < 0.5:

#Decidir aleatoriamente hacia donde cae la canica 
                nivel += 1
                contadores[nivel] += 1

#Incrementar el contador del contenedor correspondiente
                return contadores
            def graficar_histograma(contadores):
                plt.bar(range(len(contadores)), contadores, align='center')   
                plt.xlabel('contenedores')
                plt.ylabel('cantidad de canicas')
                plt.title('distribución de canicas en la máquina de galton')
                plt.show()
            if __name__ == "__main__":
                canicas = 3000
                niveles = 12
                resultados = simular_maquina_galton(canicas, niveles)
                graficar_histograma(resultados)
