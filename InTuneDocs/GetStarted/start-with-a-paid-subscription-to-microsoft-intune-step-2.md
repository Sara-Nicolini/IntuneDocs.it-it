---
# required metadata

title: Configurare un nome di dominio personalizzato | Microsoft Intune
description:
keywords:
author: Staciebarker
manager: jeffgilb
ms.date: 04/28/2016
ms.topic: get-started-article
ms.prod:
ms.service: microsoft-intune
ms.technology:
ms.assetid: 2382f36f-13d8-4a32-81ad-6cfa604889c3

# optional metadata

#ROBOTS:
#audience:
#ms.devlang:
ms.reviewer: jeffgilb
ms.suite: ems
#ms.tgt_pltfrm:
#ms.custom:

---


# Configurare un nome di dominio personalizzato

Per impostazione predefinita, Intune usa il nome di dominio **<domain>.onmicrosoft.com** creato al momento dell'iscrizione al servizio. Quando l'azienda dispone di un dominio personalizzato, è possibile configurare la propria istanza di Intune in modo da usare quel dominio anziché quello fornito con la sottoscrizione.

Prima di creare nuovi account utente oppure sincronizzare gli account dall'istanza locale di Active Directory, è consigliabile decidere subito se usare solo il dominio .onmicrosoft.com oppure aggiungere uno o più nomi di dominio personalizzati. La configurazione di un dominio personalizzato prima dell'aggiunta degli utenti può contribuire a semplificare la gestione delle identità per la sottoscrizione consentendo agli utenti di effettuare l'accesso con le stesse credenziali che usano per accedere ad altre risorse di dominio.

Quando si sottoscrive un servizio cloud Microsoft, l'istanza del servizio ottenuta è un [tenant di Azure AD](http://technet.microsoft.com/library/jj573650.aspx#BKMK_WhatIsAnAzureADTenant) di Microsoft, che fornisce identità e servizi di directory per il servizio cloud. Poiché le attività necessarie per configurare Intune in modo da usare il nome di dominio personalizzato aziendale sono le stesse che per altri tenant Azure Active Directory, usare le informazioni e le procedure disponibili in [Aggiungere un nome di dominio personalizzato ad Azure Active Directory](https://azure.microsoft.com/documentation/articles/active-directory-add-domain/)..

> [!TIP]
> Per altre informazioni sull'uso del dominio personalizzato con un servizio basato su cloud Microsoft, vedere [Panoramica concettuale dei nomi di dominio personalizzati in Azure Active Directory](https://azure.microsoft.com/documentation/articles/active-directory-add-domain-concepts/).

### Passaggi successivi
A questo punto, Passaggio 2 della *Guida introduttiva di Intune* completato.

>[!div class="step-by-step"]

>[&larr; **Accedere a Intune**](.\start-with-a-paid-subscription-to-microsoft-intune-step-1.md)     [**Aggiungere utenti a Intune** &rarr;](.\start-with-a-paid-subscription-to-microsoft-intune-step-3.md)  


<!--HONumber=May16_HO1-->


