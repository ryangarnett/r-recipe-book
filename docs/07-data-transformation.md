



# Data Transformation
Data is collected in many different ways, and for many different purposes. While the data structure may work for oen use case, it may not work for another. A few common series of tasks is to transform the strucutre and data types. This chapter will focus on transforming data to follow the [tidy data principles](https://vita.had.co.nz/papers/tidy-data.pdf).

<br>

> *It is often said that 80% of data analysis is spent on the cleaning and preparing data. And it’s not just a first step, but it must be repeated many times over the course of analysis as new problems come to light or new data is collected. <br> [Tidy data](https://cran.r-project.org/web/packages/tidyr/vignettes/tidy-data.html) - exerts from Hadly Wickham*


## Between Data Types
It is very common that the data types stored in a dataset differ from the desired data type for analysis. Data may be collected in one format for various reason, however that format many not allow for specific data analysis techniques. The following recipes outline how to change columns of data to a new data type.

### Change character data type to numeric data type in single column

```{=html}
<div id="govjjwrgst" style="overflow-x:auto;overflow-y:auto;width:auto;height:auto;">
<style>html {
  font-family: -apple-system, BlinkMacSystemFont, 'Segoe UI', Roboto, Oxygen, Ubuntu, Cantarell, 'Helvetica Neue', 'Fira Sans', 'Droid Sans', Arial, sans-serif;
}

#govjjwrgst .gt_table {
  display: table;
  border-collapse: collapse;
  margin-left: auto;
  margin-right: auto;
  color: #333333;
  font-size: 16px;
  font-weight: normal;
  font-style: normal;
  background-color: #FFFFFF;
  width: auto;
  border-top-style: solid;
  border-top-width: 2px;
  border-top-color: #A8A8A8;
  border-right-style: none;
  border-right-width: 2px;
  border-right-color: #D3D3D3;
  border-bottom-style: solid;
  border-bottom-width: 2px;
  border-bottom-color: #A8A8A8;
  border-left-style: none;
  border-left-width: 2px;
  border-left-color: #D3D3D3;
}

#govjjwrgst .gt_heading {
  background-color: #153331;
  text-align: center;
  border-bottom-color: #FFFFFF;
  border-left-style: none;
  border-left-width: 1px;
  border-left-color: #D3D3D3;
  border-right-style: none;
  border-right-width: 1px;
  border-right-color: #D3D3D3;
}

#govjjwrgst .gt_title {
  color: #FFFFFF;
  font-size: 125%;
  font-weight: initial;
  padding-top: 4px;
  padding-bottom: 4px;
  border-bottom-color: #FFFFFF;
  border-bottom-width: 0;
}

#govjjwrgst .gt_subtitle {
  color: #FFFFFF;
  font-size: 85%;
  font-weight: initial;
  padding-top: 0;
  padding-bottom: 6px;
  border-top-color: #FFFFFF;
  border-top-width: 0;
}

#govjjwrgst .gt_bottom_border {
  border-bottom-style: solid;
  border-bottom-width: 2px;
  border-bottom-color: #D3D3D3;
}

#govjjwrgst .gt_col_headings {
  border-top-style: solid;
  border-top-width: 2px;
  border-top-color: #D3D3D3;
  border-bottom-style: solid;
  border-bottom-width: 2px;
  border-bottom-color: #D3D3D3;
  border-left-style: none;
  border-left-width: 1px;
  border-left-color: #D3D3D3;
  border-right-style: none;
  border-right-width: 1px;
  border-right-color: #D3D3D3;
}

#govjjwrgst .gt_col_heading {
  color: #FFFFFF;
  background-color: #153331;
  font-size: 100%;
  font-weight: normal;
  text-transform: inherit;
  border-left-style: none;
  border-left-width: 1px;
  border-left-color: #D3D3D3;
  border-right-style: none;
  border-right-width: 1px;
  border-right-color: #D3D3D3;
  vertical-align: bottom;
  padding-top: 5px;
  padding-bottom: 6px;
  padding-left: 5px;
  padding-right: 5px;
  overflow-x: hidden;
}

#govjjwrgst .gt_column_spanner_outer {
  color: #FFFFFF;
  background-color: #153331;
  font-size: 100%;
  font-weight: normal;
  text-transform: inherit;
  padding-top: 0;
  padding-bottom: 0;
  padding-left: 4px;
  padding-right: 4px;
}

#govjjwrgst .gt_column_spanner_outer:first-child {
  padding-left: 0;
}

#govjjwrgst .gt_column_spanner_outer:last-child {
  padding-right: 0;
}

#govjjwrgst .gt_column_spanner {
  border-bottom-style: solid;
  border-bottom-width: 2px;
  border-bottom-color: #D3D3D3;
  vertical-align: bottom;
  padding-top: 5px;
  padding-bottom: 5px;
  overflow-x: hidden;
  display: inline-block;
  width: 100%;
}

#govjjwrgst .gt_group_heading {
  padding: 8px;
  color: #333333;
  background-color: #FFFFFF;
  font-size: 100%;
  font-weight: initial;
  text-transform: inherit;
  border-top-style: solid;
  border-top-width: 2px;
  border-top-color: #D3D3D3;
  border-bottom-style: solid;
  border-bottom-width: 2px;
  border-bottom-color: #D3D3D3;
  border-left-style: none;
  border-left-width: 1px;
  border-left-color: #D3D3D3;
  border-right-style: none;
  border-right-width: 1px;
  border-right-color: #D3D3D3;
  vertical-align: middle;
}

#govjjwrgst .gt_empty_group_heading {
  padding: 0.5px;
  color: #333333;
  background-color: #FFFFFF;
  font-size: 100%;
  font-weight: initial;
  border-top-style: solid;
  border-top-width: 2px;
  border-top-color: #D3D3D3;
  border-bottom-style: solid;
  border-bottom-width: 2px;
  border-bottom-color: #D3D3D3;
  vertical-align: middle;
}

#govjjwrgst .gt_from_md > :first-child {
  margin-top: 0;
}

#govjjwrgst .gt_from_md > :last-child {
  margin-bottom: 0;
}

#govjjwrgst .gt_row {
  padding-top: 8px;
  padding-bottom: 8px;
  padding-left: 5px;
  padding-right: 5px;
  margin: 10px;
  border-top-style: solid;
  border-top-width: 1px;
  border-top-color: #D3D3D3;
  border-left-style: none;
  border-left-width: 1px;
  border-left-color: #D3D3D3;
  border-right-style: none;
  border-right-width: 1px;
  border-right-color: #D3D3D3;
  vertical-align: middle;
  overflow-x: hidden;
}

#govjjwrgst .gt_stub {
  color: #333333;
  background-color: #FFFFFF;
  font-size: 100%;
  font-weight: initial;
  text-transform: inherit;
  border-right-style: solid;
  border-right-width: 2px;
  border-right-color: #D3D3D3;
  padding-left: 12px;
}

#govjjwrgst .gt_summary_row {
  color: #333333;
  background-color: #FFFFFF;
  text-transform: inherit;
  padding-top: 8px;
  padding-bottom: 8px;
  padding-left: 5px;
  padding-right: 5px;
}

#govjjwrgst .gt_first_summary_row {
  padding-top: 8px;
  padding-bottom: 8px;
  padding-left: 5px;
  padding-right: 5px;
  border-top-style: solid;
  border-top-width: 2px;
  border-top-color: #D3D3D3;
}

#govjjwrgst .gt_grand_summary_row {
  color: #333333;
  background-color: #FFFFFF;
  text-transform: inherit;
  padding-top: 8px;
  padding-bottom: 8px;
  padding-left: 5px;
  padding-right: 5px;
}

#govjjwrgst .gt_first_grand_summary_row {
  padding-top: 8px;
  padding-bottom: 8px;
  padding-left: 5px;
  padding-right: 5px;
  border-top-style: double;
  border-top-width: 6px;
  border-top-color: #D3D3D3;
}

#govjjwrgst .gt_striped {
  background-color: rgba(128, 128, 128, 0.05);
}

#govjjwrgst .gt_table_body {
  border-top-style: solid;
  border-top-width: 2px;
  border-top-color: #D3D3D3;
  border-bottom-style: solid;
  border-bottom-width: 2px;
  border-bottom-color: #D3D3D3;
}

#govjjwrgst .gt_footnotes {
  color: #333333;
  background-color: #FFFFFF;
  border-bottom-style: none;
  border-bottom-width: 2px;
  border-bottom-color: #D3D3D3;
  border-left-style: none;
  border-left-width: 2px;
  border-left-color: #D3D3D3;
  border-right-style: none;
  border-right-width: 2px;
  border-right-color: #D3D3D3;
}

#govjjwrgst .gt_footnote {
  margin: 0px;
  font-size: 90%;
  padding: 4px;
}

#govjjwrgst .gt_sourcenotes {
  color: #333333;
  background-color: #FFFFFF;
  border-bottom-style: none;
  border-bottom-width: 2px;
  border-bottom-color: #D3D3D3;
  border-left-style: none;
  border-left-width: 2px;
  border-left-color: #D3D3D3;
  border-right-style: none;
  border-right-width: 2px;
  border-right-color: #D3D3D3;
}

#govjjwrgst .gt_sourcenote {
  font-size: 90%;
  padding: 4px;
}

#govjjwrgst .gt_left {
  text-align: left;
}

#govjjwrgst .gt_center {
  text-align: center;
}

#govjjwrgst .gt_right {
  text-align: right;
  font-variant-numeric: tabular-nums;
}

#govjjwrgst .gt_font_normal {
  font-weight: normal;
}

#govjjwrgst .gt_font_bold {
  font-weight: bold;
}

#govjjwrgst .gt_font_italic {
  font-style: italic;
}

#govjjwrgst .gt_super {
  font-size: 65%;
}

#govjjwrgst .gt_footnote_marks {
  font-style: italic;
  font-weight: normal;
  font-size: 65%;
}
</style>
<table class="gt_table" style="table-layout: fixed;; width: 0px">
  <colgroup>
    <col style="width:500px;"/>
    <col style="width:200px;"/>
  </colgroup>
  
  <thead class="gt_col_headings">
    <tr>
      <th class="gt_col_heading gt_columns_bottom_border gt_left" rowspan="1" colspan="1"><strong>Description</strong></th>
      <th class="gt_col_heading gt_columns_bottom_border gt_right" rowspan="1" colspan="1"></th>
    </tr>
  </thead>
  <tbody class="gt_table_body">
    <tr><td class="gt_row gt_left">Method to change all character values to numeric values in a single column of a dataframe</td>
<td class="gt_row gt_right"><svg aria-hidden="true" role="img" viewBox="0 0 512 512" style="height:2em;width:2em;vertical-align:-0.125em;margin-left:auto;margin-right:auto;font-size:inherit;fill:#A62014;overflow:visible;position:relative;"><path d="M330.67 263.12V173.4l-52.75-24.22C219.44 218.76 197.58 400 56 400a56 56 0 0 0 0 112c212.64 0 370.65-122.87 419.18-210.34l-37.05-38.54zm131.09-128.37C493.92 74.91 477.18 26.48 458.62 3a8 8 0 0 0-11.93-.59l-22.9 23a8.06 8.06 0 0 0-.89 10.23c6.86 10.36 17.05 35.1-1.4 72.32A142.85 142.85 0 0 0 364.34 96c-28 0-54 8.54-76.34 22.59l74.67 34.29v78.24h89.09L506.44 288c3.26-12.62 5.56-25.63 5.56-39.31a154 154 0 0 0-50.24-113.94z"/></svg><svg aria-hidden="true" role="img" viewBox="0 0 512 512" style="height:2em;width:2em;vertical-align:-0.125em;margin-left:auto;margin-right:auto;font-size:inherit;fill:#9FC2B9;overflow:visible;position:relative;"><path d="M330.67 263.12V173.4l-52.75-24.22C219.44 218.76 197.58 400 56 400a56 56 0 0 0 0 112c212.64 0 370.65-122.87 419.18-210.34l-37.05-38.54zm131.09-128.37C493.92 74.91 477.18 26.48 458.62 3a8 8 0 0 0-11.93-.59l-22.9 23a8.06 8.06 0 0 0-.89 10.23c6.86 10.36 17.05 35.1-1.4 72.32A142.85 142.85 0 0 0 364.34 96c-28 0-54 8.54-76.34 22.59l74.67 34.29v78.24h89.09L506.44 288c3.26-12.62 5.56-25.63 5.56-39.31a154 154 0 0 0-50.24-113.94z"/></svg><svg aria-hidden="true" role="img" viewBox="0 0 512 512" style="height:2em;width:2em;vertical-align:-0.125em;margin-left:auto;margin-right:auto;font-size:inherit;fill:#9FC2B9;overflow:visible;position:relative;"><path d="M330.67 263.12V173.4l-52.75-24.22C219.44 218.76 197.58 400 56 400a56 56 0 0 0 0 112c212.64 0 370.65-122.87 419.18-210.34l-37.05-38.54zm131.09-128.37C493.92 74.91 477.18 26.48 458.62 3a8 8 0 0 0-11.93-.59l-22.9 23a8.06 8.06 0 0 0-.89 10.23c6.86 10.36 17.05 35.1-1.4 72.32A142.85 142.85 0 0 0 364.34 96c-28 0-54 8.54-76.34 22.59l74.67 34.29v78.24h89.09L506.44 288c3.26-12.62 5.56-25.63 5.56-39.31a154 154 0 0 0-50.24-113.94z"/></svg></td></tr>
  </tbody>
  
  
</table>
</div>
```

```{=html}
<div id="gklesqduzi" style="overflow-x:auto;overflow-y:auto;width:auto;height:auto;">
<style>html {
  font-family: -apple-system, BlinkMacSystemFont, 'Segoe UI', Roboto, Oxygen, Ubuntu, Cantarell, 'Helvetica Neue', 'Fira Sans', 'Droid Sans', Arial, sans-serif;
}

#gklesqduzi .gt_table {
  display: table;
  border-collapse: collapse;
  margin-left: auto;
  margin-right: auto;
  color: #333333;
  font-size: 16px;
  font-weight: normal;
  font-style: normal;
  background-color: #FFFFFF;
  width: auto;
  border-top-style: solid;
  border-top-width: 2px;
  border-top-color: #A8A8A8;
  border-right-style: none;
  border-right-width: 2px;
  border-right-color: #D3D3D3;
  border-bottom-style: solid;
  border-bottom-width: 2px;
  border-bottom-color: #A8A8A8;
  border-left-style: none;
  border-left-width: 2px;
  border-left-color: #D3D3D3;
}

#gklesqduzi .gt_heading {
  background-color: #153331;
  text-align: center;
  border-bottom-color: #FFFFFF;
  border-left-style: none;
  border-left-width: 1px;
  border-left-color: #D3D3D3;
  border-right-style: none;
  border-right-width: 1px;
  border-right-color: #D3D3D3;
}

#gklesqduzi .gt_title {
  color: #FFFFFF;
  font-size: 125%;
  font-weight: initial;
  padding-top: 4px;
  padding-bottom: 4px;
  border-bottom-color: #FFFFFF;
  border-bottom-width: 0;
}

#gklesqduzi .gt_subtitle {
  color: #FFFFFF;
  font-size: 85%;
  font-weight: initial;
  padding-top: 0;
  padding-bottom: 6px;
  border-top-color: #FFFFFF;
  border-top-width: 0;
}

#gklesqduzi .gt_bottom_border {
  border-bottom-style: solid;
  border-bottom-width: 2px;
  border-bottom-color: #D3D3D3;
}

#gklesqduzi .gt_col_headings {
  border-top-style: solid;
  border-top-width: 2px;
  border-top-color: #D3D3D3;
  border-bottom-style: solid;
  border-bottom-width: 2px;
  border-bottom-color: #D3D3D3;
  border-left-style: none;
  border-left-width: 1px;
  border-left-color: #D3D3D3;
  border-right-style: none;
  border-right-width: 1px;
  border-right-color: #D3D3D3;
}

#gklesqduzi .gt_col_heading {
  color: #FFFFFF;
  background-color: #1E6E6E;
  font-size: 100%;
  font-weight: normal;
  text-transform: inherit;
  border-left-style: none;
  border-left-width: 1px;
  border-left-color: #D3D3D3;
  border-right-style: none;
  border-right-width: 1px;
  border-right-color: #D3D3D3;
  vertical-align: bottom;
  padding-top: 5px;
  padding-bottom: 6px;
  padding-left: 5px;
  padding-right: 5px;
  overflow-x: hidden;
}

#gklesqduzi .gt_column_spanner_outer {
  color: #FFFFFF;
  background-color: #1E6E6E;
  font-size: 100%;
  font-weight: normal;
  text-transform: inherit;
  padding-top: 0;
  padding-bottom: 0;
  padding-left: 4px;
  padding-right: 4px;
}

#gklesqduzi .gt_column_spanner_outer:first-child {
  padding-left: 0;
}

#gklesqduzi .gt_column_spanner_outer:last-child {
  padding-right: 0;
}

#gklesqduzi .gt_column_spanner {
  border-bottom-style: solid;
  border-bottom-width: 2px;
  border-bottom-color: #D3D3D3;
  vertical-align: bottom;
  padding-top: 5px;
  padding-bottom: 5px;
  overflow-x: hidden;
  display: inline-block;
  width: 100%;
}

#gklesqduzi .gt_group_heading {
  padding: 8px;
  color: #333333;
  background-color: #FFFFFF;
  font-size: 100%;
  font-weight: initial;
  text-transform: inherit;
  border-top-style: solid;
  border-top-width: 2px;
  border-top-color: #D3D3D3;
  border-bottom-style: solid;
  border-bottom-width: 2px;
  border-bottom-color: #D3D3D3;
  border-left-style: none;
  border-left-width: 1px;
  border-left-color: #D3D3D3;
  border-right-style: none;
  border-right-width: 1px;
  border-right-color: #D3D3D3;
  vertical-align: middle;
}

#gklesqduzi .gt_empty_group_heading {
  padding: 0.5px;
  color: #333333;
  background-color: #FFFFFF;
  font-size: 100%;
  font-weight: initial;
  border-top-style: solid;
  border-top-width: 2px;
  border-top-color: #D3D3D3;
  border-bottom-style: solid;
  border-bottom-width: 2px;
  border-bottom-color: #D3D3D3;
  vertical-align: middle;
}

#gklesqduzi .gt_from_md > :first-child {
  margin-top: 0;
}

#gklesqduzi .gt_from_md > :last-child {
  margin-bottom: 0;
}

#gklesqduzi .gt_row {
  padding-top: 8px;
  padding-bottom: 8px;
  padding-left: 5px;
  padding-right: 5px;
  margin: 10px;
  border-top-style: solid;
  border-top-width: 1px;
  border-top-color: #D3D3D3;
  border-left-style: none;
  border-left-width: 1px;
  border-left-color: #D3D3D3;
  border-right-style: none;
  border-right-width: 1px;
  border-right-color: #D3D3D3;
  vertical-align: middle;
  overflow-x: hidden;
}

#gklesqduzi .gt_stub {
  color: #333333;
  background-color: #FFFFFF;
  font-size: 100%;
  font-weight: initial;
  text-transform: inherit;
  border-right-style: solid;
  border-right-width: 2px;
  border-right-color: #D3D3D3;
  padding-left: 12px;
}

#gklesqduzi .gt_summary_row {
  color: #333333;
  background-color: #FFFFFF;
  text-transform: inherit;
  padding-top: 8px;
  padding-bottom: 8px;
  padding-left: 5px;
  padding-right: 5px;
}

#gklesqduzi .gt_first_summary_row {
  padding-top: 8px;
  padding-bottom: 8px;
  padding-left: 5px;
  padding-right: 5px;
  border-top-style: solid;
  border-top-width: 2px;
  border-top-color: #D3D3D3;
}

#gklesqduzi .gt_grand_summary_row {
  color: #333333;
  background-color: #FFFFFF;
  text-transform: inherit;
  padding-top: 8px;
  padding-bottom: 8px;
  padding-left: 5px;
  padding-right: 5px;
}

#gklesqduzi .gt_first_grand_summary_row {
  padding-top: 8px;
  padding-bottom: 8px;
  padding-left: 5px;
  padding-right: 5px;
  border-top-style: double;
  border-top-width: 6px;
  border-top-color: #D3D3D3;
}

#gklesqduzi .gt_striped {
  background-color: rgba(128, 128, 128, 0.05);
}

#gklesqduzi .gt_table_body {
  border-top-style: solid;
  border-top-width: 2px;
  border-top-color: #D3D3D3;
  border-bottom-style: solid;
  border-bottom-width: 2px;
  border-bottom-color: #D3D3D3;
}

#gklesqduzi .gt_footnotes {
  color: #333333;
  background-color: #FFFFFF;
  border-bottom-style: none;
  border-bottom-width: 2px;
  border-bottom-color: #D3D3D3;
  border-left-style: none;
  border-left-width: 2px;
  border-left-color: #D3D3D3;
  border-right-style: none;
  border-right-width: 2px;
  border-right-color: #D3D3D3;
}

#gklesqduzi .gt_footnote {
  margin: 0px;
  font-size: 90%;
  padding: 4px;
}

#gklesqduzi .gt_sourcenotes {
  color: #333333;
  background-color: #FFFFFF;
  border-bottom-style: none;
  border-bottom-width: 2px;
  border-bottom-color: #D3D3D3;
  border-left-style: none;
  border-left-width: 2px;
  border-left-color: #D3D3D3;
  border-right-style: none;
  border-right-width: 2px;
  border-right-color: #D3D3D3;
}

#gklesqduzi .gt_sourcenote {
  font-size: 90%;
  padding: 4px;
}

#gklesqduzi .gt_left {
  text-align: left;
}

#gklesqduzi .gt_center {
  text-align: center;
}

#gklesqduzi .gt_right {
  text-align: right;
  font-variant-numeric: tabular-nums;
}

#gklesqduzi .gt_font_normal {
  font-weight: normal;
}

#gklesqduzi .gt_font_bold {
  font-weight: bold;
}

#gklesqduzi .gt_font_italic {
  font-style: italic;
}

#gklesqduzi .gt_super {
  font-size: 65%;
}

#gklesqduzi .gt_footnote_marks {
  font-style: italic;
  font-weight: normal;
  font-size: 65%;
}
</style>
<table class="gt_table" style="table-layout: fixed;; width: 0px">
  <colgroup>
    <col style="width:350px;"/>
    <col style="width:350px;"/>
  </colgroup>
  <thead class="gt_header">
    <tr>
      <th colspan="2" class="gt_heading gt_title gt_font_normal gt_bottom_border" style>Ingredients</th>
    </tr>
    
  </thead>
  <thead class="gt_col_headings">
    <tr>
      <th class="gt_col_heading gt_columns_bottom_border gt_center" rowspan="1" colspan="1"><strong>Package</strong></th>
      <th class="gt_col_heading gt_columns_bottom_border gt_center" rowspan="1" colspan="1"><strong>Data</strong></th>
    </tr>
  </thead>
  <tbody class="gt_table_body">
    <tr><td class="gt_row gt_center"><div class='gt_from_md'><p>readr<br>dplyr</p>
</div></td>
<td class="gt_row gt_center"><div class='gt_from_md'><p>sample.csv</p>
</div></td></tr>
  </tbody>
  
  
</table>
</div>
```

</br>

**Preparation**

```r
df <- readr::read_csv("C:/data/sample.csv")
```

</br>

**Sample Instructions**

```r
package::function(data, column_name = as.numeric(column_name))
```

</br>

**Actual Instructions**

```r
dplyr::mutate(df, column1 = as.numeric(column1))
```


### Change numeric data type to character data type in single column

```{=html}
<div id="yrynqoxvdg" style="overflow-x:auto;overflow-y:auto;width:auto;height:auto;">
<style>html {
  font-family: -apple-system, BlinkMacSystemFont, 'Segoe UI', Roboto, Oxygen, Ubuntu, Cantarell, 'Helvetica Neue', 'Fira Sans', 'Droid Sans', Arial, sans-serif;
}

#yrynqoxvdg .gt_table {
  display: table;
  border-collapse: collapse;
  margin-left: auto;
  margin-right: auto;
  color: #333333;
  font-size: 16px;
  font-weight: normal;
  font-style: normal;
  background-color: #FFFFFF;
  width: auto;
  border-top-style: solid;
  border-top-width: 2px;
  border-top-color: #A8A8A8;
  border-right-style: none;
  border-right-width: 2px;
  border-right-color: #D3D3D3;
  border-bottom-style: solid;
  border-bottom-width: 2px;
  border-bottom-color: #A8A8A8;
  border-left-style: none;
  border-left-width: 2px;
  border-left-color: #D3D3D3;
}

#yrynqoxvdg .gt_heading {
  background-color: #153331;
  text-align: center;
  border-bottom-color: #FFFFFF;
  border-left-style: none;
  border-left-width: 1px;
  border-left-color: #D3D3D3;
  border-right-style: none;
  border-right-width: 1px;
  border-right-color: #D3D3D3;
}

#yrynqoxvdg .gt_title {
  color: #FFFFFF;
  font-size: 125%;
  font-weight: initial;
  padding-top: 4px;
  padding-bottom: 4px;
  border-bottom-color: #FFFFFF;
  border-bottom-width: 0;
}

#yrynqoxvdg .gt_subtitle {
  color: #FFFFFF;
  font-size: 85%;
  font-weight: initial;
  padding-top: 0;
  padding-bottom: 6px;
  border-top-color: #FFFFFF;
  border-top-width: 0;
}

#yrynqoxvdg .gt_bottom_border {
  border-bottom-style: solid;
  border-bottom-width: 2px;
  border-bottom-color: #D3D3D3;
}

#yrynqoxvdg .gt_col_headings {
  border-top-style: solid;
  border-top-width: 2px;
  border-top-color: #D3D3D3;
  border-bottom-style: solid;
  border-bottom-width: 2px;
  border-bottom-color: #D3D3D3;
  border-left-style: none;
  border-left-width: 1px;
  border-left-color: #D3D3D3;
  border-right-style: none;
  border-right-width: 1px;
  border-right-color: #D3D3D3;
}

#yrynqoxvdg .gt_col_heading {
  color: #FFFFFF;
  background-color: #153331;
  font-size: 100%;
  font-weight: normal;
  text-transform: inherit;
  border-left-style: none;
  border-left-width: 1px;
  border-left-color: #D3D3D3;
  border-right-style: none;
  border-right-width: 1px;
  border-right-color: #D3D3D3;
  vertical-align: bottom;
  padding-top: 5px;
  padding-bottom: 6px;
  padding-left: 5px;
  padding-right: 5px;
  overflow-x: hidden;
}

#yrynqoxvdg .gt_column_spanner_outer {
  color: #FFFFFF;
  background-color: #153331;
  font-size: 100%;
  font-weight: normal;
  text-transform: inherit;
  padding-top: 0;
  padding-bottom: 0;
  padding-left: 4px;
  padding-right: 4px;
}

#yrynqoxvdg .gt_column_spanner_outer:first-child {
  padding-left: 0;
}

#yrynqoxvdg .gt_column_spanner_outer:last-child {
  padding-right: 0;
}

#yrynqoxvdg .gt_column_spanner {
  border-bottom-style: solid;
  border-bottom-width: 2px;
  border-bottom-color: #D3D3D3;
  vertical-align: bottom;
  padding-top: 5px;
  padding-bottom: 5px;
  overflow-x: hidden;
  display: inline-block;
  width: 100%;
}

#yrynqoxvdg .gt_group_heading {
  padding: 8px;
  color: #333333;
  background-color: #FFFFFF;
  font-size: 100%;
  font-weight: initial;
  text-transform: inherit;
  border-top-style: solid;
  border-top-width: 2px;
  border-top-color: #D3D3D3;
  border-bottom-style: solid;
  border-bottom-width: 2px;
  border-bottom-color: #D3D3D3;
  border-left-style: none;
  border-left-width: 1px;
  border-left-color: #D3D3D3;
  border-right-style: none;
  border-right-width: 1px;
  border-right-color: #D3D3D3;
  vertical-align: middle;
}

#yrynqoxvdg .gt_empty_group_heading {
  padding: 0.5px;
  color: #333333;
  background-color: #FFFFFF;
  font-size: 100%;
  font-weight: initial;
  border-top-style: solid;
  border-top-width: 2px;
  border-top-color: #D3D3D3;
  border-bottom-style: solid;
  border-bottom-width: 2px;
  border-bottom-color: #D3D3D3;
  vertical-align: middle;
}

#yrynqoxvdg .gt_from_md > :first-child {
  margin-top: 0;
}

#yrynqoxvdg .gt_from_md > :last-child {
  margin-bottom: 0;
}

#yrynqoxvdg .gt_row {
  padding-top: 8px;
  padding-bottom: 8px;
  padding-left: 5px;
  padding-right: 5px;
  margin: 10px;
  border-top-style: solid;
  border-top-width: 1px;
  border-top-color: #D3D3D3;
  border-left-style: none;
  border-left-width: 1px;
  border-left-color: #D3D3D3;
  border-right-style: none;
  border-right-width: 1px;
  border-right-color: #D3D3D3;
  vertical-align: middle;
  overflow-x: hidden;
}

#yrynqoxvdg .gt_stub {
  color: #333333;
  background-color: #FFFFFF;
  font-size: 100%;
  font-weight: initial;
  text-transform: inherit;
  border-right-style: solid;
  border-right-width: 2px;
  border-right-color: #D3D3D3;
  padding-left: 12px;
}

#yrynqoxvdg .gt_summary_row {
  color: #333333;
  background-color: #FFFFFF;
  text-transform: inherit;
  padding-top: 8px;
  padding-bottom: 8px;
  padding-left: 5px;
  padding-right: 5px;
}

#yrynqoxvdg .gt_first_summary_row {
  padding-top: 8px;
  padding-bottom: 8px;
  padding-left: 5px;
  padding-right: 5px;
  border-top-style: solid;
  border-top-width: 2px;
  border-top-color: #D3D3D3;
}

#yrynqoxvdg .gt_grand_summary_row {
  color: #333333;
  background-color: #FFFFFF;
  text-transform: inherit;
  padding-top: 8px;
  padding-bottom: 8px;
  padding-left: 5px;
  padding-right: 5px;
}

#yrynqoxvdg .gt_first_grand_summary_row {
  padding-top: 8px;
  padding-bottom: 8px;
  padding-left: 5px;
  padding-right: 5px;
  border-top-style: double;
  border-top-width: 6px;
  border-top-color: #D3D3D3;
}

#yrynqoxvdg .gt_striped {
  background-color: rgba(128, 128, 128, 0.05);
}

#yrynqoxvdg .gt_table_body {
  border-top-style: solid;
  border-top-width: 2px;
  border-top-color: #D3D3D3;
  border-bottom-style: solid;
  border-bottom-width: 2px;
  border-bottom-color: #D3D3D3;
}

#yrynqoxvdg .gt_footnotes {
  color: #333333;
  background-color: #FFFFFF;
  border-bottom-style: none;
  border-bottom-width: 2px;
  border-bottom-color: #D3D3D3;
  border-left-style: none;
  border-left-width: 2px;
  border-left-color: #D3D3D3;
  border-right-style: none;
  border-right-width: 2px;
  border-right-color: #D3D3D3;
}

#yrynqoxvdg .gt_footnote {
  margin: 0px;
  font-size: 90%;
  padding: 4px;
}

#yrynqoxvdg .gt_sourcenotes {
  color: #333333;
  background-color: #FFFFFF;
  border-bottom-style: none;
  border-bottom-width: 2px;
  border-bottom-color: #D3D3D3;
  border-left-style: none;
  border-left-width: 2px;
  border-left-color: #D3D3D3;
  border-right-style: none;
  border-right-width: 2px;
  border-right-color: #D3D3D3;
}

#yrynqoxvdg .gt_sourcenote {
  font-size: 90%;
  padding: 4px;
}

#yrynqoxvdg .gt_left {
  text-align: left;
}

#yrynqoxvdg .gt_center {
  text-align: center;
}

#yrynqoxvdg .gt_right {
  text-align: right;
  font-variant-numeric: tabular-nums;
}

#yrynqoxvdg .gt_font_normal {
  font-weight: normal;
}

#yrynqoxvdg .gt_font_bold {
  font-weight: bold;
}

#yrynqoxvdg .gt_font_italic {
  font-style: italic;
}

#yrynqoxvdg .gt_super {
  font-size: 65%;
}

#yrynqoxvdg .gt_footnote_marks {
  font-style: italic;
  font-weight: normal;
  font-size: 65%;
}
</style>
<table class="gt_table" style="table-layout: fixed;; width: 0px">
  <colgroup>
    <col style="width:500px;"/>
    <col style="width:200px;"/>
  </colgroup>
  
  <thead class="gt_col_headings">
    <tr>
      <th class="gt_col_heading gt_columns_bottom_border gt_left" rowspan="1" colspan="1"><strong>Description</strong></th>
      <th class="gt_col_heading gt_columns_bottom_border gt_right" rowspan="1" colspan="1"></th>
    </tr>
  </thead>
  <tbody class="gt_table_body">
    <tr><td class="gt_row gt_left">Method to change all numeric values to character values in a single column of a dataframe</td>
<td class="gt_row gt_right"><svg aria-hidden="true" role="img" viewBox="0 0 512 512" style="height:2em;width:2em;vertical-align:-0.125em;margin-left:auto;margin-right:auto;font-size:inherit;fill:#A62014;overflow:visible;position:relative;"><path d="M330.67 263.12V173.4l-52.75-24.22C219.44 218.76 197.58 400 56 400a56 56 0 0 0 0 112c212.64 0 370.65-122.87 419.18-210.34l-37.05-38.54zm131.09-128.37C493.92 74.91 477.18 26.48 458.62 3a8 8 0 0 0-11.93-.59l-22.9 23a8.06 8.06 0 0 0-.89 10.23c6.86 10.36 17.05 35.1-1.4 72.32A142.85 142.85 0 0 0 364.34 96c-28 0-54 8.54-76.34 22.59l74.67 34.29v78.24h89.09L506.44 288c3.26-12.62 5.56-25.63 5.56-39.31a154 154 0 0 0-50.24-113.94z"/></svg><svg aria-hidden="true" role="img" viewBox="0 0 512 512" style="height:2em;width:2em;vertical-align:-0.125em;margin-left:auto;margin-right:auto;font-size:inherit;fill:#9FC2B9;overflow:visible;position:relative;"><path d="M330.67 263.12V173.4l-52.75-24.22C219.44 218.76 197.58 400 56 400a56 56 0 0 0 0 112c212.64 0 370.65-122.87 419.18-210.34l-37.05-38.54zm131.09-128.37C493.92 74.91 477.18 26.48 458.62 3a8 8 0 0 0-11.93-.59l-22.9 23a8.06 8.06 0 0 0-.89 10.23c6.86 10.36 17.05 35.1-1.4 72.32A142.85 142.85 0 0 0 364.34 96c-28 0-54 8.54-76.34 22.59l74.67 34.29v78.24h89.09L506.44 288c3.26-12.62 5.56-25.63 5.56-39.31a154 154 0 0 0-50.24-113.94z"/></svg><svg aria-hidden="true" role="img" viewBox="0 0 512 512" style="height:2em;width:2em;vertical-align:-0.125em;margin-left:auto;margin-right:auto;font-size:inherit;fill:#9FC2B9;overflow:visible;position:relative;"><path d="M330.67 263.12V173.4l-52.75-24.22C219.44 218.76 197.58 400 56 400a56 56 0 0 0 0 112c212.64 0 370.65-122.87 419.18-210.34l-37.05-38.54zm131.09-128.37C493.92 74.91 477.18 26.48 458.62 3a8 8 0 0 0-11.93-.59l-22.9 23a8.06 8.06 0 0 0-.89 10.23c6.86 10.36 17.05 35.1-1.4 72.32A142.85 142.85 0 0 0 364.34 96c-28 0-54 8.54-76.34 22.59l74.67 34.29v78.24h89.09L506.44 288c3.26-12.62 5.56-25.63 5.56-39.31a154 154 0 0 0-50.24-113.94z"/></svg></td></tr>
  </tbody>
  
  
</table>
</div>
```

```{=html}
<div id="dvchpratwm" style="overflow-x:auto;overflow-y:auto;width:auto;height:auto;">
<style>html {
  font-family: -apple-system, BlinkMacSystemFont, 'Segoe UI', Roboto, Oxygen, Ubuntu, Cantarell, 'Helvetica Neue', 'Fira Sans', 'Droid Sans', Arial, sans-serif;
}

#dvchpratwm .gt_table {
  display: table;
  border-collapse: collapse;
  margin-left: auto;
  margin-right: auto;
  color: #333333;
  font-size: 16px;
  font-weight: normal;
  font-style: normal;
  background-color: #FFFFFF;
  width: auto;
  border-top-style: solid;
  border-top-width: 2px;
  border-top-color: #A8A8A8;
  border-right-style: none;
  border-right-width: 2px;
  border-right-color: #D3D3D3;
  border-bottom-style: solid;
  border-bottom-width: 2px;
  border-bottom-color: #A8A8A8;
  border-left-style: none;
  border-left-width: 2px;
  border-left-color: #D3D3D3;
}

#dvchpratwm .gt_heading {
  background-color: #153331;
  text-align: center;
  border-bottom-color: #FFFFFF;
  border-left-style: none;
  border-left-width: 1px;
  border-left-color: #D3D3D3;
  border-right-style: none;
  border-right-width: 1px;
  border-right-color: #D3D3D3;
}

#dvchpratwm .gt_title {
  color: #FFFFFF;
  font-size: 125%;
  font-weight: initial;
  padding-top: 4px;
  padding-bottom: 4px;
  border-bottom-color: #FFFFFF;
  border-bottom-width: 0;
}

#dvchpratwm .gt_subtitle {
  color: #FFFFFF;
  font-size: 85%;
  font-weight: initial;
  padding-top: 0;
  padding-bottom: 6px;
  border-top-color: #FFFFFF;
  border-top-width: 0;
}

#dvchpratwm .gt_bottom_border {
  border-bottom-style: solid;
  border-bottom-width: 2px;
  border-bottom-color: #D3D3D3;
}

#dvchpratwm .gt_col_headings {
  border-top-style: solid;
  border-top-width: 2px;
  border-top-color: #D3D3D3;
  border-bottom-style: solid;
  border-bottom-width: 2px;
  border-bottom-color: #D3D3D3;
  border-left-style: none;
  border-left-width: 1px;
  border-left-color: #D3D3D3;
  border-right-style: none;
  border-right-width: 1px;
  border-right-color: #D3D3D3;
}

#dvchpratwm .gt_col_heading {
  color: #FFFFFF;
  background-color: #1E6E6E;
  font-size: 100%;
  font-weight: normal;
  text-transform: inherit;
  border-left-style: none;
  border-left-width: 1px;
  border-left-color: #D3D3D3;
  border-right-style: none;
  border-right-width: 1px;
  border-right-color: #D3D3D3;
  vertical-align: bottom;
  padding-top: 5px;
  padding-bottom: 6px;
  padding-left: 5px;
  padding-right: 5px;
  overflow-x: hidden;
}

#dvchpratwm .gt_column_spanner_outer {
  color: #FFFFFF;
  background-color: #1E6E6E;
  font-size: 100%;
  font-weight: normal;
  text-transform: inherit;
  padding-top: 0;
  padding-bottom: 0;
  padding-left: 4px;
  padding-right: 4px;
}

#dvchpratwm .gt_column_spanner_outer:first-child {
  padding-left: 0;
}

#dvchpratwm .gt_column_spanner_outer:last-child {
  padding-right: 0;
}

#dvchpratwm .gt_column_spanner {
  border-bottom-style: solid;
  border-bottom-width: 2px;
  border-bottom-color: #D3D3D3;
  vertical-align: bottom;
  padding-top: 5px;
  padding-bottom: 5px;
  overflow-x: hidden;
  display: inline-block;
  width: 100%;
}

#dvchpratwm .gt_group_heading {
  padding: 8px;
  color: #333333;
  background-color: #FFFFFF;
  font-size: 100%;
  font-weight: initial;
  text-transform: inherit;
  border-top-style: solid;
  border-top-width: 2px;
  border-top-color: #D3D3D3;
  border-bottom-style: solid;
  border-bottom-width: 2px;
  border-bottom-color: #D3D3D3;
  border-left-style: none;
  border-left-width: 1px;
  border-left-color: #D3D3D3;
  border-right-style: none;
  border-right-width: 1px;
  border-right-color: #D3D3D3;
  vertical-align: middle;
}

#dvchpratwm .gt_empty_group_heading {
  padding: 0.5px;
  color: #333333;
  background-color: #FFFFFF;
  font-size: 100%;
  font-weight: initial;
  border-top-style: solid;
  border-top-width: 2px;
  border-top-color: #D3D3D3;
  border-bottom-style: solid;
  border-bottom-width: 2px;
  border-bottom-color: #D3D3D3;
  vertical-align: middle;
}

#dvchpratwm .gt_from_md > :first-child {
  margin-top: 0;
}

#dvchpratwm .gt_from_md > :last-child {
  margin-bottom: 0;
}

#dvchpratwm .gt_row {
  padding-top: 8px;
  padding-bottom: 8px;
  padding-left: 5px;
  padding-right: 5px;
  margin: 10px;
  border-top-style: solid;
  border-top-width: 1px;
  border-top-color: #D3D3D3;
  border-left-style: none;
  border-left-width: 1px;
  border-left-color: #D3D3D3;
  border-right-style: none;
  border-right-width: 1px;
  border-right-color: #D3D3D3;
  vertical-align: middle;
  overflow-x: hidden;
}

#dvchpratwm .gt_stub {
  color: #333333;
  background-color: #FFFFFF;
  font-size: 100%;
  font-weight: initial;
  text-transform: inherit;
  border-right-style: solid;
  border-right-width: 2px;
  border-right-color: #D3D3D3;
  padding-left: 12px;
}

#dvchpratwm .gt_summary_row {
  color: #333333;
  background-color: #FFFFFF;
  text-transform: inherit;
  padding-top: 8px;
  padding-bottom: 8px;
  padding-left: 5px;
  padding-right: 5px;
}

#dvchpratwm .gt_first_summary_row {
  padding-top: 8px;
  padding-bottom: 8px;
  padding-left: 5px;
  padding-right: 5px;
  border-top-style: solid;
  border-top-width: 2px;
  border-top-color: #D3D3D3;
}

#dvchpratwm .gt_grand_summary_row {
  color: #333333;
  background-color: #FFFFFF;
  text-transform: inherit;
  padding-top: 8px;
  padding-bottom: 8px;
  padding-left: 5px;
  padding-right: 5px;
}

#dvchpratwm .gt_first_grand_summary_row {
  padding-top: 8px;
  padding-bottom: 8px;
  padding-left: 5px;
  padding-right: 5px;
  border-top-style: double;
  border-top-width: 6px;
  border-top-color: #D3D3D3;
}

#dvchpratwm .gt_striped {
  background-color: rgba(128, 128, 128, 0.05);
}

#dvchpratwm .gt_table_body {
  border-top-style: solid;
  border-top-width: 2px;
  border-top-color: #D3D3D3;
  border-bottom-style: solid;
  border-bottom-width: 2px;
  border-bottom-color: #D3D3D3;
}

#dvchpratwm .gt_footnotes {
  color: #333333;
  background-color: #FFFFFF;
  border-bottom-style: none;
  border-bottom-width: 2px;
  border-bottom-color: #D3D3D3;
  border-left-style: none;
  border-left-width: 2px;
  border-left-color: #D3D3D3;
  border-right-style: none;
  border-right-width: 2px;
  border-right-color: #D3D3D3;
}

#dvchpratwm .gt_footnote {
  margin: 0px;
  font-size: 90%;
  padding: 4px;
}

#dvchpratwm .gt_sourcenotes {
  color: #333333;
  background-color: #FFFFFF;
  border-bottom-style: none;
  border-bottom-width: 2px;
  border-bottom-color: #D3D3D3;
  border-left-style: none;
  border-left-width: 2px;
  border-left-color: #D3D3D3;
  border-right-style: none;
  border-right-width: 2px;
  border-right-color: #D3D3D3;
}

#dvchpratwm .gt_sourcenote {
  font-size: 90%;
  padding: 4px;
}

#dvchpratwm .gt_left {
  text-align: left;
}

#dvchpratwm .gt_center {
  text-align: center;
}

#dvchpratwm .gt_right {
  text-align: right;
  font-variant-numeric: tabular-nums;
}

#dvchpratwm .gt_font_normal {
  font-weight: normal;
}

#dvchpratwm .gt_font_bold {
  font-weight: bold;
}

#dvchpratwm .gt_font_italic {
  font-style: italic;
}

#dvchpratwm .gt_super {
  font-size: 65%;
}

#dvchpratwm .gt_footnote_marks {
  font-style: italic;
  font-weight: normal;
  font-size: 65%;
}
</style>
<table class="gt_table" style="table-layout: fixed;; width: 0px">
  <colgroup>
    <col style="width:350px;"/>
    <col style="width:350px;"/>
  </colgroup>
  <thead class="gt_header">
    <tr>
      <th colspan="2" class="gt_heading gt_title gt_font_normal gt_bottom_border" style>Ingredients</th>
    </tr>
    
  </thead>
  <thead class="gt_col_headings">
    <tr>
      <th class="gt_col_heading gt_columns_bottom_border gt_center" rowspan="1" colspan="1"><strong>Package</strong></th>
      <th class="gt_col_heading gt_columns_bottom_border gt_center" rowspan="1" colspan="1"><strong>Data</strong></th>
    </tr>
  </thead>
  <tbody class="gt_table_body">
    <tr><td class="gt_row gt_center"><div class='gt_from_md'><p>readr<br>dplyr</p>
</div></td>
<td class="gt_row gt_center"><div class='gt_from_md'><p>sample.csv</p>
</div></td></tr>
  </tbody>
  
  
</table>
</div>
```

</br>

**Preparation**

```r
df <- readr::read_csv("C:/data/sample.csv")
```

</br>

**Sample Instructions**

```r
package::function(data, column_name = as.character(column_name))
```

</br>

**Actual Instructions**

```r
dplyr::mutate(df, column1 = as.character(column1))
```


### Change character data type to date data type in single column

```{=html}
<div id="pdbaotigyv" style="overflow-x:auto;overflow-y:auto;width:auto;height:auto;">
<style>html {
  font-family: -apple-system, BlinkMacSystemFont, 'Segoe UI', Roboto, Oxygen, Ubuntu, Cantarell, 'Helvetica Neue', 'Fira Sans', 'Droid Sans', Arial, sans-serif;
}

#pdbaotigyv .gt_table {
  display: table;
  border-collapse: collapse;
  margin-left: auto;
  margin-right: auto;
  color: #333333;
  font-size: 16px;
  font-weight: normal;
  font-style: normal;
  background-color: #FFFFFF;
  width: auto;
  border-top-style: solid;
  border-top-width: 2px;
  border-top-color: #A8A8A8;
  border-right-style: none;
  border-right-width: 2px;
  border-right-color: #D3D3D3;
  border-bottom-style: solid;
  border-bottom-width: 2px;
  border-bottom-color: #A8A8A8;
  border-left-style: none;
  border-left-width: 2px;
  border-left-color: #D3D3D3;
}

#pdbaotigyv .gt_heading {
  background-color: #153331;
  text-align: center;
  border-bottom-color: #FFFFFF;
  border-left-style: none;
  border-left-width: 1px;
  border-left-color: #D3D3D3;
  border-right-style: none;
  border-right-width: 1px;
  border-right-color: #D3D3D3;
}

#pdbaotigyv .gt_title {
  color: #FFFFFF;
  font-size: 125%;
  font-weight: initial;
  padding-top: 4px;
  padding-bottom: 4px;
  border-bottom-color: #FFFFFF;
  border-bottom-width: 0;
}

#pdbaotigyv .gt_subtitle {
  color: #FFFFFF;
  font-size: 85%;
  font-weight: initial;
  padding-top: 0;
  padding-bottom: 6px;
  border-top-color: #FFFFFF;
  border-top-width: 0;
}

#pdbaotigyv .gt_bottom_border {
  border-bottom-style: solid;
  border-bottom-width: 2px;
  border-bottom-color: #D3D3D3;
}

#pdbaotigyv .gt_col_headings {
  border-top-style: solid;
  border-top-width: 2px;
  border-top-color: #D3D3D3;
  border-bottom-style: solid;
  border-bottom-width: 2px;
  border-bottom-color: #D3D3D3;
  border-left-style: none;
  border-left-width: 1px;
  border-left-color: #D3D3D3;
  border-right-style: none;
  border-right-width: 1px;
  border-right-color: #D3D3D3;
}

#pdbaotigyv .gt_col_heading {
  color: #FFFFFF;
  background-color: #153331;
  font-size: 100%;
  font-weight: normal;
  text-transform: inherit;
  border-left-style: none;
  border-left-width: 1px;
  border-left-color: #D3D3D3;
  border-right-style: none;
  border-right-width: 1px;
  border-right-color: #D3D3D3;
  vertical-align: bottom;
  padding-top: 5px;
  padding-bottom: 6px;
  padding-left: 5px;
  padding-right: 5px;
  overflow-x: hidden;
}

#pdbaotigyv .gt_column_spanner_outer {
  color: #FFFFFF;
  background-color: #153331;
  font-size: 100%;
  font-weight: normal;
  text-transform: inherit;
  padding-top: 0;
  padding-bottom: 0;
  padding-left: 4px;
  padding-right: 4px;
}

#pdbaotigyv .gt_column_spanner_outer:first-child {
  padding-left: 0;
}

#pdbaotigyv .gt_column_spanner_outer:last-child {
  padding-right: 0;
}

#pdbaotigyv .gt_column_spanner {
  border-bottom-style: solid;
  border-bottom-width: 2px;
  border-bottom-color: #D3D3D3;
  vertical-align: bottom;
  padding-top: 5px;
  padding-bottom: 5px;
  overflow-x: hidden;
  display: inline-block;
  width: 100%;
}

#pdbaotigyv .gt_group_heading {
  padding: 8px;
  color: #333333;
  background-color: #FFFFFF;
  font-size: 100%;
  font-weight: initial;
  text-transform: inherit;
  border-top-style: solid;
  border-top-width: 2px;
  border-top-color: #D3D3D3;
  border-bottom-style: solid;
  border-bottom-width: 2px;
  border-bottom-color: #D3D3D3;
  border-left-style: none;
  border-left-width: 1px;
  border-left-color: #D3D3D3;
  border-right-style: none;
  border-right-width: 1px;
  border-right-color: #D3D3D3;
  vertical-align: middle;
}

#pdbaotigyv .gt_empty_group_heading {
  padding: 0.5px;
  color: #333333;
  background-color: #FFFFFF;
  font-size: 100%;
  font-weight: initial;
  border-top-style: solid;
  border-top-width: 2px;
  border-top-color: #D3D3D3;
  border-bottom-style: solid;
  border-bottom-width: 2px;
  border-bottom-color: #D3D3D3;
  vertical-align: middle;
}

#pdbaotigyv .gt_from_md > :first-child {
  margin-top: 0;
}

#pdbaotigyv .gt_from_md > :last-child {
  margin-bottom: 0;
}

#pdbaotigyv .gt_row {
  padding-top: 8px;
  padding-bottom: 8px;
  padding-left: 5px;
  padding-right: 5px;
  margin: 10px;
  border-top-style: solid;
  border-top-width: 1px;
  border-top-color: #D3D3D3;
  border-left-style: none;
  border-left-width: 1px;
  border-left-color: #D3D3D3;
  border-right-style: none;
  border-right-width: 1px;
  border-right-color: #D3D3D3;
  vertical-align: middle;
  overflow-x: hidden;
}

#pdbaotigyv .gt_stub {
  color: #333333;
  background-color: #FFFFFF;
  font-size: 100%;
  font-weight: initial;
  text-transform: inherit;
  border-right-style: solid;
  border-right-width: 2px;
  border-right-color: #D3D3D3;
  padding-left: 12px;
}

#pdbaotigyv .gt_summary_row {
  color: #333333;
  background-color: #FFFFFF;
  text-transform: inherit;
  padding-top: 8px;
  padding-bottom: 8px;
  padding-left: 5px;
  padding-right: 5px;
}

#pdbaotigyv .gt_first_summary_row {
  padding-top: 8px;
  padding-bottom: 8px;
  padding-left: 5px;
  padding-right: 5px;
  border-top-style: solid;
  border-top-width: 2px;
  border-top-color: #D3D3D3;
}

#pdbaotigyv .gt_grand_summary_row {
  color: #333333;
  background-color: #FFFFFF;
  text-transform: inherit;
  padding-top: 8px;
  padding-bottom: 8px;
  padding-left: 5px;
  padding-right: 5px;
}

#pdbaotigyv .gt_first_grand_summary_row {
  padding-top: 8px;
  padding-bottom: 8px;
  padding-left: 5px;
  padding-right: 5px;
  border-top-style: double;
  border-top-width: 6px;
  border-top-color: #D3D3D3;
}

#pdbaotigyv .gt_striped {
  background-color: rgba(128, 128, 128, 0.05);
}

#pdbaotigyv .gt_table_body {
  border-top-style: solid;
  border-top-width: 2px;
  border-top-color: #D3D3D3;
  border-bottom-style: solid;
  border-bottom-width: 2px;
  border-bottom-color: #D3D3D3;
}

#pdbaotigyv .gt_footnotes {
  color: #333333;
  background-color: #FFFFFF;
  border-bottom-style: none;
  border-bottom-width: 2px;
  border-bottom-color: #D3D3D3;
  border-left-style: none;
  border-left-width: 2px;
  border-left-color: #D3D3D3;
  border-right-style: none;
  border-right-width: 2px;
  border-right-color: #D3D3D3;
}

#pdbaotigyv .gt_footnote {
  margin: 0px;
  font-size: 90%;
  padding: 4px;
}

#pdbaotigyv .gt_sourcenotes {
  color: #333333;
  background-color: #FFFFFF;
  border-bottom-style: none;
  border-bottom-width: 2px;
  border-bottom-color: #D3D3D3;
  border-left-style: none;
  border-left-width: 2px;
  border-left-color: #D3D3D3;
  border-right-style: none;
  border-right-width: 2px;
  border-right-color: #D3D3D3;
}

#pdbaotigyv .gt_sourcenote {
  font-size: 90%;
  padding: 4px;
}

#pdbaotigyv .gt_left {
  text-align: left;
}

#pdbaotigyv .gt_center {
  text-align: center;
}

#pdbaotigyv .gt_right {
  text-align: right;
  font-variant-numeric: tabular-nums;
}

#pdbaotigyv .gt_font_normal {
  font-weight: normal;
}

#pdbaotigyv .gt_font_bold {
  font-weight: bold;
}

#pdbaotigyv .gt_font_italic {
  font-style: italic;
}

#pdbaotigyv .gt_super {
  font-size: 65%;
}

#pdbaotigyv .gt_footnote_marks {
  font-style: italic;
  font-weight: normal;
  font-size: 65%;
}
</style>
<table class="gt_table" style="table-layout: fixed;; width: 0px">
  <colgroup>
    <col style="width:500px;"/>
    <col style="width:200px;"/>
  </colgroup>
  
  <thead class="gt_col_headings">
    <tr>
      <th class="gt_col_heading gt_columns_bottom_border gt_left" rowspan="1" colspan="1"><strong>Description</strong></th>
      <th class="gt_col_heading gt_columns_bottom_border gt_right" rowspan="1" colspan="1"></th>
    </tr>
  </thead>
  <tbody class="gt_table_body">
    <tr><td class="gt_row gt_left">Method to change all character values to date values in a single column of a dataframe</td>
<td class="gt_row gt_right"><svg aria-hidden="true" role="img" viewBox="0 0 512 512" style="height:2em;width:2em;vertical-align:-0.125em;margin-left:auto;margin-right:auto;font-size:inherit;fill:#A62014;overflow:visible;position:relative;"><path d="M330.67 263.12V173.4l-52.75-24.22C219.44 218.76 197.58 400 56 400a56 56 0 0 0 0 112c212.64 0 370.65-122.87 419.18-210.34l-37.05-38.54zm131.09-128.37C493.92 74.91 477.18 26.48 458.62 3a8 8 0 0 0-11.93-.59l-22.9 23a8.06 8.06 0 0 0-.89 10.23c6.86 10.36 17.05 35.1-1.4 72.32A142.85 142.85 0 0 0 364.34 96c-28 0-54 8.54-76.34 22.59l74.67 34.29v78.24h89.09L506.44 288c3.26-12.62 5.56-25.63 5.56-39.31a154 154 0 0 0-50.24-113.94z"/></svg><svg aria-hidden="true" role="img" viewBox="0 0 512 512" style="height:2em;width:2em;vertical-align:-0.125em;margin-left:auto;margin-right:auto;font-size:inherit;fill:#9FC2B9;overflow:visible;position:relative;"><path d="M330.67 263.12V173.4l-52.75-24.22C219.44 218.76 197.58 400 56 400a56 56 0 0 0 0 112c212.64 0 370.65-122.87 419.18-210.34l-37.05-38.54zm131.09-128.37C493.92 74.91 477.18 26.48 458.62 3a8 8 0 0 0-11.93-.59l-22.9 23a8.06 8.06 0 0 0-.89 10.23c6.86 10.36 17.05 35.1-1.4 72.32A142.85 142.85 0 0 0 364.34 96c-28 0-54 8.54-76.34 22.59l74.67 34.29v78.24h89.09L506.44 288c3.26-12.62 5.56-25.63 5.56-39.31a154 154 0 0 0-50.24-113.94z"/></svg><svg aria-hidden="true" role="img" viewBox="0 0 512 512" style="height:2em;width:2em;vertical-align:-0.125em;margin-left:auto;margin-right:auto;font-size:inherit;fill:#9FC2B9;overflow:visible;position:relative;"><path d="M330.67 263.12V173.4l-52.75-24.22C219.44 218.76 197.58 400 56 400a56 56 0 0 0 0 112c212.64 0 370.65-122.87 419.18-210.34l-37.05-38.54zm131.09-128.37C493.92 74.91 477.18 26.48 458.62 3a8 8 0 0 0-11.93-.59l-22.9 23a8.06 8.06 0 0 0-.89 10.23c6.86 10.36 17.05 35.1-1.4 72.32A142.85 142.85 0 0 0 364.34 96c-28 0-54 8.54-76.34 22.59l74.67 34.29v78.24h89.09L506.44 288c3.26-12.62 5.56-25.63 5.56-39.31a154 154 0 0 0-50.24-113.94z"/></svg></td></tr>
  </tbody>
  
  
</table>
</div>
```

```{=html}
<div id="gijfoatkmu" style="overflow-x:auto;overflow-y:auto;width:auto;height:auto;">
<style>html {
  font-family: -apple-system, BlinkMacSystemFont, 'Segoe UI', Roboto, Oxygen, Ubuntu, Cantarell, 'Helvetica Neue', 'Fira Sans', 'Droid Sans', Arial, sans-serif;
}

#gijfoatkmu .gt_table {
  display: table;
  border-collapse: collapse;
  margin-left: auto;
  margin-right: auto;
  color: #333333;
  font-size: 16px;
  font-weight: normal;
  font-style: normal;
  background-color: #FFFFFF;
  width: auto;
  border-top-style: solid;
  border-top-width: 2px;
  border-top-color: #A8A8A8;
  border-right-style: none;
  border-right-width: 2px;
  border-right-color: #D3D3D3;
  border-bottom-style: solid;
  border-bottom-width: 2px;
  border-bottom-color: #A8A8A8;
  border-left-style: none;
  border-left-width: 2px;
  border-left-color: #D3D3D3;
}

#gijfoatkmu .gt_heading {
  background-color: #153331;
  text-align: center;
  border-bottom-color: #FFFFFF;
  border-left-style: none;
  border-left-width: 1px;
  border-left-color: #D3D3D3;
  border-right-style: none;
  border-right-width: 1px;
  border-right-color: #D3D3D3;
}

#gijfoatkmu .gt_title {
  color: #FFFFFF;
  font-size: 125%;
  font-weight: initial;
  padding-top: 4px;
  padding-bottom: 4px;
  border-bottom-color: #FFFFFF;
  border-bottom-width: 0;
}

#gijfoatkmu .gt_subtitle {
  color: #FFFFFF;
  font-size: 85%;
  font-weight: initial;
  padding-top: 0;
  padding-bottom: 6px;
  border-top-color: #FFFFFF;
  border-top-width: 0;
}

#gijfoatkmu .gt_bottom_border {
  border-bottom-style: solid;
  border-bottom-width: 2px;
  border-bottom-color: #D3D3D3;
}

#gijfoatkmu .gt_col_headings {
  border-top-style: solid;
  border-top-width: 2px;
  border-top-color: #D3D3D3;
  border-bottom-style: solid;
  border-bottom-width: 2px;
  border-bottom-color: #D3D3D3;
  border-left-style: none;
  border-left-width: 1px;
  border-left-color: #D3D3D3;
  border-right-style: none;
  border-right-width: 1px;
  border-right-color: #D3D3D3;
}

#gijfoatkmu .gt_col_heading {
  color: #FFFFFF;
  background-color: #1E6E6E;
  font-size: 100%;
  font-weight: normal;
  text-transform: inherit;
  border-left-style: none;
  border-left-width: 1px;
  border-left-color: #D3D3D3;
  border-right-style: none;
  border-right-width: 1px;
  border-right-color: #D3D3D3;
  vertical-align: bottom;
  padding-top: 5px;
  padding-bottom: 6px;
  padding-left: 5px;
  padding-right: 5px;
  overflow-x: hidden;
}

#gijfoatkmu .gt_column_spanner_outer {
  color: #FFFFFF;
  background-color: #1E6E6E;
  font-size: 100%;
  font-weight: normal;
  text-transform: inherit;
  padding-top: 0;
  padding-bottom: 0;
  padding-left: 4px;
  padding-right: 4px;
}

#gijfoatkmu .gt_column_spanner_outer:first-child {
  padding-left: 0;
}

#gijfoatkmu .gt_column_spanner_outer:last-child {
  padding-right: 0;
}

#gijfoatkmu .gt_column_spanner {
  border-bottom-style: solid;
  border-bottom-width: 2px;
  border-bottom-color: #D3D3D3;
  vertical-align: bottom;
  padding-top: 5px;
  padding-bottom: 5px;
  overflow-x: hidden;
  display: inline-block;
  width: 100%;
}

#gijfoatkmu .gt_group_heading {
  padding: 8px;
  color: #333333;
  background-color: #FFFFFF;
  font-size: 100%;
  font-weight: initial;
  text-transform: inherit;
  border-top-style: solid;
  border-top-width: 2px;
  border-top-color: #D3D3D3;
  border-bottom-style: solid;
  border-bottom-width: 2px;
  border-bottom-color: #D3D3D3;
  border-left-style: none;
  border-left-width: 1px;
  border-left-color: #D3D3D3;
  border-right-style: none;
  border-right-width: 1px;
  border-right-color: #D3D3D3;
  vertical-align: middle;
}

#gijfoatkmu .gt_empty_group_heading {
  padding: 0.5px;
  color: #333333;
  background-color: #FFFFFF;
  font-size: 100%;
  font-weight: initial;
  border-top-style: solid;
  border-top-width: 2px;
  border-top-color: #D3D3D3;
  border-bottom-style: solid;
  border-bottom-width: 2px;
  border-bottom-color: #D3D3D3;
  vertical-align: middle;
}

#gijfoatkmu .gt_from_md > :first-child {
  margin-top: 0;
}

#gijfoatkmu .gt_from_md > :last-child {
  margin-bottom: 0;
}

#gijfoatkmu .gt_row {
  padding-top: 8px;
  padding-bottom: 8px;
  padding-left: 5px;
  padding-right: 5px;
  margin: 10px;
  border-top-style: solid;
  border-top-width: 1px;
  border-top-color: #D3D3D3;
  border-left-style: none;
  border-left-width: 1px;
  border-left-color: #D3D3D3;
  border-right-style: none;
  border-right-width: 1px;
  border-right-color: #D3D3D3;
  vertical-align: middle;
  overflow-x: hidden;
}

#gijfoatkmu .gt_stub {
  color: #333333;
  background-color: #FFFFFF;
  font-size: 100%;
  font-weight: initial;
  text-transform: inherit;
  border-right-style: solid;
  border-right-width: 2px;
  border-right-color: #D3D3D3;
  padding-left: 12px;
}

#gijfoatkmu .gt_summary_row {
  color: #333333;
  background-color: #FFFFFF;
  text-transform: inherit;
  padding-top: 8px;
  padding-bottom: 8px;
  padding-left: 5px;
  padding-right: 5px;
}

#gijfoatkmu .gt_first_summary_row {
  padding-top: 8px;
  padding-bottom: 8px;
  padding-left: 5px;
  padding-right: 5px;
  border-top-style: solid;
  border-top-width: 2px;
  border-top-color: #D3D3D3;
}

#gijfoatkmu .gt_grand_summary_row {
  color: #333333;
  background-color: #FFFFFF;
  text-transform: inherit;
  padding-top: 8px;
  padding-bottom: 8px;
  padding-left: 5px;
  padding-right: 5px;
}

#gijfoatkmu .gt_first_grand_summary_row {
  padding-top: 8px;
  padding-bottom: 8px;
  padding-left: 5px;
  padding-right: 5px;
  border-top-style: double;
  border-top-width: 6px;
  border-top-color: #D3D3D3;
}

#gijfoatkmu .gt_striped {
  background-color: rgba(128, 128, 128, 0.05);
}

#gijfoatkmu .gt_table_body {
  border-top-style: solid;
  border-top-width: 2px;
  border-top-color: #D3D3D3;
  border-bottom-style: solid;
  border-bottom-width: 2px;
  border-bottom-color: #D3D3D3;
}

#gijfoatkmu .gt_footnotes {
  color: #333333;
  background-color: #FFFFFF;
  border-bottom-style: none;
  border-bottom-width: 2px;
  border-bottom-color: #D3D3D3;
  border-left-style: none;
  border-left-width: 2px;
  border-left-color: #D3D3D3;
  border-right-style: none;
  border-right-width: 2px;
  border-right-color: #D3D3D3;
}

#gijfoatkmu .gt_footnote {
  margin: 0px;
  font-size: 90%;
  padding: 4px;
}

#gijfoatkmu .gt_sourcenotes {
  color: #333333;
  background-color: #FFFFFF;
  border-bottom-style: none;
  border-bottom-width: 2px;
  border-bottom-color: #D3D3D3;
  border-left-style: none;
  border-left-width: 2px;
  border-left-color: #D3D3D3;
  border-right-style: none;
  border-right-width: 2px;
  border-right-color: #D3D3D3;
}

#gijfoatkmu .gt_sourcenote {
  font-size: 90%;
  padding: 4px;
}

#gijfoatkmu .gt_left {
  text-align: left;
}

#gijfoatkmu .gt_center {
  text-align: center;
}

#gijfoatkmu .gt_right {
  text-align: right;
  font-variant-numeric: tabular-nums;
}

#gijfoatkmu .gt_font_normal {
  font-weight: normal;
}

#gijfoatkmu .gt_font_bold {
  font-weight: bold;
}

#gijfoatkmu .gt_font_italic {
  font-style: italic;
}

#gijfoatkmu .gt_super {
  font-size: 65%;
}

#gijfoatkmu .gt_footnote_marks {
  font-style: italic;
  font-weight: normal;
  font-size: 65%;
}
</style>
<table class="gt_table" style="table-layout: fixed;; width: 0px">
  <colgroup>
    <col style="width:350px;"/>
    <col style="width:350px;"/>
  </colgroup>
  <thead class="gt_header">
    <tr>
      <th colspan="2" class="gt_heading gt_title gt_font_normal gt_bottom_border" style>Ingredients</th>
    </tr>
    
  </thead>
  <thead class="gt_col_headings">
    <tr>
      <th class="gt_col_heading gt_columns_bottom_border gt_center" rowspan="1" colspan="1"><strong>Package</strong></th>
      <th class="gt_col_heading gt_columns_bottom_border gt_center" rowspan="1" colspan="1"><strong>Data</strong></th>
    </tr>
  </thead>
  <tbody class="gt_table_body">
    <tr><td class="gt_row gt_center"><div class='gt_from_md'><p>readr<br>dplyr</p>
</div></td>
<td class="gt_row gt_center"><div class='gt_from_md'><p>sample.csv</p>
</div></td></tr>
  </tbody>
  
  
</table>
</div>
```

</br>

**Preparation**

```r
df <- readr::read_csv("C:/data/sample.csv")
```

</br>

**Sample Instructions**

```r
package::function(data, column_name = as.Date(column_name))
```

</br>

**Actual Instructions**

```r
dplyr::mutate(df, column1 = as.Date(column1))
```


### Change all character data columns to numeric data

```{=html}
<div id="goydlbxkmc" style="overflow-x:auto;overflow-y:auto;width:auto;height:auto;">
<style>html {
  font-family: -apple-system, BlinkMacSystemFont, 'Segoe UI', Roboto, Oxygen, Ubuntu, Cantarell, 'Helvetica Neue', 'Fira Sans', 'Droid Sans', Arial, sans-serif;
}

#goydlbxkmc .gt_table {
  display: table;
  border-collapse: collapse;
  margin-left: auto;
  margin-right: auto;
  color: #333333;
  font-size: 16px;
  font-weight: normal;
  font-style: normal;
  background-color: #FFFFFF;
  width: auto;
  border-top-style: solid;
  border-top-width: 2px;
  border-top-color: #A8A8A8;
  border-right-style: none;
  border-right-width: 2px;
  border-right-color: #D3D3D3;
  border-bottom-style: solid;
  border-bottom-width: 2px;
  border-bottom-color: #A8A8A8;
  border-left-style: none;
  border-left-width: 2px;
  border-left-color: #D3D3D3;
}

#goydlbxkmc .gt_heading {
  background-color: #153331;
  text-align: center;
  border-bottom-color: #FFFFFF;
  border-left-style: none;
  border-left-width: 1px;
  border-left-color: #D3D3D3;
  border-right-style: none;
  border-right-width: 1px;
  border-right-color: #D3D3D3;
}

#goydlbxkmc .gt_title {
  color: #FFFFFF;
  font-size: 125%;
  font-weight: initial;
  padding-top: 4px;
  padding-bottom: 4px;
  border-bottom-color: #FFFFFF;
  border-bottom-width: 0;
}

#goydlbxkmc .gt_subtitle {
  color: #FFFFFF;
  font-size: 85%;
  font-weight: initial;
  padding-top: 0;
  padding-bottom: 6px;
  border-top-color: #FFFFFF;
  border-top-width: 0;
}

#goydlbxkmc .gt_bottom_border {
  border-bottom-style: solid;
  border-bottom-width: 2px;
  border-bottom-color: #D3D3D3;
}

#goydlbxkmc .gt_col_headings {
  border-top-style: solid;
  border-top-width: 2px;
  border-top-color: #D3D3D3;
  border-bottom-style: solid;
  border-bottom-width: 2px;
  border-bottom-color: #D3D3D3;
  border-left-style: none;
  border-left-width: 1px;
  border-left-color: #D3D3D3;
  border-right-style: none;
  border-right-width: 1px;
  border-right-color: #D3D3D3;
}

#goydlbxkmc .gt_col_heading {
  color: #FFFFFF;
  background-color: #153331;
  font-size: 100%;
  font-weight: normal;
  text-transform: inherit;
  border-left-style: none;
  border-left-width: 1px;
  border-left-color: #D3D3D3;
  border-right-style: none;
  border-right-width: 1px;
  border-right-color: #D3D3D3;
  vertical-align: bottom;
  padding-top: 5px;
  padding-bottom: 6px;
  padding-left: 5px;
  padding-right: 5px;
  overflow-x: hidden;
}

#goydlbxkmc .gt_column_spanner_outer {
  color: #FFFFFF;
  background-color: #153331;
  font-size: 100%;
  font-weight: normal;
  text-transform: inherit;
  padding-top: 0;
  padding-bottom: 0;
  padding-left: 4px;
  padding-right: 4px;
}

#goydlbxkmc .gt_column_spanner_outer:first-child {
  padding-left: 0;
}

#goydlbxkmc .gt_column_spanner_outer:last-child {
  padding-right: 0;
}

#goydlbxkmc .gt_column_spanner {
  border-bottom-style: solid;
  border-bottom-width: 2px;
  border-bottom-color: #D3D3D3;
  vertical-align: bottom;
  padding-top: 5px;
  padding-bottom: 5px;
  overflow-x: hidden;
  display: inline-block;
  width: 100%;
}

#goydlbxkmc .gt_group_heading {
  padding: 8px;
  color: #333333;
  background-color: #FFFFFF;
  font-size: 100%;
  font-weight: initial;
  text-transform: inherit;
  border-top-style: solid;
  border-top-width: 2px;
  border-top-color: #D3D3D3;
  border-bottom-style: solid;
  border-bottom-width: 2px;
  border-bottom-color: #D3D3D3;
  border-left-style: none;
  border-left-width: 1px;
  border-left-color: #D3D3D3;
  border-right-style: none;
  border-right-width: 1px;
  border-right-color: #D3D3D3;
  vertical-align: middle;
}

#goydlbxkmc .gt_empty_group_heading {
  padding: 0.5px;
  color: #333333;
  background-color: #FFFFFF;
  font-size: 100%;
  font-weight: initial;
  border-top-style: solid;
  border-top-width: 2px;
  border-top-color: #D3D3D3;
  border-bottom-style: solid;
  border-bottom-width: 2px;
  border-bottom-color: #D3D3D3;
  vertical-align: middle;
}

#goydlbxkmc .gt_from_md > :first-child {
  margin-top: 0;
}

#goydlbxkmc .gt_from_md > :last-child {
  margin-bottom: 0;
}

#goydlbxkmc .gt_row {
  padding-top: 8px;
  padding-bottom: 8px;
  padding-left: 5px;
  padding-right: 5px;
  margin: 10px;
  border-top-style: solid;
  border-top-width: 1px;
  border-top-color: #D3D3D3;
  border-left-style: none;
  border-left-width: 1px;
  border-left-color: #D3D3D3;
  border-right-style: none;
  border-right-width: 1px;
  border-right-color: #D3D3D3;
  vertical-align: middle;
  overflow-x: hidden;
}

#goydlbxkmc .gt_stub {
  color: #333333;
  background-color: #FFFFFF;
  font-size: 100%;
  font-weight: initial;
  text-transform: inherit;
  border-right-style: solid;
  border-right-width: 2px;
  border-right-color: #D3D3D3;
  padding-left: 12px;
}

#goydlbxkmc .gt_summary_row {
  color: #333333;
  background-color: #FFFFFF;
  text-transform: inherit;
  padding-top: 8px;
  padding-bottom: 8px;
  padding-left: 5px;
  padding-right: 5px;
}

#goydlbxkmc .gt_first_summary_row {
  padding-top: 8px;
  padding-bottom: 8px;
  padding-left: 5px;
  padding-right: 5px;
  border-top-style: solid;
  border-top-width: 2px;
  border-top-color: #D3D3D3;
}

#goydlbxkmc .gt_grand_summary_row {
  color: #333333;
  background-color: #FFFFFF;
  text-transform: inherit;
  padding-top: 8px;
  padding-bottom: 8px;
  padding-left: 5px;
  padding-right: 5px;
}

#goydlbxkmc .gt_first_grand_summary_row {
  padding-top: 8px;
  padding-bottom: 8px;
  padding-left: 5px;
  padding-right: 5px;
  border-top-style: double;
  border-top-width: 6px;
  border-top-color: #D3D3D3;
}

#goydlbxkmc .gt_striped {
  background-color: rgba(128, 128, 128, 0.05);
}

#goydlbxkmc .gt_table_body {
  border-top-style: solid;
  border-top-width: 2px;
  border-top-color: #D3D3D3;
  border-bottom-style: solid;
  border-bottom-width: 2px;
  border-bottom-color: #D3D3D3;
}

#goydlbxkmc .gt_footnotes {
  color: #333333;
  background-color: #FFFFFF;
  border-bottom-style: none;
  border-bottom-width: 2px;
  border-bottom-color: #D3D3D3;
  border-left-style: none;
  border-left-width: 2px;
  border-left-color: #D3D3D3;
  border-right-style: none;
  border-right-width: 2px;
  border-right-color: #D3D3D3;
}

#goydlbxkmc .gt_footnote {
  margin: 0px;
  font-size: 90%;
  padding: 4px;
}

#goydlbxkmc .gt_sourcenotes {
  color: #333333;
  background-color: #FFFFFF;
  border-bottom-style: none;
  border-bottom-width: 2px;
  border-bottom-color: #D3D3D3;
  border-left-style: none;
  border-left-width: 2px;
  border-left-color: #D3D3D3;
  border-right-style: none;
  border-right-width: 2px;
  border-right-color: #D3D3D3;
}

#goydlbxkmc .gt_sourcenote {
  font-size: 90%;
  padding: 4px;
}

#goydlbxkmc .gt_left {
  text-align: left;
}

#goydlbxkmc .gt_center {
  text-align: center;
}

#goydlbxkmc .gt_right {
  text-align: right;
  font-variant-numeric: tabular-nums;
}

#goydlbxkmc .gt_font_normal {
  font-weight: normal;
}

#goydlbxkmc .gt_font_bold {
  font-weight: bold;
}

#goydlbxkmc .gt_font_italic {
  font-style: italic;
}

#goydlbxkmc .gt_super {
  font-size: 65%;
}

#goydlbxkmc .gt_footnote_marks {
  font-style: italic;
  font-weight: normal;
  font-size: 65%;
}
</style>
<table class="gt_table" style="table-layout: fixed;; width: 0px">
  <colgroup>
    <col style="width:500px;"/>
    <col style="width:200px;"/>
  </colgroup>
  
  <thead class="gt_col_headings">
    <tr>
      <th class="gt_col_heading gt_columns_bottom_border gt_left" rowspan="1" colspan="1"><strong>Description</strong></th>
      <th class="gt_col_heading gt_columns_bottom_border gt_right" rowspan="1" colspan="1"></th>
    </tr>
  </thead>
  <tbody class="gt_table_body">
    <tr><td class="gt_row gt_left">Method to change all character values to numeric values in all character columns of a dataframe</td>
<td class="gt_row gt_right"><svg aria-hidden="true" role="img" viewBox="0 0 512 512" style="height:2em;width:2em;vertical-align:-0.125em;margin-left:auto;margin-right:auto;font-size:inherit;fill:#A62014;overflow:visible;position:relative;"><path d="M330.67 263.12V173.4l-52.75-24.22C219.44 218.76 197.58 400 56 400a56 56 0 0 0 0 112c212.64 0 370.65-122.87 419.18-210.34l-37.05-38.54zm131.09-128.37C493.92 74.91 477.18 26.48 458.62 3a8 8 0 0 0-11.93-.59l-22.9 23a8.06 8.06 0 0 0-.89 10.23c6.86 10.36 17.05 35.1-1.4 72.32A142.85 142.85 0 0 0 364.34 96c-28 0-54 8.54-76.34 22.59l74.67 34.29v78.24h89.09L506.44 288c3.26-12.62 5.56-25.63 5.56-39.31a154 154 0 0 0-50.24-113.94z"/></svg><svg aria-hidden="true" role="img" viewBox="0 0 512 512" style="height:2em;width:2em;vertical-align:-0.125em;margin-left:auto;margin-right:auto;font-size:inherit;fill:#9FC2B9;overflow:visible;position:relative;"><path d="M330.67 263.12V173.4l-52.75-24.22C219.44 218.76 197.58 400 56 400a56 56 0 0 0 0 112c212.64 0 370.65-122.87 419.18-210.34l-37.05-38.54zm131.09-128.37C493.92 74.91 477.18 26.48 458.62 3a8 8 0 0 0-11.93-.59l-22.9 23a8.06 8.06 0 0 0-.89 10.23c6.86 10.36 17.05 35.1-1.4 72.32A142.85 142.85 0 0 0 364.34 96c-28 0-54 8.54-76.34 22.59l74.67 34.29v78.24h89.09L506.44 288c3.26-12.62 5.56-25.63 5.56-39.31a154 154 0 0 0-50.24-113.94z"/></svg><svg aria-hidden="true" role="img" viewBox="0 0 512 512" style="height:2em;width:2em;vertical-align:-0.125em;margin-left:auto;margin-right:auto;font-size:inherit;fill:#9FC2B9;overflow:visible;position:relative;"><path d="M330.67 263.12V173.4l-52.75-24.22C219.44 218.76 197.58 400 56 400a56 56 0 0 0 0 112c212.64 0 370.65-122.87 419.18-210.34l-37.05-38.54zm131.09-128.37C493.92 74.91 477.18 26.48 458.62 3a8 8 0 0 0-11.93-.59l-22.9 23a8.06 8.06 0 0 0-.89 10.23c6.86 10.36 17.05 35.1-1.4 72.32A142.85 142.85 0 0 0 364.34 96c-28 0-54 8.54-76.34 22.59l74.67 34.29v78.24h89.09L506.44 288c3.26-12.62 5.56-25.63 5.56-39.31a154 154 0 0 0-50.24-113.94z"/></svg></td></tr>
  </tbody>
  
  
</table>
</div>
```

```{=html}
<div id="gzypdmsvms" style="overflow-x:auto;overflow-y:auto;width:auto;height:auto;">
<style>html {
  font-family: -apple-system, BlinkMacSystemFont, 'Segoe UI', Roboto, Oxygen, Ubuntu, Cantarell, 'Helvetica Neue', 'Fira Sans', 'Droid Sans', Arial, sans-serif;
}

#gzypdmsvms .gt_table {
  display: table;
  border-collapse: collapse;
  margin-left: auto;
  margin-right: auto;
  color: #333333;
  font-size: 16px;
  font-weight: normal;
  font-style: normal;
  background-color: #FFFFFF;
  width: auto;
  border-top-style: solid;
  border-top-width: 2px;
  border-top-color: #A8A8A8;
  border-right-style: none;
  border-right-width: 2px;
  border-right-color: #D3D3D3;
  border-bottom-style: solid;
  border-bottom-width: 2px;
  border-bottom-color: #A8A8A8;
  border-left-style: none;
  border-left-width: 2px;
  border-left-color: #D3D3D3;
}

#gzypdmsvms .gt_heading {
  background-color: #153331;
  text-align: center;
  border-bottom-color: #FFFFFF;
  border-left-style: none;
  border-left-width: 1px;
  border-left-color: #D3D3D3;
  border-right-style: none;
  border-right-width: 1px;
  border-right-color: #D3D3D3;
}

#gzypdmsvms .gt_title {
  color: #FFFFFF;
  font-size: 125%;
  font-weight: initial;
  padding-top: 4px;
  padding-bottom: 4px;
  border-bottom-color: #FFFFFF;
  border-bottom-width: 0;
}

#gzypdmsvms .gt_subtitle {
  color: #FFFFFF;
  font-size: 85%;
  font-weight: initial;
  padding-top: 0;
  padding-bottom: 6px;
  border-top-color: #FFFFFF;
  border-top-width: 0;
}

#gzypdmsvms .gt_bottom_border {
  border-bottom-style: solid;
  border-bottom-width: 2px;
  border-bottom-color: #D3D3D3;
}

#gzypdmsvms .gt_col_headings {
  border-top-style: solid;
  border-top-width: 2px;
  border-top-color: #D3D3D3;
  border-bottom-style: solid;
  border-bottom-width: 2px;
  border-bottom-color: #D3D3D3;
  border-left-style: none;
  border-left-width: 1px;
  border-left-color: #D3D3D3;
  border-right-style: none;
  border-right-width: 1px;
  border-right-color: #D3D3D3;
}

#gzypdmsvms .gt_col_heading {
  color: #FFFFFF;
  background-color: #1E6E6E;
  font-size: 100%;
  font-weight: normal;
  text-transform: inherit;
  border-left-style: none;
  border-left-width: 1px;
  border-left-color: #D3D3D3;
  border-right-style: none;
  border-right-width: 1px;
  border-right-color: #D3D3D3;
  vertical-align: bottom;
  padding-top: 5px;
  padding-bottom: 6px;
  padding-left: 5px;
  padding-right: 5px;
  overflow-x: hidden;
}

#gzypdmsvms .gt_column_spanner_outer {
  color: #FFFFFF;
  background-color: #1E6E6E;
  font-size: 100%;
  font-weight: normal;
  text-transform: inherit;
  padding-top: 0;
  padding-bottom: 0;
  padding-left: 4px;
  padding-right: 4px;
}

#gzypdmsvms .gt_column_spanner_outer:first-child {
  padding-left: 0;
}

#gzypdmsvms .gt_column_spanner_outer:last-child {
  padding-right: 0;
}

#gzypdmsvms .gt_column_spanner {
  border-bottom-style: solid;
  border-bottom-width: 2px;
  border-bottom-color: #D3D3D3;
  vertical-align: bottom;
  padding-top: 5px;
  padding-bottom: 5px;
  overflow-x: hidden;
  display: inline-block;
  width: 100%;
}

#gzypdmsvms .gt_group_heading {
  padding: 8px;
  color: #333333;
  background-color: #FFFFFF;
  font-size: 100%;
  font-weight: initial;
  text-transform: inherit;
  border-top-style: solid;
  border-top-width: 2px;
  border-top-color: #D3D3D3;
  border-bottom-style: solid;
  border-bottom-width: 2px;
  border-bottom-color: #D3D3D3;
  border-left-style: none;
  border-left-width: 1px;
  border-left-color: #D3D3D3;
  border-right-style: none;
  border-right-width: 1px;
  border-right-color: #D3D3D3;
  vertical-align: middle;
}

#gzypdmsvms .gt_empty_group_heading {
  padding: 0.5px;
  color: #333333;
  background-color: #FFFFFF;
  font-size: 100%;
  font-weight: initial;
  border-top-style: solid;
  border-top-width: 2px;
  border-top-color: #D3D3D3;
  border-bottom-style: solid;
  border-bottom-width: 2px;
  border-bottom-color: #D3D3D3;
  vertical-align: middle;
}

#gzypdmsvms .gt_from_md > :first-child {
  margin-top: 0;
}

#gzypdmsvms .gt_from_md > :last-child {
  margin-bottom: 0;
}

#gzypdmsvms .gt_row {
  padding-top: 8px;
  padding-bottom: 8px;
  padding-left: 5px;
  padding-right: 5px;
  margin: 10px;
  border-top-style: solid;
  border-top-width: 1px;
  border-top-color: #D3D3D3;
  border-left-style: none;
  border-left-width: 1px;
  border-left-color: #D3D3D3;
  border-right-style: none;
  border-right-width: 1px;
  border-right-color: #D3D3D3;
  vertical-align: middle;
  overflow-x: hidden;
}

#gzypdmsvms .gt_stub {
  color: #333333;
  background-color: #FFFFFF;
  font-size: 100%;
  font-weight: initial;
  text-transform: inherit;
  border-right-style: solid;
  border-right-width: 2px;
  border-right-color: #D3D3D3;
  padding-left: 12px;
}

#gzypdmsvms .gt_summary_row {
  color: #333333;
  background-color: #FFFFFF;
  text-transform: inherit;
  padding-top: 8px;
  padding-bottom: 8px;
  padding-left: 5px;
  padding-right: 5px;
}

#gzypdmsvms .gt_first_summary_row {
  padding-top: 8px;
  padding-bottom: 8px;
  padding-left: 5px;
  padding-right: 5px;
  border-top-style: solid;
  border-top-width: 2px;
  border-top-color: #D3D3D3;
}

#gzypdmsvms .gt_grand_summary_row {
  color: #333333;
  background-color: #FFFFFF;
  text-transform: inherit;
  padding-top: 8px;
  padding-bottom: 8px;
  padding-left: 5px;
  padding-right: 5px;
}

#gzypdmsvms .gt_first_grand_summary_row {
  padding-top: 8px;
  padding-bottom: 8px;
  padding-left: 5px;
  padding-right: 5px;
  border-top-style: double;
  border-top-width: 6px;
  border-top-color: #D3D3D3;
}

#gzypdmsvms .gt_striped {
  background-color: rgba(128, 128, 128, 0.05);
}

#gzypdmsvms .gt_table_body {
  border-top-style: solid;
  border-top-width: 2px;
  border-top-color: #D3D3D3;
  border-bottom-style: solid;
  border-bottom-width: 2px;
  border-bottom-color: #D3D3D3;
}

#gzypdmsvms .gt_footnotes {
  color: #333333;
  background-color: #FFFFFF;
  border-bottom-style: none;
  border-bottom-width: 2px;
  border-bottom-color: #D3D3D3;
  border-left-style: none;
  border-left-width: 2px;
  border-left-color: #D3D3D3;
  border-right-style: none;
  border-right-width: 2px;
  border-right-color: #D3D3D3;
}

#gzypdmsvms .gt_footnote {
  margin: 0px;
  font-size: 90%;
  padding: 4px;
}

#gzypdmsvms .gt_sourcenotes {
  color: #333333;
  background-color: #FFFFFF;
  border-bottom-style: none;
  border-bottom-width: 2px;
  border-bottom-color: #D3D3D3;
  border-left-style: none;
  border-left-width: 2px;
  border-left-color: #D3D3D3;
  border-right-style: none;
  border-right-width: 2px;
  border-right-color: #D3D3D3;
}

#gzypdmsvms .gt_sourcenote {
  font-size: 90%;
  padding: 4px;
}

#gzypdmsvms .gt_left {
  text-align: left;
}

#gzypdmsvms .gt_center {
  text-align: center;
}

#gzypdmsvms .gt_right {
  text-align: right;
  font-variant-numeric: tabular-nums;
}

#gzypdmsvms .gt_font_normal {
  font-weight: normal;
}

#gzypdmsvms .gt_font_bold {
  font-weight: bold;
}

#gzypdmsvms .gt_font_italic {
  font-style: italic;
}

#gzypdmsvms .gt_super {
  font-size: 65%;
}

#gzypdmsvms .gt_footnote_marks {
  font-style: italic;
  font-weight: normal;
  font-size: 65%;
}
</style>
<table class="gt_table" style="table-layout: fixed;; width: 0px">
  <colgroup>
    <col style="width:350px;"/>
    <col style="width:350px;"/>
  </colgroup>
  <thead class="gt_header">
    <tr>
      <th colspan="2" class="gt_heading gt_title gt_font_normal gt_bottom_border" style>Ingredients</th>
    </tr>
    
  </thead>
  <thead class="gt_col_headings">
    <tr>
      <th class="gt_col_heading gt_columns_bottom_border gt_center" rowspan="1" colspan="1"><strong>Package</strong></th>
      <th class="gt_col_heading gt_columns_bottom_border gt_center" rowspan="1" colspan="1"><strong>Data</strong></th>
    </tr>
  </thead>
  <tbody class="gt_table_body">
    <tr><td class="gt_row gt_center"><div class='gt_from_md'><p>readr<br>dplyr</p>
</div></td>
<td class="gt_row gt_center"><div class='gt_from_md'><p>sample.csv</p>
</div></td></tr>
  </tbody>
  
  
</table>
</div>
```

</br>

**Preparation**

```r
df <- readr::read_csv("C:/data/sample.csv")
```

</br>

**Sample Instructions**

```r
package::function(data, is.character, as.numeric)
```

</br>

**Actual Instructions**

```r
dplyr::mutate_if(df, is.character, as.numeric)
```


### Change all numeric data columns to character data

```{=html}
<div id="onknlhvnhg" style="overflow-x:auto;overflow-y:auto;width:auto;height:auto;">
<style>html {
  font-family: -apple-system, BlinkMacSystemFont, 'Segoe UI', Roboto, Oxygen, Ubuntu, Cantarell, 'Helvetica Neue', 'Fira Sans', 'Droid Sans', Arial, sans-serif;
}

#onknlhvnhg .gt_table {
  display: table;
  border-collapse: collapse;
  margin-left: auto;
  margin-right: auto;
  color: #333333;
  font-size: 16px;
  font-weight: normal;
  font-style: normal;
  background-color: #FFFFFF;
  width: auto;
  border-top-style: solid;
  border-top-width: 2px;
  border-top-color: #A8A8A8;
  border-right-style: none;
  border-right-width: 2px;
  border-right-color: #D3D3D3;
  border-bottom-style: solid;
  border-bottom-width: 2px;
  border-bottom-color: #A8A8A8;
  border-left-style: none;
  border-left-width: 2px;
  border-left-color: #D3D3D3;
}

#onknlhvnhg .gt_heading {
  background-color: #153331;
  text-align: center;
  border-bottom-color: #FFFFFF;
  border-left-style: none;
  border-left-width: 1px;
  border-left-color: #D3D3D3;
  border-right-style: none;
  border-right-width: 1px;
  border-right-color: #D3D3D3;
}

#onknlhvnhg .gt_title {
  color: #FFFFFF;
  font-size: 125%;
  font-weight: initial;
  padding-top: 4px;
  padding-bottom: 4px;
  border-bottom-color: #FFFFFF;
  border-bottom-width: 0;
}

#onknlhvnhg .gt_subtitle {
  color: #FFFFFF;
  font-size: 85%;
  font-weight: initial;
  padding-top: 0;
  padding-bottom: 6px;
  border-top-color: #FFFFFF;
  border-top-width: 0;
}

#onknlhvnhg .gt_bottom_border {
  border-bottom-style: solid;
  border-bottom-width: 2px;
  border-bottom-color: #D3D3D3;
}

#onknlhvnhg .gt_col_headings {
  border-top-style: solid;
  border-top-width: 2px;
  border-top-color: #D3D3D3;
  border-bottom-style: solid;
  border-bottom-width: 2px;
  border-bottom-color: #D3D3D3;
  border-left-style: none;
  border-left-width: 1px;
  border-left-color: #D3D3D3;
  border-right-style: none;
  border-right-width: 1px;
  border-right-color: #D3D3D3;
}

#onknlhvnhg .gt_col_heading {
  color: #FFFFFF;
  background-color: #153331;
  font-size: 100%;
  font-weight: normal;
  text-transform: inherit;
  border-left-style: none;
  border-left-width: 1px;
  border-left-color: #D3D3D3;
  border-right-style: none;
  border-right-width: 1px;
  border-right-color: #D3D3D3;
  vertical-align: bottom;
  padding-top: 5px;
  padding-bottom: 6px;
  padding-left: 5px;
  padding-right: 5px;
  overflow-x: hidden;
}

#onknlhvnhg .gt_column_spanner_outer {
  color: #FFFFFF;
  background-color: #153331;
  font-size: 100%;
  font-weight: normal;
  text-transform: inherit;
  padding-top: 0;
  padding-bottom: 0;
  padding-left: 4px;
  padding-right: 4px;
}

#onknlhvnhg .gt_column_spanner_outer:first-child {
  padding-left: 0;
}

#onknlhvnhg .gt_column_spanner_outer:last-child {
  padding-right: 0;
}

#onknlhvnhg .gt_column_spanner {
  border-bottom-style: solid;
  border-bottom-width: 2px;
  border-bottom-color: #D3D3D3;
  vertical-align: bottom;
  padding-top: 5px;
  padding-bottom: 5px;
  overflow-x: hidden;
  display: inline-block;
  width: 100%;
}

#onknlhvnhg .gt_group_heading {
  padding: 8px;
  color: #333333;
  background-color: #FFFFFF;
  font-size: 100%;
  font-weight: initial;
  text-transform: inherit;
  border-top-style: solid;
  border-top-width: 2px;
  border-top-color: #D3D3D3;
  border-bottom-style: solid;
  border-bottom-width: 2px;
  border-bottom-color: #D3D3D3;
  border-left-style: none;
  border-left-width: 1px;
  border-left-color: #D3D3D3;
  border-right-style: none;
  border-right-width: 1px;
  border-right-color: #D3D3D3;
  vertical-align: middle;
}

#onknlhvnhg .gt_empty_group_heading {
  padding: 0.5px;
  color: #333333;
  background-color: #FFFFFF;
  font-size: 100%;
  font-weight: initial;
  border-top-style: solid;
  border-top-width: 2px;
  border-top-color: #D3D3D3;
  border-bottom-style: solid;
  border-bottom-width: 2px;
  border-bottom-color: #D3D3D3;
  vertical-align: middle;
}

#onknlhvnhg .gt_from_md > :first-child {
  margin-top: 0;
}

#onknlhvnhg .gt_from_md > :last-child {
  margin-bottom: 0;
}

#onknlhvnhg .gt_row {
  padding-top: 8px;
  padding-bottom: 8px;
  padding-left: 5px;
  padding-right: 5px;
  margin: 10px;
  border-top-style: solid;
  border-top-width: 1px;
  border-top-color: #D3D3D3;
  border-left-style: none;
  border-left-width: 1px;
  border-left-color: #D3D3D3;
  border-right-style: none;
  border-right-width: 1px;
  border-right-color: #D3D3D3;
  vertical-align: middle;
  overflow-x: hidden;
}

#onknlhvnhg .gt_stub {
  color: #333333;
  background-color: #FFFFFF;
  font-size: 100%;
  font-weight: initial;
  text-transform: inherit;
  border-right-style: solid;
  border-right-width: 2px;
  border-right-color: #D3D3D3;
  padding-left: 12px;
}

#onknlhvnhg .gt_summary_row {
  color: #333333;
  background-color: #FFFFFF;
  text-transform: inherit;
  padding-top: 8px;
  padding-bottom: 8px;
  padding-left: 5px;
  padding-right: 5px;
}

#onknlhvnhg .gt_first_summary_row {
  padding-top: 8px;
  padding-bottom: 8px;
  padding-left: 5px;
  padding-right: 5px;
  border-top-style: solid;
  border-top-width: 2px;
  border-top-color: #D3D3D3;
}

#onknlhvnhg .gt_grand_summary_row {
  color: #333333;
  background-color: #FFFFFF;
  text-transform: inherit;
  padding-top: 8px;
  padding-bottom: 8px;
  padding-left: 5px;
  padding-right: 5px;
}

#onknlhvnhg .gt_first_grand_summary_row {
  padding-top: 8px;
  padding-bottom: 8px;
  padding-left: 5px;
  padding-right: 5px;
  border-top-style: double;
  border-top-width: 6px;
  border-top-color: #D3D3D3;
}

#onknlhvnhg .gt_striped {
  background-color: rgba(128, 128, 128, 0.05);
}

#onknlhvnhg .gt_table_body {
  border-top-style: solid;
  border-top-width: 2px;
  border-top-color: #D3D3D3;
  border-bottom-style: solid;
  border-bottom-width: 2px;
  border-bottom-color: #D3D3D3;
}

#onknlhvnhg .gt_footnotes {
  color: #333333;
  background-color: #FFFFFF;
  border-bottom-style: none;
  border-bottom-width: 2px;
  border-bottom-color: #D3D3D3;
  border-left-style: none;
  border-left-width: 2px;
  border-left-color: #D3D3D3;
  border-right-style: none;
  border-right-width: 2px;
  border-right-color: #D3D3D3;
}

#onknlhvnhg .gt_footnote {
  margin: 0px;
  font-size: 90%;
  padding: 4px;
}

#onknlhvnhg .gt_sourcenotes {
  color: #333333;
  background-color: #FFFFFF;
  border-bottom-style: none;
  border-bottom-width: 2px;
  border-bottom-color: #D3D3D3;
  border-left-style: none;
  border-left-width: 2px;
  border-left-color: #D3D3D3;
  border-right-style: none;
  border-right-width: 2px;
  border-right-color: #D3D3D3;
}

#onknlhvnhg .gt_sourcenote {
  font-size: 90%;
  padding: 4px;
}

#onknlhvnhg .gt_left {
  text-align: left;
}

#onknlhvnhg .gt_center {
  text-align: center;
}

#onknlhvnhg .gt_right {
  text-align: right;
  font-variant-numeric: tabular-nums;
}

#onknlhvnhg .gt_font_normal {
  font-weight: normal;
}

#onknlhvnhg .gt_font_bold {
  font-weight: bold;
}

#onknlhvnhg .gt_font_italic {
  font-style: italic;
}

#onknlhvnhg .gt_super {
  font-size: 65%;
}

#onknlhvnhg .gt_footnote_marks {
  font-style: italic;
  font-weight: normal;
  font-size: 65%;
}
</style>
<table class="gt_table" style="table-layout: fixed;; width: 0px">
  <colgroup>
    <col style="width:500px;"/>
    <col style="width:200px;"/>
  </colgroup>
  
  <thead class="gt_col_headings">
    <tr>
      <th class="gt_col_heading gt_columns_bottom_border gt_left" rowspan="1" colspan="1"><strong>Description</strong></th>
      <th class="gt_col_heading gt_columns_bottom_border gt_right" rowspan="1" colspan="1"></th>
    </tr>
  </thead>
  <tbody class="gt_table_body">
    <tr><td class="gt_row gt_left">Method to change all numeric values to character values in all numeric columns of a dataframe</td>
<td class="gt_row gt_right"><svg aria-hidden="true" role="img" viewBox="0 0 512 512" style="height:2em;width:2em;vertical-align:-0.125em;margin-left:auto;margin-right:auto;font-size:inherit;fill:#A62014;overflow:visible;position:relative;"><path d="M330.67 263.12V173.4l-52.75-24.22C219.44 218.76 197.58 400 56 400a56 56 0 0 0 0 112c212.64 0 370.65-122.87 419.18-210.34l-37.05-38.54zm131.09-128.37C493.92 74.91 477.18 26.48 458.62 3a8 8 0 0 0-11.93-.59l-22.9 23a8.06 8.06 0 0 0-.89 10.23c6.86 10.36 17.05 35.1-1.4 72.32A142.85 142.85 0 0 0 364.34 96c-28 0-54 8.54-76.34 22.59l74.67 34.29v78.24h89.09L506.44 288c3.26-12.62 5.56-25.63 5.56-39.31a154 154 0 0 0-50.24-113.94z"/></svg><svg aria-hidden="true" role="img" viewBox="0 0 512 512" style="height:2em;width:2em;vertical-align:-0.125em;margin-left:auto;margin-right:auto;font-size:inherit;fill:#9FC2B9;overflow:visible;position:relative;"><path d="M330.67 263.12V173.4l-52.75-24.22C219.44 218.76 197.58 400 56 400a56 56 0 0 0 0 112c212.64 0 370.65-122.87 419.18-210.34l-37.05-38.54zm131.09-128.37C493.92 74.91 477.18 26.48 458.62 3a8 8 0 0 0-11.93-.59l-22.9 23a8.06 8.06 0 0 0-.89 10.23c6.86 10.36 17.05 35.1-1.4 72.32A142.85 142.85 0 0 0 364.34 96c-28 0-54 8.54-76.34 22.59l74.67 34.29v78.24h89.09L506.44 288c3.26-12.62 5.56-25.63 5.56-39.31a154 154 0 0 0-50.24-113.94z"/></svg><svg aria-hidden="true" role="img" viewBox="0 0 512 512" style="height:2em;width:2em;vertical-align:-0.125em;margin-left:auto;margin-right:auto;font-size:inherit;fill:#9FC2B9;overflow:visible;position:relative;"><path d="M330.67 263.12V173.4l-52.75-24.22C219.44 218.76 197.58 400 56 400a56 56 0 0 0 0 112c212.64 0 370.65-122.87 419.18-210.34l-37.05-38.54zm131.09-128.37C493.92 74.91 477.18 26.48 458.62 3a8 8 0 0 0-11.93-.59l-22.9 23a8.06 8.06 0 0 0-.89 10.23c6.86 10.36 17.05 35.1-1.4 72.32A142.85 142.85 0 0 0 364.34 96c-28 0-54 8.54-76.34 22.59l74.67 34.29v78.24h89.09L506.44 288c3.26-12.62 5.56-25.63 5.56-39.31a154 154 0 0 0-50.24-113.94z"/></svg></td></tr>
  </tbody>
  
  
</table>
</div>
```

```{=html}
<div id="qgqzrhkrnl" style="overflow-x:auto;overflow-y:auto;width:auto;height:auto;">
<style>html {
  font-family: -apple-system, BlinkMacSystemFont, 'Segoe UI', Roboto, Oxygen, Ubuntu, Cantarell, 'Helvetica Neue', 'Fira Sans', 'Droid Sans', Arial, sans-serif;
}

#qgqzrhkrnl .gt_table {
  display: table;
  border-collapse: collapse;
  margin-left: auto;
  margin-right: auto;
  color: #333333;
  font-size: 16px;
  font-weight: normal;
  font-style: normal;
  background-color: #FFFFFF;
  width: auto;
  border-top-style: solid;
  border-top-width: 2px;
  border-top-color: #A8A8A8;
  border-right-style: none;
  border-right-width: 2px;
  border-right-color: #D3D3D3;
  border-bottom-style: solid;
  border-bottom-width: 2px;
  border-bottom-color: #A8A8A8;
  border-left-style: none;
  border-left-width: 2px;
  border-left-color: #D3D3D3;
}

#qgqzrhkrnl .gt_heading {
  background-color: #153331;
  text-align: center;
  border-bottom-color: #FFFFFF;
  border-left-style: none;
  border-left-width: 1px;
  border-left-color: #D3D3D3;
  border-right-style: none;
  border-right-width: 1px;
  border-right-color: #D3D3D3;
}

#qgqzrhkrnl .gt_title {
  color: #FFFFFF;
  font-size: 125%;
  font-weight: initial;
  padding-top: 4px;
  padding-bottom: 4px;
  border-bottom-color: #FFFFFF;
  border-bottom-width: 0;
}

#qgqzrhkrnl .gt_subtitle {
  color: #FFFFFF;
  font-size: 85%;
  font-weight: initial;
  padding-top: 0;
  padding-bottom: 6px;
  border-top-color: #FFFFFF;
  border-top-width: 0;
}

#qgqzrhkrnl .gt_bottom_border {
  border-bottom-style: solid;
  border-bottom-width: 2px;
  border-bottom-color: #D3D3D3;
}

#qgqzrhkrnl .gt_col_headings {
  border-top-style: solid;
  border-top-width: 2px;
  border-top-color: #D3D3D3;
  border-bottom-style: solid;
  border-bottom-width: 2px;
  border-bottom-color: #D3D3D3;
  border-left-style: none;
  border-left-width: 1px;
  border-left-color: #D3D3D3;
  border-right-style: none;
  border-right-width: 1px;
  border-right-color: #D3D3D3;
}

#qgqzrhkrnl .gt_col_heading {
  color: #FFFFFF;
  background-color: #1E6E6E;
  font-size: 100%;
  font-weight: normal;
  text-transform: inherit;
  border-left-style: none;
  border-left-width: 1px;
  border-left-color: #D3D3D3;
  border-right-style: none;
  border-right-width: 1px;
  border-right-color: #D3D3D3;
  vertical-align: bottom;
  padding-top: 5px;
  padding-bottom: 6px;
  padding-left: 5px;
  padding-right: 5px;
  overflow-x: hidden;
}

#qgqzrhkrnl .gt_column_spanner_outer {
  color: #FFFFFF;
  background-color: #1E6E6E;
  font-size: 100%;
  font-weight: normal;
  text-transform: inherit;
  padding-top: 0;
  padding-bottom: 0;
  padding-left: 4px;
  padding-right: 4px;
}

#qgqzrhkrnl .gt_column_spanner_outer:first-child {
  padding-left: 0;
}

#qgqzrhkrnl .gt_column_spanner_outer:last-child {
  padding-right: 0;
}

#qgqzrhkrnl .gt_column_spanner {
  border-bottom-style: solid;
  border-bottom-width: 2px;
  border-bottom-color: #D3D3D3;
  vertical-align: bottom;
  padding-top: 5px;
  padding-bottom: 5px;
  overflow-x: hidden;
  display: inline-block;
  width: 100%;
}

#qgqzrhkrnl .gt_group_heading {
  padding: 8px;
  color: #333333;
  background-color: #FFFFFF;
  font-size: 100%;
  font-weight: initial;
  text-transform: inherit;
  border-top-style: solid;
  border-top-width: 2px;
  border-top-color: #D3D3D3;
  border-bottom-style: solid;
  border-bottom-width: 2px;
  border-bottom-color: #D3D3D3;
  border-left-style: none;
  border-left-width: 1px;
  border-left-color: #D3D3D3;
  border-right-style: none;
  border-right-width: 1px;
  border-right-color: #D3D3D3;
  vertical-align: middle;
}

#qgqzrhkrnl .gt_empty_group_heading {
  padding: 0.5px;
  color: #333333;
  background-color: #FFFFFF;
  font-size: 100%;
  font-weight: initial;
  border-top-style: solid;
  border-top-width: 2px;
  border-top-color: #D3D3D3;
  border-bottom-style: solid;
  border-bottom-width: 2px;
  border-bottom-color: #D3D3D3;
  vertical-align: middle;
}

#qgqzrhkrnl .gt_from_md > :first-child {
  margin-top: 0;
}

#qgqzrhkrnl .gt_from_md > :last-child {
  margin-bottom: 0;
}

#qgqzrhkrnl .gt_row {
  padding-top: 8px;
  padding-bottom: 8px;
  padding-left: 5px;
  padding-right: 5px;
  margin: 10px;
  border-top-style: solid;
  border-top-width: 1px;
  border-top-color: #D3D3D3;
  border-left-style: none;
  border-left-width: 1px;
  border-left-color: #D3D3D3;
  border-right-style: none;
  border-right-width: 1px;
  border-right-color: #D3D3D3;
  vertical-align: middle;
  overflow-x: hidden;
}

#qgqzrhkrnl .gt_stub {
  color: #333333;
  background-color: #FFFFFF;
  font-size: 100%;
  font-weight: initial;
  text-transform: inherit;
  border-right-style: solid;
  border-right-width: 2px;
  border-right-color: #D3D3D3;
  padding-left: 12px;
}

#qgqzrhkrnl .gt_summary_row {
  color: #333333;
  background-color: #FFFFFF;
  text-transform: inherit;
  padding-top: 8px;
  padding-bottom: 8px;
  padding-left: 5px;
  padding-right: 5px;
}

#qgqzrhkrnl .gt_first_summary_row {
  padding-top: 8px;
  padding-bottom: 8px;
  padding-left: 5px;
  padding-right: 5px;
  border-top-style: solid;
  border-top-width: 2px;
  border-top-color: #D3D3D3;
}

#qgqzrhkrnl .gt_grand_summary_row {
  color: #333333;
  background-color: #FFFFFF;
  text-transform: inherit;
  padding-top: 8px;
  padding-bottom: 8px;
  padding-left: 5px;
  padding-right: 5px;
}

#qgqzrhkrnl .gt_first_grand_summary_row {
  padding-top: 8px;
  padding-bottom: 8px;
  padding-left: 5px;
  padding-right: 5px;
  border-top-style: double;
  border-top-width: 6px;
  border-top-color: #D3D3D3;
}

#qgqzrhkrnl .gt_striped {
  background-color: rgba(128, 128, 128, 0.05);
}

#qgqzrhkrnl .gt_table_body {
  border-top-style: solid;
  border-top-width: 2px;
  border-top-color: #D3D3D3;
  border-bottom-style: solid;
  border-bottom-width: 2px;
  border-bottom-color: #D3D3D3;
}

#qgqzrhkrnl .gt_footnotes {
  color: #333333;
  background-color: #FFFFFF;
  border-bottom-style: none;
  border-bottom-width: 2px;
  border-bottom-color: #D3D3D3;
  border-left-style: none;
  border-left-width: 2px;
  border-left-color: #D3D3D3;
  border-right-style: none;
  border-right-width: 2px;
  border-right-color: #D3D3D3;
}

#qgqzrhkrnl .gt_footnote {
  margin: 0px;
  font-size: 90%;
  padding: 4px;
}

#qgqzrhkrnl .gt_sourcenotes {
  color: #333333;
  background-color: #FFFFFF;
  border-bottom-style: none;
  border-bottom-width: 2px;
  border-bottom-color: #D3D3D3;
  border-left-style: none;
  border-left-width: 2px;
  border-left-color: #D3D3D3;
  border-right-style: none;
  border-right-width: 2px;
  border-right-color: #D3D3D3;
}

#qgqzrhkrnl .gt_sourcenote {
  font-size: 90%;
  padding: 4px;
}

#qgqzrhkrnl .gt_left {
  text-align: left;
}

#qgqzrhkrnl .gt_center {
  text-align: center;
}

#qgqzrhkrnl .gt_right {
  text-align: right;
  font-variant-numeric: tabular-nums;
}

#qgqzrhkrnl .gt_font_normal {
  font-weight: normal;
}

#qgqzrhkrnl .gt_font_bold {
  font-weight: bold;
}

#qgqzrhkrnl .gt_font_italic {
  font-style: italic;
}

#qgqzrhkrnl .gt_super {
  font-size: 65%;
}

#qgqzrhkrnl .gt_footnote_marks {
  font-style: italic;
  font-weight: normal;
  font-size: 65%;
}
</style>
<table class="gt_table" style="table-layout: fixed;; width: 0px">
  <colgroup>
    <col style="width:350px;"/>
    <col style="width:350px;"/>
  </colgroup>
  <thead class="gt_header">
    <tr>
      <th colspan="2" class="gt_heading gt_title gt_font_normal gt_bottom_border" style>Ingredients</th>
    </tr>
    
  </thead>
  <thead class="gt_col_headings">
    <tr>
      <th class="gt_col_heading gt_columns_bottom_border gt_center" rowspan="1" colspan="1"><strong>Package</strong></th>
      <th class="gt_col_heading gt_columns_bottom_border gt_center" rowspan="1" colspan="1"><strong>Data</strong></th>
    </tr>
  </thead>
  <tbody class="gt_table_body">
    <tr><td class="gt_row gt_center"><div class='gt_from_md'><p>readr<br>dplyr</p>
</div></td>
<td class="gt_row gt_center"><div class='gt_from_md'><p>sample.csv</p>
</div></td></tr>
  </tbody>
  
  
</table>
</div>
```

</br>

**Preparation**

```r
df <- readr::read_csv("C:/data/sample.csv")
```

</br>

**Sample Instructions**

```r
package::function(data, is.numeric, as.character)
```

</br>

**Actual Instructions**

```r
dplyr::mutate_if(df, is.numeric, as.character)
```


### Change all character data columns to date data

```{=html}
<div id="zfaolkrhni" style="overflow-x:auto;overflow-y:auto;width:auto;height:auto;">
<style>html {
  font-family: -apple-system, BlinkMacSystemFont, 'Segoe UI', Roboto, Oxygen, Ubuntu, Cantarell, 'Helvetica Neue', 'Fira Sans', 'Droid Sans', Arial, sans-serif;
}

#zfaolkrhni .gt_table {
  display: table;
  border-collapse: collapse;
  margin-left: auto;
  margin-right: auto;
  color: #333333;
  font-size: 16px;
  font-weight: normal;
  font-style: normal;
  background-color: #FFFFFF;
  width: auto;
  border-top-style: solid;
  border-top-width: 2px;
  border-top-color: #A8A8A8;
  border-right-style: none;
  border-right-width: 2px;
  border-right-color: #D3D3D3;
  border-bottom-style: solid;
  border-bottom-width: 2px;
  border-bottom-color: #A8A8A8;
  border-left-style: none;
  border-left-width: 2px;
  border-left-color: #D3D3D3;
}

#zfaolkrhni .gt_heading {
  background-color: #153331;
  text-align: center;
  border-bottom-color: #FFFFFF;
  border-left-style: none;
  border-left-width: 1px;
  border-left-color: #D3D3D3;
  border-right-style: none;
  border-right-width: 1px;
  border-right-color: #D3D3D3;
}

#zfaolkrhni .gt_title {
  color: #FFFFFF;
  font-size: 125%;
  font-weight: initial;
  padding-top: 4px;
  padding-bottom: 4px;
  border-bottom-color: #FFFFFF;
  border-bottom-width: 0;
}

#zfaolkrhni .gt_subtitle {
  color: #FFFFFF;
  font-size: 85%;
  font-weight: initial;
  padding-top: 0;
  padding-bottom: 6px;
  border-top-color: #FFFFFF;
  border-top-width: 0;
}

#zfaolkrhni .gt_bottom_border {
  border-bottom-style: solid;
  border-bottom-width: 2px;
  border-bottom-color: #D3D3D3;
}

#zfaolkrhni .gt_col_headings {
  border-top-style: solid;
  border-top-width: 2px;
  border-top-color: #D3D3D3;
  border-bottom-style: solid;
  border-bottom-width: 2px;
  border-bottom-color: #D3D3D3;
  border-left-style: none;
  border-left-width: 1px;
  border-left-color: #D3D3D3;
  border-right-style: none;
  border-right-width: 1px;
  border-right-color: #D3D3D3;
}

#zfaolkrhni .gt_col_heading {
  color: #FFFFFF;
  background-color: #153331;
  font-size: 100%;
  font-weight: normal;
  text-transform: inherit;
  border-left-style: none;
  border-left-width: 1px;
  border-left-color: #D3D3D3;
  border-right-style: none;
  border-right-width: 1px;
  border-right-color: #D3D3D3;
  vertical-align: bottom;
  padding-top: 5px;
  padding-bottom: 6px;
  padding-left: 5px;
  padding-right: 5px;
  overflow-x: hidden;
}

#zfaolkrhni .gt_column_spanner_outer {
  color: #FFFFFF;
  background-color: #153331;
  font-size: 100%;
  font-weight: normal;
  text-transform: inherit;
  padding-top: 0;
  padding-bottom: 0;
  padding-left: 4px;
  padding-right: 4px;
}

#zfaolkrhni .gt_column_spanner_outer:first-child {
  padding-left: 0;
}

#zfaolkrhni .gt_column_spanner_outer:last-child {
  padding-right: 0;
}

#zfaolkrhni .gt_column_spanner {
  border-bottom-style: solid;
  border-bottom-width: 2px;
  border-bottom-color: #D3D3D3;
  vertical-align: bottom;
  padding-top: 5px;
  padding-bottom: 5px;
  overflow-x: hidden;
  display: inline-block;
  width: 100%;
}

#zfaolkrhni .gt_group_heading {
  padding: 8px;
  color: #333333;
  background-color: #FFFFFF;
  font-size: 100%;
  font-weight: initial;
  text-transform: inherit;
  border-top-style: solid;
  border-top-width: 2px;
  border-top-color: #D3D3D3;
  border-bottom-style: solid;
  border-bottom-width: 2px;
  border-bottom-color: #D3D3D3;
  border-left-style: none;
  border-left-width: 1px;
  border-left-color: #D3D3D3;
  border-right-style: none;
  border-right-width: 1px;
  border-right-color: #D3D3D3;
  vertical-align: middle;
}

#zfaolkrhni .gt_empty_group_heading {
  padding: 0.5px;
  color: #333333;
  background-color: #FFFFFF;
  font-size: 100%;
  font-weight: initial;
  border-top-style: solid;
  border-top-width: 2px;
  border-top-color: #D3D3D3;
  border-bottom-style: solid;
  border-bottom-width: 2px;
  border-bottom-color: #D3D3D3;
  vertical-align: middle;
}

#zfaolkrhni .gt_from_md > :first-child {
  margin-top: 0;
}

#zfaolkrhni .gt_from_md > :last-child {
  margin-bottom: 0;
}

#zfaolkrhni .gt_row {
  padding-top: 8px;
  padding-bottom: 8px;
  padding-left: 5px;
  padding-right: 5px;
  margin: 10px;
  border-top-style: solid;
  border-top-width: 1px;
  border-top-color: #D3D3D3;
  border-left-style: none;
  border-left-width: 1px;
  border-left-color: #D3D3D3;
  border-right-style: none;
  border-right-width: 1px;
  border-right-color: #D3D3D3;
  vertical-align: middle;
  overflow-x: hidden;
}

#zfaolkrhni .gt_stub {
  color: #333333;
  background-color: #FFFFFF;
  font-size: 100%;
  font-weight: initial;
  text-transform: inherit;
  border-right-style: solid;
  border-right-width: 2px;
  border-right-color: #D3D3D3;
  padding-left: 12px;
}

#zfaolkrhni .gt_summary_row {
  color: #333333;
  background-color: #FFFFFF;
  text-transform: inherit;
  padding-top: 8px;
  padding-bottom: 8px;
  padding-left: 5px;
  padding-right: 5px;
}

#zfaolkrhni .gt_first_summary_row {
  padding-top: 8px;
  padding-bottom: 8px;
  padding-left: 5px;
  padding-right: 5px;
  border-top-style: solid;
  border-top-width: 2px;
  border-top-color: #D3D3D3;
}

#zfaolkrhni .gt_grand_summary_row {
  color: #333333;
  background-color: #FFFFFF;
  text-transform: inherit;
  padding-top: 8px;
  padding-bottom: 8px;
  padding-left: 5px;
  padding-right: 5px;
}

#zfaolkrhni .gt_first_grand_summary_row {
  padding-top: 8px;
  padding-bottom: 8px;
  padding-left: 5px;
  padding-right: 5px;
  border-top-style: double;
  border-top-width: 6px;
  border-top-color: #D3D3D3;
}

#zfaolkrhni .gt_striped {
  background-color: rgba(128, 128, 128, 0.05);
}

#zfaolkrhni .gt_table_body {
  border-top-style: solid;
  border-top-width: 2px;
  border-top-color: #D3D3D3;
  border-bottom-style: solid;
  border-bottom-width: 2px;
  border-bottom-color: #D3D3D3;
}

#zfaolkrhni .gt_footnotes {
  color: #333333;
  background-color: #FFFFFF;
  border-bottom-style: none;
  border-bottom-width: 2px;
  border-bottom-color: #D3D3D3;
  border-left-style: none;
  border-left-width: 2px;
  border-left-color: #D3D3D3;
  border-right-style: none;
  border-right-width: 2px;
  border-right-color: #D3D3D3;
}

#zfaolkrhni .gt_footnote {
  margin: 0px;
  font-size: 90%;
  padding: 4px;
}

#zfaolkrhni .gt_sourcenotes {
  color: #333333;
  background-color: #FFFFFF;
  border-bottom-style: none;
  border-bottom-width: 2px;
  border-bottom-color: #D3D3D3;
  border-left-style: none;
  border-left-width: 2px;
  border-left-color: #D3D3D3;
  border-right-style: none;
  border-right-width: 2px;
  border-right-color: #D3D3D3;
}

#zfaolkrhni .gt_sourcenote {
  font-size: 90%;
  padding: 4px;
}

#zfaolkrhni .gt_left {
  text-align: left;
}

#zfaolkrhni .gt_center {
  text-align: center;
}

#zfaolkrhni .gt_right {
  text-align: right;
  font-variant-numeric: tabular-nums;
}

#zfaolkrhni .gt_font_normal {
  font-weight: normal;
}

#zfaolkrhni .gt_font_bold {
  font-weight: bold;
}

#zfaolkrhni .gt_font_italic {
  font-style: italic;
}

#zfaolkrhni .gt_super {
  font-size: 65%;
}

#zfaolkrhni .gt_footnote_marks {
  font-style: italic;
  font-weight: normal;
  font-size: 65%;
}
</style>
<table class="gt_table" style="table-layout: fixed;; width: 0px">
  <colgroup>
    <col style="width:500px;"/>
    <col style="width:200px;"/>
  </colgroup>
  
  <thead class="gt_col_headings">
    <tr>
      <th class="gt_col_heading gt_columns_bottom_border gt_left" rowspan="1" colspan="1"><strong>Description</strong></th>
      <th class="gt_col_heading gt_columns_bottom_border gt_right" rowspan="1" colspan="1"></th>
    </tr>
  </thead>
  <tbody class="gt_table_body">
    <tr><td class="gt_row gt_left">Method to change all character values to date values in all character columns of a dataframe</td>
<td class="gt_row gt_right"><svg aria-hidden="true" role="img" viewBox="0 0 512 512" style="height:2em;width:2em;vertical-align:-0.125em;margin-left:auto;margin-right:auto;font-size:inherit;fill:#A62014;overflow:visible;position:relative;"><path d="M330.67 263.12V173.4l-52.75-24.22C219.44 218.76 197.58 400 56 400a56 56 0 0 0 0 112c212.64 0 370.65-122.87 419.18-210.34l-37.05-38.54zm131.09-128.37C493.92 74.91 477.18 26.48 458.62 3a8 8 0 0 0-11.93-.59l-22.9 23a8.06 8.06 0 0 0-.89 10.23c6.86 10.36 17.05 35.1-1.4 72.32A142.85 142.85 0 0 0 364.34 96c-28 0-54 8.54-76.34 22.59l74.67 34.29v78.24h89.09L506.44 288c3.26-12.62 5.56-25.63 5.56-39.31a154 154 0 0 0-50.24-113.94z"/></svg><svg aria-hidden="true" role="img" viewBox="0 0 512 512" style="height:2em;width:2em;vertical-align:-0.125em;margin-left:auto;margin-right:auto;font-size:inherit;fill:#9FC2B9;overflow:visible;position:relative;"><path d="M330.67 263.12V173.4l-52.75-24.22C219.44 218.76 197.58 400 56 400a56 56 0 0 0 0 112c212.64 0 370.65-122.87 419.18-210.34l-37.05-38.54zm131.09-128.37C493.92 74.91 477.18 26.48 458.62 3a8 8 0 0 0-11.93-.59l-22.9 23a8.06 8.06 0 0 0-.89 10.23c6.86 10.36 17.05 35.1-1.4 72.32A142.85 142.85 0 0 0 364.34 96c-28 0-54 8.54-76.34 22.59l74.67 34.29v78.24h89.09L506.44 288c3.26-12.62 5.56-25.63 5.56-39.31a154 154 0 0 0-50.24-113.94z"/></svg><svg aria-hidden="true" role="img" viewBox="0 0 512 512" style="height:2em;width:2em;vertical-align:-0.125em;margin-left:auto;margin-right:auto;font-size:inherit;fill:#9FC2B9;overflow:visible;position:relative;"><path d="M330.67 263.12V173.4l-52.75-24.22C219.44 218.76 197.58 400 56 400a56 56 0 0 0 0 112c212.64 0 370.65-122.87 419.18-210.34l-37.05-38.54zm131.09-128.37C493.92 74.91 477.18 26.48 458.62 3a8 8 0 0 0-11.93-.59l-22.9 23a8.06 8.06 0 0 0-.89 10.23c6.86 10.36 17.05 35.1-1.4 72.32A142.85 142.85 0 0 0 364.34 96c-28 0-54 8.54-76.34 22.59l74.67 34.29v78.24h89.09L506.44 288c3.26-12.62 5.56-25.63 5.56-39.31a154 154 0 0 0-50.24-113.94z"/></svg></td></tr>
  </tbody>
  
  
</table>
</div>
```

```{=html}
<div id="yxsqvuiovr" style="overflow-x:auto;overflow-y:auto;width:auto;height:auto;">
<style>html {
  font-family: -apple-system, BlinkMacSystemFont, 'Segoe UI', Roboto, Oxygen, Ubuntu, Cantarell, 'Helvetica Neue', 'Fira Sans', 'Droid Sans', Arial, sans-serif;
}

#yxsqvuiovr .gt_table {
  display: table;
  border-collapse: collapse;
  margin-left: auto;
  margin-right: auto;
  color: #333333;
  font-size: 16px;
  font-weight: normal;
  font-style: normal;
  background-color: #FFFFFF;
  width: auto;
  border-top-style: solid;
  border-top-width: 2px;
  border-top-color: #A8A8A8;
  border-right-style: none;
  border-right-width: 2px;
  border-right-color: #D3D3D3;
  border-bottom-style: solid;
  border-bottom-width: 2px;
  border-bottom-color: #A8A8A8;
  border-left-style: none;
  border-left-width: 2px;
  border-left-color: #D3D3D3;
}

#yxsqvuiovr .gt_heading {
  background-color: #153331;
  text-align: center;
  border-bottom-color: #FFFFFF;
  border-left-style: none;
  border-left-width: 1px;
  border-left-color: #D3D3D3;
  border-right-style: none;
  border-right-width: 1px;
  border-right-color: #D3D3D3;
}

#yxsqvuiovr .gt_title {
  color: #FFFFFF;
  font-size: 125%;
  font-weight: initial;
  padding-top: 4px;
  padding-bottom: 4px;
  border-bottom-color: #FFFFFF;
  border-bottom-width: 0;
}

#yxsqvuiovr .gt_subtitle {
  color: #FFFFFF;
  font-size: 85%;
  font-weight: initial;
  padding-top: 0;
  padding-bottom: 6px;
  border-top-color: #FFFFFF;
  border-top-width: 0;
}

#yxsqvuiovr .gt_bottom_border {
  border-bottom-style: solid;
  border-bottom-width: 2px;
  border-bottom-color: #D3D3D3;
}

#yxsqvuiovr .gt_col_headings {
  border-top-style: solid;
  border-top-width: 2px;
  border-top-color: #D3D3D3;
  border-bottom-style: solid;
  border-bottom-width: 2px;
  border-bottom-color: #D3D3D3;
  border-left-style: none;
  border-left-width: 1px;
  border-left-color: #D3D3D3;
  border-right-style: none;
  border-right-width: 1px;
  border-right-color: #D3D3D3;
}

#yxsqvuiovr .gt_col_heading {
  color: #FFFFFF;
  background-color: #1E6E6E;
  font-size: 100%;
  font-weight: normal;
  text-transform: inherit;
  border-left-style: none;
  border-left-width: 1px;
  border-left-color: #D3D3D3;
  border-right-style: none;
  border-right-width: 1px;
  border-right-color: #D3D3D3;
  vertical-align: bottom;
  padding-top: 5px;
  padding-bottom: 6px;
  padding-left: 5px;
  padding-right: 5px;
  overflow-x: hidden;
}

#yxsqvuiovr .gt_column_spanner_outer {
  color: #FFFFFF;
  background-color: #1E6E6E;
  font-size: 100%;
  font-weight: normal;
  text-transform: inherit;
  padding-top: 0;
  padding-bottom: 0;
  padding-left: 4px;
  padding-right: 4px;
}

#yxsqvuiovr .gt_column_spanner_outer:first-child {
  padding-left: 0;
}

#yxsqvuiovr .gt_column_spanner_outer:last-child {
  padding-right: 0;
}

#yxsqvuiovr .gt_column_spanner {
  border-bottom-style: solid;
  border-bottom-width: 2px;
  border-bottom-color: #D3D3D3;
  vertical-align: bottom;
  padding-top: 5px;
  padding-bottom: 5px;
  overflow-x: hidden;
  display: inline-block;
  width: 100%;
}

#yxsqvuiovr .gt_group_heading {
  padding: 8px;
  color: #333333;
  background-color: #FFFFFF;
  font-size: 100%;
  font-weight: initial;
  text-transform: inherit;
  border-top-style: solid;
  border-top-width: 2px;
  border-top-color: #D3D3D3;
  border-bottom-style: solid;
  border-bottom-width: 2px;
  border-bottom-color: #D3D3D3;
  border-left-style: none;
  border-left-width: 1px;
  border-left-color: #D3D3D3;
  border-right-style: none;
  border-right-width: 1px;
  border-right-color: #D3D3D3;
  vertical-align: middle;
}

#yxsqvuiovr .gt_empty_group_heading {
  padding: 0.5px;
  color: #333333;
  background-color: #FFFFFF;
  font-size: 100%;
  font-weight: initial;
  border-top-style: solid;
  border-top-width: 2px;
  border-top-color: #D3D3D3;
  border-bottom-style: solid;
  border-bottom-width: 2px;
  border-bottom-color: #D3D3D3;
  vertical-align: middle;
}

#yxsqvuiovr .gt_from_md > :first-child {
  margin-top: 0;
}

#yxsqvuiovr .gt_from_md > :last-child {
  margin-bottom: 0;
}

#yxsqvuiovr .gt_row {
  padding-top: 8px;
  padding-bottom: 8px;
  padding-left: 5px;
  padding-right: 5px;
  margin: 10px;
  border-top-style: solid;
  border-top-width: 1px;
  border-top-color: #D3D3D3;
  border-left-style: none;
  border-left-width: 1px;
  border-left-color: #D3D3D3;
  border-right-style: none;
  border-right-width: 1px;
  border-right-color: #D3D3D3;
  vertical-align: middle;
  overflow-x: hidden;
}

#yxsqvuiovr .gt_stub {
  color: #333333;
  background-color: #FFFFFF;
  font-size: 100%;
  font-weight: initial;
  text-transform: inherit;
  border-right-style: solid;
  border-right-width: 2px;
  border-right-color: #D3D3D3;
  padding-left: 12px;
}

#yxsqvuiovr .gt_summary_row {
  color: #333333;
  background-color: #FFFFFF;
  text-transform: inherit;
  padding-top: 8px;
  padding-bottom: 8px;
  padding-left: 5px;
  padding-right: 5px;
}

#yxsqvuiovr .gt_first_summary_row {
  padding-top: 8px;
  padding-bottom: 8px;
  padding-left: 5px;
  padding-right: 5px;
  border-top-style: solid;
  border-top-width: 2px;
  border-top-color: #D3D3D3;
}

#yxsqvuiovr .gt_grand_summary_row {
  color: #333333;
  background-color: #FFFFFF;
  text-transform: inherit;
  padding-top: 8px;
  padding-bottom: 8px;
  padding-left: 5px;
  padding-right: 5px;
}

#yxsqvuiovr .gt_first_grand_summary_row {
  padding-top: 8px;
  padding-bottom: 8px;
  padding-left: 5px;
  padding-right: 5px;
  border-top-style: double;
  border-top-width: 6px;
  border-top-color: #D3D3D3;
}

#yxsqvuiovr .gt_striped {
  background-color: rgba(128, 128, 128, 0.05);
}

#yxsqvuiovr .gt_table_body {
  border-top-style: solid;
  border-top-width: 2px;
  border-top-color: #D3D3D3;
  border-bottom-style: solid;
  border-bottom-width: 2px;
  border-bottom-color: #D3D3D3;
}

#yxsqvuiovr .gt_footnotes {
  color: #333333;
  background-color: #FFFFFF;
  border-bottom-style: none;
  border-bottom-width: 2px;
  border-bottom-color: #D3D3D3;
  border-left-style: none;
  border-left-width: 2px;
  border-left-color: #D3D3D3;
  border-right-style: none;
  border-right-width: 2px;
  border-right-color: #D3D3D3;
}

#yxsqvuiovr .gt_footnote {
  margin: 0px;
  font-size: 90%;
  padding: 4px;
}

#yxsqvuiovr .gt_sourcenotes {
  color: #333333;
  background-color: #FFFFFF;
  border-bottom-style: none;
  border-bottom-width: 2px;
  border-bottom-color: #D3D3D3;
  border-left-style: none;
  border-left-width: 2px;
  border-left-color: #D3D3D3;
  border-right-style: none;
  border-right-width: 2px;
  border-right-color: #D3D3D3;
}

#yxsqvuiovr .gt_sourcenote {
  font-size: 90%;
  padding: 4px;
}

#yxsqvuiovr .gt_left {
  text-align: left;
}

#yxsqvuiovr .gt_center {
  text-align: center;
}

#yxsqvuiovr .gt_right {
  text-align: right;
  font-variant-numeric: tabular-nums;
}

#yxsqvuiovr .gt_font_normal {
  font-weight: normal;
}

#yxsqvuiovr .gt_font_bold {
  font-weight: bold;
}

#yxsqvuiovr .gt_font_italic {
  font-style: italic;
}

#yxsqvuiovr .gt_super {
  font-size: 65%;
}

#yxsqvuiovr .gt_footnote_marks {
  font-style: italic;
  font-weight: normal;
  font-size: 65%;
}
</style>
<table class="gt_table" style="table-layout: fixed;; width: 0px">
  <colgroup>
    <col style="width:350px;"/>
    <col style="width:350px;"/>
  </colgroup>
  <thead class="gt_header">
    <tr>
      <th colspan="2" class="gt_heading gt_title gt_font_normal gt_bottom_border" style>Ingredients</th>
    </tr>
    
  </thead>
  <thead class="gt_col_headings">
    <tr>
      <th class="gt_col_heading gt_columns_bottom_border gt_center" rowspan="1" colspan="1"><strong>Package</strong></th>
      <th class="gt_col_heading gt_columns_bottom_border gt_center" rowspan="1" colspan="1"><strong>Data</strong></th>
    </tr>
  </thead>
  <tbody class="gt_table_body">
    <tr><td class="gt_row gt_center"><div class='gt_from_md'><p>readr<br>dplyr</p>
</div></td>
<td class="gt_row gt_center"><div class='gt_from_md'><p>sample.csv</p>
</div></td></tr>
  </tbody>
  
  
</table>
</div>
```

</br>

**Preparation**

```r
df <- readr::read_csv("C:/data/sample.csv")
```

</br>

**Sample Instructions**

```r
package::function(data, is.chacter, as.Date)
```

</br>

**Actual Instructions**

```r
dplyr::mutate_if(df, is.character, as.Date)
```


### Change character data type to numeric data type in selected columns

```{=html}
<div id="cfsutntxse" style="overflow-x:auto;overflow-y:auto;width:auto;height:auto;">
<style>html {
  font-family: -apple-system, BlinkMacSystemFont, 'Segoe UI', Roboto, Oxygen, Ubuntu, Cantarell, 'Helvetica Neue', 'Fira Sans', 'Droid Sans', Arial, sans-serif;
}

#cfsutntxse .gt_table {
  display: table;
  border-collapse: collapse;
  margin-left: auto;
  margin-right: auto;
  color: #333333;
  font-size: 16px;
  font-weight: normal;
  font-style: normal;
  background-color: #FFFFFF;
  width: auto;
  border-top-style: solid;
  border-top-width: 2px;
  border-top-color: #A8A8A8;
  border-right-style: none;
  border-right-width: 2px;
  border-right-color: #D3D3D3;
  border-bottom-style: solid;
  border-bottom-width: 2px;
  border-bottom-color: #A8A8A8;
  border-left-style: none;
  border-left-width: 2px;
  border-left-color: #D3D3D3;
}

#cfsutntxse .gt_heading {
  background-color: #153331;
  text-align: center;
  border-bottom-color: #FFFFFF;
  border-left-style: none;
  border-left-width: 1px;
  border-left-color: #D3D3D3;
  border-right-style: none;
  border-right-width: 1px;
  border-right-color: #D3D3D3;
}

#cfsutntxse .gt_title {
  color: #FFFFFF;
  font-size: 125%;
  font-weight: initial;
  padding-top: 4px;
  padding-bottom: 4px;
  border-bottom-color: #FFFFFF;
  border-bottom-width: 0;
}

#cfsutntxse .gt_subtitle {
  color: #FFFFFF;
  font-size: 85%;
  font-weight: initial;
  padding-top: 0;
  padding-bottom: 6px;
  border-top-color: #FFFFFF;
  border-top-width: 0;
}

#cfsutntxse .gt_bottom_border {
  border-bottom-style: solid;
  border-bottom-width: 2px;
  border-bottom-color: #D3D3D3;
}

#cfsutntxse .gt_col_headings {
  border-top-style: solid;
  border-top-width: 2px;
  border-top-color: #D3D3D3;
  border-bottom-style: solid;
  border-bottom-width: 2px;
  border-bottom-color: #D3D3D3;
  border-left-style: none;
  border-left-width: 1px;
  border-left-color: #D3D3D3;
  border-right-style: none;
  border-right-width: 1px;
  border-right-color: #D3D3D3;
}

#cfsutntxse .gt_col_heading {
  color: #FFFFFF;
  background-color: #153331;
  font-size: 100%;
  font-weight: normal;
  text-transform: inherit;
  border-left-style: none;
  border-left-width: 1px;
  border-left-color: #D3D3D3;
  border-right-style: none;
  border-right-width: 1px;
  border-right-color: #D3D3D3;
  vertical-align: bottom;
  padding-top: 5px;
  padding-bottom: 6px;
  padding-left: 5px;
  padding-right: 5px;
  overflow-x: hidden;
}

#cfsutntxse .gt_column_spanner_outer {
  color: #FFFFFF;
  background-color: #153331;
  font-size: 100%;
  font-weight: normal;
  text-transform: inherit;
  padding-top: 0;
  padding-bottom: 0;
  padding-left: 4px;
  padding-right: 4px;
}

#cfsutntxse .gt_column_spanner_outer:first-child {
  padding-left: 0;
}

#cfsutntxse .gt_column_spanner_outer:last-child {
  padding-right: 0;
}

#cfsutntxse .gt_column_spanner {
  border-bottom-style: solid;
  border-bottom-width: 2px;
  border-bottom-color: #D3D3D3;
  vertical-align: bottom;
  padding-top: 5px;
  padding-bottom: 5px;
  overflow-x: hidden;
  display: inline-block;
  width: 100%;
}

#cfsutntxse .gt_group_heading {
  padding: 8px;
  color: #333333;
  background-color: #FFFFFF;
  font-size: 100%;
  font-weight: initial;
  text-transform: inherit;
  border-top-style: solid;
  border-top-width: 2px;
  border-top-color: #D3D3D3;
  border-bottom-style: solid;
  border-bottom-width: 2px;
  border-bottom-color: #D3D3D3;
  border-left-style: none;
  border-left-width: 1px;
  border-left-color: #D3D3D3;
  border-right-style: none;
  border-right-width: 1px;
  border-right-color: #D3D3D3;
  vertical-align: middle;
}

#cfsutntxse .gt_empty_group_heading {
  padding: 0.5px;
  color: #333333;
  background-color: #FFFFFF;
  font-size: 100%;
  font-weight: initial;
  border-top-style: solid;
  border-top-width: 2px;
  border-top-color: #D3D3D3;
  border-bottom-style: solid;
  border-bottom-width: 2px;
  border-bottom-color: #D3D3D3;
  vertical-align: middle;
}

#cfsutntxse .gt_from_md > :first-child {
  margin-top: 0;
}

#cfsutntxse .gt_from_md > :last-child {
  margin-bottom: 0;
}

#cfsutntxse .gt_row {
  padding-top: 8px;
  padding-bottom: 8px;
  padding-left: 5px;
  padding-right: 5px;
  margin: 10px;
  border-top-style: solid;
  border-top-width: 1px;
  border-top-color: #D3D3D3;
  border-left-style: none;
  border-left-width: 1px;
  border-left-color: #D3D3D3;
  border-right-style: none;
  border-right-width: 1px;
  border-right-color: #D3D3D3;
  vertical-align: middle;
  overflow-x: hidden;
}

#cfsutntxse .gt_stub {
  color: #333333;
  background-color: #FFFFFF;
  font-size: 100%;
  font-weight: initial;
  text-transform: inherit;
  border-right-style: solid;
  border-right-width: 2px;
  border-right-color: #D3D3D3;
  padding-left: 12px;
}

#cfsutntxse .gt_summary_row {
  color: #333333;
  background-color: #FFFFFF;
  text-transform: inherit;
  padding-top: 8px;
  padding-bottom: 8px;
  padding-left: 5px;
  padding-right: 5px;
}

#cfsutntxse .gt_first_summary_row {
  padding-top: 8px;
  padding-bottom: 8px;
  padding-left: 5px;
  padding-right: 5px;
  border-top-style: solid;
  border-top-width: 2px;
  border-top-color: #D3D3D3;
}

#cfsutntxse .gt_grand_summary_row {
  color: #333333;
  background-color: #FFFFFF;
  text-transform: inherit;
  padding-top: 8px;
  padding-bottom: 8px;
  padding-left: 5px;
  padding-right: 5px;
}

#cfsutntxse .gt_first_grand_summary_row {
  padding-top: 8px;
  padding-bottom: 8px;
  padding-left: 5px;
  padding-right: 5px;
  border-top-style: double;
  border-top-width: 6px;
  border-top-color: #D3D3D3;
}

#cfsutntxse .gt_striped {
  background-color: rgba(128, 128, 128, 0.05);
}

#cfsutntxse .gt_table_body {
  border-top-style: solid;
  border-top-width: 2px;
  border-top-color: #D3D3D3;
  border-bottom-style: solid;
  border-bottom-width: 2px;
  border-bottom-color: #D3D3D3;
}

#cfsutntxse .gt_footnotes {
  color: #333333;
  background-color: #FFFFFF;
  border-bottom-style: none;
  border-bottom-width: 2px;
  border-bottom-color: #D3D3D3;
  border-left-style: none;
  border-left-width: 2px;
  border-left-color: #D3D3D3;
  border-right-style: none;
  border-right-width: 2px;
  border-right-color: #D3D3D3;
}

#cfsutntxse .gt_footnote {
  margin: 0px;
  font-size: 90%;
  padding: 4px;
}

#cfsutntxse .gt_sourcenotes {
  color: #333333;
  background-color: #FFFFFF;
  border-bottom-style: none;
  border-bottom-width: 2px;
  border-bottom-color: #D3D3D3;
  border-left-style: none;
  border-left-width: 2px;
  border-left-color: #D3D3D3;
  border-right-style: none;
  border-right-width: 2px;
  border-right-color: #D3D3D3;
}

#cfsutntxse .gt_sourcenote {
  font-size: 90%;
  padding: 4px;
}

#cfsutntxse .gt_left {
  text-align: left;
}

#cfsutntxse .gt_center {
  text-align: center;
}

#cfsutntxse .gt_right {
  text-align: right;
  font-variant-numeric: tabular-nums;
}

#cfsutntxse .gt_font_normal {
  font-weight: normal;
}

#cfsutntxse .gt_font_bold {
  font-weight: bold;
}

#cfsutntxse .gt_font_italic {
  font-style: italic;
}

#cfsutntxse .gt_super {
  font-size: 65%;
}

#cfsutntxse .gt_footnote_marks {
  font-style: italic;
  font-weight: normal;
  font-size: 65%;
}
</style>
<table class="gt_table" style="table-layout: fixed;; width: 0px">
  <colgroup>
    <col style="width:500px;"/>
    <col style="width:200px;"/>
  </colgroup>
  
  <thead class="gt_col_headings">
    <tr>
      <th class="gt_col_heading gt_columns_bottom_border gt_left" rowspan="1" colspan="1"><strong>Description</strong></th>
      <th class="gt_col_heading gt_columns_bottom_border gt_right" rowspan="1" colspan="1"></th>
    </tr>
  </thead>
  <tbody class="gt_table_body">
    <tr><td class="gt_row gt_left">Method to change all character values to numeric values in selected character columns of a dataframe</td>
<td class="gt_row gt_right"><svg aria-hidden="true" role="img" viewBox="0 0 512 512" style="height:2em;width:2em;vertical-align:-0.125em;margin-left:auto;margin-right:auto;font-size:inherit;fill:#A62014;overflow:visible;position:relative;"><path d="M330.67 263.12V173.4l-52.75-24.22C219.44 218.76 197.58 400 56 400a56 56 0 0 0 0 112c212.64 0 370.65-122.87 419.18-210.34l-37.05-38.54zm131.09-128.37C493.92 74.91 477.18 26.48 458.62 3a8 8 0 0 0-11.93-.59l-22.9 23a8.06 8.06 0 0 0-.89 10.23c6.86 10.36 17.05 35.1-1.4 72.32A142.85 142.85 0 0 0 364.34 96c-28 0-54 8.54-76.34 22.59l74.67 34.29v78.24h89.09L506.44 288c3.26-12.62 5.56-25.63 5.56-39.31a154 154 0 0 0-50.24-113.94z"/></svg><svg aria-hidden="true" role="img" viewBox="0 0 512 512" style="height:2em;width:2em;vertical-align:-0.125em;margin-left:auto;margin-right:auto;font-size:inherit;fill:#9FC2B9;overflow:visible;position:relative;"><path d="M330.67 263.12V173.4l-52.75-24.22C219.44 218.76 197.58 400 56 400a56 56 0 0 0 0 112c212.64 0 370.65-122.87 419.18-210.34l-37.05-38.54zm131.09-128.37C493.92 74.91 477.18 26.48 458.62 3a8 8 0 0 0-11.93-.59l-22.9 23a8.06 8.06 0 0 0-.89 10.23c6.86 10.36 17.05 35.1-1.4 72.32A142.85 142.85 0 0 0 364.34 96c-28 0-54 8.54-76.34 22.59l74.67 34.29v78.24h89.09L506.44 288c3.26-12.62 5.56-25.63 5.56-39.31a154 154 0 0 0-50.24-113.94z"/></svg><svg aria-hidden="true" role="img" viewBox="0 0 512 512" style="height:2em;width:2em;vertical-align:-0.125em;margin-left:auto;margin-right:auto;font-size:inherit;fill:#9FC2B9;overflow:visible;position:relative;"><path d="M330.67 263.12V173.4l-52.75-24.22C219.44 218.76 197.58 400 56 400a56 56 0 0 0 0 112c212.64 0 370.65-122.87 419.18-210.34l-37.05-38.54zm131.09-128.37C493.92 74.91 477.18 26.48 458.62 3a8 8 0 0 0-11.93-.59l-22.9 23a8.06 8.06 0 0 0-.89 10.23c6.86 10.36 17.05 35.1-1.4 72.32A142.85 142.85 0 0 0 364.34 96c-28 0-54 8.54-76.34 22.59l74.67 34.29v78.24h89.09L506.44 288c3.26-12.62 5.56-25.63 5.56-39.31a154 154 0 0 0-50.24-113.94z"/></svg></td></tr>
  </tbody>
  
  
</table>
</div>
```

```{=html}
<div id="yoprreljmk" style="overflow-x:auto;overflow-y:auto;width:auto;height:auto;">
<style>html {
  font-family: -apple-system, BlinkMacSystemFont, 'Segoe UI', Roboto, Oxygen, Ubuntu, Cantarell, 'Helvetica Neue', 'Fira Sans', 'Droid Sans', Arial, sans-serif;
}

#yoprreljmk .gt_table {
  display: table;
  border-collapse: collapse;
  margin-left: auto;
  margin-right: auto;
  color: #333333;
  font-size: 16px;
  font-weight: normal;
  font-style: normal;
  background-color: #FFFFFF;
  width: auto;
  border-top-style: solid;
  border-top-width: 2px;
  border-top-color: #A8A8A8;
  border-right-style: none;
  border-right-width: 2px;
  border-right-color: #D3D3D3;
  border-bottom-style: solid;
  border-bottom-width: 2px;
  border-bottom-color: #A8A8A8;
  border-left-style: none;
  border-left-width: 2px;
  border-left-color: #D3D3D3;
}

#yoprreljmk .gt_heading {
  background-color: #153331;
  text-align: center;
  border-bottom-color: #FFFFFF;
  border-left-style: none;
  border-left-width: 1px;
  border-left-color: #D3D3D3;
  border-right-style: none;
  border-right-width: 1px;
  border-right-color: #D3D3D3;
}

#yoprreljmk .gt_title {
  color: #FFFFFF;
  font-size: 125%;
  font-weight: initial;
  padding-top: 4px;
  padding-bottom: 4px;
  border-bottom-color: #FFFFFF;
  border-bottom-width: 0;
}

#yoprreljmk .gt_subtitle {
  color: #FFFFFF;
  font-size: 85%;
  font-weight: initial;
  padding-top: 0;
  padding-bottom: 6px;
  border-top-color: #FFFFFF;
  border-top-width: 0;
}

#yoprreljmk .gt_bottom_border {
  border-bottom-style: solid;
  border-bottom-width: 2px;
  border-bottom-color: #D3D3D3;
}

#yoprreljmk .gt_col_headings {
  border-top-style: solid;
  border-top-width: 2px;
  border-top-color: #D3D3D3;
  border-bottom-style: solid;
  border-bottom-width: 2px;
  border-bottom-color: #D3D3D3;
  border-left-style: none;
  border-left-width: 1px;
  border-left-color: #D3D3D3;
  border-right-style: none;
  border-right-width: 1px;
  border-right-color: #D3D3D3;
}

#yoprreljmk .gt_col_heading {
  color: #FFFFFF;
  background-color: #1E6E6E;
  font-size: 100%;
  font-weight: normal;
  text-transform: inherit;
  border-left-style: none;
  border-left-width: 1px;
  border-left-color: #D3D3D3;
  border-right-style: none;
  border-right-width: 1px;
  border-right-color: #D3D3D3;
  vertical-align: bottom;
  padding-top: 5px;
  padding-bottom: 6px;
  padding-left: 5px;
  padding-right: 5px;
  overflow-x: hidden;
}

#yoprreljmk .gt_column_spanner_outer {
  color: #FFFFFF;
  background-color: #1E6E6E;
  font-size: 100%;
  font-weight: normal;
  text-transform: inherit;
  padding-top: 0;
  padding-bottom: 0;
  padding-left: 4px;
  padding-right: 4px;
}

#yoprreljmk .gt_column_spanner_outer:first-child {
  padding-left: 0;
}

#yoprreljmk .gt_column_spanner_outer:last-child {
  padding-right: 0;
}

#yoprreljmk .gt_column_spanner {
  border-bottom-style: solid;
  border-bottom-width: 2px;
  border-bottom-color: #D3D3D3;
  vertical-align: bottom;
  padding-top: 5px;
  padding-bottom: 5px;
  overflow-x: hidden;
  display: inline-block;
  width: 100%;
}

#yoprreljmk .gt_group_heading {
  padding: 8px;
  color: #333333;
  background-color: #FFFFFF;
  font-size: 100%;
  font-weight: initial;
  text-transform: inherit;
  border-top-style: solid;
  border-top-width: 2px;
  border-top-color: #D3D3D3;
  border-bottom-style: solid;
  border-bottom-width: 2px;
  border-bottom-color: #D3D3D3;
  border-left-style: none;
  border-left-width: 1px;
  border-left-color: #D3D3D3;
  border-right-style: none;
  border-right-width: 1px;
  border-right-color: #D3D3D3;
  vertical-align: middle;
}

#yoprreljmk .gt_empty_group_heading {
  padding: 0.5px;
  color: #333333;
  background-color: #FFFFFF;
  font-size: 100%;
  font-weight: initial;
  border-top-style: solid;
  border-top-width: 2px;
  border-top-color: #D3D3D3;
  border-bottom-style: solid;
  border-bottom-width: 2px;
  border-bottom-color: #D3D3D3;
  vertical-align: middle;
}

#yoprreljmk .gt_from_md > :first-child {
  margin-top: 0;
}

#yoprreljmk .gt_from_md > :last-child {
  margin-bottom: 0;
}

#yoprreljmk .gt_row {
  padding-top: 8px;
  padding-bottom: 8px;
  padding-left: 5px;
  padding-right: 5px;
  margin: 10px;
  border-top-style: solid;
  border-top-width: 1px;
  border-top-color: #D3D3D3;
  border-left-style: none;
  border-left-width: 1px;
  border-left-color: #D3D3D3;
  border-right-style: none;
  border-right-width: 1px;
  border-right-color: #D3D3D3;
  vertical-align: middle;
  overflow-x: hidden;
}

#yoprreljmk .gt_stub {
  color: #333333;
  background-color: #FFFFFF;
  font-size: 100%;
  font-weight: initial;
  text-transform: inherit;
  border-right-style: solid;
  border-right-width: 2px;
  border-right-color: #D3D3D3;
  padding-left: 12px;
}

#yoprreljmk .gt_summary_row {
  color: #333333;
  background-color: #FFFFFF;
  text-transform: inherit;
  padding-top: 8px;
  padding-bottom: 8px;
  padding-left: 5px;
  padding-right: 5px;
}

#yoprreljmk .gt_first_summary_row {
  padding-top: 8px;
  padding-bottom: 8px;
  padding-left: 5px;
  padding-right: 5px;
  border-top-style: solid;
  border-top-width: 2px;
  border-top-color: #D3D3D3;
}

#yoprreljmk .gt_grand_summary_row {
  color: #333333;
  background-color: #FFFFFF;
  text-transform: inherit;
  padding-top: 8px;
  padding-bottom: 8px;
  padding-left: 5px;
  padding-right: 5px;
}

#yoprreljmk .gt_first_grand_summary_row {
  padding-top: 8px;
  padding-bottom: 8px;
  padding-left: 5px;
  padding-right: 5px;
  border-top-style: double;
  border-top-width: 6px;
  border-top-color: #D3D3D3;
}

#yoprreljmk .gt_striped {
  background-color: rgba(128, 128, 128, 0.05);
}

#yoprreljmk .gt_table_body {
  border-top-style: solid;
  border-top-width: 2px;
  border-top-color: #D3D3D3;
  border-bottom-style: solid;
  border-bottom-width: 2px;
  border-bottom-color: #D3D3D3;
}

#yoprreljmk .gt_footnotes {
  color: #333333;
  background-color: #FFFFFF;
  border-bottom-style: none;
  border-bottom-width: 2px;
  border-bottom-color: #D3D3D3;
  border-left-style: none;
  border-left-width: 2px;
  border-left-color: #D3D3D3;
  border-right-style: none;
  border-right-width: 2px;
  border-right-color: #D3D3D3;
}

#yoprreljmk .gt_footnote {
  margin: 0px;
  font-size: 90%;
  padding: 4px;
}

#yoprreljmk .gt_sourcenotes {
  color: #333333;
  background-color: #FFFFFF;
  border-bottom-style: none;
  border-bottom-width: 2px;
  border-bottom-color: #D3D3D3;
  border-left-style: none;
  border-left-width: 2px;
  border-left-color: #D3D3D3;
  border-right-style: none;
  border-right-width: 2px;
  border-right-color: #D3D3D3;
}

#yoprreljmk .gt_sourcenote {
  font-size: 90%;
  padding: 4px;
}

#yoprreljmk .gt_left {
  text-align: left;
}

#yoprreljmk .gt_center {
  text-align: center;
}

#yoprreljmk .gt_right {
  text-align: right;
  font-variant-numeric: tabular-nums;
}

#yoprreljmk .gt_font_normal {
  font-weight: normal;
}

#yoprreljmk .gt_font_bold {
  font-weight: bold;
}

#yoprreljmk .gt_font_italic {
  font-style: italic;
}

#yoprreljmk .gt_super {
  font-size: 65%;
}

#yoprreljmk .gt_footnote_marks {
  font-style: italic;
  font-weight: normal;
  font-size: 65%;
}
</style>
<table class="gt_table" style="table-layout: fixed;; width: 0px">
  <colgroup>
    <col style="width:350px;"/>
    <col style="width:350px;"/>
  </colgroup>
  <thead class="gt_header">
    <tr>
      <th colspan="2" class="gt_heading gt_title gt_font_normal gt_bottom_border" style>Ingredients</th>
    </tr>
    
  </thead>
  <thead class="gt_col_headings">
    <tr>
      <th class="gt_col_heading gt_columns_bottom_border gt_center" rowspan="1" colspan="1"><strong>Package</strong></th>
      <th class="gt_col_heading gt_columns_bottom_border gt_center" rowspan="1" colspan="1"><strong>Data</strong></th>
    </tr>
  </thead>
  <tbody class="gt_table_body">
    <tr><td class="gt_row gt_center"><div class='gt_from_md'><p>readr<br>dplyr</p>
</div></td>
<td class="gt_row gt_center"><div class='gt_from_md'><p>sample.csv</p>
</div></td></tr>
  </tbody>
  
  
</table>
</div>
```

</br>

**Preparation**

```r
df <- readr::read_csv("C:/data/sample.csv")
```

</br>

**Sample Instructions**

```r
package::function(data, c("column_name1", "column_name2"), as.numeric)
```

</br>

**Actual Instructions**

```r
dplyr::mutate_at(df, c("column1", "column2"), as.numeric)
```


### Change numeric data type to character data type in selected columns

```{=html}
<div id="oyidsfrlfl" style="overflow-x:auto;overflow-y:auto;width:auto;height:auto;">
<style>html {
  font-family: -apple-system, BlinkMacSystemFont, 'Segoe UI', Roboto, Oxygen, Ubuntu, Cantarell, 'Helvetica Neue', 'Fira Sans', 'Droid Sans', Arial, sans-serif;
}

#oyidsfrlfl .gt_table {
  display: table;
  border-collapse: collapse;
  margin-left: auto;
  margin-right: auto;
  color: #333333;
  font-size: 16px;
  font-weight: normal;
  font-style: normal;
  background-color: #FFFFFF;
  width: auto;
  border-top-style: solid;
  border-top-width: 2px;
  border-top-color: #A8A8A8;
  border-right-style: none;
  border-right-width: 2px;
  border-right-color: #D3D3D3;
  border-bottom-style: solid;
  border-bottom-width: 2px;
  border-bottom-color: #A8A8A8;
  border-left-style: none;
  border-left-width: 2px;
  border-left-color: #D3D3D3;
}

#oyidsfrlfl .gt_heading {
  background-color: #153331;
  text-align: center;
  border-bottom-color: #FFFFFF;
  border-left-style: none;
  border-left-width: 1px;
  border-left-color: #D3D3D3;
  border-right-style: none;
  border-right-width: 1px;
  border-right-color: #D3D3D3;
}

#oyidsfrlfl .gt_title {
  color: #FFFFFF;
  font-size: 125%;
  font-weight: initial;
  padding-top: 4px;
  padding-bottom: 4px;
  border-bottom-color: #FFFFFF;
  border-bottom-width: 0;
}

#oyidsfrlfl .gt_subtitle {
  color: #FFFFFF;
  font-size: 85%;
  font-weight: initial;
  padding-top: 0;
  padding-bottom: 6px;
  border-top-color: #FFFFFF;
  border-top-width: 0;
}

#oyidsfrlfl .gt_bottom_border {
  border-bottom-style: solid;
  border-bottom-width: 2px;
  border-bottom-color: #D3D3D3;
}

#oyidsfrlfl .gt_col_headings {
  border-top-style: solid;
  border-top-width: 2px;
  border-top-color: #D3D3D3;
  border-bottom-style: solid;
  border-bottom-width: 2px;
  border-bottom-color: #D3D3D3;
  border-left-style: none;
  border-left-width: 1px;
  border-left-color: #D3D3D3;
  border-right-style: none;
  border-right-width: 1px;
  border-right-color: #D3D3D3;
}

#oyidsfrlfl .gt_col_heading {
  color: #FFFFFF;
  background-color: #153331;
  font-size: 100%;
  font-weight: normal;
  text-transform: inherit;
  border-left-style: none;
  border-left-width: 1px;
  border-left-color: #D3D3D3;
  border-right-style: none;
  border-right-width: 1px;
  border-right-color: #D3D3D3;
  vertical-align: bottom;
  padding-top: 5px;
  padding-bottom: 6px;
  padding-left: 5px;
  padding-right: 5px;
  overflow-x: hidden;
}

#oyidsfrlfl .gt_column_spanner_outer {
  color: #FFFFFF;
  background-color: #153331;
  font-size: 100%;
  font-weight: normal;
  text-transform: inherit;
  padding-top: 0;
  padding-bottom: 0;
  padding-left: 4px;
  padding-right: 4px;
}

#oyidsfrlfl .gt_column_spanner_outer:first-child {
  padding-left: 0;
}

#oyidsfrlfl .gt_column_spanner_outer:last-child {
  padding-right: 0;
}

#oyidsfrlfl .gt_column_spanner {
  border-bottom-style: solid;
  border-bottom-width: 2px;
  border-bottom-color: #D3D3D3;
  vertical-align: bottom;
  padding-top: 5px;
  padding-bottom: 5px;
  overflow-x: hidden;
  display: inline-block;
  width: 100%;
}

#oyidsfrlfl .gt_group_heading {
  padding: 8px;
  color: #333333;
  background-color: #FFFFFF;
  font-size: 100%;
  font-weight: initial;
  text-transform: inherit;
  border-top-style: solid;
  border-top-width: 2px;
  border-top-color: #D3D3D3;
  border-bottom-style: solid;
  border-bottom-width: 2px;
  border-bottom-color: #D3D3D3;
  border-left-style: none;
  border-left-width: 1px;
  border-left-color: #D3D3D3;
  border-right-style: none;
  border-right-width: 1px;
  border-right-color: #D3D3D3;
  vertical-align: middle;
}

#oyidsfrlfl .gt_empty_group_heading {
  padding: 0.5px;
  color: #333333;
  background-color: #FFFFFF;
  font-size: 100%;
  font-weight: initial;
  border-top-style: solid;
  border-top-width: 2px;
  border-top-color: #D3D3D3;
  border-bottom-style: solid;
  border-bottom-width: 2px;
  border-bottom-color: #D3D3D3;
  vertical-align: middle;
}

#oyidsfrlfl .gt_from_md > :first-child {
  margin-top: 0;
}

#oyidsfrlfl .gt_from_md > :last-child {
  margin-bottom: 0;
}

#oyidsfrlfl .gt_row {
  padding-top: 8px;
  padding-bottom: 8px;
  padding-left: 5px;
  padding-right: 5px;
  margin: 10px;
  border-top-style: solid;
  border-top-width: 1px;
  border-top-color: #D3D3D3;
  border-left-style: none;
  border-left-width: 1px;
  border-left-color: #D3D3D3;
  border-right-style: none;
  border-right-width: 1px;
  border-right-color: #D3D3D3;
  vertical-align: middle;
  overflow-x: hidden;
}

#oyidsfrlfl .gt_stub {
  color: #333333;
  background-color: #FFFFFF;
  font-size: 100%;
  font-weight: initial;
  text-transform: inherit;
  border-right-style: solid;
  border-right-width: 2px;
  border-right-color: #D3D3D3;
  padding-left: 12px;
}

#oyidsfrlfl .gt_summary_row {
  color: #333333;
  background-color: #FFFFFF;
  text-transform: inherit;
  padding-top: 8px;
  padding-bottom: 8px;
  padding-left: 5px;
  padding-right: 5px;
}

#oyidsfrlfl .gt_first_summary_row {
  padding-top: 8px;
  padding-bottom: 8px;
  padding-left: 5px;
  padding-right: 5px;
  border-top-style: solid;
  border-top-width: 2px;
  border-top-color: #D3D3D3;
}

#oyidsfrlfl .gt_grand_summary_row {
  color: #333333;
  background-color: #FFFFFF;
  text-transform: inherit;
  padding-top: 8px;
  padding-bottom: 8px;
  padding-left: 5px;
  padding-right: 5px;
}

#oyidsfrlfl .gt_first_grand_summary_row {
  padding-top: 8px;
  padding-bottom: 8px;
  padding-left: 5px;
  padding-right: 5px;
  border-top-style: double;
  border-top-width: 6px;
  border-top-color: #D3D3D3;
}

#oyidsfrlfl .gt_striped {
  background-color: rgba(128, 128, 128, 0.05);
}

#oyidsfrlfl .gt_table_body {
  border-top-style: solid;
  border-top-width: 2px;
  border-top-color: #D3D3D3;
  border-bottom-style: solid;
  border-bottom-width: 2px;
  border-bottom-color: #D3D3D3;
}

#oyidsfrlfl .gt_footnotes {
  color: #333333;
  background-color: #FFFFFF;
  border-bottom-style: none;
  border-bottom-width: 2px;
  border-bottom-color: #D3D3D3;
  border-left-style: none;
  border-left-width: 2px;
  border-left-color: #D3D3D3;
  border-right-style: none;
  border-right-width: 2px;
  border-right-color: #D3D3D3;
}

#oyidsfrlfl .gt_footnote {
  margin: 0px;
  font-size: 90%;
  padding: 4px;
}

#oyidsfrlfl .gt_sourcenotes {
  color: #333333;
  background-color: #FFFFFF;
  border-bottom-style: none;
  border-bottom-width: 2px;
  border-bottom-color: #D3D3D3;
  border-left-style: none;
  border-left-width: 2px;
  border-left-color: #D3D3D3;
  border-right-style: none;
  border-right-width: 2px;
  border-right-color: #D3D3D3;
}

#oyidsfrlfl .gt_sourcenote {
  font-size: 90%;
  padding: 4px;
}

#oyidsfrlfl .gt_left {
  text-align: left;
}

#oyidsfrlfl .gt_center {
  text-align: center;
}

#oyidsfrlfl .gt_right {
  text-align: right;
  font-variant-numeric: tabular-nums;
}

#oyidsfrlfl .gt_font_normal {
  font-weight: normal;
}

#oyidsfrlfl .gt_font_bold {
  font-weight: bold;
}

#oyidsfrlfl .gt_font_italic {
  font-style: italic;
}

#oyidsfrlfl .gt_super {
  font-size: 65%;
}

#oyidsfrlfl .gt_footnote_marks {
  font-style: italic;
  font-weight: normal;
  font-size: 65%;
}
</style>
<table class="gt_table" style="table-layout: fixed;; width: 0px">
  <colgroup>
    <col style="width:500px;"/>
    <col style="width:200px;"/>
  </colgroup>
  
  <thead class="gt_col_headings">
    <tr>
      <th class="gt_col_heading gt_columns_bottom_border gt_left" rowspan="1" colspan="1"><strong>Description</strong></th>
      <th class="gt_col_heading gt_columns_bottom_border gt_right" rowspan="1" colspan="1"></th>
    </tr>
  </thead>
  <tbody class="gt_table_body">
    <tr><td class="gt_row gt_left">Method to change all numeric values to character values in selected numeric columns of a dataframe</td>
<td class="gt_row gt_right"><svg aria-hidden="true" role="img" viewBox="0 0 512 512" style="height:2em;width:2em;vertical-align:-0.125em;margin-left:auto;margin-right:auto;font-size:inherit;fill:#A62014;overflow:visible;position:relative;"><path d="M330.67 263.12V173.4l-52.75-24.22C219.44 218.76 197.58 400 56 400a56 56 0 0 0 0 112c212.64 0 370.65-122.87 419.18-210.34l-37.05-38.54zm131.09-128.37C493.92 74.91 477.18 26.48 458.62 3a8 8 0 0 0-11.93-.59l-22.9 23a8.06 8.06 0 0 0-.89 10.23c6.86 10.36 17.05 35.1-1.4 72.32A142.85 142.85 0 0 0 364.34 96c-28 0-54 8.54-76.34 22.59l74.67 34.29v78.24h89.09L506.44 288c3.26-12.62 5.56-25.63 5.56-39.31a154 154 0 0 0-50.24-113.94z"/></svg><svg aria-hidden="true" role="img" viewBox="0 0 512 512" style="height:2em;width:2em;vertical-align:-0.125em;margin-left:auto;margin-right:auto;font-size:inherit;fill:#9FC2B9;overflow:visible;position:relative;"><path d="M330.67 263.12V173.4l-52.75-24.22C219.44 218.76 197.58 400 56 400a56 56 0 0 0 0 112c212.64 0 370.65-122.87 419.18-210.34l-37.05-38.54zm131.09-128.37C493.92 74.91 477.18 26.48 458.62 3a8 8 0 0 0-11.93-.59l-22.9 23a8.06 8.06 0 0 0-.89 10.23c6.86 10.36 17.05 35.1-1.4 72.32A142.85 142.85 0 0 0 364.34 96c-28 0-54 8.54-76.34 22.59l74.67 34.29v78.24h89.09L506.44 288c3.26-12.62 5.56-25.63 5.56-39.31a154 154 0 0 0-50.24-113.94z"/></svg><svg aria-hidden="true" role="img" viewBox="0 0 512 512" style="height:2em;width:2em;vertical-align:-0.125em;margin-left:auto;margin-right:auto;font-size:inherit;fill:#9FC2B9;overflow:visible;position:relative;"><path d="M330.67 263.12V173.4l-52.75-24.22C219.44 218.76 197.58 400 56 400a56 56 0 0 0 0 112c212.64 0 370.65-122.87 419.18-210.34l-37.05-38.54zm131.09-128.37C493.92 74.91 477.18 26.48 458.62 3a8 8 0 0 0-11.93-.59l-22.9 23a8.06 8.06 0 0 0-.89 10.23c6.86 10.36 17.05 35.1-1.4 72.32A142.85 142.85 0 0 0 364.34 96c-28 0-54 8.54-76.34 22.59l74.67 34.29v78.24h89.09L506.44 288c3.26-12.62 5.56-25.63 5.56-39.31a154 154 0 0 0-50.24-113.94z"/></svg></td></tr>
  </tbody>
  
  
</table>
</div>
```

```{=html}
<div id="nhgtrpzevy" style="overflow-x:auto;overflow-y:auto;width:auto;height:auto;">
<style>html {
  font-family: -apple-system, BlinkMacSystemFont, 'Segoe UI', Roboto, Oxygen, Ubuntu, Cantarell, 'Helvetica Neue', 'Fira Sans', 'Droid Sans', Arial, sans-serif;
}

#nhgtrpzevy .gt_table {
  display: table;
  border-collapse: collapse;
  margin-left: auto;
  margin-right: auto;
  color: #333333;
  font-size: 16px;
  font-weight: normal;
  font-style: normal;
  background-color: #FFFFFF;
  width: auto;
  border-top-style: solid;
  border-top-width: 2px;
  border-top-color: #A8A8A8;
  border-right-style: none;
  border-right-width: 2px;
  border-right-color: #D3D3D3;
  border-bottom-style: solid;
  border-bottom-width: 2px;
  border-bottom-color: #A8A8A8;
  border-left-style: none;
  border-left-width: 2px;
  border-left-color: #D3D3D3;
}

#nhgtrpzevy .gt_heading {
  background-color: #153331;
  text-align: center;
  border-bottom-color: #FFFFFF;
  border-left-style: none;
  border-left-width: 1px;
  border-left-color: #D3D3D3;
  border-right-style: none;
  border-right-width: 1px;
  border-right-color: #D3D3D3;
}

#nhgtrpzevy .gt_title {
  color: #FFFFFF;
  font-size: 125%;
  font-weight: initial;
  padding-top: 4px;
  padding-bottom: 4px;
  border-bottom-color: #FFFFFF;
  border-bottom-width: 0;
}

#nhgtrpzevy .gt_subtitle {
  color: #FFFFFF;
  font-size: 85%;
  font-weight: initial;
  padding-top: 0;
  padding-bottom: 6px;
  border-top-color: #FFFFFF;
  border-top-width: 0;
}

#nhgtrpzevy .gt_bottom_border {
  border-bottom-style: solid;
  border-bottom-width: 2px;
  border-bottom-color: #D3D3D3;
}

#nhgtrpzevy .gt_col_headings {
  border-top-style: solid;
  border-top-width: 2px;
  border-top-color: #D3D3D3;
  border-bottom-style: solid;
  border-bottom-width: 2px;
  border-bottom-color: #D3D3D3;
  border-left-style: none;
  border-left-width: 1px;
  border-left-color: #D3D3D3;
  border-right-style: none;
  border-right-width: 1px;
  border-right-color: #D3D3D3;
}

#nhgtrpzevy .gt_col_heading {
  color: #FFFFFF;
  background-color: #1E6E6E;
  font-size: 100%;
  font-weight: normal;
  text-transform: inherit;
  border-left-style: none;
  border-left-width: 1px;
  border-left-color: #D3D3D3;
  border-right-style: none;
  border-right-width: 1px;
  border-right-color: #D3D3D3;
  vertical-align: bottom;
  padding-top: 5px;
  padding-bottom: 6px;
  padding-left: 5px;
  padding-right: 5px;
  overflow-x: hidden;
}

#nhgtrpzevy .gt_column_spanner_outer {
  color: #FFFFFF;
  background-color: #1E6E6E;
  font-size: 100%;
  font-weight: normal;
  text-transform: inherit;
  padding-top: 0;
  padding-bottom: 0;
  padding-left: 4px;
  padding-right: 4px;
}

#nhgtrpzevy .gt_column_spanner_outer:first-child {
  padding-left: 0;
}

#nhgtrpzevy .gt_column_spanner_outer:last-child {
  padding-right: 0;
}

#nhgtrpzevy .gt_column_spanner {
  border-bottom-style: solid;
  border-bottom-width: 2px;
  border-bottom-color: #D3D3D3;
  vertical-align: bottom;
  padding-top: 5px;
  padding-bottom: 5px;
  overflow-x: hidden;
  display: inline-block;
  width: 100%;
}

#nhgtrpzevy .gt_group_heading {
  padding: 8px;
  color: #333333;
  background-color: #FFFFFF;
  font-size: 100%;
  font-weight: initial;
  text-transform: inherit;
  border-top-style: solid;
  border-top-width: 2px;
  border-top-color: #D3D3D3;
  border-bottom-style: solid;
  border-bottom-width: 2px;
  border-bottom-color: #D3D3D3;
  border-left-style: none;
  border-left-width: 1px;
  border-left-color: #D3D3D3;
  border-right-style: none;
  border-right-width: 1px;
  border-right-color: #D3D3D3;
  vertical-align: middle;
}

#nhgtrpzevy .gt_empty_group_heading {
  padding: 0.5px;
  color: #333333;
  background-color: #FFFFFF;
  font-size: 100%;
  font-weight: initial;
  border-top-style: solid;
  border-top-width: 2px;
  border-top-color: #D3D3D3;
  border-bottom-style: solid;
  border-bottom-width: 2px;
  border-bottom-color: #D3D3D3;
  vertical-align: middle;
}

#nhgtrpzevy .gt_from_md > :first-child {
  margin-top: 0;
}

#nhgtrpzevy .gt_from_md > :last-child {
  margin-bottom: 0;
}

#nhgtrpzevy .gt_row {
  padding-top: 8px;
  padding-bottom: 8px;
  padding-left: 5px;
  padding-right: 5px;
  margin: 10px;
  border-top-style: solid;
  border-top-width: 1px;
  border-top-color: #D3D3D3;
  border-left-style: none;
  border-left-width: 1px;
  border-left-color: #D3D3D3;
  border-right-style: none;
  border-right-width: 1px;
  border-right-color: #D3D3D3;
  vertical-align: middle;
  overflow-x: hidden;
}

#nhgtrpzevy .gt_stub {
  color: #333333;
  background-color: #FFFFFF;
  font-size: 100%;
  font-weight: initial;
  text-transform: inherit;
  border-right-style: solid;
  border-right-width: 2px;
  border-right-color: #D3D3D3;
  padding-left: 12px;
}

#nhgtrpzevy .gt_summary_row {
  color: #333333;
  background-color: #FFFFFF;
  text-transform: inherit;
  padding-top: 8px;
  padding-bottom: 8px;
  padding-left: 5px;
  padding-right: 5px;
}

#nhgtrpzevy .gt_first_summary_row {
  padding-top: 8px;
  padding-bottom: 8px;
  padding-left: 5px;
  padding-right: 5px;
  border-top-style: solid;
  border-top-width: 2px;
  border-top-color: #D3D3D3;
}

#nhgtrpzevy .gt_grand_summary_row {
  color: #333333;
  background-color: #FFFFFF;
  text-transform: inherit;
  padding-top: 8px;
  padding-bottom: 8px;
  padding-left: 5px;
  padding-right: 5px;
}

#nhgtrpzevy .gt_first_grand_summary_row {
  padding-top: 8px;
  padding-bottom: 8px;
  padding-left: 5px;
  padding-right: 5px;
  border-top-style: double;
  border-top-width: 6px;
  border-top-color: #D3D3D3;
}

#nhgtrpzevy .gt_striped {
  background-color: rgba(128, 128, 128, 0.05);
}

#nhgtrpzevy .gt_table_body {
  border-top-style: solid;
  border-top-width: 2px;
  border-top-color: #D3D3D3;
  border-bottom-style: solid;
  border-bottom-width: 2px;
  border-bottom-color: #D3D3D3;
}

#nhgtrpzevy .gt_footnotes {
  color: #333333;
  background-color: #FFFFFF;
  border-bottom-style: none;
  border-bottom-width: 2px;
  border-bottom-color: #D3D3D3;
  border-left-style: none;
  border-left-width: 2px;
  border-left-color: #D3D3D3;
  border-right-style: none;
  border-right-width: 2px;
  border-right-color: #D3D3D3;
}

#nhgtrpzevy .gt_footnote {
  margin: 0px;
  font-size: 90%;
  padding: 4px;
}

#nhgtrpzevy .gt_sourcenotes {
  color: #333333;
  background-color: #FFFFFF;
  border-bottom-style: none;
  border-bottom-width: 2px;
  border-bottom-color: #D3D3D3;
  border-left-style: none;
  border-left-width: 2px;
  border-left-color: #D3D3D3;
  border-right-style: none;
  border-right-width: 2px;
  border-right-color: #D3D3D3;
}

#nhgtrpzevy .gt_sourcenote {
  font-size: 90%;
  padding: 4px;
}

#nhgtrpzevy .gt_left {
  text-align: left;
}

#nhgtrpzevy .gt_center {
  text-align: center;
}

#nhgtrpzevy .gt_right {
  text-align: right;
  font-variant-numeric: tabular-nums;
}

#nhgtrpzevy .gt_font_normal {
  font-weight: normal;
}

#nhgtrpzevy .gt_font_bold {
  font-weight: bold;
}

#nhgtrpzevy .gt_font_italic {
  font-style: italic;
}

#nhgtrpzevy .gt_super {
  font-size: 65%;
}

#nhgtrpzevy .gt_footnote_marks {
  font-style: italic;
  font-weight: normal;
  font-size: 65%;
}
</style>
<table class="gt_table" style="table-layout: fixed;; width: 0px">
  <colgroup>
    <col style="width:350px;"/>
    <col style="width:350px;"/>
  </colgroup>
  <thead class="gt_header">
    <tr>
      <th colspan="2" class="gt_heading gt_title gt_font_normal gt_bottom_border" style>Ingredients</th>
    </tr>
    
  </thead>
  <thead class="gt_col_headings">
    <tr>
      <th class="gt_col_heading gt_columns_bottom_border gt_center" rowspan="1" colspan="1"><strong>Package</strong></th>
      <th class="gt_col_heading gt_columns_bottom_border gt_center" rowspan="1" colspan="1"><strong>Data</strong></th>
    </tr>
  </thead>
  <tbody class="gt_table_body">
    <tr><td class="gt_row gt_center"><div class='gt_from_md'><p>readr<br>dplyr</p>
</div></td>
<td class="gt_row gt_center"><div class='gt_from_md'><p>sample.csv</p>
</div></td></tr>
  </tbody>
  
  
</table>
</div>
```

</br>

**Preparation**

```r
df <- readr::read_csv("C:/data/sample.csv")
```

</br>

**Sample Instructions**

```r
package::function(data, c("column_name1", "column_name2"), as.character)
```

</br>

**Actual Instructions**

```r
dplyr::mutate_at(df, c("column1", "column2"), as.character)
```


### Change character data type to date data type in selected columns

```{=html}
<div id="jsfzetfozm" style="overflow-x:auto;overflow-y:auto;width:auto;height:auto;">
<style>html {
  font-family: -apple-system, BlinkMacSystemFont, 'Segoe UI', Roboto, Oxygen, Ubuntu, Cantarell, 'Helvetica Neue', 'Fira Sans', 'Droid Sans', Arial, sans-serif;
}

#jsfzetfozm .gt_table {
  display: table;
  border-collapse: collapse;
  margin-left: auto;
  margin-right: auto;
  color: #333333;
  font-size: 16px;
  font-weight: normal;
  font-style: normal;
  background-color: #FFFFFF;
  width: auto;
  border-top-style: solid;
  border-top-width: 2px;
  border-top-color: #A8A8A8;
  border-right-style: none;
  border-right-width: 2px;
  border-right-color: #D3D3D3;
  border-bottom-style: solid;
  border-bottom-width: 2px;
  border-bottom-color: #A8A8A8;
  border-left-style: none;
  border-left-width: 2px;
  border-left-color: #D3D3D3;
}

#jsfzetfozm .gt_heading {
  background-color: #153331;
  text-align: center;
  border-bottom-color: #FFFFFF;
  border-left-style: none;
  border-left-width: 1px;
  border-left-color: #D3D3D3;
  border-right-style: none;
  border-right-width: 1px;
  border-right-color: #D3D3D3;
}

#jsfzetfozm .gt_title {
  color: #FFFFFF;
  font-size: 125%;
  font-weight: initial;
  padding-top: 4px;
  padding-bottom: 4px;
  border-bottom-color: #FFFFFF;
  border-bottom-width: 0;
}

#jsfzetfozm .gt_subtitle {
  color: #FFFFFF;
  font-size: 85%;
  font-weight: initial;
  padding-top: 0;
  padding-bottom: 6px;
  border-top-color: #FFFFFF;
  border-top-width: 0;
}

#jsfzetfozm .gt_bottom_border {
  border-bottom-style: solid;
  border-bottom-width: 2px;
  border-bottom-color: #D3D3D3;
}

#jsfzetfozm .gt_col_headings {
  border-top-style: solid;
  border-top-width: 2px;
  border-top-color: #D3D3D3;
  border-bottom-style: solid;
  border-bottom-width: 2px;
  border-bottom-color: #D3D3D3;
  border-left-style: none;
  border-left-width: 1px;
  border-left-color: #D3D3D3;
  border-right-style: none;
  border-right-width: 1px;
  border-right-color: #D3D3D3;
}

#jsfzetfozm .gt_col_heading {
  color: #FFFFFF;
  background-color: #153331;
  font-size: 100%;
  font-weight: normal;
  text-transform: inherit;
  border-left-style: none;
  border-left-width: 1px;
  border-left-color: #D3D3D3;
  border-right-style: none;
  border-right-width: 1px;
  border-right-color: #D3D3D3;
  vertical-align: bottom;
  padding-top: 5px;
  padding-bottom: 6px;
  padding-left: 5px;
  padding-right: 5px;
  overflow-x: hidden;
}

#jsfzetfozm .gt_column_spanner_outer {
  color: #FFFFFF;
  background-color: #153331;
  font-size: 100%;
  font-weight: normal;
  text-transform: inherit;
  padding-top: 0;
  padding-bottom: 0;
  padding-left: 4px;
  padding-right: 4px;
}

#jsfzetfozm .gt_column_spanner_outer:first-child {
  padding-left: 0;
}

#jsfzetfozm .gt_column_spanner_outer:last-child {
  padding-right: 0;
}

#jsfzetfozm .gt_column_spanner {
  border-bottom-style: solid;
  border-bottom-width: 2px;
  border-bottom-color: #D3D3D3;
  vertical-align: bottom;
  padding-top: 5px;
  padding-bottom: 5px;
  overflow-x: hidden;
  display: inline-block;
  width: 100%;
}

#jsfzetfozm .gt_group_heading {
  padding: 8px;
  color: #333333;
  background-color: #FFFFFF;
  font-size: 100%;
  font-weight: initial;
  text-transform: inherit;
  border-top-style: solid;
  border-top-width: 2px;
  border-top-color: #D3D3D3;
  border-bottom-style: solid;
  border-bottom-width: 2px;
  border-bottom-color: #D3D3D3;
  border-left-style: none;
  border-left-width: 1px;
  border-left-color: #D3D3D3;
  border-right-style: none;
  border-right-width: 1px;
  border-right-color: #D3D3D3;
  vertical-align: middle;
}

#jsfzetfozm .gt_empty_group_heading {
  padding: 0.5px;
  color: #333333;
  background-color: #FFFFFF;
  font-size: 100%;
  font-weight: initial;
  border-top-style: solid;
  border-top-width: 2px;
  border-top-color: #D3D3D3;
  border-bottom-style: solid;
  border-bottom-width: 2px;
  border-bottom-color: #D3D3D3;
  vertical-align: middle;
}

#jsfzetfozm .gt_from_md > :first-child {
  margin-top: 0;
}

#jsfzetfozm .gt_from_md > :last-child {
  margin-bottom: 0;
}

#jsfzetfozm .gt_row {
  padding-top: 8px;
  padding-bottom: 8px;
  padding-left: 5px;
  padding-right: 5px;
  margin: 10px;
  border-top-style: solid;
  border-top-width: 1px;
  border-top-color: #D3D3D3;
  border-left-style: none;
  border-left-width: 1px;
  border-left-color: #D3D3D3;
  border-right-style: none;
  border-right-width: 1px;
  border-right-color: #D3D3D3;
  vertical-align: middle;
  overflow-x: hidden;
}

#jsfzetfozm .gt_stub {
  color: #333333;
  background-color: #FFFFFF;
  font-size: 100%;
  font-weight: initial;
  text-transform: inherit;
  border-right-style: solid;
  border-right-width: 2px;
  border-right-color: #D3D3D3;
  padding-left: 12px;
}

#jsfzetfozm .gt_summary_row {
  color: #333333;
  background-color: #FFFFFF;
  text-transform: inherit;
  padding-top: 8px;
  padding-bottom: 8px;
  padding-left: 5px;
  padding-right: 5px;
}

#jsfzetfozm .gt_first_summary_row {
  padding-top: 8px;
  padding-bottom: 8px;
  padding-left: 5px;
  padding-right: 5px;
  border-top-style: solid;
  border-top-width: 2px;
  border-top-color: #D3D3D3;
}

#jsfzetfozm .gt_grand_summary_row {
  color: #333333;
  background-color: #FFFFFF;
  text-transform: inherit;
  padding-top: 8px;
  padding-bottom: 8px;
  padding-left: 5px;
  padding-right: 5px;
}

#jsfzetfozm .gt_first_grand_summary_row {
  padding-top: 8px;
  padding-bottom: 8px;
  padding-left: 5px;
  padding-right: 5px;
  border-top-style: double;
  border-top-width: 6px;
  border-top-color: #D3D3D3;
}

#jsfzetfozm .gt_striped {
  background-color: rgba(128, 128, 128, 0.05);
}

#jsfzetfozm .gt_table_body {
  border-top-style: solid;
  border-top-width: 2px;
  border-top-color: #D3D3D3;
  border-bottom-style: solid;
  border-bottom-width: 2px;
  border-bottom-color: #D3D3D3;
}

#jsfzetfozm .gt_footnotes {
  color: #333333;
  background-color: #FFFFFF;
  border-bottom-style: none;
  border-bottom-width: 2px;
  border-bottom-color: #D3D3D3;
  border-left-style: none;
  border-left-width: 2px;
  border-left-color: #D3D3D3;
  border-right-style: none;
  border-right-width: 2px;
  border-right-color: #D3D3D3;
}

#jsfzetfozm .gt_footnote {
  margin: 0px;
  font-size: 90%;
  padding: 4px;
}

#jsfzetfozm .gt_sourcenotes {
  color: #333333;
  background-color: #FFFFFF;
  border-bottom-style: none;
  border-bottom-width: 2px;
  border-bottom-color: #D3D3D3;
  border-left-style: none;
  border-left-width: 2px;
  border-left-color: #D3D3D3;
  border-right-style: none;
  border-right-width: 2px;
  border-right-color: #D3D3D3;
}

#jsfzetfozm .gt_sourcenote {
  font-size: 90%;
  padding: 4px;
}

#jsfzetfozm .gt_left {
  text-align: left;
}

#jsfzetfozm .gt_center {
  text-align: center;
}

#jsfzetfozm .gt_right {
  text-align: right;
  font-variant-numeric: tabular-nums;
}

#jsfzetfozm .gt_font_normal {
  font-weight: normal;
}

#jsfzetfozm .gt_font_bold {
  font-weight: bold;
}

#jsfzetfozm .gt_font_italic {
  font-style: italic;
}

#jsfzetfozm .gt_super {
  font-size: 65%;
}

#jsfzetfozm .gt_footnote_marks {
  font-style: italic;
  font-weight: normal;
  font-size: 65%;
}
</style>
<table class="gt_table" style="table-layout: fixed;; width: 0px">
  <colgroup>
    <col style="width:500px;"/>
    <col style="width:200px;"/>
  </colgroup>
  
  <thead class="gt_col_headings">
    <tr>
      <th class="gt_col_heading gt_columns_bottom_border gt_left" rowspan="1" colspan="1"><strong>Description</strong></th>
      <th class="gt_col_heading gt_columns_bottom_border gt_right" rowspan="1" colspan="1"></th>
    </tr>
  </thead>
  <tbody class="gt_table_body">
    <tr><td class="gt_row gt_left">Method to change all character values to date values in selected character columns of a dataframe</td>
<td class="gt_row gt_right"><svg aria-hidden="true" role="img" viewBox="0 0 512 512" style="height:2em;width:2em;vertical-align:-0.125em;margin-left:auto;margin-right:auto;font-size:inherit;fill:#A62014;overflow:visible;position:relative;"><path d="M330.67 263.12V173.4l-52.75-24.22C219.44 218.76 197.58 400 56 400a56 56 0 0 0 0 112c212.64 0 370.65-122.87 419.18-210.34l-37.05-38.54zm131.09-128.37C493.92 74.91 477.18 26.48 458.62 3a8 8 0 0 0-11.93-.59l-22.9 23a8.06 8.06 0 0 0-.89 10.23c6.86 10.36 17.05 35.1-1.4 72.32A142.85 142.85 0 0 0 364.34 96c-28 0-54 8.54-76.34 22.59l74.67 34.29v78.24h89.09L506.44 288c3.26-12.62 5.56-25.63 5.56-39.31a154 154 0 0 0-50.24-113.94z"/></svg><svg aria-hidden="true" role="img" viewBox="0 0 512 512" style="height:2em;width:2em;vertical-align:-0.125em;margin-left:auto;margin-right:auto;font-size:inherit;fill:#9FC2B9;overflow:visible;position:relative;"><path d="M330.67 263.12V173.4l-52.75-24.22C219.44 218.76 197.58 400 56 400a56 56 0 0 0 0 112c212.64 0 370.65-122.87 419.18-210.34l-37.05-38.54zm131.09-128.37C493.92 74.91 477.18 26.48 458.62 3a8 8 0 0 0-11.93-.59l-22.9 23a8.06 8.06 0 0 0-.89 10.23c6.86 10.36 17.05 35.1-1.4 72.32A142.85 142.85 0 0 0 364.34 96c-28 0-54 8.54-76.34 22.59l74.67 34.29v78.24h89.09L506.44 288c3.26-12.62 5.56-25.63 5.56-39.31a154 154 0 0 0-50.24-113.94z"/></svg><svg aria-hidden="true" role="img" viewBox="0 0 512 512" style="height:2em;width:2em;vertical-align:-0.125em;margin-left:auto;margin-right:auto;font-size:inherit;fill:#9FC2B9;overflow:visible;position:relative;"><path d="M330.67 263.12V173.4l-52.75-24.22C219.44 218.76 197.58 400 56 400a56 56 0 0 0 0 112c212.64 0 370.65-122.87 419.18-210.34l-37.05-38.54zm131.09-128.37C493.92 74.91 477.18 26.48 458.62 3a8 8 0 0 0-11.93-.59l-22.9 23a8.06 8.06 0 0 0-.89 10.23c6.86 10.36 17.05 35.1-1.4 72.32A142.85 142.85 0 0 0 364.34 96c-28 0-54 8.54-76.34 22.59l74.67 34.29v78.24h89.09L506.44 288c3.26-12.62 5.56-25.63 5.56-39.31a154 154 0 0 0-50.24-113.94z"/></svg></td></tr>
  </tbody>
  
  
</table>
</div>
```

```{=html}
<div id="zpoyjhlxjt" style="overflow-x:auto;overflow-y:auto;width:auto;height:auto;">
<style>html {
  font-family: -apple-system, BlinkMacSystemFont, 'Segoe UI', Roboto, Oxygen, Ubuntu, Cantarell, 'Helvetica Neue', 'Fira Sans', 'Droid Sans', Arial, sans-serif;
}

#zpoyjhlxjt .gt_table {
  display: table;
  border-collapse: collapse;
  margin-left: auto;
  margin-right: auto;
  color: #333333;
  font-size: 16px;
  font-weight: normal;
  font-style: normal;
  background-color: #FFFFFF;
  width: auto;
  border-top-style: solid;
  border-top-width: 2px;
  border-top-color: #A8A8A8;
  border-right-style: none;
  border-right-width: 2px;
  border-right-color: #D3D3D3;
  border-bottom-style: solid;
  border-bottom-width: 2px;
  border-bottom-color: #A8A8A8;
  border-left-style: none;
  border-left-width: 2px;
  border-left-color: #D3D3D3;
}

#zpoyjhlxjt .gt_heading {
  background-color: #153331;
  text-align: center;
  border-bottom-color: #FFFFFF;
  border-left-style: none;
  border-left-width: 1px;
  border-left-color: #D3D3D3;
  border-right-style: none;
  border-right-width: 1px;
  border-right-color: #D3D3D3;
}

#zpoyjhlxjt .gt_title {
  color: #FFFFFF;
  font-size: 125%;
  font-weight: initial;
  padding-top: 4px;
  padding-bottom: 4px;
  border-bottom-color: #FFFFFF;
  border-bottom-width: 0;
}

#zpoyjhlxjt .gt_subtitle {
  color: #FFFFFF;
  font-size: 85%;
  font-weight: initial;
  padding-top: 0;
  padding-bottom: 6px;
  border-top-color: #FFFFFF;
  border-top-width: 0;
}

#zpoyjhlxjt .gt_bottom_border {
  border-bottom-style: solid;
  border-bottom-width: 2px;
  border-bottom-color: #D3D3D3;
}

#zpoyjhlxjt .gt_col_headings {
  border-top-style: solid;
  border-top-width: 2px;
  border-top-color: #D3D3D3;
  border-bottom-style: solid;
  border-bottom-width: 2px;
  border-bottom-color: #D3D3D3;
  border-left-style: none;
  border-left-width: 1px;
  border-left-color: #D3D3D3;
  border-right-style: none;
  border-right-width: 1px;
  border-right-color: #D3D3D3;
}

#zpoyjhlxjt .gt_col_heading {
  color: #FFFFFF;
  background-color: #1E6E6E;
  font-size: 100%;
  font-weight: normal;
  text-transform: inherit;
  border-left-style: none;
  border-left-width: 1px;
  border-left-color: #D3D3D3;
  border-right-style: none;
  border-right-width: 1px;
  border-right-color: #D3D3D3;
  vertical-align: bottom;
  padding-top: 5px;
  padding-bottom: 6px;
  padding-left: 5px;
  padding-right: 5px;
  overflow-x: hidden;
}

#zpoyjhlxjt .gt_column_spanner_outer {
  color: #FFFFFF;
  background-color: #1E6E6E;
  font-size: 100%;
  font-weight: normal;
  text-transform: inherit;
  padding-top: 0;
  padding-bottom: 0;
  padding-left: 4px;
  padding-right: 4px;
}

#zpoyjhlxjt .gt_column_spanner_outer:first-child {
  padding-left: 0;
}

#zpoyjhlxjt .gt_column_spanner_outer:last-child {
  padding-right: 0;
}

#zpoyjhlxjt .gt_column_spanner {
  border-bottom-style: solid;
  border-bottom-width: 2px;
  border-bottom-color: #D3D3D3;
  vertical-align: bottom;
  padding-top: 5px;
  padding-bottom: 5px;
  overflow-x: hidden;
  display: inline-block;
  width: 100%;
}

#zpoyjhlxjt .gt_group_heading {
  padding: 8px;
  color: #333333;
  background-color: #FFFFFF;
  font-size: 100%;
  font-weight: initial;
  text-transform: inherit;
  border-top-style: solid;
  border-top-width: 2px;
  border-top-color: #D3D3D3;
  border-bottom-style: solid;
  border-bottom-width: 2px;
  border-bottom-color: #D3D3D3;
  border-left-style: none;
  border-left-width: 1px;
  border-left-color: #D3D3D3;
  border-right-style: none;
  border-right-width: 1px;
  border-right-color: #D3D3D3;
  vertical-align: middle;
}

#zpoyjhlxjt .gt_empty_group_heading {
  padding: 0.5px;
  color: #333333;
  background-color: #FFFFFF;
  font-size: 100%;
  font-weight: initial;
  border-top-style: solid;
  border-top-width: 2px;
  border-top-color: #D3D3D3;
  border-bottom-style: solid;
  border-bottom-width: 2px;
  border-bottom-color: #D3D3D3;
  vertical-align: middle;
}

#zpoyjhlxjt .gt_from_md > :first-child {
  margin-top: 0;
}

#zpoyjhlxjt .gt_from_md > :last-child {
  margin-bottom: 0;
}

#zpoyjhlxjt .gt_row {
  padding-top: 8px;
  padding-bottom: 8px;
  padding-left: 5px;
  padding-right: 5px;
  margin: 10px;
  border-top-style: solid;
  border-top-width: 1px;
  border-top-color: #D3D3D3;
  border-left-style: none;
  border-left-width: 1px;
  border-left-color: #D3D3D3;
  border-right-style: none;
  border-right-width: 1px;
  border-right-color: #D3D3D3;
  vertical-align: middle;
  overflow-x: hidden;
}

#zpoyjhlxjt .gt_stub {
  color: #333333;
  background-color: #FFFFFF;
  font-size: 100%;
  font-weight: initial;
  text-transform: inherit;
  border-right-style: solid;
  border-right-width: 2px;
  border-right-color: #D3D3D3;
  padding-left: 12px;
}

#zpoyjhlxjt .gt_summary_row {
  color: #333333;
  background-color: #FFFFFF;
  text-transform: inherit;
  padding-top: 8px;
  padding-bottom: 8px;
  padding-left: 5px;
  padding-right: 5px;
}

#zpoyjhlxjt .gt_first_summary_row {
  padding-top: 8px;
  padding-bottom: 8px;
  padding-left: 5px;
  padding-right: 5px;
  border-top-style: solid;
  border-top-width: 2px;
  border-top-color: #D3D3D3;
}

#zpoyjhlxjt .gt_grand_summary_row {
  color: #333333;
  background-color: #FFFFFF;
  text-transform: inherit;
  padding-top: 8px;
  padding-bottom: 8px;
  padding-left: 5px;
  padding-right: 5px;
}

#zpoyjhlxjt .gt_first_grand_summary_row {
  padding-top: 8px;
  padding-bottom: 8px;
  padding-left: 5px;
  padding-right: 5px;
  border-top-style: double;
  border-top-width: 6px;
  border-top-color: #D3D3D3;
}

#zpoyjhlxjt .gt_striped {
  background-color: rgba(128, 128, 128, 0.05);
}

#zpoyjhlxjt .gt_table_body {
  border-top-style: solid;
  border-top-width: 2px;
  border-top-color: #D3D3D3;
  border-bottom-style: solid;
  border-bottom-width: 2px;
  border-bottom-color: #D3D3D3;
}

#zpoyjhlxjt .gt_footnotes {
  color: #333333;
  background-color: #FFFFFF;
  border-bottom-style: none;
  border-bottom-width: 2px;
  border-bottom-color: #D3D3D3;
  border-left-style: none;
  border-left-width: 2px;
  border-left-color: #D3D3D3;
  border-right-style: none;
  border-right-width: 2px;
  border-right-color: #D3D3D3;
}

#zpoyjhlxjt .gt_footnote {
  margin: 0px;
  font-size: 90%;
  padding: 4px;
}

#zpoyjhlxjt .gt_sourcenotes {
  color: #333333;
  background-color: #FFFFFF;
  border-bottom-style: none;
  border-bottom-width: 2px;
  border-bottom-color: #D3D3D3;
  border-left-style: none;
  border-left-width: 2px;
  border-left-color: #D3D3D3;
  border-right-style: none;
  border-right-width: 2px;
  border-right-color: #D3D3D3;
}

#zpoyjhlxjt .gt_sourcenote {
  font-size: 90%;
  padding: 4px;
}

#zpoyjhlxjt .gt_left {
  text-align: left;
}

#zpoyjhlxjt .gt_center {
  text-align: center;
}

#zpoyjhlxjt .gt_right {
  text-align: right;
  font-variant-numeric: tabular-nums;
}

#zpoyjhlxjt .gt_font_normal {
  font-weight: normal;
}

#zpoyjhlxjt .gt_font_bold {
  font-weight: bold;
}

#zpoyjhlxjt .gt_font_italic {
  font-style: italic;
}

#zpoyjhlxjt .gt_super {
  font-size: 65%;
}

#zpoyjhlxjt .gt_footnote_marks {
  font-style: italic;
  font-weight: normal;
  font-size: 65%;
}
</style>
<table class="gt_table" style="table-layout: fixed;; width: 0px">
  <colgroup>
    <col style="width:350px;"/>
    <col style="width:350px;"/>
  </colgroup>
  <thead class="gt_header">
    <tr>
      <th colspan="2" class="gt_heading gt_title gt_font_normal gt_bottom_border" style>Ingredients</th>
    </tr>
    
  </thead>
  <thead class="gt_col_headings">
    <tr>
      <th class="gt_col_heading gt_columns_bottom_border gt_center" rowspan="1" colspan="1"><strong>Package</strong></th>
      <th class="gt_col_heading gt_columns_bottom_border gt_center" rowspan="1" colspan="1"><strong>Data</strong></th>
    </tr>
  </thead>
  <tbody class="gt_table_body">
    <tr><td class="gt_row gt_center"><div class='gt_from_md'><p>readr<br>dplyr</p>
</div></td>
<td class="gt_row gt_center"><div class='gt_from_md'><p>sample.csv</p>
</div></td></tr>
  </tbody>
  
  
</table>
</div>
```

</br>

**Preparation**

```r
df <- readr::read_csv("C:/data/sample.csv")
```

</br>

**Sample Instructions**

```r
package::function(data, c("column_name1", "column_name2"), as.Date)
```

</br>

**Actual Instructions**

```r
dplyr::mutate_at(df, c("column1", "column2"), as.Date)
```


## Reshaping Data
