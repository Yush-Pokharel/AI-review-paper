## Wiley Interdisciplinary Reviews: Water

## SYSTEMATIC REVIEW OPEN ACCESS

# Remote Sensing for Monitoring Macroplastics in Rivers: A Review

Ashenafi Tadesse Marye1,2| Cristina Caramiello³ | Dario De Nardi⁴ | Domenico Miglino³ | Gaia Proietti⁵ | Khim Cathleen Saddi3,6,7| Chiara Biscarini⁵ | Salvatore Manfreda³ | Matteo Poggi⁴ | Flavia Tauro⁸

1 Department of Economics, Engineering, Society, and Business Organization, University of Tuscia, Viterbo, Italy |2Department of Natural Resources Management, College of Agriculture and Environmental Sciences, University of Gondar, Gondar, Ethiopia |3Department of Civil, Architectural and Environmental Engineering, University of Naples Federico II, Naples, Italy |4Department of Computer Science and Engineering, University of Bologna, Bologna, Italy |5UNESCO Chair in Water Resources Management and Culture, University for Foreigners of Perugia, Perugia, Italy |6Istituto Universitario di Studi Superiori IUSS Pavia, Pavia, Italy |7Department of Civil Engineering and Architecture, Ateneo de Naga University, Naga, Philippines |8Department for Innovation in Biological, Agro-Food and Forest Systems, University of Tuscia, Viterbo, Italy

**Correspondence:** Flavia Tauro (flavia.tauro@unitus.it)

**Received:** 24 September 2024 | **Revised:** 28 February 2025 | **Accepted:** 7 March 2025

**Associate Editor:** Qiuhong Tang | **Editor-in-Chief:** Wendy Jepson

**Funding:** We gratefully acknowledge financial support provided by: the Italian Ministry of University and Research under the PRIN project 2022MMBA8X “RiverWatch: a citizen-science approach to pollution monitoring”—CUP J53D23002260006, grant agreement no. 961, 06/30/2023; ECS 0000024 Rome Technopole—CUP B83C22002820006, PNRR Mission 4 Component 2 Investment 1.5, funded from the European Union (EU) Next-Generation EU; and RETURN Extended Partnership funded from the Next-Generation EU (National Recovery and Resilience Plan NRRP, Mission 4, Component 2, Investment

1.3 – D.D. 1243 2/8/2022, PE0000005). **ABSTRACT** **Keywords:** Plastics | remote sensing | rivers | satellite | Unmanned Aerial Systems Given the exponential rise in global plastic production and its significant ecological and socio-
economic impacts, monitoring macroplastics in rivers has become a central focus of water management efforts. However, standardized monitoring methodologies are lagging behind the rate of plastic waste currently entering aquatic systems on a global scale. This translates into a shortage of spatially and temporally refined data on the macroplastic pollution circulating in inland waters. Recent advancements in remote sensing techniques, primarily satellites, UASs, fixed and handheld cameras combined with crowd- sourced data and automated macroplastic detection using machine and deep learning, offer promising opportunities for versatile monitoring solutions. Thus, this paper reviews state- of- the- art approaches and emerging methods for macroplastic identification in rivers to provide researchers with a comprehensive inventory of techniques and to encourage the scientific community to harmonize monitoring methods and define standard protocols. According to our investigation, addressing the challenges of remote sensing- **1 | Introduction** Europe-Plastic  2024), and is expected to double again by 2050 based river macroplastics monitoring mandates further efforts to enhance and integrate multiple platforms with an emphasis on (Stegmann et  al.  2022). In 2019 alone, over 18% of plastic re-Since the 1950s, over 8000 million tonnes (Mt) of plastics have long-term monitoring. sulted in mismanaged waste, with 6.1 Mt ended up in rivers, been produced globally (OECD 2022). Over the past two decades, lakes, and oceans, exceeding prior annual discharge estimates production nearly doubled from 234 to over 400 Mt (OECD 2022; (0.41–4 Mt per year) (Jambeck et al. 2015; Lebreton et al. 2017;

This is an open access article under the terms of the Creative Commons Attribution License, which permits use, distribution and reproduction in any medium, provided the original work is properly cited. © 2025 The Author(s). *WIREs Water* published by Wiley Periodicals LLC.

*Wiley Interdisciplinary Reviews: Water,* 2025; 12:e70020 1 of 21 [https://doi.org/10.1002/wat2.70020](https://doi.org/10.1002/wat2.70020)

Schmidt et al. 2017; Meijer et al. 2021; Gallitelli and Scalici 2022). Rivers also act as reservoirs or sinks for plastics (Tramoy, Gasperi, Colasse, Silvestre, et al. 2020; van Emmerik, Mellink, et  al.  2022; Mennekes et  al.  2024; Oswald et  al.  2025). Plastic pollution poses a major threat to our planet's health (MacLeod et al. 2021; Fletcher et al. 2023). The implications of recently es- calating plastic pollution are alarming not only for the marine and freshwater ecosystems (Bucci et  al.  2020; Azevedo-Santos et al. 2021; González-

Fernández et al. 2021; Battisti et al. 2023;

MacAfee and Löhr  2024) but also for the socioeconomic well-being of global communities. Besides the direct dumping into water bodies, mismanagement of terrestrial plastics feeds such debris to rivers (Liro et al. 2020; Tramoy et al. 2020), a process further exacerbated during flash floods (Roebroek et  al.  2021; van Emmerik, Kirschke, et  al.  2023; MacAfee and Löhr  2024; Cózar et  al.  2024). Furthermore, in urban areas, plastic debris clogs drainage systems, increasing the risk of flooding (Lebreton and Andrady  2019; Honingh et  al.  2020; Nepal and Bharadwaj 2022). Altogether, these phenomena are expected to increase with climate change (MacAfee and Löhr 2024).

Internationally, stakeholders are working to reduce plastic pollution in aquatic and terrestrial ecosystems (Da Costa et al. 2020; Knoblauch and Mederake  2021; Dauvergne  2023). However, global monitoring efforts, particularly in freshwater systems, remain limited (Winton et al. 2020; Earn et al. 2021; Kirschke the literature, three broad plastic categories are typically de ( *<* 5mm) (Browne  2015-; fined based on size: microplastics Andrady  2017; Lusher et  al.  2017), macroplastics ( ≥ 5mm) (Kawecki and Nowack  2019), and megaplastics ( *>* 1000mm) (Lusher et al. 2017; GESAMP 2019). In some instances, the additional category of mesoplastics is adopted to refer to materials ranging from 5 to 25 mm (Lusher et  al.  2017; GESAMP  2019; Nihei et al. 2024). As illustrated in Figure 1, research on freshwater plastic pollution has increased in recent years; however, much of the scientific focus remains on microplastics (Blettler et  al.  2018; Gallitelli and Scalici  2022; Zhao et  al.  2024). Most likely, this attention is related to detection advancements as well as increased awareness of their ecological and human health implications, including ecotoxicology, risk assessment and total environmental health (Lusher et al. 2021; Rochman 2018).

Monitoring plastic dynamics is vital for informed decision-making and assessing mitigation efforts. Yet, a lack of standardized methods for macroplastic monitoring is the bottleneck to draw concrete indications on river plastic movement (Hurley et al. 2023). This leads to limited data with insufficient spatial and temporal coverage. According to recent studies, macroplastics that leak into rivers persist for decades or even centuries (van Emmerik, Mellink, et al. 2022; Mennekes et al. 2024). They are often transformed into microplastics due to fragmentation and photodegradation (European-Parliament 2018; Tursi et al. 2022; Liro et  al.  2023; Huang and Xia  2024). Once converted into

et  al.  2023; Nava et  al.  2023). Despite the lack of consensus in

ications 100 Microplastic

Macroplastic

bl Pu

**FIGURE 1** | Number of studies on micro- and macro-

## 2 of 21

Ye ars

plastics in freshwater (June 2024, Web of Science).

*Wiley Interdisciplinary Reviews: Water,* 2025 smaller particles, plastics are extremely difficult to track and remove. On the other hand, macroplastics can be monitored through several techniques, including visual observation, physical interception, remote sensing, and underwater sensing (Gallitelli, Girard, et  al.  2024). However, many of these methods remain in the early stages of development (van Emmerik and Schwarz  2020). Environmental practice largely relies on either visual observations or physical interception. In visual observations, operators directly assess floating and partially submerged plastics, providing insight into their types, sizes, and loads (González-Fernández and Hanke  2017; Castro-Jiménez et al.  2019; González-Fernández et al.  2021; Pinto et al.  2024). Although cost-effective, this method can be resource- intensive for long-term monitoring and susceptible to detection biases. In contrast, physical interception actively traps plastic debris using nets or passive barriers like booms (Cowger et al. 2022; Vriend et al. 2020; Blettler et al. 2023). The effectiveness of these methods depends on factors like deployment location, net and mesh dimensions, and flow conditions (Wendt-Potthoff et  al.  2020; Hurley et  al.  2023). Although physical interception provides tangible data on plastic pollution, it requires multiple points in larger rivers and faces challenges for frequent application due to operational costs, possible risks and logistical difficulties.

Alternatively, recent advancements in remote monitoring, artificial intelligence, citizen science, and crowd- sourced data offer significant potential for improving river systems monitoring (Tauro et  al.  2018; Manfreda et  al.  2024). Particularly, remote sensing-based monitoring (through satellite, Unmanned

based systems) provides a scalable solution for frequent and objective observations. Remote sensing methods can be integrated with data- driven algorithms such as machine learning (ML) and deep learning (DL), hold promise in unsupervised identification of floating macroplastics types, and can enhance reliability in detection and quantification over time (Jakovljevic et al.  2020; Wendt-Potthoff et al. 2020; Wolf et al. 2020; Iordache et al. 2022; Solé Gómez et  al.  2022; Tasseron et  al.  2022; Jia et  al.  2023; Mohsen et al. 2023; Sakti et al. 2023). However, despite these advantages, such methods are relatively unexplored in river systems (Geraeds et al. 2019; Solé Gómez et al. 2022) compared to their use in marine environments (Waqas et al. 2023).

Towards improving monitoring practices, this paper offers a systematic review of emerging remote sensing methods and tools to tackle macroplastic identification in riverine environments. This review specifically focuses on buoyant macroplastics within river systems, excluding underwater and other environments such as marine and terrestrial ecosystems. It emphasizes image acquisition methodologies, detailing the platforms used, including satellites, UAS, and fixed or handheld cameras. In addition, we examine data collection processes and image analysis methods. Our objectives are twofold: from one perspective we aim to provide researchers and practitioners with a comprehensive inventory of techniques applicable to diverse experimental settings; and from another perspective given the urgent need for reliable and consistent methodologies, this review aims to support the development of effective and comparable monitoring strategies.

This review is organized as follows. In Section 2, we present rou- tinely adopted techniques for assaying macroplastics in rivers;

## 2 | The State of the Art

in Section

**2.1 | Visual Observations** 3, we focus on remote image-
based methods as well as on the analytical tools currently available to sense plastics in Visual observations entail inspection, quantification, and catego-

images; in Section rization of floating and slightly submerged macroplastics in riv 4, we critically point out advantages and lim-- ers by operators. This method allows to directly assess the type, itations of the reviewed methods, and in Section 5, we provide a dimensions, and characteristics of plastic pollution (González-conclusion and outlook. Fernández and Hanke 2017; Castro-Jiménez et  al.  2019; González-Fernández et  al.  2021; Pinto et  al.  2024). It is relatively inexpensive since it does not require special equipment. However, producing fine- scale, long-term data with this method can become both cost- and labor- intensive. As demonstrated by the RIMMEL project and census by the Italian Ministry for Ecological Transition and SNPA (Vighi et al.  2022; JRC  2016), in spite of their simplicity, visual observations have proven effective for large-scale and long-term monitoring. However, the efficacy of this approach relies on several aspects associated with the configuration of the monitoring site and sampling timing. First, it is essential to conduct the observations from a monitoring location that accurately captures most of the river section while guaranteeing that even small objects are seen. For instance, surveys are frequently performed from an elevated po- sition like a bridge or along the riverside (Pinto et al. 2024). The

near the river mouth could be ideal for transport studies (van Emmerik, van Klaveren, et al. 2020; Kuizenga et al. 2023). The height of the observation point controls the smallest detectable plastic size (Castro-Jiménez et  al.  2019), while the bridge's dimensions determine the width of the observable section. Second, since flow velocity variations (along with the river section morphology) influence plastic waste accumulation and transport, the sampling duration and frequency of visual observations should adapt to flow changes. While the duration of monitor ( *>* 1000 items ∕ h), sampling duration typically ranges-from 1 to 2 ing surveys also depends on the plastic load (van Emmerik, van min per section, while for lower loads (100 items ∕ h), it ranges up to 15 Klaveren, et al. 2020 min per section (Wendt- ), it is usually recommended that observa Potthoff et al. 2020). - Bias and errors may arise from missing or misidentifying plas tions are performed at least hourly for rivers with significant-tics, especially small or transparent objects (Castro-flow changes. Ideally, the number of surveys should be propor-Jiménez et al. tional to the number of monitored sections. For high plastic load

2019), and accuracy may decrease due to water turbidity,
rivers sun glare, as well as during periods of high plastic loads and extended observation times (van Emmerik, de Lange, et al. 2022; Kuizenga et al. 2023). Towards mitigating such errors, it is usually preferred to conduct surveys in teams (including at least an observer and a recorder) (Pinto et al. 2024), and to use binocu- lars (Cesarini et al. 2023). To minimize subjectivity and improve accuracy, however, adopting alternative methods, such as cameras for passive counting or DL (van Lieshout et al. 2020) as well as combining observations with physical interception methods 3 of 21

Aerial Systems [UASs], and fixed or handheld camera- choice of the river section also affects the results: selecting a spot (Kuizenga et  al.  2023), is recommended. Citizen science has proven an effective approach to acquiring larger visual observation datasets of river channels and riversides (Rech et al. 2015; Kiessling et al. 2019; van Emmerik, Roebroek, et al. 2020; van Emmerik, Seibert, et  al.  2020; Honorato-Zimmer et  al.  2021; Kiessling et al. 2021; Liro, Zielonka, Hajdukiewicz, et al. 2023). Various riverside macroplastic monitoring protocols have been developed. Some adopt procedures originally designed for marine plastic monitoring, such as OSPAR Beach and NOAA Beach Litter (OSPAR 2010; Lippiatt et al. 2013; van Emmerik, Vriend, et  al.  2020), while others rely on newly developed approaches, including Plastic Pirates, CrowdWater (Kiessling et al. 2019; van Emmerik, Seibert, et al. 2020), and harmonized techniques particularly designed for riparian environments (Gallitelli, Cutini, et al. 2024). It is important to note that balancing between im- precise measurements or human biases and citizen participation is crucial.

## 2.2 | Physical Interception

Unlike noninvasive visual observations, physical interception involves trapping and removing plastic debris from rivers using physical barriers. Physical interception can be classified as active sampling, which uses equipment such as nets (Cowger et al. 2022), and passive sampling, which relies on existing infra- structure such as booms (Vriend et al. 2020; Blettler et al. 2023). Nets, which are meshed screens or bags, can be fixed at bridges (van Emmerik et al. 2019; Cowger et al. 2022) or deployed from riverbanks (Moore et  al.  2011; Munari et  al.  2021) and boats (Karpova et  al.  2022; Oswald et  al.  2023), and positioned at different depths to capture various plastic transport pathways. Additionally, they can be deployed in fleets to sample different parts of the water column (Blondel and Buschman 2022; Hurley et  al.  2023; Oswald et  al.  2023). The quantity of macroplastics intercepted by nets relies on variables such as net dimensions, mesh size, deployment site, and water flow conditions (Wendt-Potthoff et al. 2020; Hurley et al. 2023). A flow velocity greater than 1m∕ s can be powerful, while lower flow velocities may not be sufficient to keep the net properly positioned, thus hindering effective plastic collection (van Emmerik and Schwarz  2020). Booms are floating barriers designed to gather natural and non-natural materials across sections of a river channel. While they are primarily used for clean-up and pollution prevention, a few studies have explored their use for sampling purposes and evaluated their effectiveness in controlling macroplastic pollution (Blettler et  al.  2023; Hurley et  al.  2023). These studies involve isolating, counting, categorizing, and weighing the collected plastic material (Malik et al. 2020; Vriend et al. 2020; Sari et al.  2022; Blettler et al.  2023). Booms can also include a mesh or screen to catch debris just below the water's surface (Sari et al. 2022). River macroplastic monitoring using physical interception involves diverse duration, frequencies, deployment locations, and depth. For instance, monitoring is different for large rivers compared to small streams. Large rivers may need several monitoring spots across their width, while small streams can often be sampled from the bank or by wading.

The duration may vary within short intervals lasting minutes or less (Moore et al. 2011; Weideman et al. 2020), to extended periods lasting up to a few days (Morritt et al. 2014), with frequency 4 of 21

guided by monitoring objectives and resource constraints. Similarly, it may be possible to select multiple monitoring sites at the same river cross- section depending on the specific purpose of the campaign, that is, if the survey aims to collect comprehensive data or evaluate cross- sectional variability. Rivers with del- tas and intermittent streams require flexible and ad hoc designed monitoring approaches (Wendt-Potthoff et al. 2020). Among the advantages of physical interception, the possibility to provide direct and tangible data on plastic pollution is certainly a valuable asset. However, practical difficulties, costs, and possible risks to **3 | Remote Sensing** operators may hamper frequent implementations. Image-based monitoring in freshwater settings can provide large scale spatial coverage at potentially frequent temporal resolutions. A bibliographic search was conducted using Web of Science and Google Scholar with various keyword combi- nations, including “river litter,” “river debris,” “plastic debris,” “macroplastics,” “remote sensing,” “drones,” “Unmanned Aerial Vehicles,” “cameras,” “machine learning,” and “deep learning.” After removing duplicates and excluding studies outside the scope of this review (e.g., those focusing on marine, soil, biota or other plastic size categories), research articles specifically addressing the use of remote sensing for monitoring buoyant macroplastics in river systems were selected. Upon careful evaluation of the identified studies, only peer- review articles providing sufficient methodological details for accurate interpretation were included. As a result, a total of 16 studies were retrieved. Most of the literature emerged between 2022 and 2023, indicat- ing a recent surge in research interest in this field.

The platforms used by these studies so far can be categorized into three types: spaceborne, airborne (UAS), and ground-based (fixed and handheld cameras). All the reviewed studies utilized passive sensors, relying on naturally available energy, across various platform types, except one study that used an active sensor that generates its own illumination, from a spaceborne platform (Simpson et al. 2022). Within the reviewed studies, 20% utilized only satellite or spaceborne platforms (Solé Gómez et al. 2022; Simpson et al. 2022; Mohsen et al. 2023; Sakti et al. 2023). 40% used airborne platforms, such as UASs at different elevations and resolutions (Geraeds et al. 2019; Jakovljevic et al. 2020; Wolf et al. 2020; Cortesi et al. 2022; Maharjan et al. 2022; Schreyers et al. 2021). These studies predominantly used the visible spectral range. Only one study integrated data from both satellites (Sentinel- 2 and Pleiades) and UASs (Sakti et al. 2023). Ground-based cameras mounted on a fixed location, such as bridges (van Lieshout et  al.  2020; Iordache et  al.  2022), masts, or handheld (De Giglio et al. 2020), accounted for 33% of the analyzed papers. Approximately half of the studies with ground-based platforms also used a combination of fixed and handheld or UAS data; and were conducted in different image-capturing settings, such as natural environment (van Lieshout et al. 2020), semi-controlled experiments in a natural environment (De Giglio et  al. *Wiley Interdisciplinary Reviews: Water,* 2020 2025; Iordache et  al.  2022; Tasseron et  al.  2022; Jia et  al.  2023) and lab-based (Tasseron et  al.  2022). While all spaceborne-based studies utilized multispectral images, ground-based efforts also demonstrated the use of hyperspectral images in detecting river macroplastics (Tasseron et al. 2022). All studies were conducted across various regions globally, reflecting a diverse geographical distribution of research efforts and underscoring the growing recognition of the urgency to address plastic pollution.

## 3.1 | Satellite- and UASs-Based Monitoring

Sensing macroplastics through satellites and drones has involved diverse sensors, experimental setups and data acquisition and processing settings. Table  1 summarizes key studies, focusing on: (i) the platform adopted for data acquisition; (ii) the sensor mounted on the platform; (iii) altitude of data collection; sensor features, such as (iv) spatial resolution and (v) spectral range; (vi) eventual image preprocessing procedures; (vii) area of interest; (viii) targeted plastics class(es); (ix) detection methods; (x) and accuracy assessment.

Satellite-based research demonstrated the feasibility of detecting and quantifying plastic debris accumulation along rivers, river shores, lakes, and reservoirs. As reported in Table  1, the spatial resolution of the satellite versus UASs data varied across the studies. Mainly, moderate- resolution sensors (10 m) of Sentinel 2 were commonly used due to their unique spectral bands in the VIS, NIR, and SWIR ranges, though they struggled in precisely identifying small and dispersed plastic particles in rivers (Solé Gómez et al. 2022; Simpson et al. 2022; Mohsen et al. 2023; Sakti et al. 2023). Higher-resolution yet commercial satellites, such as Pleiades (50 cm) and WorldView- 3 (31 cm), provide finer detail, enhancing detection accuracy. For instance, (Sakti et al.  2023) validated Sentinel- 2 detection performance using Pleiades imager y.

## < 2 cm

with 2–5 Complementary to the large- cm range, depending on altitude and sensor type. At

low altitudes (≤ 90 m), they also allowed detailed categoriza scale monitoring capabilities en-- abled by satellites, UASs-tion, morphological attributes (e.g., size) and quantification of

plastic items. The varying altitudes and multi-based studies leverage detailed spa-tial data and precise detection algorithms (Geraeds et al. altitude data ac 2019-;

quisition mainly depended on the specific objective of the exper Jakovljevic et  al.  2020; Wolf et  al.  2020; Cortesi et  al.  2022-;

iment. For instance, in the pioneering UAS-Maharjan et al. 2022). UASs achieved resolutions often based river plastic monitoring study by Geraeds et  al.  (2019), multi-altitude data acquisition was employed that balanced spatial coverage and detection detail by capturing images at various heights (5, 15, and 63 m for plastic counting, identifying transport hotspots and broader flow analysis and riverbank plastic detection, respectively). Similar approaches were adopted by Schreyers et al. (2021) to unravel the influence of water hyacinths on the transport and accumulation of plastic debris within river ecosystems. It is worth noting that the spatial resolution from such platforms depends not only on altitude but also on camera quality, sensor type and focal length, which can significantly influence the spatial resolution (see Figure 2).

Capturing plastic-specific absorption or reflection traits with

based plastic monitoring. Spaceborne-based studies mainly use multispectral and RGB (visible) imagery, respectively. The effectiveness of UAS-based RGB imaging

primarily depended on the plastic's size, distinctive color, and favorable weather conditions (Maharjan et  al.  2022). RGB imaging lacks data from other wavelengths essential for effective plastic detection. To address this limitation, many UAS-based studies relied on high spatial resolution. However, this approach involved a trade- off in spatial coverage, as images were captured at lower altitudes to achieve higher resolution (Jakovljevic et al. 2020; Wolf et al. 2020). In contrast, multispectral sensors on UAS (RGB, Violet, Red Edge1, Red Edge2, NIR1 [Near-Infrared- 1], NIR2, and NIR3) effectively distinguished floating plastics from water at 80 m altitude (Cortesi et al. 2022).

1150, 1210, 1215, 1400, 1430, and 1460 nm while vegeta-The wavelengths between 1215 and 1732 nm were identified tion absorption peaks at 1450 nm. This enables differentiation as particularly effective in the detection of plastics (Garaba from water and vegetation (Tasseron et  al.  2021). The analy- et  al. sis was also compared to Sentinel- 2018; Garaba and Dierssen  2018 ). Consistently, a hyperspectral study (400–1700 nm) in laboratory settings revealed 2 and Worldview-distinct reflectance and absorption traits for plastics and 3 satellite vegetation in the 950–1700 bands, previously used for river plastic monitoring. (Solé Gómez m range, while water showed al- most no reflectance (Tasseron et  al. et  al.  2022; Simpson et  al.  2022; Mohsen et  al.

2021). Similarly, various
2023; Sakti plastic polymers showed high absorption at wavelengths of et al. 2023). According to Tasseron et al. (2021), Sentinel- 2 bands B5–B8 (705–842 nm) and B10 (1375 nm) were crucial for distinguishing plastics from water and vegetation, and B6 (740 nm) and B8 (842 nm), are fundamental for computing the FDI and detecting floating plastics.

Building on these spectral characteristics of plastics, Solé Gómez et  al.  (2022) utilized Sentinel- 2 imagery to detect plastics in rivers and reservoirs. Their findings align with previ- ous studies: plastics exhibited maximum spectral signatures around B8, B8a (865 nm), and B11 (1610 nm), with a minimum at B9 (940 nm) (see fig. 3 of Solé Gómez et al. (2022) and fig. 4 of Mohsen et al. (2023)). Solé Gómez et al. (2022) also observed a sharp rise in reflectance at 705 nm (B5) in areas with high vegetation cover, which helped differentiate plastics from vegetation. However, rivers near urban areas presented challenges in distinguishing plastics, as construction materials and their sur- roundings exhibited high reflectance values similar to those of plastics, thus complicating the differentiation (Sakti et al. 2023). A similar approach by Mohsen et al. (2023), reported that artificial barriers shared a similar spectral signature with plastic materials, particularly in the SWIR and NIR bands of Sentinel-

2. To
distinguish them, inspecting the 842 and 1610 nm wavelengths, was beneficial since barriers and plastics show opposite spectral signatures.

Despite advances in spaceborne- and UAS-based imaging, plastic detection can still be improved. Hyperspectral imaging, with its detailed spectral capture, enhances plastic identification by leveraging unique absorption and reflection traits. Corbari et  al.  (2020) characterized the spectral signatures of 5 of 21 common polymers found in the Mediterranean Sea, showing that WorldView- 3 and PRISMA hyperspectral images outper- form other alternative satellites for such applications. This capability is critical for identifying different types of plastics and

high spectral resolution is key to advancing remote sensing- and airborne-

**TABLE 1** | Summary of satellite and UASs image-

based studies. **Spectral Spatial Image Area of Detection** **Sources Platform Sensor Altitude range** <u>resolution</u> **preprocessing study Target class(es)** <u>and analysis</u> **Accuracy**

Solé Gómez Satellite Sentinel-2 786 km 13 bands: VIS, 10–60 m Use of ready River Man- made debris Manual IoU and confusion et al. ( 2022) VNIR, SWIR products shores labeling, matrices and Ultra Blue spectral checking, FDI, NDVI, NDWI, U- Net, U- Net3DE, and Deeplab V3+

Simpson Satellite Sentinel-1 ~700 km Center 20 × 5 m Calibration, River, Macroplastic VV, VH ROC et al. ( 2022) SAR frequency: deblurring, lake and intensity, and

5.405GHz and subset creation, reservoir the Ratio of all Bandwidth: multi-looking, pixels, Change 0–100 MHz ellipsoid detection
## correction and systems

co-registration

Sakti Satellite Sentinel-2 786 km 13 bands: VIS, 10–60 m Use of ready Riverbanks Plastic debris R F, Confusion matrix et al. ( 2023) & UAS VNIR, SWIR products Mahalanobis and Kappa and Ultra Blue distance and coefficient adjusted PI

Pleiades 620 km Panchromatic, 5 × 10− 1m Use of ready — — — Used to validate VIS, Deep products the Sentinel-2A Blue, Red Edge analysis and NIR

DJI Phantom 75 × 10− 3km VIS 5 × 10− 2m NA — — — Used to validate 4 Pro the Sentinel-2A analysis

Mohsen Satellite Sentinel-2 786 km 13 bands: VIS, 10–60 m Atmospheric River and Riverine litter PI, FDI, Overall accuracy, *Wiley Interdisciplinary Reviews: Water,* et al. ( 2023) VNIR, SWIR correction; reservoir NDVI, NDWI, precision, recall, and Ultra Blue nearest neighbor ANN, SVM, *F*1-score, and resampling RF, NB Cohen kappa and DT score (K-hat)

(Continues) **TABLE 1** | (Continued)

## Spectral Spatial Image Area of Detection

## Sources Platform Sensor Altitude range <u>resolution</u> preprocessing study Target class(es) <u>and analysis</u> Accuracy

Geraeds UAS DJI Phantom 5 × 10− 3km VIS 1–2× 10− 3m Image River Macroplastic Visual NA et al. ( 2019) 4 Advanced categorization particles (> 2.5cm) interpretation (floating plastic and manual with partially labeling using submerged) Zooniverse Project Builder

Jakovljevic UAS DJI Mavic 12–90 × 10− 3km VIS 4 × 10− 3m Generate River and Floating and U- Net Precision, recall, et al. ( 2020) pro high-resolution reservoir underwater plastic and *F*-score orthophoto using SfM algorithm, manual labeling, multiresolution segmentation using eCognition

Wolf UAS DJI 4 6 × 10− 3km VIS ~2 × 10− 3m Geo-referencing Rivers, Floating and PLD-CNN, Precision, Recall et al. ( 2020) Phantom Pro and mosaicking, waterways washed ashore PLQ-CNN, and *F*1-score photography automated and beaches macroplastic SVM and RF UAS point cloud (diameter> 25 mm) densification, 3D mesh generation, digital surface modeling and orthomosaic

Maharjan UAS DJI 30 × 10− 3km VIS ~1 × 10− 2m Mosaicking River and Floating plastics Manual Mean Average et al. ( 2022) Phantom 4 (creating grid canal labeling and Precision and patches) YOLO: v2, v3, *F*1-Score v4 and v5

Cortesi UAS DJI Matrice 20– VIS and NIR 1.6 & Geometric River Floating plastics Multi-step RF Precision, recall, et al. ( 2022) 80 × 10− 3km 4.2× 10− 2m corrections & accuracy and co-registration *F*1-score

Schreyers UAS DJI Phantom 5–10 × 10− 3km VIS 2 × 10− 3m Image River Floating plastics & Manual NA et al. ( 2021) 4 Pro categorization Aquatic vegetation labeling & 7 of 21 <u>Color filtering</u>

*Note:* Refer to text for acronyms. **FIGURE 2** | Remote sensing of the riverine environment: Illustrating altitude versus resolution in drone (D) and satellite (S) platforms: (Sa)

Sentinel- 2 (Solé Gómez et al. 2022; Sakti et al. 2023; Mohsen et al. 2023); (Sb) Sentinel- 1 SAR (Simpson et al. 2022); (Sc) Pleiades (Sakti et al. 2023); (Da) (Geraeds et  al.  2019; Schreyers et  al.  2021); (Db) (Jakovljevic et  al.  2020); (Dc) (Maharjan et  al.  2022); (Dd) (Sakti et  al.  2023); (De) (Wolf et al. 2020); (Df, Dg) (Cortesi et al. 2022); (Dh) (Jakovljevic et al. 2020). The elevation for both types of platforms is not scaled and images illustrating resolutions were pixelized. differentiating them from other materials in complex environments such as rivers.

Remote sensing raw data often contains errors and noise from de- vice defects and environmental conditions. Image preprocessing corrects these issues to enhance data quality. It includes atmospheric correction, masking, cloud detection, spotting white caps, glare correction, georeferencing, mosaicking, and orthophoto generation. These measures are crucial for preparing images for better classification and effective subsequent analysis. Although most of the satellite-based studies examined did not perform image counting (image interpretation), statistical methods, indices- pre- based approaches, ML, and DL. Visual image interpretation, processing, instead relying on pre- used in UAS-existing products, Mohsen based studies, inspects images to detect and clas- et al. (2023) applied atmospheric correction and nearest- sify plastic debris based on visual traits like shape, color, and neighbor texture. While straightforward, it is labor-resampling techniques on Sentinel- intensive, prone to 2 imagery. Additionally, human error, and requires high spatial resolution. For instance, Simpson et al. (2022) undertook calibration, deblurring, subset cre-Geraeds et al. (2019) used visual image interpretation and com- ation, polarimetric matrices establishment through multi- pared it with visual observations and trawl- looking, net sampling. The ellipsoid correction and co- comparison showed a strong alignment between plastic density registration for single look complex profiles from image interpretation and other methods. However, (SLC) acquisitions of Synthetic Aperture Radar (SAR) data. UAS- discrepancies arose in plastic transport distribution because based imagery required various preprocessing techniques such as visual surveys were conducted for longer periods and at sub- image categorization (Geraeds et  al.  2019; Schreyers et  al.  2021), stantial distances (500 m) from UASs surveys, plastic pathways mosaicking (Wolf et al. 2020; Maharjan et al. 2022), geometric cor- changed during tidal cycles, and potential counting errors were rections, co-registration and area-introduced. Similarly, in Schreyers et al. (2021), the UASs sur-

based object selection to avoid vey method designed by Geraeds et al. (2019) was used. Therein,

false positives from sunlight- plastic items were detected, their size and category determined, induced glare (Cortesi et  al.  2022). and their distribution across the river width and vegetation area Wolf et al. (2020) further performed geo-assessed. The areas of vegetation and plastic were estimated 8 of 21 referencing, point cloud based on flying elevation, image width in pixels, sensor width, *Wiley Interdisciplinary Reviews: Water,* 2025 densification, 3D mesh generation, digital surface modeling, and and camera focal length. Findings highlighted that vegetation orthomosaic creation to generate geometrically corrected im-contributed 78% of plastic transportation in the highly plastic- (VV) and cross- polarization intensity (VH), as well as coherent detectors, specifically, the power difference, power ratio, and Hotelling–Lawley trace detectors. The study achieved a true positive detection rate of 95% with only 0.1% false alarms using coherent detectors from SLC acquisitions, outperforming those using incoherent detectors from Ground Range-Detected acquisitions. Additionally, it reported that VH signals are more effective at identifying floating plastic accumulation in water than VV signals.

In addition to visual interpretation and statistical methods, several studies applied ML algorithms for imagery analysis. These algorithms can be classified based on their learning approach into supervised, unsupervised, semi-supervised, and reinforcement learning algorithms (Omia et  al.  2023). Some of the reviewed studies used supervised learning algorithms, which rely on labeled data to train a model for both classifying and predicting new data. Within this set of approaches, methods such as Random Forest (RF) (Cortesi et  al.  2022; Mohsen et  al.  2023; Sakti et  al.  2023), Mahalanobis distance (MD) (Sakti et  al.  2023), Support Vector Machines (SVM), Naïve Bayes (NB), Decision Tree (DT), and Artificial Neural Network (ANN) (Mohsen et  al.  2023) were applied to classify plastics based on their spectral characteristics. For instance, as shown in Table  1, RF and MD were combined with indices such as the Plastic Index (PI), Adjusted Plastic Index (API), and Normalized Difference Vegetation Index (NDVI) to detect illegal plastic dumping along the Citarum River (Indonesia) (Sakti et al. 2023). Using Sentinel- 2, Pleiades 1a/1b, and UAS images, both RF and MD classifiers detected plastic waste along the riverbanks but had difficulty distinguishing it from ground and buildings due to similar spectral signatures (Sakti et al.  2023). Similarly, the spectral similarity between sun-glare and plastics posed a challenge for the RF classifier in a UAS-based study by Cortesi et al. (2022), resulting in false positives. To address this, the study employed area-based object selection, retaining only objects with an area above a set threshold, which signifi-

resolution images. Additionally, Mohsen et al. (2023) conducted a comprehensive investigation integrating indices such as PI, 100 m² (Mohsen et al. 2023). Floating Debris Index (FDI), Normalized Difference Water

DL algorithms have advanced plastic monitoring capabilities Index (NDWI), and NDVI with ANN, SVM, RF, NB, and DT

in rivers by extracting objects directly from raw data, enabling using Sentinel- 2 and Google Earth database images. According tasks such as classification and detection among others. These to their analysis, better detection performance was achieved algorithms can be categorized as pixel-using SVM, RF, and ANN. However, due to the spatial resolu based or object- - tion constraint of Sentinel-based, each offering unique advantages and challenges. Convolutional 2 images, the study was only able to

neural networks (CNNs) are the most commonly used for image-detect litter hotspots greater than

## based plastic detection in river environments.

Pixel-based approaches, commonly employed for clustering, have proven effective in segmenting plastics from other environmental elements, such as water and debris. For instance, CNNs applied to satellite and UAS imagery have enabled effective classification (Jakovljevic et al. 2020; Wolf et al. 2020; Solé

Gómez et al. 2022). Wolf et al. (2020) developed a dual-CNN system (APLASTIC-

Q): the plastic litter detector (PLD-
CNN) and plastic litter quantifier (PLQ-CNN). These dual-CNN models achieve classification overall accuracies exceeding 80% (PLD-CNN) and PLQ-CNN with 73% overall accuracies, offering a detailed breakdown of litter types and quantities. Similarly, Jakovljevic et  al.  (2020) showed strong pixel- wise classification performance using ResNet50, ResNeXt50, Xception, and Inception-ResNet v2 in semi-controlled experiments. Among the tested models, ResUNet50 achieved 0.78 accuracy (*F*1-score) on the Crna Rijeka River dataset. The model also performed well in shallow water, a challenging environment for such classifiers due to the similar spectral signatures of the riverbed and plastic debris. Furthermore, U- Net architectures (U- Net and U- Net3DE) and DeepLab (Deeplab V3+) were also used for satellite images in combination with Floating Debris Index (FDI) (Solé Gómez et  al.  2022). This approach enabled accuracy in debris pixel detection; however, the low representation of the debris class in the entire dataset was also thought to affect the results. Among the tested algorithms, the Deeplab V3+Xception backbone performed well in cross- validation, achieving an Intersection over Union (IoU) of approximately 0.5 and debris accuracy of around 80% (Solé Gómez et al. 2022).

In addition to pixel-based DL approaches, object detection frameworks like You Only Look Once (YOLO) have been applied to UAS-based RGB imagery for identifying plastic debris in

versions (from YOLOv2 to YOLOv5), the pre- trained YOLOv5s model emerged as the most effective for river plastic detection.

**3.2 | Fixed and Handheld Camera-Based** Its lightweight nature makes it ideal for limited processing **Monitoring** power or storage. In contrast, YOLOv4 achieves higher accuracy but with greater computational demands (Maharjan et al. 2022). Fixed and handheld cameras have become vital tools in address-However, these algorithms face challenges when applied to di- ing the growing issue of plastic pollution. They have provided verse environmental conditions. For instance, some CNN-valuable insights into macroplastic detection through diverse
based sensors and methodologies (Table 2). Practically, camera-models struggle to distinguish plastic pixels at the boundar-based ies of other materials, such as water, wood or rocks. Similarly, monitoring has entailed securing a camera on a bridge or a mast coarser spatial resolution limits the performance of classifiers located in the banks. Observation periods across studies vary, (Jakovljevic et  al. ranging from a single day to extended campaigns spanning up 2020). Furthermore, PLD- to 26 days, capturing thousands of images. For instance, in van CNN model faced challenges in distinguishing low-Lieshout et al. (2020), a bridge-mounted camera setup captured density (less than three items per tile) from high- 1272 images over 26 observation days in five locations, while Jia et  al.  (2023) utilized a combination of GoPro cameras and density (three or more items per tile) plastic 9 of 21 litter, revealing limitations in their adaptability to certain scenarios Wolf et al. (2020). These factors imply the critical need to leverage datasets that capture a broad range of environmental variability to enhance the generalizability of trained models.

cantly improved detection precision from 3.1% to 89.7% for high-canals and rivers (Maharjan et al. 2022). Among 12 tested YOLO

**TABLE 2** | Summary of fixed and handheld camera-

|Source|van Lieshout et al. (2020)|based studies. De Giglio et al. (2020)|Lin et al. (2021)|Tasseron et al. (2022)|Iordache et al. (2022)|Jia et al. (2023)|
|---|---|---|---|---|---|---|
|Platform Sensor Observation-days Number of images Viewing angle (°) Camera height (m) Spectral range Sensor resolution Preprocessing Wiley Interdisciplinary Reviews: Water, Area of study Classes|Fixed on bridges Dahua Easy4ip IPC-HDBW1435EP- W 26 1272 106 4.0–8.0 RGB 4 MP Frame extraction River Plastic & Organic debris|Handheld MAIA- W V2 3 NS NS 1.7–40 9 bands: VIS–NIR 1.2 MP Geometric & radiometric Data format conversion correction River & riverbank Plastic, Water, vegetation, & rock|Handheld NS NS 2400 NS NS RGB NS Waterway grass, branch, bottle, milk boxes, plastic garbage & a ball|Fixed on a tripod (NE) & fixed on a supporting frame (LB) Specim FX17 & Snapscan NE: 1 and LB: NS NS NE: NS & LB: 90 NE: NS and LB: 0.5 74 bands: NIR to SWIR LB: HR: 640 pixels/line and VR: NS and NE: 0.77 MP Manual reflectance correction & intensity normalization, extracting RoI, Spectral matching River Leaf, plastic bags, Water, vegetation, wood, rock, plastic, & sand|UAS & fixed on bridge MicaSense RedEdge- M 2 613 NS Fixed: 7 5 bands: VIS–NIR NS DN to radiance transformation, sky glint correction & removal of saturated pixels Land & water Grass, tree, soil, water, cement, painted surface, metal, plastic, wood|Handheld & fixed on bridge GoPro HERO4 & GoPro MAX 360 & a phone (Huawei P30 Pro) 10 9473 0 and 45 2.7 and 4.0 RGB 2.1 MP Frame extraction Canal Plastics, metal tins, paper, & cardboard items|

(Continues) **)**

## 2023

Based DL SqueezeNet DenseNet121, **Jia et al. (**Pixel-MobileNetV2, & Overall Accuracy ResNet50, InceptionV3,

**)**

## 2022

RF Score, and Accuracy **Iordache** 1- **et al. (** Supervised ML *F* Precision, Recall,

**)** SAM **2022**

## Tasseron

**et al. (**Supervised & SVM & SAM, Unsupervised MLSID, & SID-Confusion matrix

**)**

## 2021

## YOLO v5s, YOLO v5smAP

**Lin et al. (** F M A-F M A- Object detection DLYOLOv2 to YOLOv5,

**)**

## 2020 smartphones to collect 9473 images in 10 days. Although smartphone cameras have demonstrated potential for plastic detection and could be integrated into citizen science initiatives, this approach remains under-explored. Fixed camera monitoring 0.5 m in techniques operate at varying heights, from as low as laboratory setups to as high as 40 m in field conditions, providing flexibility to adapt to diverse monitoring scenarios.

Visible (van Lieshout et al. 2020; Lin et al. 2021; Jia et al. 2023), multispectral (De Giglio et  al.  2020; Iordache et  al.  2022), and hyperspectral (Tasseron et  al.  2021, 2022) sensors have been used to detect and classify plastics in rivers offering enhanced identification capabilities. Preprocessing techniques, including frame extraction (van Lieshout et al.  2020; Jia et al.  2023), geometric and radiometric corrections (De Giglio et  al.  2020; Tasseron et al. 2022; Iordache et al. 2022), data format conversion (Lin et  al.  2021), extracting regions of interest (RoI) and spectral matching (Tasseron et al. 2022) were performed by most of the reviewed studies to ensure accurate detection and classification. These monitoring techniques have been tested in diverse environments, from rivers (De Giglio et al. 2020; van Lieshout et al. 2020; Tasseron et al. 2022) and canals (Jia et al. 2023) to land-water interfaces (De Giglio et al. 2020; Iordache et al. 2022), targeting mainly plastics and vegetation. Supervised, unsupervised and hybrid approaches of ML as well as pixel- and object-based DL algorithms are central to these efforts.

For instance, in De Giglio et  al.  (2020), supervised, unsupervised, and hybrid ML techniques were employed to detect and classify plastics from images captured with a handheld multispectral camera covering a range from visible to near-infrared (NIR) (akin to the WorldView- 2 satellite sensor wavelengths) along the Reno River (Italy). Experiments were executed under different weather conditions (sunny and cloudy), and with diverse experimental setups. Upon preprocessing, images were classified through the ENVI software (NV5 Geospatial  2014) using K- means, isodata, maximum likelihood, and DT, with the latter method resulting in the highest reliability. Importantly, De Giglio et  al.  (2020) demonstrated that the spectral signature of the sample plastics revealed high radiance levels in the rededge and NIR bands, with notable fluctuations across the visible bands corresponding to the distinct colors of plastics. Moreover, a supervised ML approach, Linear Discriminant Analysis (LDA), was applied to differentiate floating items from water and to evaluate the contribution of each wavelength in discriminating vegetation and plastics (Tasseron et al. 2021). This lab-based study employed a dual hyperspectral camera setup and highlighted the critical role of bands within the NIR-SWIR range in effectively distinguishing plastics from other debris (Tasseron et  al.  2021). Towards further explora- tion of hyperspectral data in a natural environment, Tasseron et al. (2022) built on experimental findings achieved in the lab to classify images taken in natural settings at the Waal River (Netherlands). Images from both experimental setups (lab and outdoors) were preprocessed to enable spectral matching, and then classified via support vector machines (SVM), Spectral Angle Mapper (SAM), Spectral Information Divergence (SID), 11 of 21

and a logarithmic combination of SAM and SID. Lab-based training was instrumental in classifying images in natural settings, where SAM led to the highest accuracy of 96% among all algorithms.

& Hybrid MLmeans, Isodata, & Decision tree K-Global Accuracy & Kappa Coefficient **De Giglio et al. (** Maximum likelihood, Unsupervised, Supervised

**)**

**2020** CNN & 2 *R* &

**van Lieshout** **et al. (** Faster R- Inception v2

Object Detection DL Average Precision

(Continued) |

**Source** Classifier Algorithm

**TABLE 2**

Performance evaluation Abbreviations: HR, horizontal resolution; LB, laboratory; NE, natural environment; NS, not specified; VR, vertical resolution (check the text for other acronyms).

In addition to ML, both pixel- and object-based DL algorithms have also been utilized for advancing river plastic monitoring. Namely, in van Lieshout et  al.  (2020), plastic pollution across five rivers in Jakarta, Indonesia, was investigated by analyzing footage captured by an outdoor surveillance camera in the visible spectral range. The analysis was performed using Faster R- CNN (Regional-Convolutional Neural Network) and Inception v2 for segmentation and classification, respectively, with results compared to visual observations for validation. Notably, this approach achieved a precision of approximately 69% in estimating plastic density. The automated procedure roughly detected 35% more plastics than visual observations, and it proved even more effective during periods of high plastic transport. Similarly, five DL architectures (ResNet50, InceptionV3, Dense Convolutional Network [DenseNet121], mobile architecture [MobileNetV2], and a smaller CNN architecture called [SqueezeNet]) were employed for similar purposes on images captured from smartphone and fixed cameras on a bridge (Jia et  al.  2023). Among these architectures, SqueezeNet and DenseNet121 stood out, achieving overall accuracies of 89.6% and 91.7%, respectively (Jia et al. 2023). Further advancements in DL were demonstrated by Lin et al. (2021), where the YOLOv5s algorithm, enhanced with a feature map attention (FMA) layer, achieved a mean average precision (mAP) of 79.41% for detecting floating plastics.

It is important to note that some studies overlooked crucial details about image collection processes and sensor setups, which are vital for ensuring reproducibility. In fact, evaluating the performance and adaptability of models across diverse environmental conditions, locations, and sensor setups is essential for effective large-scale and long-term monitoring strategies. For instance, van Lieshout et al. (2020) demonstrated model adaptability under varying conditions, including plastic density, water surface conditions (waves), observation altitude, and the presence or absence of organic material. They recommended supple- menting training datasets with location-specific data to achieve better generalization to new locations. Similarly, the flexibility of detection algorithms was assessed in Iordache et  al.  (2022), where a RF algorithm initially tailored to identify land areas (> 88% accuracy) was applied to detect litter in a semi-controlled experiment. In this case, the algorithm was fed multispectral images taken by a MicaSense RedEdge camera mounted on a UAS and fixed on a bridge. However, experimental findings suggested that detection accuracy can be enhanced with algorithms separately trained for land and water areas, whereby distinct spectral properties and litter characteristics are adequately taken into account. Moreover, Tasseron et al. (2022) highlighted that variable weather and light conditions necessitate frequent sensor calibration in hyperspectral imaging. They also noted that low atmospheric transmittance in the 1350–1400 nm range introduces considerable noise, posing additional challenges for accurate plastic detection.

While the efforts thus far are highly valuable, future research should also prioritize long-term monitoring with extended observation periods to encompass a broader range of conditions 12 of 21 in natural systems. Most of current studies are confined to controlled or semi-controlled environments, with observation periods typically lasting only a few days. This limitation often necessitates image manipulation to generate additional data for training, testing, and evaluating models. ## 3.3 | Indices Used in River Macroplastics Detection

Several image-based indices have been introduced to detect floating debris in the visible, NIR, and SWIR bands captured with remote sensing platforms (see Table 3). The FDI was developed by Biermann et al. (2020) from Sentinel- 2 bands (4, 6, 8, and

11) in combination with the floating algae index (FAI) (Hu 740 nm to take 2009; Hu et al. advantage of the difference between NIR and baseline reflection 2015; Wang and Hu 2016). Instead of the standard red band, this index leverages the red edge band at of NIR that enables the separation of materials reflecting NIR (like seaweed, wood, and spume) from materials absorbing NIR (like water). In Tasseron et al. (2021), the FDI is computed from hyperspectral images taken in lab-
based experiments, whereby this index shows promise in distinguishing between plastics (like LDPE [Low-Density Polyethylene], PP [Polypropylene], and PS [Polystyrene]) and vegetation.

However, limitations were also noted in FDI's sensitivity to submerged debris as it was also highlighted by Moshtaghi et al. (2021).

In Solé Gómez et  al.  (2022), floating debris accumulation and its seasonal variations in river environments is investigated as in Biermann et  al.  (2020) using Sentinel- 2 images for training classifiers. According to this study though, application of the FDI results into a small IoU score for debris (equal to 0.0023). Similarly, Mohsen et al. (2023) assessed the feasibility of adopting different bands and indices towards river plastic detection, whereby such indicators are used as inputs for training various models (DT, NB, SVM, RF, and ANN). The study found that FDI was the least influential index compared to alternative bands (SWIR and NIR) and indices (PI, NDWI, and NDVI). Such limited performance of FDI could be associated to the turbidity of rivers (Biermann et al. 2020; Moshtaghi et al. 2021).

In Themistocleous et  al.  (2020), the PI is developed, tested, and compared to alternative established indices for detecting plastic debris on the sea surface using Sentinel- 2 images as in Biermann et al. (2020). To provide a sound comparison across platforms, in Themistocleous et  al.  (2020), a plastic target resembling water bottles was deployed near Limassol, Cyprus, and multispectral images were captured by Sentinel- 2 and, simultaneously, with UASs. Experimental findings highlighted the newly developed PI as highly effective in identifying floating plastic objects, surpass- ing the performance of other indices. Following the introduction of the PI, in Sakti et al. (2023), such an index was adjusted (API) to monitor spatiotemporal variations of illegal dumping, particularly plastics along riverbanks, Table 3. The API included corrections for vegetation using the NDVI, and for land and buildings using the Modified Normalized Difference Built- **4 | Challenges and Opportunities** up Index (MNDBI). The analysis supported that the API enhanced plastic detection in riverine environments compared to the original PI. The inherent heterogeneity of plastics as well as the multi-scale nature of processes involved in their transport are at the basis of monitoring complexity and hamper the use of a single

*Wiley Interdisciplinary Reviews: Water,* 2025 **TABLE 3** | Indices used in river macroplastic detection.

## Indices Equations Pros and cons Developed and used

() a FDI *Pros*: alignment with plastic Biermann et al. (2020), Mohsen

|FDI = R − [R NIR|+ RE2|R SWIR1|− R RE2|
|---|---|---|---|
|𝜆 (NIR ×|+ 𝜆) RED|× 10]||
|𝜆 (SWIR1|− 𝜆 RED|)||

spectral peaks: helps separate et al. (2023), Solé Gómez et al. (2022), plastics from natural materials and Tasseron et al. (2021) like vegetation or water. *Cons*: sensitive to turbidity, submerged plastics (due to NIR absorption by water), sun glint and other reflective conditions.

PI PI =*R*NIR*Pros*: simplicity; plastic-Themistocleous et al. (2020), a Sakti *R* NIR+ *R*RED water discrimination. et al. (2023), Mohsen et al. (2023) *Cons*: limited spectral and Tasseron et al. (2021) coverage; potential confusion with vegetation (struggles to distinguish plastics from materials like vegetation that also reflect strongly in NIR); sensitive to turbidity, sun glint and other reflective conditions.

API IF(NDVI*>*0): PI₁ = PI *Pros*: vegetation and Sakti et al. (2023) a

## − NDVI, ELSE: PI₁ = PI

built-up area correction. *Cons*: tested only on riverbanks; IF(MNDBI*>*0): PI₂ = PI₁ sensitive to sun glint and

## − MNDBI, ELSE: PI₂ = PI₁

other reflective conditions.

NDVI <u>(RNIR− RRED)</u> — Biermann et al. (2020), Tasseron ( *R* NIR+ *R*RED) et al. (2021), and Sakti et al. (2023)

MNDBI <u>(RSWIR− RNIR)</u> — Sakti et al. (2023) ( *R* SWIR+ *R*NIR)

NDWI <u>(RGREEN− RNIR)</u> — Mohsen et al. (2023) ( *R* GREEN+ *R*NIR)

*Note:* FDI was developed using Sentinel 2 bands with central wavelength of RED 664.6/665.0; RE2: 740.5/739.1; NIR: 832.8/833, and RSWIR1: 1613.7/1610.4 and PI was

also developed using Sentinel 2 without atmospheric correction. Pros and cons are specifically outlined for indices developed for plastic detection. a Index developer.

monitoring technique. For instance, satellite imagery offers extensive coverage, thus being ideal for large-scale plastic pollution monitoring (Table  4). This capability allows for assessing plastic distribution across vast areas, thus providing valuable insights into spatial patterns and seasonal variations (Simpson classification and detection in river environments. A limited et  al.  2022; Solé Gómez et  al.  2022; Mohsen et  al.  2023; Sakti spectral range can hinder the differentiation of plastic debris et  al.  2023). However, satellite imagery frequently encounters from surrounding objects and natural features in rivers (Sakti challenges related to return periods and spatial resolution, par-et al. 2023). While open- ticularly when relying on open-source satellite imagery offers reason- source satellite images that make able spectral resolution, it is still not adequate to monitor mac- the accurate detection of small plastic debris especially difficult roplastics (Sakti et al. 2023). On the other hand, most satellites (Salgado-Hernanz et al. 2021; Solé Gómez et al. 2022). Despite with high spatial resolution often lack sufficient spectral reso- the availability of commercial high- lution, making it challenging to distinguish and classify plastic resolution satellite sensors debris accurately. In addition, cost and accessibility may pose such as WorldView and Pleiades, this challenge persists, partic-barriers to the widespread use of satellite imagery. Finding a ularly in rivers with narrow channels or densely vegetated areas balance between spectral and spatial resolution is thus essen- where plastic debris may be concealed (Simpson et  al.  2022). tial for enhancing accuracy and precision in classification and In addition, satellite-detection efforts. based monitoring is affected by sun glare, cloud cover, shadows, airborne particles in the atmosphere, and Plastic pollution in rivers also exhibits temporal variability, high solar zenith angles, which can impact both the quality and with debris motion influenced by river discharge, flow velocity, analysis of the data (Salgado-water level, precipitation events, extreme weather events, tide Hernanz et al. 2021). patterns, river morphological units, river and riparian vegetation, and engineering structures along with other hydrological 13 of 21

Besides spatial resolution, spectral resolution also stands out and environmental factors (Kurniawan and Imron  2019; van as a critical factor influencing the accuracy of macroplastic Emmerik and Schwarz  2020; Roebroek et  al.  2021; Cowger et al. 2022; Gallitelli and Scalici 2022; Liro et al. 2022; Cesarini et  al.  2023; Laverre et  al.  2023; van Emmerik, Kirschke, To partially mitigate limitations posed by a single monitoring et al. 2023; van Emmerik, Schreyers, et al. 2023; MacAfee and approach, integration from alternative technologies may be Löhr  2024). Hence, in addition to spatial and spectral reso-promising. For example, a study by Simpson et al. (2022) indi- lution, temporal resolution also plays a crucial role in plastic cates the applicability of microwave bands via SAR images to de- detection and monitoring. Satellite revisits may only roughly tect plastics and other floating debris. Further, data fusion with allow for tracking changes over time, such as the bulk motion imagery collected with UASs equipped with high- and accumulation of plastic debris in rivers. However, dynamic resolution processes are not accurately captured. Moreover, delays be-cameras can complement satellite- tween image acquisition and data availability can hinder near-based monitoring by provid-real-time applications. ing spatially- and spectrally- refined data in short time frames

**TABLE 4** | Advantages and limitations of remote sensing methods.

(Jakovljevic et  al.  2020; Wolf et  al.  2020; Cortesi et  al.  2022;

|Methods|Advantages|Maharjan et al. 2022). However, it is important to note that data Limitations|
|---|---|---|
|Satellite UAS|Large area coverage : enables monitoring of extensive regions. Cost-effectiveness : open- source data (e.g., Sentinel- 2) reduces costs for broad river monitoring. Preprocessed data : simplifies analysis for users. Broad temporal coverage : supports historical analysis with decades of satellite data. Consistent geographic coverage : enables consistent & comparable data collection. Ease of automation : can be integrated with AI for automated detection and analysis. Low operational cost & human effort : mostly no need for field presence; data is accessible remotely. High spatial resolution : enables detailed monitoring of small plastics. On- demand data collection : can be deployed in response to immediate needs, enabling near- real- time monitoring. Flexible flight altitudes : enable objective- based assessment & reduce atmospheric distortions by flying at low altitudes. Detailed temporal monitoring : can be deployed frequently to track rapid plastic accumulation changes. Ability to target specific locations : can focus on hotspots, such as river mouths or urban river sections, where plastics accumulate. Capability to access remote or dangerous areas : enhances data collection in challenging terrains.|Coarse spatial resolution : satellite sensors, especially open- source, often have limited resolution, making small debris detection challenging. Atmospheric interference : cloud cover, haze, & shadows can limit the visibility of plastics. Obstruction from riparian vegetation : riparian vegetation & its shadows may obscure plastics. Update lag : delays between image capture & availability, which limits near-real-time applications. Limited spectral resolution : some satellites may face challenges in distinguishing plastics from other materials due to limited spectral bands. Long revisit time : satellite revisit times of days to weeks limit capturing rapid changes. Limited area coverage : covering extensive areas requires multiple flights or a larger UAS fleet. Operational costs : operations require pilots, maintenance, & battery charging, adding to monitoring expenses. Weather dependence : susceptible to interference from wind, rain, fog, sun glare, & glint. Battery life & storage constraints : restrict monitoring duration & volume. Regulatory and safety constraints : subject to regulations & may require permits. Preprocessing requirements : requires extra time and tools.|

*Ease of automation*: can be integrated with AI *Interference from riparian vegetation*: for automated detection and analysis. vegetation interference & shadowing (Continues) complicate monitoring. 14 of 21 *Potential for hyperspectral & multispectral cameras*:*Wiley Interdisciplinary Reviews: Water,* 2025 enhance precise plastic detection & classification by leveraging unique spectral signatures. **TABLE 4** | (Continued)

|Methods|Advantages|Limitations|
|---|---|---|
|Fixed Handheld (including smartphones)|Continuous monitoring : allows long- term data collection at a specific location. Low operational costs : costs limited to installation, maintenance, and retrieval. Potential for enhanced multispectral or hyperspectral imaging : enhance precise plastic detection & classification by leveraging unique spectral signatures. High spatial resolution : provides high- quality images for detecting small debris. Real- time data collection : supports immediate detection & response to plastic accumulation. Ease of automation : can be integrated with AI for automated detection & analysis. Portability, flexibility, & accessibility : easy to deploy for on- the- spot observations. Cost-effective : widely available & relatively inexpensive. High image quality : modern smartphones & cameras often feature high- resolution sensors. Flexibility : allows targeted monitoring of specific locations. Easy integration with apps & cloud storage : enables direct image uploads to cloud platforms for analysis. Ease of automation : can be integrated with AI for automated detection and analysis.|Static monitoring locations : limit spatial flexibility. Weather dependence : susceptible to interference from rain, fog, sun glare, & glint. Power requirements : often require reliable power sources. Preprocessing requirements : lead to extra computational time. Manual operation required : require personnel to capture data, increasing labor costs. Limited area coverage : it can only capture small areas at a time. Weather dependence : susceptible to interference from rain, fog, sun glare, & glint. Inconsistency in data collection : manual operation may cause variations in camera setup (e.g., angle), complicating analysis. Battery life & storage constraints : restrict monitoring duration & volume. Lower spectral sensitivity : smartphones & commercial cameras lack advanced spectral imaging.|

*Connectivity*: smartphones offer GPS & internet for geotagging & real-*Preprocessing requirements*: require fusion presents challenges, such as incompatible data formats time sharing. extra computational time. and sensors characteristics, temporal misalignment, variations in radiometric calibration, georeferencing accuracy, and sig *Citizen science potential*: involves non- - *Variation in data quality*: citizen science

nificant computational resource requirements. Such factors specialists in monitoring efforts, increasing coverage area pose challenges compared to satellites (Jakovljevic initiatives with varying camera specifications

can complicate the integration process, potentially affecting dataset, coverage, & awareness. et al. 2020; Cortesi et al. can cause data quality inconsistencies. 2022; Maharjan et al. 2022). With re-

the quality and reliability of the fused data (Lahat et  al.  2015; gards to spectral resolution, UASs enable hyperspectral imag-Ghamisi et al. 2019; Li et al. 2022). ery acquisition thus opening novel perspectives towards plastics identification (Tasseron et al. 2021; Manfreda and Dor 2023). UASs usually fly below 100 m, thus offering a spatial resolution below 1 m. Their low and flexible flight altitudes minimize vul-However, this advancement is accompanied by increased data nerability to atmospheric distortions, facilitate objective-processing complexity. Additionally, regulatory requirements, based such as flight permits from both civil and military aviation au- assessments, and improve detection accuracy (Tauro et al. 2015; thorities, may be stricter when utilizing sensors with extended Tauro et  al.  2016; Tauro et  al.  2016; Manfreda et  al.  2018). spectral capabilities (Salgado-Additionally, UASs can be deployed frequently to monitor rapid Hernanz et  al.  2021; Iordache changes, and target specific areas, including hotspots such as et al. 2022). Finally, commercial UASs may also present altitude river mouths, urban river sections, and locations inaccessible to inaccuracies that stem from internal stabilization processes personnel. While they tend to be cost- and can significantly impact data quality (Geraeds et al. 2019). effective and enable near-These inaccuracies can be alleviated through altitude monitor-real-ing using Real-15 of 21 time monitoring, their limited flight range and narrow time GPS, employing higher resolution cameras at elevated altitudes, and utilizing custom- made drones as suggested by Geraeds et al. (2019). Furthermore, dynamic weather conditions mandate frequent sensor re- calibration to mitigate issues like cloud-induced shadows (Geraeds et al. 2019; Jakovljevic et al.  2020; Maharjan et al.  2022). Further, atmospheric transmittance issues in specific spectral ranges further complicate accurate analysis of hyperspectral imagery (Tasseron et al. 2022).

Fixed-, handheld-cameras, and smartphones offer unique opportunities for river plastic monitoring, with specific challenges that need to be considered for optimal use in different contexts (Table  4). Fixed cameras excel in continuous, long-term monitoring, making them ideal for persistent surveillance at specific locations and fostering environmental monitoring at the edge (Tosi et  al.  2020; Livoroi et  al.  2021; Noto et  al.  2022; Tauro et  al.  2022). They provide high spatial resolution, ensuring high-quality images for detecting small debris. These cameras also hold potential for advanced imaging capabilities like multispectral or hyperspectral analysis, which can significantly enhance plastic identification. However, their limited field of view and static positioning restrict their ability to monitor large and changing river systems. Moreover, fixed cameras require reliable power sources and network connectivity, adding

to operational complexity. In contrast, handheld cameras and smartphones offer flexibility and portability, enabling easy deployment for targeted observations of specific locations, such as hotspots like river mouths or urban river sections. This portability makes them highly cost-effective and accessible, especially smartphones, which also feature GPS and real-time connectivity for geotagging and cloud data sharing. These devices allow for rapid response and can involve citizen scientists in monitoring efforts, expanding dataset coverage and raising awareness (Nardi et al. 2021). However, handheld devices require manual operation, which can lead to inconsistencies in data collection, such as variations in image angle, scale, and quality. Their limited area coverage and battery life constraints make them less suitable for extended monitoring, and lower spectral sensitivity limits their ability to capture detailed information compared to fixed or specialized cameras. Furthermore, UASs-, fixed and handheld camera-based imagery tends to be affected by mete- orological factors and atmospheric constraints. For instance, variations in brightness, wind speed, river flow rates, water turbidity, shadows, and reflections can influence detection accuracy (Geraeds et  al.  2019; Jakovljevic et  al.  2020; Tasseron

**FIGURE 3** |

ing an example of detection fusion using spectral RGB data.

16 of 21 *Wiley Interdisciplinary Reviews: Water,* 2025

Illustration of the opportunities in data assimilation for detecting river plastic with RGB cameras in two case studies in Indonesia and the Netherlands: (A) raw image with plastic targets, (B) YOLOv8 model detection, and (C) red/green binarized band ratio with varying binarization value (BV). Violet circles in (A) were some of the plastics that YOLO failed to detect, which the binarization aims to discriminate in (C), thus provid-

et al.  2022). In turn, images also require preprocessing, which increases computational time.

Integrating artificial intelligence with image-based plastic detection automates the process, enabling real-time data collection and facilitating rapid responses to plastic accumulation. This also supports informed, timely management and mitigation strategies. Further, ML and DL approaches for imagery detection and classification could be essential for overcoming image quality challenges and improving the accuracy and efficiency of continuous river plastic monitoring (Waqas et al. 2023). Latest advancements in ML and DL techniques, have indeed demonstrated promising outcomes in detecting and categorizing macroplastics within river environments. These advancements have been further propelled by the rapid evolution of graphics processing unit (GPU) computing, which has significantly enhanced computational capabilities. Leveraging images from various sources, these techniques have been successfully employed in several river macroplastic- focused studies (Jakovljevic et al.  2020; Wolf et al. 2020; Iordache et al. 2022; Solé Gómez et al. 2022; Tasseron et al. 2022; Jia et al. 2023; Mohsen et al. 2023; Sakti et al. 2023). Notably, supervised ML such as RF, SVM, NB, and DT, and unsupervised ML, namely, K- means, Isodata and Maximum Likelihood have been crucial for accurate detection and classification. Additionally, pixel-based DL approaches for both image segmentation and classification such as U- Net and, U- Net3DE, Deeplab V3, ResNet50, InceptionV3, DenseNet121, MobileNetV2, and SqueezeNet, have significantly advanced image segmentation and classification tasks. Object detection DL methods, including Faster R- CNN, and advancements of the YOLO family as well as improvements such as FMA-YOLOv5s, have expanded the capabilities and enabled more precise and efficient plastic detection in various river environments (Lin et al. 2021; Maharjan et  al.  2022). Further, this class of algorithms can be comple- mented with spectral data towards potential detection fusion to improve river plastic detection performance (see Figure  3). However, the effectiveness of these algorithms heavily depends on the availability of extensive datasets for training, validation, and transferability. Unfortunately, macroplastics datasets are often limited, highlighting the need for collaborative efforts to establish open data sources and a shared repository (Solé Gómez et al. 2022; Tasseron et al. 2022; Manfreda et al. 2024).

In this context, the initiative Ocean Scan, recognized by the International Ocean Color Coordinating Group (IOCCG) task force on Remote Sensing of Marine Litter and Debris, serves as a relevant example. It provides a global repository of in situ observations and matching remote-sensing images of marine litter and debris, along with standardized methodologies and tools for accessing, gathering, and categorizing in situ marine litter data. These tools include a user- friendly web portal and a mobile application for easy data access and submission. Creating a similar system for river environments or integrating it with existing da- tabases would significantly mitigate the scarcity of datasets. In fact, citizen science presents a viable option for image collection and labeling by engaging local communities, environmental or- ganizations, schools, and individual volunteers, addressing data scarcity within a single river or across different rivers (Rech et  al.  2015; Battisti and Gippoliti  2019; Geraeds et  al.  2019; Kiessling et al. 2019; van Emmerik, Roebroek, et al. 2020; van Emmerik, Seibert, et  al.  2020; Honorato-Zimmer et  al.  2021; Kiessling et al. 2021; Liro, Zielonka, Hajdukiewicz, et al. 2023). An example is the RiverWatch project (RiverWatch 2024), which attempts to involve volunteers to monitor macroplastics in the Sarno River (Italy), one of the most polluted rivers in Europe. Through systematic data collection and image-based docu- mentation, such initiatives have the potential to contribute to a database that can support scientific research, policy deci- sions, and public awareness campaigns (Popa et al. 2022; Fraisl et  al.  2023). This approach may not only expand the available data pool but also facilitate a better understanding on how to ad- vance algorithm transferability in various environmental contexts (van Emmerik, Seibert, et al. 2020; Iordache et al. 2022; Jia et al. 2023; Liro, Zielonka, Hajdukiewicz, et al. 2023). Thus, citizen science not only supplements traditional monitoring methods but also fosters a more inclusive and scalable approach to tackling riverine plastic pollution.

## 5 | Conclusion and Outlook

While monitoring plastics in river systems is at the forefront of the water management agenda, individual research efforts have been mostly directed towards testing multiple and diverse technologies. We have provided a comprehensive review of the remote sensing approaches for detecting macroplastics in river settings. Since most of the reported methodologies have been just recently introduced, considerable steps are still to be undertaken towards improving and harmonizing plastics monitoring by remote sensing. Plastic monitoring using UASs and fixed and handheld cameras has shown promising potential. In contrast, monitoring through satellite imagery faces challenges due to limitations in spatial, temporal, and spectral resolution. Machine learning and deep learning techniques have greatly enhanced plastic detection by enabling more accurate image processing and analysis. Nevertheless, they are still challenged by transferability and weather-induced distortions such as sun glare. Plastic spectral signatures in river settings remain relatively untapped, and leveraging hyperspectral signals across various platforms could uncover unknown properties of plastic materials in fluvial systems. Besides, adopting and testing indices developed for alternative environments, such as marine, as well as integrating multiple platforms with continuous, long-term monitoring could help overcome the challenges associated <u>with river macroplastics monitoring.</u>

**Author Contributions**

**Ashenafi Tadesse Marye:** data curation (lead), investigation (lead), methodology (lead), software (lead), validation (lead), visualization (lead), writing – original draft (lead). **Cristina Caramiello:** writing – review and editing (supporting). **Dario De Nardi:** writing – review and editing (supporting). **Domenico Miglino:** writing – review and editing (supporting). **Gaia Proietti:** writing – review and editing (supporting). **Khim Cathleen Saddi:** visualization (equal), writing – review and editing (equal). **Chiara Biscarini:** funding acquisition (equal), project administration (equal), supervision (equal), writing – review and editing (supporting). **Salvatore Manfreda:** funding acquisition (equal), project administration (equal), supervision (equal), writing – review and editing (supporting). **Matteo Poggi:** funding acquisition (equal), project administration (equal), supervision (equal), writing – review and editing (supporting). **Flavia Tauro:** conceptualization (lead), funding acquisition (lead), methodology (lead), project administration (lead), resources (lead), supervision (lead), writing – review and editing (lead).

## 17 of 21 **Acknowledgments**

The authors sincerely thank the editors and reviewers for their in- sightful suggestions, which improved our manuscript. We gratefully acknowledge financial support provided by: the Italian Ministry of University and Research under the PRIN project 2022MMBA8X “RiverWatch: a citizen-science approach to pollution monitoring”— CUP J53D23002260006, grant agreement n. 961, 06/30/2023; ECS 0000024 Rome Technopole—CUP B83C22002820006, PNRR Mission 4 Component 2 Investment 1.5, funded from the European Union (EU) Next-Generation EU; and RETURN Extended Partnership funded from the Next-Generation EU (National Recovery and Resilience Plan NRRP, Mission 4, Component 2, Investment 1.3 – D.D. 1243 2/8/2022, PE0000005). Open access publishing facilitated by Universita degli Studi della Tuscia, as part of the Wiley-CRUI-CARE agreement.

**Conflicts of Interest**

The authors declare no conflicts of interest.

**Data Availability Statement**

Data sharing is not applicable to this article as no new data were created or analyzed in this study.

**Related WIREs Articles**

Plastic debris in rivers

**References**

Andrady, A. L. 2017. “The Plastic in Microplastics: A Review.” *Marine* *Pollution Bulletin* 119, no. 1: 12–22.

Azevedo-Santos, V. M., M. F. Brito, P. S. Manoel, et  al. 2021. “Plastic Pollution: A Focus on Freshwater Biodiversity.” *Ambio* 50, no. 7: 1313–

1324. [https://doi.org/10.1007/s13280-020-01496-5](https://doi.org/10.1007/s13280-020-01496-5). Battisti, C., L. Gallitelli, S. Vanadia, and M. Scalici. 2023. “General MacroLitter as a Proxy for Fishing Lines, Hooks and Nets Entrapping Beach-Nesting Birds: Implications for Clean-
Ups.” *Marine Pollution* *Bulletin* 186: 114502.

Battisti, C., and S. Gippoliti. 2019. “Not Just Trash! Anthropogenic Marine Litter as a ‘Charismatic Threat’ Driving Citizen-Based Conservation Management Actions.” *Animal Conservation* 22, no. 4: 311–313.

Biermann, L., D. Clewley, V. Martinez-Vicente, and K. Topouzelis.

2020. “Finding Plastic Patches in Coastal Waters Using Optical Satellite Data.” *Scientific Reports* 10, no. 1: 5364. [https://doi.org/10.1038/s41598-](https://doi.org/10.1038/s41598-) 020-62298-z. Blettler, M. C., E. Abrial, F. R. Khan, N. Sivri, and L. A. Espinola.
2018. “Freshwater Plastic Pollution: Recognizing Research Biases and Identifying Knowledge Gaps.” *Water Research* 143: 416–424. Blettler, M. C., E. Agustini, E. Abrial, et  al. 2023. “The Challenge of Reducing Macroplastic Pollution: Testing the Effectiveness of a River Boom Under Real Environmental Conditions.” *Science of the Total* *Environment* 870: 161941. Blondel, E., and F. A. Buschman. 2022. “Vertical and Horizontal Plastic Litter Distribution in a Bend of a Tidal River.” *Frontiers in Environmental* *Science* 10: 861457. Browne, M. A. 2015. “Sources and Pathways of Microplastics to Habitats.” In *Marine Anthropogenic Litter*, 229–244. Springer 18 of 21 International Publishing. Bucci, K., M. Tulio, and C. Rochman. 2020. “What Is Known and Unknown About the Effects of Plastic Pollution: A Meta-
Analysis and

River: Plastic Pollution and Loading to the NW Mediterranean Sea.” *Marine Pollution Bulletin* 146: 60–66.

Cesarini, G., R. Crosti, S. Secco, L. Gallitelli, and M. Scalici. 2023. “From City to Sea: Spatiotemporal Dynamics of Floating Macrolitter in the Tiber River.” *Science of the Total Environment* 857: 159713.

Corbari, L., A. Maltese, F. Capodici, M. Mangano, G. Sarà, and G. Ciraolo. 2020. “Indoor Spectroradiometric Characterization of Plastic Litters Commonly Polluting the Mediterranean Sea: Toward the Application of Multispectral Imagery.” *Scientific Reports* 10, no. 1: 19850.

Cortesi, I., A. Masiero, G. Tucci, and K. Topouzelis. 2022. “UAV-Based River Plastic Detection With a Multispectral Camera.” *International* *Archives of the Photogrammetry, Remote Sensing and Spatial Information* *Sciences* 43: 855–861.

Cowger, W., A. Gray, S. Brownlee, H. Hapich, A. Deshpande, and K. Waldschläger. 2022. “Estimating Floating Macroplastic Flux in the Santa Ana River, California.” *Journal of Hydrology: Regional Studies* 44: 101264.

Cózar, A., M. Arias, G. Suaria, et al. 2024. “Proof of Concept for a New Sensor to Monitor Marine Litter From Space.” *Nature Communications* 15, no. 1: 4637. [https://doi.org/10.1038/s41467-024-48674-7](https://doi.org/10.1038/s41467-024-48674-7).

Da Costa, J. P., C. Mouneyrac, M. Costa, A. C. Duarte, and T. Rocha-Santos. 2020. “The Role of Legislation, Regulatory Initiatives and Guidelines on the Control of Plastic Pollution.” *Frontiers in* *Environmental Science* 8: 104.

Dauvergne, P. 2023. “Governing Plastics: The Power and Importance of Activism in the Global South.” *Environmental Science & Policy* 147: 147–153.

De Giglio, M., M. Dubbini, I. Cortesi, M. Maraviglia, E. I. Parisi, and

G. Tucci. 2020. “Plastics Waste Identification in River Ecosystems by Multispectral Proximal Sensing: A Preliminary Methodology Study.” *Water and Environment Journal* 35, no. 2: 569–579. Earn, A., K. Bucci, and C. M. Rochman. 2021. “A Systematic Review of the Literature on Plastic Pollution in the Laurentian Great Lakes and Its Effects on Freshwater Biota.” *Journal of Great Lakes Research* 47, no. 1: 120–133. European-Parliament. 2018. “Microplastics: Sources, Effects and Solutions.” [https://www.europarl.europa.eu/topics/en/article/20181](https://www.europarl.europa.eu/topics/en/article/20181) 116STO19217/microplastics-sources-effects-and-solutions. Europe-Plastic. 2024. “Plastics—The Fast Facts 2024.” [https://pla](https://pla) st icseurope.org/knowledge-hub/plastics-the-fast-facts-2024/. Fletcher, S., A. March, K. Roberts, et al. 2023. *Turning Off the Tap: How* *the World Can End Plastic Pollution and Create a Circular Economy*. United Nations Environment Programme. Fraisl, D., L. See, R. Bowers, et  al. 2023. “The Contributions of Citizen Science to Sdg Monitoring and Reporting on Marine Plastics.” *Sustainability Science* 18, no. 6: 2629–2647. Gallitelli, L., M. Cutini, and M. Scalici. 2024. “Riparian Vegetation Plastic Monitoring: A Harmonized Protocol for Sampling Macrolitter in Vegetated Riverine Habitats.” *Science of the Total Environment Wiley Interdisciplinary Reviews: Water,* 912: 2025 169570. Gallitelli, L., P. Girard, U. Andriolo, et al. 2024. “Monitoring Macroplastics in Aquatic and Terrestrial Ecosystems: Expert Survey Garaba, S. P., and H. M. Dierssen. 2018. “An Airborne Remote Sensing Case Study of Synthetic Hydrocarbon Detection Using Short Wave Infrared Absorption Features Identified From Marine-Harvested Macro- and Microplastics.” *Remote Sensing of Environment* 205: 224–235.

Geraeds, M., T. van Emmerik, R. de Vries, and M. S. bin Ab Razak. 2019. “Riverine Plastic Litter Monitoring Using Unmanned Aerial Vehicles (UAVs).” *Remote Sensing* 11, no. 17: 2045.

GESAMP. 2019. “Guidelines for the Monitoring and Assessment of Plastic Litter and Microplastics in the Ocean.” *GESAMP Reports and* *Studies* 99: 1–130.

Ghamisi, P., B. Rasti, N. Yokoya, et  al. 2019. “Multisource and Multitemporal Data Fusion in Remote Sensing: A Comprehensive Review of the State of the Art.” *IEEE Geoscience and Remote Sensing* *Magazine* 7, no. 1: 6–39.

González-Fernández, D., A. Cózar, G. Hanke, et  al. 2021. “Floating Macrolitter Leaked From Europe Into the Ocean.” *Nature Sustainability* 4, no. 6: 474–483.

González-Fernández, D., and G. Hanke. 2017. “Toward a Harmonized Approach for Monitoring of Riverine Floating Macro Litter Inputs to the Marine Environment.” *Frontiers in Marine Science* 4, no. 86: 1–7.

Honingh, D., T. van Emmerik, W. Uijttewaal, H. Kardhana, O. Hoes, and N. Van de Giesen. 2020. “Urban River Water Level Increase Through Plastic Waste Accumulation at a Rack Structure.” *Frontiers in* *Earth Science* 8: 28.

Honorato-Zimmer, D., T. Kiessling, M. Gatta-Rosemary, et  al. 2021. “Mountain Streams Flushing Litter to the Sea–Andean Rivers as Conduits for Plastic Pollution.” *Environmental Pollution* 291: 118166.

Hu, C. 2009. “A Novel Ocean Color Index to Detect Floating Algae in the Global Oceans.” *Remote Sensing of Environment* 113, no. 10: 2118–2129.

Hu, C., L. Feng, R. F. Hardy, and E. J. Hochberg. 2015. “Spectral and Spatial Requirements of Remote Measurements of Pelagic Sargassum Macroalgae.” *Remote Sensing of Environment* 167: 229–246.

Huang, W., and X. Xia. 2024. “Element Cycling With Micro (Nano) Plastics.” *Science* 385, no. 6712: 933–935.

Hurley, R., H. F. V. Braaten, L. Nizzetto, et al. 2023. “Measuring Riverine Macroplastic: Methods, Harmonisation, and Quality Control.” *Water* *Research* 235: 119902.

Iordache, M.-

D., L. De Keukelaere, R. Moelans, et al. 2022. “Targeting
Plastics: Machine Learning Applied to Litter Detection in Aerial Multispectral Images.” *Remote Sensing* 14, no. 22: 5820.

Jakovljevic, G., M. Govedarica, and F. Alvarez-Taboada. 2020. “A Deep Learning Model for Automatic Plastic Mapping Using Unmanned Aerial Vehicle (UAV) Data.” *Remote Sensing* 12, no. 9: 1515.

Jambeck, J. R., R. Geyer, C. Wilcox, et  al. 2015. “Plastic Waste Inputs From Land Into the Ocean.” *Science* 347, no. 6223: 768–771.

Jia, T., A. J. Vallendar, R. de Vries, Z. Kapelan, and R. Taormina. 2023. “Advancing Deep Learning-Based Detection of Floating Litter Using a Novel Open Dataset.” *Frontiers in Water* 5: 1298465.

JRC, E. 2016. “European Commission, Joint Research Center. Exploratory Research Project: RIMMEL (RIverine and Marine Floating Macro Litter Monitoring and Modeling of Environmental Loading).”

Karpova, E., E. Abliazov, S. Statkevich, and C. N. Dinh. 2022. “Features of the Accumulation of Macroplastic on the River Bottom in the Mekong Delta and the Impact on Fish and Decapods.” *Environmental Pollution* 297: 118747.

Kawecki, D., and B. Nowack. 2019. “Polymer-Specific Modeling of the

Kiessling, T., K. Knickmeier, K. Kruse, D. Brennecke, A. Nauendorf, and

M. Thiel. 2019. “Plastic Pirates Sample Litter at Rivers in Germany— Riverside Litter and Litter Sources Estimated by Schoolchildren.” *Environmental Pollution* 245: 545–557. Kiessling, T., K. Knickmeier, K. Kruse, et  al. 2021. “Schoolchildren Discover Hotspots of Floating Plastic Litter in Rivers Using a Large-Scale Collaborative Approach.” *Science of the Total Environment* 789: 147849. Kirschke, S., T. H. van Emmerik, S. Nath, C. Schmidt, and K. Wendt-Potthoff. 2023. “Barriers to Plastic Monitoring in Freshwaters in the Global South.” *Environmental Science & Policy* 146: 162–170. Knoblauch, D., and L. Mederake. 2021. “Government Policies Combatting Plastic Pollution.” *Current Opinion in Toxicology* 28: 87–96. Kuizenga, B., P. F. Tasseron, K. Wendt-
Potthoff, and T. H. M. van Emmerik. 2023. “From Source to Sea: Floating Macroplastic Transport Along the Rhine River.” *Frontiers in Environmental Science* 11: 1180872.

Kurniawan, S. B., and M. F. Imron. 2019. “Seasonal Variation of Plastic Debris Accumulation in the Estuary of Wonorejo River, Surabaya, Indonesia.” *Environmental Technology & Innovation* 16: 100490.

Lahat, D., T. Adali, and C. Jutten. 2015. “Multimodal Data Fusion: An Overview of Methods, Challenges, and Prospects.” *Proceedings of the* *IEEE* 103, no. 9: 1449–1477.

Laverre, M., P. Kerhervé, M. Constant, et  al. 2023. “Heavy Rains Control the Floating Macroplastic Inputs Into the Sea From Coastal Mediterranean Rivers: A Case Study on the Têt River (NW Mediterranean Sea).” *Science of the Total Environment* 877: 162733.

Lebreton, L., and A. Andrady. 2019. “Future Scenarios of Global Plastic Waste Generation and Disposal.” *Palgrave Communications* 5, no. 1: 6. [https://doi.org/10.1057/s41599-018-0212-7](https://doi.org/10.1057/s41599-018-0212-7).

Lebreton, L. C., J. Van Der Zwet, J.-

W. Damsteeg, B. Slat, A. Andrady,
and J. Reisser. 2017. “River Plastic Emissions to the World's Oceans.” *Nature Communications* 8, no. 1: 15611.

Li, J., D. Hong, L. Gao, et  al. 2022. “Deep Learning in Multimodal Remote Sensing Data Fusion: A Comprehensive Review.” *International* *Journal of Applied Earth Observation and Geoinformation* 112: 102926.

Lin, F., T. Hou, Q. Jin, and A. You. 2021. “Improved YOLO Based Detection Algorithm for Floating Debris in Waterway.” *Entropy* 23, no. 9: 1111.

Lippiatt, S., S. Opfer, and C. Arthur. 2013. “Marine Debris Monitoring and Assessment: Recommendations for Monitoring Debris Trends in the Marine Environment.”

Liro, M., T. v. Emmerik, B. Wyżga, J. Liro, and P. Mikuś. 2020. “Macroplastic Storage and Remobilization in Rivers.” *Water* 12, no. 7:

2055. Liro, M., P. Mikuś, and B. Wyżga. 2022. “First Insight Into the Macroplastic Storage in a Mountain River: The Role of In-
River Vegetation Cover, Wood Jams and Channel Morphology.” *Science of the* *Total Environment* 838: 156354.

Liro, M., A. Zielonka, H. Hajdukiewicz, et  al. 2023. “Litter Selfie: A Citizen Science Guide for Photorecording Macroplastic Deposition Along Mountain Rivers Using a Smartphone.” *Water* 15, no. 17: 3116.

Liro, M., A. Zielonka, and T. H. van Emmerik. 2023. “Macroplastic 19 of 21 Fragmentation in Rivers.” *Environment International* 180: 108186.

Livoroi, A.- Environmental Emissions of Seven Commodity Plastics as Macro- Lusher, A. L., N. A. Welden, P. Sobral, and M. Cole. 2017. “Sampling, Isolating and Identifying Microplastics Ingested by Fish and Invertebrates.” *Analytical Methods* 9, no. 9: 1346–1360.

MacAfee, E. A., and A. J. Löhr. 2024. “Multi-Scalar Interactions Between Mismanaged Plastic Waste and Urban Flooding in an Era of Climate Change and Rapid Urbanization.” *Wiley Interdisciplinary* *Reviews: Water* 11, no. 2: e1708.

MacLeod, M., H. P. H. Arp, M. B. Tekman, and A. Jahnke. 2021. “The Global Threat From Plastic Pollution.” *Science* 373, no. 6550: 61–65.

Maharjan, N., H. Miyazaki, B. M. Pati, M. N. Dailey, S. Shrestha, and

T. Nakamura. 2022. “Detection of River Plastic Using UAV Sensor Data and Deep Learning.” *Remote Sensing* 14, no. 13: 3049. Malik, N. K. A., L. A. Manaf, N. R. Jamil, M. H. Rosli, Z. H. Ash'aari, and A. S. M. Adhar. 2020. “Variation of Floatable Litter Load and Its Compositions Captured at Floating Debris Boom (FDB) Structure.” *Journal of Material Cycles and Waste Management* 22: 1744–1767. Manfreda, S., and E. B. Dor. 2023. “Remote Sensing of the Environment Using Unmanned Aerial Systems.” In *Unmanned Aerial Systems for* *Monitoring Soil, Vegetation, and Riverine Environments*, 3–36. Elsevier. Manfreda, S., M. F. McCabe, P. E. Miller, et  al. 2018. “On the Use of Unmanned Aerial Systems for Environmental Monitoring.” *Remote* *Sensing* 10, no. 4: 641. Manfreda, S., D. Miglino, K. C. Saddi, et  al. 2024. “Advancing River Monitoring Using Image-
Based Techniques: Challenges and Opportunities.” *Hydrological Sciences Journal* 69, no. 6: 657–677.

Meijer, L. J., T. van Emmerik, R. Van Der Ent, C. Schmidt, and L. Lebreton. 2021. “More Than 1000 Rivers Account for 80% of Global Riverine Plastic Emissions Into the Ocean.” *Science Advances* 7, no. 18: eaaz5803.

Mennekes, D., Y. A. Mellink, L. J. Schreyers, T. H. van Emmerik, and B. Nowack. 2024. “Macroplastic Fate and Transport Modeling: Freshwaters Act as Main Reservoirs.” *ACS ES T Water* 4: 2470–2481.

Mohsen, A., T. Kiss, and F. Kovács. 2023. “Machine Learning-Based Detection and Mapping of Riverine Litter Utilizing Sentinel- 2 Imagery.” *Environmental Science and Pollution Research* 30, no. 25: 67742–67757.

Moore, C. J., G. L. Lattin, and A. Zellers. 2011. “Quantity and Type of Plastic Debris Flowing From Two Urban Rivers to Coastal Waters and Beaches of Southern California.” *Revista de Gestão Costeira Integrada-Journal of Integrated Coastal Zone Management* 11, no. 1: 65–73.

Morritt, D., P. V. Stefanoudis, D. Pearce, O. A. Crimmen, and P. F. Clark. 2014. “Plastic in the Thames: A River Runs Through It.” *Marine* *Pollution Bulletin* 78, no. 1–2: 196–200.

Moshtaghi, M., E. Knaeps, S. Sterckx, S. Garaba, and D. Meire. 2021. “Spectral Reflectance of Marine Macroplastics in the VNIR and SWIR Measured in a Controlled Environment.” *Scientific Reports* 11, no. 1:

5436. Munari, C., M. Scoponi, A. A. Sfriso, et al. 2021. “Temporal Variation of Floatable Plastic Particles in the Largest Italian River, the Po.” *Marine* *Pollution Bulletin* 171: 112805. Nardi, F., C. Cudennec, T. Abrate, et al. 2021. “Citizens and Hydrology (Candhy): Conceptualizing a Transdisciplinary Framework for Citizen Science Addressing Hydrological Challenges.” *Hydrological Sciences* *Journal* 67, no. 16: 2534–2551. Nava, V., S. Chandra, J. Aherne, et al. 2023. “Plastic Debris in Lakes and Reservoirs.” *Nature* 619, no. 7969: 317–322. Nepal, M., and B. Bharadwaj. 2022. “Making Urban Waste Management and Drainage Sustainable in Nepal.” In *Climate Change and Community* *Resilience: Insights From South Asia*, 325–338. Springer. Nihei, Y., H. Ota, M. Tanaka, T. Kataoka, and J. Kashiwada. 2024. 20 of 21 “Comparison of Concentration, Shape, and Polymer Composition
Between Microplastics and Mesoplastics in Japanese River Waters.” *Water Research* 249: 120979.

Noto, S., F. Tauro, A. Petroselli, C. Apollonio, G. Botter, and S. Grimaldi.

2022. “Low-Cost Stage-
Camera System for Continuous Water-Level Monitoring in Ephemeral Streams.” *Hydrological Sciences Journal* 67, no. 9: 1439–1448.

NV5 Geospatial. 2014. “Envi.”

OECD. 2022. *Global Plastics Outlook: Economic Drivers, Environmental* *Impacts and Policy Options*. OECD Publishing.

Omia, E., H. Bae, E. Park, et al. 2023. “Remote Sensing in Field Crop Monitoring: A Comprehensive Review of Sensor Systems, Data Analyses and Recent Advances.” *Remote Sensing* 15, no. 2: 354.

OSPAR, C. 2010. *Guideline for Monitoring Marine Litter on the Beaches* *in the Ospar Maritime Area*, 1. OSPAR Commission.

Oswald, S. B., A. M. Ragas, M. M. Schoor, and F. P. Collas. 2023. “Quantification and Characterization of Macro- and Mesoplastic Items in the Water Column of the River Waal.” *Science of the Total* *Environment* 877: 162827.

Oswald, S. B., A. M. Ragas, M. M. Schoor, and F. P. Collas. 2025. “Plastic Transport in Rivers: Bridging the Gap Between Surface and Water Column.” *Water Research* 269: 122768.

Pinto, R. B., L. Bogerd, M. van der Ploeg, K. Duah, R. Uijlenhoet, and T.

H. van Emmerik. 2024. “Catchment Scale Assessment of Macroplastic Pollution in the Odaw River, Ghana.” *Marine Pollution Bulletin* 198: 115813. Popa, C. L., S. I. Dontu, D. Savastru, and E. M. Carstea. 2022. “Role of Citizen Scientists in Environmental Plastic Litter Research—A Systematic Review.” *Sustainability* 14, no. 20: 13265. Rech, S., V. Macaya-
Caquilpán, J. Pantoja, M. Rivadeneira, C. K. Campodónico, and M. Thiel. 2015. “Sampling of Riverine Litter With Citizen Scientists—Findings and Recommendations.” *Environmental* *Monitoring and Assessment* 187: 1–18.

RiverWatch. 2024. “Riverwatch: A Citizen-Science Approach to River Pollution Monitoring.” [https://riverwatch-prin.github.io/](https://riverwatch-prin.github.io/).

Rochman, C. M. 2018. “Microplastics Research—From Sink to Source.” *Science* 360, no. 6384: 28–29.

Roebroek, C. T., S. Harrigan, T. H. van Emmerik, et al. 2021. “Plastic in Global Rivers: Are Floods Making It Worse?” *Environmental Research* *Letters* 16, no. 2: 025003.

Sakti, A. D., E. Sembiring, P. Rohayani, et  al. 2023. “Identification of Illegally Dumped Plastic Waste in a Highly Polluted River in Indonesia Using Sentinel- 2 Satellite Imagery.” *Scientific Reports* 13, no. 1: 5039.

Salgado-Hernanz, P. M., J. Bauzà, C. Alomar, M. Compa, L. Romero, and S. Deudero. 2021. “Assessment of Marine Litter Through Remote Sensing: Recent Approaches and Future Goals.” *Marine Pollution* *Bulletin* 168: 112347.

Sari, M. M., P. Andarani, S. Notodarmojo, et al. 2022. “Plastic Pollution in the Surface Water in Jakarta, Indonesia.” *Marine Pollution Bulletin* 182: 114023.

Schmidt, C., T. Krauth, and S. Wagner. 2017. “Export of Plastic Debris by Rivers Into the Sea.” *Environmental Science & Technology* 51, no. 21: 12246–12253. *Wiley Interdisciplinary Reviews: Water,* 2025

Schreyers, L., T. van Emmerik, T. L. Nguyen, et al. 2021. “Plastic Plants: The Role of Water Hyacinths in Plastic Transport in Tropical Rivers.” *Frontiers in Environmental Science* 9: 686334.

Simpson, M. D., A. Marino, P. de Maagt, et  al. 2022. “Monitoring of Plastic Islands in River Environment Using Sentinel- 1 SAR Data.” *Remote Sensing* 14, no. 18: 4473. Solé Gómez, l., L. Scandolo, and E. Eisemann. 2022. “A Learning Approach for River Debris Detection.” *International Journal of Applied* *Earth Observation and Geoinformation* 107: 102682.

Stegmann, P., V. Daioglou, M. Londo, D. P. van Vuuren, and M. Junginger. 2022. “Plastic Futures and Their CO₂ Emissions.” *Nature* 612, no. 7939: 272–276.

Tasseron, P., T. van Emmerik, J. Peller, L. Schreyers, and L. Biermann.

2021. “Advancing Floating Macroplastic Detection From Space Using Experimental Hyperspectral Imagery.” *Remote Sensing* 13, no. 12: 2335. Tasseron, P. F., L. Schreyers, J. Peller, L. Biermann, and T. van Emmerik.
2022. “Toward Robust River Plastic Detection: Combining Lab and Field-Based Hyperspectral Imagery.” *Earth and Space Science* 9, no. 11: e2022EA002518. [https://doi.org/10.1029/2022EA002518](https://doi.org/10.1029/2022EA002518). Tauro, F., S. Noto, G. Botter, and S. Grimaldi. 2022. “Assessing the Optimal Stage-
Cam Target for Continuous Water Level Monitoring in Ephemeral Streams: Experimental Evidence.” *Remote Sensing* 14, no. 23: 6064.

Tauro, F., C. Pagano, P. Phamduy, S. Grimaldi, and M. Porfiri. 2015. “Large-Scale Particle Image Velocimetry From an Unmanned Aerial Vehicle.” *IEEE/ASME Transactions on Mechatronics* 20, no. 6: 3269–3275.

Tauro, F., A. Petroselli, and E. Arcangeletti. 2016. “Assessment of Drone-Based Surface Flow Observations.” *Hydrological Processes* 30, no. 7: 1114–1130.

Tauro, F., M. Porfiri, and S. Grimaldi. 2016. “Surface Flow Measurements From Drones.” *Journal of Hydrology* 540: 240–245.

Tauro, F., J. Selker, N. van de Giesen, et al. 2018. “Measurements and

Disciplinarity to Sense the Hydrological Cycle.” *Hydrological Sciences* *Journal* 63, no. 2: 169–196.

Themistocleous, K., C. Papoutsa, S. Michaelides, and D. Hadjimitsis.

2020. “Investigating Detection of Floating Plastic Litter From Space Using Sentinel-
2 Imagery.” *Remote Sensing* 12, no. 16: 2648.

Tosi, F., M. Rocca, F. Aleotti, et  al. 2020. “Enabling Image-Based Streamflow Monitoring at the Edge.” *Remote Sensing* 12, no. 12: 2047.

Tramoy, R., J. Gasperi, L. Colasse, et al. 2020. “Transfer Dynamics of Macroplastics in Estuaries—New Insights From the Seine Estuary: Part

2. Short-Term Dynamics Based on GPS-
Trackers.” *Marine Pollution* *Bulletin* 160: 111566.

Tramoy, R., J. Gasperi, L. Colasse, and B. Tassin. 2020. “Transfer Dynamic of Macroplastics in Estuaries—New Insights From the Seine Estuary: Part 1. Long Term Dynamic Based on Date-Prints on Stranded Debris.” *Marine Pollution Bulletin* 152: 110894.

Tursi, A., M. Baratta, T. Easton, et al. 2022. “Microplastics in Aquatic Systems, a Comprehensive Review: Origination, Accumulation, Impact, and Removal Technologies.” *RSC Advances* 12, no. 44: 28318–28340.

van Emmerik, T., S. de Lange, R. Frings, et al. 2022. “Hydrology as a Driver of Floating River Plastic Transport.” *Earth's Future* 10, no. 8: e2022EF002811.

van Emmerik, T., M. Loozen, K. Van Oeveren, F. Buschman, and G. Prinsen. 2019. “Riverine Plastic Emission From Jakarta Into the Ocean.” *Environmental Research Letters* 14, no. 8: 084033.

van Emmerik, T., Y. Mellink, R. Hauk, K. Waldschläger, and L. Schreyers. 2022. “Rivers as Plastic Reservoirs.” *Frontiers in Water* 3: 786936.

van Emmerik, T., C. Roebroek, W. De Winter, P. Vriend, M. Boonstra, and M. Hougee. 2020. “Riverbank Macrolitter in the Dutch Rhine– Meuse Delta.” *Environmental Research Letters* 15, no. 10: 104087.

van Emmerik, T., and A. Schwarz. 2020. “Plastic Debris in Rivers.” *WIREs Water* 7, no. 1: e1398. [https://doi.org/10.1002/wat2.1398](https://doi.org/10.1002/wat2.1398).

van Emmerik, T., J. Seibert, B. Strobl, et  al. 2020. “Crowd-Based Observations of Riverine Macroplastic Pollution.” *Frontiers in Earth* *Science* 8: 298.

van Emmerik, T., J. van Klaveren, L. J. J. Meijer, J. W. Krooshof, D. A.

A. Palmos, and M. A. Tanchuling. 2020. “Manila River Mouths Act as Temporary Sinks for Macroplastic Pollution.” *Frontiers in Marine* *Science* 7: 1–8. van Emmerik, T., P. Vriend, and J. Roebroek. 2020. *An Evaluation of the* *River-OSPAR Method for Quantifying Macrolitter on Dutch Riverbanks*. Wageningen University. van Emmerik, T. H., S. Kirschke, L. J. Schreyers, S. Nath, C. Schmidt, and K. Wendt-
Potthoff. 2023. “Estimating Plastic Pollution in Rivers Through Harmonized Monitoring Strategies.” *Marine Pollution Bulletin* 196: 115503.

van Emmerik, T. H., L. J. Schreyers, Y. A. Mellink, T. Sok, and M.

E. Arias. 2023. “Large Variation in Mekong River Plastic Transport Between Wet and Dry Season.” *Frontiers in Environmental Science* 11: 1173946. van Lieshout, C., K. van Oeveren, T. Emmerik, and E. Postma. 2020. “Automated River Plastic Monitoring Using Deep Learning and Cameras.” *Earth and Space Science* 7, no. 8: e2019EA000960. https:// doi.org/10.1029/2019EA000960. Vighi, M., L. Ruiz-
Orejón, and G. Hanke. 2022. *Monitoring of Floating* *Marine Macro Litter*. European Commission.

Vriend, P., C. van Calcar, M. Kooi, H. Landman, R. Pikaar, and T. van Emmerik. 2020. “Rapid Assessment of Floating Macroplastic Transport in the Rhine.” *Frontiers in Marine Science* 7: 10. [https://doi.org/10.3389/](https://doi.org/10.3389/) fmars.2020.00010.

Wang, M., and C. Hu. 2016. “Mapping and Quantifying Sargassum Distribution and Coverage in the Central West Atlantic Using MODIS Observations.” *Remote Sensing of Environment* 183: 350–367.

Waqas, M., M. S. Wong, A. Stocchino, S. Abbas, S. Hafeez, and R. Zhu.

2023. “Marine Plastic Pollution Detection and Identification by Using Remote Sensing-
Meta Analysis.” *Marine Pollution Bulletin* 197: 115746.

Weideman, E. A., V. Perold, and P. G. Ryan. 2020. “Limited Long-Distance Transport of Plastic Pollution by the Orange-Vaal River System, South Africa.” *Science of the Total Environment* 727: 138653.

Wendt-Potthoff, K., T. Avellán, T. van Emmerik, et al. 2020. *Monitoring* *Plastics in Rivers and Lakes: Guidelines for the Harmonization of* *Methodologies*. United Nations Environment Programme.

Winton, D. J., L. G. Anderson, S. Rocliffe, and S. Loiselle. 2020. “Macroplastic Pollution in Freshwater Environments: Focusing Public and Policy Action.” *Science of the Total Environment* 704: 135242.

Wolf, M., K. van den Berg, S. P. Garaba, et al. 2020. “Machine Learning for Aquatic Plastic Litter Detection, Classification and Quantification (Aplastic-q).” *Environmental Research Letters* 15, no. 11: 114042.

Zhao, B., R. E. Richardson, and F. You. 2024. “Microplastics Monitoring in Freshwater Systems: A Review of Global Efforts, Knowledge Gaps, and Research Priorities.” *Journal of Hazardous Materials* 477: 135329. 21 of 21

Observations in the XXI Century (MOXXI): Innovation and Multi-