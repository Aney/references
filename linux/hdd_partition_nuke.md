# 

# Find drives

    lsblk

The above command can be used to see all drives and partions, as well as where they're mounted.

# Nuke

To remove all data from a drive and replace it with nothing do

    dd if=/dev/zero of=/dev/<drive> bs=1M

You can append `status=progress` to the end to see how far it's going.

This also words on partitions, you just need to make sure it's selected.

    dd if=/dev/urandom

Above is an alternative to replace the data blocks with random data. This is better for when giving the device to another person, but will take longer.

# Parition

This can be done with a number of utilities, such as `parted` and `fdisk`
