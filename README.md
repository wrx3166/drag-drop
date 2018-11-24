# drag-drop
It can to drag and drop more or single row，drag-drop plugin for jquery datatable 
get start
import drag-drop.js file to your page



let selector = '#tableId';
let dragDroppable = new TableDragAndDrop(selector, testData, table);
Drag-drop-datatable
This is drag-drop plugin for datatable 
We can to drog and drop siggle row or more rows on datatable 
There is one point we should to pay more attentions 


'createdRow': function (row, data, dataIndex) {
     $(row).attr('category', data.category);
         if (data.category == "A") {
             $(row).attr('draggable', true);
          }
      }
      
As the code writed ,drag-drap single row or more rows is based on category properties 
IF all of the rows are same category, we only can drag-drop single row 
IF some rows category properties are "A" and some rows category properties are "B",so we think category "B" rows Are belong to category "A" rows,so we can drag-drop more rows 
