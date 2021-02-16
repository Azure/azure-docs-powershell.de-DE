---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataShare.dll-Help.xml
Module Name: Az.DataShare
online version: https://docs.microsoft.com/en-us/powershell/module/az.datashare/remove-azdatasharesubscription
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Remove-AzDataShareSubscription.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Remove-AzDataShareSubscription.md
ms.openlocfilehash: eb2b7f1e22ff3d2fccdff0d84a77f5c68ca8e70d
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100167769"
---
# <span data-ttu-id="a9e42-101">Remove-AzDataShareSubscription</span><span class="sxs-lookup"><span data-stu-id="a9e42-101">Remove-AzDataShareSubscription</span></span>

## <span data-ttu-id="a9e42-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a9e42-102">SYNOPSIS</span></span>
<span data-ttu-id="a9e42-103">entfernt ein Freigabeabonnement</span><span class="sxs-lookup"><span data-stu-id="a9e42-103">removes a share subscription</span></span>

## <span data-ttu-id="a9e42-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="a9e42-104">SYNTAX</span></span>

### <span data-ttu-id="a9e42-105">ByFieldsParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="a9e42-105">ByFieldsParameterSet (Default)</span></span>
```
Remove-AzDataShareSubscription -ResourceGroupName <String> -AccountName <String> -Name <String> [-PassThru]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a9e42-106">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="a9e42-106">ByResourceIdParameterSet</span></span>
```
Remove-AzDataShareSubscription -ResourceId <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a9e42-107">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="a9e42-107">ByObjectParameterSet</span></span>
```
Remove-AzDataShareSubscription -InputObject <PSDataShareSubscription> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a9e42-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="a9e42-108">DESCRIPTION</span></span>
<span data-ttu-id="a9e42-109">Das **Cmdlet "Remove-AzDataShareSubscription"** entfernt ein Freigabeabonnement</span><span class="sxs-lookup"><span data-stu-id="a9e42-109">The **Remove-AzDataShareSubscription** cmdlet removes a share subscription</span></span>

## <span data-ttu-id="a9e42-110">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="a9e42-110">EXAMPLES</span></span>

### <span data-ttu-id="a9e42-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="a9e42-111">Example 1</span></span>
```
PS C:\> Remove-AzDataShareSubscription -ResourceGroupName "ADS" -AccountName "WikiAds" -Name "AdsShareSubscription"
Are you sure you want to remove sharesubscription "AdsShareSubscription"? 
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): Y
```

<span data-ttu-id="a9e42-112">Mit diesen Befehlen wird eine ShareSubscription namens AdsShareSubscription aus dem WikiAds-Konto entfernt.</span><span class="sxs-lookup"><span data-stu-id="a9e42-112">This commands removes a sharesubscription named AdsShareSubscription from account WikiAds.</span></span> 

## <span data-ttu-id="a9e42-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="a9e42-113">PARAMETERS</span></span>

### <span data-ttu-id="a9e42-114">-AccountName</span><span class="sxs-lookup"><span data-stu-id="a9e42-114">-AccountName</span></span>
<span data-ttu-id="a9e42-115">Name des Azure-Datenfreigabekontos.</span><span class="sxs-lookup"><span data-stu-id="a9e42-115">Azure data share account name.</span></span>

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

### <span data-ttu-id="a9e42-116">-AsJob</span><span class="sxs-lookup"><span data-stu-id="a9e42-116">-AsJob</span></span>
<span data-ttu-id="a9e42-117">{{Fill AsJob Description}}</span><span class="sxs-lookup"><span data-stu-id="a9e42-117">{{Fill AsJob Description}}</span></span>

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

### <span data-ttu-id="a9e42-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a9e42-118">-DefaultProfile</span></span>
<span data-ttu-id="a9e42-119">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="a9e42-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a9e42-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="a9e42-120">-InputObject</span></span>
<span data-ttu-id="a9e42-121">Abonnementobjekt für azure data share</span><span class="sxs-lookup"><span data-stu-id="a9e42-121">Azure data share subscription object</span></span>


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

### <span data-ttu-id="a9e42-122">-Name</span><span class="sxs-lookup"><span data-stu-id="a9e42-122">-Name</span></span>
<span data-ttu-id="a9e42-123">Name des Azure Data Share-Abonnements</span><span class="sxs-lookup"><span data-stu-id="a9e42-123">Azure data share subscription name</span></span>

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

### <span data-ttu-id="a9e42-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="a9e42-124">-PassThru</span></span>
<span data-ttu-id="a9e42-125">Rückgabeobjekt (sofern angegeben)</span><span class="sxs-lookup"><span data-stu-id="a9e42-125">Return object (if specified).</span></span>

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

### <span data-ttu-id="a9e42-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a9e42-126">-ResourceGroupName</span></span>
<span data-ttu-id="a9e42-127">Der Ressourcengruppenname des Azure Data Share-Kontos</span><span class="sxs-lookup"><span data-stu-id="a9e42-127">The resource group name of the azure data share account</span></span>

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

### <span data-ttu-id="a9e42-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="a9e42-128">-ResourceId</span></span>
<span data-ttu-id="a9e42-129">Die Ressourcen-ID des Azure Data Share-Abonnements</span><span class="sxs-lookup"><span data-stu-id="a9e42-129">The resource id of the azure data share subscription</span></span>

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

### <span data-ttu-id="a9e42-130">-Confirm</span><span class="sxs-lookup"><span data-stu-id="a9e42-130">-Confirm</span></span>
<span data-ttu-id="a9e42-131">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="a9e42-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a9e42-132">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="a9e42-132">-WhatIf</span></span>
<span data-ttu-id="a9e42-133">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="a9e42-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a9e42-134">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="a9e42-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a9e42-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a9e42-135">CommonParameters</span></span>
<span data-ttu-id="a9e42-136">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a9e42-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a9e42-137">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="a9e42-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a9e42-138">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="a9e42-138">INPUTS</span></span>

### <span data-ttu-id="a9e42-139">System.String</span><span class="sxs-lookup"><span data-stu-id="a9e42-139">System.String</span></span>

### <span data-ttu-id="a9e42-140">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareSubscription</span><span class="sxs-lookup"><span data-stu-id="a9e42-140">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareSubscription</span></span>

## <span data-ttu-id="a9e42-141">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="a9e42-141">OUTPUTS</span></span>

### <span data-ttu-id="a9e42-142">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="a9e42-142">System.Boolean</span></span>

## <span data-ttu-id="a9e42-143">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="a9e42-143">NOTES</span></span>

## <span data-ttu-id="a9e42-144">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="a9e42-144">RELATED LINKS</span></span>
