# route-planner

Finds the best route on a road map: the fastest way to drive somewhere, or a mixed route where you drive part of the way, park, and walk the rest.

## What it does

Reads a road network from CSV files and computes optimal routes over it:

- **Driving-only** — the fastest route between two points.
- **Driving + walking** — drive, park, and walk the last stretch, within a maximum walking time you set.
- **Restrictions** — avoid specific locations or streets, force a route through a mandatory stop, or cap the total walking time.

It uses a custom graph with a `MutablePriorityQueue` for the shortest-path search.

## Stack

C++ with the STL, built with CMake. Road and location data in CSV.

## How to run

```bash
mkdir build && cd build
cmake .. && make
./main        # then choose options from the menu
```

## What I built

Group project (group G155) for the Algorithm Design course (2024/25), built through pair programming — we worked together and the commits landed on a teammate's repository, so the git history here does not split cleanly by author. My contribution is in the routing and graph code alongside my teammates.

## What I would do differently

Separate the route-search algorithms from the menu and I/O so they can be unit-tested directly, and add a small benchmark over the larger datasets to compare the driving-only and driving-plus-walking searches.
