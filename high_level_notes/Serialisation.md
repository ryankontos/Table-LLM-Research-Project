# Serialisation for Table Processing in LLMs

## Introduction
Serialisation is the process of converting tables into a linear, text-based format that can be easily understood by Large Language Models (LLMs). Since LLMs are typically better at processing sequential text rather than two-dimensional tables, serialisation helps by flattening the table data into a format the model can handle more effectively.

There are 3 main serialisation methods:

## 1. Row-Wise

In row-wise serialisation, you take each row of the table and convert it into a single line of text. The values in the row are connected with a separator, like a comma, pipe (`|`), or colon (`:`).

### Example
Consider this table:

| First Name | Last Name   | Status |
|------------|-------------|--------|
| Ryan       | Kontos      | Student|
| Diego      | Molla-Aliod | Staff  |

**Serialised Row-Wise:**

- `First Name: Ryan | Last Name: Kontos | Status: Student`
- `First Name: Diego | Last Name: Molla-Aliod | Status: Staff`

Here, each row becomes a single line of text. This method is easy for LLMs to process because it mimics the natural flow of sentences.

### When to Use It
Rw-wise serialisation is helpful when the relationship between the values in each row is important.

## 2. Column-Wise Serialisation

### What It Is
In column-wise serialisation, you process each column separately, listing all the values in one column together before moving on to the next column.

### Example
Using the same table:

| First Name | Last Name   | Status |
|------------|-------------|--------|
| Ryan       | Kontos      | Student|
| Diego      | Molla-Aliod | Staff  |

**Serialised Column-Wise:**

- `First Name: Ryan, Diego`
- `Last Name: Kontos, Molla-Aliod`
- `Status: Student, Staff`

Each column’s data is grouped together. This approach is useful when you want to focus on comparing or analysing data within a single column.

### When to Use It
Column-wise serialisation is ideal when you need to compare or analyse data in one column, like comparing first names, last names, or statuses.

## 3. Cell-Wise Serialisation

### What It Is
Cell-wise serialisation breaks the table down into individual cells, with each cell’s data linked to its specific row and column.

### Example
Using the same table:

| First Name | Last Name   | Status |
|------------|-------------|--------|
| Ryan       | Kontos      | Student|
| Diego      | Molla-Aliod | Staff  |

**Serialised Cell-Wise:**

- `Cell(1,1): First Name: Ryan | Cell(1,2): Last Name: Kontos | Cell(1,3): Status: Student`
- `Cell(2,1): First Name: Diego | Cell(2,2): Last Name: Molla-Aliod | Cell(2,3): Status: Staff`

Each cell is identified by its position in the table. This method provides the most detail and keeps the table’s structure clear.

### When to Use It
Cell-wise serialisation is best for preserving the exact structure of the table, like when dealing with complex tables that might have merged cells or specific layouts.

## Conclusion

Serialisation is very effective at making tables easier for LLMs to process. The method depends on specific needs. Row-wise is simple and straightforward, column-wise is good for comparisons, and cell-wise keeps the most detail.