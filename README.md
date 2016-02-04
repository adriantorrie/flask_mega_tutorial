# flask_mega_tutorial

** Original concept, code, and all rights associated with The Flask Mega Tutorial belong to Miguel Grinberg.

This repo is to document my effort working through [The Flask Mega Tutorial](http://blog.miguelgrinberg.com/post/the-flask-mega-tutorial-part-i-hello-world) by Miguel Grinberg, using Miniconda as an environment manager (as opposed to `pyvenv` or `virtualenv`), and Sublime Text 3 (ST3) as my development environment. 

I'm doing this on Windows (I'm sorry if that made you cry).

# Setup

* [Install Miniconda](http://conda.pydata.org/docs/install/quick.html#windows-miniconda-install)

* Type the following into a standard windows command prompt once Miniconda is installed to setup the environment that we will use. This environment will be called `flask_mega` and only have `python3` and `flask` installed initially:
  * `conda update conda`
  * `conda create -n flask_mega python=3 flask`
  * `activate flask_mega`
  * `where python`
  * Write down the location of the `python.exe` path for your new `flask_mega` environment, it should be something similar to: `C:\Users\<user>\MiniConda3\envs\flask_mega\python.exe`

* Create a folder (replace `<user>` with your user name)
  * `C:\Users\<user>\AppData\Roaming\Sublime Text 3\Packages\flask_mega` 

* Create a file in this folder called 
  * `flask_mega.sublime-build`

* Add the following code block to the new file and save. Ensure you have forward slashes `/` (Unix style path), and double quotes `"` (JSON style quotes):

```json
{
    "cmd": ["C:/Users/<user>/MiniConda3/envs/flask_mega/python.exe", "-u", "$file"],
    "file_regex": "^[ ]*File \"(...*?)\", line ([0-9]*)",
    "selector": "source.python"
}
```

* Close and reopen ST3
  * Select from the ST3 menu `Tools > Build System > flask_mega`
