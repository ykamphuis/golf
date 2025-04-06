import { useState } from 'react';
import { Card, CardContent } from '@/components/ui/card';
import { Button } from '@/components/ui/button';
import { Tabs, TabsList, TabsTrigger, TabsContent } from '@/components/ui/tabs';

const models = [
  { name: 'Golf 5', img: 'https://tse4.mm.bing.net/th?id=OIP.SJRzNrSi0FZALnuoHP6RmQHaFj&pid=Api' },
  { name: 'Golf 6', img: 'https://tse3.mm.bing.net/th?id=OIP.7--PENfmqYea8Sm6IHCfWgHaFP&pid=Api' },
  { name: 'Golf 7', img: 'https://cdn.pixabay.com/photo/2017/09/12/13/41/auto-2748120_1280.jpg' },
  { name: 'Golf 7.5', img: 'https://tse1.mm.bing.net/th?id=OIP.z2Gr1fgF-tdsG0OWXn3pVQHaEK&pid=Api' },
  { name: 'Golf 8', img: 'https://tse2.mm.bing.net/th?id=OIP.3cZ__ggWBl-UQaGKHn-6PwHaE8&pid=Api' },
  { name: 'Golf 8.5', img: 'https://tse4.mm.bing.net/th?id=OIP.DVeUIQi6OlhcmRxRxN9ljwHaEK&pid=Api' },
];

const upgradesData = {
  'Golf 5': {
    motor: [
      {
        name: 'K&N Performance Luchtfilter',
        img: 'https://cdn.knfilters.com/images/l/knfilters-57s-9500-performance-air-intake-system.jpg',
        price: '€89,00',
        link: 'https://www.knfilters.com',
      },
      {
        name: 'Milltek Sport Uitlaatsysteem',
        img: 'https://cdn.performanceexhausts.com/images/milltek-mk5-gti.jpg',
        price: '€699,00',
        link: 'https://www.millteksport.com',
      },
    ],
    exterieur: [
      {
        name: 'Maxton Design Bodykit',
        img: 'https://tse2.mm.bing.net/th?id=OIP.6apio_TXk4TTBmqD6IVpegHaFj&pid=Api',
        price: '€320,00',
        link: 'https://www.maxtondesign.co.uk/vw-golf-mk5',
      },
    ],
    interieur: [
      {
        name: 'Aluminium DSG Schakelpeddels',
        img: 'https://cdn.shopify.com/s/files/1/0608/0461/3720/products/schakelpeddels.jpg',
        price: '€45,00',
        link: 'https://www.performanceparts.nl',
      },
    ],
    verlagingsets: [
      {
        name: 'FK Coilover Set',
        img: 'https://tse3.mm.bing.net/th/id/OIP.NXZyveJuQ1qRA3YlF37bigHaE7?pid=Api',
        price: '€479,00',
        link: 'https://fk-coilovers.com/products/fk-coilovers-volkswagen-golf-5',
      },
    ],
  },
  'Golf 6': {
    motor: [
      {
        name: 'APR Stage 1 ECU Upgrade',
        img: 'https://www.goapr.com/includes/img/products/ecu_upgrade.jpg',
        price: '€599,00',
        link: 'https://www.goapr.com/products/ecu_upgrade/parts/ECU-20T-EA888-1',
      },
      {
        name: 'Forge Motorsport Intercooler',
        img: 'https://www.forgemotorsport.co.uk/images/products/FMGOLF6FMIC.jpg',
        price: '€850,00',
        link: 'https://www.forgemotorsport.co.uk/Front_Mounting_Intercooler_for_VW_Golf_Mk6--product--1007.html',
      },
    ],
    exterieur: [
      {
        name: 'Maxton Design Voorspoiler',
        img: 'https://www.uwautoonderdeel.nl/Files/2/18000/18979/ProductPhotos/Source/maxton-design-volkswagen-golf-6-voorspoiler-spoiler-splitter-1.jpg',
        price: '€169,95',
        link: 'https://www.uwautoonderdeel.nl/Maxton-Design-Golf-6-Splitter-Spoiler-Diffuser-Tsi-Tdi-Fsi-R20-Gti',
      },
      {
        name: 'Maxton Design Achterdiffuser',
        img: 'https://www.uwautoonderdeel.nl/Files/2/18000/18979/ProductPhotos/Source/maxton-design-volkswagen-golf-6-achterdiffuser-1.jpg',
        price: '€194,00',
        link: 'https://www.uwautoonderdeel.nl/Maxton-Design-Golf-6-Splitter-Spoiler-Diffuser-Tsi-Tdi-Fsi-R20-Gti',
      },
    ],
    interieur: [
      {
        name: 'GTI Edition Schakelpook',
        img: 'https://www.uwautoonderdeel.nl/Files/2/18000/18979/ProductPhotos/Source/dsg-pook-knop-vervangen-leder-met-rood-bies-accent-gti-tcr-clubsport-look-1.jpg',
        price: '€34,95',
        link: 'https://www.uwautoonderdeel.nl/Dsg-Pook-knop-Vervangen-leder-met-rood-bies-accent-GTI-Tcr-Clubsport-look',
      },
    ],
    verlagingsets: [
      {
        name: 'H&R Verlaging Veren Set',
        img: 'https://www.hrsprings.com/application/search/results/4/1/2010',
        price: '€220,00',
        link: 'https://www.hrsprings.com/application/search/results/4/1/2010',
      },
    ],
  },
  'Golf 7': {
    motor: [
      {
        name: 'RacingLine Performance R
::contentReference[oaicite:5]{index=5}
 
