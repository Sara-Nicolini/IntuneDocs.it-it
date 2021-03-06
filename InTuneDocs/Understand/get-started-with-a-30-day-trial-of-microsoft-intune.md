---
# required metadata

title: Guida alla valutazione di Intune | Microsoft Intune
description:
keywords:
author: Staciebarker
manager: jeffgilb
ms.date: 04/28/2016
ms.topic: get-started-article
ms.prod:
ms.service: microsoft-intune
ms.technology:
ms.assetid: 619a1d11-3d22-4635-8f70-770eba3e1712

# optional metadata

#ROBOTS:
#audience:
#ms.devlang:
ms.reviewer: jeffgilb
ms.suite: ems
#ms.tgt_pltfrm:
#ms.custom:

---

# Guida alla valutazione di Intune
La configurazione di una versione di valutazione gratuita per 30 giorni di Microsoft Intune per gestire i dispositivi mobili e i computer è un’attività facile e veloce. Nella versione di valutazione è possibile aggiungere fino a 100 utenti e dispositivi, impostare i gruppi, configurare i criteri di conformità e registrare e gestire i dispositivi mobili e i computer in pochi passaggi.

In questo argomento vengono spiegate le informazioni di base per attivare ed eseguire una versione di valutazione di Intune e viene illustrata una panoramica del servizio di Intune in modo da poterne valutare caratteristiche e funzionalità.

Questo video dimostrativo della durata di cinque minuti spiega com’è facile iniziare a usare una versione di valutazione gratuita di Microsoft Intune e gestire i dispositivi:

<iframe width="675" height="480" src="https://www.youtube.com/embed/ltcZvm4VOFU" frameborder="0" allowfullscreen></iframe>

## Prima di iniziare
Prima di iniziare a usare Intune, è necessario:

-   Un dispositivo con un Web browser abilitato per Silverlight da usare per accedere ai siti Web in cui verranno creati gli account utente di Intune (l'**interfaccia di amministrazione di Office 365**) e dove vengono gestiti dispositivi, gruppi e criteri (la **console di amministrazione di Intune**)).

-   Un secondo dispositivo con un Web browser da usare per testare la modalità di registrazione e di gestione dei dispositivi degli utenti Intune tramite il portale aziendale. Verrà testato anche il modo con cui gli utenti trovano e installano le app e richiedono l'assistenza degli amministratori. Se non si ha un secondo dispositivo, è possibile impostare la modalità di privacy nello stesso browser usato per l'amministrazione di Intune. Ad esempio, in Internet Explorer è possibile fare clic su **Strumenti** &gt; **InPrivate Browsing**).

-   Se è disponibile un account Microsoft Online Services, sono necessarie le credenziali di amministratore per l'account. Le credenziali di amministratore tenant non sono necessarie se non si dispone di un account di questo tipo oppure si vuole usare questo tenant di Intune solo per una valutazione.

-   Se si intende gestire dispositivi iOS o Windows Phone con la versione di valutazione di Intune, sono necessari certificati, o chiavi, e account per recuperare i certificati (vedere la tabella seguente). Con i dispositivi Android non sono necessari certificati aggiuntivi.

    |Piattaforma|Requisiti relativi ai certificati|Altre informazioni|
    |------------|----------------------------|--------------------|
    |Windows Phone 8.1 e Windows Phone 8 |Non è necessario alcun certificato per gli utenti di Windows Phone 8.1 che installano l'app Portale aziendale dallo Store. È richiesto un certificato Symantec per gli utenti di Windows Phone 8.0 oppure per usare Intune per distribuire l'app Portale aziendale in dispositivi Windows Phone 8.1.|Questa guida presuppone che gli utenti scarichino l'app Portale aziendale dallo Store in un dispositivo Windows Phone 8.1 o di una versione successiva. Per informazioni sul supporto di Windows Phone 8.0, vedere [Set up Windows Phone management with Microsoft Intune](/Intune/DeployUse/set-up-windows-phone-management-with-microsoft-intune) (Impostare la gestione di Windows Phone con Microsoft Intune).|
    |Dispositivi Windows 10, Windows RT 8.1, Windows RT o Windows 8.1|Non sono previsti requisiti del certificato per registrare i dispositivi Windows RT e Windows.|[Installare il client PC Windows con Microsoft Intune](/Intune/DeployUse/install-the-windows-pc-client-with-microsoft-intune).|
    |iOS 7.1 o versione successiva|Ottenere un certificato per il servizio Apple Push Notification.|Richiedere da Apple un certificato di Apple Push Notification Service, come descritto in: [Set up iOS and Mac management with Microsoft Intune](/Intune/DeployUse/set-up-ios-and-mac-management-with-microsoft-intune) (Impostare la gestione iOS e Mac con Microsoft Intune).|

## Passaggi per completare una valutazione di 30 giorni di Intune
- [Passaggio 1: Accedere o iscriversi per una valutazione di 30 giorni](get-started-with-a-30-day-trial-of-microsoft-intune-step-1.md). Prima di iscriversi o accedere a Intune, valutare se accedere con un account esistente o creare un account temporaneo da usare solo per il periodo della valutazione di 30 giorni di Microsoft Intune.
- [Passaggio 2: Aggiungere utenti](get-started-with-a-30-day-trial-of-microsoft-intune-step-2.md). Dopo aver configurato l'account, aggiungere singoli account utente a Intune oppure aggiungere gli utenti in blocco (vedere le istruzioni in questa sezione). Prima di iniziare, è importante comprendere come vengono gestiti gli account amministratore in Intune.
- [Passaggio 3: Creare gruppi per organizzare utenti e dispositivi](get-started-with-a-30-day-trial-of-microsoft-intune-step-3.md). I gruppi in Intune offrono una grande flessibilità per la gestione di dispositivi e utenti. È possibile configurare i gruppi in base alle esigenze dell'organizzazione, ad esempio per località geografica, reparto o caratteristiche dell'hardware, e usarli per eseguire una vasta gamma di attività amministrative, dall'impostazione dei criteri per un set di utenti alla distribuzione di applicazioni a un set di dispositivi.
- [Passaggio 4: Creare i criteri e pubblicare un'app](get-started-with-a-30-day-trial-of-microsoft-intune-step-4.md). I criteri di Intune specificano impostazioni che consentono di controllare le configurazioni di sicurezza dei dispositivi mobili, di eseguire la manutenzione delle impostazioni di Windows Firewall e Endpoint Protection per i computer, nonché di distribuire applicazioni.
- [Passaggio 5: Registrare dispositivi mobili e installare un'app](get-started-with-a-30-day-trial-of-microsoft-intune-step-5.md). Per configurare la gestione dei dispositivi mobili con Intune, è necessario impostare prima l'autorità di gestione dei dispositivi mobili, abilitare la gestione per piattaforme dei dispositivi specifiche e registrare i dispositivi con l'app Portale aziendale. È quindi possibile distribuire l'app Microsoft Skype pubblicata.
- [Passaggio 6: Altre opzioni e funzionalità aggiuntive](get-started-with-a-30-day-trial-of-microsoft-intune-step-6.md). Scegliere come usare avvisi, report e altre funzionalità di Intune per soddisfare le esigenze aziendali.
- [Passaggio 7: Fasi successive](get-started-with-a-30-day-trial-of-microsoft-intune-step-7.md). Prepararsi a passare a una sottoscrizione a pagamento di Intune e sfruttare i vantaggi del FastTrack Center Benefit di Intune.


### Passaggi successivi
Ora è possibile avviare la sottoscrizione per la valutazione di 30 giorni.

>[!div class="step-by-step"]
[**Iscriversi a Intune** &rarr;](.\get-started-with-a-30-day-trial-of-microsoft-intune-step-1.md)

### Vedere anche
[Guida introduttiva a Intune](/intune/get-started/start-with-a-paid-subscription-to-microsoft-intune)


<!--HONumber=May16_HO1-->


