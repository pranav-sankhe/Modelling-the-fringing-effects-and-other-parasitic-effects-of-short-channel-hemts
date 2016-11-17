---
layout: post
comments: true

Title: Modelling the fringing effects and their impact on High Electron Mobility Transistors. 
author: Pranav Sankhe
category: [Informative]
tags: [Mosfets, Parasitic capacitance]

---



# Modelling the fringing effects and other parasitic effects and their impact on High Electron Mobility Transistors

In 2016 summers when I was an 1st year undergraduate, I had a opportunity to work under Prof. Dipankar Saha on the topic of modelling the high frequency transistors considering the effects of fringing effect of field lines on the performance and get their I-V characteristics accordingly.
So here I have penned(typed) down a brief expert of the whole process and I got to say, this whole process may seem all tedious and geeky at the first glance but you know it's actually cool. I bet you will really enjoy exploring a particular field a little out of you regular courses and much more in detail.  

Watch out for every electronic item around you. You will find no device without a mosfet in it. Your cell phones contain billions and trillions of them and these guys are the ones who actually behind the execution of everything you do on a smartphone. 

So let's see what's so great about this baby out there. Fundamentally mosfets (metal oxide semiconductor field effect transistor) are electronic devices used to amplify or switch electrical signals. You can design logic gates by using mosfets and this opens the whole digital world for you.

The structure of a mosfet.  

**                            ![](https://lh4.googleusercontent.com/rTxqLNvAim4yZLIj2-qmD2EvbStXG-4z3rAhowgQMHply4A2xgMCbbM1QeFnokH-GzE6rKwmf_HvdAbzCYki1ZKxSTfopcmehLUsRh5GV_jYUU0PSq-vhEWIbQqXNlSF0WydOzAN)**

MOSFET showing gate (G), body (B), source (S) and drain (D) terminals. The gate is separated from the body by an insulating layer (white)

**Composition :**

- The gate terminal is essentially made up of a highly conducting materials. Earlier they used metals like aluminium for it  but nowadays highly doped semiconductor is used.
- The semiconductor used in the substrate usually is silicon. Better semiconductors like gallium arsenide are not preferred since they fail to provide good insulating interfaces.
- The oxide is used for its insulating properties. Generally silicon dioxide is used an oxide.   

### **Working:**

When a voltage is applied between gate and body terminal, electrons accumulate at the interface of oxide and substrate. Thus an electron channel is formed which serves the purpose of conducting charge carriers from source to drain terminals.
</br>
By controlling the voltage we can control the current flowing between the source and drain. By changing the voltage what we change is the conductivity of the channel and thus changing the current.
</br>
In JFETS enhanced mode and depletion mode are two major types of transistor which are classified based on the fact that whether the transistor is in ON state or OFF state. By ‘On’ state I simply mean that the channel at the semiconductor-oxide interface is conducting some current.

### **Modes of operation: Enhancement and depletion Mode  **

In enhancement mode the device is OFF when the gate voltage is zero. The gate voltage needs to be changed to turn the device on. Enhancement mode mosfets are generally used in switching the electrical signals.

In depletion mode the mosfet is On even when the gate voltage is zero. The reason for this is that a thin conducting layer is introduced at the semiconductor-oxide interface. Thus a gate voltage is not needed for the channel to form since it is already there. Depletion mode mosfets are generally used to amplify the signals.

## **Short channel effects in mosfets**

Mosfets are said to have short channels when the channel length is of same order as the width of the depletion layer.  The channel length is reduced to increase the operational speed and to reduce the components per chip. 
</br>
But by reducing the channel length we observe some effects called as short-channel effects.

### **The short-channel effects we observe are attributed to two facts:**

1.  The limitations on electron characteristics when they flow through the channel.

2.  The threshold  voltage of the mosfet changes.

**Note:** threshold voltage is the bare minimum voltage needed to just start the conduction through the channel.

### **The short-channel effects are named as follows:**

1.  drain-induced barrier lowering and punchthrough

2.  surface scattering

3.  velocity saturation

4.  impact ionization

5.  hot electrons

### **Drain-induced barrier lowering and punchthrough:**

Let’s understand the punchthrough effect. When the depletion layer surrounding the source terminal extends and merges with the depletion layer of drain terminal the charge carriers get a route to travel through. This is called as punchthrough effect. Punchthrough can be minimized with thinner oxides, larger substrate doping, shallower junctions, and obviously with longer channels.

**                         ![d21281.gif](https://lh4.googleusercontent.com/BW1r77c-YVSFQe9DKgD5XKKe64aU1FnKs9mGOJAy5jnPUvYFjGjX32eg0eP71e-x3SVZ7Yxv7FrTog9Y6Iy3qwGcUyfo0PyCBWdp9LrSJ3blw5tjzftsRlUPT6Sclv3lJ3SxPZQx)**

Drain induced barrier lowering:  we know that when when the gate voltage is zero there exists a potential barrier which prevents the electrons to flow. When the gate voltage is increased the barrier potential lowers enabling the current to flow. Since the in normal mosfets the channel length is sufficiently large the source-drain voltage doesn’t affect the potential barrier. But in short-channel mosfets the drain  barrier potential gets affected by  both gate voltage and source-drain voltage.

If you increase the source-drain voltage the potential barrier decreases allowing the electrons to flow. This is called drain induced barrier lowering . The channel current that flows under this conditions (Vgs<Vt) is called the sub-threshold current.

### **Surface scattering :**

Since the the depletion layer extends into the channel region of the mosfet the electric field component (directed from drain to source) increases. The surface mobility therefore becomes field-dependent. Since the carrier transport in a MOSFET is confined within the narrow inversion layer, and the surface scattering (that is the collisions suffered by the electrons that are accelerated toward the interface by Ex) causes reduction of the mobility, the electrons move with great difficulty parallel to the interface.

**![short-channel-effects-9-638.jpg](https://lh4.googleusercontent.com/g35dHKZvsi6KsRE7t1oPQtQX3HyDRwX84VBEjqALFGu_gaexgqPEKdlLBq3rNRNs4RScd62EEVfD_WvPlQUSfMEJfihxmeAe58e0b93SiYoQdKC6--w32Pb1XPTXGchgM4bI7xJd)**

### **Velocity Saturation:**

 At low Ey, the electron drift velocity vde in the channel varies linearly with the electric field intensity. However, as ey increases above 104 V/cm, the drift velocity tends to increase more slowly, and approaches a saturation value of Vde(sat)=107 cm/s around ey =105 V/cm at 300 K.

**Note :** the current here is limited due to velocity saturation not due to pinchoff.

**Note: pinchoff :** To form the channel the potential difference between gate and oxide-semiconductor interface must exceed the bare minimum needed voltage i.e threshold voltage.

**                             ![](https://docs.google.com/drawings/d/swmGBGJaNa6uMclDpDcsEnA/image?w=577&h=188&rev=1&ac=1)**

When the drain voltage Vd > Vg + Vt, the current becomes saturated. The reason is that when you increase the drain voltage more than a certain value which is defined by the above equation, the channel thickness at the drain terminal becomes zero. Thus the current through the channel becomes saturated.

Electrically, the effect of pinch off is that the channel no longer acts like a simple resistor. The current becomes fixed (saturated) at the value just prior to pinch off.

### **Impact Ionization:**

Another undesirable short channel effect is caused due to the high velocity of electrons in the presence of high strength  longitudinal electric fields that can generate electron-hole pairs due to impact ionization(by impacting electrons on silicon atoms and ionizing them). In general Impact ionization is the process in a material by which one energetic [charge carrier](https://en.wikipedia.org/wiki/Charge_carrier) can lose energy by the creation of other charge carriers.

**                ![img412.png](https://lh5.googleusercontent.com/xrxxPe1GOJxOfXGWB9vh8eQT_7b3gsBFEJgzny7e8IbiWXEWlq68L1nS1WTrZFjh50Xm11MB1zcYji1RZHs-xUACqsJ79nsM7O1VVG3W4QfOIuYktN00X3ZkShTmiuNmMLij7g0n)**

It happens as follows: electrons are normally attracted towards the drain while the holes enter the substrate material. The region between the source and drain can act as base of npn transistor, drain acts as a collector and source as an emitter. If the above mentioned holes formed due to impact ionization are collected by the source the corresponding hole current can create a voltage drop of about 0.6 volts and the normally reverse biased pn junction.

When electrons are injected into the base from the emitter(source) they travel through the channel towards the drain and in the process gain more energy. This creates more electron-hole pairs making the situation worse.

### **Hot electrons:**

Another problem related to the high electric fields is that the high energy electrons can enter in the oxide layer where they get trapped thus charging the oxide layers which increases the threshold voltage and simultaneously adversely affecting the gate control over the drain current.   

To get the expression of the threshold voltage of the short channel mosfet **[click here](https://www.google.co.in/url?sa=t&rct=j&q=&esrc=s&source=web&cd=3&ved=0ahUKEwi1qKi1mI_NAhXMp48KHediC7wQFggmMAI&url=http%3A%2F%2Fwww0.cs.ucl.ac.uk%2Fstaff%2Fucacdxq%2Fprojects%2Fvlsi%2Freport.pdf&usg=AFQjCNF3_nXScfWpFA2huW8DrDEYmCPiRg&sig2=NsSnvhcfxh6bY_Cuqir3ow&bvm=bv.123664746,d.c2I&cad=rja).**


The analysis of how mosfets work is largely based on the analysis of the mos capacitance. So let's have a look at it.

After all the analysis and stuff we get the mosfet current and voltage relation.

**![mosfet_equ.gif](https://lh3.googleusercontent.com/zwC88JY-9aiIl35OyZ-Aiu3nq9T4b8JPkukG_aOexhfMPNR7o4JGKWg-0yPWqBh-PGfs0gcOk8D01z7D4AOdtfS5cFBgX83B7qavINnUrG12H_9R7HEXPOyN278qYme8SJeELVIW)**

Where, Vgs = voltage applied at the gate terminal
       Ids = Current flowing from source and drain terminal
       Vds = voltage difference between source and drain terminal
       Vt = threshold voltage 
       K depends on mos capacitance, permittivities and dimensions of mosfet. 

### **Mos Capacitance**

Basically, mosfet works on the charge build up by the mos capacitance. Whenever we talk about the mos capacitance we are referring to the capacitance between the body(semiconductor) and the gate electrode(metal). 

The conventional formulae of current and voltage relation considers just the parallel capacitance. 
When we go to nano scale the fringing of field lines which is ignored at normal dimensions, come to picture and significantly affect the performance of these devices.
So the non-trivial part is to model this fringing effect. 

**A more deeper insight :** When I need to see how the electron channel in the mosfet is formed, I need to analyse how the associated regions of mosfet interact with each other. This interaction leads to the build up of some charges. We are looking for this interaction which turns out to be the capacitance. Therefore to study the overall capacitance we need to account every single electric field line. And that’s what we are gonna do.  



**Capacitance calculation in normal mosfets**

**![](https://docs.google.com/drawings/d/sfs_fzvgK64A3uRyJd_VgHg/image?w=624&h=427&rev=233&ac=1)**

The infinitesimal capacitance in the high k and spacer regions can be written as follows:

Consider a fringing field line intersecting the interface between the spacer oxide and high k oxide at a distance y from gate electrode.

**![1.png](https://lh3.googleusercontent.com/DLzPAMY26_ghZMfmr41accIcul51vrl03qqVATG2FvDonla7x9zrD3jHTT5kwCqhxx-LzyjGHEdJ7upu55YtW3I8X-DDAw3Gz6TxyJgoWLF5axZljyxEksIQr7pZKkbAD-fXfevd)**

**    High k region(C1)                       Spacer region(C2)**

**![Screenshot from 2016-07-05 23-45-58.png](https://lh3.googleusercontent.com/8aRsEaGkZ_WLPgSHLIwDn7nFEjCdQssfT308FBh5-d4resa1yUZUbZFE0ZgMQ69spppDjUtvphx3cZwkN71D5ctJ2Uz7zQSHWNA0UWfCkewltb53UOTUCq9vL5Ei3G8_eP8UmEOY)..........................(1)**

As you can see from the diagram the capacitances dC1 and dC2 are in series the net infinitesimal capacitance will be a series equivalent of the above mentioned capacitances.  

Finally after obtaining the infinitesimal capacitance, to obtain the net capacitance we need to integrate it by setting the limits of ‘t’ from ‘0’ to ‘tox’.

**The expression we get is :**

**![expression.png](https://lh3.googleusercontent.com/jk6TBkpFem3gUWvxcZhcYju358pKOI4jAqTnOC48l57WA9ruCUqSDgy8IAqDoyAhLLLzZDP7U9T09-RTqs8AwImgMfiJO9Il3iy9fw3cXjgTMBMKjtjk31qlq3DM2JX2IJUVouT1)...................(2)**

Now during the derivation of this expression we assumed the fringe lines to be circular. We will eliminate that now.

The model given by Kamchouchi and Zaky of parasitic capacitance gives the parasitic capacitance per unit length considering the electric field lines  fringing from the entire perimeter of the bottom edge of the gate electrode.

**                               ![2.png](https://lh3.googleusercontent.com/Pq-lG3DGBC1U79BXH6O-J0LaWXgSgQJf-8pPHPhapkIgq5401-pPHGONVoGhwy9R43RDXE9fiLeleMQ-dk9ZY9nbaLcJqulFbj68pq3RTplyW5jpgR7eEIQ5E-JkVsRkSdStNqGZ)..........................(3)**

The total fringe capacitance can be obtained by multiplying Cbottom by the perimeter of the bottom edge of the gate electrode.

But since here we are accounting only the electric field lines fringing from the bottom edge of the gate electrode to either the source or the drain region only, the internal fringe capacitance can be written as:

**             ![3.png](https://lh6.googleusercontent.com/kPxurulyEwI1vPz_2nrHCSyNJ7WIwogaYy9C4nwanyZYoNGkc2g7EXrtHhe-uu0AbZFVIpgg1WQOD5bzQueF-UVSPswCwqE4ME9Qww826cj8pPPfBk5s0XBaKXwyK4OE45BULe4O)**

**                                                                              …………………..(4)**

If you carefully observe you can see that eq(2) reduces to eq(4) if you substitute ![8.png](https://lh4.googleusercontent.com/Wje8ZrR7Ztk3W2yhxkTH9_JO4gb7wqAkYPhvWMBWN3zRf3Cvqyx52n90ehXCH1uzsuk31DLpcT31cFAfMeDaeVGfaZ4CQ6vWx0Fyk_31yyHim-FA4kZ0LzzuNHj13RTdsjjBrA9k)but for a constant term. This constant term accounts for the fact that the fringe lines are not circular. Therefore we will multiply eq(2) with 0.15\. The final expression we get :

**            ![4.png](https://lh5.googleusercontent.com/3SSCBgkMw_CvBZD3tk22_mlx91nUs6dIa4icm1WfMOpv4EkVAlt-erc2EasYEECpCBuIT2AXmMnLWXIt0EEMJEMGHkbFleetbh6PiyNNzfCQTe2pYq5UHyhQcUW_4vAwvkm6UFeV)  ………….(5)**

The Kamochouchi and Zaky model  assumes that the separation between the electrodes is very small in comparison to the length of the electrodes which is obviously not the case in short channel mosfets.

Now as tox/Lg increases ,there is more crowding of the field lines in the spacer region. The fringing field from the gate to source/drain regions increases as the function of tox/Lg.

To account all this we modify the dielectric of spacer dielectric constant.

**   ![5.png](https://lh4.googleusercontent.com/ScJcSZzR2oDu4GkIBmZI6pNqHu7ZYVS1g-XW_foO1aBIuf-pES7Ynj_YEi7kZQziM79i9EyzVHqIrSiW1UPDIRnbFwfA1HtEHmwzKkmejiKWBoWFbPOTUv37b4p_eZEQFZXdUMXz)**

Substitute this in equation(5) . So finally we have our expression :

Where**![6.png](https://lh4.googleusercontent.com/ubOA90bTjutca6O8eTHHBzxDOfiAKmLKglbzZMPEz0JC8r7-7yvPRaHNjhAm1aQ9dQlMGgEzmktXEVGsa2IT-ZUsnJf_4y4ow-HmRKr2LvtJmCT72CKW8WJdFq7fvJUm2jHL8x6E)**

**                     ![7.png](https://lh6.googleusercontent.com/rZ13IOi0p7pT9o0si5ONh4mINx5RT2nQ41BYVFFQMZATL_Iy_io6XVzouRN0Mutpt3SHPeF7vj8sZRezBq2lIVEs7uvU0O_ObcOTYrdalixziEs9UKcYShrQAKHFWDjElDQjHjTF)**

**____________________________________________________________________________________________________________**

My job was to analyse a different type of mosfets called as HEMTs (High Electron Mobility Transistors) 
               
							High Electron Mobility Transistors (HEMT) :

**![](https://docs.google.com/drawings/d/sGvIjBKK-ldOj5JTDGO2RQg/image?w=624&h=375&rev=831&ac=1)**

**Schottky Contact :** This is a contact between a metal and a lightly doped semiconductor.

**[Note :** Ohmic contact is a contact between a metal and a doped semiconductor.]

In the above diagram of hemt, source and drains are in ohmic contacts and gate has a schottky contact.

**These heterojunction have high carrier mobility.**

**Such high speeds are due to the following reasons:**

One layer is heavily doped with donor atoms thus it has excess of electrons in its conduction band. This electrons will diffuse to the adjacent non-doped layer due to availibility of lower energy states there. This creates an electric field. This diffusion process continues until electron diffusion and drift balance each other, creating a junction. The undoped region now has excess majority charge carriers and also since the undoped layer didn’t had any donor atoms to prove as an obstacle for electron movement.

The band discontinuities across the conduction and valence band among the different layers can be modified separately.

The diffusion process leads to the accumulation of the electron along the boundary of these layers(doped and non doped). The accumulation of electrons leads to a very high current in the heterojunction. The accumulated electrons are also known as 2 DEG or 2 D electron gas.

**Note:** 2DEG is an electron gas that can is free to move in 2 dimensions but tightly confined in the 3rd dimension. this confinement leads to quantized energy levels for motion in 3rd dimension. Thus it appears to be 2-D sheet embedded 3D.

**So to summarize we can say that hemt is a field effect transistor which incorporates a junction between 2 materials with different band gaps as the channel.**

**![20090624-01bl_tcm100-930131.jpg](https://lh5.googleusercontent.com/bIVl15YiHOqUejaekYgxwhCEDIwl8U44CYx5gjy0O6jrNgljghhSqVUsC7ryGz8xXMn6kGZj0fJanPnIa9yS0chmbQJMvIIw5fubHy_THrr-ZM9dw-prhNUJuis0DpKu40GDsJM4)**
</br>


Before actually getting started with the modelling of capacitance just have a look at the impact of parasitic capacitance on the performance of these devices.

**It is found out that the gate extrinsic capacitance contributes significantly to the parasitic delay -approx 50% of the delay in these highly scaled devices.**

**Now this gate capacitance comprises of 2 components:**

**1\.** Parallel plate capacitance between the Tgate and the surrounding electrodes.

**2\.** The fringing capacitance between the gate stem and the access regions.
</br>
When the gate length is reduced below 100nm the parasitic RC charging delay caused by source drain resistance and parasitic capacitance can account for a significant fraction in the delay of the device. 
</br> 

Now we will proceed to the actual calculations involved in obtaining the net capacitance of hemt. 
Sorry for not using mathjax :p   

We would need a analytical formula for capacitance between 2 plates of specified dimensions and a particular angle between them.

**![1.jpg](https://lh5.googleusercontent.com/9h1s3rkN2IpkZjZ2TQMi7PSjGjpW7Ge1lTUAAPIfnx1FYyv-AauhNNlkJZ-voXTAbiGiGWrkMoEuBfSegQk1xCZXef5O4RsmVi2MpA7d3NDj_IsO0OucpVKagojuCDm-hucqyqEp)**

![2.jpg](https://lh5.googleusercontent.com/FrSbGcs6dOA_9H4gI6zM1pUzKD1zrv4_qgxpPpVwbs-1RYEAOhEyjEoS0WN0DxMo8ls5O1VD8regZ9_GMq0tobKsqqmPEkOUqQcKapsEUAiAlWEWaFEei9SZHsgDQvQZDmWaV0E-)**

**![3.jpg](https://lh3.googleusercontent.com/6-WmpmZ_mB3xBg0m2aQQEdAXcltuhPQk8V6CcCMREbUkNODWFV9gxtz5VpgIbawKR_3mQZWY_WHcBXhimaYkSFFg1UuyaNi8dAKrw6w61M37iATwfDQPjTgjuhKrJtmCXpnKkw_v)**


So now we have the expression of the net capacitance of HEMTS.

Having the capacitance expression we proceed to find the charge density of the channel and then get the current expression. 

![6.jpg](https://lh6.googleusercontent.com/1PcwzjKBscpefjG0PVPyAOsK7g9MxzSQfwD1PhJ-aVUcqzou8xuThjNskuzGaJzG4nQewBo5W45XrvqbasnAVfv8CNSmJRv3-faODgJlJJHMtpfSzmakgLzJiArPZEGSYxFktwfQ)**

**![7.jpg](https://lh5.googleusercontent.com/tdUdq1Z5sAUWXLiWu54jyWTUeql6elbfv1WShYhPTTXzxVAm-975H1wLSWn6v5AOdcsBPsEcaYLlTkdhRMrU59Cz1rUI0mm9mAqSsh9jJ2yIYQQ7QVTL-NC-NUkXbKtPar_f1OHq)**

</br>
Some of methods proposed to reduce the parasitic capacitance and its contribution in the delay of HEMTS. 

**![4.jpg](https://lh6.googleusercontent.com/M5_Asu3cRNtP3Hawu_4RFB69msVxaa2jtBsYQLZl_BqCYLneUAvJV9kpAZ14dYfks_LjNkTNlSiPHcDKZQaePc7G2btMjDpbjIJv8mLcVVLftTK6mNbrOCjR3ZhNpTlBQ-KFFM2l)**  

**![5.jpg](https://lh5.googleusercontent.com/FDJ9SEtXwydYPshiGz1oFWYxaXbj5mBJdo0FJ-GJWcazZXhwEX12MFi4oxfX3LLMcfgaeuzMsqnT6JWjk-41Iw99AYpPSkvMtiWZiVoX_rSdJiDe5qOKyI2TnwOBc60Pkvk8EDbt)** 


Thankyou for reading.  

Credits to some papers refered : 

- The electrostatic capacitance of an inclined plate capacitor by Yumin Xiang
- Effect of Fringing Capacitances on the RF Performance of GaN HEMTs With T-Gates

