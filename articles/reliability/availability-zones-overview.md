---
title: What are Azure regions and availability zones?
description: Learn about regions and availability zones and how they work to help you achieve reliability
ms.service: reliability
ms.subservice: availability-zones
ms.topic: conceptual
ms.date: 10/25/2022
ms.author: anaharris
author: anaharris
ms.reviewer: asinghal
ms.custom: references_regions
---


# Che cosa sono le aree e le zone di disponibilità di Azure?

ALe aree e le zone di disponibilità di Azure sono progettate per aiutarti a ottenere affidabilità per i carichi di lavoro business-critical. Azure gestisce più aree geografiche. Queste differenti demarcazioni definiscono i limiti del ripristino di emergenza e della residenza dei dati in una o più aree di Azure. Il mantenimento di molte regioni garantisce che i clienti siano supportati in tutto il mondo.

## Regioni

Ogni area di Azure include data center distribuiti all'interno di un perimetro definito dalla latenza. Sono connessi tramite una rete regionale dedicata a bassa latenza. Questa progettazione garantisce che i servizi di Azure in qualsiasi area offrano le migliori prestazioni e sicurezza possibili. 

Per vedere quali aree supportano le zone di disponibilità, vedere Aree di Azure con supporto per le zone di disponibilità.(availability-zones-service-support.md#azure-regions-with-availability-zone-support).

## Zone di disponibilità

Gli errori possono variare da guasti software e hardware a eventi come terremoti, inondazioni e incendi. La tolleranza agli errori viene raggiunta grazie alla ridondanza e all'isolamento logico dei servizi di Azure. Per garantire la resilienza, in tutte le aree abilitate per le zone di disponibilità sono presenti almeno tre zone di disponibilità separate.

Le zone di disponibilità di Azure sono connesse da una rete ad alte prestazioni con una latenza di andata e ritorno inferiore a 2 ms. Aiutano i tuoi dati a rimanere sincronizzati e accessibili quando le cose vanno male. Ogni zona è composta da uno o più data center dotati di infrastrutture di alimentazione, raffreddamento e rete indipendenti. Le zone di disponibilità sono progettate in modo che, se una zona è interessata, i servizi regionali, la capacità e la disponibilità elevata siano supportati dalle altre due zone.

![Image showing physically separate availability zone locations within an Azure region.](media/availability-zones.png)

Le posizioni dei data center vengono selezionate utilizzando rigorosi criteri di valutazione del rischio di vulnerabilità. Questo processo identifica tutti i rischi significativi specifici del data center e considera i rischi condivisi tra le zone di disponibilità.

Con le zone di disponibilità, è possibile progettare e gestire applicazioni e database che passano automaticamente da un'area all'altra senza interruzioni. Le zone di disponibilità di Azure sono a disponibilità elevata, a tolleranza di errore e più scalabili rispetto alle tradizionali infrastrutture di data center singole o multiple.

Ogni data center è assegnato a una zona fisica. Le aree fisiche vengono mappate alle aree logiche nella sottoscrizione di Azure. Alle sottoscrizioni di Azure viene assegnato automaticamente questo mapping al momento della creazione di una sottoscrizione. È possibile usare l'API ARM dedicata denominata: checkZonePeers (/rest/api/resources/subscriptions/check-zone-peers) checkZonePeers per  confrontare il mapping delle zone per soluzioni resilienti che si estendono su più sottoscrizioni.

È possibile progettare soluzioni resilienti usando i servizi di Azure che usano le zone di disponibilità. Collocare le risorse di elaborazione, archiviazione, rete e dati in una zona di disponibilità e replicare questa disposizione in altre zone di disponibilità.

I servizi abilitati per le zone di disponibilità di Azure sono progettati per fornire il giusto livello di resilienza e flessibilità. Possono essere configurati in due modi. Possono essere ridondanti di zona, con replica automatica tra zone, o zonali, con istanze aggiunte a una zona specifica. È inoltre possibile combinare questi approcci.

Alcune organizzazioni richiedono un'elevata disponibilità di zone di disponibilità e protezione da fenomeni su larga scala e disastri regionali. Le aree di Azure sono progettate per offrire protezione contro le emergenze localizzate con zone di disponibilità e protezione dalle emergenze geografiche o di grandi dimensioni con ripristino di emergenza, usando un'altra area. Per altre informazioni su business continuity, disaster recovery e replica tra aree, vedere Replica tra aree in Azure. [Replica Cross-region in Azure](cross-region-replication-azure.md).

![Image showing availability zones that protect against localized disasters and regional or large geography disasters by using another region.](media/availability-zones-region-geography.png)

To see which services support availability zones, see [Azure regions with availability zone support](availability-zones-service-support.md#azure-regions-with-availability-zone-support).


## Next steps

> [!div class="nextstepaction"]
> [Azure services and regions with availability zones](availability-zones-service-support.md)

> [!div class="nextstepaction"]
> [Availability zone migration guidance](availability-zones-migration-overview.md)

> [!div class="nextstepaction"]
> [Availability of service by category](availability-service-by-category.md)

> [!div class="nextstepaction"]
> [Microsoft commitment to expand Azure availability zones to more regions](https://azure.microsoft.com/blog/our-commitment-to-expand-azure-availability-zones-to-more-regions/)

> [!div class="nextstepaction"]
> [Build solutions for high availability using availability zones](/azure/architecture/high-availability/building-solutions-for-high-availability)
