# 29PR
# 29 Практика
```
import java.util.Scanner;

public class RoadsCounter {
    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);

        int N = scanner.nextInt();

        if (N == 0) {
            System.out.println(0);
            return;
        }

        //Матрица смежности
        int[][] adjacencyMatrix = new int[N][N];
        for (int i = 0; i < N; i++) {
            for (int j = 0; j < N; j++) {
                adjacencyMatrix[i][j] = scanner.nextInt();
            }
        }

        int roadCount = 0;
        for (int i = 0; i < N; i++) {
            for (int j = i + 1; j < N; j++) { 
                if (adjacencyMatrix[i][j] == 1) {
                    roadCount++;
                }
            }
        }

        System.out.println(roadCount);
    }
}
```
