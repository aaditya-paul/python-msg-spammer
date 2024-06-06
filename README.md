# PyAutoGUI Script

This repository contains a Python script that automates typing and keyboard actions using the `pyautogui` library. The script includes different functionalities such as typing from a file, continuous custom typing, and copying and pasting text.

## Features

- **Typing from a File**: Reads content from a file and types each word, pressing "Enter" after each word.
- **Custom Typing**: Continuously types a custom message and presses "Enter".
- **Copy and Paste**: Continuously pastes text from the clipboard and presses "Enter".

## Installation

1. **Clone the Repository**

    ```sh
    git clone https://github.com/your-username/your-repository.git
    cd your-repository
    ```

2. **Install Dependencies**

    Ensure you have Python installed. Then, install the required Python library:

    ```sh
    pip install pyautogui
    ```

## Usage

1. **Typing from a File**

    Uncomment the following section in the script to read and type from a file:

    ```python
    f = open("spam.txt", 'r') 
    # f = open("OIP.jpg", 'r')  # Example of another file

    for word in f:
        pyautogui.typewrite(word)
        pyautogui.press("enter")
        time.sleep(0.1)
    f.close()
    ```

2. **Custom Typing**

    Uncomment the following section to continuously type a custom message:

    ```python
    while True:
        pyautogui.typewrite(":3")
        pyautogui.press("enter")
        time.sleep(0.1)
    ```

3. **Copy and Paste**

    Uncomment one of the following sections to continuously paste text from the clipboard:

    ```python
    while True:
        pyautogui.keyDown('ctrl')
        pyautogui.keyDown("v")
        pyautogui.keyUp('ctrl')
        pyautogui.keyUp('v')
        time.sleep(0.1)
        pyautogui.press("enter")
        time.sleep(0.1)
    ```

    ```python
    while True:
        pyautogui.keyDown('ctrl')
        pyautogui.keyDown("v")
        time.sleep(0.5)
        pyautogui.press("enter")
        time.sleep(0.5)
    ```

## Notes

- **Safety**: Be cautious when running scripts that automate keyboard actions. Ensure you have control over stopping the script to avoid unwanted behavior.
- **Sleep Time**: Adjust the `time.sleep()` duration as needed to match your requirements.

## License

This project is licensed under the MIT License. See the [LICENSE](LICENSE) file for details.

## Contributing

Feel free to open issues or submit pull requests if you have suggestions or improvements.

## Acknowledgements

- [PyAutoGUI Documentation](https://pyautogui.readthedocs.io/)

