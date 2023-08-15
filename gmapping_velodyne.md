when run gampping , it will operate tf-trees: link the **map** to **odom** \
if we want to run the gmapping, the laser_scan's frameid(**velodyne** in VeloLidar) should link to **base_link**(the car coordinate). \
these four tf-tree is necessary.so if we publish the transform tree manuly,which means the base_link is static,the gmapping would just build one frame map; \
to run the gampping correctly , there should be a publisher to publish the moving base_link----like wheel odometry module.

may the gmapping need the move information to do registeration!
