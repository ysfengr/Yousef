# Task 01 Solution - Yousef

error_count = 0

# Open both files using 'with' for safe handling
with open('server_log.txt', 'r') as source_log, open('errors_only.txt', 'w') as error_file:
    
    # Process the file line by line
    for line in source_log:
        # Check if the line is an error entry
        if line.startswith('ERROR'):
            error_file.write(line)
            error_count += 1 # Increment the counter
            
print(f"Total Errors Found: {error_count}")
