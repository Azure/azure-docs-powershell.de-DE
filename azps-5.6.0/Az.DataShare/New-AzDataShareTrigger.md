---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataShare.dll-Help.xml
Module Name: Az.DataShare
online version: https://docs.microsoft.com/powershell/module/az.datashare/new-azdatasharetrigger
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/New-AzDataShareTrigger.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/New-AzDataShareTrigger.md
ms.openlocfilehash: fe082dc38f8a16dcca897623c4817d728fdaf3c3
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101924984"
---
# <span data-ttu-id="1ce5d-101">New-AzDataShareTrigger</span><span class="sxs-lookup"><span data-stu-id="1ce5d-101">New-AzDataShareTrigger</span></span>

## <span data-ttu-id="1ce5d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1ce5d-102">SYNOPSIS</span></span>
<span data-ttu-id="1ce5d-103">Erstellt einen Trigger für ein Freigabeabonnement.</span><span class="sxs-lookup"><span data-stu-id="1ce5d-103">Creates a trigger for share subscription.</span></span>

## <span data-ttu-id="1ce5d-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="1ce5d-104">SYNTAX</span></span>

```
New-AzDataShareTrigger -ResourceGroupName <String> -AccountName <String> [-ShareSubscriptionName <String>]
 -Name <String> -RecurrenceInterval <String> -SynchronizationTime <DateTime> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1ce5d-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="1ce5d-105">DESCRIPTION</span></span>
<span data-ttu-id="1ce5d-106">Das **New-AzDataShareTrigger-Cmdlet** erstellt einen Trigger für das Freigabeabonnement für das angegebene Serienintervall und die Synchronisierungszeit unter azure data share account.</span><span class="sxs-lookup"><span data-stu-id="1ce5d-106">The **New-AzDataShareTrigger** cmdlet creates a trigger for share subscription for the specified recurrence interval and synchronization time under azure data share account.</span></span>

## <span data-ttu-id="1ce5d-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="1ce5d-107">EXAMPLES</span></span>

### <span data-ttu-id="1ce5d-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="1ce5d-108">Example 1</span></span>
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

<span data-ttu-id="1ce5d-109">Mit diesem Befehl wird ein neuer Trigger AdsTrigger für das Share-Abonnement AdsShareSubscription mit einem täglichen Intervall von 9:00 Uhr erstellt.</span><span class="sxs-lookup"><span data-stu-id="1ce5d-109">This command creates a new trigger AdsTrigger for share subscription AdsShareSubscription with a daily recurrence interval of 9 am.</span></span>

## <span data-ttu-id="1ce5d-110">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="1ce5d-110">PARAMETERS</span></span>

### <span data-ttu-id="1ce5d-111">-AccountName</span><span class="sxs-lookup"><span data-stu-id="1ce5d-111">-AccountName</span></span>
<span data-ttu-id="1ce5d-112">Name des Azure-Datenfreigabekontos</span><span class="sxs-lookup"><span data-stu-id="1ce5d-112">Azure data share account name</span></span>

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

### <span data-ttu-id="1ce5d-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="1ce5d-113">-AsJob</span></span>
<span data-ttu-id="1ce5d-114">{{Fill AsJob Description}}</span><span class="sxs-lookup"><span data-stu-id="1ce5d-114">{{Fill AsJob Description}}</span></span>

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

### <span data-ttu-id="1ce5d-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1ce5d-115">-DefaultProfile</span></span>
<span data-ttu-id="1ce5d-116">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="1ce5d-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1ce5d-117">-Name</span><span class="sxs-lookup"><span data-stu-id="1ce5d-117">-Name</span></span>
<span data-ttu-id="1ce5d-118">Name des Azure-Datenfreigabetriggers</span><span class="sxs-lookup"><span data-stu-id="1ce5d-118">Azure data share trigger name</span></span>

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

### <span data-ttu-id="1ce5d-119">-RecurrenceInterval</span><span class="sxs-lookup"><span data-stu-id="1ce5d-119">-RecurrenceInterval</span></span>
<span data-ttu-id="1ce5d-120">Das Serienintervall für den Trigger (Tag oder Stunde)</span><span class="sxs-lookup"><span data-stu-id="1ce5d-120">The recurrence interval for the trigger (Day or Hour)</span></span>

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

### <span data-ttu-id="1ce5d-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1ce5d-121">-ResourceGroupName</span></span>
<span data-ttu-id="1ce5d-122">Der Ressourcengruppenname des Azure Data Share-Kontos</span><span class="sxs-lookup"><span data-stu-id="1ce5d-122">The resource group name of the azure data share account</span></span>

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

### <span data-ttu-id="1ce5d-123">-ShareSubscriptionName</span><span class="sxs-lookup"><span data-stu-id="1ce5d-123">-ShareSubscriptionName</span></span>
<span data-ttu-id="1ce5d-124">Azure Data Share Subscription Name</span><span class="sxs-lookup"><span data-stu-id="1ce5d-124">Azure data share subscription name</span></span>

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

### <span data-ttu-id="1ce5d-125">-SynchronizationTime</span><span class="sxs-lookup"><span data-stu-id="1ce5d-125">-SynchronizationTime</span></span>
<span data-ttu-id="1ce5d-126">Die Startzeit der geplanten Synchronisierung für den Trigger</span><span class="sxs-lookup"><span data-stu-id="1ce5d-126">The start time of the scheduled synchronization for the trigger</span></span>

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

### <span data-ttu-id="1ce5d-127">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="1ce5d-127">-Confirm</span></span>
<span data-ttu-id="1ce5d-128">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="1ce5d-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1ce5d-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1ce5d-129">-WhatIf</span></span>
<span data-ttu-id="1ce5d-130">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="1ce5d-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1ce5d-131">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="1ce5d-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1ce5d-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1ce5d-132">CommonParameters</span></span>
<span data-ttu-id="1ce5d-133">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1ce5d-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1ce5d-134">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="1ce5d-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1ce5d-135">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="1ce5d-135">INPUTS</span></span>

### <span data-ttu-id="1ce5d-136">Keine</span><span class="sxs-lookup"><span data-stu-id="1ce5d-136">None</span></span>

## <span data-ttu-id="1ce5d-137">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="1ce5d-137">OUTPUTS</span></span>

### <span data-ttu-id="1ce5d-138">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareInvitation</span><span class="sxs-lookup"><span data-stu-id="1ce5d-138">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareInvitation</span></span>

## <span data-ttu-id="1ce5d-139">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="1ce5d-139">NOTES</span></span>

## <span data-ttu-id="1ce5d-140">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="1ce5d-140">RELATED LINKS</span></span>
