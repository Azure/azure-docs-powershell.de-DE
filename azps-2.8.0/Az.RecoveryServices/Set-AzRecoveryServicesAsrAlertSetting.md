---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/set-azrecoveryservicesasralertsetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Set-AzRecoveryServicesAsrAlertSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Set-AzRecoveryServicesAsrAlertSetting.md
ms.openlocfilehash: 21106b2c5a8e36f58b6593049fccf28994b0af46
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93824248"
---
# <span data-ttu-id="6d846-101">Set-AzRecoveryServicesAsrAlertSetting</span><span class="sxs-lookup"><span data-stu-id="6d846-101">Set-AzRecoveryServicesAsrAlertSetting</span></span>

## <span data-ttu-id="6d846-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="6d846-102">SYNOPSIS</span></span>
<span data-ttu-id="6d846-103">Konfigurieren Sie die Einstellungen für die Azure Site Recovery-Benachrichtigung (e-Mail-Benachrichtigung) für den Tresor.</span><span class="sxs-lookup"><span data-stu-id="6d846-103">Configure Azure Site Recovery notification settings (email notification) for the vault.</span></span>

## <span data-ttu-id="6d846-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="6d846-104">SYNTAX</span></span>

### <span data-ttu-id="6d846-105">Festlegen (Standard)</span><span class="sxs-lookup"><span data-stu-id="6d846-105">Set (Default)</span></span>
```
Set-AzRecoveryServicesAsrAlertSetting [-CustomEmailAddress <String[]>] [-LocaleID <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6d846-106">EmailToSubscriptionOwner</span><span class="sxs-lookup"><span data-stu-id="6d846-106">EmailToSubscriptionOwner</span></span>
```
Set-AzRecoveryServicesAsrAlertSetting [-EnableEmailSubscriptionOwner] [-CustomEmailAddress <String[]>]
 [-LocaleID <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6d846-107">DisableEmailToSubcriptionOwner</span><span class="sxs-lookup"><span data-stu-id="6d846-107">DisableEmailToSubcriptionOwner</span></span>
```
Set-AzRecoveryServicesAsrAlertSetting [-DisableEmailToSubscriptionOwner] [-CustomEmailAddress <String[]>]
 [-LocaleID <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6d846-108">Deaktivieren</span><span class="sxs-lookup"><span data-stu-id="6d846-108">Disable</span></span>
```
Set-AzRecoveryServicesAsrAlertSetting [-DisableNotification] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6d846-109">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="6d846-109">DESCRIPTION</span></span>
<span data-ttu-id="6d846-110">Das Cmdlet " **Satz-AzRecoveryServicesAsrNotificationSetting** " konfiguriert Azure Site Recovery Notification-Einstellungen (e-Mail-Benachrichtigung) für den Tresor.</span><span class="sxs-lookup"><span data-stu-id="6d846-110">The **Set-AzRecoveryServicesAsrNotificationSetting** cmdlet configures Azure Site Recovery notification settings (email notification) for the vault.</span></span>

## <span data-ttu-id="6d846-111">Beispiele</span><span class="sxs-lookup"><span data-stu-id="6d846-111">EXAMPLES</span></span>

### <span data-ttu-id="6d846-112">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="6d846-112">Example 1</span></span>
```
PS C:\> Set-AzRecoveryServicesAsrAlertSetting -DisableNotification

CustomEmailAddress EmailSubscriptionOwner Locale
------------------ ---------------------- ------
{}                 Off                    en-US
```

<span data-ttu-id="6d846-113">Benachrichtigung deaktivieren.</span><span class="sxs-lookup"><span data-stu-id="6d846-113">Disable notification.</span></span>

### <span data-ttu-id="6d846-114">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="6d846-114">Example 2</span></span>
```
PS C:\> Set-AzRecoveryServicesAsrAlertSetting -CustomEmailAddress "abcxxxx@xxxx.com" -EnableEmailSubscriptionOwner

CustomEmailAddress     EmailSubscriptionOwner Locale
------------------     ---------------------- ------
{abcxxxx@xxxx.com} On                     en-US
```

<span data-ttu-id="6d846-115">Benachrichtigung für benutzerdefinierte e-Mail-Adressen und Abonnementbesitzer einrichten</span><span class="sxs-lookup"><span data-stu-id="6d846-115">Set notification for custom email address(s) and for subscription owner.</span></span>

## <span data-ttu-id="6d846-116">Parameter</span><span class="sxs-lookup"><span data-stu-id="6d846-116">PARAMETERS</span></span>

### <span data-ttu-id="6d846-117">-CustomEmailAddress</span><span class="sxs-lookup"><span data-stu-id="6d846-117">-CustomEmailAddress</span></span>
<span data-ttu-id="6d846-118">Benachrichtigung an e-Mails.</span><span class="sxs-lookup"><span data-stu-id="6d846-118">Alert / Notification sent to emails.</span></span>

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

### <span data-ttu-id="6d846-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6d846-119">-DefaultProfile</span></span>
<span data-ttu-id="6d846-120">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="6d846-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="6d846-121">-DisableEmailToSubscriptionOwner</span><span class="sxs-lookup"><span data-stu-id="6d846-121">-DisableEmailToSubscriptionOwner</span></span>
<span data-ttu-id="6d846-122">Switch-Parameter gibt an, dass Benachrichtigung an den Abonnementbesitzer aktiviert werden soll.</span><span class="sxs-lookup"><span data-stu-id="6d846-122">Switch parameter specifies enable notification to subscription owner.</span></span>

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

### <span data-ttu-id="6d846-123">-DisableNotification</span><span class="sxs-lookup"><span data-stu-id="6d846-123">-DisableNotification</span></span>
<span data-ttu-id="6d846-124">Flag, um alle Benachrichtigungen zu deaktivieren.</span><span class="sxs-lookup"><span data-stu-id="6d846-124">Flag to disable all notification.</span></span>

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

### <span data-ttu-id="6d846-125">-EnableEmailSubscriptionOwner</span><span class="sxs-lookup"><span data-stu-id="6d846-125">-EnableEmailSubscriptionOwner</span></span>
<span data-ttu-id="6d846-126">Switch-Parameter gibt an, dass Benachrichtigung an den Abonnementbesitzer aktiviert werden soll.</span><span class="sxs-lookup"><span data-stu-id="6d846-126">Switch parameter specifies enable notification to subscription owner.</span></span>

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

### <span data-ttu-id="6d846-127">-Gebietsschema-Nr</span><span class="sxs-lookup"><span data-stu-id="6d846-127">-LocaleID</span></span>
<span data-ttu-id="6d846-128">E-Mail-Sprache der Benachrichtigungs-Versicherungen an Benutzer (unterstützte Kulturcodes von Microsoft).</span><span class="sxs-lookup"><span data-stu-id="6d846-128">Email language of alert /notification to user(supported culture codes from microsoft).</span></span> 

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

### <span data-ttu-id="6d846-129">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="6d846-129">-Confirm</span></span>
<span data-ttu-id="6d846-130">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="6d846-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6d846-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6d846-131">-WhatIf</span></span>
<span data-ttu-id="6d846-132">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="6d846-132">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="6d846-133">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="6d846-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6d846-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6d846-134">CommonParameters</span></span>
<span data-ttu-id="6d846-135">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6d846-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6d846-136">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6d846-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6d846-137">Eingaben</span><span class="sxs-lookup"><span data-stu-id="6d846-137">INPUTS</span></span>

### <span data-ttu-id="6d846-138">Keine</span><span class="sxs-lookup"><span data-stu-id="6d846-138">None</span></span>

## <span data-ttu-id="6d846-139">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="6d846-139">OUTPUTS</span></span>

### <span data-ttu-id="6d846-140">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRAlertSetting</span><span class="sxs-lookup"><span data-stu-id="6d846-140">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRAlertSetting</span></span>

## <span data-ttu-id="6d846-141">Notizen</span><span class="sxs-lookup"><span data-stu-id="6d846-141">NOTES</span></span>

## <span data-ttu-id="6d846-142">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="6d846-142">RELATED LINKS</span></span>
