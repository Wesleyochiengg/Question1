#include <iostream>
#include <string>

class Car {
private:
    std::string brand;
    std::string model;
    float price;
    int mileage;

public:
    Car(std::string b, std::string m, float p, int mil) : brand(b), model(m), price(p), mileage(mil) {}

    void display() {
        std::cout << "Brand: " << brand << std::endl;
        std::cout << "Model: " << model << std::endl;
        std::cout << "Price: $" << price << std::endl;
        std::cout << "Mileage: " << mileage << " miles" << std::endl;
    }

    void drive(int distance) {
        mileage += distance;
        std::cout << "Updated Mileage: " << mileage << " miles" << std::endl;
    }
};

int main() {
    Car myCar("Toyota", "Corolla", 20000, 5000);
    myCar.display();
    myCar.drive(150);
    myCar.drive(300);
    return 0;
}
