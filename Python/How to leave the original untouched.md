import shutil

# Define the source file and the destination file
source_file = 'datasets/car-sales.csv'
destination_file = 'datasets/car-sales-copy.csv'

# Copy the file
shutil.copyfile(source_file, destination_file)

Python
import shutil
import pandas as pd

# Copy the file (Step 1)
source_file = 'datasets/car-sales.csv'
destination_file = 'datasets/car-sales-copy.csv'
shutil.copyfile(source_file, destination_file)

# Read the copy (Step 2)
df = pd.read_csv('datasets/car-sales-copy.csv')

# Make changes (Step 3)
df['Price'] = df['Price'] * 1.1  # Increase all prices by 10%

# Save the changes (Step 4)
df.to_csv('datasets/car-sales-copy.csv', index=False)