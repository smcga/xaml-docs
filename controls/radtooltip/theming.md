---
title: Theming
page_title: Theming
description: Theming
slug: radtooltip-theming
tags: theming
published: True
position: 3
---

# Theming



## 

Telerik themes are not turned on by default in __RadToolTip__. In order to use the predefined Telerik styles you can define a __ContentTemplate__ for the __RadToolTip__ component and use the __RadToolTipContentView__ control inside the template.

The following code example demonstrates how to set up __RadToolTip__ to use the Telerik themes.

#### __XAML__
    Ellipse Width="80" Height="80" Fill="#FF1B9DDE" Stroke="#FF1B9DDE" StrokeThickness="2"
              telerik:RadToolTipService.Placement="Top"
              telerik:RadToolTipService.VerticalOffset="-10"
              telerik:RadToolTipService.ToolTipContent="RadToolTip">
        <telerik:RadToolTipService.ToolTipContentTemplate>
            <DataTemplate>
                <telerik:RadToolTipContentView>
                    <TextBlock Text="{Binding}" />
                </telerik:RadToolTipContentView>
            </DataTemplate>
        </telerik:RadToolTipService.ToolTipContentTemplate>
    </Ellipse>

{% if site.site_name == 'WPF' %}

Another approach that can be used for setting up the __RadToolTip__ theming is to set the __ToolTipContentTemplate__ property to null and then define the __RadToolTipContentView__ control inside the __ToolTipContent__.

#### __XAML__
    <Ellipse Width="80" Height="80" Fill="#FF1B9DDE" Stroke="#FF1B9DDE" StrokeThickness="2"
           telerik:RadToolTipService.Placement="Top"
           telerik:RadToolTipService.VerticalOffset="-10"
           telerik:RadToolTipService.ToolTipContentTemplate="{x:Null}">
      <telerik:RadToolTipService.ToolTipContent>
          <telerik:RadToolTipContentView>
              <TextBlock Text="RadToolTip" />
          </telerik:RadToolTipContentView>
      </telerik:RadToolTipService.ToolTipContent>
    </Ellipse>
              

{% endif %}

The end result is demonstrated in the picture below:
{% if site.site_name == 'WPF' %}![radtooltip-theming-wpf 01](images/radtooltip-theming-wpf_01.png){% endif %}{% if site.site_name == 'Silverlight' %}![radtooltip-theming-sl 01](images/radtooltip-theming-sl_01.png){% endif %}

# See Also

 * [Getting Started]({%slug radtooltip-getting-started%})
