# Dictionary-Mapper
"Dictionary Mapper" that allows users to create a new dictionary by copying values from the initial dictionary based on specific paths and mappings provided as input. 
# Project Description:
The "Dictionary Mapper" project will include a Python script that takes an initial dictionary, a list of paths, and a dictionary of mappings as inputs, and generates a new dictionary based on the specified paths and mappings. The script will be designed to handle any type of key or list and generate a new dictionary of nested dictionaries and lists.

The program will first validate the input parameters to ensure that they are in the correct format. It will then iterate through the paths and mappings to copy the values from the initial dictionary into a new dictionary based on the specified mappings.

The code will be well-documented and include inline comments to ensure that other developers can understand the code's functionality and modify it as necessary. Additionally, the code will be unit-tested to ensure that it works as expected.

The project will be published on GitHub under an open-source license. The repository will include a README file that provides an overview of the project, instructions on how to use the script, and information on how to contribute to the project.

# Benefits:
The "Dictionary Mapper" project will provide a useful tool for developers who need to manipulate nested dictionaries and lists. By providing a generic solution that can handle any type of key or list, this project will save developers time and effort in writing custom code to handle specific use cases.

Publishing the project on GitHub will also allow other developers to contribute to the project, suggest improvements, and report issues. This collaborative approach will help to ensure that the project remains up-to-date and relevant.

# Conclusion:
We believe that the "Dictionary Mapper" project will be a valuable tool for developers who need to manipulate nested dictionaries and lists. By publishing the project on GitHub, we hope to encourage collaboration and contribute to the open-source community.


# Mapper
This script allows you to map values from a given dictionary to a new dictionary based on a set of mappings and paths.

# Requirements
This script requires Python 3.x to be installed.

# Installation
Clone the repository to your local machine using git clone https://github.com/Hamara-Jillo/Dictionary-Mapper/
Navigate to the root directory of the project.
Install the required dependencies using pip install -r requirements.txt
#Usage
The Mapper class is initialized with the following parameters:

input_dict: The dictionary containing the input values to be mapped
mappings: A dictionary containing the mappings of keys from the input dictionary to keys in the output dictionary
paths: A list of paths to search for in the input dictionary, where * can be used as a wildcard for any key
To use the Mapper class, create an instance with the required parameters and call the map() method. This will return a new dictionary with the mapped values.

# Example usage:
import Mapper

input_dict = {
    "user": {
        "name": "John",
        "age": 30,
        "email": "john@example.com",
        "address": {
            "street": "123 Main St",
            "city": "Anytown",
            "state": "CA",
            "zip": "12345"
        }
    },
    "products": [
        {
            "name": "Product 1",
            "price": 10.99
        },
        {
            "name": "Product 2",
            "price": 5.99
        }
    ]
}

maps = {
    "user.name": "user.full_name",
    "user.address.street": "address.street",
}

pths = [["user.name" ],["user.address.street"]]

mapper = Mapper(input_dict, mappings, paths)
output_dict = mapper.map()

print(output_dict)
# Output:
{'user': {'full_name': 'John'}, 'address': {'street': '123 Main St'}}

# License
This project is licensed under the MIT License - see the LICENSE file for details.
