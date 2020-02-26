# Backup, Restore Visual Studio Mac preference
## Table of Content

## Location

/Users/`<username>`/Library/Preferences/XamarinStudio-`[version#]`/__`MonoDevelopProperties.xml`__

> `Library` folder may be hidden.  
> Use `Command + Shift + .` to toggle show/hide files

## MonoDevelopProperties.xml Structure

```xml
<MonoDevelopProperties version="2.0">
  <Property key="FavoriteRecentFiles" />
  <Property key="MonoDevelop.Core.FirstRun" value="False" />
  <Property key="MonoDevelop.Core.LastRunVersion" value="8.4.7.17" />
  <Property key="MonoDevelop.Ide.AddinUpdater.LastCheck" value="02/26/2020 14:58:43" />
  <Property key="MonoDevelop.Ide.UserInterfaceTheme" value="Dark" />
</MonoDevelopProperties>
```

## Reset settings

Leave `MonoDevelopProperties` empty to reset _Visual Studio Mac_ settings

```xml
<MonoDevelopProperties version="2.0">

</MonoDevelopProperties>
```

## Restore

Replace content of `MonoDevelopProperties` to restore settings

```xml
<MonoDevelopProperties version="2.0">
    <!--Your setting goes here-->
</MonoDevelopProperties>
```