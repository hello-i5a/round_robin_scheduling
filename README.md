# CPU Scheduling Algorithm: Round Robin Scheduling

A Python implementation of Round Robin CPU Scheduling with Gantt chart visualization, turnaround, and waiting time calculations.

## Features

- Simulates the Round Robin (RR) algorithm where each process gets a fixed time quantum to execute.
- Displays the process execution timeline with interactive features.
- Shows detailed information for each process, such as arrival time, burst time, waiting time, and turnaround time.
- Automatically calculates and displays average turnaround and waiting times for all processes.

## Explanation of the Code

1. **Process Class**

   The `Process` class is designed to store attributes for each process. These attributes include:

   - **`pid`**: Process ID (e.g., 'A', 'B', 'C').
   - **`arrival_time`**: Time at which the process arrives in the ready queue.
   - **`burst_time`**: Time the process requires for CPU execution.
   - **`remaining_burst_time`**: Tracks how much CPU time is left for the process to complete.
   - **`completion_time`**: The time at which the process finishes execution.
   - **`turnaround_time`**: The total time taken for a process to complete from arrival to completion.
   - **`waiting_time`**: Time the process spends waiting in the ready queue.

2. **`get_user_input()`**:

   - Prompts the user for the **time quantum** and details of each process, such as arrival time and burst time.
   - Returns the time quantum and a list of `Process` objects that represent each process.

3. **`round_robin_scheduling(processes, time_quantum)`**:

   - Implements the **Round Robin Scheduling Algorithm**.
   - Processes are executed in a round-robin manner using a time quantum. If a process does not finish within the time quantum, it is preempted and placed back in the ready queue.
   - Returns the **Gantt chart data**, **average turnaround time**, **average waiting time**, and **a list of executed processes**.

4. **`plot_gantt_chart(gantt_data)`**:

   - Uses Plotly to generate an **interactive Gantt chart** that visualizes the scheduling of processes over time.
   - Displays the start and end times of each process on the chart.

5. **`plot_process_details(executed_processes)`**:

   - Uses Plotly to generate an **interactive table** showing detailed information for each process, including arrival time, burst time, completion time, turnaround time, and waiting time.

6. **`get_user_input()`**

   - **Time Quantum**: The user is first prompted to input the **time quantum** (the maximum time a process can run before being preempted).
   - **Process Details**: The program then asks for the **arrival time** and **burst time** of each process.
   - **Execution**: After all the input is provided, the Round Robin scheduling algorithm runs, and the program displays results in the form of a Gantt chart and a table.

   **Results**: The notebook outputs the following:

   - **Average Turnaround Time** and **Average Waiting Time**.
   - **Interactive Gantt Chart** that visualizes the scheduling of processes.
   - **Process Details Table** showing the detailed statistics of each process.

## Running the Program

1. **Dependencies**

   The project requires the following Python libraries:

   - `pandas`
   - `numpy`
   - `plotly`

   To install these dependencies, use the following command:

   ```bash
   pip install -r requirements.txt
   ```

2. **Running the Notebook**
   - Open the `main.ipynb` notebook in a Jupyter Notebook environment.
   - Run each cell sequentially to execute the program.
   - The program will prompt you to enter the number of processes and the details for each process.
   - After inputting the process details, the program will:
     1. Display the **average turnaround time** and **average waiting time**.
     2. Show a **Gantt chart** of process execution.
     3. Display a **table** with detailed process information.
