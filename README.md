# Different-Weights
Let's define a split of n as a nonincreasing sequence of positive integers, the sum of which is n. For example, the following sequences are splits of 8 : [4, 4], [3, 3, 2], [2, 2, 1, 1, 1, 1], [5, 2, 1] The following sequences aren't splits of 8: [1, 7], [5, 4], [11, −3], [1, 1, 4, 1, 1] 


#include <iostream>
#include <unordered_set>

int main() {
    int n;
    std::cin >> n;
    std::unordered_set<int> uniqueWeights;

    for (int i = 1; i <= n / 2; ++i) {
        uniqueWeights.insert(n - i);
    }

    int result = uniqueWeights.size() + 1;
    std::cout << result << std::endl;

    return 0;
}
