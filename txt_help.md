

Solution

```
import java.math.BigDecimal;

public class Formula1RaceRunner {

    static BigDecimal calculateAverageSpeed(int numberOfCars, BigDecimal totalDistance, BigDecimal totalTime) {
        BigDecimal averageDistance = totalDistance.divide(new BigDecimal(numberOfCars), 2, BigDecimal.ROUND_HALF_UP);
        BigDecimal averageTime = totalTime.divide(new BigDecimal(numberOfCars), 2, BigDecimal.ROUND_HALF_UP);

        return averageDistance.divide(averageTime, 2, BigDecimal.ROUND_HALF_UP);
    }

    public static void main(String[] args) {
        int numberOfCars = 5;
        BigDecimal totalDistance = new BigDecimal("12000"); // in meters
        BigDecimal totalTime = new BigDecimal("720.5"); // in seconds

        BigDecimal averageSpeed = calculateAverageSpeed(numberOfCars, totalDistance, totalTime);

        System.out.println("Average speed for the Formula 1 cars: " + averageSpeed.setScale(1, BigDecimal.ROUND_HALF_UP) + " m/s");
    }
}
```

Test

