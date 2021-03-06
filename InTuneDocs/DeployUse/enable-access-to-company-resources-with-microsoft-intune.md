---
# required metadata

title: Abilitare l'accesso alle risorse aziendali | Microsoft Intune
description:
keywords:
author: Nbigman
manager: jeffgilb
ms.date: 04/28/2016
ms.topic: article
ms.prod:
ms.service: microsoft-intune
ms.technology:
ms.assetid: 3dd8dd4e-e165-4d0c-97b7-b3e86ebab909

# optional metadata

#ROBOTS:
#audience:
#ms.devlang:
ms.reviewer: jeffgilb
ms.suite: ems
#ms.tgt_pltfrm:
#ms.custom:

---

# Abilitare l'accesso alle risorse aziendali con Microsoft Intune
I profili Microsoft Intune Wi-Fi, VPN e di posta elettronica interagiscono per consentire agli utenti di accedere ai file e alle risorse necessari per svolgere le proprie attività, ovunque si trovino. I profili di certificati consentono di proteggere tale accesso.

## [Profili Wi-Fi](wi-fi-connections-in-microsoft-intune.md) e piattaforme supportate

Distribuire le impostazioni di rete wireless agli utenti. La distribuzione di queste impostazioni consente di ridurre al minimo le operazioni che l'utente finale deve eseguire per connettersi alla rete aziendale.
#### Piattaforme supportate

|Windows 8.1 e versioni successive|Windows Phone 8.1 e versioni successive|iOS|Android|Samsung KNOX|
|---------------------|---------------------------|---|-------|------------|
|Sì (è possibile importare un profilo Wi-Fi Windows)|Sì (è possibile configurare un URI OMA) |sì|Sì|sì|

## [Profili VPN](vpn-connections-in-microsoft-intune.md) e piattaforme supportate
Distribuire le impostazioni di rete privata virtuale (VPN) per gli utenti. La distribuzione di queste impostazioni consente di ridurre al minimo le operazioni che l'utente finale deve eseguire per connettersi alle risorse nella rete aziendale.

|Windows 8.1 e versioni successive|Windows Phone 8.1 e versioni successive|iOS|Android|Samsung KNOX|
|---------------------|---------------------------|---|-------|------------|
|Sì|Sì|Sì|Sì|Sì|

## [Profili di posta elettronica](configure-access-to-corporate-email-using-email-profiles-with-microsoft-intune.md) e piattaforme supportate
È possibile creare, distribuire e monitorare le impostazioni native di posta elettronica nei dispositivi aziendali.

|Windows 8.1 e versioni successive|Windows Phone 8.1 e versioni successive|iOS|Android|Samsung KNOX|
|---------------------|---------------------------|---|-------|------------|
|No|Sì|Sì|No|Sì|
> [!NOTE]
> [Questo post di blog del team di Intune](http://blogs.technet.com/b/microsoftintune/archive/2015/02/23/using-oma-uri-to-create-custom-wi-fi-profiles-for-windows-phone-8-1.aspx) offre informazioni su come configurare un profilo Wi-Fi Windows Phone 8.1 usando un URI OMA.

## [Profili di certificati](secure-resource-access-with-certificate-profiles.md) e piattaforme supportate
Consentono di proteggere l'accesso alle risorse aziendali tra cui reti wireless e le connessioni VPN.

|Windows 8.1 e versioni successive|Windows Phone 8.1 e versioni successive|iOS|Android|Samsung KNOX|
|---------------------|---------------------------|---|-------|------------|
|sì|Sì|Sì|Sì|Sì|


<!--HONumber=May16_HO1-->


