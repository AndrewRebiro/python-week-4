# python-week-4
def modify_content(content):
    # Example modification: Convert content to uppercase
    return content.upper()

try:
    
    input_filename = input("Enter the name of the file to read from: ")
    with open(input_filename, "r") as infile:
        original_content = infile.read()

    
    modified_content = modify_content(original_content)

  
    output_filename = input("Enter the name of the file to write the modified content to: ")

    
    with open(output_filename, "w") as outfile:
        outfile.write(modified_content)

    print(f"File has been modified and saved as '{output_filename}'.")

except FileNotFoundError:
    print("❌ Error: The file you entered was not found.")
except IOError:
    print("❌ Error: There was a problem reading or writing the file.")
except Exception as e:
    print(f"❌ An unexpected error occurred: {e}")
