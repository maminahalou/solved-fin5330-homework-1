Download Link: https://assignmentchef.com/product/solved-fin5330-homework-1
<br>
Consider the daily stock returns of American Express (AXP), Caterpillar (CAT), and Starbucks (SBUX) from January 1999 to December 2008. The data are daily prices in the file <em>stock-datahwk1.txt</em>.

<ul>

 <li>(a) Calculate simple returns for the three series.</li>

</ul>

<table width="420">

 <tbody>

  <tr>

   <td width="23">0</td>

   <td width="153">18542 19990104</td>

   <td width="244">CAT 47.3750 -0.000822 0.011409</td>

  </tr>

  <tr>

   <td width="23">1</td>

   <td width="153">18542 19990105</td>

   <td width="244">CAT 47.2500 0.011879 0.009512</td>

  </tr>

  <tr>

   <td width="23">2</td>

   <td width="153">18542 19990106</td>

   <td width="244">CAT 48.5000 0.021143 0.014866</td>

  </tr>

  <tr>

   <td width="23">3</td>

   <td width="153">18542 19990107</td>

   <td width="244">CAT 48.9375 -0.000798 0.003560</td>

  </tr>

  <tr>

   <td width="23">4</td>

   <td width="153">18542 19990108</td>

   <td width="244">CAT 51.0000 0.004602 0.009410</td>

  </tr>

 </tbody>

</table>

<ul>

 <li>(b) Express the simple returns in percentages. Compute the sample mean, standard deviation, skewness, excess kurtosis, minimum, and maximum of the percentage simple returns.</li>

 <li>(c) Transform the simple returns to log returns.</li>

 <li>(d) Express the log returns in percentages. Compute the sample mean, standard deviation, skewness, excess kurtosis, minimum, and maximum of the percentage log returns.</li>

 <li>(e) Test the null hypothesis that the mean of the log returns of each stock is zero. That is, perform three separate tests. Use 5% significance level to draw your conclusion.</li>

 <li>(f) Plot histograms for each of the three series (both simple and log returns – so six graphs</li>

</ul>

total).

<ul>

 <li>(g) Test the null hypothesis that the lag-2 autocorrelation is zero for log returns.</li>

</ul>

Here is some code to extract the price time series from the raw data in Python:

<table width="451">

 <tbody>

  <tr>

   <td width="46">2515</td>

   <td width="153">59176 19990104</td>

   <td width="252">AXP 101.5000 -0.000822 0.011409</td>

  </tr>

  <tr>

   <td width="46">2516</td>

   <td width="153">59176 19990105</td>

   <td width="252">AXP 99.5625 0.011879 0.009512</td>

  </tr>

  <tr>

   <td width="46">2517</td>

   <td width="153">59176 19990106</td>

   <td width="252">AXP 103.6250 0.021143 0.014866</td>

  </tr>

  <tr>

   <td width="46">2518</td>

   <td width="153">59176 19990107</td>

   <td width="252">AXP 104.8750 -0.000798 0.003560</td>

  </tr>

  <tr>

   <td width="46">2519</td>

   <td width="153">59176 19990108</td>

   <td width="252">AXP 108.0625 0.004602 0.009410</td>

  </tr>

 </tbody>

</table>

[7]:      PERMNO    date TICKER  PRC   vwretd   ewretd

<table width="428">

 <tbody>

  <tr>

   <td width="46">5025</td>

   <td width="153">59176 20081224</td>

   <td width="229">AXP 17.97 0.004514 0.005042</td>

  </tr>

  <tr>

   <td width="46">5026</td>

   <td width="153">59176 20081226</td>

   <td width="229">AXP 17.91 0.007191 0.011107</td>

  </tr>

  <tr>

   <td width="46">5027</td>

   <td width="153">59176 20081229</td>

   <td width="229">AXP 17.70 -0.004365 -0.015163</td>

  </tr>

  <tr>

   <td width="46">5028</td>

   <td width="153">59176 20081230</td>

   <td width="229">AXP 18.00 0.024764 0.021418</td>

  </tr>

  <tr>

   <td width="46">5029</td>

   <td width="153">59176 20081231</td>

   <td width="229">AXP 18.55 0.017404 0.034456</td>

  </tr>

 </tbody>

</table>

<table width="428">

 <tbody>

  <tr>

   <td width="46">2510</td>

   <td width="153">18542 20081224</td>

   <td width="229">CAT 41.91 0.004514 0.005042</td>

  </tr>

  <tr>

   <td width="46">2511</td>

   <td width="153">18542 20081226</td>

   <td width="229">CAT 42.72 0.007191 0.011107</td>

  </tr>

  <tr>

   <td width="46">2512</td>

   <td width="153">18542 20081229</td>

   <td width="229">CAT 42.34 -0.004365 -0.015163</td>

  </tr>

  <tr>

   <td width="46">2513</td>

   <td width="153">18542 20081230</td>

   <td width="229">CAT 43.66 0.024764 0.021418</td>

  </tr>

  <tr>

   <td width="46">2514</td>

   <td width="153">18542 20081231</td>

   <td width="229">CAT 44.67 0.017404 0.034456</td>

  </tr>

 </tbody>

</table>

[6]:    PERMNO    date TICKER    PRC   vwretd   ewretd

<table width="420">

 <tbody>

  <tr>

   <td width="23">0</td>

   <td width="153">18542 19990104</td>

   <td width="244">CAT 47.3750 -0.000822 0.011409</td>

  </tr>

  <tr>

   <td width="23">1</td>

   <td width="153">18542 19990105</td>

   <td width="244">CAT 47.2500 0.011879 0.009512</td>

  </tr>

  <tr>

   <td width="23">2</td>

   <td width="153">18542 19990106</td>

   <td width="244">CAT 48.5000 0.021143 0.014866</td>

  </tr>

  <tr>

   <td width="23">3</td>

   <td width="153">18542 19990107</td>

   <td width="244">CAT 48.9375 -0.000798 0.003560</td>

  </tr>

  <tr>

   <td width="23">4</td>

   <td width="153">18542 19990108</td>

   <td width="244">CAT 51.0000 0.004602 0.009410</td>

  </tr>

 </tbody>

</table>

[8]:      PERMNO    date TICKER  PRC   vwretd   ewretd

[9]:      PERMNO    date TICKER    PRC   vwretd   ewretd

<table width="443">

 <tbody>

  <tr>

   <td width="46">5030</td>

   <td width="145">77702 19990104</td>

   <td width="252">SBUX 53.8750 -0.000822 0.011409</td>

  </tr>

  <tr>

   <td width="46">5031</td>

   <td width="145">77702 19990105</td>

   <td width="252">SBUX 52.0000 0.011879 0.009512</td>

  </tr>

  <tr>

   <td width="46">5032</td>

   <td width="145">77702 19990106</td>

   <td width="252">SBUX 51.5625 0.021143 0.014866</td>

  </tr>

  <tr>

   <td width="46">5033</td>

   <td width="145">77702 19990107</td>

   <td width="252">SBUX 51.7500 -0.000798 0.003560</td>

  </tr>

  <tr>

   <td width="46">5034</td>

   <td width="145">77702 19990108</td>

   <td width="252">SBUX 52.8750 0.004602 0.009410</td>

  </tr>

 </tbody>

</table>

[10]:     PERMNO    date TICKER  PRC   vwretd   ewretd

<table width="420">

 <tbody>

  <tr>

   <td width="46">7540</td>

   <td width="145">77702 20081224</td>

   <td width="229">SBUX 9.34 0.004514 0.005042</td>

  </tr>

  <tr>

   <td width="46">7541</td>

   <td width="145">77702 20081226</td>

   <td width="229">SBUX 9.35 0.007191 0.011107</td>

  </tr>

  <tr>

   <td width="46">7542</td>

   <td width="145">77702 20081229</td>

   <td width="229">SBUX 9.03 -0.004365 -0.015163</td>

  </tr>

  <tr>

   <td width="46">7543</td>

   <td width="145">77702 20081230</td>

   <td width="229">SBUX 9.36 0.024764 0.021418</td>

  </tr>

  <tr>

   <td width="46">7544</td>

   <td width="145">77702 20081231</td>

   <td width="229">SBUX 9.46 0.017404 0.034456</td>

  </tr>

 </tbody>

</table>

You can access the price time series as (for example for AXP):

<table width="169">

 <tbody>

  <tr>

   <td width="108">[11]: 2515</td>

   <td width="61">101.5000</td>

  </tr>

  <tr>

   <td width="108">2516</td>

   <td width="61">99.5625</td>

  </tr>

  <tr>

   <td width="108">2517</td>

   <td width="61">103.6250</td>

  </tr>

  <tr>

   <td width="108">2518</td>

   <td width="61">104.8750</td>

  </tr>

  <tr>

   <td width="108">2519</td>

   <td width="61">108.0625</td>

  </tr>

  <tr>

   <td width="108">2520</td>

   <td width="61">106.2500</td>

  </tr>

  <tr>

   <td width="108">2521</td>

   <td width="61">102.3750</td>

  </tr>

  <tr>

   <td width="108">2522</td>

   <td width="61">98.6875</td>

  </tr>

  <tr>

   <td width="108">2523</td>

   <td width="61">96.0000</td>

  </tr>

  <tr>

   <td width="108">2524</td>

   <td width="61">104.3750</td>

  </tr>

  <tr>

   <td width="108">2525</td>

   <td width="61">100.5000</td>

  </tr>

  <tr>

   <td width="108">2526</td>

   <td width="61">102.0000</td>

  </tr>

  <tr>

   <td width="108">2527</td>

   <td width="61">102.5000</td>

  </tr>

  <tr>

   <td width="108">2528</td>

   <td width="61">98.5000</td>

  </tr>

  <tr>

   <td width="108">2529</td>

   <td width="61">101.5000</td>

  </tr>

  <tr>

   <td width="108">2530</td>

   <td width="61">101.7500</td>

  </tr>

  <tr>

   <td width="108">2531</td>

   <td width="61">99.4375</td>

  </tr>

  <tr>

   <td width="108">2532</td>

   <td width="61">100.4375</td>

  </tr>

  <tr>

   <td width="108">2533</td>

   <td width="61">102.8750</td>

  </tr>

  <tr>

   <td width="108">2534</td>

   <td width="61">100.7500</td>

  </tr>

  <tr>

   <td width="108">2535</td>

   <td width="61">99.6875</td>

  </tr>

  <tr>

   <td width="108">2536</td>

   <td width="61">100.5000</td>

  </tr>

  <tr>

   <td width="108">2537</td>

   <td width="61">100.2500</td>

  </tr>

  <tr>

   <td width="108">2538</td>

   <td width="61">98.1250</td>

  </tr>

  <tr>

   <td width="108">2539</td>

   <td width="61">97.0625</td>

  </tr>

 </tbody>

</table>

<ul>

 <li>9375</li>

 <li>7500</li>

 <li>0000</li>

 <li>9375</li>

 <li>1875</li>

</ul>

…

<ul>

 <li>3800</li>

 <li>7400</li>

 <li>2300</li>

 <li>6900</li>

 <li>1800</li>

 <li>3700</li>

 <li>3000</li>

 <li>3100</li>

 <li>6400</li>

 <li>7600</li>

 <li>8700</li>

 <li>8400</li>

 <li>7800</li>

 <li>4400</li>

 <li>2900</li>

 <li>5600</li>

 <li>1300</li>

 <li>3400</li>

 <li>3400</li>

 <li>0600</li>

 <li>8100</li>

 <li>9000</li>

 <li>4300</li>

 <li>4200</li>

 <li>9600</li>

 <li>9700</li>

 <li>9100</li>

 <li>7000</li>

 <li>0000</li>

 <li>5500</li>

</ul>

Name: PRC, Length: 2515, dtype: float64

[ ]: