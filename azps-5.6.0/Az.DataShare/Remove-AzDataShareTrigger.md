---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataShare.dll-Help.xml
Module Name: Az.DataShare
online version: https://docs.microsoft.com/powershell/module/az.datashare/remove-azdatasharetrigger
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Remove-AzDataShareTrigger.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Remove-AzDataShareTrigger.md
ms.openlocfilehash: 9ee4c8c25f6a9575283c8e5f077be7107756f701
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101925880"
---
# <span data-ttu-id="75677-101">Remove-AzDataShareTrigger</span><span class="sxs-lookup"><span data-stu-id="75677-101">Remove-AzDataShareTrigger</span></span>

## <span data-ttu-id="75677-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="75677-102">SYNOPSIS</span></span>
<span data-ttu-id="75677-103">entfernt einen Trigger</span><span class="sxs-lookup"><span data-stu-id="75677-103">removes a trigger</span></span>

## <span data-ttu-id="75677-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="75677-104">SYNTAX</span></span>

### <span data-ttu-id="75677-105">ByFieldsParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="75677-105">ByFieldsParameterSet (Default)</span></span>
```
Remove-AzDataShareTrigger -ResourceGroupName <String> -AccountName <String> [-ShareSubscriptionName <String>]
 -Name <String> [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="75677-106">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="75677-106">ByResourceIdParameterSet</span></span>
```
Remove-AzDataShareTrigger -ResourceId <String> [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="75677-107">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="75677-107">ByObjectParameterSet</span></span>
```
Remove-AzDataShareTrigger -InputObject <PSDataShareTrigger> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="75677-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="75677-108">DESCRIPTION</span></span>
<span data-ttu-id="75677-109">Das **Cmdlet Remove-AzDataShareTrigger** entfernt einen Datenfreigabetrigger</span><span class="sxs-lookup"><span data-stu-id="75677-109">The **Remove-AzDataShareTrigger** cmdlet removes a datashare trigger</span></span>

## <span data-ttu-id="75677-110">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="75677-110">EXAMPLES</span></span>

### <span data-ttu-id="75677-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="75677-111">Example 1</span></span>
```
PS C:\> Remove-AzDataShareTrigger -ResourceGroupName "ADS" -AccountName "WikiAds" -ShareSubscriptionName "AdsShareSubscription" -Name "AdsTrigger"

Are you sure you want to remove trigger "AdsTrigger"? 
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): Y
```

<span data-ttu-id="75677-112">Mit diesen Befehlen wird ein Trigger namens AdsTrigger aus dem Share-Abonnement AdsShareSubscription entfernt.</span><span class="sxs-lookup"><span data-stu-id="75677-112">This commands removes a trigger named AdsTrigger from share subscription AdsShareSubscription.</span></span> 

## <span data-ttu-id="75677-113">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="75677-113">PARAMETERS</span></span>

### <span data-ttu-id="75677-114">-AccountName</span><span class="sxs-lookup"><span data-stu-id="75677-114">-AccountName</span></span>
<span data-ttu-id="75677-115">Name des Azure-Datenfreigabekontos</span><span class="sxs-lookup"><span data-stu-id="75677-115">Azure data share account name</span></span>

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

### <span data-ttu-id="75677-116">-AsJob</span><span class="sxs-lookup"><span data-stu-id="75677-116">-AsJob</span></span>
<span data-ttu-id="75677-117">{{Fill AsJob Description}}</span><span class="sxs-lookup"><span data-stu-id="75677-117">{{Fill AsJob Description}}</span></span>

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

### <span data-ttu-id="75677-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="75677-118">-DefaultProfile</span></span>
<span data-ttu-id="75677-119">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="75677-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="75677-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="75677-120">-InputObject</span></span>
<span data-ttu-id="75677-121">Azure-Datenfreigabetriggerobjekt</span><span class="sxs-lookup"><span data-stu-id="75677-121">Azure data share trigger object</span></span>


```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareTrigger
Parameter Sets: ByObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="75677-122">-Name</span><span class="sxs-lookup"><span data-stu-id="75677-122">-Name</span></span>
<span data-ttu-id="75677-123">Name des Azure-Datenfreigabetriggers</span><span class="sxs-lookup"><span data-stu-id="75677-123">Azure data share trigger name</span></span>

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

### <span data-ttu-id="75677-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="75677-124">-PassThru</span></span>
<span data-ttu-id="75677-125">Rückgabeobjekt (sofern angegeben).</span><span class="sxs-lookup"><span data-stu-id="75677-125">Return object (if specified).</span></span>

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

### <span data-ttu-id="75677-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="75677-126">-ResourceGroupName</span></span>
<span data-ttu-id="75677-127">Der Ressourcengruppenname des Azure Data Share-Kontos</span><span class="sxs-lookup"><span data-stu-id="75677-127">The resource group name of the azure data share account</span></span>

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

### <span data-ttu-id="75677-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="75677-128">-ResourceId</span></span>
<span data-ttu-id="75677-129">Die Ressourcen-ID des Azure-Datenfreigabetriggers</span><span class="sxs-lookup"><span data-stu-id="75677-129">The resource id of azure data share trigger</span></span>

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

### <span data-ttu-id="75677-130">-ShareSubscriptionName</span><span class="sxs-lookup"><span data-stu-id="75677-130">-ShareSubscriptionName</span></span>
<span data-ttu-id="75677-131">Azure Data Share Subscription Name</span><span class="sxs-lookup"><span data-stu-id="75677-131">Azure data share subscription name</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="75677-132">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="75677-132">-Confirm</span></span>
<span data-ttu-id="75677-133">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="75677-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="75677-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="75677-134">-WhatIf</span></span>
<span data-ttu-id="75677-135">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="75677-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="75677-136">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="75677-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="75677-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="75677-137">CommonParameters</span></span>
<span data-ttu-id="75677-138">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="75677-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="75677-139">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="75677-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="75677-140">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="75677-140">INPUTS</span></span>

### <span data-ttu-id="75677-141">System.String</span><span class="sxs-lookup"><span data-stu-id="75677-141">System.String</span></span>

### <span data-ttu-id="75677-142">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareTrigger</span><span class="sxs-lookup"><span data-stu-id="75677-142">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareTrigger</span></span>

## <span data-ttu-id="75677-143">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="75677-143">OUTPUTS</span></span>

### <span data-ttu-id="75677-144">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="75677-144">System.Boolean</span></span>

## <span data-ttu-id="75677-145">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="75677-145">NOTES</span></span>

## <span data-ttu-id="75677-146">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="75677-146">RELATED LINKS</span></span>
