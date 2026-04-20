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








<!-- ALUCINACIONES -->
# DURANTE 18/04/26-4
❌ Posible error: orden de condiciones
Tu orden actual:

Circulatorio (390-459 o 785)

Respiratorio (460-519 o 786)

Digestivo (520-579 o 787)

Diabetes (250-251) ⬅️ ¡Esto nunca se ejecutará!
Problema: 250 es menor que 390, pero 250 NO está en ningún rango anterior... ¡espera! Sí está. 250 es menor que 390, entonces ninguna condición anterior lo captura. Está bien, el orden no afecta a 250 porque ningún rango anterior lo incluye.


