Pagination (Angular)
===
Simple-2-use custom made pagination component for angular.

Installation
====
Install rg-pagination-lib with npm:
```
$ npm install --save rg-pagination-lib
```

Usage
===
```
<rg-pagination
  [currentPage]="currentPage"
  [count]="count"
  [perPage]="perPage"
  [pagesToShow]="pagesToShow"
  [itemsPerPageList]="itemsPerPageList"
  [selectedItemPerPage]="selectedItemPerPage"
  (goPrev)="goToPrev()"
  (goNext)="goToNext()"
  (goToItemPerPage)="goToItemPerPage($event)"
></rg-pagination>

```
Steps to Follow 
===
1. Add below link in ```index.html``` file.
```
 <link
  rel="stylesheet"
  href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/4.7.0/css/font-awesome.min.css"
/>
```
2. Import ```rg-pagination-lib``` module in ```app.module.ts``` file.
```
import { RgPaginationLibModule } from 'rg-pagination-lib';
```
3. In ```app.component.html``` , add the following 

```
<rg-pagination
  [currentPage]="currentPage"
  [count]="count"
  [perPage]="perPage"
  [pagesToShow]="pagesToShow"
  [itemsPerPageList]="itemsPerPageList"
  [selectedItemPerPage]="selectedItemPerPage"
  (goPrev)="goToPrev()"
  (goNext)="goToNext()"
  (goToItemPerPage)="goToItemPerPage($event)"
></rg-pagination>
```
4. In ```app.component.ts``` , add the following 

```
export class AppComponent {
  public currentPage = 1; 
  public count = 100; 
  public perPage = 1; 
  public pagesToShow = 1; 
  public selectedItemPerPage;
  public itemsPerPageList = [10, 20, 50, 100, 500]; //default value
  title = 'lib-tester';
  goToItemPerPage(event) {
    this.selectedItemPerPage = event;
  }
  goToPrev() {
      console.log('IN Previous');
  }
  goToNext() {
      console.log('IN Next');

  }
}
```
5. Final Result looks like 

![Look of rg-pagination](https://github.com/renu0627/rg-pagination-lib/blob/master/src/assets/rg-pagination.png)


Params
===

 Name| Type | Description
------------ | ------------- | -------------
currentPage | Number | Shows which page is currently opened from PageList
count | Number | Shows Total Count of items present 
pagesToShow | Number | Shows PageList derived from ```selectedItemPerPage``` and ```count```
itemsPerPageList | Number [] | Shows List of Items Per Page
selectedItemPerPage | Number | Shows selected Items Per Page
goPrev | fn() | Click on Previous Arrow will call this function
goNext | fn() | Click on Next Arrow will call this function
goToItemPerPage | fn() | Click on ItemsPerPage List will call this function 


Happy Coding ! :stuck_out_tongue_closed_eyes:
===