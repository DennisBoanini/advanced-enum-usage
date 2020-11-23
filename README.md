`import java.util.function.BiFunction;
 
 public class Demo {
     private enum EOperation {
         ADD((x, y) -> x + y),
         SUBTRACT((x, y) -> x - y),
         MULTIPLY((x, y) -> x * y),
         DIVIDE((x, y) -> x / y);
 
         private final BiFunction<Integer, Integer, Integer> operation;
 
         EOperation(BiFunction<Integer, Integer, Integer> operation) {
             this.operation = operation;
         }
 
         public int applyOperation(int x, int y) {
             return this.operation.apply(x, y);
         }
     }
 
     public static void main(String[] args) {
         System.out.println("SUM: " + EOperation.ADD.applyOperation(3, 5));
         System.out.println("SUBTRACT: " + EOperation.SUBTRACT.applyOperation(3, 5));
         System.out.println("MULTIPLY: " + EOperation.MULTIPLY.applyOperation(3, 5));
         System.out.println("DIVIDE: " + EOperation.DIVIDE.applyOperation(3, 5));
     }
 }`