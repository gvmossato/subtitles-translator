# 🎞️ Subtitles Translator

Minimal Python script developed to machine-translate a `.srt` file (commonly used for subtitles) from a `SOURCE_LANGUAGE` to a `TARGET_LANGUAGE` using Google Translate.

# 📦 Requirements

Main dependencies:

* [deep-translator](https://pypi.org/project/deep-translator/)
* [black](https://pypi.org/project/black/) (Optional)
* [isort](https://pypi.org/project/isort/) (Optional)

Alternatively, you can refer to `requirements.txt` for an extensive list.

# ✨ Use

1. Place all the files to be translated in the `./sub` folder;
2. Edit the `SOURCE_LANGUAGE` and `TARGET_LANGUAGE` variables accordingly, use the Google Translate language names (for reference, [read the docs](https://deep-translator.readthedocs.io/en/latest/usage.html#google-translate));
3. Install the required dependencies using `pip install -r requirements.txt`;
4. Run `python translate.py`;
5. Wait until the process completes, the translated files will be located in the `./out` folder.

Example of use:

![example](https://github.com/gvmossato/subtitles-translator/assets/41247052/14cdca30-9811-4807-b29d-e3c37b6c7c1d)

# 📝 About

A `.srt` file is typically structured as follows:

```
Index
Start time --> End time
Subtitle string 1
Subtitle string 2
Subtitle string n

Index
Start time --> End time
Subtitle string 1
Subtitle string 2
Subtitle string n

Index
Start time --> End time
Subtitle string 1
Subtitle string 2
Subtitle string n

...
```

This script essentially breaks down the file, sending each subtitle string from each group to Google Translate and then reassembles the file with the provided translations.

# ❗ Caveats

Before using, consider the following:

* Performance was not a concern, which means excessive use may result in excessive tedium;
* Strings are translated independently, potentially leading to imprecise translations (no context is maintained).
