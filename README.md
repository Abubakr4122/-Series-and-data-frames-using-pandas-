# -Series-and-data-frames-using-pandas-
15. Series and data frames using pandas 
import pandas as pd
data = {
    'Name': ['Alice', 'Bob', 'Charlie', 'David'],
    'Age': [25, 30, 35, 40],
    'Score': [85, 90, 95, 80]}
df = pd.DataFrame(data)
sorted_df = df.sort_values('Age', ascending=True)
multi_sorted_df = df.sort_values(['Score', 'Age'])
indexed_df = df.set_index('Name')
reset_df = indexed_df.reset_index()
print("Original DataFrame:\n", df, "\n")
print("Sorted by Age:\n", sorted_df, "\n")
print("Sorted by Score then Age:\n", multi_sorted_df, "\n")
print("DataFrame with Name as index:\n", indexed_df, "\n")
print("Reset index:\n", reset_df, "\n")
Output: 
Original DataFrame:
     Name  Age  Score
0  Alice   25     85
1    Bob   30     90
2 Charlie   35     95
3  David   40     80
Sorted by Age:
     Name  Age  Score
0  Alice   25     85
1    Bob   30     90
2 Charlie   35     95
3  David   40     80
Sorted by Score then Age:
     Name  Age  Score
3  David   40     80
0  Alice   25     85
1    Bob   30     90
2 Charlie   35     95
DataFrame with Name as index:
     Name  Age  Score            
Alice     25     85
Bob       30     90
Charlie   35     95
David     40     80
Reset index:
     Name  Age  Score
0  Alice   25     85
1    Bob   30     90
2 Charlie   35     95
3  David   40     80

