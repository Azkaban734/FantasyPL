# Fantasy Premier League Optimization

This project aims to build the most cost-efficient Fantasy Premier League (FPL) team using optimization techniques. The objective is to maximize the total expected points for each week while adhering to various constraints.

## Project Description

The project uses Python and the PuLP library to solve a linear programming problem. The optimization considers several constraints such as budget, player positions, team limits, and player availability.

## Requirements

- Python 3.11.9
- pandas
- pulp

## Installation

To install the required packages, run:
```bash
pip install pandas pulp
```

## Usage

1. **Load Player Data**: The player data is loaded from a CSV file named `fplAnalytics-playerStautsData.csv`. It's acquired from https://www.fplanalytics.com/playerStatus.html. 
2. **Filter Available Players**: Only players with the status 'Available' are considered.
3. **Calculate Cost Effectiveness**: A new column `ppc` (points per cost) is created.
4. **Optimization**: The optimization problem is defined and solved using PuLP.
5. **Output**: The selected players and their positions are printed, along with the total points per game.

## Running the Notebook

To run the notebook, execute the cells in the following order:

1. Import necessary libraries.
2. Load the player data.
3. Filter to only available players.
4. Calculate the `ppc` column.
5. Define and solve the optimization problem.
6. Print the selected players and total points per game.

## Constraints

- Total cost must be less than 100.
- At most 3 players from the same team.
- Players must have played at least 1200 minutes.
- The team must consist of 1 goalkeeper, 3 defenders, 4 midfielders, and 3 forwards.
- The budget for the starting 11 is set to 83.4 to account for cheap bench players.

## License

This project is licensed under the MIT License.
