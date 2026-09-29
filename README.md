# How to Render a Stripline Behind the Series in Syncfusion Blazor Chart

## Overview

This sample demonstrates how to render a stripline behind chart data series using Syncfusion [Blazor Charts](https://www.syncfusion.com/blazor-components/blazor-charts). The implementation configures a stripline on the primary X-axis and uses the `ZIndex.Behind` setting to ensure the stripline is displayed underneath the chart series.

This approach is useful for highlighting specific ranges, time periods, or categories without obscuring the plotted data. The sample uses a column chart bound to a collection of weather data and visually emphasizes a region of the chart through a configurable stripline.

## Key Features

- Uses the `SfChart` component to render a chart.
- Configures `ChartPrimaryXAxis` with `ValueType="ValueType.Category"`.
- Adds a stripline through the `ChartStriplines` collection.
- Uses `ChartStripline` to define the highlighted region.
- Sets `ZIndex="ZIndex.Behind"` to render the stripline beneath the chart series.
- Uses `StartFromAxis="true"` to start stripline rendering from the axis origin.
- Controls stripline width using the `Size` property.
- Customizes stripline appearance using:
  - `Color`
  - `Opacity`
- Displays category-based data using `ChartSeries`.
- Binds data through the `DataSource` property.
- Maps category and value fields using:
  - `XName`
  - `YName`
- Renders the chart using `Type="ChartSeriesType.Column"`.

## Prerequisites

- [Visual Studio 2022](https://visualstudio.microsoft.com/vs/) or [Visual Studio Code](https://code.visualstudio.com/)
- [.NET SDK](https://dotnet.microsoft.com/en-us/download/dotnet) compatible with the project's target framework

## How to Run the Project

**Visual Studio 2022**

1. Clone or download this repository.
2. Open the `Stripline/Stripline.csproj` project file in Visual Studio 2022.
3. Restore NuGet packages when prompted.
4. Build the project.
5. Run the application using `Ctrl+F5`.

**Visual Studio Code**

1. Clone or download this repository.
2. Open the repository folder in Visual Studio Code.
3. Open the integrated terminal.
4. Navigate to the project directory.

```bash
cd Stripline
dotnet restore
dotnet run
```

5. Open the local URL displayed in the terminal after the application starts.

## Project Structure

`Stripline/Pages/Index.razor` - Contains the `SfChart`, `ChartPrimaryXAxis`, `ChartStripline`, chart series configuration, and sample weather data used to demonstrate stripline rendering behind a series.

## Support and Feedback

- For general product questions, visit the [Syncfusion Community Forum](https://www.syncfusion.com/forums) or [Syncfusion Support](https://www.syncfusion.com/support).
- To report an issue specific to this sample, open a GitHub issue in this repository.
- Refer to the official Chart StripLine documentation: https://help.syncfusion.com/chart-sdk/blazor/charts/strip-line

## License

This is a Syncfusion sample project provided to demonstrate product usage. Review the [Syncfusion license terms](https://www.syncfusion.com/sales/pricing?category=ui-components) before using Syncfusion components in your own applications.