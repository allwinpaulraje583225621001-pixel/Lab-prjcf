#include <bits/stdc++.h>
using namespace std;

int getLastMoment(int n, vector<int>& left, vector<int>& right) {
    int lastTime = 0;

    // Ants moving to the left
    for (int pos : left) {
        lastTime = max(lastTime, pos);
    }

    // Ants moving to the right
    for (int pos : right) {
        lastTime = max(lastTime, n - pos);
    }

    return lastTime;
}

int main() {
    int n = 4;
    vector<int> left = {2};
    vector<int> right = {0, 1, 3};

    cout << getLastMoment(n, left, right) << endl; // Output: 4
    return 0;
}
