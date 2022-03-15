# Relation Inference Among Sensor Time Series With Neural Networks In The Frequency Domain

In this project, we focus on analyzing time-series data observed at the sensors in order to understand their spatial relationships. CNN is deployed in order to encode the similarity. Our network takes time-series triplets transformed via the Short-time Fourier Transform (STFT) as an input. The deep metric neural network outputs a one dimensional tensor that encodes the relatedness among the time series. These output tensors are used for determining which room a sensor is located in, followed with an approximate min k-cut algorithm. To summarize, we aim to ﬁnd which sensors are co-located in the same physical space, exercising the spatial relationship component of their relation inference.

## Structure of the project
```
├── README.md
├── GenericAlgorithm
│   ├── README.md
│   ├── setup.py
│   ├── pk_rooms.json
│   ├── k_rooms.json
│   ├── corr.mat
│   ├── all_rooms.json
│   ├── configs
│   │   └── sizes_grid_search
│   ├── colocation
│   │   ├── __init__.py
│   │   ├── run.py
│   │   ├── utils
│   │   ├── tasks
│   │   ├── optimizers
│   │   ├── data_loader
│   │   └── core
│   └── analyze_output
│       ├── accurate_room_pattern.py
│       ├── all_consecutive_rooms.py 
│       ├── replace_room_id_with_original.py
│       └── __output__
│
├── losses
│   ├── __init__.py
│   └── loss.py
│
├── models
│   ├── __init__.py
│   └── stn.py
│
├── utils
│   ├── util.py
│   └── stn.py
│
├── 10_rooms.json
├── Data.py
├── Try.py
├── loss.py
├── main.py
└── stn.yaml
```

## Usage
You can run this project using following command:
```
python main.py
```
