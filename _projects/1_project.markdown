---
layout: page
title: Coos Estuary dynamics
img: /assets/img/coos_thumb_1.jpeg
---

<div class="img_row">
    <img class="col one left" src="{{ site.baseurl }}/assets/img/pic1.png" alt="" title="example image"/>
    <img class="col two right" src="{{ site.baseurl }}/assets/img/pic3.jpeg" alt="" title="example image"/>
</div>

I worked with [Dave Sutherland](https://www.oceanice.org) and used the [Finite Volume Coastal Ocean Model](http://fvcom.smast.umassd.edu/fvcom/) (FVCOM) for the Coos Estuary in Oregon. The freshwater input into the Coos estuary, and subsequently the hydrography of the estuary and along estuary baroclinic pressure gradient, is highly seasonal (Sutherland and O'Neil 2016), begging the question of how does the estuarine exchange flow, the tidally averaged water movement, change through out the year? To answer this and other questions about the hydrodynamics and salt distribution of the Coos Estuary, we set up FVCOM using high resolution bathymetry mapped onto a high resolution unstructured grid. The movie below shows surface salinity during wet-season background (non-discharge event) conditions.

<video width="600" controls>
  <source src="/assets/img/movie_cut.mp4" type="video/mp4">
</video>

The Total Exchange Flow method (TEF; MacCready 2011) was used to quantify the estuarine exchange flow for an annual model run. This method is advantageous because it incorporates both tidal and subtidal motions by using a salinity coordinate instead of an Eulerian coordinate for calculating the exchange flow through cross sections in the estuary. Using the Total Exchange Flow, we found that the tidal component is the dominant component (compared with the subtidal), and that although the along estuary baroclinic pressure gradient changes quite a bit over the year, the inflowing component of the exchange flow doesn't change very much seasonally, but rather with the spring-neap cycle. The plots below summarize the results over the year of 2014.

<img src="/assets/img/Fig7.png" alt="ex" width="700"/>
 
The inflow corresponds with the tidal volume flux, which is converted to a TEF inflow by a number of dispersive processes. There is a strong seasonal component in vertical stratification, mixing (quantified as the dissipation of salinity variance), and the outflowing component of the exchange flow. The seasonality of the outflowing component is important for residence time and transport, especially in the upper reaches of the estuary where the wet season river flux is much larger than the local exchange flow.

<img src="/assets/img/Fig9.png" alt="ex" width="700"/>

We also studied how connecting tributaries to the main stem of the estuary mix the water from the main stem and the local fresher water from tributary rivers. Because the main stem's river flux is much larger, fresher water can be imported into tributaries from the main stem, and mixed water will be exported. To study these features we used a variation of TEF extended to more than two salinity classes.

This work is [published in the Journal of Physical Oceanography](https://journals.ametsoc.org/doi/abs/10.1175/JPO-D-19-0108.1) with coauthors Dave Sutherland and [Dave Ralston](https://www2.whoi.edu/staff/dralston/). I put some FVCOM setup and processing codes [here](https://github.com/tedconroy/ocean-model-codes).

**References**

Sutherland, D.A. and O'Neill, M.A., 2016. Hydrographic and dissolved oxygen variability in a seasonal Pacific Northwest estuary. Estuarine, Coastal and Shelf Science, 172, pp.47-59.

MacCready, P., 2011. Calculating estuarine exchange flow using isohaline coordinates. Journal of Physical Oceanography, 41(6), pp.1116-1124.
