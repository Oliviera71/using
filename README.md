
#include <iostream>
#include <string>
#include <cstdlib>
#include <ctime>

using namespace std;

// Function to generate random temperature in Celsius
double generateTemperature() {
    return -10.0 + static_cast<double>(rand()) / (static_cast<double>(RAND_MAX / 40.0));
}

int main() {
    const string cities[] = {"London", "Paris", "Berlin", "Rome", "Madrid"};
    const int numCities = sizeof(cities) / sizeof(cities[0]);

    srand(time(nullptr)); // Seed the random number generator with current time

    cout << "European Weather Forecast" << endl;

    for (int i = 0; i < numCities; ++i) {
        double temperature = generateTemperature();
        cout << cities[i] << ": " << temperature << "°C" << endl;
    }

    return 0;
}

