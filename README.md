# parcial1algoritmos
Algoritmo DistribucionSeguro
    Definir suma_asegurada, aseguradora, socios, socio_especial Como Real
	
    Escribir "Ingrese la suma asegurada: "
    Leer suma_asegurada
	
    Si suma_asegurada <= 100000 Entonces
        aseguradora = suma_asegurada * 0.8
        socios = suma_asegurada * 0.2 / 2
    Sino
        Si suma_asegurada > 100000 Y suma_asegurada < 120000 Entonces
            aseguradora = 100000 * 0.8
            socios = 100000 * 0.2 / 2
            resto = suma_asegurada - 100000
            socios = socios + resto / 2
        Sino
            aseguradora = 100000 * 0.8
            socios = 100000 * 0.2 / 2
            resto = suma_asegurada - 120000
            aseguradora = aseguradora + 20000 * 0.8
            socios = socios + 20000 * 0.2 / 2
            socio_especial = resto
        Fin Si
    Fin Si
	
    Escribir "La aseguradora recibe: ", aseguradora
    Escribir "Los socios reciben: ", socios , " cada uno"
    Escribir "El socio especial recibe: ", socio_especial
    
FinAlgoritmo
