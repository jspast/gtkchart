# GtkChart

## Introduction

The beginnings of a small chart widget library for GTK4.

This is a spinoff from the [lxi-tools](https://lxi-tools.github.io) project.

Much can be improved but it is better than nothing.

Looking for maintainer/contributors to help improve this library.

## Motivation

Couldn't find a chart library for GTK4 so created one.

## Features

 * Various chart types
   * Line
   * Scatter
   * Linear gauge
   * Angular gauge
   * Number
 * Dimensionally scalable
 * Plot and render data live
 * Save rendered chart to PNG
 * Save plotted data to CSV

## Todo

 * Optimize Cairo/snapshot code
 * Make charts zoomable
 * Make charts handle negative axis values
 * Etc.

## Usage

```
// Required for GtkChart to be recognized by builder
gtk_chart_get_type();
...
GtkWidget *chart = gtk_chart_new();
gtk_chart_set_type(chart, GTK_CHART_TYPE_LINE);
gtk_chart_set_title(chart, "Title");
gtk_chart_set_label(chart, "Label");
gtk_chart_set_x_label(chart, "X label [ ]");
gtk_chart_set_y_label(chart, "Y label [ ]");
gtk_chart_set_x_max(chart, 100);
gtk_chart_set_y_max(chart, 10);
gtk_chart_set_width(chart, 800);
...
gtk_chart_plot_point(chart, 0.0, 0.0);
gtk_chart_plot_point(chart, 1.0, 1.0);
gtk_chart_plot_point(chart, 2.0, 2.0);
gtk_chart_plot_point(chart, 3.0, 3.0);
...
gtk_chart_save_csv(chart, "chart0.csv");
gtk_chart_save_png(chart, "chart0.png");
```

## Chart types

<p align="center">
<img src="images/line.png">
<img src="images/scatter.png">
<img src="images/gauge-angular.png">
<img src="images/gauge-line.png">
<img src="images/number.png">
</p>
