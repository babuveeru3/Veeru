# Veeru
Software Developer;
#include <stdio.h>
#include <stdlib.h>
#include <string.h>

// Function to calculate the sum of numbers in an array
int calculateSum(int numbers[], int size) {
    int sum = 0;
    for (int i = 0; i < size; i++) {
        sum += numbers[i];
    }
    return sum;
}

int main() {
    // Read data from a JSON file
    FILE* file = fopen("data.json", "r");
    if (file == NULL) {
        printf("Error opening file.\n");
        return 1;
    }
    char buffer[1024];
    fread(buffer, sizeof(buffer), 1, file);
    fclose(file);

    // Parse the JSON data
    // (Assuming you have a JSON parsing library available)
    // JSON parsing code goes here

    // Extract an array of numbers from the JSON data
    int numbers[] = {1, 2, 3, 4, 5};
    int size = sizeof(numbers) / sizeof(numbers[0]);

    // Calculate the sum of numbers
    int sum = calculateSum(numbers, size);

    // Print the result
    printf("Sum: %d\n", sum);

    return 0;
}

