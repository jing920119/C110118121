```java


class CShape {
    private String color;

    public CShape(String color) {
        this.color = color;
    }

    public double getArea() {
        return 0.0;
    }
}

class CTriangle extends CShape {
    private double a, b, c;

    public CTriangle(String color, double a, double b, double c) {
        super(color);
        this.a = a;
        this.b = b;
        this.c = c;
    }

    @Override
    public double getArea() {
        // 計算並輸出三角形面積
        double s = (a + b + c) / 2;
        return Math.sqrt(s * (s - a) * (s - b) * (s - c));
    }
}

public class Main {
    public static void main(String[] args) {
        CTriangle redTriangle = new CTriangle("红色", 3.0, 4.0, 5.0);
        double area = redTriangle.getArea();
        System.out.println("三角形的顏色為: " + redTriangle.color);
        System.out.println("三角形的面積為: " + area);
    }
}

```
