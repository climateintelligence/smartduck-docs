# GUI for Climate Services Information Systems

## Example: Phoenix

* Birdhouse provides a web-based application where birds can be linked into it for GUI usage.  [Phoenix](https://github.com/bird-house/pyramid-phoenix). Phoenix is a web application to work with processing services like our *duck* demo.
We have deployed the *duck* demo on a virtual machine at [DKRZ](https://www.dkrz.de/en/).
In the following example we run the *duck* infill process using the Phoenix app.

## Infill with Duck

Go to the Phoenix app:
https://bovec.dkrz.de

* Choose the *Duck* processing service
```{figure} /media/phoenix-duck-wps.png
:scale: 50%
```

* Use the *ClintAI* process
```{figure} /media/phoenix-duck-processes.png
:scale: 50%
```

* Select a HadCRUT5 dataset for the infill process
```{figure} /media/phoenix-duck-infill.png
:scale: 50%
```

* Wait for the process to finish ...
```{figure} /media/phoenix-duck-monitor.png
:scale: 50%
```

* When the process has finished go to the *details* to show the outputs
```{figure} /media/phoenix-duck-outputs.png
:scale: 50%
```

* Outputs: a plot before the infill
```{figure} /media/duck-plot-before.png
:scale: 50%
```

* Outputs: a plot after the infill
```{figure} /media/duck-plot-after.png
:scale: 50%
```
