# user-component-dataset

This is a preliminary dataset of user component states, which is used in the published paper, [li2022blockchian](https://ieeexplore.ieee.org/document/9951342g).

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


