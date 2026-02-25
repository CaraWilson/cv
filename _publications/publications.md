---
layout: single   
title: "Publications"
permalink: /publications/
author_profile: true
---

<style>
  .filter-btn {
    background-color: #f1f1f1;
    border: none;
    color: #333;
    padding: 8px 16px;
    text-align: center;
    text-decoration: none;
    display: inline-block;
    font-size: 14px;
    margin: 4px 2px;
    cursor: pointer;
    border-radius: 4px;
    transition: 0.3s;
  }
  .filter-btn:hover { background-color: #ddd; }
  .active { background-color: #2c3e50; color: white; }
  
  ol.reversed-list {
    display: flex;
    flex-direction: column;
  }
  ol.reversed-list li {
    margin-bottom: 12px;
  }
  ol.reversed-list a {
    color: #2980b9;
    text-decoration: none;
  }
  ol.reversed-list a:hover {
    text-decoration: underline;
  }
</style>

<div id="categoryButtons" style="margin-bottom: 15px;">
  <button class="filter-btn active" onclick="filterCategory('all', this)">Show All</button>
  <button class="filter-btn" onclick="filterCategory('satellite', this)">Satellite Oceanography</button>
  <button class="filter-btn" onclick="filterCategory('fisheries', this)">Fisheries</button>
  <button class="filter-btn" onclick="filterCategory('southern-ocean', this)">Southern Ocean</button>
  <button class="filter-btn" onclick="filterCategory('blooms', this)">Chlorophyll Blooms</button>
  <button class="filter-btn" onclick="filterCategory('hydrothermal', this)">Hydrothermal</button>
  <button class="filter-btn" onclick="filterCategory('other', this)">other</button>
</div>

<input type="text" id="pubSearch" onkeyup="filterPubs()" placeholder="Search by keyword, year, or co-author..." style="width: 100%; padding: 12px; margin-bottom: 20px; border: 1px solid #ccc; border-radius: 4px;">

<script>
let currentCategory = 'all';

function filterCategory(category, btn) {
  currentCategory = category;
  let buttons = document.getElementsByClassName("filter-btn");
  for (let b of buttons) { b.classList.remove("active"); }
  btn.classList.add("active");
  filterPubs();
}

function filterPubs() {
  let input = document.getElementById('pubSearch');
  let filter = input.value.toUpperCase();
  let ol = document.getElementsByClassName("reversed-list")[0];
  let li = ol.getElementsByTagName('li');

  for (let i = 0; i < li.length; i++) {
    let txtValue = li[i].textContent || li[i].innerText;
    let categories = li[i].getAttribute('data-category') || "";
    let matchesSearch = txtValue.toUpperCase().indexOf(filter) > -1;
    let matchesCategory = (currentCategory === 'all' || categories.includes(currentCategory));

    li[i].style.display = (matchesSearch && matchesCategory) ? "" : "none";
  }
}
</script>

<ol reversed class="reversed-list">
  <li data-category="southern-ocean"><b>Wilson, C.</b>, J. Hinke and M. Mazloff (2025), Long-distance winter migrations of chinstrap penguins and elephant seals to a persistent bloom at the edge of the Ross Gyre, Scientific Reports, <a href="https://doi.org/10.1038/s41598-025-87433-6">https://doi.org/10.1038/s41598-025-87433-6</a>.</li>
  <li data-category="satellite fisheries "><b>Wilson, C.</b>, and D. H. Robinson (2022) Satellite Monitoring of Sea Surface Temperature and Chlorophyll for Sustainable Fishing ERDDAP, Proceeding of the 2022 IEEE International Geoscience and Remote Sensing Symposium</li>
  <li data-category="blooms"><b>Wilson, C.</b> (2021), Evidence of Episodic Nitrate Injections in the Oligotrophic North Pacific Associated with Surface Chlorophyll Blooms, Journal of Geophysical Research: Oceans. 126, e2021JC017169. <a href="https://doi.org/10.1029/2021JC017169">https://doi.org/10.1029/2021JC017169</a>.</li>
  <li data-category="fisheries satellite">Welch, H., S. Brodie, M.G. Jacox, D.H. Robinson, <b>C. Wilson</b>, et al. (2020) Considerations for transferring an operational dynamic ocean management tool between ocean color products. Remote Sensing of the Environment. 242, 111753.<a href="https://doi.org/10.1016/j.rse.2020.111753">https://doi.org/10.1016/j.rse.2020.111753</a>.</li>
  <li data-category="other"><b>Wilson, C.</b>, D. H. Robinson and R.A. Simons (2020) ERDDAP: Providing easy access to remote sensing data for scientists and students, Proceeding of the 2020 IEEE International Geoscience and Remote Sensing Symposium</li>
  <li data-category="fisheries satellite"><b>Wilson, C.</b>, D.H. Robinson and S.K. Shotwell (2020) Overcoming Barriers to the use of Satellite data in Fisheries Management, Proceeding of the 2020 IEEE International Geoscience and Remote Sensing Symposium.</li>
  <li data-category="satellite"><b>Wilson, C.</b>, Robinson, D.H. (2019) Lessons Learned from the NOAA CoastWatch Ocean Satellite Course Developed for Integrating Oceanographic Satellite data into Operational Use. <a href="https://doi.org/10.3390/ijgi8080354">https://doi.org/10.3390/ijgi8080354</a></li>
  <li data-category="blooms">Anderson E.E., <b>C. Wilson</b>, A. H. Knap and T. A. Villareal (2018), Summer diatom blooms in the eastern North Pacific gyre investigated with a long-endurance autonomous surface vehicle. <a href="https://doi.org/10.7717/peerj.5387">https://doi.org/10.7717/peerj.5387</a></li>
  <li data-category="satellite">Eguchi, T., et al. (including <b>Cara Wilson</b>) (2018), Loggerhead turtles (Caretta caretta) in the California Current: abundance, distribution, and anomalous warming. <a href="https://doi.org/10.3389/fmars.2018.00452">https://doi.org/10.3389/fmars.2018.00452</a></li>
  <li data-category="satellite">Lotliker, A.A., et al. (including <b>C. Wilson</b>) (2018), Noctiluca blooms are not associated with hypoxia in the Northeastern Arabian Sea. Harmful Algae, 74, 46-57.<a href="https://doi.org/10.1016/j.hal.2018.03.008">https://doi.org/10.1016/j.hal.2018.03.008</a></li>
  <li data-category="satellite">Lee, Z., et al. (including <b>C. Wilson</b>) (2018), Global water clarity: continuing a century-long monitoring, Eos, 99, <a href="https://doi.org/10.1029/2018EO097251">https://doi.org/10.1029/2018EO097251</a></li>
  <li data-category="satellite">Qi, L., C. Hu, M. Wang, S. Shang and <b>C. Wilson</b> (2017), Floating algae blooms in the East China Sea, Geophys. Res. Lett., <a href="https://doi.org/10.1002/2017GL075525">https://doi.org/10.1002/2017GL075525</a></li>
  <li data-category="satellite fisheries"><b>Wilson, C.</b>, et al. (2016) Southern right whale calf mortality at Península Valdés, Argentina: are harmful algal blooms to blame?, <a href="https://doi.org/10.1111/mms.12263">https://doi.org/10.1111/mms.12263</a>.</li>
  <li data-category="satellite">Rose, R.A., et al. (including <b>C. Wilson</b>) (2014). Ten Ways Remote Sensing Can Contribute to Conservation. <a href="https://doi.org/10.1111/cobi.12397">https://doi.org/10.1111/cobi.12397</a></li>
  <li data-category="satellite">Villareal, T.A. & <b>C. Wilson</b> (2014) A comparison of the Pac-X trans-Pacific Wave Glider data and satellite data. <a href="https://doi.org/10.1371/journal.pone.0092280">https://doi.org/10.1371/journal.pone.0092280</a>.</li>
  <li data-category="fisheries">Fernadez, D. & <b>C. Wilson</b> (2013), User Engagement and Requirements, IOOS 2012 Summit Report.</li>
  <li data-category="blooms"><b>Wilson, C.</b>, et al. (2013). Chlorophyll bloom development and the Subtropical Front in the North Pacific, <a href="https://doi.org/10.1002/jgrc.20143">https://doi.org/10.1002/jgrc.20143</a></li>
  <li data-category="blooms">Krause, J.W., et al. (including <b>C. Wilson</b>) (2013), Biogenic silica cycling during summer phytoplankton blooms in the North Pacific subtropical gyre. Deep-Sea Research I, 71, 49-60.<a href="https://doi.org/10.1016/j.dsr.2012.09.002">https://doi.org/10.1016/j.dsr.2012.09.002</a></li>
  <li data-category="blooms">Krause, J.W., et al. (including <b>C. Wilson</b>) (2012) Increased kinetic efficiency for silicic acid uptake, Limnology & Oceanography, 57,1084-1098.<a href="https://doi.org/10.4319/lo.2012.57.4.1084">https://doi.org/10.4319/lo.2012.57.4.1084</a></li>
  <li data-category="blooms">Villareal, T.A., et al. (including <b>C. Wilson</b>) (2012) Summer diatom blooms in the North Pacific Subtropical Gyre: 2008-2009. <a href="https://doi.org/10.1371/journal.pone.0033109">https://doi.org/10.1371/journal.pone.0033109</a></li>
  <li data-category="blooms"><b>Wilson, C.</b> (2011), Chlorophyll anomalies along the critical latitude at 30°N in the NE Pacific, <a href="https://doi.org/10.1029/2011GL048210">https://doi.org/10.1029/2011GL048210</a></li>
  <li data-category="blooms">Villareal, T., L. Adornato, <b>C. Wilson</b>, & C. Schoenbaechler (2011), Summer blooms of diatom-diazotroph assemblages (DDAs), <a href="https://doi.org/10.1029/2010JC006268">https://doi.org/10.1029/2010JC006268</a></li>
  <li data-category="fisheries satellite"><b>Wilson, C.</b> (2011) The rocky road from research to operations for satellite ocean-colour data in fishery management. <a href="https://doi.org/10.1093/icesjms/fsq168">https://doi.org/10.1093/icesjms/fsq168</a>.</li>
  <li data-category="satellite">Yoder, J.A., S.C. Doney, D.A. Siegel, & <b>C. Wilson.</b> (2010) Study of Marine Ecosystems and Biogeochemistry Now and in the Future. Oceanography, 23(4), 128-141.</li>
  <li data-category="fisheries satellite"><b>Wilson, C.</b> (2010) Fisheries, Encyclopedia of Remote Sensing.</li>
  <li data-category="fisheries satellite"><b>Wilson, C.</b>, et al. (2009). Remote Sensing Applications to Fisheries Management. IOCCG report #8.</li>
  <li data-category="fisheries satellite">Bundy, A., et al. (including <b>C. Wilson</b>) (2009) Building Links with the Fishing Communities, IOCCG report #8.</li>
  <li data-category="fisheries satellite"><b>Wilson, C.</b>, et al. (2008). Ocean Colour Radiometry and Fisheries, IOCCG report #7.</li>
  <li data-category="satellite">Hoepffner, N., <b>C. Wilson</b>, & S. Lavender (2008). Ocean Colour and Climate Change, IOCCG report #7.</li>
  <li data-category="satellite">Hoepffner, N., et al. (including <b>C. Wilson</b>) (2008). Biogeochemical Cycles, IOCCG report #7.</li>
  <li data-category="blooms"><b>Wilson, C.</b> & X. Qiu (2008). Global distribution of summer chlorophyll blooms in the oligotrophic gyres. Prog. Ocean., 78, 107-134.</li>
  <li data-category="blooms"><b>Wilson, C.</b>, et al. (2008). Biological and physical forcings of late summer chlorophyll blooms at 30°N. <a href="https://doi.org/10.1016/j.jmarsys.2005.09.018">https://doi.org/10.1016/j.jmarsys.2005.09.018</a>.</li>
  <li data-category="fisheries satellite">Friedl, L., <b>C. Wilson</b>, et al. (2006), Using Satellite Data Products to Manage Living Marine Resources, EOS, 87(41), 437.</li>
  <li data-category="satellite"><b>Wilson, C.</b> and V.J. Coles (2005). Global climatological relationships between satellite biological and physical observations. <a href="https://doi.org/10.1029/2004JC002724">https://doi.org/10.1029/2004JC002724</a>.</li>
  <li data-category="fisheries">Hinke, J.T., D.G. Foley, <b>C. Wilson</b> & G.M. Watters (2005), Persistent habitat use by Chinook salmon, Mar. Ecol. Prog. Ser., 304, 207-220.</li>
  <li data-category="satellite">Bograd, S.J., et al. (including <b>C. Wilson</b>) (2004). On the seasonal and interannual migrations of the Transition Zone Chlorophyll Front. <a href="https://doi.org/10.1029/2004GL020637">https://doi.org/10.1029/2004GL020637</a></li>
  <li data-category="satellite">Coles, V.J., <b>C. Wilson</b> & R.R. Hood (2004). Remote sensing of new production fueled by nitrogen fixation. <a href="https://doi.org/10.1029/2003019018">https://doi.org/10.1029/2003019018</a></li>
  <li data-category="blooms"><b>Wilson, C.</b> (2003). Late summer chlorophyll blooms in the oligotrophic North Pacific subtropical gyre. <a href="https://doi.org/10.1029/2003GL017770">https://doi.org/10.1029/2003GL017770</a></li>
  <li data-category="satellite"><b>Wilson, C.</b> & D. Adamec (2002). A global view of bio-physical coupling from SeaWiFS and TOPEX, <a href="https://doi.org/10.1029/2001GL014063">https://doi.org/10.1029/2001GL014063</a>.</li>
  <li data-category="satellite"><b>Wilson, C.</b> & D. Adamec (2001). Correlations between surface chlorophyll and sea surface height in the tropical Pacific. J. Geophys. Res., 106, 31,175-31,188.</li>
  <li data-category="hydrothermal southern-ocean">Klinkhammer, G.P., et al. (including <b>C. Wilson</b>) (2001). Discovery of new hydrothermal vent sites in Bransfield Strait, Antarctica.</li>
  <li data-category="hydrothermal southern-ocean"><b>Wilson, C.</b>, G.P. Klinkhammer, & C.S. Chin (1999). Hydrography of the Central and East Basins of the Bransfield Strait, Antarctica. J. Phys. Ocean., 29: 465-479.</li>
  <li data-category="other">Ashjian, C. J., et al. (including <b>C. Wilson</b>) (1998). Diel vertical migration of zooplankton biomass. Cont. Shelf Res., 18, 831-858.</li>
  <li data-category="hydrothermal">Biscoito, M., et al. (including <b>C. Wilson</b>), eds (1998). Proceedings of the first international symposium on deep-sea hydrothermal biology.</li>
  <li data-category="hydrothermal">Chin, C. S., G. P. Klinkhammer & <b>C. Wilson</b> (1998). Detection of hydrothermal plumes on the northern MAR. Earth Planet. Sci. Lett.</li>
  <li data-category="hydrothermal">Langmuir, C. L., et al. (including <b>C. Wilson</b>) (1997). Hydrothermal vents near a mantle hot spot: Lucky Strike vent field at 37°N.</li>
  <li data-category="other">Klinkhammer, G.P., et al. (including <b>C. Wilson</b>) (1997). Distributions of dissolved manganese and fluorescent DOM in the Columbia River estuary.</li>
  <li data-category="other">Klinkhammer G. P., <b>C. Wilson</b>, et al. (1996). Dissolved humic organic matter in the Columbia River estuary.</li>
  <li data-category="hydrothermal"><b>Wilson, C.</b>, et al. (1996). Hydrothermal anomalies at Lucky Strike (37°17'N), on the Mid-Atlantic Ridge. Earth Planet. Sci. Lett.</li>
  <li data-category="hydrothermal">Klinkhammer, G. P., et al. (including <b>C. Wilson</b>) (1995). Venting from the Mid-Atlantic Ridge at 37°17'N.</li>
  <li data-category="hydrothermal"><b>Wilson, C.</b>, et al. (1995). Hydrography above the Mid-Atlantic Ridge (33°-40°N) and within the Lucky Strike segment.</li>
  <li data-category="other">Falkowski, P. G., et al. (including <b>C. Wilson</b>) (1992). Natural versus anthropogenic factors affecting low-level cloud albedo. Science.</li>
  <li data-category="other">Falkowski, P. G. and <b>C. Wilson</b> (1992). Phytoplankton productivity in the North Pacific Ocean since 1900. Nature.</li>
  <li data-category="other"><b>Wilson, C.</b> and D. W. R. Wallace (1990). Using the nutrient ratio NO/PO as a tracer of continental shelf waters in the central Arctic Ocean.</li>
</ol>
