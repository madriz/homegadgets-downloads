# HomeGadgets desktop app: downloads

This repository holds the installers for the HomeGadgets desktop app and nothing
else. There is no source code here. Each release is a built program, its
checksum, and a small `latest.json` describing it.

HomeGadgets compares what Canadian retailers charge for electronics and
appliances. The desktop app searches that catalogue and can check a product's
price live, from your own computer. More about it: <https://www.homegadgets.ca/apps>

## Download

**Windows (64-bit), the released version:**
<https://github.com/madriz/homegadgets-downloads/releases/latest/download/HomeGadgets-windows-x64-setup.exe>

That address always gives the newest released version. When no version is
released it answers "not found"; that is deliberate, not a broken link.

Builds marked **Pre-release** on the
[Releases page](https://github.com/madriz/homegadgets-downloads/releases) are
test builds. They are there to be tried before release and may misbehave.

There is no Mac or Linux version yet.

## Windows will warn you

The installer is not signed with a paid developer certificate, so Windows shows
"Windows protected your PC" the first time. Choose **More info**, then
**Run anyway**. You can check the file first: every release lists its SHA-256,
and in PowerShell

```powershell
Get-FileHash .\HomeGadgets-windows-x64-setup.exe -Algorithm SHA256
```

should print the same value.

## Each version works for about a month

A copy of the app stops working on the first Sunday of a month and asks you to
download the new one. The date a version stops is in its release notes and in
`latest.json` (`expires`). A new version is published here before that date.
Installing it over the old one is all it takes.

## What the app does and does not do

* Prices are in Canadian dollars. Catalogue prices are ones we recorded, with
  the date. A live check reads the retailers' own pages at the moment you ask,
  from your computer and your internet connection.
* Live checks are limited to 50 a day.
* There is no account. The app sends no name, email or location. It carries a
  random install id, its version and its build date.
* Some links to retailers are affiliate links, and HomeGadgets may earn a
  commission if you buy, at no extra cost to you. That never changes which
  price is shown or the order.

## Terms

The app is early software, provided as is. See [TERMS.md](TERMS.md).

HomeGadgets is independent. It does not sell products and is not affiliated
with or endorsed by any retailer or manufacturer.
