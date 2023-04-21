---
layout: page
title: On-board Computer for Small-Satellites
permalink: /projects/project_cdh/
---

<p align ="justify">
During my eighth semester at <a href="https://www.iist.ac.in/">IIST</a>, I worked on the design of an On-board computer as part of my project work. The OBC Board, also called the Command and Data Handling (C&DH) subsystem is designed to be used in small satellite projects. 
</p>

<p align="justify">
The OBC Board is built around the <a href = "https://www.microchip.com/en-us/products/fpgas-and-plds/system-on-chip-fpgas/smartfusion-2-fpgas#">SmartFusion 2 SoC </a> FPGA which incorporates ARM Cortex M3, SRAM, SECDED, eNVM, RTC and various other features. This chip works at 3.3 IO supply and 1.2 V core supply. C&DH includes one SD card slot, one 64Mb SPI-Flash, one ADC and one 9-axis IMU. It uses <a href= "https://www.ti.com/lit/ds/symlink/tps3813.pdf?ts=1682089504081&ref_url=https%253A%252F%252Fwww.ti.com%252Fsitesearch%252Fen-us%252Fdocs%252Funiversalsearch.tsp%253FlangPref%253Den-US%2526searchTerm%253DTPS3813%2526nr%253D112">TPS3813</a> for voltage supervision and as external watch dog. In-order to make the design isolated, Power and Signal Isolators have been used. One additional advantage of using isolators is that those pins for interface can be left unused without causing any risk to the system. The OBC board is a six layered PCB with the FG484 ball pin IC (M2S090).  Figure below shows the <i>Functional Block Diagram</i> design of the OBC Board.
</p>

<figure>
	<img src="{{ site.baseurl }}/projects/project_cdh/pro_cdh_1.png" alt="Functional Block Diagram of the OBC Board" style="width:100%; height:100%">      
	<figcaption> <center> Functional Block Diagram  of the OBC Board</center> </figcaption>
</figure>

<p align="justify">
The OBC Board is compatible with the interface requirements for <a href="https://www.iist.ac.in/sspace">Ahan-1</a> and <a href= "https://sanidhyavijaywat.co.in/projects/iistaarest/">AAReST Mirror Satellite</a>. Some additional interface (RS485 and GPIOs) are also provided for in-orbit testing and qualification experiment on the PSLV Stage-4 platform (<a href = "https://sanidhyavijaywat.co.in/projects/pilot/">PILOT</a>). All the digital/ analog interfaces are connected to the small satellite PC104 standard connector. The number of interfaces provided is as follows -
</p>

1. I2C - 6
2. UART (3.3 V) - 2
3. GPIO (OUT) - 7
4. GPIO (IN) - 4
5. RS485 - 3

<figure>
	<img src="{{ site.baseurl }}/projects/project_cdh/pro_cdh_2.png" alt="The OBC Board designed at IIST">      
	<figcaption> <center>The OBC Board designed at IIST</center> </figcaption>
</figure>

## Salient Highlights of the board


### Isolated Design
The Board contains various digital isolators for interface isolation with other sub-systems, if isolated power is provided then fully CDH design can be achieved.

### In-Orbit Programming
System Controller SPI pins for programming have been provided so that in-orbit FPGA programming experiment can be conducted.


<b>Here are some images taken during the testing of the OBC Board</b>

<div class="row">
	<div class="column">
	  	<figure>
			<img src="{{ site.baseurl }}/projects/project_cdh/pro_cdh_4.jpg" alt="JTAG testing" style="width:100%; height:100%">      
		</figure>
	</div>
	<div class="column">
	  	<figure>
			<img src="{{ site.baseurl }}/projects/project_cdh/pro_cdh_3.jpg" alt="Testing shorts" style="width:100%; height:100%">      
		</figure>
	</div>
	<div class="column">
	  	<figure>
			<img src="{{ site.baseurl }}/projects/project_cdh/pro_cdh_5.jpg" alt="Testing ground connections" style="width:100%; height:100%">      
		</figure>
	</div>

</div>

## Video Gallery

<iframe width="100%" height = "400px" src="https://www.youtube.com/embed/cReyMUQI3Gc" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" allowfullscreen></iframe>

<iframe width="100%" height = "400px" src="https://www.youtube.com/embed/x-l3eD9SuRc" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" allowfullscreen></iframe>


<iframe width="100%" height = "400px" src="https://www.youtube.com/embed/Ir24FzQ4z3M" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" allowfullscreen></iframe>


