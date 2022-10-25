These files are hsdmdmtpvrp01, hsdmdmtpvrp02, ..., hsdmdmtpvrp20

These data files are the ones considered in:
"A tabu search algorithm for the periodic vehicle routing problem 
with multiple vehicle trips and accessibility restrictions"
by F. Alonso, M.J. Alvarez and J.E. Beasley,
Journal of the Operational Research Society vol.59, 2008, pp963-976

The format of data files is as described below.

The first line contains the following information:

        t m n d tl

where

        t = number of days of the period
		
		m = number of vehicles

        n = number of customers

        d = number of depots

        tl = planning horizon for each period


The next m lines contain, for each vehicle, the following information:

        p k Q S c

where

        p = Vehicle type
		
		k = number of avaiable vehicles
        
        Q = maximum load of a vehicle

        S = speed of a vehicle

        f = Fixed cost per period of use
		
		c = Operation cost per unit of distance travelled
        

The next n lines contain, for each customer, the following information:

        a x y q ut f a list e

where

        a = consumer ID

        x = x coordinate

        y = y coordinate

        q = demand

        ut = time to load a vehicle

        f = frequency of visit

        a = number of possible visit combinations

        list = list of all possible visit combinations

        e = possible vehicle type visits
        
The next line d lines contains the information about the depots:

        b x y

where

        b = depot ID

        x = x coordinate of the depot

        y = y coordinate of the depot

The speed constants are used to transform distance units into time units

Hence the time to travel between two customers is equal to the Euclidean distance between 
them multiplied by the appropriate proportionality constant.

Each visit combination is coded with the decimal equivalent of the corresponding binary bit
string. For example, for 5 periods, the code 10 which is equivalent to the bit string 01010
means that a customer is visited on days 2 and 4. (Days are numbered from left to right.)

