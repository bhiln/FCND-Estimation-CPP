#FCND-Estimation Writeup
Brian Hilnbrand

##Step 1
To calculate the standard deviation of the GPS and IMU, I performed the following method. I logged a full 10s loop of the data into a text file. Next, I removed the top header line in the log, so only time and value were left in a csv file. I then used Numpy in Python to import the txt file as a numpy array. Next, I used the numpy standard deviation tool to calculate the standard deviation of the values in the file.
```
$ fname = os.path.join("Graph2.txt")
$ imu_x = np.loadtxt(fname, delimiter=",")
$ np.std(imu_x[:,1])
0.51095120101124747
```
![Alt text](./std.jpg?raw=true "Title")

##Step 2
