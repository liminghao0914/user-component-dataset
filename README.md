# user-component-dataset

This is a preliminary dataset of user component states as an assistive statistics for mobile edge computing (MEC), which is used in the published paper, [li2022blockchian](https://ieeexplore.ieee.org/document/9951342g) and will be used in more future works.

# Introduction

Welcome to the user-component-dataset open-source dataset! This dataset is intended for use in [PartFlow](https://github.com/liminghao0914/PartFlow). It contains 85081  items of component states in sequence with timestamps and is released under the [license type, such as "MIT" or "CC BY-SA 4.0"].

# Data Description

The component status data is a discrete sequential structure stored in JSON files. The preliminary dataset will be continuously updated to include more users, devices, and apps. 
We divide the data set by device into these folders. Each folder contains two JSON files, one containing device information and the other consisting of a list of component state data received from the device.

## Data Format

The data is provided in JSON. Each item includes the following fields: ["type", "status", "class", "descipt", "timestamp", "runtime", "uid"].

An example of one item:

    {
      "type": "session",
      "status": "compareDelta",
      "class": "www.littlefoxes.reftime.fragment.RecordFragment$4",
      "descript": "(Ljava/lang/Object;Ljava/lang/Object;)I",
      "timestamp": {
        "$numberLong": "1622026054338"
      },
      "runtime": 9,
      "uid": "0F875EB3F61294A92A9AAD64D92414C8"
    }


# Usage

To use the dataset, simply insert them into MongoDB.

Firstly, install ``mongoimport`` in your environment, which has already installed MongoDB.

For Linux,

    sudo dpkg -l mongodb-database-tools
    
For MacOS,
    
    sudo dpkg -l mongodb-database-tools
    
For Windows, download the MSI installer [here](https://www.mongodb.com/try/download/database-tools?tck=docs_databasetools) and add the toolkits to ``PATH``.


After installation, insert user component data by

    mongoimport --jsonArray --db db --collection [uid] --[uid].json
    
Besides the data log, we are alse required to add devices information to the database.

    mongoimport --jsonArray --db db --collection devices_info --devices_info.json

