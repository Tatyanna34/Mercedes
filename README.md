# Mercedesclass Mercedes:
    def __init__(self, model, year):
        self.model = model
        self.year = year
        self.engine_running = False

    def start_engine(self):
        if not self.engine_running:
            self.engine_running = True
            print(f"The engine of the {self.model} is now running.")
        else:
            print(f"The engine of the {self.model} is already running.")

    def stop_engine(self):
        if self.engine_running:
            self.engine_running = False
            print(f"The engine of the {self.model} is now stopped.")
        else:
            print(f"The engine of the {self.model} is already stopped.")

    def display_status(self):
        status = "running" if self.engine_running else "stopped"
        print(f"The {self.year} {self.model} engine is currently {status}.")

# Example usage
my_car = Mercedes(model="Mercedes-Benz C-Class", year=2024)
my_car.display_status()  # Check initial status
my_car.start_engine()    # Start the engine
my_car.display_status()  # Check status after starting
my_car.stop_engine()     # Stop the engine
my_car.display_status()  # Check status after stopping
