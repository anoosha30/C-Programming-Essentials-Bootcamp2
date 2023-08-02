# C++ Programming-Essentials-Bootcamp2
Assignment - C++ Programming Essentials Bootcamp

#include <iostream>
#include <string>

// Function to reverse a string
std::string reverseString(const std::string& str) {
    std::string reversedStr = str;
    int left = 0;
    int right = str.length() - 1;

    while (left < right) {
        // Swap characters at left and right indices
        char temp = reversedStr[left];
        reversedStr[left] = reversedStr[right];
        reversedStr[right] = temp;

        // Move the pointers towards the center
        left++;
        right--;
    }

    return reversedStr;
}

int main() {
    std::string inputString;

    // Prompt the user to enter a string
    std::cout << "Enter a string: ";
    std::getline(std::cin, inputString);

    // Call the reverseString function to reverse the string
    std::string reversedString = reverseString(inputString);

    // Display the reversed string
    std::cout << "Reversed string: " << reversedString << std::endl;

    return 0;
}
