# Clean-up-the-trash
This script is my small practice program in Python.

Why did I do this?
I’m practicing working with Python, libraries, and text cleaning. This script helped me better understand regular expressions, working with translation libraries, and text processing.

---


If you need something similar — feel free to take it and adapt it for your tasks!

This program removes timing marks (like "50:05") and timestamps, and also removes empty lines from the text.
It translates the cleaned text into the desired language (default is Italian).
It shows the number of characters in the original text.
If you need to quickly clean the text from timestamps (for example, from subtitles) and translate it, this script will do the job.


What’s needed to run it?

1) ```Python 3.11.1```

2) Install  `deep_translator` , which includes the GoogleTranslator class.
This can be done in bash: `pip install deep-translator`

 ### _<span style="color:silver; font-weight:bold">How does the program work?</span>_

#### 1. Text Input:  There is a variable transcript, where I input the text that needs to be cleaned and translated.

#### 2. ` RemoveTiming and Empty Lines. Function`
We explicitly state that in this function, we remove timestamps, extra empty lines, and timing. 

Next, we have the function: 

#### ```Split Test.```

Since the Google Translate API has a source='<span style="color:red">5000</span>' -character limit for translation, we need to split the text

So, we break the length and split the text into parts, so that we can later translate the entire text, which might exceed 5000 characters(perhaps).

#### ```Text Translation```


In ```DevTranslateText```, we use the<span style="color:red">`Deep Translator`</span> object, which we run from the deep_translator library.

We specify that the text should be automatically detected in the source parameter. Then, the cleaned text will be stored in the transcript variable, and all unwanted elements (like timestamps and empty lines) will be removed through the cleaning process.

 2.Output Result
First, the number of characters in the original text should be displayed.
Then, the translated text will be shown.
3.  Running the Program
Make sure everything is set up (Python and the `deep_translator` library).
Open the file in your editor (e.g., `VSCode or PyCharm`).
Click Run or run it through the terminal:

bash

What will the program output:
```python

Numb of simbols: 72
Jack stupì subito il mago irritato con
 le sue mosse audaci e imprevedibili.

```
  We then assign the function we wrote for removing timestamps and empty lines to a variable.
Next, we need to check how many characters we have in the text initially to display the character count, and whether it exceeds or is under 5000 characters. We output this information on the screen so the user can see what is acceptable and what is not.

Then, in the <span style="color:red">`if`</span> statement, we split the text if its length exceeds 5000 characters.
We check that if count (the length we calculate from the text) is greater than 5000, we split the text into parts.




We also specify the target language to which we need to translate the text.
This can be any language, for example, I have Italian set by default. You can set any language you want. Below, I’ve listed the 10 most popular languages that you can choose from. Where we mention translated_parts, we are translating each part of the text.


 - <span style="color:blue">English: en</span>
- <span style="color:blue">German: de</span>
- <span style="color:blue">Italian: it</span>
- <span style="color:blue">French: fr</span>
- <span style="color:blue">Japanese: ja</span>
- <span style="color:blue">Chinese: zh-CN</span>
- <span style="color:blue">Spanish: es</span>
- <span style="color:blue">Russia: ru </span>
- <span style="color:blue">Spanish: es</span>
- <span style="color:blue">Portuguese: pt</span>
- <span style="color:blue">Arabic: ar</span>


French for example :
```

 translated_text = translate_text(cleaned_text, target_lang='fr')<-
                                                            -----

```
And the text itself is placed into the transcript variable.   

