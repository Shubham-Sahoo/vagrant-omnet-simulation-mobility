# Vagrant box for simulation with Omnet++ and SimuLTE

A readme for vagrant box with Omnet++ simulation setup for "Machine Learning Integration in 5G Systems for QoE Estimation" project.

## Requirements
1. Vagrant - Tested with version 2.2.4 (available at: https://www.vagrantup.com/downloads.html)
2. An internet connection
3. Patience - as setup might take a few minutes

## Vagrant box setup
In the `\vagrant-omnet-simulation-mobility` folder use: 
```bash
$ vagrant up
```

And wait until the vagrant box setup is complete.

## Using the Omnet++ simulator

To access the box and the simulation environment use the following command while remaining in the `\vagrant-omnet-simulation-mobility` folder:

```bash
$ vagrant ssh
```

This will establish an ssh connection to the box. In there you can access the simulation environment.

### Running a simulation

In order to run simulation campaigns (as they were run within the project) switch to the `SimNetwork1/simulations` folder:

```bash
$ cd SimNetwork1/simulations
```

and use the following command to run an exemplary simulation campaign:

```bash
$ ./run_sim_campaign.sh -c swimMovementFP_ds0_p2_s50-50 -t 1
```

This will run a simulation campaign with the name "swimMovementFP_ds0_p2_s50-50".

-c argument specifies the campaign name. You can find what simulation campaigns are available in the `omnetpp.ini` file.