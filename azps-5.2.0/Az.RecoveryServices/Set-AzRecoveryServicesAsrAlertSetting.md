---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/set-azrecoveryservicesasralertsetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Set-AzRecoveryServicesAsrAlertSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Set-AzRecoveryServicesAsrAlertSetting.md
ms.openlocfilehash: c7821ddfd07b17a77c482a770b28672ccd664cb4
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98360715"
---
# <span data-ttu-id="891f6-101">Set-AzRecoveryServicesAsrAlertSetting</span><span class="sxs-lookup"><span data-stu-id="891f6-101">Set-AzRecoveryServicesAsrAlertSetting</span></span>

## <span data-ttu-id="891f6-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="891f6-102">SYNOPSIS</span></span>
<span data-ttu-id="891f6-103">Konfigurieren Sie die Benachrichtigungseinstellungen für die Azure-Websitewiederherstellung (E-Mail-Benachrichtigung) für den Tresor.</span><span class="sxs-lookup"><span data-stu-id="891f6-103">Configure Azure Site Recovery notification settings (email notification) for the vault.</span></span>

## <span data-ttu-id="891f6-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="891f6-104">SYNTAX</span></span>

### <span data-ttu-id="891f6-105">Festlegen (Standard)</span><span class="sxs-lookup"><span data-stu-id="891f6-105">Set (Default)</span></span>
```
Set-AzRecoveryServicesAsrAlertSetting [-CustomEmailAddress <String[]>] [-LocaleID <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="891f6-106">EmailToSubscriptionOwner</span><span class="sxs-lookup"><span data-stu-id="891f6-106">EmailToSubscriptionOwner</span></span>
```
Set-AzRecoveryServicesAsrAlertSetting [-EnableEmailSubscriptionOwner] [-CustomEmailAddress <String[]>]
 [-LocaleID <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="891f6-107">DisableEmailToSubcriptionOwner</span><span class="sxs-lookup"><span data-stu-id="891f6-107">DisableEmailToSubcriptionOwner</span></span>
```
Set-AzRecoveryServicesAsrAlertSetting [-DisableEmailToSubscriptionOwner] [-CustomEmailAddress <String[]>]
 [-LocaleID <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="891f6-108">Deaktivieren</span><span class="sxs-lookup"><span data-stu-id="891f6-108">Disable</span></span>
```
Set-AzRecoveryServicesAsrAlertSetting [-DisableNotification] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="891f6-109">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="891f6-109">DESCRIPTION</span></span>
<span data-ttu-id="891f6-110">Das **Cmdlet "Set-AzRecoveryServicesAsrNotificationSetting"** konfiguriert die Benachrichtigungseinstellungen für die Azure-Websitewiederherstellung (E-Mail-Benachrichtigung) für den Tresor.</span><span class="sxs-lookup"><span data-stu-id="891f6-110">The **Set-AzRecoveryServicesAsrNotificationSetting** cmdlet configures Azure Site Recovery notification settings (email notification) for the vault.</span></span>

## <span data-ttu-id="891f6-111">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="891f6-111">EXAMPLES</span></span>

### <span data-ttu-id="891f6-112">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="891f6-112">Example 1</span></span>
```powershell
PS C:\> Set-AzRecoveryServicesAsrAlertSetting -DisableNotification

CustomEmailAddress EmailSubscriptionOwner Locale
------------------ ---------------------- ------
{}                 Off                    en-US
```

<span data-ttu-id="891f6-113">"Benachrichtigung deaktivieren" aus.</span><span class="sxs-lookup"><span data-stu-id="891f6-113">Disable notification.</span></span>

### <span data-ttu-id="891f6-114">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="891f6-114">Example 2</span></span>
```powershell
PS C:\> Set-AzRecoveryServicesAsrAlertSetting -CustomEmailAddress "abcxxxx@xxxx.com" -EnableEmailSubscriptionOwner

CustomEmailAddress     EmailSubscriptionOwner Locale
------------------     ---------------------- ------
{abcxxxx@xxxx.com} On                     en-US
```

<span data-ttu-id="891f6-115">Legen Sie Benachrichtigungen für benutzerdefinierte E-Mail-Adressen und Für Abonnementbesitzer festgelegt.</span><span class="sxs-lookup"><span data-stu-id="891f6-115">Set notification for custom email address(s) and for subscription owner.</span></span>

### <span data-ttu-id="891f6-116">Beispiel 3</span><span class="sxs-lookup"><span data-stu-id="891f6-116">Example 3</span></span>

<span data-ttu-id="891f6-117">Konfigurieren Sie die Benachrichtigungseinstellungen für die Azure-Websitewiederherstellung (E-Mail-Benachrichtigung) für den Tresor.</span><span class="sxs-lookup"><span data-stu-id="891f6-117">Configure Azure Site Recovery notification settings (email notification) for the vault.</span></span> <span data-ttu-id="891f6-118">(automatisch generiert)</span><span class="sxs-lookup"><span data-stu-id="891f6-118">(autogenerated)</span></span>

```powershell <!-- Aladdin Generated Example --> 
Set-AzRecoveryServicesAsrAlertSetting -CustomEmailAddress 'abcxxxx@xxxx.com' -DisableEmailToSubscriptionOwner
```

## <span data-ttu-id="891f6-119">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="891f6-119">PARAMETERS</span></span>

### <span data-ttu-id="891f6-120">-CustomEmailAddress</span><span class="sxs-lookup"><span data-stu-id="891f6-120">-CustomEmailAddress</span></span>
<span data-ttu-id="891f6-121">Benachrichtigung/Benachrichtigung, die an E-Mails gesendet wird.</span><span class="sxs-lookup"><span data-stu-id="891f6-121">Alert / Notification sent to emails.</span></span>

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

### <span data-ttu-id="891f6-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="891f6-122">-DefaultProfile</span></span>
<span data-ttu-id="891f6-123">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="891f6-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="891f6-124">-DisableEmailToSubscriptionOwner</span><span class="sxs-lookup"><span data-stu-id="891f6-124">-DisableEmailToSubscriptionOwner</span></span>
<span data-ttu-id="891f6-125">"Parameter wechseln" gibt die Benachrichtigung an den Abonnementbesitzer an.</span><span class="sxs-lookup"><span data-stu-id="891f6-125">Switch parameter specifies enable notification to subscription owner.</span></span>

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

### <span data-ttu-id="891f6-126">-DisableNotification</span><span class="sxs-lookup"><span data-stu-id="891f6-126">-DisableNotification</span></span>
<span data-ttu-id="891f6-127">Kennzeichnen, um alle Benachrichtigungen zu deaktivieren.</span><span class="sxs-lookup"><span data-stu-id="891f6-127">Flag to disable all notification.</span></span>

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

### <span data-ttu-id="891f6-128">-EnableEmailSubscriptionOwner</span><span class="sxs-lookup"><span data-stu-id="891f6-128">-EnableEmailSubscriptionOwner</span></span>
<span data-ttu-id="891f6-129">"Parameter wechseln" gibt die Benachrichtigung an den Abonnementbesitzer an.</span><span class="sxs-lookup"><span data-stu-id="891f6-129">Switch parameter specifies enable notification to subscription owner.</span></span>

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

### <span data-ttu-id="891f6-130">-LocaleID</span><span class="sxs-lookup"><span data-stu-id="891f6-130">-LocaleID</span></span>
<span data-ttu-id="891f6-131">E-Mail-Sprache der Warnung/Benachrichtigung an Benutzer (unterstützte Kulturcodes von Microsoft).</span><span class="sxs-lookup"><span data-stu-id="891f6-131">Email language of alert /notification to user(supported culture codes from microsoft).</span></span> 

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

### <span data-ttu-id="891f6-132">-Confirm</span><span class="sxs-lookup"><span data-stu-id="891f6-132">-Confirm</span></span>
<span data-ttu-id="891f6-133">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="891f6-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="891f6-134">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="891f6-134">-WhatIf</span></span>
<span data-ttu-id="891f6-135">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="891f6-135">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="891f6-136">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="891f6-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="891f6-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="891f6-137">CommonParameters</span></span>
<span data-ttu-id="891f6-138">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="891f6-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="891f6-139">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="891f6-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="891f6-140">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="891f6-140">INPUTS</span></span>

### <span data-ttu-id="891f6-141">Keine</span><span class="sxs-lookup"><span data-stu-id="891f6-141">None</span></span>

## <span data-ttu-id="891f6-142">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="891f6-142">OUTPUTS</span></span>

### <span data-ttu-id="891f6-143">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRAlertSetting</span><span class="sxs-lookup"><span data-stu-id="891f6-143">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRAlertSetting</span></span>

## <span data-ttu-id="891f6-144">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="891f6-144">NOTES</span></span>

## <span data-ttu-id="891f6-145">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="891f6-145">RELATED LINKS</span></span>
