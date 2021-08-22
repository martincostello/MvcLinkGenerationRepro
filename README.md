# MVC Html.ActionLink Repro with Minimal Actions

To reproduce the issue, clone the repo using at least .NET SDK version `6.0.100-rc.1.21420.39` and follow the steps below:

1. Run app with `dotnet run`
1. Open a browser and navigate to `http://localhost:7175/`
1. Click the `Privacy »` button.

## Expected Behaviour

The browser opens the `http://localhost:7175/Home/Privacy` page.

## Actual Behaviour

The browser opens the `http://localhost:7175/something?action=Privacy&controller=Home` path, displaying the word `something`.

Change the value of `addMinimalApi` to `false` in `Program.cs` to see the intended behaviour.
