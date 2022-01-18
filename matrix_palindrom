/*
Дана прямоугольная целочисленная матрица размера m строк и n
столбцов. Найти среди строк матрицы палиндромы, то есть строки, 
элементы которых читаются одинаково с начала и с конца.
*/

#include <iostream>
using namespace std;

class Matrix {
public:
	//создание динамической матрицы
	void createMatrix(int**& a, int m, int n) {
		a = new int* [m];
		for (int i = 0; i < m; i++) {
			a[i] = new int[n];
		}
	}

	//заполнение матрицы
	void fillingMatrix(int**& a, int m, int n) {
		srand(time(NULL));
		for (int i = 0; i < m; i++) {
			for (int j = 0; j < n; j++) {
				cin >> a[i][j];
			}
		}
	}

	//вывод матрицы
	void printMatrix(int** a, int m, int n) {
		for (int i = 0; i < m; i++) {
			for (int j = 0; j < n; j++) {
				cout << a[i][j] << " ";
			}
			cout << endl;
		}
	}

	//проверка на палиндром строки
	void palindrom_check(int** a, int m, int n){
		bool palindrom = true;

		for (int i = 0; i < m; i++) {
			for (int j = 0; j < n; j++)
					if (a[i][j] != a[i][n - j - 1])
						palindrom = false;
				
			if (palindrom) {
				for (int p = 0; p < n; p++)
					cout << a[i][p] << "\t";
				cout << endl;
			}
			palindrom = true;
		}
	}


};

int main() {
	Matrix x;
	int m, n;
	cout << "Enter the size for dynamic matrix(m, n): ";
	cin >> m >> n;
	int** a = NULL;

	x.createMatrix(a, m, n);
	x.fillingMatrix(a, m, n);
	cout << endl;
	x.printMatrix(a, m, n);
	cout << endl;
	x.palindrom_check(a, m, n);

	//зачистка динамических массивов
	for (int i = 0; i < m; i++) {
		delete[] a[i];
	}
	delete[] a;

	return 0;
}
