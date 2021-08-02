# THE EXPANDED ROW APPROACH
Our only concern is:
1. Adding the container with a placeholder for other components.
2. Ability to access the click event of the row to enable the expanded row.


## The Solution?  


---  

### THE TABLE    
The data table component used for 'list-view'.  

**Data Source** 
Our data source.  

**matSort**  
Directive used by the table to control its sorting.

**Class**  
The 'Selector' that selects the 'mat-elevation-z8' element attribute in the stylesheet.

**ngClass**: 

**['displayActionsBar']**    
A boolean that is initally set to false.  




```html  
<table mat-table 
  [dataSource]="dataSource"  
  matSort (matSortChange)="onListViewSort($event)" 
  class="mat-elevation-z8" 
  [ngClass]="{'fixedHeader': displayActionsBar}" 
  style="width:100%">
</table>
```  

--- 


# THE SELECTOR  


**['dateFormatString']**  
[??WHATISTHIS??](#)  

**['displayActionsBar']**    
A boolean that is initally set to false.  
```ts  
// some code ....

@Input() public displayActionsBar: boolean = false;  

// more code ....
```

**['displayedColumns']**  
[??WHATISTHIS??](#)  

**['listDataSource']**. 
[??WHATISTHIS??](#) 

**['tableLength']**. 
A number.  

**OUTLINE: 'leads-list-new-view.component.ts'**  
```ts  

export class LeadsListNewViewComponent implements OnInit {
  // some code ....

  public tableLength: number = 0; 

  // more code ....

  ngOnInit(): void {

    // A number. The number of leads in the service.
    this.leadsService.onLeadsListCount.subscribe((res) => this.tableLength = res);
  }

  // METHOD: 'ON TABLE SELECTOR CHECKBOX CLICKED'  
  public onTableSelectCheckboxClicked({selectType}) {

  }

}

```




(onSortFired)="onSortClicked($event)" 
(onColumnClick)="onTableClicked($event)"
(selectClicked)="onTableSelectCheckboxClicked($event)"
(onPaginateFire)="onPaginate($event)" 
page="Leads" 

[timeFormatString


```html  
(onSortFired)="onSortClicked($event)" 
            [listDataSource]="leadsTableList" 
            [displayedColumns]="displayColumns" 
            (onColumnClick)="onTableClicked($event)"
            (selectClicked)="onTableSelectCheckboxClicked($event)"
            [tableLength]="tableLength" 
            (onPaginateFire)="onPaginate($event)" 
            page="Leads" 
            [displayActionsBar]="displayActionsBarFlag" 
            [dateFormatString]="authService.dateFormatString" 
            [timeFormatString

```  