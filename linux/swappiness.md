# Swappiness

# Clear Swap

	sudo swapoff -a; sudo swapon -a

# Check swapiness

	cat /proc/sys/vm/swappiness

This is recommended to be ~10, but many times it's set to 60

# Change swapiness

	sudo sysctl vm.swappiness=10
