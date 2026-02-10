# obapps3

[OBApps](https://sourceforge.net/projects/obapps) (by Eric Bohlman) ported to Python 3 and wxPython 4.

A graphical editor for Openbox application settings, packaged for [OxyOS](https://os.oxy.so).

## Installation

```bash
sudo python setup.py install
```

Or just place `obapps` somewhere on your `PATH` and make sure it is executable.

## Requirements

- Python 3
- wxPython 4
- python-xlib

## Usage

OBApps uses `~/.config/openbox/rc.xml` (or the config file Openbox was started with) by default. You can specify another file as an argument:

```bash
obapps.py .config/openbox/myrc.xml
```

- Enter or change the name, class, role, or type settings by clicking in their entries in the listbox.
- Using the **Find** button to get settings by clicking on a window changes the settings for the currently selected item in the listbox; it does not add a new entry unless nothing is highlighted. You will usually want to use the **New** button to create a new item first.
- Blank entries for name/class/role/type are ignored. If you want any of those fields to be stored as literally blank attributes (e.g. to match only a window with a blank role), enter `""` or `''` in the field.
- Changes are written to the `rc.xml` file only when the **Apply** button is used. Openbox will automatically be reconfigured when this is done.

## Bugs/Limitations

Since this code is very preliminary, make sure to back up your `rc.xml` file before using obapps3.

## License

See [LICENSE](../blob/master/LICENSE).

---
Part of [OxyOS](https://os.oxy.so) | [GitHub](https://github.com/OxyHQ)
