# Quick Start Guide

## Prerequisites
- Java 11+ installed
- Git (for cloning and submitting)

## Getting Started (5 minutes)

### 1. Clone the Repository
```bash
git clone <your-repo-url>
cd assignment4-graph-algorithms
```

### 2. Build the Project
```bash
./build.sh
```

### 3. Generate Test Datasets
```bash
./generate_datasets.sh
```

### 4. Run on Sample Data
```bash
./run.sh data/tasks.json
```

## Quick Commands

| Command | Description |
|---------|-------------|
| `./build.sh` | Compile all Java source files |
| `./generate_datasets.sh` | Generate 9 test datasets |
| `./run.sh [dataset]` | Run on specific dataset |
| `./check_submission.sh` | Verify submission is complete |

## Run Examples

```bash
# Run on provided dataset
./run.sh data/tasks.json

# Run on small DAG
./run.sh data/small_dag.json

# Run on large complex graph
./run.sh data/large_complex.json
```

## What You'll See

The program outputs:
1. **SCC Analysis** - Strongly connected components found
2. **Condensation Graph** - Compressed DAG representation
3. **Topological Sort** - Valid processing order
4. **Shortest Paths** - Optimal paths from source
5. **Longest Paths** - Critical path identification
6. **Performance Metrics** - Timing and operation counts

## Project Structure at a Glance

```
assignment4-graph-algorithms/
├── src/main/java/
│   ├── Main.java                    # Run this
│   ├── DatasetGenerator.java        # Generate datasets
│   └── graph/
│       ├── scc/                     # SCC algorithms
│       ├── topo/                    # Topological sort
│       ├── dagsp/                   # DAG shortest/longest path
│       └── utils/                   # Graph utilities
├── data/                            # 10 test datasets
├── README.md                        # Full documentation
└── *.sh                             # Helper scripts
```

## Testing

The implementation includes:
- ✅ 3 JUnit test classes
- ✅ 25+ test cases
- ✅ Edge case coverage
- ✅ Performance instrumentation

## Algorithms Implemented

| Algorithm | Complexity | File |
|-----------|------------|------|
| Tarjan's SCC | O(V + E) | `TarjanSCC.java` |
| Kosaraju's SCC | O(V + E) | `KosarajuSCC.java` |
| Kahn's Topological Sort | O(V + E) | `TopologicalSort.java` |
| DFS Topological Sort | O(V + E) | `TopologicalSort.java` |
| DAG Shortest Path | O(V + E) | `DAGShortestPath.java` |
| DAG Longest Path | O(V + E) | `DAGShortestPath.java` |

## Troubleshooting

### Compilation Error
```bash
# Make sure Java is installed
java -version

# Rebuild
rm -rf bin/
./build.sh
```

### Missing Datasets
```bash
./generate_datasets.sh
```

### Permission Denied
```bash
chmod +x *.sh
```

## Next Steps

1. **Read** the full [README.md](README.md) for detailed documentation
2. **Review** [EXPERIMENT_RESULTS.md](EXPERIMENT_RESULTS.md) for performance analysis
3. **Check** [data/DATASETS.md](data/DATASETS.md) for dataset descriptions
4. **Run** `./check_submission.sh` to verify everything

## Support

For issues:
1. Check README.md
2. Review code comments (Javadoc)
3. Run check_submission.sh for diagnostics

---

**Time to get started:** ~5 minutes  
**Time to understand:** ~30 minutes  
**Time to master:** Review the code! 🚀
