class HighPressureWasher:
    def __init__(self, motor_power, water_flow_rate, pressure_rating):
        self.motor_power = motor_power  # 電動機功率，決定水壓
        self.water_flow_rate = water_flow_rate  # 水流速率，影響清洗範圍
        self.pressure_rating = pressure_rating  # 水壓等級，清洗的強度

    def start(self):
        print(f"Starting washer with {self.motor_power} kW motor.")
        print(f"Pressure: {self.pressure_rating} bar, Flow rate: {self.water_flow_rate} L/min")
        
    def stop(self):
        print("Stopping the high-pressure washer.")

    def wash_surface(self, surface_type):
        if surface_type == 'concrete':
            print("Using high pressure to clean concrete surface.")
        elif surface_type == 'car':
            print("Using medium pressure to clean car surface.")
        else:
            print("Adjusting pressure for different surface.")
            
# 創建高壓清洗機物件並使用
washer = HighPressureWasher(2.5, 10, 120)
washer.start()
washer.wash_surface('car')
washer.stop()
# HighPressureWasher
