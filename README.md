# HomeGadgets Price Now: downloads

[Français](README.fr.md)

This repository holds the installers for HomeGadgets Price Now, the HomeGadgets
desktop app, and nothing else. There is no source code here. Each release is a
built program, its checksum, and a small `latest.json` describing it.

## What it does

HomeGadgets compares what Canadian retailers charge for electronics and
appliances. Price Now searches that catalogue and can check a product's price
live, from your own computer, at the moment you ask. More about it:
<https://www.homegadgets.ca/apps>

## Install

**Windows (64-bit), the released version:**
<https://github.com/madriz/homegadgets-downloads/releases/latest/download/HomeGadgets-windows-x64-setup.exe>

That address always gives the newest released version. When no version is
released it answers "not found"; that is deliberate, not a broken link.

Builds marked **Pre-release** on the
[Releases page](https://github.com/madriz/homegadgets-downloads/releases) are
test builds. They are there to be tried before release and may misbehave.

1. Download `HomeGadgets-windows-x64-setup.exe`.
2. Check it (optional): every release lists its SHA-256. In PowerShell,
   `Get-FileHash .\HomeGadgets-windows-x64-setup.exe -Algorithm SHA256` should
   print the same value.
3. Run it. The installer is not signed with a paid developer certificate, so
   Windows shows "Windows protected your PC" the first time. Choose
   **More info**, then **Run anyway**.

To update, install the new version over the old one. To remove it, use
**Settings > Apps > Installed apps > HomeGadgets > Uninstall**.

## System requirements

* Windows 10 or Windows 11, 64-bit.
* Microsoft Edge WebView2, which Windows 11 already has. If it is missing, the
  installer downloads it, so the first install needs an internet connection.
* Room for the installer, which is about 90 MB.
* An internet connection whenever you use the app.

There is no Mac or Linux version.

## Each version stops working on a set date

A version stops working at 00:00, your computer's local time, on the **first
Sunday of the month after the month it was built in**, and asks you to download
the new one. A version built in November 2026 stops on Sunday 6 December 2026.
The date is in each release's notes and in `latest.json` (`expires`). A new
version is published here before that date; installing it is all it takes.

The HomeGadgets server applies the same date to the price feed (one day later,
so no time zone is cut off early), and HomeGadgets can switch the app off at any
time.

## Limitations

* This is early software (a beta), provided as is.
* Windows only.
* Live checks are limited to 50 a day. Catalogue searches are limited to 100 a
  day for each install, and again by address and in total on our server.
* A live check reads the retailer's own page. Some retailers refuse automated
  page reads or change their pages; then the check fails or finds nothing.
* A catalogue price is one we recorded earlier, shown with its date. Any price
  can differ from what the retailer charges at checkout. Taxes, delivery,
  installation and fees are not included unless the app says so. Stock is not
  guaranteed.
* Changing your computer's date does not keep an expired version working.

## What the app sends

To the HomeGadgets server (`mcp.homegadgets.ca`), with each request:

* what you typed in the search box, or the product a live check is for;
* a random install id, made on your computer the first time the app starts;
* the app's version, its build date, an app identifier (not a password; it
  only counts the app's searches against its own allowance) and the name of
  the app.

There is no account. The app sends no name, email address, location or
browsing history, and the language you choose stays on your computer.

A live check contacts the retailer's website directly from your computer and
your internet connection, the same way your browser would. That retailer sees
your IP address, as with any visit.

## Amazon and affiliate links

The Amazon button never opens Amazon directly: it opens the product's page on
homegadgets.ca at its Amazon section. As an Amazon Associate I earn from
qualifying purchases. This does not affect what you pay.

Some other links to retailers are affiliate links, and HomeGadgets may earn a
commission if you buy. It costs you nothing extra, and it never changes which
price is shown or the order: the ranking is by price alone.

## Use at your own risk, no warranty

You use the app at your own risk. It is provided as is and as available,
without warranty of any kind. The price and terms on the retailer's own page are
the ones that count; check them before you buy. HomeGadgets does not sell
anything and is not a party to any purchase. The full terms are in
[TERMS.md](TERMS.md) and the licence is in [LICENSE.md](LICENSE.md).

HomeGadgets is independent and is not affiliated with or endorsed by any
retailer or manufacturer.

## Contact

Use the contact form at <https://www.homegadgets.ca/contact>.
