---
layout: documentation
---

# Torque or MPI on Mesos

Torque is cluster scheduler that we have ported in a very simple way (via some Python wrappers around Torque) to run on top of Mesos. This port can be found in `MESOS_HOME/frameworks/torque`. There is a README.txt in that directory with some details. But for now while were in Alpha looking directly at the python source for the framework scheduler and executor will be helpful.

We have also run MPICH2 directly on top of mesos. See `MESOS_HOME/frameworks/mpi` for this port. Basically it sets up the MPICH2 MPD ring for you when you use nmpiexec (which is named that way because Mesos used to be called **N**exus).