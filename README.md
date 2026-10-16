# Task16-Selecting-Rows-and-Columns-with-loc-and-iloc- 

ting rows and columns in a Pandas DataFrame using label-based selection (`loc[]`) and position-based selection (`iloc[]`).

## Tools Used
- Python
- Pandas
- Google Colab / Jupyter Notebook

## Dataset
A small student dataset is created for practice.

| Name | Age | Marks |
|---|---:|---:|
| Ravi | 18 | 85 |
| Priya | 19 | 92 |
| Rahul | 18 | 78 |
| Sneha | 20 | 95 |
| Arjun | 19 | 88 |


data = {
    "Name": ["Ravi", "Priya", "Rahul", "Sneha", "Arjun"],
    "Age": [18, 19, 18, 20, 19],
    "Marks": [85, 92, 78, 95, 88]
}

df = pd.DataFrame(data)
print(df)

# loc[] examples
print(df.loc[0])                         # Select row with label 0
print(df.loc[:, "Name"])                 # Select the Name column
print(df.loc[1, "Marks"])                 # Select Priya's marks
print(df.loc[1:3])                       # Select labels 1 through 3 (inclusive)
print(df.loc[0:2, ["Name", "Marks"]])    # Select rows and chosen columns

# iloc[] examples
print(df.iloc[0])                        # Select first row by position
print(df.iloc[:, 0])                     # Select first column by position
print(df.iloc[1, 2])                     # Select second row, third column
print(df.iloc[1:4])                      # Select positions 1 through 3
print(df.iloc[0:3, [0, 2]])              # Select first 3 rows, Name and Marks
```

## Difference Between `loc[]` and `iloc[]`

| Feature | `loc[]` | `iloc[]` |
|---|---|---|
| Selection method | Uses row/column labels | Uses integer positions |
| Example | `df.loc[1, "Marks"]` | `df.iloc[1, 2]` |
| Slice endpoint | Included | Excluded |
| Column selection | Column name, e.g. `"Name"` | Column position, e.g. `0` |

## Key Learnings
- `loc[]` is used for label-based selection.
- `iloc[]` is used for integer-position-based selection.
- `:` selects all rows or columns along that axis.
- `loc[]` includes the ending label in slices, while `iloc[]` excludes the ending position.
- Both methods can select rows and columns together.

## How to Run
1. Open Google Colab or Jupyter Notebook.
2. Create a new notebook.
3. Copy the code examples into a cell and run it.
4. Save the notebook as `Selecting_Rows_Columns_loc_iloc.ipynb`.

## Repository Name
`pandas-loc-iloc-selection`

