# LEADS MANAGEMENT REPLICA [v.charlie]
**Author**: Elwood Berry  
**Company**: Antera Software USA, Inc.  

---  

## Summary  
AUG 2nd, 2021  
  
**The Expanded Row Approach**  
Our only concern is:
1. Adding the container with a placeholder for other components.
2. Ability to access the click event of the row to enable the expanded row.
  
---  
** - versus - **  
---  
  

### INSTALL NEW COMPONENT 
Our goal is to add another component ('expanded-list-view') to the [kanban library](https://github.com/Antera-Software/Antera-libraries/tree/master/libs/kanban/src/lib).
```  
npm i @anterasoftware/angular-material-kanban  
```  


---  

## ADDING TO A COMPONENT  
This is an exercise in adding 'KanbanModule' to a component to leverage its features.  

### MODULE  
**app.module.ts**  
```ts  
// LIBRARIES 
import { KanbanModule } from '@anterasoftware/angular-material-kanban';


@NgModule({
  imports:[
    // other imports ...
    KanbanModule]







--- 


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

**['displayActionsBar']**    
A boolean that is initally set to false.  
```ts  
// some code ....

@Input() public displayActionsBar: boolean = false;  

// more code ....
```  

---  

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

---  


**['dateFormatString']**  
[??WHATISTHIS??](#)  



**['displayedColumns']**  
[??WHATISTHIS??](#)  

**['listDataSource']**. 
[??WHATISTHIS??](#) 






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




# PENDING DELETION...  

### Dependencies  
1. [@angular/material](https://www.npmjs.com/package/@angular/material)
2. [@angular/flex-layout](https://www.npmjs.com/package/@angular/flex-layout) | **See Examples**: [Layout Demos](https://tburleson-layouts-demos.firebaseapp.com/#/docs)



```html  
HTML goes here.
```  

```ts  
'TYPESCRIPT goes here'
```  