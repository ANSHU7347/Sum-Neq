#include <iostream>
#include <vector>
using namespace std;
int main() {
    int r;
    cin >> r;
    while (r > 0) {
        int p;
        cin >> p;
        vector<int> arr(p);
        for (int j = 0; j < p; j++) {
            int valuess;
            cin >> valuess;
            arr[j] = valuess;
        }

        bool sa = true;
        int fir = arr[0];
        for (int j = 1; j < p; j++) {
            if (arr[j] != fir)
                sa = false;
        }
        if (sa) {
            cout << "no" << endl;
        } else {
            if (p == 4) {
                if (arr[0] + arr[1] == arr[2] + arr[3]) {
                    cout << "no" << endl;
                } else {
                    cout << "YES" << endl;
                }
            } else {
                cout << "YES" << endl;
            }
        }
        r--;
    }
    return 0;
}
