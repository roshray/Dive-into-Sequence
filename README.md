# Dive-into-Sequence


### Overview of RNN 

![unfold_RNN](https://github.com/roshray/Dive-into-Sequence/blob/master/img/unfold-rnn.jpg)

### RNN network steps 

                $$\begin{equation*}
                    \ a^t = b + Ws^{t-1} + Ux^t .........(1)\\
                    \ s^t = tanh(a^t)           .........(2)\\
                     \ o^t = c + Vs^t           .........(3)\\
                     \ p^t = softmax(o^t)       .........(4)
                    \end{equation*}$$

the parameters are the bias vectors b and c along with the weight matrices U , V and W , respectively, for input-to-hidden, hidden-to output and hidden-to-hidden connections. This is an example of a recurrent network that maps an input sequence to an output sequence of the same length

### Derivation attempt

![derivation](https://github.com/roshray/Dive-into-Sequence/blob/master/img/derivation.jpg)

**Four Effective ways to learn RNN -** 

     1)LSTM:They are designed to remember values for long time.

     2)Hessian Free Optimization:

     3)Echo State Network:

     4)Good Intialization of Momentum:

### Long Short Term Memory Network ::

    They are designed(a memory cell using logistic and linear units with multiplicative interactions)to remember values for long time(like hundred of time steps.).

![lstm_gate:source:http://deeplearning.net](https://github.com/roshray/Dive-into-Sequence/blob/master/img/lstm_gate.png)


#### Brief understanding of Long Short Term Memory ::

![key_Elements_LSTM](https://github.com/roshray/Dive-into-Sequence/blob/master/img/LSTM_GATE.jpg)

- 1)A memory cell or Information cell using logistic and linear units with multiplicative interactions.

      It is responsible for holding the data and the three logistic GATES(write,keep and read) define the flow of data inside the LSTM.

- 2)WRITE GATE or INPUT GATE is responsible for writing data into memory cell.

      Information gets into the cell whenever its "WRITE" gate is ON.
      Its recieve the same input and the state of the network__
      It also recieve the recurrent net's output data from the most current time step.
      It uses the input to detemine how much of the output data should be written in memory cell.
      
- 3)KEEP GATE or FORGET GATE is maintains or delete data from memory cell.

      The Informaion stays in the cell so long as its "KEEP" gate is ON.
      Its recieve the same input and the state of the network and then calculates how much of the current data should be remember.

- 4)READ GATE or OUTPUT GATE reads data from information cell and send back to recurrent network.

      Information can be read from the cell on its "READ" gate.
      It reads a value from information cell,and this value is interpreted as signal between -1 and 1.
      The input data and state of the network are then used to dtermine how much of this signal should be send to the recurrent network.
      
**NOTE Manupulating GATES,a recurrent network is able to remember what it needs and forget what is no longer useful.**

![gates_formu:medium](https://github.com/roshray/Dive-into-Sequence/blob/master/img/gates_formu.gif)

[CODE](https://github.com/roshray/Dive-into-Sequence/blob/master/LSTM-02.ipynb)


