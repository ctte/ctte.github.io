<p align="left">
	<img src="/Figure1(a)MSE%20for%20link%20speed%20prediction.png" alt="Figure1(a)"  width="300" height="250" align="left">
	&emsp;&emsp;&emsp;
  <img src="/Figure1(b)MAE%20for%20link%20speed%20prediction.png" alt="Figure1(b)"  width="300" height="250" align="center">
</p>
<p>
		<em>Figure1(a) MSE for link speed prediction &emsp;&emsp;&emsp; Figure1(b) MAE for link speed prediction</em>
</p>

### __Figure 1. Link speed prediction accuracy, with/out road network.We can observe that road network reduces the MSE from 22.5 to 16.9, and reduces MAE from 2.4 to 2.2.__

-------------------------------------
<p align="left">
	<img src="/Figure2(a)MSE%20for%20link%20speed%20prediction.png" alt="Figure2(a)"  width="300" height="250" align="left">
	&emsp;&emsp;&emsp;
  <img src="/Figure2(b)MAE%20for%20link%20speed%20prediction.png" alt="Figure2(b)"  width="300" height="250" align="center">
</p>
<p>
		<em>Figure2(a) MSE for link speed prediction &emsp;&emsp;&emsp; Figure2(b) MAE for link speed prediction</em>
</p>

### __Figure 2. Link speed prediction accuracy, with/out attention mechanism.We can observe that out attention mechanism reduces the MSE from 16.9 to 16.2, and reduces the MAE from 2.3 to 2.1.__

-------------------------------------------

<p align="left">
	<img src="/Figure3(a)MSE%20for%20travel%20time%20estimation.png" alt="Figure3(a)"  width="300" height="250" align="left">
	&emsp;&emsp;&emsp;
  <img src="/Figure3(b)MAE%20for%20travel%20time%20estimation.png" alt="Figure3(b)"  width="300" height="250" align="center">
</p>
<p>
		<em>Figure3(a) MSE for travel time estimation &emsp;&emsp;&emsp; Figure3(b) MAE for travel time estimation</em>
</p>
<div align="left">
  <img src="/Figure3(c)MAPE%20for%20travel%20time%20estimation.png" alt="Figur3(c)"  width="300" height="250" align="left">
</div><br /><br /><br /><br /><br /><br /><br /><br /><br /><br /><br />
<div>
		<em>Figure3(c) MAPE for travel time estimation</em>
</div>

### __Figure 3. Travel time estimation accuracy, with random embedding or deepwalk for road network.We can observe that with the random embedding or deepwalk embedding for road network, the MSE is 235576 and 192460, the MAE is 292 and 273, and the MAPE is 34% and 24%, respectively. The deepwalk representation helps to convergence the loss quickly and reaching to a much lower level.__

-------------------------------------
<p align="left">
	<img src="/Figure4(a)random%20embedding%20for%20ETA.png" alt="Figure4(a)"  width="300" height="250" align="left">
	&emsp;&emsp;&emsp;
  <img src="/Figure4(b)ResNet%20for%20ETA.png" alt="Figure4(b)"  width="300" height="250" align="center">
</p>
<p>
		<em>Figure4(a)  random embedding for ETA &emsp;&emsp;&emsp;&emsp;&emsp; Figure4(b) ResNet for ETA</em>
</p>

### __Figure 4. MAPE for travel time estimation: (a) random embedding with/out ResNet; (b) deepwalk with/out ResNet.We can observe tha the ResNet module reduces the MAPE significantly, from 94% to 39% for random embedding, and from 93% to 24% for deepwalk embedding.__

-------------------------------------------
<p align="left">
	<img src="/latest.PNG" alt="Figure5"  width="300" height="250" align="left">
	&emsp;&emsp;&emsp;
</p><br /><br /><br /><br /><br /><br /><br /><br /><br />
<p>
		<em>Figure5 MAPE for IMU</em>
</p>

### __Figure 5. MAPE for travel time estimation with IMU data, reducing the MAPE value with 0.5%.We put the IMU data into conv1d layers with different kernel size (specifically, they're 6, 12 and 18) and 6 out channels. Moreover, we concat the output features and input them with a FC layer to get a scale factor, then amend the output of nerual network with this scalue factor (multiplication). Since our IMU data is very sparse (1 sample/3 seconds), it only reduces the MAPE loss with 0.5%. The experiment proves the effectiveness of IMU data, and we will test more fine-grained IMU data in the future for more improvement.__

-------------------------------------------
<p align="left">
	<img src="/Figure6(a)Dropout%20vs%20MAPE.png" alt="Figure6(a)"  width="300" height="250" align="left">
	&emsp;&emsp;&emsp;
  <img src="/Figure6(b)Hidden%20state%20size%20vs%20MAPE.png" alt="Figure6(b)"  width="300" height="250" align="center">
</p>
<p>
		<em>Figure6(a) Dropout vs MAPE &emsp;&emsp;&emsp;&emsp;&emsp; Figure6(b)Hidden state size vs MAPE</em>
</p>

### __Figure 6. MAPE for nerual network hyper-parameters: (a) dropout value; (b) hidden state size.We have set the dropout value with 0.2, 0.5, and 0.7, and the MAPE loss is 24.4%, 24.38%, and 24.14%, respectively. In addition, we have set the number of LSTM hidden state size with 16, 32, and 64 (all with dropout at 0.2), and the corresponding MAPE loss is 24.02%, 24.18%, and 24.32%, respectively. Such experiment shows the rubostness of our model with different hyper-parameters.__

-------------------------------------------
<p align="left">
	<img src="/Figure7(a)Travel%20time%20vs%20MAPE.png" alt="Figure7(a)"  width="300" height="250" align="left">
	&emsp;&emsp;&emsp;
  
</p><br /><br /><br /><br /><br /><br /><br /><br /><br />
<p>
		<em>Figure7 Travel time vs MAPE &emsp;&emsp;&emsp;&emsp;&emsp; </em>
</p>

### __Figure 7. MAPE vs travel time.We can observe that the MAPE loss increases with longer travel time, but its variance reduces. This is consistent with our common sense.__

-------------------------------------------
<!--
![Figure1(a)](/Figure1(a)MSE%20for%20link%20speed%20prediction.png)  
__Figure1(a) MSE for link speed prediction__
![Figure1(b)](/Figure1(b)MAE%20for%20link%20speed%20prediction.png)  
__Figure1(b) MAE for link speed prediction__
## __Figure 1. Link speed prediction accuracy, with/out road network.__
-------------------------------------
![Figure2(a)](/Figure2(a)MSE%20for%20link%20speed%20prediction.png)  
__Figure2(a) MSE for link speed prediction__
![Figure2(b)](/Figure2(b)MAE%20for%20link%20speed%20prediction.png)  
__Figure2(b) MAE for link speed prediction__
## __Figure 2. Link speed prediction accuracy, with/out attention mechanism.__
------------------------------------
![Figure3(a)](/Figure3(a)MSE%20for%20travel%20time%20estimation.png)  
__Figure3(a) MSE for travel time estimation__
![Figure3(b)](/Figure3(b)MAE%20for%20travel%20time%20estimation.png)  
__Figure3(b) MAE for travel time estimation__
![Figure3(c)](/Figure3(c)MAPE%20for%20travel%20time%20estimation.png)  
__Figure3(c) MAPE for travel time estimation__
## __Figure 3. Travel time estimation accuracy, with random embedding or deepwalk for road network.__
------------------------------------
![Figure4(a)random embedding for ETA](/Figure4(a)random%20embedding%20for%20ETA.png)   
__Figure4(a)  random embedding for ETA__
![Figure4(b)](Figure4(b)ResNet%20for%20ETA.png)   
__Figure4(b) ResNet for ETA__
## __Figure 4. MAPE for travel time estimation: (a) random embedding with/out ResNet; (b) deepwalk with/out ResNet.__
-->
