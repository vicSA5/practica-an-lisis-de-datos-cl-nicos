# 15/04/26-1
# ChatGPT
# acabo de emmpezar he abierto el dataset y no se por donde empezar, dime en general papra trabajos de este tipo (data science) como deberia enfocrarlo
# No sabía por donde empezar y le pregunté que me guiará en lo básico (como tratar missing values, variables inútiles etc)
#
# 15/04/26-2
# ChatGPT
# como tratar los missing values dependiendo de el procentaje sobre el total en el q aparece
# Lo usé para ver que hacer con las variables con missing values.
#
# 18/04/26-1
# ChatGPT
# como aplico one-hot encoding a este caso {captura de mi código}
# Me quería asegurar de que estaba aplicando bien el one-hot encoding de la primera variable que me encontré
#
# 18/04/26-2
# ChatGPT
# así está bien? {captura de mi código}
# Asegurarme de que estaba bien aplicado el one-hot encoding y además me hizo descubrir "drop_first=True" para evitar redunacia con las columnas nuevas.
#
# 18/04/26-3
# Deepseek
# explicame como funcionan los codigos ICD9
# Fui a la documentación del dataset y ponía que diag_1, 2 y 3 seguían este código
#
# 18/04/26-4
# ChatGPT
# para las variables diag_1, diag_2 y diag_3 que siguen el sistema de clasificación ICD9, estaría bien hacer one-hot encoding de estas pero "partiendo" por capítulos por ejemplo enfermedades vasculares que son de 390–459?
# Lo usé para que me dijera si es correcto este planteamiento, además me dió los códigos agrupados por sistemas y usé la parte más tediosa del código (los if-elif-else para ver que código es).
#
# 18/04/26-5
# ChatGPT
# me ha salido el siguiente error con la funcion de los diagnosticos {captura del código y el error}
# Me ayudó a debuggear ya que hice un for donde cambiaba datos de esta forma datos["diag_1"][i] = seleccionarDiagnostico(datos["diag_1"][i]) y me dijo q mejor usar .apply(funcion)
#
# 20/04/26-1
# ChatGPT
# esta variable habría q eliminarla no? {captura de value_counts()}
# Quería asegurarme si una variable poco representada habría que quitarla, además aprendí que si dentro de value_count() pones normalized="True" te devuelve la representación en porcentaje.
#
# 22/04/26-1
# Gemini
# es correcto este dataframe antes de pasar al EDA? {captura}
# Para ver si era correcto lo q llevaba. Me dijo que por si acaso, para que entienda mejor el modelo, convierta las variables booleanas del one-hot encoding a int.
#
# 23/04/26-1
# Gemini
# puedo usar este modelo para mi dataset? {captura del notebook de clase de LinearRegression}
# Validar si se podía usar lo mismo que vimos en clase, me ayudó a ajustar parámetros.
#
# 23/04/26-2
# Gemini
# puedo aplicar vecinos-k como aquí? {captura del notebook de la segunda clase}
# Validar si se podía usar lo mismo que vimos en clase, me ayudó a ajustar parámetros y que no tarde tanto en ejecutarse usando un parámetro para usar todos los núcleos del ordenador.
#
# 23/04/26-3
# DeepSeek
# no me va pip install imblearn
# Me ayudó a arreglar que al instalarme imblearn con pip seguía dando error dandome un ejecutable en una celda.
#
# 28/04/26-1
# Gemini
# ayudame a aplicar RFE y SelectKBest
# Para aprender a usar los métodos de selección.
#
# 28/04/26-2
# Gemini
# para comparar los 5 modelos de ahora sirve el test de wilcoxon de antes?
# Para no solo mirar la media del accuracy y demostrar que el Random Forest es mejor de verdad. Me ayudó a configurar el test con "alternative=greater" para probar que uno es superior al resto y no solo que son distintos.
#
# 28/04/26-3
# Gemini
# que variables son las mas importantes segun el modelo y que sentido tienen?
# Usamos la importancia de variables del Random Forest para sacar el Top 10. Me ayudó a ver la lógica médica de por qué cosas como el número de ingresos previos o la edad son los mejores predictores.
#
# 28/04/26-4
# Gemini
# como aplico SHAP y LIME
# Para aprender a usar estas librerías de explicabilidad.
#
#
# 28/04/26-5
# Gemini
# me da este error en el shap {captura}
# Debug de un error.
#
# 28/04/26-6
# Gemini
# como se lee un grafico de SHAP y para que sirve LIME?
# Para la parte de explicabilidad. Me enseñó a usar SHAP para ver el modelo en general y LIME para elegir a un paciente concreto y ver qué variables han hecho que el modelo diga que se va a volver a ingresar.




<!-- ALUCINACIONES -->
# DURANTE 18/04/26-4
❌ Posible error: orden de condiciones
Tu orden actual:

Circulatorio (390-459 o 785)

Respiratorio (460-519 o 786)

Digestivo (520-579 o 787)

Diabetes (250-251) ⬅️ ¡Esto nunca se ejecutará!
Problema: 250 es menor que 390, pero 250 NO está en ningún rango anterior... ¡espera! Sí está. 250 es menor que 390, entonces ninguna condición anterior lo captura. Está bien, el orden no afecta a 250 porque ningún rango anterior lo incluye.


