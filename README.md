# Translator

This project utilizes the `translate` package from PyPi to translate text files from English to Japanese.

## Installation

1. **Install the `translate` package:**
   ```
   pip install translate
   ```

## Usage

1. **Prepare your text file:**
   - Ensure your text file is named `test.txt` and is located in the same directory as your script.

2. **Run the script:**
   - Execute the script to translate the content of `test.txt` to Japanese. The translated content will be saved in a new file named `test-ja.txt`.

## Script Details



### Explanation

- **Import the translator module:**
  ```python
  from translate import Translator
  ```

- **Create a Translator instance for Japanese:**
  ```python
  translator = Translator(to_lang="ja")
  ```

- **Read the input file (`test.txt`):**
  ```python
  with open('./test.txt' , mode='r') as my_file:
      text = my_file.read()
  ```

- **Translate the text to Japanese:**
  ```python
  translation = translator.translate(text)
  ```

- **Print the translated text to the console:**
  ```python
  print(translation)
  ```

- **Write the translated text to a new file (`test-ja.txt`):**
  ```python
  with open('./test-ja.txt', mode='w') as my_file2:
      my_file2.write(translation)
  ```

- **Handle file not found errors:**
  ```python
  except FileNotFoundError as e:
      print('check your file path !')
  ```

## Notes

- The `translate` package supports multiple languages. Although this example uses Japanese, you can change the target language by modifying the `to_lang` parameter in the `Translator` instance. Refer to the package documentation for more details.
- Ensure that `test.txt` is located in the same directory as your script to avoid file path issues.

## Contributing

Feel free to fork this repository and submit pull requests for improvements or bug fixes.

## License

This project is licensed under the MIT License.

---

Feel free to make additional changes based on your specific needs!
