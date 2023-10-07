# proyecto


package proyectoFinal; 

import java.util.Scanner; 

public class ProyectoFinal { 

 

double coords [] = new double [4];	 

 

Scanner teclado = new Scanner(System.in); 

Scanner teclado2 = new Scanner(System.in); 

 

String apicultor1; 

String apicultor2; 

String apicultor3; 

 

String cedulaApi; 

 

String cedula2; 

String ciudad1; 

String ciudad2; 

String ciudad3; 

String ciudad4; 

String ciudad5; 

  

String marron="\u001B[38;5;130m"; 

 String rojo="\u001B[31m"; 

 String verde="\u001B[32m"; 

 String comun="\u001B[0m"; 

 

 

public void menuPrincipal(){ 

System.out.println("Menú Principal"); 

System.out.println ("Elija acción a realizar"); 

System.out.println ("1. Ir a Apicultor"); 

System.out.println("2. Ir a ciudad"); 

System.out.println("3. Ir a Colmenar"); 

System.out.println ("4. Ir a Centro de Extracción"); 

System.out.println("5. Ir a Tramo"); 

System.out.println("6. Ir a Estadísticas"); 

 

int opcion=teclado.nextInt(); 

 

switch (opcion) { 

 

case 1: 

menuApicultor(); 

break; 

 

case 2: 

menuCiudad(); 

break; 

 

case 3: 

menuColmenar(); 

break; 

 

case 4: 

menuCentroDeExtraccion(); 

break; 

 

case 5: 

menuTramo(); 

break; 

 

case 6: 

menuEstadisticas(); 

break; 

 

default: 

System.out.println("ERROR. No se encontró esa opción en la base de datos"); 

menuPrincipal(); 

break; 

} 

} 

 

public void menuApicultor(){ 

int opcion; 

 

do { 

System.out.println("Menú Apicultor"); 

System.out.println("Elija la accion que desea realizar"); 

System.out.println("1. Volver a menú principal"); 

System.out.println("2. Registrar Apicultor"); 

System.out.println("3. Ver listado de apicultores"); 

System.out.println("4. Modificar"); 

System.out.println ("5. Buscar"); 

System.out.println ("6. Eliminar"); 

System.out.println ("7. salir"); 

 

opcion=teclado.nextInt(); 

 

switch (opcion) { 

 

case 1: 

menuPrincipal(); 

break; 

 

case 2: 

registrarApicultor(); 

break; 

 

case 3: 

listadoDeApicultores(); 

break; 

 

case 4: 

System.out.println ("Modificar apicultor"); 

System.out.println("En construcción…"); 

break; 

 

case 5: 

System.out.println ("Buscar apicultor"); 

System.out.println("En construcción…"); 

break; 

 

case 6: 

System.out.println("Eliminar Apicultor"); 

System.out.println("En construcción…"); 

break; 

 

case 7: 

System.out.println("Hasta Pronto"); 

System.exit(opcion); 

break; 

 

default: 

System.out.println("ERROR. No se encontró esa opción en la base de datos "); 

menuApicultor(); 

break; 

} 

}while(opcion !=10); 

} 

 

 

public void registrarApicultor() { 

 

 

String nombre; 

String direccion;  

String ciudad; 

String departamento; 

String email; 

int telefono; 

int añoDeRegistro; 

 

System.out.println("Por favor, llenar el siguiente formulario para ser registrado:"); 

 

do {  

System.out.println("Ingrese su cedula"); 

cedulaApi = teclado2.nextLine(); 

} while (cedulaApi.length()< 8 ); 

 

do {  

System.out.println("Ingrese su nombre"); 

nombre = teclado2.nextLine(); 

} while (nombre.length()<2); 

 

do { 

System.out.println("Ingrese su direccion"); 

direccion = teclado2.nextLine(); 

} while (direccion.length() < 4); 

 

do { 

System.out.println("Ingrese su ciudad"); 

ciudad = teclado2.nextLine(); 

} while (ciudad.length() < 3); 

 

do { 

System.out.println("Ingrese su departamento"); 

departamento = teclado2.nextLine(); 

} while (departamento.length() < 4 ); 

 

do { 

System.out.println("Ingrese su email"); 

email = teclado2.nextLine(); 

} while (email.length() < 4); 

 

do { 

System.out.println("ingrese su numero de telefono"); 

telefono = teclado.nextInt(); 

} while (telefono < 9); 

 

do { 

System.out.println("Ingrese su año de registro"); 

añoDeRegistro = teclado.nextInt(); 

} while (añoDeRegistro < 0); 

 

System.out.println("Se registraron sus datos correctamente"); 

 

 

 

if(apicultor1 == null) { 

 apicultor1 = nombre+ "#" +cedulaApi+ "#" +direccion+ "#" +ciudad+ "#" +departamento+ "#" +email+ "#" +telefono+ "#" +añoDeRegistro; 

}	 

else if (apicultor2 == null) 

 apicultor2 = nombre+ "#" +cedulaApi+ "#" +direccion+ "#" +ciudad+ "#" +departamento+ "#" +email+ "#" +telefono+ "#" +añoDeRegistro; 

 

else if (apicultor3 == null) 

 apicultor3 = nombre+ "#" +cedulaApi+ "#" +direccion+ "#" +ciudad+ "#" +departamento+ "#" +email+ "#" +telefono+ "#" +añoDeRegistro; 

} 

 

 

public void listadoDeApicultores(){ 

System.out.println(apicultor1); 

System.out.println(apicultor2); 

System.out.println(apicultor3); 

} 

 

 

 

 

public void menuCiudad(){ 

 

System.out.println("Menú Ciudad"); 

System.out.println("Elija acción a realizar "); 

System.out.println("1. Volver a menú Ciudad"); 

System.out.println("2. Registrar Ciudad"); 

System.out.println("3. Modificar Ciudad"); 

System.out.println("4. Buscar Ciudad"); 

System.out.println("5. Eliminar Ciudad"); 

 

int opcion=teclado.nextInt(); 

 

switch (opcion) { 

case 1: 

menuPrincipal(); 

break; 

 

case 2: 

System.out.println("Registrar Ciudad"); 

registrarCiudad(); 

break; 

 

case 3: 

System.out.println("Mostrar Ciudad"); 

System.out.println("En construcción…"); 

menuCiudad(); 

break; 

 

case 4: 

System.out.println ("Buscar ciudad"); 

System.out.println("En construcción…"); 

menuCiudad(); 

break; 

 

case 5: 

System.out.println("Eliminar Ciudad"); 

System.out.println("En construcción…"); 

menuCiudad(); 

break; 

 

default: 

System.out.println( "ERROR. No se encontró esa opción en la base de datos"); 

menuCiudad(); 

break; 

} 

} 

 

 

public void registrarCiudad() { 

 

 

double coordx; 

double coordy; 

String ciudad; 

 

 

do { 

System.out.println("Ingrese nombre de la ciudad"); 

ciudad= teclado.nextLine(); 

} while (ciudad.length() < 2);  

 

System.out.println("Ingrese coordenada X"); 

coordx = teclado.nextDouble(); 

 

 

System.out.println("Ingrese coordenada Y"); 

coordy =teclado.nextDouble(); 

 

 

for (int poscoord=0; poscoord < coords.length; poscoord= poscoord +2) { 

 

coords [poscoord]= coordx; 

poscoord++; 

coords [poscoord]= coordy; 

poscoord++; 

 

if (Double.compare(coords[poscoord], coordx)== 0 && Double.compare(coords[poscoord+1], coordy)==0 ) { 

 

System.out.println (rojo+ "ERROR" +comun); 

 

} else { 

 

System.out.println (verde+ "Ok" +comun); 

} 

} 

 

 

} 

 

 

 

 

 

 

public void preCargarCiudad() { 

 

 

ciudad1 = "13131#2211313#Montevideo";  

 

ciudad2 = "238342#347789789#Flores";  

  

ciudad3 = "5478956#547896#Canelones";  

 

ciudad4 = "54785478#567347#Tacuarembo";  

 

 

 

} 

 

 

public void menuColmenar(){ 

System.out.println("Menú Colmenar "); 

System.out.println ("Elija accion a realizar"); 

System.out.println ("1. Volver al menú principal"); 

System.out.println("2. Registrar Colmenar "); 

System.out.println("3. Modificar Colmenar "); 

System.out.println ("4. Buscar Colmenar"); 

System.out.println ("5. Eliminar Colmenar "); 

int opcion=teclado.nextInt(); 

 

switch (opcion) { 

 

case 1: 

menuPrincipal(); 

break; 

 

case 2: 

System.out.println("Registrar Colmenar"); 

registrarColmenar(); 

break; 

 

case 3: 

System.out.println("Mostrar Colmenar"); 

System.out.println("En construcción…"); 

menuColmenar(); 

break; 

 

case 4: 

System.out.println ("Buscar Colmenar"); 

System.out.println("En construcción…"); 

menuColmenar(); 

break; 

 

case 5: 

System.out.println ("Eliminar Colmenar"); 

System.out.println( "En construcción…"); 

menuColmenar(); 

break; 

 

default: 

System.out.println("ERROR. No se encontró esa opción en la base de datos"); 

menuColmenar(); 

break; 

} 

} 

 

public void registrarColmenar() { 

 

double coordX;  

double coordY;  

String apicultor;  

 int capacidad;  

 

/*	int cedulasC [] = new int [10]; 

 

cedulasC[0]= 57648795; 

cedulasC[1]= 20954678; 

cedulasC[2]= 28529685; 

cedulasC[3]= 20934678; 

cedulasC[4]= 97866363; 

*/ 

 

String aux1[]= apicultor1.split("#"); 

String aux2[]= apicultor2.split("#"); 

String aux3[]= apicultor3.split("#"); 

 

 

do { 

System.out.println("Ingrese cedula de el Apicultor: "); 

apicultor= teclado2.nextLine(); 

 

if (apicultor.compareTo(aux1[1])==0) { 

 

System.out.println("Las cedulas coinciden"); 

} 

System.out.println("Ingrese la cantidad de miel que se estrae de el colmenar por mes: " +comun); 

capacidad = teclado.nextInt();  

 

if (capacidad ==0) { 

System.out.println(rojo+ "ERROR. La capacidad del colmenar no puede ser menor a 0" +comun ); 

System.out.println("Ingrese la cantidad de miel que se estrae de el colmenar por mes: " +comun); 

capacidad = teclado.nextInt();  

 

} else if (capacidad != 0) { 

System.out.println( verde+ "Ok"+comun); 

 

} while (apicultor.length() < 2); 

 

 

 

if (apicultor.compareTo(aux2[1])==0) { 

 

System.out.println("Las cedulas coinciden"); 

} 

System.out.println("Ingrese la cantidad de miel que se estrae de el colmenar por mes: " +comun); 

capacidad = teclado.nextInt();  

 

if (capacidad ==0) { 

System.out.println(rojo+ "ERROR. La capacidad del colmenar no puede ser menor a 0" +comun ); 

System.out.println("Ingrese la cantidad de miel que se estrae de el colmenar por mes: " +comun); 

capacidad = teclado.nextInt();  

 

} else if (capacidad != 0) { 

System.out.println( verde+ "Ok"+comun); 

 

 

} while (apicultor.length() < 2);  

 

 

 

if (apicultor.compareTo(aux3[1])==0) { 

 

System.out.println(verde+ "Las cedulas coinciden"+ comun); 

} 

System.out.println("Ingrese la cantidad de miel que se estrae de el colmenar por mes: " +comun); 

capacidad = teclado.nextInt();  

 

if (capacidad ==0) { 

System.out.println(rojo+ "ERROR. La capacidad del colmenar no puede ser menor a 0" +comun ); 

System.out.println("Ingrese la cantidad de miel que se estrae de el colmenar por mes: " +comun); 

capacidad = teclado.nextInt();  

 

} else if (capacidad != 0) { 

System.out.println( verde+ "Ok"+comun); 

} 

 

} while (apicultor.length() < 2);  

 

 

 

/*	for (int casillaC=0; casillaC < cedulasC.length; casiila) 

System.out.println("Usted ya esta registrado en el programa"); 

} else { 

System.out.println(rojo+ "ERROR. esta cedula no esta registrada en el sistema"+ comun); 

}*/ 

 

 

 

for (int poscoord=0; poscoord < coords.length; poscoord= poscoord +2) { 

 

System.out.println("Ingrese coordenada X del Colmenar: "); 

coordX = teclado.nextInt(); 

 

 

System.out.println("Ingrese coordenada Y del Colmenar: "); 

coordY =teclado.nextInt(); 

 

 

coords [poscoord]= coordX; 

poscoord++; 

coords [poscoord]= coordY; 

poscoord++; 

if (coords[poscoord] == coords[poscoord]+2) { 

System.out.println (rojo+ "ERROR" +comun); 

 

}  

if (coords[poscoord] != coords[poscoord]+2){  

System.out.println (verde+ "Ok" +comun); 

} 

} 

 

 

System.out.println( "#" +apicultor+ "#"+ coords+ "#" + capacidad); 

 

 

 

} 

 

public void menuCentroDeExtraccion(){ 

 

System.out.println("Menú Centro de Extracción "); 

System.out.print ("Elija accion a realizar"); 

System.out.println("1. Volver al menú principal"); 

System.out.println("2. Registrar Centro de Extracción"); 

System.out.println("3. Modificar Centro de Extracción "); 

System.out.println("4. Buscar Centro de Extracción "); 

System.out.println("5. Eliminar Centro de Extracción "); 

 

int opcion=teclado.nextInt(); 

 

switch (opcion) { 

case 1: 

menuPrincipal(); 

break; 

 

case 2: 

System.out.println("Registrar Centro de extracción"); 

System.out.println("En construcción…"); 

menuCentroDeExtraccion(); 

break; 

 

case 3: 

System.out.println("Mostrar Centro de extracción"); 

System.out.println("En construcción…"); 

menuCentroDeExtraccion(); 

break; 

 

case 4: 

System.out.println ("Buscar Centro de extracción"); 

System.out.println( "En construcción…"); 

menuCentroDeExtraccion(); 

break; 

 

case 5: 

System.out.println ("Eliminar Centro de Extracción"); 

System.out.println( "En construcción…"); 

menuCentroDeExtraccion(); 

break; 

 

default: 

System.out.println( "ERROR. No se encontró esa opción en la base de datos"); 

menuCentroDeExtraccion(); 

break; 

} 

} 

 

public void menuTramo(){ 

 

System.out.println("Menú Tramo"); 

System.out.println("Elija accion a realizar"); 

System.out.println("1. Volver al menú principal "); 

System.out.println("2. Registrar Tramo "); 

System.out.println("3. Modificar Tramo"); 

System.out.println("4. Buscar Tramo"); 

System.out.println ("5. Eliminar Tramo"); 

 

int opcion=teclado.nextInt(); 

switch (opcion) { 

case 1: 

menuPrincipal(); 

break; 

 

case 2: 

System.out.println("Registrar Tramo"); 

System.out.println("En construcción…" ); 

menuTramo(); 

break; 

 

case 3: 

System.out.println("Mostrar Tramo"); 

System.out.println("En construcción…"); 

menuTramo(); 

break; 

 

case 4: 

System.out.println("Buscar Tramo"); 

System.out.println("En construcción…"); 

menuTramo(); 

break; 

 

case 5: 

System.out.println ("Eliminar Tramo"); 

System.out.println( "En construcción…"); 

menuTramo(); 

break; 

 

default: 

System.out.println("ERROR. No se encontro esa opcion en la base de datos"); 

menuTramo(); 

break; 

} 

} 

 

public void menuEstadisticas(){ 

 

System.out.println("Menú Estadística"); 

System.out.println("Elija accion a realizar"); 

System.out.println("1. Volver al menú principal"); 

System.out.println("2. Registrar Estadística "); 

System.out.println("3. Modificar Estadística"); 

System.out.println("4. Buscar Estadística"); 

System.out.println("5. Eliminar Estadística"); 

 

int opcion=teclado.nextInt(); 

 

switch (opcion) { 

case 1: 

menuPrincipal(); 

break; 

 

case 2: 

System.out.println("Registrar Estadística"); 

registrarCentroDeExtraccion(); 

break; 

 

case 3: 

System.out.println("Mostrar Estadística"); 

System.out.println("En construcción…"); 

break; 

 

case 4: 

System.out.println("Buscar Estadística"); 

System.out.println("En construcción…"); 

break; 

 

case 5: 

System.out.println("Eliminar Estadística"); 

System.out.println("En construcción…"); 

break; 

 

default: System.out.println("ERROR. No se encontro esa opcion en la base de datos"); 

menuEstadisticas(); 

break; 

} 

} 

 

public void registrarCentroDeExtraccion() { 

 

 

int doblecoord [] = new int [10]; 

 

double coordXX;  

double coordYY;  

int capacidades; 

  

for (int casilla =0; casilla< doblecoord.length; casilla++ ) {	 

 

 

System.out.println("Ingrese coordenada X del Centro de Extraccion: "); 

coordXX = teclado.nextDouble(); 

 

 

 

 

} 

 

for (int casilla =0; casilla< doblecoord.length; casilla++ ) {	 

 

} 

System.out.println("Ingrese coordenada Y del Centro de Extraccion: "); 

coordYY = teclado.nextDouble(); 

 

 

 

 System.out.println("Ingrese la capacidad de produccion de miel por mes: "); 

capacidades= teclado.nextInt(); 

 

if (capacidades <0) { 

System.out.println(rojo+" ERROR. La capacidadad no puede ser menor a 0"+comun); 

 

} else if (capacidades >=0) { 

System.out.println(verde +"Ok" +comun); 

} 

 

 

} 

 

public static void main(String[] args) { 

ProyectoFinal nombre = new ProyectoFinal (); 

nombre.preCargarCiudad(); 

nombre.menuPrincipal(); 

} 

} 

 
