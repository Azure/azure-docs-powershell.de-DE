---
external help file: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: AzureRM.RecoveryServices.SiteRecovery
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.recoveryservices.siterecovery/set-azurermrecoveryservicesasralertsetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices.SiteRecovery/help/Set-AzureRmRecoveryServicesAsrAlertSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices.SiteRecovery/help/Set-AzureRmRecoveryServicesAsrAlertSetting.md
ms.openlocfilehash: 70816649b33cd91c7d378b3588b443e4dd5b8fe9
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93495750"
---
# <span data-ttu-id="d77ac-101">Set-AzureRmRecoveryServicesAsrAlertSetting</span><span class="sxs-lookup"><span data-stu-id="d77ac-101">Set-AzureRmRecoveryServicesAsrAlertSetting</span></span>

## <span data-ttu-id="d77ac-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="d77ac-102">SYNOPSIS</span></span>
<span data-ttu-id="d77ac-103">Konfigurieren Sie die Einstellungen für die Azure Site Recovery-Benachrichtigung (e-Mail-Benachrichtigung) für den Tresor.</span><span class="sxs-lookup"><span data-stu-id="d77ac-103">Configure Azure Site Recovery notification settings (email notification) for the vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d77ac-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="d77ac-104">SYNTAX</span></span>

### <span data-ttu-id="d77ac-105">Festlegen (Standard)</span><span class="sxs-lookup"><span data-stu-id="d77ac-105">Set (Default)</span></span>
```
Set-AzureRmRecoveryServicesAsrAlertSetting [-CustomEmailAddress <String[]>] [-LocaleID <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d77ac-106">EmailToSubscriptionOwner</span><span class="sxs-lookup"><span data-stu-id="d77ac-106">EmailToSubscriptionOwner</span></span>
```
Set-AzureRmRecoveryServicesAsrAlertSetting [-EnableEmailSubscriptionOwner] [-CustomEmailAddress <String[]>]
 [-LocaleID <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d77ac-107">DisableEmailToSubcriptionOwner</span><span class="sxs-lookup"><span data-stu-id="d77ac-107">DisableEmailToSubcriptionOwner</span></span>
```
Set-AzureRmRecoveryServicesAsrAlertSetting [-DisableEmailToSubscriptionOwner] [-CustomEmailAddress <String[]>]
 [-LocaleID <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d77ac-108">Deaktivieren</span><span class="sxs-lookup"><span data-stu-id="d77ac-108">Disable</span></span>
```
Set-AzureRmRecoveryServicesAsrAlertSetting [-DisableNotification] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d77ac-109">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="d77ac-109">DESCRIPTION</span></span>
<span data-ttu-id="d77ac-110">Das Cmdlet " **Satz-AzureRmRecoveryServicesAsrNotificationSetting** " konfiguriert Azure Site Recovery Notification-Einstellungen (e-Mail-Benachrichtigung) für den Tresor.</span><span class="sxs-lookup"><span data-stu-id="d77ac-110">The **Set-AzureRmRecoveryServicesAsrNotificationSetting** cmdlet configures Azure Site Recovery notification settings (email notification) for the vault.</span></span>

## <span data-ttu-id="d77ac-111">Beispiele</span><span class="sxs-lookup"><span data-stu-id="d77ac-111">EXAMPLES</span></span>

### <span data-ttu-id="d77ac-112">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="d77ac-112">Example 1</span></span>
```
PS C:\> Set-AzureRmRecoveryServicesAsrAlertSetting -DisableNotification

CustomEmailAddress EmailSubscriptionOwner Locale
------------------ ---------------------- ------
{}                 Off                    en-US
```

<span data-ttu-id="d77ac-113">Benachrichtigung deaktivieren.</span><span class="sxs-lookup"><span data-stu-id="d77ac-113">Disable notification.</span></span>

### <span data-ttu-id="d77ac-114">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="d77ac-114">Example 2</span></span>
```
PS C:\> Set-AzureRmRecoveryServicesAsrAlertSetting -CustomEmailAddress "abcxxxx@xxxx.com" -EmailSubscriptionOwner

CustomEmailAddress     EmailSubscriptionOwner Locale
------------------     ---------------------- ------
{abcxxxx@xxxx.com} On                     en-US
```

<span data-ttu-id="d77ac-115">Benachrichtigung für benutzerdefinierte e-Mail-Adressen und Abonnementbesitzer einrichten</span><span class="sxs-lookup"><span data-stu-id="d77ac-115">Set notification for custom email address(s) and for subscription owner.</span></span>

## <span data-ttu-id="d77ac-116">Parameter</span><span class="sxs-lookup"><span data-stu-id="d77ac-116">PARAMETERS</span></span>

### <span data-ttu-id="d77ac-117">-CustomEmailAddress</span><span class="sxs-lookup"><span data-stu-id="d77ac-117">-CustomEmailAddress</span></span>
<span data-ttu-id="d77ac-118">Benachrichtigung an e-Mails.</span><span class="sxs-lookup"><span data-stu-id="d77ac-118">Alert / Notification sent to emails.</span></span>

```yaml
Type: System.String[]
Parameter Sets: Set, EmailToSubscriptionOwner, DisableEmailToSubcriptionOwner
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d77ac-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d77ac-119">-DefaultProfile</span></span>
<span data-ttu-id="d77ac-120">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="d77ac-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d77ac-121">-DisableEmailToSubscriptionOwner</span><span class="sxs-lookup"><span data-stu-id="d77ac-121">-DisableEmailToSubscriptionOwner</span></span>
<span data-ttu-id="d77ac-122">Switch-Parameter gibt an, dass Benachrichtigung an den Abonnementbesitzer aktiviert werden soll.</span><span class="sxs-lookup"><span data-stu-id="d77ac-122">Switch parameter specifies enable notification to subscription owner.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: DisableEmailToSubcriptionOwner
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d77ac-123">-DisableNotification</span><span class="sxs-lookup"><span data-stu-id="d77ac-123">-DisableNotification</span></span>
<span data-ttu-id="d77ac-124">Flag, um alle Benachrichtigungen zu deaktivieren.</span><span class="sxs-lookup"><span data-stu-id="d77ac-124">Flag to disable all notification.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: Disable
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d77ac-125">-EnableEmailSubscriptionOwner</span><span class="sxs-lookup"><span data-stu-id="d77ac-125">-EnableEmailSubscriptionOwner</span></span>
<span data-ttu-id="d77ac-126">Switch Parameter gibt an, dass Benachrichtigung an den Abonnementbesitzer aktiviert werden soll.</span><span class="sxs-lookup"><span data-stu-id="d77ac-126">Switch paramter specifies enable notification to subscription owner.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: EmailToSubscriptionOwner
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d77ac-127">-Gebietsschema-Nr</span><span class="sxs-lookup"><span data-stu-id="d77ac-127">-LocaleID</span></span>
<span data-ttu-id="d77ac-128">E-Mail-Sprache der Benachrichtigungs-/notifcation an Benutzer (unterstützte Kulturcodes von Microsoft).</span><span class="sxs-lookup"><span data-stu-id="d77ac-128">Email language of alert /notifcation to user(supported culture codes from microsoft).</span></span> 

```yaml
Type: System.String
Parameter Sets: Set, EmailToSubscriptionOwner, DisableEmailToSubcriptionOwner
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d77ac-129">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="d77ac-129">-Confirm</span></span>
<span data-ttu-id="d77ac-130">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="d77ac-130">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d77ac-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d77ac-131">-WhatIf</span></span>
<span data-ttu-id="d77ac-132">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="d77ac-132">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="d77ac-133">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="d77ac-133">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d77ac-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d77ac-134">CommonParameters</span></span>
<span data-ttu-id="d77ac-135">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d77ac-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d77ac-136">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d77ac-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d77ac-137">Eingaben</span><span class="sxs-lookup"><span data-stu-id="d77ac-137">INPUTS</span></span>

### <span data-ttu-id="d77ac-138">Keine</span><span class="sxs-lookup"><span data-stu-id="d77ac-138">None</span></span>

## <span data-ttu-id="d77ac-139">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="d77ac-139">OUTPUTS</span></span>

### <span data-ttu-id="d77ac-140">System. Collections. Generic. IEnumerable ' 1 [[Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRAlertSetting, Microsoft. Azure. Commands. RecoveryServices. SiteRecovery, Version = 0.1.1.0, Culture = neutral, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="d77ac-140">System.Collections.Generic.IEnumerable\`1[[Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRAlertSetting, Microsoft.Azure.Commands.RecoveryServices.SiteRecovery, Version=0.1.1.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="d77ac-141">Notizen</span><span class="sxs-lookup"><span data-stu-id="d77ac-141">NOTES</span></span>

## <span data-ttu-id="d77ac-142">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="d77ac-142">RELATED LINKS</span></span>
