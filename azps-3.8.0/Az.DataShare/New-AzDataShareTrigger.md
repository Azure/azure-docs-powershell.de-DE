---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataShare.dll-Help.xml
Module Name: Az.DataShare
online version: https://docs.microsoft.com/en-us/powershell/module/az.datashare/new-azdatasharetrigger
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/New-AzDataShareTrigger.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/New-AzDataShareTrigger.md
ms.openlocfilehash: a0f8651bab30cf5a439b6e16110b34e7d256aa3a
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/21/2020
ms.locfileid: "93996529"
---
# <span data-ttu-id="d6f1a-101">New-AzDataShareTrigger</span><span class="sxs-lookup"><span data-stu-id="d6f1a-101">New-AzDataShareTrigger</span></span>

## <span data-ttu-id="d6f1a-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="d6f1a-102">SYNOPSIS</span></span>
<span data-ttu-id="d6f1a-103">Erstellt einen Trigger für das Freigabe Abonnement.</span><span class="sxs-lookup"><span data-stu-id="d6f1a-103">Creates a trigger for share subscription.</span></span>

## <span data-ttu-id="d6f1a-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="d6f1a-104">SYNTAX</span></span>

```
New-AzDataShareTrigger -ResourceGroupName <String> -AccountName <String> [-ShareSubscriptionName <String>]
 -Name <String> -RecurrenceInterval <String> -SynchronizationTime <DateTime> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d6f1a-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="d6f1a-105">DESCRIPTION</span></span>
<span data-ttu-id="d6f1a-106">Das Cmdlet **New-AzDataShareTrigger** erstellt einen Trigger für das Freigabe Abonnement für das angegebene Serienintervall und die Synchronisierungszeit unter Azure Data Share-Konto.</span><span class="sxs-lookup"><span data-stu-id="d6f1a-106">The **New-AzDataShareTrigger** cmdlet creates a trigger for share subscription for the specified recurrence interval and synchronization time under azure data share account.</span></span>

## <span data-ttu-id="d6f1a-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="d6f1a-107">EXAMPLES</span></span>

### <span data-ttu-id="d6f1a-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="d6f1a-108">Example 1</span></span>
```
PS C:\> New-AzDataShareTrigger -ResourceGroupName "ADS" -AccountName "WikiAds" -ShareSubscriptionName "AdsShareSubscription" -Name "AdsTrigger" -RecurrenceInterval "Day" -SynchronizationTime "9:00"
CreatedAt           : 7/10/2019 12:16:34 AM
CreatedBy           : Ads test
ProvisioningState   : Succeeded
RecurrenceInterval  : Day
SynchronizationMode : Incremental
SynchronizationTime : 7/9/2019 9:00:00 AM
TriggerStatus       : Active
Id                  : /subscriptions/1834da9b-787a-44f6-ae81-60707ab8c957/resourceGroups/ADS/providers/Microsoft.DataShare/accounts/WikiAds/shareSubscriptions/AdsShareSubscription/triggers/AdsTrigger
Name                : AdsTrigger
Type                : Microsoft.DataShare/Triggers
```

<span data-ttu-id="d6f1a-109">Dieser Befehl erstellt einen neuen Trigger-AdsTrigger für Share-Abonnement-AdsShareSubscription mit einem täglichen Serienintervall von 9 Uhr.</span><span class="sxs-lookup"><span data-stu-id="d6f1a-109">This command creates a new trigger AdsTrigger for share subscription AdsShareSubscription with a daily recurrence interval of 9 am.</span></span>

## <span data-ttu-id="d6f1a-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="d6f1a-110">PARAMETERS</span></span>

### <span data-ttu-id="d6f1a-111">-Kontoname</span><span class="sxs-lookup"><span data-stu-id="d6f1a-111">-AccountName</span></span>
<span data-ttu-id="d6f1a-112">Name des Azure-Datenfreigabe Kontos</span><span class="sxs-lookup"><span data-stu-id="d6f1a-112">Azure data share account name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d6f1a-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="d6f1a-113">-AsJob</span></span>
<span data-ttu-id="d6f1a-114">{{Fill AsJob Description}}</span><span class="sxs-lookup"><span data-stu-id="d6f1a-114">{{Fill AsJob Description}}</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d6f1a-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d6f1a-115">-DefaultProfile</span></span>
<span data-ttu-id="d6f1a-116">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="d6f1a-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d6f1a-117">-Name</span><span class="sxs-lookup"><span data-stu-id="d6f1a-117">-Name</span></span>
<span data-ttu-id="d6f1a-118">Name des Azure Data Freigabe-Triggers</span><span class="sxs-lookup"><span data-stu-id="d6f1a-118">Azure data share trigger name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d6f1a-119">-RecurrenceInterval</span><span class="sxs-lookup"><span data-stu-id="d6f1a-119">-RecurrenceInterval</span></span>
<span data-ttu-id="d6f1a-120">Das Wiederholungsintervall für den Trigger (Tag oder Stunde)</span><span class="sxs-lookup"><span data-stu-id="d6f1a-120">The recurrence interval for the trigger (Day or Hour)</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d6f1a-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d6f1a-121">-ResourceGroupName</span></span>
<span data-ttu-id="d6f1a-122">Der Name der Ressourcengruppe des Azure Data Share-Kontos</span><span class="sxs-lookup"><span data-stu-id="d6f1a-122">The resource group name of the azure data share account</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d6f1a-123">-ShareSubscriptionName</span><span class="sxs-lookup"><span data-stu-id="d6f1a-123">-ShareSubscriptionName</span></span>
<span data-ttu-id="d6f1a-124">Name des Azure Data Share-Abonnements</span><span class="sxs-lookup"><span data-stu-id="d6f1a-124">Azure data share subscription name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d6f1a-125">-Synchronisierungs Zeitwahl</span><span class="sxs-lookup"><span data-stu-id="d6f1a-125">-SynchronizationTime</span></span>
<span data-ttu-id="d6f1a-126">Die Startzeit der geplanten Synchronisierung für den Trigger</span><span class="sxs-lookup"><span data-stu-id="d6f1a-126">The start time of the scheduled synchronization for the trigger</span></span>

```yaml
Type: System.DateTime
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d6f1a-127">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="d6f1a-127">-Confirm</span></span>
<span data-ttu-id="d6f1a-128">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="d6f1a-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d6f1a-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d6f1a-129">-WhatIf</span></span>
<span data-ttu-id="d6f1a-130">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="d6f1a-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d6f1a-131">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="d6f1a-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d6f1a-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d6f1a-132">CommonParameters</span></span>
<span data-ttu-id="d6f1a-133">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d6f1a-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d6f1a-134">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d6f1a-134">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d6f1a-135">Eingaben</span><span class="sxs-lookup"><span data-stu-id="d6f1a-135">INPUTS</span></span>

### <span data-ttu-id="d6f1a-136">Keine</span><span class="sxs-lookup"><span data-stu-id="d6f1a-136">None</span></span>

## <span data-ttu-id="d6f1a-137">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="d6f1a-137">OUTPUTS</span></span>

### <span data-ttu-id="d6f1a-138">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareInvitation</span><span class="sxs-lookup"><span data-stu-id="d6f1a-138">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareInvitation</span></span>

## <span data-ttu-id="d6f1a-139">Notizen</span><span class="sxs-lookup"><span data-stu-id="d6f1a-139">NOTES</span></span>

## <span data-ttu-id="d6f1a-140">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="d6f1a-140">RELATED LINKS</span></span>
