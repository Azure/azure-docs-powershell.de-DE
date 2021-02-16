---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataShare.dll-Help.xml
Module Name: Az.DataShare
online version: https://docs.microsoft.com/en-us/powershell/module/az.datashare/remove-azdatasharetrigger
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Remove-AzDataShareTrigger.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Remove-AzDataShareTrigger.md
ms.openlocfilehash: f4eff969d93f1c243b9dc15652249bc9800bfd45
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100170802"
---
# <span data-ttu-id="48cfe-101">Remove-AzDataShareTrigger</span><span class="sxs-lookup"><span data-stu-id="48cfe-101">Remove-AzDataShareTrigger</span></span>

## <span data-ttu-id="48cfe-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="48cfe-102">SYNOPSIS</span></span>
<span data-ttu-id="48cfe-103">Entfernt einen Trigger</span><span class="sxs-lookup"><span data-stu-id="48cfe-103">removes a trigger</span></span>

## <span data-ttu-id="48cfe-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="48cfe-104">SYNTAX</span></span>

### <span data-ttu-id="48cfe-105">ByFieldsParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="48cfe-105">ByFieldsParameterSet (Default)</span></span>
```
Remove-AzDataShareTrigger -ResourceGroupName <String> -AccountName <String> [-ShareSubscriptionName <String>]
 -Name <String> [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="48cfe-106">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="48cfe-106">ByResourceIdParameterSet</span></span>
```
Remove-AzDataShareTrigger -ResourceId <String> [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="48cfe-107">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="48cfe-107">ByObjectParameterSet</span></span>
```
Remove-AzDataShareTrigger -InputObject <PSDataShareTrigger> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="48cfe-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="48cfe-108">DESCRIPTION</span></span>
<span data-ttu-id="48cfe-109">Das **Cmdlet "Remove-AzDataShareTrigger"** entfernt einen Datenfreigabetrigger.</span><span class="sxs-lookup"><span data-stu-id="48cfe-109">The **Remove-AzDataShareTrigger** cmdlet removes a datashare trigger</span></span>

## <span data-ttu-id="48cfe-110">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="48cfe-110">EXAMPLES</span></span>

### <span data-ttu-id="48cfe-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="48cfe-111">Example 1</span></span>
```
PS C:\> Remove-AzDataShareTrigger -ResourceGroupName "ADS" -AccountName "WikiAds" -ShareSubscriptionName "AdsShareSubscription" -Name "AdsTrigger"

Are you sure you want to remove trigger "AdsTrigger"? 
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): Y
```

<span data-ttu-id="48cfe-112">Mit diesen Befehlen wird ein Trigger mit dem Namen "AdsTrigger" aus dem AdsShareSubscription-Freigabeabonnement entfernt.</span><span class="sxs-lookup"><span data-stu-id="48cfe-112">This commands removes a trigger named AdsTrigger from share subscription AdsShareSubscription.</span></span> 

## <span data-ttu-id="48cfe-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="48cfe-113">PARAMETERS</span></span>

### <span data-ttu-id="48cfe-114">-AccountName</span><span class="sxs-lookup"><span data-stu-id="48cfe-114">-AccountName</span></span>
<span data-ttu-id="48cfe-115">Name des Azure-Datenfreigabekontos</span><span class="sxs-lookup"><span data-stu-id="48cfe-115">Azure data share account name</span></span>

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

### <span data-ttu-id="48cfe-116">-AsJob</span><span class="sxs-lookup"><span data-stu-id="48cfe-116">-AsJob</span></span>
<span data-ttu-id="48cfe-117">{{Fill AsJob Description}}</span><span class="sxs-lookup"><span data-stu-id="48cfe-117">{{Fill AsJob Description}}</span></span>

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

### <span data-ttu-id="48cfe-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="48cfe-118">-DefaultProfile</span></span>
<span data-ttu-id="48cfe-119">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="48cfe-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="48cfe-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="48cfe-120">-InputObject</span></span>
<span data-ttu-id="48cfe-121">Azure Data Share Trigger Object</span><span class="sxs-lookup"><span data-stu-id="48cfe-121">Azure data share trigger object</span></span>


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

### <span data-ttu-id="48cfe-122">-Name</span><span class="sxs-lookup"><span data-stu-id="48cfe-122">-Name</span></span>
<span data-ttu-id="48cfe-123">Name des Azure-Datenfreigabe-Triggers</span><span class="sxs-lookup"><span data-stu-id="48cfe-123">Azure data share trigger name</span></span>

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

### <span data-ttu-id="48cfe-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="48cfe-124">-PassThru</span></span>
<span data-ttu-id="48cfe-125">Rückgabeobjekt (sofern angegeben)</span><span class="sxs-lookup"><span data-stu-id="48cfe-125">Return object (if specified).</span></span>

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

### <span data-ttu-id="48cfe-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="48cfe-126">-ResourceGroupName</span></span>
<span data-ttu-id="48cfe-127">Der Ressourcengruppenname des Azure Data Share-Kontos</span><span class="sxs-lookup"><span data-stu-id="48cfe-127">The resource group name of the azure data share account</span></span>

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

### <span data-ttu-id="48cfe-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="48cfe-128">-ResourceId</span></span>
<span data-ttu-id="48cfe-129">Die Ressourcen-ID des Azure Data Share Triggers</span><span class="sxs-lookup"><span data-stu-id="48cfe-129">The resource id of azure data share trigger</span></span>

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

### <span data-ttu-id="48cfe-130">-ShareSubscriptionName</span><span class="sxs-lookup"><span data-stu-id="48cfe-130">-ShareSubscriptionName</span></span>
<span data-ttu-id="48cfe-131">Name des Azure Data Share-Abonnements</span><span class="sxs-lookup"><span data-stu-id="48cfe-131">Azure data share subscription name</span></span>

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

### <span data-ttu-id="48cfe-132">-Confirm</span><span class="sxs-lookup"><span data-stu-id="48cfe-132">-Confirm</span></span>
<span data-ttu-id="48cfe-133">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="48cfe-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="48cfe-134">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="48cfe-134">-WhatIf</span></span>
<span data-ttu-id="48cfe-135">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="48cfe-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="48cfe-136">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="48cfe-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="48cfe-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="48cfe-137">CommonParameters</span></span>
<span data-ttu-id="48cfe-138">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="48cfe-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="48cfe-139">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="48cfe-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="48cfe-140">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="48cfe-140">INPUTS</span></span>

### <span data-ttu-id="48cfe-141">System.String</span><span class="sxs-lookup"><span data-stu-id="48cfe-141">System.String</span></span>

### <span data-ttu-id="48cfe-142">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareTrigger</span><span class="sxs-lookup"><span data-stu-id="48cfe-142">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareTrigger</span></span>

## <span data-ttu-id="48cfe-143">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="48cfe-143">OUTPUTS</span></span>

### <span data-ttu-id="48cfe-144">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="48cfe-144">System.Boolean</span></span>

## <span data-ttu-id="48cfe-145">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="48cfe-145">NOTES</span></span>

## <span data-ttu-id="48cfe-146">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="48cfe-146">RELATED LINKS</span></span>
