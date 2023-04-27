//Maquina expendedora de cafe PCN Solutions//
Proceso Maquina_Expendedora_Cafe
	
	Definir opcion, total, pago, cambio Como Entero
	Definir respuesta Como Caracter
	
	Repetir
		total <- 50
		Escribir "Bienvenido a la Maquina Expendedora de Cafe!"
		Escribir "Por favor seleccione el tipo de cafe que desea:"
		Escribir "1. Cafe Expreso DOP50"
		Escribir "2. Capuccino DOP50"
		Escribir "3. Capuccino Italiano DOP50"
		Escribir "4. Caramel Capuccino DOP50"
		Escribir "5. Capuccino Suizo DOP50"
		
		Leer opcion
		
		Segun opcion Hacer
			1:
				Escribir "Ha seleccionado Cafe Expreso."
			2:
				Escribir "Ha seleccionado Capuccino."
			3:
				Escribir "Ha seleccionado Capuccino Italiano."
			4:
				Escribir "Ha seleccionado Caramel Capuccino."
			5:
				Escribir "Ha seleccionado Capuccino Suizo."
			De Otro Modo:
				Escribir "Opcion invalida, por favor seleccione una opcion valida."
				Esperartecla
			Fin Segun
			
			Escribir "El costo del cafe seleccionado es de $50 pesos."
			Escribir "Por favor ingrese la cantidad de dinero que desea pagar:"
			
			Leer pago
			
			Mientras pago < total Hacer
				Escribir "El pago ingresado es insuficiente, por favor ingrese una cantidad mayor o igual a $50 pesos."
				Leer pago
			Fin Mientras
			
			cambio <- pago - total
			
			Si cambio >= 50 Entonces
				Escribir "Gracias por su compra. El cafe seleccionado sera dispersado en breve."
				Escribir "Su cambio es de $", cambio  " pesos."
				Escribir "¿Desea continuar comprando? (S/N)"
				Leer respuesta
				Si respuesta = "S" Entonces
					Esperartecla
					Borrarpantalla
					costo=50
					cambio = pago - costo
					Escribir "Gracias por su compra. Su cambio es de ", cambio, " pesos."
				Sino
					Escribir "Retire su cambio de $", cambio " pesos. Gracias por su compra."
					Esperartecla
				Fin Si
			Sino
				Escribir "Gracias por su compra. El cafe seleccionado sera dispensado en breve."
			Fin Si
			
		Hasta Que respuesta = "N"
		
		
		
FinProceso
