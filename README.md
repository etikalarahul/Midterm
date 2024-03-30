Rahul reddy etikala "re227"

# Advanced Calculator Application

The Advanced Calculator Application is an advanced Python tool designed to execute various mathematical computations efficiently. It covers fundamental arithmetic operations, statistical analysis, and extends its functionality through dynamically loaded plugins. This guide provides detailed instructions on how to set up, utilize, and contribute to the calculator app.

## Key Features

- **Arithmetic Functions**: Supports basic arithmetic operations such as addition, subtraction, multiplication, and division.
- **Statistical Analysis**: Calculates statistical measures including mean, median, and standard deviation.
- **History Tracking**: Manages a record of calculations allowing users to view, save, clear, or delete history.
- **Plugin Framework**: Enhances functionality by integrating additional operations through plugins.
- **Configuration via Environment Variables**: Customizes behavior using environment variables.

## Setup and Installation

### Prerequisites:

- Python 3.8 or higher
- Pip for package management

### Installation Steps

1. **Clone the Repository**:
   Clone the project from the repository URL to your local machine using `git clone <repository_url>`, then navigate into the project directory.

2. **Virtual Environment**:
   Create a virtual environment to manage project dependencies:
   - **Windows**: Execute `python -m venv env`, then activate the environment with `.\env\Scripts\activate`.
   - **macOS/Linux**: Run `python3 -m venv env`, then activate with `source env/bin/activate`.

3. **Install Dependencies**:
   Install necessary Python packages by executing `pip install -r requirements.txt`.

4. **Environment Configuration**:
   Create a `.env` file in the project root to specify configurations such as `LOG_LEVEL` and `HISTORY_SAVE_PATH`. Detailed instructions are available in the Environment Variables section.

## Usage Instructions

Launch the calculator application via the command line:

```bash
python main.py
Follow the prompts on the command line interface to perform calculations, manage history, or utilize plugins.

For instance, to add operands, enter:

bash
Copy code
add <operand1> <operand2> [<operand3> ...]
Certain operations like log and square require only one operand.

**Supported Operations
Basic Arithmetic: add, subtract, multiply, divide
Statistical Calculations: mean, median, stddev
History Commands: view history, clear history, delete history
Managing History
The HistoryManager class offers functionalities to handle calculation history, which is stored in history.csv within the data folder. Ensure the directory and file are present or can be created by the application.

**Logging
Every operation performed within the app generates a log in operations.log within the logs directory.

**Plugin System
Expand the application's capabilities by adding plugins in the plugins directory. Plugins must adhere to the OperationStrategy interface.

**Environment Variables
Adjust application behavior using the following environment variables in your .env file:

LOG_LEVEL: Specifies the logging level (e.g., INFO, DEBUG).
HISTORY_SAVE_PATH: Defines the path for saving the history file.
ENABLE_HISTORY_FEATURE: Enables or disables history management (True or False).