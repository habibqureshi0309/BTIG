Overview
AgGridtoPdf is a Node.js module designed to streamline Ag-Grid data export to PDF with advanced customization options. This module offers a seamless integration for users seeking to enhance their Ag-Grid export functionality with features such as grouping, aggregation, styling, and more.

Installation
To integrate AgGridtoPdf into your project, install it via npm:

bash
npm install btig
Usage
Import the AgGridtoPdf component and pass it to the onFirstDataRendered prop of your AgGridReact component:

javascript:
import React from 'react';
import { AgGridReact } from 'ag-grid-react';
import AgGridtoPdf from 'btig';

const MyAgGridComponent = () => {
  return (
    <div>
      {/* Pass AgGridtoPdf component to onFirstDataRendered prop */}
      <AgGridReact
        onFirstDataRendered={AgGridtoPdf}
      />
    </div>
  );
};

export default MyAgGridComponent;

Features
1. Add Filters Button
Upon integration, a button is provided to seamlessly add filters to your Ag-Grid export functionality.

2. Filters Modal
Clicking the "Add Filters" button opens a modal with the following customization options:

Group By:
Multiselect dropdown listing all columns of the Ag-Grid table.
Users can select multiple columns to apply group-by in the exported PDF.

Aggregate Values By:
Multiselect dropdown listing all columns of the Ag-Grid table.
Checkbox options for Sum, Average, Count.
Selected checkboxes apply corresponding filters in the exported PDF.

Body Text-Wrapping:
Enables text wrapping in the exported PDF, ensuring content is displayed inline.

Customized Header and Footer:
Users can add a heading or logo to the header and footer sections.

Font and Font Color:
Customize font size, font style, and font color for the exported PDF.

Number Formatting:
Select number formatting style for the exported result.

Date Formatting:
Select date formatting style for the exported result.

Coloring Based on Groups and Aggregated Values:
Choose specific colors to apply on rows based on groups and aggregated values.

3. Export PDF
Default Formatting:
Set default formatting settings for the exported result.

After implementing all the filters, find the "Export PDF" button at the bottom of the modal. Clicking this button will generate and download a PDF, applying all the selected filters to the datatable data.

Example
javascript
import React from 'react';
import { AgGridReact } from 'ag-grid-react';
import AgGridtoPdf from 'btig';

const MyAgGridComponent = () => {
  return (
    <div>
      {/* Pass AgGridtoPdf component to onFirstDataRendered prop */}
      <AgGridReact
        onFirstDataRendered={AgGridtoPdf}
      />
    </div>
  );
};

export default MyAgGridComponent;


License
This project is licensed under the MIT License - see the LICENSE file for details.

Acknowledgments
Special thanks to the developers who contributed to this module and the Ag-Grid community for their ongoing support.