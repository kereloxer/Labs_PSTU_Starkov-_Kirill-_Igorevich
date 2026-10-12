#include <iostream>
#include <cmath>
#include <iomanip>

using namespace std;

int main() {
    setlocale(LC_ALL, "Russian");

    cout << "=== Лабораторная работа №1 (Вариант 4) ===" << endl << endl;

    // --- Часть 1: Вычисление выражения ---
    // Формула: ((a + b)^3 - a^3) / (3*a*b^2 + b^3 + 3*a^2*b)
    
    // Вычисление для типа float
    float a_f = 1000.0f;
    float b_f = 0.0001f;
    
    float num_f = pow(a_f + b_f, 3) - pow(a_f, 3);
    float den_f = 3 * a_f * pow(b_f, 2) + pow(b_f, 3) + 3 * pow(a_f, 2) * b_f;
    float res_f = num_f / den_f;

    // Вычисление для типа double
    double a_d = 1000.0;
    double b_d = 0.0001;

    double num_d = pow(a_d + b_d, 3) - pow(a_d, 3);
    double den_d = 3 * a_d * pow(b_d, 2) + pow(b_d, 3) + 3 * pow(a_d, 2) * b_d;
    double res_d = num_d / den_d;

    cout << "1. Результаты вычисления выражения:" << endl;
    cout << "При float:  " << setprecision(8) << res_f << endl;
    cout << "При double: " << setprecision(8) << res_d << endl << endl;

    // --- Часть 2: Операции инкремента / декремента ---
    int n = 5;
    int m = 10;

    cout << "2. Результаты логических и арифметических выражений (при n=5, m=10):" << endl;
    
    // 1) n++ * m
    int n1 = n, m1 = m;
    int res1 = n1++ * m1;
    cout << "1) n++ * m = " << res1 << " (новое n = " << n1 << ")" << endl;

    // 2) n++ < m
    int n2 = n, m2 = m;
    bool res2 = n2++ < m2;
    cout << "2) n++ < m = " << (res2 ? "true (1)" : "false (0)") << " (новое n = " << n2 << ")" << endl;

    // 3) m-- > m
    int n3 = n, m3 = m;
    bool res3 = m3-- > m3; // Внимание: поведение зависит от порядка вычисления аргументов
    cout << "3) m-- > m = " << (res3 ? "true (1)" : "false (0)") << " (новое m = " << m3 << ")" << endl;

    return 0;
}
