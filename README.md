# DmDS
A dual-mode local search algorithm for solving the minimum dominating set problem

## Usage
Please use the following command to execute DmDS： *ds ${graph} ${seed} ${time} ${para}*

- ${graph}： The DIMACS format file must be an undirected, unweighted graph with no self-loops.
- ${seed}: An integer.
- ${time}: Time limit (s).
- ${para}: A parameter in the range 0--100.

### Docker Usage
You can also run DmDS using Docker. Follow these steps to get started:
1. **Pull the Docker Image**
   
`docker pull ghcr.io/your-username/dmds-image:latest`

2. **Run DmDS in Docker**

An Example: `docker run --rm dmds-image /dataset/V100U150_1 1 10 50`
   
Assuming your input file is `instance.dimacs` and located at `/path/to/your/data/` on your local machine, you can run DmDS in a Docker container using the following command:

`docker run --rm -v /path/to/your/data:/dataset ghcr.io/your-username/dmds-image ./dmds /dataset/instance.dimacs 1 10 50`

- **`-v /path/to/your/data:/dataset`**: Mount your local directory (`/path/to/your/data`) to the container’s `/dataset` directory.
- **`./dmds /dataset/instance.dimacs 1 10 50`**: Run the DmDS algorithm with the input file `instance.dimacs` and the specified parameters.


## bibtex
@article{zhu2024dual,
  title={A dual-mode local search algorithm for solving the minimum dominating set problem},
  author={Zhu, Enqiang and Zhang, Yu and Wang, Shengzhi and Strash, Darren and Liu, Chanjuan},
  journal={Knowledge-Based Systems},
  volume={298},
  pages={111950},
  year={2024},
  publisher={Elsevier}
}
