



# Preview Data
Reviewing data is an important part of data analysis. There are many different methods to review data within R, however a common practice to review data is to manually visualize the values in columns of a dataframe. This section will explore options for manually exploring data within a dataframe.


## Inspect Data Structure
Prior to performing data analysis it is good to understand the elements, data types, and examples of the data within a dataframe. 


### Preview the structure of a dataframe

```{=html}
<div id="rzufwfhueg" style="overflow-x:auto;overflow-y:auto;width:auto;height:auto;">
<style>html {
  font-family: -apple-system, BlinkMacSystemFont, 'Segoe UI', Roboto, Oxygen, Ubuntu, Cantarell, 'Helvetica Neue', 'Fira Sans', 'Droid Sans', Arial, sans-serif;
}

#rzufwfhueg .gt_table {
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

#rzufwfhueg .gt_heading {
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

#rzufwfhueg .gt_title {
  color: #FFFFFF;
  font-size: 125%;
  font-weight: initial;
  padding-top: 4px;
  padding-bottom: 4px;
  border-bottom-color: #FFFFFF;
  border-bottom-width: 0;
}

#rzufwfhueg .gt_subtitle {
  color: #FFFFFF;
  font-size: 85%;
  font-weight: initial;
  padding-top: 0;
  padding-bottom: 6px;
  border-top-color: #FFFFFF;
  border-top-width: 0;
}

#rzufwfhueg .gt_bottom_border {
  border-bottom-style: solid;
  border-bottom-width: 2px;
  border-bottom-color: #D3D3D3;
}

#rzufwfhueg .gt_col_headings {
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

#rzufwfhueg .gt_col_heading {
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

#rzufwfhueg .gt_column_spanner_outer {
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

#rzufwfhueg .gt_column_spanner_outer:first-child {
  padding-left: 0;
}

#rzufwfhueg .gt_column_spanner_outer:last-child {
  padding-right: 0;
}

#rzufwfhueg .gt_column_spanner {
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

#rzufwfhueg .gt_group_heading {
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

#rzufwfhueg .gt_empty_group_heading {
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

#rzufwfhueg .gt_from_md > :first-child {
  margin-top: 0;
}

#rzufwfhueg .gt_from_md > :last-child {
  margin-bottom: 0;
}

#rzufwfhueg .gt_row {
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

#rzufwfhueg .gt_stub {
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

#rzufwfhueg .gt_summary_row {
  color: #333333;
  background-color: #FFFFFF;
  text-transform: inherit;
  padding-top: 8px;
  padding-bottom: 8px;
  padding-left: 5px;
  padding-right: 5px;
}

#rzufwfhueg .gt_first_summary_row {
  padding-top: 8px;
  padding-bottom: 8px;
  padding-left: 5px;
  padding-right: 5px;
  border-top-style: solid;
  border-top-width: 2px;
  border-top-color: #D3D3D3;
}

#rzufwfhueg .gt_grand_summary_row {
  color: #333333;
  background-color: #FFFFFF;
  text-transform: inherit;
  padding-top: 8px;
  padding-bottom: 8px;
  padding-left: 5px;
  padding-right: 5px;
}

#rzufwfhueg .gt_first_grand_summary_row {
  padding-top: 8px;
  padding-bottom: 8px;
  padding-left: 5px;
  padding-right: 5px;
  border-top-style: double;
  border-top-width: 6px;
  border-top-color: #D3D3D3;
}

#rzufwfhueg .gt_striped {
  background-color: rgba(128, 128, 128, 0.05);
}

#rzufwfhueg .gt_table_body {
  border-top-style: solid;
  border-top-width: 2px;
  border-top-color: #D3D3D3;
  border-bottom-style: solid;
  border-bottom-width: 2px;
  border-bottom-color: #D3D3D3;
}

#rzufwfhueg .gt_footnotes {
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

#rzufwfhueg .gt_footnote {
  margin: 0px;
  font-size: 90%;
  padding: 4px;
}

#rzufwfhueg .gt_sourcenotes {
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

#rzufwfhueg .gt_sourcenote {
  font-size: 90%;
  padding: 4px;
}

#rzufwfhueg .gt_left {
  text-align: left;
}

#rzufwfhueg .gt_center {
  text-align: center;
}

#rzufwfhueg .gt_right {
  text-align: right;
  font-variant-numeric: tabular-nums;
}

#rzufwfhueg .gt_font_normal {
  font-weight: normal;
}

#rzufwfhueg .gt_font_bold {
  font-weight: bold;
}

#rzufwfhueg .gt_font_italic {
  font-style: italic;
}

#rzufwfhueg .gt_super {
  font-size: 65%;
}

#rzufwfhueg .gt_footnote_marks {
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
    <tr><td class="gt_row gt_left">Method to inspect the data structure and elements of a dataframe</td>
<td class="gt_row gt_right"><svg aria-hidden="true" role="img" viewBox="0 0 512 512" style="height:2em;width:2em;vertical-align:-0.125em;margin-left:auto;margin-right:auto;font-size:inherit;fill:#9FC2B9;overflow:visible;position:relative;"><path d="M330.67 263.12V173.4l-52.75-24.22C219.44 218.76 197.58 400 56 400a56 56 0 0 0 0 112c212.64 0 370.65-122.87 419.18-210.34l-37.05-38.54zm131.09-128.37C493.92 74.91 477.18 26.48 458.62 3a8 8 0 0 0-11.93-.59l-22.9 23a8.06 8.06 0 0 0-.89 10.23c6.86 10.36 17.05 35.1-1.4 72.32A142.85 142.85 0 0 0 364.34 96c-28 0-54 8.54-76.34 22.59l74.67 34.29v78.24h89.09L506.44 288c3.26-12.62 5.56-25.63 5.56-39.31a154 154 0 0 0-50.24-113.94z"/></svg><svg aria-hidden="true" role="img" viewBox="0 0 512 512" style="height:2em;width:2em;vertical-align:-0.125em;margin-left:auto;margin-right:auto;font-size:inherit;fill:#9FC2B9;overflow:visible;position:relative;"><path d="M330.67 263.12V173.4l-52.75-24.22C219.44 218.76 197.58 400 56 400a56 56 0 0 0 0 112c212.64 0 370.65-122.87 419.18-210.34l-37.05-38.54zm131.09-128.37C493.92 74.91 477.18 26.48 458.62 3a8 8 0 0 0-11.93-.59l-22.9 23a8.06 8.06 0 0 0-.89 10.23c6.86 10.36 17.05 35.1-1.4 72.32A142.85 142.85 0 0 0 364.34 96c-28 0-54 8.54-76.34 22.59l74.67 34.29v78.24h89.09L506.44 288c3.26-12.62 5.56-25.63 5.56-39.31a154 154 0 0 0-50.24-113.94z"/></svg><svg aria-hidden="true" role="img" viewBox="0 0 512 512" style="height:2em;width:2em;vertical-align:-0.125em;margin-left:auto;margin-right:auto;font-size:inherit;fill:#9FC2B9;overflow:visible;position:relative;"><path d="M330.67 263.12V173.4l-52.75-24.22C219.44 218.76 197.58 400 56 400a56 56 0 0 0 0 112c212.64 0 370.65-122.87 419.18-210.34l-37.05-38.54zm131.09-128.37C493.92 74.91 477.18 26.48 458.62 3a8 8 0 0 0-11.93-.59l-22.9 23a8.06 8.06 0 0 0-.89 10.23c6.86 10.36 17.05 35.1-1.4 72.32A142.85 142.85 0 0 0 364.34 96c-28 0-54 8.54-76.34 22.59l74.67 34.29v78.24h89.09L506.44 288c3.26-12.62 5.56-25.63 5.56-39.31a154 154 0 0 0-50.24-113.94z"/></svg></td></tr>
  </tbody>
  
  
</table>
</div>
```

```{=html}
<div id="elltrvfpjl" style="overflow-x:auto;overflow-y:auto;width:auto;height:auto;">
<style>html {
  font-family: -apple-system, BlinkMacSystemFont, 'Segoe UI', Roboto, Oxygen, Ubuntu, Cantarell, 'Helvetica Neue', 'Fira Sans', 'Droid Sans', Arial, sans-serif;
}

#elltrvfpjl .gt_table {
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

#elltrvfpjl .gt_heading {
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

#elltrvfpjl .gt_title {
  color: #FFFFFF;
  font-size: 125%;
  font-weight: initial;
  padding-top: 4px;
  padding-bottom: 4px;
  border-bottom-color: #FFFFFF;
  border-bottom-width: 0;
}

#elltrvfpjl .gt_subtitle {
  color: #FFFFFF;
  font-size: 85%;
  font-weight: initial;
  padding-top: 0;
  padding-bottom: 6px;
  border-top-color: #FFFFFF;
  border-top-width: 0;
}

#elltrvfpjl .gt_bottom_border {
  border-bottom-style: solid;
  border-bottom-width: 2px;
  border-bottom-color: #D3D3D3;
}

#elltrvfpjl .gt_col_headings {
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

#elltrvfpjl .gt_col_heading {
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

#elltrvfpjl .gt_column_spanner_outer {
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

#elltrvfpjl .gt_column_spanner_outer:first-child {
  padding-left: 0;
}

#elltrvfpjl .gt_column_spanner_outer:last-child {
  padding-right: 0;
}

#elltrvfpjl .gt_column_spanner {
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

#elltrvfpjl .gt_group_heading {
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

#elltrvfpjl .gt_empty_group_heading {
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

#elltrvfpjl .gt_from_md > :first-child {
  margin-top: 0;
}

#elltrvfpjl .gt_from_md > :last-child {
  margin-bottom: 0;
}

#elltrvfpjl .gt_row {
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

#elltrvfpjl .gt_stub {
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

#elltrvfpjl .gt_summary_row {
  color: #333333;
  background-color: #FFFFFF;
  text-transform: inherit;
  padding-top: 8px;
  padding-bottom: 8px;
  padding-left: 5px;
  padding-right: 5px;
}

#elltrvfpjl .gt_first_summary_row {
  padding-top: 8px;
  padding-bottom: 8px;
  padding-left: 5px;
  padding-right: 5px;
  border-top-style: solid;
  border-top-width: 2px;
  border-top-color: #D3D3D3;
}

#elltrvfpjl .gt_grand_summary_row {
  color: #333333;
  background-color: #FFFFFF;
  text-transform: inherit;
  padding-top: 8px;
  padding-bottom: 8px;
  padding-left: 5px;
  padding-right: 5px;
}

#elltrvfpjl .gt_first_grand_summary_row {
  padding-top: 8px;
  padding-bottom: 8px;
  padding-left: 5px;
  padding-right: 5px;
  border-top-style: double;
  border-top-width: 6px;
  border-top-color: #D3D3D3;
}

#elltrvfpjl .gt_striped {
  background-color: rgba(128, 128, 128, 0.05);
}

#elltrvfpjl .gt_table_body {
  border-top-style: solid;
  border-top-width: 2px;
  border-top-color: #D3D3D3;
  border-bottom-style: solid;
  border-bottom-width: 2px;
  border-bottom-color: #D3D3D3;
}

#elltrvfpjl .gt_footnotes {
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

#elltrvfpjl .gt_footnote {
  margin: 0px;
  font-size: 90%;
  padding: 4px;
}

#elltrvfpjl .gt_sourcenotes {
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

#elltrvfpjl .gt_sourcenote {
  font-size: 90%;
  padding: 4px;
}

#elltrvfpjl .gt_left {
  text-align: left;
}

#elltrvfpjl .gt_center {
  text-align: center;
}

#elltrvfpjl .gt_right {
  text-align: right;
  font-variant-numeric: tabular-nums;
}

#elltrvfpjl .gt_font_normal {
  font-weight: normal;
}

#elltrvfpjl .gt_font_bold {
  font-weight: bold;
}

#elltrvfpjl .gt_font_italic {
  font-style: italic;
}

#elltrvfpjl .gt_super {
  font-size: 65%;
}

#elltrvfpjl .gt_footnote_marks {
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
    <tr><td class="gt_row gt_center"><div class='gt_from_md'><p>readr</p>
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
function(data)
```

</br>

**Actual Instructions**

```r
str(df)
```


## Preview Data
Manually reviewing data is a common practice to understand the data in a dataframe. R provides many options for manually reviewing dataframes.


### Subset of rows to preview in a dataframe

```{=html}
<div id="hfirzwzjqz" style="overflow-x:auto;overflow-y:auto;width:auto;height:auto;">
<style>html {
  font-family: -apple-system, BlinkMacSystemFont, 'Segoe UI', Roboto, Oxygen, Ubuntu, Cantarell, 'Helvetica Neue', 'Fira Sans', 'Droid Sans', Arial, sans-serif;
}

#hfirzwzjqz .gt_table {
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

#hfirzwzjqz .gt_heading {
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

#hfirzwzjqz .gt_title {
  color: #FFFFFF;
  font-size: 125%;
  font-weight: initial;
  padding-top: 4px;
  padding-bottom: 4px;
  border-bottom-color: #FFFFFF;
  border-bottom-width: 0;
}

#hfirzwzjqz .gt_subtitle {
  color: #FFFFFF;
  font-size: 85%;
  font-weight: initial;
  padding-top: 0;
  padding-bottom: 6px;
  border-top-color: #FFFFFF;
  border-top-width: 0;
}

#hfirzwzjqz .gt_bottom_border {
  border-bottom-style: solid;
  border-bottom-width: 2px;
  border-bottom-color: #D3D3D3;
}

#hfirzwzjqz .gt_col_headings {
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

#hfirzwzjqz .gt_col_heading {
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

#hfirzwzjqz .gt_column_spanner_outer {
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

#hfirzwzjqz .gt_column_spanner_outer:first-child {
  padding-left: 0;
}

#hfirzwzjqz .gt_column_spanner_outer:last-child {
  padding-right: 0;
}

#hfirzwzjqz .gt_column_spanner {
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

#hfirzwzjqz .gt_group_heading {
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

#hfirzwzjqz .gt_empty_group_heading {
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

#hfirzwzjqz .gt_from_md > :first-child {
  margin-top: 0;
}

#hfirzwzjqz .gt_from_md > :last-child {
  margin-bottom: 0;
}

#hfirzwzjqz .gt_row {
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

#hfirzwzjqz .gt_stub {
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

#hfirzwzjqz .gt_summary_row {
  color: #333333;
  background-color: #FFFFFF;
  text-transform: inherit;
  padding-top: 8px;
  padding-bottom: 8px;
  padding-left: 5px;
  padding-right: 5px;
}

#hfirzwzjqz .gt_first_summary_row {
  padding-top: 8px;
  padding-bottom: 8px;
  padding-left: 5px;
  padding-right: 5px;
  border-top-style: solid;
  border-top-width: 2px;
  border-top-color: #D3D3D3;
}

#hfirzwzjqz .gt_grand_summary_row {
  color: #333333;
  background-color: #FFFFFF;
  text-transform: inherit;
  padding-top: 8px;
  padding-bottom: 8px;
  padding-left: 5px;
  padding-right: 5px;
}

#hfirzwzjqz .gt_first_grand_summary_row {
  padding-top: 8px;
  padding-bottom: 8px;
  padding-left: 5px;
  padding-right: 5px;
  border-top-style: double;
  border-top-width: 6px;
  border-top-color: #D3D3D3;
}

#hfirzwzjqz .gt_striped {
  background-color: rgba(128, 128, 128, 0.05);
}

#hfirzwzjqz .gt_table_body {
  border-top-style: solid;
  border-top-width: 2px;
  border-top-color: #D3D3D3;
  border-bottom-style: solid;
  border-bottom-width: 2px;
  border-bottom-color: #D3D3D3;
}

#hfirzwzjqz .gt_footnotes {
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

#hfirzwzjqz .gt_footnote {
  margin: 0px;
  font-size: 90%;
  padding: 4px;
}

#hfirzwzjqz .gt_sourcenotes {
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

#hfirzwzjqz .gt_sourcenote {
  font-size: 90%;
  padding: 4px;
}

#hfirzwzjqz .gt_left {
  text-align: left;
}

#hfirzwzjqz .gt_center {
  text-align: center;
}

#hfirzwzjqz .gt_right {
  text-align: right;
  font-variant-numeric: tabular-nums;
}

#hfirzwzjqz .gt_font_normal {
  font-weight: normal;
}

#hfirzwzjqz .gt_font_bold {
  font-weight: bold;
}

#hfirzwzjqz .gt_font_italic {
  font-style: italic;
}

#hfirzwzjqz .gt_super {
  font-size: 65%;
}

#hfirzwzjqz .gt_footnote_marks {
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
    <tr><td class="gt_row gt_left">Method to visually inspect the first few rows of a dataframe</td>
<td class="gt_row gt_right"><svg aria-hidden="true" role="img" viewBox="0 0 512 512" style="height:2em;width:2em;vertical-align:-0.125em;margin-left:auto;margin-right:auto;font-size:inherit;fill:#9FC2B9;overflow:visible;position:relative;"><path d="M330.67 263.12V173.4l-52.75-24.22C219.44 218.76 197.58 400 56 400a56 56 0 0 0 0 112c212.64 0 370.65-122.87 419.18-210.34l-37.05-38.54zm131.09-128.37C493.92 74.91 477.18 26.48 458.62 3a8 8 0 0 0-11.93-.59l-22.9 23a8.06 8.06 0 0 0-.89 10.23c6.86 10.36 17.05 35.1-1.4 72.32A142.85 142.85 0 0 0 364.34 96c-28 0-54 8.54-76.34 22.59l74.67 34.29v78.24h89.09L506.44 288c3.26-12.62 5.56-25.63 5.56-39.31a154 154 0 0 0-50.24-113.94z"/></svg><svg aria-hidden="true" role="img" viewBox="0 0 512 512" style="height:2em;width:2em;vertical-align:-0.125em;margin-left:auto;margin-right:auto;font-size:inherit;fill:#9FC2B9;overflow:visible;position:relative;"><path d="M330.67 263.12V173.4l-52.75-24.22C219.44 218.76 197.58 400 56 400a56 56 0 0 0 0 112c212.64 0 370.65-122.87 419.18-210.34l-37.05-38.54zm131.09-128.37C493.92 74.91 477.18 26.48 458.62 3a8 8 0 0 0-11.93-.59l-22.9 23a8.06 8.06 0 0 0-.89 10.23c6.86 10.36 17.05 35.1-1.4 72.32A142.85 142.85 0 0 0 364.34 96c-28 0-54 8.54-76.34 22.59l74.67 34.29v78.24h89.09L506.44 288c3.26-12.62 5.56-25.63 5.56-39.31a154 154 0 0 0-50.24-113.94z"/></svg><svg aria-hidden="true" role="img" viewBox="0 0 512 512" style="height:2em;width:2em;vertical-align:-0.125em;margin-left:auto;margin-right:auto;font-size:inherit;fill:#9FC2B9;overflow:visible;position:relative;"><path d="M330.67 263.12V173.4l-52.75-24.22C219.44 218.76 197.58 400 56 400a56 56 0 0 0 0 112c212.64 0 370.65-122.87 419.18-210.34l-37.05-38.54zm131.09-128.37C493.92 74.91 477.18 26.48 458.62 3a8 8 0 0 0-11.93-.59l-22.9 23a8.06 8.06 0 0 0-.89 10.23c6.86 10.36 17.05 35.1-1.4 72.32A142.85 142.85 0 0 0 364.34 96c-28 0-54 8.54-76.34 22.59l74.67 34.29v78.24h89.09L506.44 288c3.26-12.62 5.56-25.63 5.56-39.31a154 154 0 0 0-50.24-113.94z"/></svg></td></tr>
  </tbody>
  
  
</table>
</div>
```

```{=html}
<div id="jsakvuhkha" style="overflow-x:auto;overflow-y:auto;width:auto;height:auto;">
<style>html {
  font-family: -apple-system, BlinkMacSystemFont, 'Segoe UI', Roboto, Oxygen, Ubuntu, Cantarell, 'Helvetica Neue', 'Fira Sans', 'Droid Sans', Arial, sans-serif;
}

#jsakvuhkha .gt_table {
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

#jsakvuhkha .gt_heading {
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

#jsakvuhkha .gt_title {
  color: #FFFFFF;
  font-size: 125%;
  font-weight: initial;
  padding-top: 4px;
  padding-bottom: 4px;
  border-bottom-color: #FFFFFF;
  border-bottom-width: 0;
}

#jsakvuhkha .gt_subtitle {
  color: #FFFFFF;
  font-size: 85%;
  font-weight: initial;
  padding-top: 0;
  padding-bottom: 6px;
  border-top-color: #FFFFFF;
  border-top-width: 0;
}

#jsakvuhkha .gt_bottom_border {
  border-bottom-style: solid;
  border-bottom-width: 2px;
  border-bottom-color: #D3D3D3;
}

#jsakvuhkha .gt_col_headings {
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

#jsakvuhkha .gt_col_heading {
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

#jsakvuhkha .gt_column_spanner_outer {
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

#jsakvuhkha .gt_column_spanner_outer:first-child {
  padding-left: 0;
}

#jsakvuhkha .gt_column_spanner_outer:last-child {
  padding-right: 0;
}

#jsakvuhkha .gt_column_spanner {
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

#jsakvuhkha .gt_group_heading {
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

#jsakvuhkha .gt_empty_group_heading {
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

#jsakvuhkha .gt_from_md > :first-child {
  margin-top: 0;
}

#jsakvuhkha .gt_from_md > :last-child {
  margin-bottom: 0;
}

#jsakvuhkha .gt_row {
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

#jsakvuhkha .gt_stub {
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

#jsakvuhkha .gt_summary_row {
  color: #333333;
  background-color: #FFFFFF;
  text-transform: inherit;
  padding-top: 8px;
  padding-bottom: 8px;
  padding-left: 5px;
  padding-right: 5px;
}

#jsakvuhkha .gt_first_summary_row {
  padding-top: 8px;
  padding-bottom: 8px;
  padding-left: 5px;
  padding-right: 5px;
  border-top-style: solid;
  border-top-width: 2px;
  border-top-color: #D3D3D3;
}

#jsakvuhkha .gt_grand_summary_row {
  color: #333333;
  background-color: #FFFFFF;
  text-transform: inherit;
  padding-top: 8px;
  padding-bottom: 8px;
  padding-left: 5px;
  padding-right: 5px;
}

#jsakvuhkha .gt_first_grand_summary_row {
  padding-top: 8px;
  padding-bottom: 8px;
  padding-left: 5px;
  padding-right: 5px;
  border-top-style: double;
  border-top-width: 6px;
  border-top-color: #D3D3D3;
}

#jsakvuhkha .gt_striped {
  background-color: rgba(128, 128, 128, 0.05);
}

#jsakvuhkha .gt_table_body {
  border-top-style: solid;
  border-top-width: 2px;
  border-top-color: #D3D3D3;
  border-bottom-style: solid;
  border-bottom-width: 2px;
  border-bottom-color: #D3D3D3;
}

#jsakvuhkha .gt_footnotes {
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

#jsakvuhkha .gt_footnote {
  margin: 0px;
  font-size: 90%;
  padding: 4px;
}

#jsakvuhkha .gt_sourcenotes {
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

#jsakvuhkha .gt_sourcenote {
  font-size: 90%;
  padding: 4px;
}

#jsakvuhkha .gt_left {
  text-align: left;
}

#jsakvuhkha .gt_center {
  text-align: center;
}

#jsakvuhkha .gt_right {
  text-align: right;
  font-variant-numeric: tabular-nums;
}

#jsakvuhkha .gt_font_normal {
  font-weight: normal;
}

#jsakvuhkha .gt_font_bold {
  font-weight: bold;
}

#jsakvuhkha .gt_font_italic {
  font-style: italic;
}

#jsakvuhkha .gt_super {
  font-size: 65%;
}

#jsakvuhkha .gt_footnote_marks {
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
    <tr><td class="gt_row gt_center"><div class='gt_from_md'><p>readr</p>
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
function(data)
```

</br>

**Actual Instructions**

```r
head(df)
```

### Specify a set number of rows to preview in a dataframe

```{=html}
<div id="qacmzwcvth" style="overflow-x:auto;overflow-y:auto;width:auto;height:auto;">
<style>html {
  font-family: -apple-system, BlinkMacSystemFont, 'Segoe UI', Roboto, Oxygen, Ubuntu, Cantarell, 'Helvetica Neue', 'Fira Sans', 'Droid Sans', Arial, sans-serif;
}

#qacmzwcvth .gt_table {
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

#qacmzwcvth .gt_heading {
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

#qacmzwcvth .gt_title {
  color: #FFFFFF;
  font-size: 125%;
  font-weight: initial;
  padding-top: 4px;
  padding-bottom: 4px;
  border-bottom-color: #FFFFFF;
  border-bottom-width: 0;
}

#qacmzwcvth .gt_subtitle {
  color: #FFFFFF;
  font-size: 85%;
  font-weight: initial;
  padding-top: 0;
  padding-bottom: 6px;
  border-top-color: #FFFFFF;
  border-top-width: 0;
}

#qacmzwcvth .gt_bottom_border {
  border-bottom-style: solid;
  border-bottom-width: 2px;
  border-bottom-color: #D3D3D3;
}

#qacmzwcvth .gt_col_headings {
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

#qacmzwcvth .gt_col_heading {
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

#qacmzwcvth .gt_column_spanner_outer {
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

#qacmzwcvth .gt_column_spanner_outer:first-child {
  padding-left: 0;
}

#qacmzwcvth .gt_column_spanner_outer:last-child {
  padding-right: 0;
}

#qacmzwcvth .gt_column_spanner {
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

#qacmzwcvth .gt_group_heading {
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

#qacmzwcvth .gt_empty_group_heading {
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

#qacmzwcvth .gt_from_md > :first-child {
  margin-top: 0;
}

#qacmzwcvth .gt_from_md > :last-child {
  margin-bottom: 0;
}

#qacmzwcvth .gt_row {
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

#qacmzwcvth .gt_stub {
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

#qacmzwcvth .gt_summary_row {
  color: #333333;
  background-color: #FFFFFF;
  text-transform: inherit;
  padding-top: 8px;
  padding-bottom: 8px;
  padding-left: 5px;
  padding-right: 5px;
}

#qacmzwcvth .gt_first_summary_row {
  padding-top: 8px;
  padding-bottom: 8px;
  padding-left: 5px;
  padding-right: 5px;
  border-top-style: solid;
  border-top-width: 2px;
  border-top-color: #D3D3D3;
}

#qacmzwcvth .gt_grand_summary_row {
  color: #333333;
  background-color: #FFFFFF;
  text-transform: inherit;
  padding-top: 8px;
  padding-bottom: 8px;
  padding-left: 5px;
  padding-right: 5px;
}

#qacmzwcvth .gt_first_grand_summary_row {
  padding-top: 8px;
  padding-bottom: 8px;
  padding-left: 5px;
  padding-right: 5px;
  border-top-style: double;
  border-top-width: 6px;
  border-top-color: #D3D3D3;
}

#qacmzwcvth .gt_striped {
  background-color: rgba(128, 128, 128, 0.05);
}

#qacmzwcvth .gt_table_body {
  border-top-style: solid;
  border-top-width: 2px;
  border-top-color: #D3D3D3;
  border-bottom-style: solid;
  border-bottom-width: 2px;
  border-bottom-color: #D3D3D3;
}

#qacmzwcvth .gt_footnotes {
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

#qacmzwcvth .gt_footnote {
  margin: 0px;
  font-size: 90%;
  padding: 4px;
}

#qacmzwcvth .gt_sourcenotes {
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

#qacmzwcvth .gt_sourcenote {
  font-size: 90%;
  padding: 4px;
}

#qacmzwcvth .gt_left {
  text-align: left;
}

#qacmzwcvth .gt_center {
  text-align: center;
}

#qacmzwcvth .gt_right {
  text-align: right;
  font-variant-numeric: tabular-nums;
}

#qacmzwcvth .gt_font_normal {
  font-weight: normal;
}

#qacmzwcvth .gt_font_bold {
  font-weight: bold;
}

#qacmzwcvth .gt_font_italic {
  font-style: italic;
}

#qacmzwcvth .gt_super {
  font-size: 65%;
}

#qacmzwcvth .gt_footnote_marks {
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
    <tr><td class="gt_row gt_left">Method to visually inspect a specific number of rows of a dataframe</td>
<td class="gt_row gt_right"><svg aria-hidden="true" role="img" viewBox="0 0 512 512" style="height:2em;width:2em;vertical-align:-0.125em;margin-left:auto;margin-right:auto;font-size:inherit;fill:#9FC2B9;overflow:visible;position:relative;"><path d="M330.67 263.12V173.4l-52.75-24.22C219.44 218.76 197.58 400 56 400a56 56 0 0 0 0 112c212.64 0 370.65-122.87 419.18-210.34l-37.05-38.54zm131.09-128.37C493.92 74.91 477.18 26.48 458.62 3a8 8 0 0 0-11.93-.59l-22.9 23a8.06 8.06 0 0 0-.89 10.23c6.86 10.36 17.05 35.1-1.4 72.32A142.85 142.85 0 0 0 364.34 96c-28 0-54 8.54-76.34 22.59l74.67 34.29v78.24h89.09L506.44 288c3.26-12.62 5.56-25.63 5.56-39.31a154 154 0 0 0-50.24-113.94z"/></svg><svg aria-hidden="true" role="img" viewBox="0 0 512 512" style="height:2em;width:2em;vertical-align:-0.125em;margin-left:auto;margin-right:auto;font-size:inherit;fill:#9FC2B9;overflow:visible;position:relative;"><path d="M330.67 263.12V173.4l-52.75-24.22C219.44 218.76 197.58 400 56 400a56 56 0 0 0 0 112c212.64 0 370.65-122.87 419.18-210.34l-37.05-38.54zm131.09-128.37C493.92 74.91 477.18 26.48 458.62 3a8 8 0 0 0-11.93-.59l-22.9 23a8.06 8.06 0 0 0-.89 10.23c6.86 10.36 17.05 35.1-1.4 72.32A142.85 142.85 0 0 0 364.34 96c-28 0-54 8.54-76.34 22.59l74.67 34.29v78.24h89.09L506.44 288c3.26-12.62 5.56-25.63 5.56-39.31a154 154 0 0 0-50.24-113.94z"/></svg><svg aria-hidden="true" role="img" viewBox="0 0 512 512" style="height:2em;width:2em;vertical-align:-0.125em;margin-left:auto;margin-right:auto;font-size:inherit;fill:#9FC2B9;overflow:visible;position:relative;"><path d="M330.67 263.12V173.4l-52.75-24.22C219.44 218.76 197.58 400 56 400a56 56 0 0 0 0 112c212.64 0 370.65-122.87 419.18-210.34l-37.05-38.54zm131.09-128.37C493.92 74.91 477.18 26.48 458.62 3a8 8 0 0 0-11.93-.59l-22.9 23a8.06 8.06 0 0 0-.89 10.23c6.86 10.36 17.05 35.1-1.4 72.32A142.85 142.85 0 0 0 364.34 96c-28 0-54 8.54-76.34 22.59l74.67 34.29v78.24h89.09L506.44 288c3.26-12.62 5.56-25.63 5.56-39.31a154 154 0 0 0-50.24-113.94z"/></svg></td></tr>
  </tbody>
  
  
</table>
</div>
```

```{=html}
<div id="mgjbhbplwj" style="overflow-x:auto;overflow-y:auto;width:auto;height:auto;">
<style>html {
  font-family: -apple-system, BlinkMacSystemFont, 'Segoe UI', Roboto, Oxygen, Ubuntu, Cantarell, 'Helvetica Neue', 'Fira Sans', 'Droid Sans', Arial, sans-serif;
}

#mgjbhbplwj .gt_table {
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

#mgjbhbplwj .gt_heading {
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

#mgjbhbplwj .gt_title {
  color: #FFFFFF;
  font-size: 125%;
  font-weight: initial;
  padding-top: 4px;
  padding-bottom: 4px;
  border-bottom-color: #FFFFFF;
  border-bottom-width: 0;
}

#mgjbhbplwj .gt_subtitle {
  color: #FFFFFF;
  font-size: 85%;
  font-weight: initial;
  padding-top: 0;
  padding-bottom: 6px;
  border-top-color: #FFFFFF;
  border-top-width: 0;
}

#mgjbhbplwj .gt_bottom_border {
  border-bottom-style: solid;
  border-bottom-width: 2px;
  border-bottom-color: #D3D3D3;
}

#mgjbhbplwj .gt_col_headings {
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

#mgjbhbplwj .gt_col_heading {
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

#mgjbhbplwj .gt_column_spanner_outer {
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

#mgjbhbplwj .gt_column_spanner_outer:first-child {
  padding-left: 0;
}

#mgjbhbplwj .gt_column_spanner_outer:last-child {
  padding-right: 0;
}

#mgjbhbplwj .gt_column_spanner {
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

#mgjbhbplwj .gt_group_heading {
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

#mgjbhbplwj .gt_empty_group_heading {
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

#mgjbhbplwj .gt_from_md > :first-child {
  margin-top: 0;
}

#mgjbhbplwj .gt_from_md > :last-child {
  margin-bottom: 0;
}

#mgjbhbplwj .gt_row {
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

#mgjbhbplwj .gt_stub {
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

#mgjbhbplwj .gt_summary_row {
  color: #333333;
  background-color: #FFFFFF;
  text-transform: inherit;
  padding-top: 8px;
  padding-bottom: 8px;
  padding-left: 5px;
  padding-right: 5px;
}

#mgjbhbplwj .gt_first_summary_row {
  padding-top: 8px;
  padding-bottom: 8px;
  padding-left: 5px;
  padding-right: 5px;
  border-top-style: solid;
  border-top-width: 2px;
  border-top-color: #D3D3D3;
}

#mgjbhbplwj .gt_grand_summary_row {
  color: #333333;
  background-color: #FFFFFF;
  text-transform: inherit;
  padding-top: 8px;
  padding-bottom: 8px;
  padding-left: 5px;
  padding-right: 5px;
}

#mgjbhbplwj .gt_first_grand_summary_row {
  padding-top: 8px;
  padding-bottom: 8px;
  padding-left: 5px;
  padding-right: 5px;
  border-top-style: double;
  border-top-width: 6px;
  border-top-color: #D3D3D3;
}

#mgjbhbplwj .gt_striped {
  background-color: rgba(128, 128, 128, 0.05);
}

#mgjbhbplwj .gt_table_body {
  border-top-style: solid;
  border-top-width: 2px;
  border-top-color: #D3D3D3;
  border-bottom-style: solid;
  border-bottom-width: 2px;
  border-bottom-color: #D3D3D3;
}

#mgjbhbplwj .gt_footnotes {
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

#mgjbhbplwj .gt_footnote {
  margin: 0px;
  font-size: 90%;
  padding: 4px;
}

#mgjbhbplwj .gt_sourcenotes {
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

#mgjbhbplwj .gt_sourcenote {
  font-size: 90%;
  padding: 4px;
}

#mgjbhbplwj .gt_left {
  text-align: left;
}

#mgjbhbplwj .gt_center {
  text-align: center;
}

#mgjbhbplwj .gt_right {
  text-align: right;
  font-variant-numeric: tabular-nums;
}

#mgjbhbplwj .gt_font_normal {
  font-weight: normal;
}

#mgjbhbplwj .gt_font_bold {
  font-weight: bold;
}

#mgjbhbplwj .gt_font_italic {
  font-style: italic;
}

#mgjbhbplwj .gt_super {
  font-size: 65%;
}

#mgjbhbplwj .gt_footnote_marks {
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
    <tr><td class="gt_row gt_center"><div class='gt_from_md'><p>readr</p>
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
function(data, number)
```

</br>

**Actual Instructions**

```r
head(df, 100)
```

### Preview all rows of a dataframe

```{=html}
<div id="meszeqhzhe" style="overflow-x:auto;overflow-y:auto;width:auto;height:auto;">
<style>html {
  font-family: -apple-system, BlinkMacSystemFont, 'Segoe UI', Roboto, Oxygen, Ubuntu, Cantarell, 'Helvetica Neue', 'Fira Sans', 'Droid Sans', Arial, sans-serif;
}

#meszeqhzhe .gt_table {
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

#meszeqhzhe .gt_heading {
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

#meszeqhzhe .gt_title {
  color: #FFFFFF;
  font-size: 125%;
  font-weight: initial;
  padding-top: 4px;
  padding-bottom: 4px;
  border-bottom-color: #FFFFFF;
  border-bottom-width: 0;
}

#meszeqhzhe .gt_subtitle {
  color: #FFFFFF;
  font-size: 85%;
  font-weight: initial;
  padding-top: 0;
  padding-bottom: 6px;
  border-top-color: #FFFFFF;
  border-top-width: 0;
}

#meszeqhzhe .gt_bottom_border {
  border-bottom-style: solid;
  border-bottom-width: 2px;
  border-bottom-color: #D3D3D3;
}

#meszeqhzhe .gt_col_headings {
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

#meszeqhzhe .gt_col_heading {
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

#meszeqhzhe .gt_column_spanner_outer {
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

#meszeqhzhe .gt_column_spanner_outer:first-child {
  padding-left: 0;
}

#meszeqhzhe .gt_column_spanner_outer:last-child {
  padding-right: 0;
}

#meszeqhzhe .gt_column_spanner {
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

#meszeqhzhe .gt_group_heading {
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

#meszeqhzhe .gt_empty_group_heading {
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

#meszeqhzhe .gt_from_md > :first-child {
  margin-top: 0;
}

#meszeqhzhe .gt_from_md > :last-child {
  margin-bottom: 0;
}

#meszeqhzhe .gt_row {
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

#meszeqhzhe .gt_stub {
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

#meszeqhzhe .gt_summary_row {
  color: #333333;
  background-color: #FFFFFF;
  text-transform: inherit;
  padding-top: 8px;
  padding-bottom: 8px;
  padding-left: 5px;
  padding-right: 5px;
}

#meszeqhzhe .gt_first_summary_row {
  padding-top: 8px;
  padding-bottom: 8px;
  padding-left: 5px;
  padding-right: 5px;
  border-top-style: solid;
  border-top-width: 2px;
  border-top-color: #D3D3D3;
}

#meszeqhzhe .gt_grand_summary_row {
  color: #333333;
  background-color: #FFFFFF;
  text-transform: inherit;
  padding-top: 8px;
  padding-bottom: 8px;
  padding-left: 5px;
  padding-right: 5px;
}

#meszeqhzhe .gt_first_grand_summary_row {
  padding-top: 8px;
  padding-bottom: 8px;
  padding-left: 5px;
  padding-right: 5px;
  border-top-style: double;
  border-top-width: 6px;
  border-top-color: #D3D3D3;
}

#meszeqhzhe .gt_striped {
  background-color: rgba(128, 128, 128, 0.05);
}

#meszeqhzhe .gt_table_body {
  border-top-style: solid;
  border-top-width: 2px;
  border-top-color: #D3D3D3;
  border-bottom-style: solid;
  border-bottom-width: 2px;
  border-bottom-color: #D3D3D3;
}

#meszeqhzhe .gt_footnotes {
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

#meszeqhzhe .gt_footnote {
  margin: 0px;
  font-size: 90%;
  padding: 4px;
}

#meszeqhzhe .gt_sourcenotes {
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

#meszeqhzhe .gt_sourcenote {
  font-size: 90%;
  padding: 4px;
}

#meszeqhzhe .gt_left {
  text-align: left;
}

#meszeqhzhe .gt_center {
  text-align: center;
}

#meszeqhzhe .gt_right {
  text-align: right;
  font-variant-numeric: tabular-nums;
}

#meszeqhzhe .gt_font_normal {
  font-weight: normal;
}

#meszeqhzhe .gt_font_bold {
  font-weight: bold;
}

#meszeqhzhe .gt_font_italic {
  font-style: italic;
}

#meszeqhzhe .gt_super {
  font-size: 65%;
}

#meszeqhzhe .gt_footnote_marks {
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
    <tr><td class="gt_row gt_left">Method to visually inspect all rows of a dataframe</td>
<td class="gt_row gt_right"><svg aria-hidden="true" role="img" viewBox="0 0 512 512" style="height:2em;width:2em;vertical-align:-0.125em;margin-left:auto;margin-right:auto;font-size:inherit;fill:#9FC2B9;overflow:visible;position:relative;"><path d="M330.67 263.12V173.4l-52.75-24.22C219.44 218.76 197.58 400 56 400a56 56 0 0 0 0 112c212.64 0 370.65-122.87 419.18-210.34l-37.05-38.54zm131.09-128.37C493.92 74.91 477.18 26.48 458.62 3a8 8 0 0 0-11.93-.59l-22.9 23a8.06 8.06 0 0 0-.89 10.23c6.86 10.36 17.05 35.1-1.4 72.32A142.85 142.85 0 0 0 364.34 96c-28 0-54 8.54-76.34 22.59l74.67 34.29v78.24h89.09L506.44 288c3.26-12.62 5.56-25.63 5.56-39.31a154 154 0 0 0-50.24-113.94z"/></svg><svg aria-hidden="true" role="img" viewBox="0 0 512 512" style="height:2em;width:2em;vertical-align:-0.125em;margin-left:auto;margin-right:auto;font-size:inherit;fill:#9FC2B9;overflow:visible;position:relative;"><path d="M330.67 263.12V173.4l-52.75-24.22C219.44 218.76 197.58 400 56 400a56 56 0 0 0 0 112c212.64 0 370.65-122.87 419.18-210.34l-37.05-38.54zm131.09-128.37C493.92 74.91 477.18 26.48 458.62 3a8 8 0 0 0-11.93-.59l-22.9 23a8.06 8.06 0 0 0-.89 10.23c6.86 10.36 17.05 35.1-1.4 72.32A142.85 142.85 0 0 0 364.34 96c-28 0-54 8.54-76.34 22.59l74.67 34.29v78.24h89.09L506.44 288c3.26-12.62 5.56-25.63 5.56-39.31a154 154 0 0 0-50.24-113.94z"/></svg><svg aria-hidden="true" role="img" viewBox="0 0 512 512" style="height:2em;width:2em;vertical-align:-0.125em;margin-left:auto;margin-right:auto;font-size:inherit;fill:#9FC2B9;overflow:visible;position:relative;"><path d="M330.67 263.12V173.4l-52.75-24.22C219.44 218.76 197.58 400 56 400a56 56 0 0 0 0 112c212.64 0 370.65-122.87 419.18-210.34l-37.05-38.54zm131.09-128.37C493.92 74.91 477.18 26.48 458.62 3a8 8 0 0 0-11.93-.59l-22.9 23a8.06 8.06 0 0 0-.89 10.23c6.86 10.36 17.05 35.1-1.4 72.32A142.85 142.85 0 0 0 364.34 96c-28 0-54 8.54-76.34 22.59l74.67 34.29v78.24h89.09L506.44 288c3.26-12.62 5.56-25.63 5.56-39.31a154 154 0 0 0-50.24-113.94z"/></svg></td></tr>
  </tbody>
  
  
</table>
</div>
```

```{=html}
<div id="ioteafykmm" style="overflow-x:auto;overflow-y:auto;width:auto;height:auto;">
<style>html {
  font-family: -apple-system, BlinkMacSystemFont, 'Segoe UI', Roboto, Oxygen, Ubuntu, Cantarell, 'Helvetica Neue', 'Fira Sans', 'Droid Sans', Arial, sans-serif;
}

#ioteafykmm .gt_table {
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

#ioteafykmm .gt_heading {
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

#ioteafykmm .gt_title {
  color: #FFFFFF;
  font-size: 125%;
  font-weight: initial;
  padding-top: 4px;
  padding-bottom: 4px;
  border-bottom-color: #FFFFFF;
  border-bottom-width: 0;
}

#ioteafykmm .gt_subtitle {
  color: #FFFFFF;
  font-size: 85%;
  font-weight: initial;
  padding-top: 0;
  padding-bottom: 6px;
  border-top-color: #FFFFFF;
  border-top-width: 0;
}

#ioteafykmm .gt_bottom_border {
  border-bottom-style: solid;
  border-bottom-width: 2px;
  border-bottom-color: #D3D3D3;
}

#ioteafykmm .gt_col_headings {
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

#ioteafykmm .gt_col_heading {
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

#ioteafykmm .gt_column_spanner_outer {
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

#ioteafykmm .gt_column_spanner_outer:first-child {
  padding-left: 0;
}

#ioteafykmm .gt_column_spanner_outer:last-child {
  padding-right: 0;
}

#ioteafykmm .gt_column_spanner {
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

#ioteafykmm .gt_group_heading {
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

#ioteafykmm .gt_empty_group_heading {
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

#ioteafykmm .gt_from_md > :first-child {
  margin-top: 0;
}

#ioteafykmm .gt_from_md > :last-child {
  margin-bottom: 0;
}

#ioteafykmm .gt_row {
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

#ioteafykmm .gt_stub {
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

#ioteafykmm .gt_summary_row {
  color: #333333;
  background-color: #FFFFFF;
  text-transform: inherit;
  padding-top: 8px;
  padding-bottom: 8px;
  padding-left: 5px;
  padding-right: 5px;
}

#ioteafykmm .gt_first_summary_row {
  padding-top: 8px;
  padding-bottom: 8px;
  padding-left: 5px;
  padding-right: 5px;
  border-top-style: solid;
  border-top-width: 2px;
  border-top-color: #D3D3D3;
}

#ioteafykmm .gt_grand_summary_row {
  color: #333333;
  background-color: #FFFFFF;
  text-transform: inherit;
  padding-top: 8px;
  padding-bottom: 8px;
  padding-left: 5px;
  padding-right: 5px;
}

#ioteafykmm .gt_first_grand_summary_row {
  padding-top: 8px;
  padding-bottom: 8px;
  padding-left: 5px;
  padding-right: 5px;
  border-top-style: double;
  border-top-width: 6px;
  border-top-color: #D3D3D3;
}

#ioteafykmm .gt_striped {
  background-color: rgba(128, 128, 128, 0.05);
}

#ioteafykmm .gt_table_body {
  border-top-style: solid;
  border-top-width: 2px;
  border-top-color: #D3D3D3;
  border-bottom-style: solid;
  border-bottom-width: 2px;
  border-bottom-color: #D3D3D3;
}

#ioteafykmm .gt_footnotes {
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

#ioteafykmm .gt_footnote {
  margin: 0px;
  font-size: 90%;
  padding: 4px;
}

#ioteafykmm .gt_sourcenotes {
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

#ioteafykmm .gt_sourcenote {
  font-size: 90%;
  padding: 4px;
}

#ioteafykmm .gt_left {
  text-align: left;
}

#ioteafykmm .gt_center {
  text-align: center;
}

#ioteafykmm .gt_right {
  text-align: right;
  font-variant-numeric: tabular-nums;
}

#ioteafykmm .gt_font_normal {
  font-weight: normal;
}

#ioteafykmm .gt_font_bold {
  font-weight: bold;
}

#ioteafykmm .gt_font_italic {
  font-style: italic;
}

#ioteafykmm .gt_super {
  font-size: 65%;
}

#ioteafykmm .gt_footnote_marks {
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
    <tr><td class="gt_row gt_center"><div class='gt_from_md'><p>readr</p>
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
data
```

</br>

**Actual Instructions**

```r
df
```

### Preview all rows of a dataframe within a viewer

```{=html}
<div id="zumuvrowdg" style="overflow-x:auto;overflow-y:auto;width:auto;height:auto;">
<style>html {
  font-family: -apple-system, BlinkMacSystemFont, 'Segoe UI', Roboto, Oxygen, Ubuntu, Cantarell, 'Helvetica Neue', 'Fira Sans', 'Droid Sans', Arial, sans-serif;
}

#zumuvrowdg .gt_table {
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

#zumuvrowdg .gt_heading {
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

#zumuvrowdg .gt_title {
  color: #FFFFFF;
  font-size: 125%;
  font-weight: initial;
  padding-top: 4px;
  padding-bottom: 4px;
  border-bottom-color: #FFFFFF;
  border-bottom-width: 0;
}

#zumuvrowdg .gt_subtitle {
  color: #FFFFFF;
  font-size: 85%;
  font-weight: initial;
  padding-top: 0;
  padding-bottom: 6px;
  border-top-color: #FFFFFF;
  border-top-width: 0;
}

#zumuvrowdg .gt_bottom_border {
  border-bottom-style: solid;
  border-bottom-width: 2px;
  border-bottom-color: #D3D3D3;
}

#zumuvrowdg .gt_col_headings {
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

#zumuvrowdg .gt_col_heading {
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

#zumuvrowdg .gt_column_spanner_outer {
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

#zumuvrowdg .gt_column_spanner_outer:first-child {
  padding-left: 0;
}

#zumuvrowdg .gt_column_spanner_outer:last-child {
  padding-right: 0;
}

#zumuvrowdg .gt_column_spanner {
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

#zumuvrowdg .gt_group_heading {
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

#zumuvrowdg .gt_empty_group_heading {
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

#zumuvrowdg .gt_from_md > :first-child {
  margin-top: 0;
}

#zumuvrowdg .gt_from_md > :last-child {
  margin-bottom: 0;
}

#zumuvrowdg .gt_row {
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

#zumuvrowdg .gt_stub {
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

#zumuvrowdg .gt_summary_row {
  color: #333333;
  background-color: #FFFFFF;
  text-transform: inherit;
  padding-top: 8px;
  padding-bottom: 8px;
  padding-left: 5px;
  padding-right: 5px;
}

#zumuvrowdg .gt_first_summary_row {
  padding-top: 8px;
  padding-bottom: 8px;
  padding-left: 5px;
  padding-right: 5px;
  border-top-style: solid;
  border-top-width: 2px;
  border-top-color: #D3D3D3;
}

#zumuvrowdg .gt_grand_summary_row {
  color: #333333;
  background-color: #FFFFFF;
  text-transform: inherit;
  padding-top: 8px;
  padding-bottom: 8px;
  padding-left: 5px;
  padding-right: 5px;
}

#zumuvrowdg .gt_first_grand_summary_row {
  padding-top: 8px;
  padding-bottom: 8px;
  padding-left: 5px;
  padding-right: 5px;
  border-top-style: double;
  border-top-width: 6px;
  border-top-color: #D3D3D3;
}

#zumuvrowdg .gt_striped {
  background-color: rgba(128, 128, 128, 0.05);
}

#zumuvrowdg .gt_table_body {
  border-top-style: solid;
  border-top-width: 2px;
  border-top-color: #D3D3D3;
  border-bottom-style: solid;
  border-bottom-width: 2px;
  border-bottom-color: #D3D3D3;
}

#zumuvrowdg .gt_footnotes {
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

#zumuvrowdg .gt_footnote {
  margin: 0px;
  font-size: 90%;
  padding: 4px;
}

#zumuvrowdg .gt_sourcenotes {
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

#zumuvrowdg .gt_sourcenote {
  font-size: 90%;
  padding: 4px;
}

#zumuvrowdg .gt_left {
  text-align: left;
}

#zumuvrowdg .gt_center {
  text-align: center;
}

#zumuvrowdg .gt_right {
  text-align: right;
  font-variant-numeric: tabular-nums;
}

#zumuvrowdg .gt_font_normal {
  font-weight: normal;
}

#zumuvrowdg .gt_font_bold {
  font-weight: bold;
}

#zumuvrowdg .gt_font_italic {
  font-style: italic;
}

#zumuvrowdg .gt_super {
  font-size: 65%;
}

#zumuvrowdg .gt_footnote_marks {
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
    <tr><td class="gt_row gt_left">Method to visually inspect all rows of a dataframe</td>
<td class="gt_row gt_right"><svg aria-hidden="true" role="img" viewBox="0 0 512 512" style="height:2em;width:2em;vertical-align:-0.125em;margin-left:auto;margin-right:auto;font-size:inherit;fill:#9FC2B9;overflow:visible;position:relative;"><path d="M330.67 263.12V173.4l-52.75-24.22C219.44 218.76 197.58 400 56 400a56 56 0 0 0 0 112c212.64 0 370.65-122.87 419.18-210.34l-37.05-38.54zm131.09-128.37C493.92 74.91 477.18 26.48 458.62 3a8 8 0 0 0-11.93-.59l-22.9 23a8.06 8.06 0 0 0-.89 10.23c6.86 10.36 17.05 35.1-1.4 72.32A142.85 142.85 0 0 0 364.34 96c-28 0-54 8.54-76.34 22.59l74.67 34.29v78.24h89.09L506.44 288c3.26-12.62 5.56-25.63 5.56-39.31a154 154 0 0 0-50.24-113.94z"/></svg><svg aria-hidden="true" role="img" viewBox="0 0 512 512" style="height:2em;width:2em;vertical-align:-0.125em;margin-left:auto;margin-right:auto;font-size:inherit;fill:#9FC2B9;overflow:visible;position:relative;"><path d="M330.67 263.12V173.4l-52.75-24.22C219.44 218.76 197.58 400 56 400a56 56 0 0 0 0 112c212.64 0 370.65-122.87 419.18-210.34l-37.05-38.54zm131.09-128.37C493.92 74.91 477.18 26.48 458.62 3a8 8 0 0 0-11.93-.59l-22.9 23a8.06 8.06 0 0 0-.89 10.23c6.86 10.36 17.05 35.1-1.4 72.32A142.85 142.85 0 0 0 364.34 96c-28 0-54 8.54-76.34 22.59l74.67 34.29v78.24h89.09L506.44 288c3.26-12.62 5.56-25.63 5.56-39.31a154 154 0 0 0-50.24-113.94z"/></svg><svg aria-hidden="true" role="img" viewBox="0 0 512 512" style="height:2em;width:2em;vertical-align:-0.125em;margin-left:auto;margin-right:auto;font-size:inherit;fill:#9FC2B9;overflow:visible;position:relative;"><path d="M330.67 263.12V173.4l-52.75-24.22C219.44 218.76 197.58 400 56 400a56 56 0 0 0 0 112c212.64 0 370.65-122.87 419.18-210.34l-37.05-38.54zm131.09-128.37C493.92 74.91 477.18 26.48 458.62 3a8 8 0 0 0-11.93-.59l-22.9 23a8.06 8.06 0 0 0-.89 10.23c6.86 10.36 17.05 35.1-1.4 72.32A142.85 142.85 0 0 0 364.34 96c-28 0-54 8.54-76.34 22.59l74.67 34.29v78.24h89.09L506.44 288c3.26-12.62 5.56-25.63 5.56-39.31a154 154 0 0 0-50.24-113.94z"/></svg></td></tr>
  </tbody>
  
  
</table>
</div>
```

```{=html}
<div id="tevlbidtlr" style="overflow-x:auto;overflow-y:auto;width:auto;height:auto;">
<style>html {
  font-family: -apple-system, BlinkMacSystemFont, 'Segoe UI', Roboto, Oxygen, Ubuntu, Cantarell, 'Helvetica Neue', 'Fira Sans', 'Droid Sans', Arial, sans-serif;
}

#tevlbidtlr .gt_table {
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

#tevlbidtlr .gt_heading {
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

#tevlbidtlr .gt_title {
  color: #FFFFFF;
  font-size: 125%;
  font-weight: initial;
  padding-top: 4px;
  padding-bottom: 4px;
  border-bottom-color: #FFFFFF;
  border-bottom-width: 0;
}

#tevlbidtlr .gt_subtitle {
  color: #FFFFFF;
  font-size: 85%;
  font-weight: initial;
  padding-top: 0;
  padding-bottom: 6px;
  border-top-color: #FFFFFF;
  border-top-width: 0;
}

#tevlbidtlr .gt_bottom_border {
  border-bottom-style: solid;
  border-bottom-width: 2px;
  border-bottom-color: #D3D3D3;
}

#tevlbidtlr .gt_col_headings {
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

#tevlbidtlr .gt_col_heading {
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

#tevlbidtlr .gt_column_spanner_outer {
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

#tevlbidtlr .gt_column_spanner_outer:first-child {
  padding-left: 0;
}

#tevlbidtlr .gt_column_spanner_outer:last-child {
  padding-right: 0;
}

#tevlbidtlr .gt_column_spanner {
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

#tevlbidtlr .gt_group_heading {
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

#tevlbidtlr .gt_empty_group_heading {
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

#tevlbidtlr .gt_from_md > :first-child {
  margin-top: 0;
}

#tevlbidtlr .gt_from_md > :last-child {
  margin-bottom: 0;
}

#tevlbidtlr .gt_row {
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

#tevlbidtlr .gt_stub {
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

#tevlbidtlr .gt_summary_row {
  color: #333333;
  background-color: #FFFFFF;
  text-transform: inherit;
  padding-top: 8px;
  padding-bottom: 8px;
  padding-left: 5px;
  padding-right: 5px;
}

#tevlbidtlr .gt_first_summary_row {
  padding-top: 8px;
  padding-bottom: 8px;
  padding-left: 5px;
  padding-right: 5px;
  border-top-style: solid;
  border-top-width: 2px;
  border-top-color: #D3D3D3;
}

#tevlbidtlr .gt_grand_summary_row {
  color: #333333;
  background-color: #FFFFFF;
  text-transform: inherit;
  padding-top: 8px;
  padding-bottom: 8px;
  padding-left: 5px;
  padding-right: 5px;
}

#tevlbidtlr .gt_first_grand_summary_row {
  padding-top: 8px;
  padding-bottom: 8px;
  padding-left: 5px;
  padding-right: 5px;
  border-top-style: double;
  border-top-width: 6px;
  border-top-color: #D3D3D3;
}

#tevlbidtlr .gt_striped {
  background-color: rgba(128, 128, 128, 0.05);
}

#tevlbidtlr .gt_table_body {
  border-top-style: solid;
  border-top-width: 2px;
  border-top-color: #D3D3D3;
  border-bottom-style: solid;
  border-bottom-width: 2px;
  border-bottom-color: #D3D3D3;
}

#tevlbidtlr .gt_footnotes {
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

#tevlbidtlr .gt_footnote {
  margin: 0px;
  font-size: 90%;
  padding: 4px;
}

#tevlbidtlr .gt_sourcenotes {
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

#tevlbidtlr .gt_sourcenote {
  font-size: 90%;
  padding: 4px;
}

#tevlbidtlr .gt_left {
  text-align: left;
}

#tevlbidtlr .gt_center {
  text-align: center;
}

#tevlbidtlr .gt_right {
  text-align: right;
  font-variant-numeric: tabular-nums;
}

#tevlbidtlr .gt_font_normal {
  font-weight: normal;
}

#tevlbidtlr .gt_font_bold {
  font-weight: bold;
}

#tevlbidtlr .gt_font_italic {
  font-style: italic;
}

#tevlbidtlr .gt_super {
  font-size: 65%;
}

#tevlbidtlr .gt_footnote_marks {
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
    <tr><td class="gt_row gt_center"><div class='gt_from_md'><p>readr</p>
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
function(data)
```

</br>

**Actual Instructions**

```r
View(df)
```
