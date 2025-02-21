
 
    public class CalculadoraContable {

    public static void main(String[] args) {
        // Datos de entrada
        double dolares1Cantidad = 10000;
        double dolares1Cotizacion = 1230;
        double dolares2Cantidad = 50000;
        double dolares2Cotizacion = 1300;
        double realesCantidad = 2500;
        double realesCotizacion = 5.70;
        double cuentasPorPagar = 124685750;

        // Cálculos
        double arsDolares1 = dolares1Cantidad * dolares1Cotizacion;
        double arsDolares2 = dolares2Cantidad * dolares2Cotizacion;
        double arsReales = realesCantidad * realesCotizacion;
        double totalPagado = arsDolares1 + arsDolares2 + arsReales;
        double chequeCaja = totalPagado / 2;
        double totalCompra = totalPagado + cuentasPorPagar;

        // Mostrar resultados
        System.out.println("Total en USD (ARS): " + (arsDolares1 + arsDolares2) + " ARS");
        System.out.println("Total en Reales (ARS): " + arsReales + " ARS");
        System.out.println("Pago con Cheque/Caja: " + chequeCaja + " ARS");
        System.out.println("Cuentas por Pagar: " + cuentasPorPagar + " ARS");
        System.out.println("Total de la Compra: " + totalCompra + " ARS");
    }
}
