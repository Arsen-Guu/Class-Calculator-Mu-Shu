#include <iostream>
using namespace std;
class Parent {
private:
	float b;
	float a;
public:
	float GetA() {
		return a;
	}
	float GetB() {
		return b;
	}
	void SetA(float Mu) {
		a = Mu;
	}
	void SetB(float Shu) {
		b = Shu;
	}
	float Sum() {
		float sum = GetA() + GetB();
		cout << "Addition result: " << sum << endl;
		return sum;
	}
	float Sub() {
		float sub = GetA() - GetB();
		cout << "Subtraction result: " << sub << endl;
		return sub;
	}
	float Div() {
		float div = GetA() / GetB();;
		cout << "Division Result: " << div << endl;
		return div;
	}
	float Mul() {
		float mul = GetA() * GetB();
		cout << "The result of the multiplication: " << mul << endl;
		return mul;
	}
};
class Calculator: public Parent
{
public:
	float Div() {
		float div = GetA() / GetB();
		cout << "Result of whole division: " << div << endl;
		return div;
	}
	float DivRem() {
		float divrem = static_cast<int>(GetA()) % static_cast<int>(GetB());
		cout << "Result of division with remainder: " << divrem << endl;
		return divrem;
	}
};

	void main() {
		Parent First;
		Calculator Second;
		Second.SetA(5);
		Second.SetB(2);
		Second.Sum();
		Second.Sub();
		Second.Div();
		Second.Mul();
		Second.DivRem();
	}
