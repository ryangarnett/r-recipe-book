# (PART\*) Lunch {-}





# Aggregating Data


## Single Column


### Get the unique values within a column

```{=html}
<div id="cgqmqyfjgx" style="overflow-x:auto;overflow-y:auto;width:auto;height:auto;">
<style>html {
  font-family: -apple-system, BlinkMacSystemFont, 'Segoe UI', Roboto, Oxygen, Ubuntu, Cantarell, 'Helvetica Neue', 'Fira Sans', 'Droid Sans', Arial, sans-serif;
}

#cgqmqyfjgx .gt_table {
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

#cgqmqyfjgx .gt_heading {
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

#cgqmqyfjgx .gt_title {
  color: #FFFFFF;
  font-size: 125%;
  font-weight: initial;
  padding-top: 4px;
  padding-bottom: 4px;
  border-bottom-color: #FFFFFF;
  border-bottom-width: 0;
}

#cgqmqyfjgx .gt_subtitle {
  color: #FFFFFF;
  font-size: 85%;
  font-weight: initial;
  padding-top: 0;
  padding-bottom: 6px;
  border-top-color: #FFFFFF;
  border-top-width: 0;
}

#cgqmqyfjgx .gt_bottom_border {
  border-bottom-style: solid;
  border-bottom-width: 2px;
  border-bottom-color: #D3D3D3;
}

#cgqmqyfjgx .gt_col_headings {
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

#cgqmqyfjgx .gt_col_heading {
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

#cgqmqyfjgx .gt_column_spanner_outer {
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

#cgqmqyfjgx .gt_column_spanner_outer:first-child {
  padding-left: 0;
}

#cgqmqyfjgx .gt_column_spanner_outer:last-child {
  padding-right: 0;
}

#cgqmqyfjgx .gt_column_spanner {
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

#cgqmqyfjgx .gt_group_heading {
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

#cgqmqyfjgx .gt_empty_group_heading {
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

#cgqmqyfjgx .gt_from_md > :first-child {
  margin-top: 0;
}

#cgqmqyfjgx .gt_from_md > :last-child {
  margin-bottom: 0;
}

#cgqmqyfjgx .gt_row {
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

#cgqmqyfjgx .gt_stub {
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

#cgqmqyfjgx .gt_summary_row {
  color: #333333;
  background-color: #FFFFFF;
  text-transform: inherit;
  padding-top: 8px;
  padding-bottom: 8px;
  padding-left: 5px;
  padding-right: 5px;
}

#cgqmqyfjgx .gt_first_summary_row {
  padding-top: 8px;
  padding-bottom: 8px;
  padding-left: 5px;
  padding-right: 5px;
  border-top-style: solid;
  border-top-width: 2px;
  border-top-color: #D3D3D3;
}

#cgqmqyfjgx .gt_grand_summary_row {
  color: #333333;
  background-color: #FFFFFF;
  text-transform: inherit;
  padding-top: 8px;
  padding-bottom: 8px;
  padding-left: 5px;
  padding-right: 5px;
}

#cgqmqyfjgx .gt_first_grand_summary_row {
  padding-top: 8px;
  padding-bottom: 8px;
  padding-left: 5px;
  padding-right: 5px;
  border-top-style: double;
  border-top-width: 6px;
  border-top-color: #D3D3D3;
}

#cgqmqyfjgx .gt_striped {
  background-color: rgba(128, 128, 128, 0.05);
}

#cgqmqyfjgx .gt_table_body {
  border-top-style: solid;
  border-top-width: 2px;
  border-top-color: #D3D3D3;
  border-bottom-style: solid;
  border-bottom-width: 2px;
  border-bottom-color: #D3D3D3;
}

#cgqmqyfjgx .gt_footnotes {
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

#cgqmqyfjgx .gt_footnote {
  margin: 0px;
  font-size: 90%;
  padding: 4px;
}

#cgqmqyfjgx .gt_sourcenotes {
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

#cgqmqyfjgx .gt_sourcenote {
  font-size: 90%;
  padding: 4px;
}

#cgqmqyfjgx .gt_left {
  text-align: left;
}

#cgqmqyfjgx .gt_center {
  text-align: center;
}

#cgqmqyfjgx .gt_right {
  text-align: right;
  font-variant-numeric: tabular-nums;
}

#cgqmqyfjgx .gt_font_normal {
  font-weight: normal;
}

#cgqmqyfjgx .gt_font_bold {
  font-weight: bold;
}

#cgqmqyfjgx .gt_font_italic {
  font-style: italic;
}

#cgqmqyfjgx .gt_super {
  font-size: 65%;
}

#cgqmqyfjgx .gt_footnote_marks {
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
    <tr><td class="gt_row gt_left">Method to get all unique values within a single column of a dataframe</td>
<td class="gt_row gt_right"><svg aria-hidden="true" role="img" viewBox="0 0 512 512" style="height:2em;width:2em;vertical-align:-0.125em;margin-left:auto;margin-right:auto;font-size:inherit;fill:#A62014;overflow:visible;position:relative;"><path d="M330.67 263.12V173.4l-52.75-24.22C219.44 218.76 197.58 400 56 400a56 56 0 0 0 0 112c212.64 0 370.65-122.87 419.18-210.34l-37.05-38.54zm131.09-128.37C493.92 74.91 477.18 26.48 458.62 3a8 8 0 0 0-11.93-.59l-22.9 23a8.06 8.06 0 0 0-.89 10.23c6.86 10.36 17.05 35.1-1.4 72.32A142.85 142.85 0 0 0 364.34 96c-28 0-54 8.54-76.34 22.59l74.67 34.29v78.24h89.09L506.44 288c3.26-12.62 5.56-25.63 5.56-39.31a154 154 0 0 0-50.24-113.94z"/></svg><svg aria-hidden="true" role="img" viewBox="0 0 512 512" style="height:2em;width:2em;vertical-align:-0.125em;margin-left:auto;margin-right:auto;font-size:inherit;fill:#9FC2B9;overflow:visible;position:relative;"><path d="M330.67 263.12V173.4l-52.75-24.22C219.44 218.76 197.58 400 56 400a56 56 0 0 0 0 112c212.64 0 370.65-122.87 419.18-210.34l-37.05-38.54zm131.09-128.37C493.92 74.91 477.18 26.48 458.62 3a8 8 0 0 0-11.93-.59l-22.9 23a8.06 8.06 0 0 0-.89 10.23c6.86 10.36 17.05 35.1-1.4 72.32A142.85 142.85 0 0 0 364.34 96c-28 0-54 8.54-76.34 22.59l74.67 34.29v78.24h89.09L506.44 288c3.26-12.62 5.56-25.63 5.56-39.31a154 154 0 0 0-50.24-113.94z"/></svg><svg aria-hidden="true" role="img" viewBox="0 0 512 512" style="height:2em;width:2em;vertical-align:-0.125em;margin-left:auto;margin-right:auto;font-size:inherit;fill:#9FC2B9;overflow:visible;position:relative;"><path d="M330.67 263.12V173.4l-52.75-24.22C219.44 218.76 197.58 400 56 400a56 56 0 0 0 0 112c212.64 0 370.65-122.87 419.18-210.34l-37.05-38.54zm131.09-128.37C493.92 74.91 477.18 26.48 458.62 3a8 8 0 0 0-11.93-.59l-22.9 23a8.06 8.06 0 0 0-.89 10.23c6.86 10.36 17.05 35.1-1.4 72.32A142.85 142.85 0 0 0 364.34 96c-28 0-54 8.54-76.34 22.59l74.67 34.29v78.24h89.09L506.44 288c3.26-12.62 5.56-25.63 5.56-39.31a154 154 0 0 0-50.24-113.94z"/></svg></td></tr>
  </tbody>
  
  
</table>
</div>
```

```{=html}
<div id="ajbjlpcryc" style="overflow-x:auto;overflow-y:auto;width:auto;height:auto;">
<style>html {
  font-family: -apple-system, BlinkMacSystemFont, 'Segoe UI', Roboto, Oxygen, Ubuntu, Cantarell, 'Helvetica Neue', 'Fira Sans', 'Droid Sans', Arial, sans-serif;
}

#ajbjlpcryc .gt_table {
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

#ajbjlpcryc .gt_heading {
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

#ajbjlpcryc .gt_title {
  color: #FFFFFF;
  font-size: 125%;
  font-weight: initial;
  padding-top: 4px;
  padding-bottom: 4px;
  border-bottom-color: #FFFFFF;
  border-bottom-width: 0;
}

#ajbjlpcryc .gt_subtitle {
  color: #FFFFFF;
  font-size: 85%;
  font-weight: initial;
  padding-top: 0;
  padding-bottom: 6px;
  border-top-color: #FFFFFF;
  border-top-width: 0;
}

#ajbjlpcryc .gt_bottom_border {
  border-bottom-style: solid;
  border-bottom-width: 2px;
  border-bottom-color: #D3D3D3;
}

#ajbjlpcryc .gt_col_headings {
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

#ajbjlpcryc .gt_col_heading {
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

#ajbjlpcryc .gt_column_spanner_outer {
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

#ajbjlpcryc .gt_column_spanner_outer:first-child {
  padding-left: 0;
}

#ajbjlpcryc .gt_column_spanner_outer:last-child {
  padding-right: 0;
}

#ajbjlpcryc .gt_column_spanner {
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

#ajbjlpcryc .gt_group_heading {
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

#ajbjlpcryc .gt_empty_group_heading {
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

#ajbjlpcryc .gt_from_md > :first-child {
  margin-top: 0;
}

#ajbjlpcryc .gt_from_md > :last-child {
  margin-bottom: 0;
}

#ajbjlpcryc .gt_row {
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

#ajbjlpcryc .gt_stub {
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

#ajbjlpcryc .gt_summary_row {
  color: #333333;
  background-color: #FFFFFF;
  text-transform: inherit;
  padding-top: 8px;
  padding-bottom: 8px;
  padding-left: 5px;
  padding-right: 5px;
}

#ajbjlpcryc .gt_first_summary_row {
  padding-top: 8px;
  padding-bottom: 8px;
  padding-left: 5px;
  padding-right: 5px;
  border-top-style: solid;
  border-top-width: 2px;
  border-top-color: #D3D3D3;
}

#ajbjlpcryc .gt_grand_summary_row {
  color: #333333;
  background-color: #FFFFFF;
  text-transform: inherit;
  padding-top: 8px;
  padding-bottom: 8px;
  padding-left: 5px;
  padding-right: 5px;
}

#ajbjlpcryc .gt_first_grand_summary_row {
  padding-top: 8px;
  padding-bottom: 8px;
  padding-left: 5px;
  padding-right: 5px;
  border-top-style: double;
  border-top-width: 6px;
  border-top-color: #D3D3D3;
}

#ajbjlpcryc .gt_striped {
  background-color: rgba(128, 128, 128, 0.05);
}

#ajbjlpcryc .gt_table_body {
  border-top-style: solid;
  border-top-width: 2px;
  border-top-color: #D3D3D3;
  border-bottom-style: solid;
  border-bottom-width: 2px;
  border-bottom-color: #D3D3D3;
}

#ajbjlpcryc .gt_footnotes {
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

#ajbjlpcryc .gt_footnote {
  margin: 0px;
  font-size: 90%;
  padding: 4px;
}

#ajbjlpcryc .gt_sourcenotes {
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

#ajbjlpcryc .gt_sourcenote {
  font-size: 90%;
  padding: 4px;
}

#ajbjlpcryc .gt_left {
  text-align: left;
}

#ajbjlpcryc .gt_center {
  text-align: center;
}

#ajbjlpcryc .gt_right {
  text-align: right;
  font-variant-numeric: tabular-nums;
}

#ajbjlpcryc .gt_font_normal {
  font-weight: normal;
}

#ajbjlpcryc .gt_font_bold {
  font-weight: bold;
}

#ajbjlpcryc .gt_font_italic {
  font-style: italic;
}

#ajbjlpcryc .gt_super {
  font-size: 65%;
}

#ajbjlpcryc .gt_footnote_marks {
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
package::function(data, column_name)
```

</br>

**Actual Instructions**

```r
dplyr::distinct(df, species)
```


### Get the unique values and their frequency within a column

```{=html}
<div id="zdkvdujqby" style="overflow-x:auto;overflow-y:auto;width:auto;height:auto;">
<style>html {
  font-family: -apple-system, BlinkMacSystemFont, 'Segoe UI', Roboto, Oxygen, Ubuntu, Cantarell, 'Helvetica Neue', 'Fira Sans', 'Droid Sans', Arial, sans-serif;
}

#zdkvdujqby .gt_table {
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

#zdkvdujqby .gt_heading {
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

#zdkvdujqby .gt_title {
  color: #FFFFFF;
  font-size: 125%;
  font-weight: initial;
  padding-top: 4px;
  padding-bottom: 4px;
  border-bottom-color: #FFFFFF;
  border-bottom-width: 0;
}

#zdkvdujqby .gt_subtitle {
  color: #FFFFFF;
  font-size: 85%;
  font-weight: initial;
  padding-top: 0;
  padding-bottom: 6px;
  border-top-color: #FFFFFF;
  border-top-width: 0;
}

#zdkvdujqby .gt_bottom_border {
  border-bottom-style: solid;
  border-bottom-width: 2px;
  border-bottom-color: #D3D3D3;
}

#zdkvdujqby .gt_col_headings {
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

#zdkvdujqby .gt_col_heading {
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

#zdkvdujqby .gt_column_spanner_outer {
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

#zdkvdujqby .gt_column_spanner_outer:first-child {
  padding-left: 0;
}

#zdkvdujqby .gt_column_spanner_outer:last-child {
  padding-right: 0;
}

#zdkvdujqby .gt_column_spanner {
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

#zdkvdujqby .gt_group_heading {
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

#zdkvdujqby .gt_empty_group_heading {
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

#zdkvdujqby .gt_from_md > :first-child {
  margin-top: 0;
}

#zdkvdujqby .gt_from_md > :last-child {
  margin-bottom: 0;
}

#zdkvdujqby .gt_row {
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

#zdkvdujqby .gt_stub {
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

#zdkvdujqby .gt_summary_row {
  color: #333333;
  background-color: #FFFFFF;
  text-transform: inherit;
  padding-top: 8px;
  padding-bottom: 8px;
  padding-left: 5px;
  padding-right: 5px;
}

#zdkvdujqby .gt_first_summary_row {
  padding-top: 8px;
  padding-bottom: 8px;
  padding-left: 5px;
  padding-right: 5px;
  border-top-style: solid;
  border-top-width: 2px;
  border-top-color: #D3D3D3;
}

#zdkvdujqby .gt_grand_summary_row {
  color: #333333;
  background-color: #FFFFFF;
  text-transform: inherit;
  padding-top: 8px;
  padding-bottom: 8px;
  padding-left: 5px;
  padding-right: 5px;
}

#zdkvdujqby .gt_first_grand_summary_row {
  padding-top: 8px;
  padding-bottom: 8px;
  padding-left: 5px;
  padding-right: 5px;
  border-top-style: double;
  border-top-width: 6px;
  border-top-color: #D3D3D3;
}

#zdkvdujqby .gt_striped {
  background-color: rgba(128, 128, 128, 0.05);
}

#zdkvdujqby .gt_table_body {
  border-top-style: solid;
  border-top-width: 2px;
  border-top-color: #D3D3D3;
  border-bottom-style: solid;
  border-bottom-width: 2px;
  border-bottom-color: #D3D3D3;
}

#zdkvdujqby .gt_footnotes {
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

#zdkvdujqby .gt_footnote {
  margin: 0px;
  font-size: 90%;
  padding: 4px;
}

#zdkvdujqby .gt_sourcenotes {
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

#zdkvdujqby .gt_sourcenote {
  font-size: 90%;
  padding: 4px;
}

#zdkvdujqby .gt_left {
  text-align: left;
}

#zdkvdujqby .gt_center {
  text-align: center;
}

#zdkvdujqby .gt_right {
  text-align: right;
  font-variant-numeric: tabular-nums;
}

#zdkvdujqby .gt_font_normal {
  font-weight: normal;
}

#zdkvdujqby .gt_font_bold {
  font-weight: bold;
}

#zdkvdujqby .gt_font_italic {
  font-style: italic;
}

#zdkvdujqby .gt_super {
  font-size: 65%;
}

#zdkvdujqby .gt_footnote_marks {
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
    <tr><td class="gt_row gt_left">Method to get all unique values and their frequency within a single column of a dataframe</td>
<td class="gt_row gt_right"><svg aria-hidden="true" role="img" viewBox="0 0 512 512" style="height:2em;width:2em;vertical-align:-0.125em;margin-left:auto;margin-right:auto;font-size:inherit;fill:#A62014;overflow:visible;position:relative;"><path d="M330.67 263.12V173.4l-52.75-24.22C219.44 218.76 197.58 400 56 400a56 56 0 0 0 0 112c212.64 0 370.65-122.87 419.18-210.34l-37.05-38.54zm131.09-128.37C493.92 74.91 477.18 26.48 458.62 3a8 8 0 0 0-11.93-.59l-22.9 23a8.06 8.06 0 0 0-.89 10.23c6.86 10.36 17.05 35.1-1.4 72.32A142.85 142.85 0 0 0 364.34 96c-28 0-54 8.54-76.34 22.59l74.67 34.29v78.24h89.09L506.44 288c3.26-12.62 5.56-25.63 5.56-39.31a154 154 0 0 0-50.24-113.94z"/></svg><svg aria-hidden="true" role="img" viewBox="0 0 512 512" style="height:2em;width:2em;vertical-align:-0.125em;margin-left:auto;margin-right:auto;font-size:inherit;fill:#9FC2B9;overflow:visible;position:relative;"><path d="M330.67 263.12V173.4l-52.75-24.22C219.44 218.76 197.58 400 56 400a56 56 0 0 0 0 112c212.64 0 370.65-122.87 419.18-210.34l-37.05-38.54zm131.09-128.37C493.92 74.91 477.18 26.48 458.62 3a8 8 0 0 0-11.93-.59l-22.9 23a8.06 8.06 0 0 0-.89 10.23c6.86 10.36 17.05 35.1-1.4 72.32A142.85 142.85 0 0 0 364.34 96c-28 0-54 8.54-76.34 22.59l74.67 34.29v78.24h89.09L506.44 288c3.26-12.62 5.56-25.63 5.56-39.31a154 154 0 0 0-50.24-113.94z"/></svg><svg aria-hidden="true" role="img" viewBox="0 0 512 512" style="height:2em;width:2em;vertical-align:-0.125em;margin-left:auto;margin-right:auto;font-size:inherit;fill:#9FC2B9;overflow:visible;position:relative;"><path d="M330.67 263.12V173.4l-52.75-24.22C219.44 218.76 197.58 400 56 400a56 56 0 0 0 0 112c212.64 0 370.65-122.87 419.18-210.34l-37.05-38.54zm131.09-128.37C493.92 74.91 477.18 26.48 458.62 3a8 8 0 0 0-11.93-.59l-22.9 23a8.06 8.06 0 0 0-.89 10.23c6.86 10.36 17.05 35.1-1.4 72.32A142.85 142.85 0 0 0 364.34 96c-28 0-54 8.54-76.34 22.59l74.67 34.29v78.24h89.09L506.44 288c3.26-12.62 5.56-25.63 5.56-39.31a154 154 0 0 0-50.24-113.94z"/></svg></td></tr>
  </tbody>
  
  
</table>
</div>
```

```{=html}
<div id="acdppgwilw" style="overflow-x:auto;overflow-y:auto;width:auto;height:auto;">
<style>html {
  font-family: -apple-system, BlinkMacSystemFont, 'Segoe UI', Roboto, Oxygen, Ubuntu, Cantarell, 'Helvetica Neue', 'Fira Sans', 'Droid Sans', Arial, sans-serif;
}

#acdppgwilw .gt_table {
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

#acdppgwilw .gt_heading {
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

#acdppgwilw .gt_title {
  color: #FFFFFF;
  font-size: 125%;
  font-weight: initial;
  padding-top: 4px;
  padding-bottom: 4px;
  border-bottom-color: #FFFFFF;
  border-bottom-width: 0;
}

#acdppgwilw .gt_subtitle {
  color: #FFFFFF;
  font-size: 85%;
  font-weight: initial;
  padding-top: 0;
  padding-bottom: 6px;
  border-top-color: #FFFFFF;
  border-top-width: 0;
}

#acdppgwilw .gt_bottom_border {
  border-bottom-style: solid;
  border-bottom-width: 2px;
  border-bottom-color: #D3D3D3;
}

#acdppgwilw .gt_col_headings {
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

#acdppgwilw .gt_col_heading {
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

#acdppgwilw .gt_column_spanner_outer {
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

#acdppgwilw .gt_column_spanner_outer:first-child {
  padding-left: 0;
}

#acdppgwilw .gt_column_spanner_outer:last-child {
  padding-right: 0;
}

#acdppgwilw .gt_column_spanner {
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

#acdppgwilw .gt_group_heading {
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

#acdppgwilw .gt_empty_group_heading {
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

#acdppgwilw .gt_from_md > :first-child {
  margin-top: 0;
}

#acdppgwilw .gt_from_md > :last-child {
  margin-bottom: 0;
}

#acdppgwilw .gt_row {
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

#acdppgwilw .gt_stub {
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

#acdppgwilw .gt_summary_row {
  color: #333333;
  background-color: #FFFFFF;
  text-transform: inherit;
  padding-top: 8px;
  padding-bottom: 8px;
  padding-left: 5px;
  padding-right: 5px;
}

#acdppgwilw .gt_first_summary_row {
  padding-top: 8px;
  padding-bottom: 8px;
  padding-left: 5px;
  padding-right: 5px;
  border-top-style: solid;
  border-top-width: 2px;
  border-top-color: #D3D3D3;
}

#acdppgwilw .gt_grand_summary_row {
  color: #333333;
  background-color: #FFFFFF;
  text-transform: inherit;
  padding-top: 8px;
  padding-bottom: 8px;
  padding-left: 5px;
  padding-right: 5px;
}

#acdppgwilw .gt_first_grand_summary_row {
  padding-top: 8px;
  padding-bottom: 8px;
  padding-left: 5px;
  padding-right: 5px;
  border-top-style: double;
  border-top-width: 6px;
  border-top-color: #D3D3D3;
}

#acdppgwilw .gt_striped {
  background-color: rgba(128, 128, 128, 0.05);
}

#acdppgwilw .gt_table_body {
  border-top-style: solid;
  border-top-width: 2px;
  border-top-color: #D3D3D3;
  border-bottom-style: solid;
  border-bottom-width: 2px;
  border-bottom-color: #D3D3D3;
}

#acdppgwilw .gt_footnotes {
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

#acdppgwilw .gt_footnote {
  margin: 0px;
  font-size: 90%;
  padding: 4px;
}

#acdppgwilw .gt_sourcenotes {
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

#acdppgwilw .gt_sourcenote {
  font-size: 90%;
  padding: 4px;
}

#acdppgwilw .gt_left {
  text-align: left;
}

#acdppgwilw .gt_center {
  text-align: center;
}

#acdppgwilw .gt_right {
  text-align: right;
  font-variant-numeric: tabular-nums;
}

#acdppgwilw .gt_font_normal {
  font-weight: normal;
}

#acdppgwilw .gt_font_bold {
  font-weight: bold;
}

#acdppgwilw .gt_font_italic {
  font-style: italic;
}

#acdppgwilw .gt_super {
  font-size: 65%;
}

#acdppgwilw .gt_footnote_marks {
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
package::function(data, column_name) %>%
  package::function() %>%
  package::function()
```

</br>

**Actual Instructions**

```r
dplyr::group_by(df, species) %>%
  dplyr::tally() %>%
  dplyr::ungroup()
```


### Get the unique values and their frequency within a column while ordering from the smallest value

```{=html}
<div id="winvplvjrk" style="overflow-x:auto;overflow-y:auto;width:auto;height:auto;">
<style>html {
  font-family: -apple-system, BlinkMacSystemFont, 'Segoe UI', Roboto, Oxygen, Ubuntu, Cantarell, 'Helvetica Neue', 'Fira Sans', 'Droid Sans', Arial, sans-serif;
}

#winvplvjrk .gt_table {
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

#winvplvjrk .gt_heading {
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

#winvplvjrk .gt_title {
  color: #FFFFFF;
  font-size: 125%;
  font-weight: initial;
  padding-top: 4px;
  padding-bottom: 4px;
  border-bottom-color: #FFFFFF;
  border-bottom-width: 0;
}

#winvplvjrk .gt_subtitle {
  color: #FFFFFF;
  font-size: 85%;
  font-weight: initial;
  padding-top: 0;
  padding-bottom: 6px;
  border-top-color: #FFFFFF;
  border-top-width: 0;
}

#winvplvjrk .gt_bottom_border {
  border-bottom-style: solid;
  border-bottom-width: 2px;
  border-bottom-color: #D3D3D3;
}

#winvplvjrk .gt_col_headings {
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

#winvplvjrk .gt_col_heading {
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

#winvplvjrk .gt_column_spanner_outer {
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

#winvplvjrk .gt_column_spanner_outer:first-child {
  padding-left: 0;
}

#winvplvjrk .gt_column_spanner_outer:last-child {
  padding-right: 0;
}

#winvplvjrk .gt_column_spanner {
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

#winvplvjrk .gt_group_heading {
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

#winvplvjrk .gt_empty_group_heading {
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

#winvplvjrk .gt_from_md > :first-child {
  margin-top: 0;
}

#winvplvjrk .gt_from_md > :last-child {
  margin-bottom: 0;
}

#winvplvjrk .gt_row {
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

#winvplvjrk .gt_stub {
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

#winvplvjrk .gt_summary_row {
  color: #333333;
  background-color: #FFFFFF;
  text-transform: inherit;
  padding-top: 8px;
  padding-bottom: 8px;
  padding-left: 5px;
  padding-right: 5px;
}

#winvplvjrk .gt_first_summary_row {
  padding-top: 8px;
  padding-bottom: 8px;
  padding-left: 5px;
  padding-right: 5px;
  border-top-style: solid;
  border-top-width: 2px;
  border-top-color: #D3D3D3;
}

#winvplvjrk .gt_grand_summary_row {
  color: #333333;
  background-color: #FFFFFF;
  text-transform: inherit;
  padding-top: 8px;
  padding-bottom: 8px;
  padding-left: 5px;
  padding-right: 5px;
}

#winvplvjrk .gt_first_grand_summary_row {
  padding-top: 8px;
  padding-bottom: 8px;
  padding-left: 5px;
  padding-right: 5px;
  border-top-style: double;
  border-top-width: 6px;
  border-top-color: #D3D3D3;
}

#winvplvjrk .gt_striped {
  background-color: rgba(128, 128, 128, 0.05);
}

#winvplvjrk .gt_table_body {
  border-top-style: solid;
  border-top-width: 2px;
  border-top-color: #D3D3D3;
  border-bottom-style: solid;
  border-bottom-width: 2px;
  border-bottom-color: #D3D3D3;
}

#winvplvjrk .gt_footnotes {
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

#winvplvjrk .gt_footnote {
  margin: 0px;
  font-size: 90%;
  padding: 4px;
}

#winvplvjrk .gt_sourcenotes {
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

#winvplvjrk .gt_sourcenote {
  font-size: 90%;
  padding: 4px;
}

#winvplvjrk .gt_left {
  text-align: left;
}

#winvplvjrk .gt_center {
  text-align: center;
}

#winvplvjrk .gt_right {
  text-align: right;
  font-variant-numeric: tabular-nums;
}

#winvplvjrk .gt_font_normal {
  font-weight: normal;
}

#winvplvjrk .gt_font_bold {
  font-weight: bold;
}

#winvplvjrk .gt_font_italic {
  font-style: italic;
}

#winvplvjrk .gt_super {
  font-size: 65%;
}

#winvplvjrk .gt_footnote_marks {
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
    <tr><td class="gt_row gt_left">Method to get all unique values and ordering their frequency from smallest to largest within a single column of a dataframe</td>
<td class="gt_row gt_right"><svg aria-hidden="true" role="img" viewBox="0 0 512 512" style="height:2em;width:2em;vertical-align:-0.125em;margin-left:auto;margin-right:auto;font-size:inherit;fill:#A62014;overflow:visible;position:relative;"><path d="M330.67 263.12V173.4l-52.75-24.22C219.44 218.76 197.58 400 56 400a56 56 0 0 0 0 112c212.64 0 370.65-122.87 419.18-210.34l-37.05-38.54zm131.09-128.37C493.92 74.91 477.18 26.48 458.62 3a8 8 0 0 0-11.93-.59l-22.9 23a8.06 8.06 0 0 0-.89 10.23c6.86 10.36 17.05 35.1-1.4 72.32A142.85 142.85 0 0 0 364.34 96c-28 0-54 8.54-76.34 22.59l74.67 34.29v78.24h89.09L506.44 288c3.26-12.62 5.56-25.63 5.56-39.31a154 154 0 0 0-50.24-113.94z"/></svg><svg aria-hidden="true" role="img" viewBox="0 0 512 512" style="height:2em;width:2em;vertical-align:-0.125em;margin-left:auto;margin-right:auto;font-size:inherit;fill:#9FC2B9;overflow:visible;position:relative;"><path d="M330.67 263.12V173.4l-52.75-24.22C219.44 218.76 197.58 400 56 400a56 56 0 0 0 0 112c212.64 0 370.65-122.87 419.18-210.34l-37.05-38.54zm131.09-128.37C493.92 74.91 477.18 26.48 458.62 3a8 8 0 0 0-11.93-.59l-22.9 23a8.06 8.06 0 0 0-.89 10.23c6.86 10.36 17.05 35.1-1.4 72.32A142.85 142.85 0 0 0 364.34 96c-28 0-54 8.54-76.34 22.59l74.67 34.29v78.24h89.09L506.44 288c3.26-12.62 5.56-25.63 5.56-39.31a154 154 0 0 0-50.24-113.94z"/></svg><svg aria-hidden="true" role="img" viewBox="0 0 512 512" style="height:2em;width:2em;vertical-align:-0.125em;margin-left:auto;margin-right:auto;font-size:inherit;fill:#9FC2B9;overflow:visible;position:relative;"><path d="M330.67 263.12V173.4l-52.75-24.22C219.44 218.76 197.58 400 56 400a56 56 0 0 0 0 112c212.64 0 370.65-122.87 419.18-210.34l-37.05-38.54zm131.09-128.37C493.92 74.91 477.18 26.48 458.62 3a8 8 0 0 0-11.93-.59l-22.9 23a8.06 8.06 0 0 0-.89 10.23c6.86 10.36 17.05 35.1-1.4 72.32A142.85 142.85 0 0 0 364.34 96c-28 0-54 8.54-76.34 22.59l74.67 34.29v78.24h89.09L506.44 288c3.26-12.62 5.56-25.63 5.56-39.31a154 154 0 0 0-50.24-113.94z"/></svg></td></tr>
  </tbody>
  
  
</table>
</div>
```

```{=html}
<div id="aqcjwvvcdh" style="overflow-x:auto;overflow-y:auto;width:auto;height:auto;">
<style>html {
  font-family: -apple-system, BlinkMacSystemFont, 'Segoe UI', Roboto, Oxygen, Ubuntu, Cantarell, 'Helvetica Neue', 'Fira Sans', 'Droid Sans', Arial, sans-serif;
}

#aqcjwvvcdh .gt_table {
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

#aqcjwvvcdh .gt_heading {
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

#aqcjwvvcdh .gt_title {
  color: #FFFFFF;
  font-size: 125%;
  font-weight: initial;
  padding-top: 4px;
  padding-bottom: 4px;
  border-bottom-color: #FFFFFF;
  border-bottom-width: 0;
}

#aqcjwvvcdh .gt_subtitle {
  color: #FFFFFF;
  font-size: 85%;
  font-weight: initial;
  padding-top: 0;
  padding-bottom: 6px;
  border-top-color: #FFFFFF;
  border-top-width: 0;
}

#aqcjwvvcdh .gt_bottom_border {
  border-bottom-style: solid;
  border-bottom-width: 2px;
  border-bottom-color: #D3D3D3;
}

#aqcjwvvcdh .gt_col_headings {
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

#aqcjwvvcdh .gt_col_heading {
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

#aqcjwvvcdh .gt_column_spanner_outer {
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

#aqcjwvvcdh .gt_column_spanner_outer:first-child {
  padding-left: 0;
}

#aqcjwvvcdh .gt_column_spanner_outer:last-child {
  padding-right: 0;
}

#aqcjwvvcdh .gt_column_spanner {
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

#aqcjwvvcdh .gt_group_heading {
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

#aqcjwvvcdh .gt_empty_group_heading {
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

#aqcjwvvcdh .gt_from_md > :first-child {
  margin-top: 0;
}

#aqcjwvvcdh .gt_from_md > :last-child {
  margin-bottom: 0;
}

#aqcjwvvcdh .gt_row {
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

#aqcjwvvcdh .gt_stub {
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

#aqcjwvvcdh .gt_summary_row {
  color: #333333;
  background-color: #FFFFFF;
  text-transform: inherit;
  padding-top: 8px;
  padding-bottom: 8px;
  padding-left: 5px;
  padding-right: 5px;
}

#aqcjwvvcdh .gt_first_summary_row {
  padding-top: 8px;
  padding-bottom: 8px;
  padding-left: 5px;
  padding-right: 5px;
  border-top-style: solid;
  border-top-width: 2px;
  border-top-color: #D3D3D3;
}

#aqcjwvvcdh .gt_grand_summary_row {
  color: #333333;
  background-color: #FFFFFF;
  text-transform: inherit;
  padding-top: 8px;
  padding-bottom: 8px;
  padding-left: 5px;
  padding-right: 5px;
}

#aqcjwvvcdh .gt_first_grand_summary_row {
  padding-top: 8px;
  padding-bottom: 8px;
  padding-left: 5px;
  padding-right: 5px;
  border-top-style: double;
  border-top-width: 6px;
  border-top-color: #D3D3D3;
}

#aqcjwvvcdh .gt_striped {
  background-color: rgba(128, 128, 128, 0.05);
}

#aqcjwvvcdh .gt_table_body {
  border-top-style: solid;
  border-top-width: 2px;
  border-top-color: #D3D3D3;
  border-bottom-style: solid;
  border-bottom-width: 2px;
  border-bottom-color: #D3D3D3;
}

#aqcjwvvcdh .gt_footnotes {
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

#aqcjwvvcdh .gt_footnote {
  margin: 0px;
  font-size: 90%;
  padding: 4px;
}

#aqcjwvvcdh .gt_sourcenotes {
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

#aqcjwvvcdh .gt_sourcenote {
  font-size: 90%;
  padding: 4px;
}

#aqcjwvvcdh .gt_left {
  text-align: left;
}

#aqcjwvvcdh .gt_center {
  text-align: center;
}

#aqcjwvvcdh .gt_right {
  text-align: right;
  font-variant-numeric: tabular-nums;
}

#aqcjwvvcdh .gt_font_normal {
  font-weight: normal;
}

#aqcjwvvcdh .gt_font_bold {
  font-weight: bold;
}

#aqcjwvvcdh .gt_font_italic {
  font-style: italic;
}

#aqcjwvvcdh .gt_super {
  font-size: 65%;
}

#aqcjwvvcdh .gt_footnote_marks {
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
package::function(data, column_name) %>%
  package::function() %>%
  package::function() %>%
  package::function(n)
```

</br>

**Actual Instructions**

```r
dplyr::group_by(df, species) %>%
  dplyr::tally() %>%
  dplyr::ungroup() %>%
  dplyr::arrange(n)
```


### Get the unique values and their frequency within a column while ordering from the largest value

```{=html}
<div id="sqbfgidjou" style="overflow-x:auto;overflow-y:auto;width:auto;height:auto;">
<style>html {
  font-family: -apple-system, BlinkMacSystemFont, 'Segoe UI', Roboto, Oxygen, Ubuntu, Cantarell, 'Helvetica Neue', 'Fira Sans', 'Droid Sans', Arial, sans-serif;
}

#sqbfgidjou .gt_table {
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

#sqbfgidjou .gt_heading {
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

#sqbfgidjou .gt_title {
  color: #FFFFFF;
  font-size: 125%;
  font-weight: initial;
  padding-top: 4px;
  padding-bottom: 4px;
  border-bottom-color: #FFFFFF;
  border-bottom-width: 0;
}

#sqbfgidjou .gt_subtitle {
  color: #FFFFFF;
  font-size: 85%;
  font-weight: initial;
  padding-top: 0;
  padding-bottom: 6px;
  border-top-color: #FFFFFF;
  border-top-width: 0;
}

#sqbfgidjou .gt_bottom_border {
  border-bottom-style: solid;
  border-bottom-width: 2px;
  border-bottom-color: #D3D3D3;
}

#sqbfgidjou .gt_col_headings {
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

#sqbfgidjou .gt_col_heading {
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

#sqbfgidjou .gt_column_spanner_outer {
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

#sqbfgidjou .gt_column_spanner_outer:first-child {
  padding-left: 0;
}

#sqbfgidjou .gt_column_spanner_outer:last-child {
  padding-right: 0;
}

#sqbfgidjou .gt_column_spanner {
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

#sqbfgidjou .gt_group_heading {
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

#sqbfgidjou .gt_empty_group_heading {
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

#sqbfgidjou .gt_from_md > :first-child {
  margin-top: 0;
}

#sqbfgidjou .gt_from_md > :last-child {
  margin-bottom: 0;
}

#sqbfgidjou .gt_row {
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

#sqbfgidjou .gt_stub {
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

#sqbfgidjou .gt_summary_row {
  color: #333333;
  background-color: #FFFFFF;
  text-transform: inherit;
  padding-top: 8px;
  padding-bottom: 8px;
  padding-left: 5px;
  padding-right: 5px;
}

#sqbfgidjou .gt_first_summary_row {
  padding-top: 8px;
  padding-bottom: 8px;
  padding-left: 5px;
  padding-right: 5px;
  border-top-style: solid;
  border-top-width: 2px;
  border-top-color: #D3D3D3;
}

#sqbfgidjou .gt_grand_summary_row {
  color: #333333;
  background-color: #FFFFFF;
  text-transform: inherit;
  padding-top: 8px;
  padding-bottom: 8px;
  padding-left: 5px;
  padding-right: 5px;
}

#sqbfgidjou .gt_first_grand_summary_row {
  padding-top: 8px;
  padding-bottom: 8px;
  padding-left: 5px;
  padding-right: 5px;
  border-top-style: double;
  border-top-width: 6px;
  border-top-color: #D3D3D3;
}

#sqbfgidjou .gt_striped {
  background-color: rgba(128, 128, 128, 0.05);
}

#sqbfgidjou .gt_table_body {
  border-top-style: solid;
  border-top-width: 2px;
  border-top-color: #D3D3D3;
  border-bottom-style: solid;
  border-bottom-width: 2px;
  border-bottom-color: #D3D3D3;
}

#sqbfgidjou .gt_footnotes {
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

#sqbfgidjou .gt_footnote {
  margin: 0px;
  font-size: 90%;
  padding: 4px;
}

#sqbfgidjou .gt_sourcenotes {
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

#sqbfgidjou .gt_sourcenote {
  font-size: 90%;
  padding: 4px;
}

#sqbfgidjou .gt_left {
  text-align: left;
}

#sqbfgidjou .gt_center {
  text-align: center;
}

#sqbfgidjou .gt_right {
  text-align: right;
  font-variant-numeric: tabular-nums;
}

#sqbfgidjou .gt_font_normal {
  font-weight: normal;
}

#sqbfgidjou .gt_font_bold {
  font-weight: bold;
}

#sqbfgidjou .gt_font_italic {
  font-style: italic;
}

#sqbfgidjou .gt_super {
  font-size: 65%;
}

#sqbfgidjou .gt_footnote_marks {
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
    <tr><td class="gt_row gt_left">Method to get all unique values and ordering their frequency from largest to smallest within a single column of a dataframe</td>
<td class="gt_row gt_right"><svg aria-hidden="true" role="img" viewBox="0 0 512 512" style="height:2em;width:2em;vertical-align:-0.125em;margin-left:auto;margin-right:auto;font-size:inherit;fill:#A62014;overflow:visible;position:relative;"><path d="M330.67 263.12V173.4l-52.75-24.22C219.44 218.76 197.58 400 56 400a56 56 0 0 0 0 112c212.64 0 370.65-122.87 419.18-210.34l-37.05-38.54zm131.09-128.37C493.92 74.91 477.18 26.48 458.62 3a8 8 0 0 0-11.93-.59l-22.9 23a8.06 8.06 0 0 0-.89 10.23c6.86 10.36 17.05 35.1-1.4 72.32A142.85 142.85 0 0 0 364.34 96c-28 0-54 8.54-76.34 22.59l74.67 34.29v78.24h89.09L506.44 288c3.26-12.62 5.56-25.63 5.56-39.31a154 154 0 0 0-50.24-113.94z"/></svg><svg aria-hidden="true" role="img" viewBox="0 0 512 512" style="height:2em;width:2em;vertical-align:-0.125em;margin-left:auto;margin-right:auto;font-size:inherit;fill:#9FC2B9;overflow:visible;position:relative;"><path d="M330.67 263.12V173.4l-52.75-24.22C219.44 218.76 197.58 400 56 400a56 56 0 0 0 0 112c212.64 0 370.65-122.87 419.18-210.34l-37.05-38.54zm131.09-128.37C493.92 74.91 477.18 26.48 458.62 3a8 8 0 0 0-11.93-.59l-22.9 23a8.06 8.06 0 0 0-.89 10.23c6.86 10.36 17.05 35.1-1.4 72.32A142.85 142.85 0 0 0 364.34 96c-28 0-54 8.54-76.34 22.59l74.67 34.29v78.24h89.09L506.44 288c3.26-12.62 5.56-25.63 5.56-39.31a154 154 0 0 0-50.24-113.94z"/></svg><svg aria-hidden="true" role="img" viewBox="0 0 512 512" style="height:2em;width:2em;vertical-align:-0.125em;margin-left:auto;margin-right:auto;font-size:inherit;fill:#9FC2B9;overflow:visible;position:relative;"><path d="M330.67 263.12V173.4l-52.75-24.22C219.44 218.76 197.58 400 56 400a56 56 0 0 0 0 112c212.64 0 370.65-122.87 419.18-210.34l-37.05-38.54zm131.09-128.37C493.92 74.91 477.18 26.48 458.62 3a8 8 0 0 0-11.93-.59l-22.9 23a8.06 8.06 0 0 0-.89 10.23c6.86 10.36 17.05 35.1-1.4 72.32A142.85 142.85 0 0 0 364.34 96c-28 0-54 8.54-76.34 22.59l74.67 34.29v78.24h89.09L506.44 288c3.26-12.62 5.56-25.63 5.56-39.31a154 154 0 0 0-50.24-113.94z"/></svg></td></tr>
  </tbody>
  
  
</table>
</div>
```

```{=html}
<div id="kpdzahmhtl" style="overflow-x:auto;overflow-y:auto;width:auto;height:auto;">
<style>html {
  font-family: -apple-system, BlinkMacSystemFont, 'Segoe UI', Roboto, Oxygen, Ubuntu, Cantarell, 'Helvetica Neue', 'Fira Sans', 'Droid Sans', Arial, sans-serif;
}

#kpdzahmhtl .gt_table {
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

#kpdzahmhtl .gt_heading {
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

#kpdzahmhtl .gt_title {
  color: #FFFFFF;
  font-size: 125%;
  font-weight: initial;
  padding-top: 4px;
  padding-bottom: 4px;
  border-bottom-color: #FFFFFF;
  border-bottom-width: 0;
}

#kpdzahmhtl .gt_subtitle {
  color: #FFFFFF;
  font-size: 85%;
  font-weight: initial;
  padding-top: 0;
  padding-bottom: 6px;
  border-top-color: #FFFFFF;
  border-top-width: 0;
}

#kpdzahmhtl .gt_bottom_border {
  border-bottom-style: solid;
  border-bottom-width: 2px;
  border-bottom-color: #D3D3D3;
}

#kpdzahmhtl .gt_col_headings {
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

#kpdzahmhtl .gt_col_heading {
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

#kpdzahmhtl .gt_column_spanner_outer {
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

#kpdzahmhtl .gt_column_spanner_outer:first-child {
  padding-left: 0;
}

#kpdzahmhtl .gt_column_spanner_outer:last-child {
  padding-right: 0;
}

#kpdzahmhtl .gt_column_spanner {
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

#kpdzahmhtl .gt_group_heading {
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

#kpdzahmhtl .gt_empty_group_heading {
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

#kpdzahmhtl .gt_from_md > :first-child {
  margin-top: 0;
}

#kpdzahmhtl .gt_from_md > :last-child {
  margin-bottom: 0;
}

#kpdzahmhtl .gt_row {
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

#kpdzahmhtl .gt_stub {
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

#kpdzahmhtl .gt_summary_row {
  color: #333333;
  background-color: #FFFFFF;
  text-transform: inherit;
  padding-top: 8px;
  padding-bottom: 8px;
  padding-left: 5px;
  padding-right: 5px;
}

#kpdzahmhtl .gt_first_summary_row {
  padding-top: 8px;
  padding-bottom: 8px;
  padding-left: 5px;
  padding-right: 5px;
  border-top-style: solid;
  border-top-width: 2px;
  border-top-color: #D3D3D3;
}

#kpdzahmhtl .gt_grand_summary_row {
  color: #333333;
  background-color: #FFFFFF;
  text-transform: inherit;
  padding-top: 8px;
  padding-bottom: 8px;
  padding-left: 5px;
  padding-right: 5px;
}

#kpdzahmhtl .gt_first_grand_summary_row {
  padding-top: 8px;
  padding-bottom: 8px;
  padding-left: 5px;
  padding-right: 5px;
  border-top-style: double;
  border-top-width: 6px;
  border-top-color: #D3D3D3;
}

#kpdzahmhtl .gt_striped {
  background-color: rgba(128, 128, 128, 0.05);
}

#kpdzahmhtl .gt_table_body {
  border-top-style: solid;
  border-top-width: 2px;
  border-top-color: #D3D3D3;
  border-bottom-style: solid;
  border-bottom-width: 2px;
  border-bottom-color: #D3D3D3;
}

#kpdzahmhtl .gt_footnotes {
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

#kpdzahmhtl .gt_footnote {
  margin: 0px;
  font-size: 90%;
  padding: 4px;
}

#kpdzahmhtl .gt_sourcenotes {
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

#kpdzahmhtl .gt_sourcenote {
  font-size: 90%;
  padding: 4px;
}

#kpdzahmhtl .gt_left {
  text-align: left;
}

#kpdzahmhtl .gt_center {
  text-align: center;
}

#kpdzahmhtl .gt_right {
  text-align: right;
  font-variant-numeric: tabular-nums;
}

#kpdzahmhtl .gt_font_normal {
  font-weight: normal;
}

#kpdzahmhtl .gt_font_bold {
  font-weight: bold;
}

#kpdzahmhtl .gt_font_italic {
  font-style: italic;
}

#kpdzahmhtl .gt_super {
  font-size: 65%;
}

#kpdzahmhtl .gt_footnote_marks {
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
package::function(data, column_name) %>%
  package::function() %>%
  package::function() %>%
  package::function(function(n))
```

</br>

**Actual Instructions**

```r
dplyr::group_by(df, species) %>%
  dplyr::tally() %>%
  dplyr::ungroup() %>%
  dplyr::arrange(desc(n))
```


## Multiple Columns

