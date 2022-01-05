# Load Data
```
import pickle
f = open(filename, "rb")
data = pickle.load(f)
```
# Data Structure
```
data--key 		       	   : number of note
    |-value			   : A python dict include all the information in the note.
	|-num    		   : integer, showing the number of note.
	|-fs    	           : integer, showing the sample rate(usually 44100).
	|-start  		   : float, showing the start time(s).
   	|-end       		   : float, showing the end time(s).
   	|-name         		   : string, showing the name of note.
   	|-envelope		   : 1d float list of envelope(sample rate=fs).
   	|-pitch   		   : 1d float list of pitch contour.
   	|-harmonics 		   : 2d float list of the amplitude ratio between harmonics.
        	|-first dimension  : include 10 lists, each list represents to a harmonics in order.
        	|-second dimension : 1d float list, contains a amplitude curve describing the variety of amplitude in time domain.
```
