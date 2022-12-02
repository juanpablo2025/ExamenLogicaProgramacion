package examen;

import java.util.Scanner;

/**
 *
 * @Juan Pablo Avendaño y Stefani Lopez
 */
public class Examen {

{

    /**
     * @param args the command line arguments
     */
    public static void main(String[] args) {
        
        Scanner a = new Scanner(System.in);
	String nombre = "", sexo = "", secc="";
        int edad=0,edadt=0, mujeres=0,n;  
	double salaHora = 0, horatra = 0,salarios=0,retencion=0,retenciont=0;
	System.out.print("Ingresar el numero de registros: ");
        n = a.nextInt();
        for (int i = 1; i <= n; i++) 
        {
	System.out.print("Ingresar nombre del trabajador: ");
	nombre = a.next();
        System.out.print("Ingresar sexo del trabajador(f o M):");
	sexo= a.next();
        System.out.print("Ingresar edad:");
	edad = a.nextInt();
        System.out.print("Ingresar sección( 'P'= planta, 'S' = Seguridad, 'T'= Tecnología e Informatica, 'A' = Adminitrativo: ");
	secc = a.next();
        System.out.print("Ingresar valor de la hora: ");
	salaHora = a.nextDouble();
	System.out.print("Ingresar horas trabajadas: ");
	horatra = a.nextDouble();
				
        double salario=horatra*salaHora;
        retencion = 0.07*salario;
       
        System.out.println("\n nombre:"+nombre + "\n Salario : " + salario + "\n Retención: " + retencion + "\n");
        
        if(edad >=50)
        {
            edadt++; 
        }
        if(secc.equals("s"))
        {
            salarios =+salario; 
        }
        if(sexo.equals("f")&& secc.equals("t"))
        {
            mujeres++; 
        }
         if(secc.equals("A"))
        {
            retenciont=+retencion;
        }
    }
        System.out.println( "Numero de Empleados mayores a 50 años:"+ edadt);
        System.out.println( "Total de Dinero pagado a empleados de Seguridad:"+ salarios);
        System.out.println( "Total de mujeres laborando en Tecnologia e informatica:"+ mujeres); 
        System.out.println( "Total de retencion en la fuente de los adminitrativos:"+ retencion);  
       
            
    
    }
}