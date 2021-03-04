---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataShare.dll-Help.xml
Module Name: Az.DataShare
online version: https://docs.microsoft.com/powershell/module/az.datashare/stop-azdatasharesubscriptionsynchronization
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Stop-AzDataShareSubscriptionSynchronization.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Stop-AzDataShareSubscriptionSynchronization.md
ms.openlocfilehash: d92886989acbe4d78eea49ffecde90d434c88986
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101925867"
---
# <span data-ttu-id="8e4a3-101">Stop-AzDataShareSubscriptionSynchronization</span><span class="sxs-lookup"><span data-stu-id="8e4a3-101">Stop-AzDataShareSubscriptionSynchronization</span></span>

## <span data-ttu-id="8e4a3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8e4a3-102">SYNOPSIS</span></span>
<span data-ttu-id="8e4a3-103">Beendet die laufende Synchronisierung für ein Freigabeabonnement.</span><span class="sxs-lookup"><span data-stu-id="8e4a3-103">Stops ongoing synchronization for a share subscription.</span></span> <span data-ttu-id="8e4a3-104">Ein Freigabeabonnement kann über seine Ressourcen-ID oder seinen Namen angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="8e4a3-104">A share subscription can be specified through its resource id or its name.</span></span>

## <span data-ttu-id="8e4a3-105">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="8e4a3-105">SYNTAX</span></span>

### <span data-ttu-id="8e4a3-106">ByFieldsParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="8e4a3-106">ByFieldsParameterSet (Default)</span></span>
```
Stop-AzDataShareSubscriptionSynchronization -ResourceGroupName <String> -AccountName <String>
 -ShareSubscriptionName <String> -SynchronizationId <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8e4a3-107">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="8e4a3-107">ByResourceIdParameterSet</span></span>
```
Stop-AzDataShareSubscriptionSynchronization -SynchronizationId <String> -ResourceId <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8e4a3-108">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="8e4a3-108">ByObjectParameterSet</span></span>
```
Stop-AzDataShareSubscriptionSynchronization -InputObject <PSDataShareSubscription> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8e4a3-109">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="8e4a3-109">DESCRIPTION</span></span>
<span data-ttu-id="8e4a3-110">Das **Cmdlet Stop-AzDataShareSubscriptionSynchronization** beendet die laufende Synchronisierung für ein Freigabeabonnement</span><span class="sxs-lookup"><span data-stu-id="8e4a3-110">The **Stop-AzDataShareSubscriptionSynchronization** cmdlet stops ongoing synchronization for a share subscription</span></span>

## <span data-ttu-id="8e4a3-111">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="8e4a3-111">EXAMPLES</span></span>

### <span data-ttu-id="8e4a3-112">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="8e4a3-112">Example 1</span></span>
```
PS C:\> Stop-AzDataShareSubscriptionSynchronization -ResourceGroupName "ADS" -AccountName "WikiAds" -ShareSubscriptionName "AdsShareSubscription" -SynchronizationId 20a4416b-b33b-4539-a908-71dc8ef698fb

Confirm
AdsShareSubscription
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): Y

durationMs        : 231869
endTime           : 
message           :
startTime         : 7/9/2019 11:40:53 PM
status            : Canceled
synchronizationId : 20a4416b-b33b-4539-a908-71dc8ef698fb
```

<span data-ttu-id="8e4a3-113">Beendet die fortlaufende Synchronisierung, die durch id identifiziert wurde – 20a4416b-b33b-4539-a908-71dc8ef698fb</span><span class="sxs-lookup"><span data-stu-id="8e4a3-113">Stops ongoing synchronization identified by id - 20a4416b-b33b-4539-a908-71dc8ef698fb</span></span>

## <span data-ttu-id="8e4a3-114">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="8e4a3-114">PARAMETERS</span></span>

### <span data-ttu-id="8e4a3-115">-AccountName</span><span class="sxs-lookup"><span data-stu-id="8e4a3-115">-AccountName</span></span>
<span data-ttu-id="8e4a3-116">Name des Azure-Datenfreigabekontos</span><span class="sxs-lookup"><span data-stu-id="8e4a3-116">Azure data share account name</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8e4a3-117">-AsJob</span><span class="sxs-lookup"><span data-stu-id="8e4a3-117">-AsJob</span></span>
<span data-ttu-id="8e4a3-118">{{Fill AsJob Description}}</span><span class="sxs-lookup"><span data-stu-id="8e4a3-118">{{Fill AsJob Description}}</span></span>

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

### <span data-ttu-id="8e4a3-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8e4a3-119">-DefaultProfile</span></span>
<span data-ttu-id="8e4a3-120">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="8e4a3-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8e4a3-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="8e4a3-121">-InputObject</span></span>
<span data-ttu-id="8e4a3-122">Azure Data Share Subscription Object</span><span class="sxs-lookup"><span data-stu-id="8e4a3-122">Azure data share subscription object</span></span>


```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareSubscription
Parameter Sets: ByObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="8e4a3-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8e4a3-123">-ResourceGroupName</span></span>
<span data-ttu-id="8e4a3-124">Der Ressourcengruppenname des Azure Data Share-Kontos</span><span class="sxs-lookup"><span data-stu-id="8e4a3-124">The resource group name of the azure data share account</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8e4a3-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="8e4a3-125">-ResourceId</span></span>
<span data-ttu-id="8e4a3-126">Die Ressourcen-ID des Azure Share-Abonnements</span><span class="sxs-lookup"><span data-stu-id="8e4a3-126">The resource id of the azure share subscription</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8e4a3-127">-ShareSubscriptionName</span><span class="sxs-lookup"><span data-stu-id="8e4a3-127">-ShareSubscriptionName</span></span>
<span data-ttu-id="8e4a3-128">Azure Data Share Subscription Name</span><span class="sxs-lookup"><span data-stu-id="8e4a3-128">Azure data share subscription name</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8e4a3-129">-SynchronizationId</span><span class="sxs-lookup"><span data-stu-id="8e4a3-129">-SynchronizationId</span></span>
<span data-ttu-id="8e4a3-130">Synchronisierungs-ID, die beendet werden muss</span><span class="sxs-lookup"><span data-stu-id="8e4a3-130">Synchronization id that needs to be stopped</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet, ByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8e4a3-131">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="8e4a3-131">-Confirm</span></span>
<span data-ttu-id="8e4a3-132">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="8e4a3-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8e4a3-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8e4a3-133">-WhatIf</span></span>
<span data-ttu-id="8e4a3-134">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="8e4a3-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8e4a3-135">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="8e4a3-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8e4a3-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8e4a3-136">CommonParameters</span></span>
<span data-ttu-id="8e4a3-137">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8e4a3-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8e4a3-138">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="8e4a3-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8e4a3-139">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="8e4a3-139">INPUTS</span></span>

### <span data-ttu-id="8e4a3-140">System.String</span><span class="sxs-lookup"><span data-stu-id="8e4a3-140">System.String</span></span>

### <span data-ttu-id="8e4a3-141">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareSubscription</span><span class="sxs-lookup"><span data-stu-id="8e4a3-141">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareSubscription</span></span>

## <span data-ttu-id="8e4a3-142">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="8e4a3-142">OUTPUTS</span></span>

### <span data-ttu-id="8e4a3-143">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareSubscriptionSynchronization</span><span class="sxs-lookup"><span data-stu-id="8e4a3-143">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareSubscriptionSynchronization</span></span>

## <span data-ttu-id="8e4a3-144">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="8e4a3-144">NOTES</span></span>

## <span data-ttu-id="8e4a3-145">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="8e4a3-145">RELATED LINKS</span></span>
