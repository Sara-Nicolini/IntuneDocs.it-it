---
# required metadata

title: Usare la cancellazione remota per proteggere i dati | Microsoft Intune
description:
keywords:
author: NathBarn
manager: jeffgilb
ms.date: 04/28/2016
ms.topic: article
ms.prod:
ms.service: microsoft-intune
ms.technology:
ms.assetid: 8519e411-3d48-44eb-9b41-3e4fd6a93112

# optional metadata

#ROBOTS:
#audience:
#ms.devlang:
ms.reviewer: jeffgilb
ms.suite: ems
#ms.tgt_pltfrm:
#ms.custom:

---

# Proteggere i dati con la cancellazione selettiva o completa tramite Microsoft Intune
Come con i dispositivi, a un certo punto è preferibile o necessario [ritirare le applicazioni](retire-apps-using-microsoft-intune.md) distribuite su PC e dispositivi mobili in quanto non più necessarie. Si potrebbe anche voler rimuovere dati aziendali dal dispositivo. A tale scopo, Intune offre funzionalità di cancellazione completa e selettiva. Poiché i dispositivi mobili possono memorizzare dati aziendali riservati e garantire l'accesso a numerose risorse aziendali, è possibile eseguire un comando di cancellazione remota da Intune per cancellare il contenuto di un dispositivo perso o rubato. Gli utenti possono inviare un comando di cancellazione remota dei dati del dispositivo anche da Intune su dispositivi privati registrati in Intune.

  > [!NOTE]
  > Questo argomento riguarda solo la cancellazione dei dispositivi gestiti da Intune. Anche il [portale di anteprima di Azure](https://portal.azure.com) può essere usato per [cancellare i dati aziendali dalle app](wipe-managed-company-app-data-with-microsoft-intune.md)

## Cancellazione completa


La **cancellazione completa** ripristina le impostazioni predefinite di un dispositivo rimuovendo tutti i dati e le impostazioni dell'azienda e dell'utente. Il dispositivo verrà rimosso da Intune. La cancellazione completa è utile per la reimpostazione di un dispositivo prima di consegnarlo a un nuovo utente o nei casi in cui il dispositivo è stato smarrito o rubato.  **Prestare attenzione alla selezione della cancellazione completa. Non sarà possibile recuperare i dati nel dispositivo**.

## Cancellazione selettiva

La **cancellazione selettiva** rimuove i dati aziendali, compresi i dati sulla gestione delle app mobili (MAM), ove applicabile, le impostazioni e i profili di posta elettronica da un dispositivo. La cancellazione selettiva lascia i dati personali dell'utente sul dispositivo. Il dispositivo verrà rimosso da Intune. La tabella seguente descrive i dati che vengono rimossi in base al tipo di piattaforma e l'effetto sui dati che rimangono nel dispositivo dopo una cancellazione selettiva.

**iOS**

|Tipo di dati|iOS|
|-------------|-------|
|App aziendali e dati associati installati da Intune.|Le app vengono disinstallate e vengono rimossi i dati dell'app aziendale.<br /><br />I dati delle app Microsoft che usano la gestione delle app mobili vengono rimossi. L'app non viene rimossa.|
|Impostazioni|Le configurazioni dei criteri di Intune non vengono più applicate e gli utenti possono modificare le impostazioni.|
|Impostazioni del profilo Wi-Fi e VPN|Rimosso|
|Impostazioni del profilo certificato|Certificati rimossi e revocati.|
|Agente di gestione|Il profilo di gestione viene rimosso.|
|Posta elettronica|I profili di posta elettronica di cui viene eseguito il provisioning tramite Intune vengono rimossi e il messaggio di posta elettronica memorizzato nella cache del dispositivo viene eliminato.|
|Separazione di Azure Active Directory (AAD)|Record AAD rimosso|
|Contatti | I contatti sincronizzati direttamente dall'app alla Rubrica nativa vengono rimossi.  Tutti i contatti sincronizzati dalla Rubrica nativa a un'altra origine esterna non possono essere cancellati. <br /> <br />Attualmente è supportata solo l'app Outlook.

**Android**

|Tipo di dati|Android|Android Samsung KNOX|
|-------------|-----------|------------------------|
|Collegamenti Web|Rimosso.|Rimosso|
|App Google Play non gestite|Le app e i dati rimangono installati|Le app e i dati rimangono installati|
|App line-of-business non gestite|Le app e i dati rimangono installati|Le app vengono disinstallate e, di conseguenza, i dati locali delle app vengono rimossi. Non vengono rimossi i dati esterni all'app, ad esempio quelli presenti sulla scheda SD.|
|App Google Play gestite|I dati dell'app vengono rimossi. L'app non viene rimossa. I dati protetti dalla crittografia MAM all'esterno dell'app (scheda SD e così via) restano crittografati e sono inutilizzabili, ma non vengono rimossi.|I dati dell'app vengono rimossi. L'app non viene rimossa. I dati protetti dalla crittografia MAM all'esterno dell'app (scheda SD e così via) restano crittografati, ma non vengono rimossi.|
|App line-of-business gestite|I dati dell'app vengono rimossi. L'app non viene rimossa. I dati protetti dalla crittografia MAM all'esterno dell'app (scheda SD e così via) restano crittografati e sono inutilizzabili, ma non vengono rimossi.|I dati dell'app vengono rimossi. L'app non viene rimossa. I dati protetti dalla crittografia MAM all'esterno dell'app (scheda SD e così via) restano crittografati, ma non vengono rimossi.|
|Impostazioni|Le configurazioni dei criteri di Intune non vengono più applicate e gli utenti possono modificare le impostazioni.|Le configurazioni dei criteri di Intune non vengono più applicate e gli utenti possono modificare le impostazioni.|
|Impostazioni del profilo Wi-Fi e VPN|Rimosso|Rimosso|
|Impostazioni del profilo certificato|Certificati revocati, ma non rimossi.|Certificati rimossi e revocati.|
|Agente di gestione|Il privilegio di amministratore del dispositivo viene revocato.|Il privilegio di amministratore del dispositivo viene revocato.|
|Posta elettronica|I messaggi di posta elettronica ricevuti dall'app Microsoft Outlook per Android vengono rimossi.|I profili di posta elettronica di cui viene eseguito il provisioning tramite Intune vengono rimossi e il messaggio di posta elettronica memorizzato nella cache del dispositivo viene eliminato.|
|Separazione di Azure Active Directory (AAD)|Record AAD rimosso|Record AAD rimosso|
|Contatti | I contatti sincronizzati direttamente dall'app alla Rubrica nativa vengono rimossi.  Tutti i contatti sincronizzati dalla Rubrica nativa a un'altra origine esterna non possono essere cancellati. <br /> <br />Attualmente è supportata solo l'app Outlook.|I contatti sincronizzati direttamente dall'app alla Rubrica nativa vengono rimossi.  Tutti i contatti sincronizzati dalla Rubrica nativa a un'altra origine esterna non possono essere cancellati. <br /> <br />Attualmente è supportata solo l'app Outlook.

**Windows**

|Tipo di dati|Windows 8.1 (MDM) e Windows RT 8.1|Windows RT|Windows Phone 8 e Windows Phone 8.1|Windows 10|
|-------------|----------------------------------------------------------------|--------------|-----------------------------------------|--------|
|App aziendali e dati associati installati da Intune.|Ai file protetti da EFS verrà revocata la chiave e l'utente non sarà in grado di aprire i file.|Le app aziendali non verranno rimosse.|Vengono disinstallate le app installate inizialmente tramite il portale aziendale e vengono rimossi i dati dell'app aziendale.|Le app vengono disinstallate e le chiavi di trasferimento locale vengono rimosse.|
|Impostazioni|Le configurazioni dei criteri di Intune non vengono più applicate e gli utenti possono modificare le impostazioni.|Le configurazioni dei criteri di Intune non vengono più applicate e gli utenti possono modificare le impostazioni.|Le configurazioni dei criteri di Intune non vengono più applicate e gli utenti possono modificare le impostazioni.|Le configurazioni dei criteri di Intune non vengono più applicate e gli utenti possono modificare le impostazioni.|
|Impostazioni del profilo Wi-Fi e VPN|Rimosso|Rimosso|Non supportato|Rimosso|
|Impostazioni del profilo certificato|Certificati rimossi e revocati.|Certificati rimossi e revocati.|Non supportato|Certificati rimossi e revocati.|
|Posta elettronica|Rimuove le applicazioni di posta elettronica abilitate per EFS, tra cui i messaggi e gli allegati dell'applicazione Windows Mail.|Non supportato|I profili di posta elettronica di cui viene eseguito il provisioning tramite Intune vengono rimossi e il messaggio di posta elettronica memorizzato nella cache del dispositivo viene eliminato.|Rimuove le applicazioni di posta elettronica abilitate per EFS, tra cui i messaggi e gli allegati dell'applicazione Windows Mail. Rimuove gli account di posta elettronica di cui Intune ha effettuato il provisioning.|
|Separazione di Azure Active Directory (AAD)|No|No|Record AAD rimosso|Non applicabile. Windows 10 non supporta la cancellazione selettiva per dispositivi appartenenti ad Azure Active Directory|

### Cancellare un dispositivo in modalità remota dalla console di amministrazione di Intune

1.  Selezionare i dispositivi da cancellare. Possono essere cercati per utente o per dispositivo.

    -   **Utente:**

        1.  Nella [console di amministrazione di Intune](https://manage.microsoft.com/) scegliere **Gruppi**&gt;**Tutti gli utenti**

        2.  Scegliere il nome dell'utente il cui dispositivo mobile deve essere cancellato. Scegliere **Visualizza proprietà**

        3.  Nella pagina **Proprietà** relativa all'utente scegliere **Dispositivi**, quindi il nome del dispositivo mobile di cui cancellare i dati. Usare CTRL+clic per selezionare più dispositivi.

    -   **Dispositivo:**

        1.  Nella [console di amministrazione di Intune](https://manage.microsoft.com/) scegliere **Gruppi**&gt;**Tutti i dispositivi mobili**

      ![Avvio di un'operazione di ritiro o di cancellazione](../media/dev-sa-wipe.png)

        2.  Scegliere **Dispositivi**, quindi il nome del dispositivo mobile di cui cancellare i dati. Usare CTRL+clic per selezionare più dispositivi.

2.  Scegliere **Disattiva/Cancella**.

3.  Verrà visualizzato un messaggio in cui si richiede di confermare il ritiro del dispositivo.

    -   Per eseguire una **cancellazione selettiva** che rimuove solo le app e i dati aziendali, scegliere **Sì**.

    -   Per eseguire una **cancellazione completa** che cancella tutte le app e i dati e ripristina le impostazioni predefinite del dispositivo, selezionare **Cancellazione del dispositivo prima della disattivazione**. Questa azione si applica a tutte le piattaforme tranne Windows 8.1. **Non è possibile ripristinare i dati rimossi con una cancellazione completa**.

Sono necessari meno di 15 minuti per propagare la cancellazione in tutti i tipi di dispositivo.

## Cancellare contenuti abilitati per Encryption File System (EFS)
La cancellazione selettiva dei contenuti crittografati con EFS è supportata da Windows 8.1 e Windows RT 8.1. Quanto descritto di seguito si applica alla cancellazione selettiva di contenuti abilitati EFS:

-   Solo le app e i dati protetti da EFS che usano lo stesso dominio Internet come account di Intune vengono cancellati in modo selettivo. Per altre informazioni, vedere l'argomento relativo alla [cancellazione selettiva di Windows per la gestione dei dati dei dispositivi](http://technet.microsoft.com/library/dn486874.aspx).

-   In caso di modifiche al dominio associato con EFS, potranno essere necessarie fino a 48 ore prima che le app e i dati che usano il nuovo dominio siano cancellati in modo selettivo.

-   Ogni dominio registrato con Intune verrà cancellato.

I dati e le app che sono attualmente supportati dalla cancellazione selettiva EFS sono:

-   App di posta elettronica per Windows

-   Cartelle di lavoro

-   File e cartelle crittografate con EFS. Per altre informazioni, vedere le [procedure consigliate per la crittografia del file system](http://support.microsoft.com/kb/223316).

-   Se gestisce la propria identità in Active Directory, l'organizzazione deve usare lo strumento di sincronizzazione directory (DirSync) per sincronizzare le informazioni in AAD garantendo il corretto funzionamento della cancellazione selettiva EFS.  Per altre informazioni, vedere [Scenario di sincronizzazione della directory](http://technet.microsoft.com/library/dn441212.aspx) nella documentazione di Azure Active Directory.

## Monitorare le azioni di disattivazione, cancellazione ed eliminazione
Per ottenere un report dei dispositivi che sono stati disattivati, cancellati o eliminati e di chi ha eseguito l'azione:

1.  Nella [console di amministrazione di Intune](https://manage.microsoft.com/) scegliere **Report**&gt;**Report cronologia dispositivo**

2.  Specificare una data di inizio e una data di fine per il report, quindi scegliere **Visualizza report**


### Vedere anche
[Retire devices (Ritirare i dispositivi)](retire-devices-from-microsoft-intune-management.md)

[Windows Selective Wipe for Device Data Management (Cancellazione selettiva Windows per la gestione dei dati dei dispositivi)](http://technet.microsoft.com/library/dn486874.aspx)


<!--HONumber=May16_HO4-->


