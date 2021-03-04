---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataShare.dll-Help.xml
Module Name: Az.DataShare
online version: https://docs.microsoft.com/powershell/module/az.datashare/remove-azdatasharesubscription
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Remove-AzDataShareSubscription.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Remove-AzDataShareSubscription.md
ms.openlocfilehash: 4cb023fecb020e37535f47823df6f02ee9f5050e
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101946595"
---
# <span data-ttu-id="9336a-101">Remove-AzDataShareSubscription</span><span class="sxs-lookup"><span data-stu-id="9336a-101">Remove-AzDataShareSubscription</span></span>

## <span data-ttu-id="9336a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9336a-102">SYNOPSIS</span></span>
<span data-ttu-id="9336a-103">entfernt ein Freigabeabonnement</span><span class="sxs-lookup"><span data-stu-id="9336a-103">removes a share subscription</span></span>

## <span data-ttu-id="9336a-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="9336a-104">SYNTAX</span></span>

### <span data-ttu-id="9336a-105">ByFieldsParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="9336a-105">ByFieldsParameterSet (Default)</span></span>
```
Remove-AzDataShareSubscription -ResourceGroupName <String> -AccountName <String> -Name <String> [-PassThru]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9336a-106">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="9336a-106">ByResourceIdParameterSet</span></span>
```
Remove-AzDataShareSubscription -ResourceId <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9336a-107">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="9336a-107">ByObjectParameterSet</span></span>
```
Remove-AzDataShareSubscription -InputObject <PSDataShareSubscription> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9336a-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="9336a-108">DESCRIPTION</span></span>
<span data-ttu-id="9336a-109">Das **Cmdlet Remove-AzDataShareSubscription** entfernt ein Freigabeabonnement</span><span class="sxs-lookup"><span data-stu-id="9336a-109">The **Remove-AzDataShareSubscription** cmdlet removes a share subscription</span></span>

## <span data-ttu-id="9336a-110">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="9336a-110">EXAMPLES</span></span>

### <span data-ttu-id="9336a-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="9336a-111">Example 1</span></span>
```
PS C:\> Remove-AzDataShareSubscription -ResourceGroupName "ADS" -AccountName "WikiAds" -Name "AdsShareSubscription"
Are you sure you want to remove sharesubscription "AdsShareSubscription"? 
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): Y
```

<span data-ttu-id="9336a-112">Mit diesen Befehlen wird eine ShareSubscription namens AdsShareSubscription aus dem Konto WikiAds entfernt.</span><span class="sxs-lookup"><span data-stu-id="9336a-112">This commands removes a sharesubscription named AdsShareSubscription from account WikiAds.</span></span> 

## <span data-ttu-id="9336a-113">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="9336a-113">PARAMETERS</span></span>

### <span data-ttu-id="9336a-114">-AccountName</span><span class="sxs-lookup"><span data-stu-id="9336a-114">-AccountName</span></span>
<span data-ttu-id="9336a-115">Name des Azure-Datenfreigabekontos.</span><span class="sxs-lookup"><span data-stu-id="9336a-115">Azure data share account name.</span></span>

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

### <span data-ttu-id="9336a-116">-AsJob</span><span class="sxs-lookup"><span data-stu-id="9336a-116">-AsJob</span></span>
<span data-ttu-id="9336a-117">{{Fill AsJob Description}}</span><span class="sxs-lookup"><span data-stu-id="9336a-117">{{Fill AsJob Description}}</span></span>

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

### <span data-ttu-id="9336a-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9336a-118">-DefaultProfile</span></span>
<span data-ttu-id="9336a-119">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="9336a-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9336a-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="9336a-120">-InputObject</span></span>
<span data-ttu-id="9336a-121">Azure Data Share Subscription Object</span><span class="sxs-lookup"><span data-stu-id="9336a-121">Azure data share subscription object</span></span>


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

### <span data-ttu-id="9336a-122">-Name</span><span class="sxs-lookup"><span data-stu-id="9336a-122">-Name</span></span>
<span data-ttu-id="9336a-123">Azure Data Share Subscription Name</span><span class="sxs-lookup"><span data-stu-id="9336a-123">Azure data share subscription name</span></span>

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

### <span data-ttu-id="9336a-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="9336a-124">-PassThru</span></span>
<span data-ttu-id="9336a-125">Rückgabeobjekt (sofern angegeben).</span><span class="sxs-lookup"><span data-stu-id="9336a-125">Return object (if specified).</span></span>

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

### <span data-ttu-id="9336a-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9336a-126">-ResourceGroupName</span></span>
<span data-ttu-id="9336a-127">Der Ressourcengruppenname des Azure Data Share-Kontos</span><span class="sxs-lookup"><span data-stu-id="9336a-127">The resource group name of the azure data share account</span></span>

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

### <span data-ttu-id="9336a-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="9336a-128">-ResourceId</span></span>
<span data-ttu-id="9336a-129">Die Ressourcen-ID des Azure Data Share-Abonnements</span><span class="sxs-lookup"><span data-stu-id="9336a-129">The resource id of the azure data share subscription</span></span>

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

### <span data-ttu-id="9336a-130">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="9336a-130">-Confirm</span></span>
<span data-ttu-id="9336a-131">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="9336a-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9336a-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9336a-132">-WhatIf</span></span>
<span data-ttu-id="9336a-133">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="9336a-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9336a-134">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="9336a-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9336a-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9336a-135">CommonParameters</span></span>
<span data-ttu-id="9336a-136">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9336a-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9336a-137">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="9336a-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9336a-138">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="9336a-138">INPUTS</span></span>

### <span data-ttu-id="9336a-139">System.String</span><span class="sxs-lookup"><span data-stu-id="9336a-139">System.String</span></span>

### <span data-ttu-id="9336a-140">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareSubscription</span><span class="sxs-lookup"><span data-stu-id="9336a-140">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareSubscription</span></span>

## <span data-ttu-id="9336a-141">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="9336a-141">OUTPUTS</span></span>

### <span data-ttu-id="9336a-142">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="9336a-142">System.Boolean</span></span>

## <span data-ttu-id="9336a-143">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="9336a-143">NOTES</span></span>

## <span data-ttu-id="9336a-144">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="9336a-144">RELATED LINKS</span></span>
