---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/set-azrecoveryservicesasralertsetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Set-AzRecoveryServicesAsrAlertSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Set-AzRecoveryServicesAsrAlertSetting.md
ms.openlocfilehash: ca17774085e76adad57698c2b0b5689ec1c276e2
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93659825"
---
# <span data-ttu-id="9cdf1-101">Set-AzRecoveryServicesAsrAlertSetting</span><span class="sxs-lookup"><span data-stu-id="9cdf1-101">Set-AzRecoveryServicesAsrAlertSetting</span></span>

## <span data-ttu-id="9cdf1-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="9cdf1-102">SYNOPSIS</span></span>
<span data-ttu-id="9cdf1-103">Konfigurieren Sie die Einstellungen für die Azure Site Recovery-Benachrichtigung (e-Mail-Benachrichtigung) für den Tresor.</span><span class="sxs-lookup"><span data-stu-id="9cdf1-103">Configure Azure Site Recovery notification settings (email notification) for the vault.</span></span>

## <span data-ttu-id="9cdf1-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="9cdf1-104">SYNTAX</span></span>

### <span data-ttu-id="9cdf1-105">Festlegen (Standard)</span><span class="sxs-lookup"><span data-stu-id="9cdf1-105">Set (Default)</span></span>
```
Set-AzRecoveryServicesAsrAlertSetting [-CustomEmailAddress <String[]>] [-LocaleID <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9cdf1-106">EmailToSubscriptionOwner</span><span class="sxs-lookup"><span data-stu-id="9cdf1-106">EmailToSubscriptionOwner</span></span>
```
Set-AzRecoveryServicesAsrAlertSetting [-EnableEmailSubscriptionOwner] [-CustomEmailAddress <String[]>]
 [-LocaleID <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9cdf1-107">DisableEmailToSubcriptionOwner</span><span class="sxs-lookup"><span data-stu-id="9cdf1-107">DisableEmailToSubcriptionOwner</span></span>
```
Set-AzRecoveryServicesAsrAlertSetting [-DisableEmailToSubscriptionOwner] [-CustomEmailAddress <String[]>]
 [-LocaleID <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9cdf1-108">Deaktivieren</span><span class="sxs-lookup"><span data-stu-id="9cdf1-108">Disable</span></span>
```
Set-AzRecoveryServicesAsrAlertSetting [-DisableNotification] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9cdf1-109">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="9cdf1-109">DESCRIPTION</span></span>
<span data-ttu-id="9cdf1-110">Das Cmdlet " **Satz-AzRecoveryServicesAsrNotificationSetting** " konfiguriert Azure Site Recovery Notification-Einstellungen (e-Mail-Benachrichtigung) für den Tresor.</span><span class="sxs-lookup"><span data-stu-id="9cdf1-110">The **Set-AzRecoveryServicesAsrNotificationSetting** cmdlet configures Azure Site Recovery notification settings (email notification) for the vault.</span></span>

## <span data-ttu-id="9cdf1-111">Beispiele</span><span class="sxs-lookup"><span data-stu-id="9cdf1-111">EXAMPLES</span></span>

### <span data-ttu-id="9cdf1-112">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="9cdf1-112">Example 1</span></span>
```
PS C:\> Set-AzRecoveryServicesAsrAlertSetting -DisableNotification

CustomEmailAddress EmailSubscriptionOwner Locale
------------------ ---------------------- ------
{}                 Off                    en-US
```

<span data-ttu-id="9cdf1-113">Benachrichtigung deaktivieren.</span><span class="sxs-lookup"><span data-stu-id="9cdf1-113">Disable notification.</span></span>

### <span data-ttu-id="9cdf1-114">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="9cdf1-114">Example 2</span></span>
```
PS C:\> Set-AzRecoveryServicesAsrAlertSetting -CustomEmailAddress "abcxxxx@xxxx.com" -EmailSubscriptionOwner

CustomEmailAddress     EmailSubscriptionOwner Locale
------------------     ---------------------- ------
{abcxxxx@xxxx.com} On                     en-US
```

<span data-ttu-id="9cdf1-115">Benachrichtigung für benutzerdefinierte e-Mail-Adressen und Abonnementbesitzer einrichten</span><span class="sxs-lookup"><span data-stu-id="9cdf1-115">Set notification for custom email address(s) and for subscription owner.</span></span>

## <span data-ttu-id="9cdf1-116">Parameter</span><span class="sxs-lookup"><span data-stu-id="9cdf1-116">PARAMETERS</span></span>

### <span data-ttu-id="9cdf1-117">-CustomEmailAddress</span><span class="sxs-lookup"><span data-stu-id="9cdf1-117">-CustomEmailAddress</span></span>
<span data-ttu-id="9cdf1-118">Benachrichtigung an e-Mails.</span><span class="sxs-lookup"><span data-stu-id="9cdf1-118">Alert / Notification sent to emails.</span></span>

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

### <span data-ttu-id="9cdf1-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9cdf1-119">-DefaultProfile</span></span>
<span data-ttu-id="9cdf1-120">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="9cdf1-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9cdf1-121">-DisableEmailToSubscriptionOwner</span><span class="sxs-lookup"><span data-stu-id="9cdf1-121">-DisableEmailToSubscriptionOwner</span></span>
<span data-ttu-id="9cdf1-122">Switch-Parameter gibt an, dass Benachrichtigung an den Abonnementbesitzer aktiviert werden soll.</span><span class="sxs-lookup"><span data-stu-id="9cdf1-122">Switch parameter specifies enable notification to subscription owner.</span></span>

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

### <span data-ttu-id="9cdf1-123">-DisableNotification</span><span class="sxs-lookup"><span data-stu-id="9cdf1-123">-DisableNotification</span></span>
<span data-ttu-id="9cdf1-124">Flag, um alle Benachrichtigungen zu deaktivieren.</span><span class="sxs-lookup"><span data-stu-id="9cdf1-124">Flag to disable all notification.</span></span>

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

### <span data-ttu-id="9cdf1-125">-EnableEmailSubscriptionOwner</span><span class="sxs-lookup"><span data-stu-id="9cdf1-125">-EnableEmailSubscriptionOwner</span></span>
<span data-ttu-id="9cdf1-126">Switch Parameter gibt an, dass Benachrichtigung an den Abonnementbesitzer aktiviert werden soll.</span><span class="sxs-lookup"><span data-stu-id="9cdf1-126">Switch paramter specifies enable notification to subscription owner.</span></span>

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

### <span data-ttu-id="9cdf1-127">-Gebietsschema-Nr</span><span class="sxs-lookup"><span data-stu-id="9cdf1-127">-LocaleID</span></span>
<span data-ttu-id="9cdf1-128">E-Mail-Sprache der Benachrichtigungs-/notifcation an Benutzer (unterstützte Kulturcodes von Microsoft).</span><span class="sxs-lookup"><span data-stu-id="9cdf1-128">Email language of alert /notifcation to user(supported culture codes from microsoft).</span></span> 

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

### <span data-ttu-id="9cdf1-129">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="9cdf1-129">-Confirm</span></span>
<span data-ttu-id="9cdf1-130">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="9cdf1-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9cdf1-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9cdf1-131">-WhatIf</span></span>
<span data-ttu-id="9cdf1-132">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="9cdf1-132">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="9cdf1-133">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="9cdf1-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9cdf1-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9cdf1-134">CommonParameters</span></span>
<span data-ttu-id="9cdf1-135">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9cdf1-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9cdf1-136">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9cdf1-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9cdf1-137">Eingaben</span><span class="sxs-lookup"><span data-stu-id="9cdf1-137">INPUTS</span></span>

### <span data-ttu-id="9cdf1-138">Keine</span><span class="sxs-lookup"><span data-stu-id="9cdf1-138">None</span></span>

## <span data-ttu-id="9cdf1-139">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="9cdf1-139">OUTPUTS</span></span>

### <span data-ttu-id="9cdf1-140">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRAlertSetting</span><span class="sxs-lookup"><span data-stu-id="9cdf1-140">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRAlertSetting</span></span>

## <span data-ttu-id="9cdf1-141">Notizen</span><span class="sxs-lookup"><span data-stu-id="9cdf1-141">NOTES</span></span>

## <span data-ttu-id="9cdf1-142">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="9cdf1-142">RELATED LINKS</span></span>
