# Task 3 — Create Swap (Partition + LV Methods)

## Instructions

### Part A — Create Swap Using a Partition

1. Identify your practice disk using:
2. Create a new partition on `/dev/your_disk` using `fdisk`.
3. Change the partition type to Linux swap:
4. Write changes and exit.
5. Format the new partition as swap
6. Enable swap using.
7. Verify swap is active.
8. Disable swap.




### **Part B — Create Swap Using an LVM Logical Volume**

1. Ensure you already have a volume group.
2. Create a new 256M logical volume named `lvswap` inside `labvg`.
3. Format the LV as swap using.
4. Enable swap.
5. Verify swap is active.
6. Disable swap.
