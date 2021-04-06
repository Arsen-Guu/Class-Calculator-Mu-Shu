# Class-Calculator-Mu-Shu
#include <iostream>
using namespace std;
class Parent {
protected:
	float b;
	float a;
public:
	float GetAandB() {
		return a;
		return b;
	}
	void SetAandB(float Mu, float Shu) {
		a = Mu;
		b = Shu;
	}
	float Sum() {
		float sum = a + b;
		cout << "Addition result: " << sum << endl;
		return sum;
	}
	float Sub() {
		float sub = a - b;
		cout << "Subtraction result: " << sub << endl;
		return sub;
	}
	float Div() {
		float div = a / b;;
		cout << "Division Result: " << div << endl;
		return div;
	}
	float Mul() {
		float mul = a * b;
		cout << "The result of the multiplication: " << mul << endl;
		return mul;
	}
};
class Calculator: public Parent
{
public:
	float Div() {
		float div = a / b;
		cout << "Result of whole division: " << div << endl;
		return div;
	}
	float DivRem() {
		float divrem = static_cast<int>(a) % static_cast<int>(b);
		cout << "Result of division with remainder: " << divrem << endl;
		return divrem;
	}
};

	void main() {
		Parent First;
		Calculator Second;
		Second.SetAandB(5, 2);
		Second.GetAandB();
		Second.Sum();
		Second.Sub();
		Second.Div();
		Second.Mul();
		Second.DivRem();
	}
