# exp.9
abstract class Shape{
    public int length,breadth;
    abstract public void Area();
};

class Rectangle extends Shape{
    Rectangle(int length,int breadth){
        super.length=length;
        super.breadth=breadth;
    }
    @Override
    public void Area(){
        System.out.println("the area of the Rectangle:"+(super.length*super.breadth));
    }
};

class Triangle extends Shape{
    Triangle(int heigth,int base){
        super.length=heigth;
        super.breadth=base;
    }
    @Override
    public void Area(){
        System.out.println("the area of the Triangle:"+(0.5*super.length*super.breadth));
    }
};

class Circle extends Shape{
    Circle(int radius){
        super.length=radius;
        //super.breadth=base;
    }
    @Override
    public void Area(){
        System.out.println("the area of the Circle:"+(3.14*super.length*super.length));
    }
};

class Main{
    public static void main(String[] args) {
        Shape rect=new Rectangle(10, 10);
        rect.Area();
        Shape tri=new Triangle(10, 10);
        tri.Area();
        Shape cir=new Circle(10);
        cir.Area();
    }
};
