# Swiss holidays for GNU/Emacs calendar

This mode adds Swiss holidays for the GNU/Emacs calendar.

## Sources of data

* [Feiertage in der Schweiz](https://de.wikipedia.org/wiki/Feiertage_in_der_Schweiz)
* [CalendarLocalization](https://www.emacswiki.org/emacs/CalendarLocalization) on the EmacsWiki

## Installation

```
M-x package-install [RET] swiss-holidays [RET]
```
## Configuration

To use `swiss-holidays` in your calendar

``` emacs-lisp
(setq holiday-other-holidays swiss-holidays)
```

If you'd like to add regional holidays, pick additional holidays from
`swiss-holidays-catholic`, `swiss-holidays-epiphany`,
`swiss-holidays-st-joseph-day` or `swiss-holidays-labour-day`.

For the canton of Zürich for example you'd use the following:

``` emacs-lisp
(setq holiday-other-holidays
	(append swiss-holidays swiss-holidays-labour-day))
```

For the canton of Schwyz you could use the following:

``` emacs-lisp
(setq holiday-other-holidays
	(append swiss-holidays swiss-holidays-catholic swiss-holidays-epiphany swiss-holidays-st-joseph-day))
```

## License

GPLv3 for the code. Calendar data is [CC-by-sa-3.0](https://de.wikipedia.org/wiki/Wikipedia:Lizenzbestimmungen_Commons_Attribution-ShareAlike_3.0_Unported).

## Thanks

A lot of inspiration for this package came from reading the source of [russian-holidays](https://github.com/grafov/russian-holidays)
