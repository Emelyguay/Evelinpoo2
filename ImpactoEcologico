import java.util.ArrayList;

// Interfaz para el cálculo del impacto ecológico
interface ImpactoEcologico {
    double obtenerImpactoEcologico();
}

// Clase para representar un edificio
class Edificio implements ImpactoEcologico {
    private String nombre;
    private double emisionesPorMetroCuadrado;

    public Edificio(String nombre, double emisionesPorMetroCuadrado) {
        this.nombre = nombre;
        this.emisionesPorMetroCuadrado = emisionesPorMetroCuadrado;
    }

    @Override
    public double obtenerImpactoEcologico() {
        // Suponiendo un edificio de 600 m^2
        return 600 * emisionesPorMetroCuadrado;
    }

    public String toString() {
        return "Edificio: " + nombre;
    }
}

// Clase para representar un auto
class Auto implements ImpactoEcologico {
    private String modelo;
    private double emisionesPorKilometro;

    public Auto(String modelo, double emisionesPorKilometro) {
        this.modelo = modelo;
        this.emisionesPorKilometro = emisionesPorKilometro;
    }

    @Override
    public double obtenerImpactoEcologico() {
        // Suponiendo un recorrido promedio de 10000 km al año
        return 10000 * emisionesPorKilometro;
    }

    public String toString() {
        return "Auto: " + modelo;
    }
}

// Clase para representar una bicicleta
class Bicicleta implements ImpactoEcologico {
    private String tipo;
    private double emisionesPorKilometro;

    public Bicicleta(String tipo, double emisionesPorKilometro) {
        this.tipo = tipo;
        this.emisionesPorKilometro = emisionesPorKilometro;
    }

    @Override
    public double obtenerImpactoEcologico() {
        // Suponiendo un recorrido promedio de 5000 km al año
        return 5000 * emisionesPorKilometro;
    }

    public String toString() {
        return "Bicicleta: " + tipo;
    }
}

// Clase principal que utiliza las clases anteriores
public class Main {
    public static void main(String[] args) {
        // Crear objetos de cada clase con emisiones específicas de CO2
        Edificio edificio = new Edificio("Edificio A", 1000.0 / 600);  // 1000 kg de CO2 / 600 m^2
        Auto auto = new Auto("Toyota", 0.143);  // 143 gramos de CO2 por km
        Bicicleta bicicleta = new Bicicleta("De montaña", 0.021);  // 21 gramos de CO2 por km

        // Crear un ArrayList de ImpactoEcologico y agregar los objetos
        ArrayList<ImpactoEcologico> listaImpactoEcologico = new ArrayList<>();
        listaImpactoEcologico.add(edificio);
        listaImpactoEcologico.add(auto);
        listaImpactoEcologico.add(bicicleta);

        // Iterar a través de la lista e imprimir el impacto ecológico
        for (ImpactoEcologico elemento : listaImpactoEcologico) {
            System.out.println(elemento.toString() + " - Impacto ecológico: " + elemento.obtenerImpactoEcologico() + " kg de CO2");
        }
    }
}
