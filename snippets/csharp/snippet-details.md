# Snippet Details

## `cmd`

```c#
#region nameCommand
private DelegateCommand _nameCommand;
public DelegateCommand nameCommand => _nameCommand ??= new DelegateCommand(async () =>
{
    if (IsBusy) return;
    IsBusy = true;
    IsBusy = false;
});
#endregion
```

## `cmdcan`

```c#
#region nameCommand
private DelegateCommand _nameCommand;
public DelegateCommand nameCommand => _nameCommand ??= new DelegateCommand(
    executeMethod: async () =>
    {
        if (IsBusy) return;
        IsBusy = true;
        IsBusy = false;
    },
    canExecuteMethod: () =>
    {
        return !IsBusy;
    })
    .ObservesProperty(() => IsBusy);
#endregion
```

## `cmdcant`

```c#
#region nameCommand
private DelegateCommand<object> _nameCommand;
public DelegateCommand<object> nameCommand => _nameCommand ??= new DelegateCommand<object>(
    executeMethod: async arg =>
    {
        if (IsBusy) return;
        IsBusy = true;
        IsBusy = false;
    },
    canExecuteMethod: arg =>
    {
        return !IsBusy;
    })
    .ObservesProperty(() => IsBusy);
#endregion
```

## `cmdt`

```c#
#region nameCommand
private DelegateCommand<object> _nameCommand;
public DelegateCommand<object> nameCommand => _nameCommand ??= new DelegateCommand<object>(async arg =>
{
    if (IsBusy) return;
    IsBusy = true;
    IsBusy = false;
});
#endregion
```

## `cmt`

```c#
/* ==================================================================================================
 * 
 * ================================================================================================*/
```

## `propb`

```c#
#region name
public static BindableProperty nameProperty = BindableProperty.Create(nameof(name), typeof(string), typeof(MenuViewModel), default(string), BindingMode.OneWay);
public string name
{
    get { return (string)GetValue(nameProperty); }
    set { SetValue(nameProperty, value); }
}
#endregion
```

## `propbchanged`

```c#
#region name
public static BindableProperty nameProperty = BindableProperty.Create(nameof(name), typeof(string), typeof(MenuViewModel), default(string), BindingMode.OneWay, propertyChanged: nameChanged);
private static void nameChanged(BindableObject bindable, object oldValueObject, object newValueObject)
{
    var @this = (MenuViewModel)bindable;
    var oldValue = (string)oldValueObject;
    var newValue = (string)newValueObject;
}
public string name
{
    get { return (string)GetValue(nameProperty); }
    set { SetValue(nameProperty, value); }
}
#endregion
```

## `props`

```c#
private string _name;
public string Name
{
    get { return _name; }
    set { SetProperty(ref _name, value); }
}
```

## `propv`

```c#
public ValidatableObject<T> name { get; set; } = new ValidatableObject<T>(false);
```
## `propa`

```c#
#region Value
public static readonly BindableProperty ValueProperty = BindableProperty.CreateAttached("Value", typeof(string), typeof(ClassName), default(string));
public static string GetValue(BindableObject bindable)
    => (string)bindable.GetValue(ValueProperty);
public static void SetValue(BindableObject bindable, string value)
    => bindable.SetValue(ValueProperty, value);
#endregion```

## `propj`

```c#
[JsonProperty("name")]
public string Name { get; set; }
```