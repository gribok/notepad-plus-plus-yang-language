# notepad-plus-plus-yang-language
YANG modeling language files for syntax highlighting and auto-completion for Notepad++.

Definition of keywords is based on [RFC7950](https://tools.ietf.org/html/rfc7950) for YANG 1.1 (contains [RFC6020](https://tools.ietf.org/html/rfc6020) as well).

## Getting Started
This instruction will get you a setup for YANG syntax-highlighting and auto-completion in Notepad++.

### Prerequisites

Download and install [Notepad++](https://notepad-plus-plus.org/downloads/).

### Installing

1. Clone repository to get definition files
```bash
$ git clone https://github.com/gribok/notepad-plus-plus-yang-language.git
```

2. Import User Defined Language (UDL) for YANG. There are two main ways to do this.

    1. Copy the XML `yang_by-gribok.xml` into the `<notepad++_install_directory>/userDefineLangs` subfolder.

       For Notepad++ **v7.6.1 and earlier** this option doesn't exist.

    2. Use the Import button.
       Navigate per menu bar to `Languages > Define Your Language`. It will bring up a dialog box. Click on `import` button and insert the source XML `yang_by-gribok.xml`. The UDL will be immediately available.

    The differences between those two methods are when the UDL will be available to Notepad++, and which config file will hold that UDL, per UDL File Locations.

3. Copy **auto-completion file** `yang.xml` to `<notepad++_install_directory>/autoCompletion` subdirectory of the Notepad++ install folder.

   For Notepad++ **v7.6.1 and earlier** copy to `<notepad++_install_directory>/plugins/APIs`.

   The name of auto-completion file is important and have to be named as the name definition inside of the UDL file.

   **For example:**

   ``` bash
   $ cat yang_by-gribok.xml
   [output omitted]
   <UserLang name="YANG" ext="yang" udlVersion="2.1">
   [output omitted]
   ```

   Then the name of auto-completion file have to be `yang.xml`.

4. Exit all instances of Notepad++ and reload, then the new UDL with auto-completion will be available.

5. Enjoy!

## Documentation
Detailed documentation about [User Defined Language Documentation](https://npp-user-manual.org/docs/user-defined-language-system/).

Detailed documentation about [Auto Completion](https://npp-user-manual.org/docs/auto-completion/).

Further UDLs for different languages under [notepad-plus-plus/userDefinedLanguages](https://github.com/notepad-plus-plus/userDefinedLanguages)

## Contributing
Be welcome to pull requests!

## License

This project is licensed under the GNU License - see the [LICENSE](LICENSE) file for details
