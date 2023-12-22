# How-to-render-stripline-behind-the-series-in-Blazor-chart

This article describes how to render stripline behind the series in Blazor Chart Component.

**Creating Stripline behind the series in Blazor chart**

[Blazor Chart](https://www.syncfusion.com/blazor-components/blazor-charts) supports rendering stripline behind the series by using [**ZIndex**](https://help.syncfusion.com/cr/blazor/Syncfusion.Blazor.Charts.ZIndex.html) property of stripline. This property takes values as `Behind` and `Over`. By default, stripline appears behind the series.

The following code example demonstrates how to render stripline behind the series in Blazor chart.

**Index.razor**
 
```cshtml

@using Syncfusion.Blazor.Charts

<SfChart>
    <ChartPrimaryXAxis ValueType="Syncfusion.Blazor.Charts.ValueType.Category">
        <ChartStriplines>
            <ChartStripline StartFromAxis="true" Size="4" ZIndex="ZIndex.Behind" Opacity="0.5" Color="green" />
        </ChartStriplines>
    </ChartPrimaryXAxis>

    <ChartSeriesCollection>
        <ChartSeries Type="ChartSeriesType.Column" DataSource="@WeatherReports" XName="X" YName="Y">
        </ChartSeries>
    </ChartSeriesCollection>
</SfChart>

@code {

    public class ChartData
    {
        public string X { get; set; }
        public double Y { get; set; }
    }

    public List<ChartData> WeatherReports = new List<ChartData>
    {
        new ChartData { X = "Sun", Y = 28 },
        new ChartData { X = "Mon", Y = 27 },
        new ChartData { X = "Tue", Y = 33 },
        new ChartData { X = "Wed", Y = 36 },
        new ChartData { X = "Thu", Y = 28 },
        new ChartData { X = "Fri", Y = 30 },
        new ChartData { X = "Sat", Y = 31 }
    };
}

```

The following image screenshot illustrates the output of the above code snippet.

**Output:**

![Stripline-behind-series-in-Blazor-chart](/stripline-behind-series.png)
 
**Conclusion**

I hope you enjoyed learning how to render stripline behind the series in Blazor Chart Component.

You can refer to our [Blazor Chart feature tour](https://www.syncfusion.com/blazor-components/blazor-charts) page to know about its other groundbreaking feature representations and [documentation](https://blazor.syncfusion.com/documentation/chart/getting-started), and how to quickly get started for configuration specifications. You can also explore our [Blazor Chart example](https://blazor.syncfusion.com/demos/chart/line?theme=bootstrap5) to understand how to create and manipulate data.

For current customers, you can check out our components from the [License and Downloads](https://www.syncfusion.com/sales/teamlicense) page. If you are new to Syncfusion, you can try our 30-day [free trial](https://www.syncfusion.com/downloads/blazor) to check out our other controls.

If you have any queries or require clarifications, please let us know in the comments section below. You can also contact us through our [support forums](https://www.syncfusion.com/forums), [support portal](https://support.syncfusion.com/create), or [feedback portal](https://www.syncfusion.com/feedback/blazor-components?control=charts). We are always happy to assist you!