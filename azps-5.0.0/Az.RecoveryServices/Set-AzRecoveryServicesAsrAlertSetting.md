---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/set-azrecoveryservicesasralertsetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Set-AzRecoveryServicesAsrAlertSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Set-AzRecoveryServicesAsrAlertSetting.md
ms.openlocfilehash: c7821ddfd07b17a77c482a770b28672ccd664cb4
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94178425"
---
# <span data-ttu-id="36fd5-101">Set-AzRecoveryServicesAsrAlertSetting</span><span class="sxs-lookup"><span data-stu-id="36fd5-101">Set-AzRecoveryServicesAsrAlertSetting</span></span>

## <span data-ttu-id="36fd5-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="36fd5-102">SYNOPSIS</span></span>
<span data-ttu-id="36fd5-103">Konfigurieren Sie die Einstellungen für die Azure Site Recovery-Benachrichtigung (e-Mail-Benachrichtigung) für den Tresor.</span><span class="sxs-lookup"><span data-stu-id="36fd5-103">Configure Azure Site Recovery notification settings (email notification) for the vault.</span></span>

## <span data-ttu-id="36fd5-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="36fd5-104">SYNTAX</span></span>

### <span data-ttu-id="36fd5-105">Festlegen (Standard)</span><span class="sxs-lookup"><span data-stu-id="36fd5-105">Set (Default)</span></span>
```
Set-AzRecoveryServicesAsrAlertSetting [-CustomEmailAddress <String[]>] [-LocaleID <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="36fd5-106">EmailToSubscriptionOwner</span><span class="sxs-lookup"><span data-stu-id="36fd5-106">EmailToSubscriptionOwner</span></span>
```
Set-AzRecoveryServicesAsrAlertSetting [-EnableEmailSubscriptionOwner] [-CustomEmailAddress <String[]>]
 [-LocaleID <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="36fd5-107">DisableEmailToSubcriptionOwner</span><span class="sxs-lookup"><span data-stu-id="36fd5-107">DisableEmailToSubcriptionOwner</span></span>
```
Set-AzRecoveryServicesAsrAlertSetting [-DisableEmailToSubscriptionOwner] [-CustomEmailAddress <String[]>]
 [-LocaleID <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="36fd5-108">Deaktivieren</span><span class="sxs-lookup"><span data-stu-id="36fd5-108">Disable</span></span>
```
Set-AzRecoveryServicesAsrAlertSetting [-DisableNotification] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="36fd5-109">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="36fd5-109">DESCRIPTION</span></span>
<span data-ttu-id="36fd5-110">Das Cmdlet " **Satz-AzRecoveryServicesAsrNotificationSetting** " konfiguriert Azure Site Recovery Notification-Einstellungen (e-Mail-Benachrichtigung) für den Tresor.</span><span class="sxs-lookup"><span data-stu-id="36fd5-110">The **Set-AzRecoveryServicesAsrNotificationSetting** cmdlet configures Azure Site Recovery notification settings (email notification) for the vault.</span></span>

## <span data-ttu-id="36fd5-111">Beispiele</span><span class="sxs-lookup"><span data-stu-id="36fd5-111">EXAMPLES</span></span>

### <span data-ttu-id="36fd5-112">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="36fd5-112">Example 1</span></span>
```powershell
PS C:\> Set-AzRecoveryServicesAsrAlertSetting -DisableNotification

CustomEmailAddress EmailSubscriptionOwner Locale
------------------ ---------------------- ------
{}                 Off                    en-US
```

<span data-ttu-id="36fd5-113">Benachrichtigung deaktivieren.</span><span class="sxs-lookup"><span data-stu-id="36fd5-113">Disable notification.</span></span>

### <span data-ttu-id="36fd5-114">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="36fd5-114">Example 2</span></span>
```powershell
PS C:\> Set-AzRecoveryServicesAsrAlertSetting -CustomEmailAddress "abcxxxx@xxxx.com" -EnableEmailSubscriptionOwner

CustomEmailAddress     EmailSubscriptionOwner Locale
------------------     ---------------------- ------
{abcxxxx@xxxx.com} On                     en-US
```

<span data-ttu-id="36fd5-115">Benachrichtigung für benutzerdefinierte e-Mail-Adressen und Abonnementbesitzer einrichten</span><span class="sxs-lookup"><span data-stu-id="36fd5-115">Set notification for custom email address(s) and for subscription owner.</span></span>

### <span data-ttu-id="36fd5-116">Beispiel 3</span><span class="sxs-lookup"><span data-stu-id="36fd5-116">Example 3</span></span>

<span data-ttu-id="36fd5-117">Konfigurieren Sie die Einstellungen für die Azure Site Recovery-Benachrichtigung (e-Mail-Benachrichtigung) für den Tresor.</span><span class="sxs-lookup"><span data-stu-id="36fd5-117">Configure Azure Site Recovery notification settings (email notification) for the vault.</span></span> <span data-ttu-id="36fd5-118">automatisch</span><span class="sxs-lookup"><span data-stu-id="36fd5-118">(autogenerated)</span></span>

```powershell <!-- Aladdin Generated Example --> 
Set-AzRecoveryServicesAsrAlertSetting -CustomEmailAddress 'abcxxxx@xxxx.com' -DisableEmailToSubscriptionOwner
```

## <span data-ttu-id="36fd5-119">Parameter</span><span class="sxs-lookup"><span data-stu-id="36fd5-119">PARAMETERS</span></span>

### <span data-ttu-id="36fd5-120">-CustomEmailAddress</span><span class="sxs-lookup"><span data-stu-id="36fd5-120">-CustomEmailAddress</span></span>
<span data-ttu-id="36fd5-121">Benachrichtigung an e-Mails.</span><span class="sxs-lookup"><span data-stu-id="36fd5-121">Alert / Notification sent to emails.</span></span>

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

### <span data-ttu-id="36fd5-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="36fd5-122">-DefaultProfile</span></span>
<span data-ttu-id="36fd5-123">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="36fd5-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="36fd5-124">-DisableEmailToSubscriptionOwner</span><span class="sxs-lookup"><span data-stu-id="36fd5-124">-DisableEmailToSubscriptionOwner</span></span>
<span data-ttu-id="36fd5-125">Switch-Parameter gibt an, dass Benachrichtigung an den Abonnementbesitzer aktiviert werden soll.</span><span class="sxs-lookup"><span data-stu-id="36fd5-125">Switch parameter specifies enable notification to subscription owner.</span></span>

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

### <span data-ttu-id="36fd5-126">-DisableNotification</span><span class="sxs-lookup"><span data-stu-id="36fd5-126">-DisableNotification</span></span>
<span data-ttu-id="36fd5-127">Flag, um alle Benachrichtigungen zu deaktivieren.</span><span class="sxs-lookup"><span data-stu-id="36fd5-127">Flag to disable all notification.</span></span>

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

### <span data-ttu-id="36fd5-128">-EnableEmailSubscriptionOwner</span><span class="sxs-lookup"><span data-stu-id="36fd5-128">-EnableEmailSubscriptionOwner</span></span>
<span data-ttu-id="36fd5-129">Switch-Parameter gibt an, dass Benachrichtigung an den Abonnementbesitzer aktiviert werden soll.</span><span class="sxs-lookup"><span data-stu-id="36fd5-129">Switch parameter specifies enable notification to subscription owner.</span></span>

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

### <span data-ttu-id="36fd5-130">-Gebietsschema-Nr</span><span class="sxs-lookup"><span data-stu-id="36fd5-130">-LocaleID</span></span>
<span data-ttu-id="36fd5-131">E-Mail-Sprache der Benachrichtigungs-Versicherungen an Benutzer (unterstützte Kulturcodes von Microsoft).</span><span class="sxs-lookup"><span data-stu-id="36fd5-131">Email language of alert /notification to user(supported culture codes from microsoft).</span></span> 

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

### <span data-ttu-id="36fd5-132">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="36fd5-132">-Confirm</span></span>
<span data-ttu-id="36fd5-133">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="36fd5-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="36fd5-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="36fd5-134">-WhatIf</span></span>
<span data-ttu-id="36fd5-135">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="36fd5-135">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="36fd5-136">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="36fd5-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="36fd5-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="36fd5-137">CommonParameters</span></span>
<span data-ttu-id="36fd5-138">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="36fd5-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="36fd5-139">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="36fd5-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="36fd5-140">Eingaben</span><span class="sxs-lookup"><span data-stu-id="36fd5-140">INPUTS</span></span>

### <span data-ttu-id="36fd5-141">Keine</span><span class="sxs-lookup"><span data-stu-id="36fd5-141">None</span></span>

## <span data-ttu-id="36fd5-142">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="36fd5-142">OUTPUTS</span></span>

### <span data-ttu-id="36fd5-143">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRAlertSetting</span><span class="sxs-lookup"><span data-stu-id="36fd5-143">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRAlertSetting</span></span>

## <span data-ttu-id="36fd5-144">Notizen</span><span class="sxs-lookup"><span data-stu-id="36fd5-144">NOTES</span></span>

## <span data-ttu-id="36fd5-145">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="36fd5-145">RELATED LINKS</span></span>
