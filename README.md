# responsive-table-generator

This is a simple python script to generate responsive HTML tables.

# Usage
In your css file, insert the following media query along with any additional styles to the table.
```css
@media screen and (max-width: 906px){
  .responsive-table > thead > tr > th,
  .responsive-table > tbody > tr > th,
  .responsive-table > tfoot > tr > th,
  .responsive-table > thead > tr > td,
  .responsive-table > tbody > tr > td,
  .responsive-table > tfoot > tr > td {
    padding: 1em;
    vertical-align: top;
    border-top: 0;
  }
  
  .responsive-table thead {
    display: none;
  }

  .responsive-table tr {
    margin-bottom: 10px;
    display: block;
  }

  .responsive-table > tbody > tr > td {
    display: block;
    text-align: right;
    font-size: 0.8em;
    vertical-align: bottom;
    border-bottom: 1px solid rgba(0, 0, 0, 0.12);
  }

  .responsive-table td:before{
    content: attr(data-label);
    float: left;
    text-transform: uppercase;
    letter-spacing: 1px;
    font-weight: 600;
    vertical-align: bottom;
    margin-right: 0.5em;
  }
}
```

To generate a table, simply navigate to the script and run the following on the command line:
``` shell
  python gen.py
```
