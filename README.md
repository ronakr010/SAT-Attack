# SAT-Attack
◦ Implemented SAT-attack to break Logic Encryption techniques like Random Logic Locking (RLL)
◦ Applied RLL on Logic circuits with key-size = 32, 64 &128 bits for Logic Encryption
◦ Applied SAT-attack on RLL encrypted ISCAS’89 and ITC’99 benchmark circuits to found correct key
◦ Analysed time taken and No. of iterations taken to break Logic Encryption



**The SAT attack**
Prior to 2015, most of the logic locking schemes focussed on increasing the output corruption of logic circuits. However in 2015, a potent attack was introduced, called SAT attack, which made use of boolean satisfiability to break most of the logic locking schemes. It requires two things to attack; one is locked gate level net-list and other being activated chip (oracle). In this attack, a miter circuit is constructed of the locked netlist such that there are two different keys but same primary inputs. The clauses are constructed for the above miter and a satisfying clause for primary input is found out such that outputs are different for two keys. This is referred to as distinguishing input pattern (DIP). DIP is then applied to oracle to find the correct output. The correct output for the given DIP is added as a constraint to SAT. It ensures that for the particular DIP, solver eliminates all the keys having outputs different from correct output. Thus, in one iteration multiple keys can be eliminated. This process is repeated until there are no DIPs. After that, the key which satisfies all the DIP constraints emerges as the correct one.

