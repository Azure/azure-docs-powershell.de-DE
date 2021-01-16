---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataShare.dll-Help.xml
Module Name: Az.DataShare
online version: https://docs.microsoft.com/en-us/powershell/module/az.datashare/remove-azdatasharedatasetmapping
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Remove-AzDataShareDataSetMapping.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Remove-AzDataShareDataSetMapping.md
ms.openlocfilehash: 16b212a0c5549f74b56e8c80be8d949a025ecb24
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98377123"
---
# <span data-ttu-id="d2676-101">Remove-AzDataShareDataSetMapping</span><span class="sxs-lookup"><span data-stu-id="d2676-101">Remove-AzDataShareDataSetMapping</span></span>

## <span data-ttu-id="d2676-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d2676-102">SYNOPSIS</span></span>
<span data-ttu-id="d2676-103">Entfernt eine Datasetzuordnung</span><span class="sxs-lookup"><span data-stu-id="d2676-103">Removes a dataset mapping</span></span>

## <span data-ttu-id="d2676-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="d2676-104">SYNTAX</span></span>

### <span data-ttu-id="d2676-105">ByFieldsParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="d2676-105">ByFieldsParameterSet (Default)</span></span>
```
Remove-AzDataShareDataSetMapping -ResourceGroupName <String> -AccountName <String>
 -ShareSubscriptionName <String> -Name <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d2676-106">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="d2676-106">ByResourceIdParameterSet</span></span>
```
Remove-AzDataShareDataSetMapping -ResourceId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d2676-107">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="d2676-107">ByObjectParameterSet</span></span>
```
Remove-AzDataShareDataSetMapping -InputObject <PSDataShareDataSetMapping> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d2676-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="d2676-108">DESCRIPTION</span></span>
<span data-ttu-id="d2676-109">Das **Cmdlet "Remove-AzDataShareDataSetMapping"** entfernt Datasetzuordnungen.</span><span class="sxs-lookup"><span data-stu-id="d2676-109">The **Remove-AzDataShareDataSetMapping** cmdlet removes a dataset mappings.</span></span>

## <span data-ttu-id="d2676-110">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="d2676-110">EXAMPLES</span></span>

### <span data-ttu-id="d2676-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="d2676-111">Example 1</span></span>
```
PS C:\> Remove-AzDataShareDataSetMapping -ResourceGroupName "ADS" -AccountName "WikiAds" -ShareSubscriptionName "AdsShareSubscription" -Name "DSM"
Are you sure you want to remove dataset mapping "DSM"? 
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): Y
```

<span data-ttu-id="d2676-112">Mit diesen Befehlen wird das Dataset namens DSM aus sharesubscription WikiAds entfernt.</span><span class="sxs-lookup"><span data-stu-id="d2676-112">This commands removes the dataset named DSM from sharesubscription WikiAds.</span></span> 

## <span data-ttu-id="d2676-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="d2676-113">PARAMETERS</span></span>

### <span data-ttu-id="d2676-114">-AccountName</span><span class="sxs-lookup"><span data-stu-id="d2676-114">-AccountName</span></span>
<span data-ttu-id="d2676-115">Name des Azure-Datenfreigabekontos</span><span class="sxs-lookup"><span data-stu-id="d2676-115">Azure data share account name</span></span>

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

### <span data-ttu-id="d2676-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d2676-116">-DefaultProfile</span></span>
<span data-ttu-id="d2676-117">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="d2676-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d2676-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="d2676-118">-InputObject</span></span>
<span data-ttu-id="d2676-119">Das Zuordnungsobjekt für azure-Datensets</span><span class="sxs-lookup"><span data-stu-id="d2676-119">The azure data set mapping object</span></span>


```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareDataSetMapping
Parameter Sets: ByObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d2676-120">-Name</span><span class="sxs-lookup"><span data-stu-id="d2676-120">-Name</span></span>
<span data-ttu-id="d2676-121">Name der Zuordnung von Azure-Datensets</span><span class="sxs-lookup"><span data-stu-id="d2676-121">Azure data set mapping name</span></span>

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

### <span data-ttu-id="d2676-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="d2676-122">-PassThru</span></span>
<span data-ttu-id="d2676-123">Rückgabeobjekt (sofern angegeben)</span><span class="sxs-lookup"><span data-stu-id="d2676-123">Return object (if specified).</span></span>

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

### <span data-ttu-id="d2676-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d2676-124">-ResourceGroupName</span></span>
<span data-ttu-id="d2676-125">Der Ressourcengruppenname des Azure Data Share-Kontos</span><span class="sxs-lookup"><span data-stu-id="d2676-125">The resource group name of the azure data share account</span></span>

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

### <span data-ttu-id="d2676-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="d2676-126">-ResourceId</span></span>
<span data-ttu-id="d2676-127">Die Ressourcen-ID der Azure-Datensetzuordnung</span><span class="sxs-lookup"><span data-stu-id="d2676-127">The resource id of the azure data set mapping</span></span>

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

### <span data-ttu-id="d2676-128">-ShareSubscriptionName</span><span class="sxs-lookup"><span data-stu-id="d2676-128">-ShareSubscriptionName</span></span>
<span data-ttu-id="d2676-129">Name des Azure Data Share-Abonnements</span><span class="sxs-lookup"><span data-stu-id="d2676-129">Azure data share subscription name</span></span>

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

### <span data-ttu-id="d2676-130">-Confirm</span><span class="sxs-lookup"><span data-stu-id="d2676-130">-Confirm</span></span>
<span data-ttu-id="d2676-131">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="d2676-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d2676-132">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="d2676-132">-WhatIf</span></span>
<span data-ttu-id="d2676-133">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="d2676-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d2676-134">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="d2676-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d2676-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d2676-135">CommonParameters</span></span>
<span data-ttu-id="d2676-136">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d2676-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d2676-137">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="d2676-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d2676-138">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="d2676-138">INPUTS</span></span>

### <span data-ttu-id="d2676-139">System.String</span><span class="sxs-lookup"><span data-stu-id="d2676-139">System.String</span></span>

### <span data-ttu-id="d2676-140">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareDataSetMapping</span><span class="sxs-lookup"><span data-stu-id="d2676-140">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareDataSetMapping</span></span>

## <span data-ttu-id="d2676-141">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="d2676-141">OUTPUTS</span></span>

### <span data-ttu-id="d2676-142">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="d2676-142">System.Boolean</span></span>

## <span data-ttu-id="d2676-143">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="d2676-143">NOTES</span></span>

## <span data-ttu-id="d2676-144">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="d2676-144">RELATED LINKS</span></span>
