---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataShare.dll-Help.xml
Module Name: Az.DataShare
online version: https://docs.microsoft.com/en-us/powershell/module/az.datashare/remove-azdatasharedataset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Remove-AzDataShareDataSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Remove-AzDataShareDataSet.md
ms.openlocfilehash: c3d5105fc3b43a3f6b7ff8b45c5ba8236fed656b
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98377150"
---
# <span data-ttu-id="ee8c5-101">Remove-AzDataShareDataSet</span><span class="sxs-lookup"><span data-stu-id="ee8c5-101">Remove-AzDataShareDataSet</span></span>

## <span data-ttu-id="ee8c5-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ee8c5-102">SYNOPSIS</span></span>
<span data-ttu-id="ee8c5-103">Entfernt eine Datasetzuordnung</span><span class="sxs-lookup"><span data-stu-id="ee8c5-103">Removes a dataset mapping</span></span>

## <span data-ttu-id="ee8c5-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="ee8c5-104">SYNTAX</span></span>

### <span data-ttu-id="ee8c5-105">ByFieldsParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="ee8c5-105">ByFieldsParameterSet (Default)</span></span>
```
Remove-AzDataShareDataSet -ResourceGroupName <String> -AccountName <String> -ShareName <String> -Name <String>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ee8c5-106">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="ee8c5-106">ByResourceIdParameterSet</span></span>
```
Remove-AzDataShareDataSet -ResourceId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ee8c5-107">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="ee8c5-107">ByObjectParameterSet</span></span>
```
Remove-AzDataShareDataSet -InputObject <PSDataShareDataSet> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ee8c5-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="ee8c5-108">DESCRIPTION</span></span>
<span data-ttu-id="ee8c5-109">Das **Cmdlet "Remove-AzDataShareDataSet"** entfernt ein Dataset.</span><span class="sxs-lookup"><span data-stu-id="ee8c5-109">The **Remove-AzDataShareDataSet** cmdlet removes a dataset.</span></span>

## <span data-ttu-id="ee8c5-110">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="ee8c5-110">EXAMPLES</span></span>

### <span data-ttu-id="ee8c5-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="ee8c5-111">Example 1</span></span>
```
PS C:\> Remove-AzDataShareDataSet -ResourceGroupName "ADS" -AccountName "WikiAds" -ShareName "AdsShare" -Name "DS"
Are you sure you want to remove dataset mapping "DS"? 
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): Y
```

<span data-ttu-id="ee8c5-112">Mit diesen Befehlen wird das Dataset namens DS aus "WikiAds teilen" entfernt.</span><span class="sxs-lookup"><span data-stu-id="ee8c5-112">This commands removes the dataset named DS from share WikiAds.</span></span> 

## <span data-ttu-id="ee8c5-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="ee8c5-113">PARAMETERS</span></span>

### <span data-ttu-id="ee8c5-114">-AccountName</span><span class="sxs-lookup"><span data-stu-id="ee8c5-114">-AccountName</span></span>
<span data-ttu-id="ee8c5-115">Name des Azure-Datenfreigabekontos.</span><span class="sxs-lookup"><span data-stu-id="ee8c5-115">Azure data share account name.</span></span>

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

### <span data-ttu-id="ee8c5-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ee8c5-116">-DefaultProfile</span></span>
<span data-ttu-id="ee8c5-117">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="ee8c5-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ee8c5-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="ee8c5-118">-InputObject</span></span>
<span data-ttu-id="ee8c5-119">Das Azure-Datenset-Objekt.</span><span class="sxs-lookup"><span data-stu-id="ee8c5-119">The azure data set object.</span></span>


```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareDataSet
Parameter Sets: ByObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ee8c5-120">-Name</span><span class="sxs-lookup"><span data-stu-id="ee8c5-120">-Name</span></span>
<span data-ttu-id="ee8c5-121">Name des Azure-Datensets.</span><span class="sxs-lookup"><span data-stu-id="ee8c5-121">Azure data set name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ee8c5-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="ee8c5-122">-PassThru</span></span>
<span data-ttu-id="ee8c5-123">Rückgabeobjekt (sofern angegeben)</span><span class="sxs-lookup"><span data-stu-id="ee8c5-123">Return object (if specified).</span></span>

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

### <span data-ttu-id="ee8c5-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ee8c5-124">-ResourceGroupName</span></span>
<span data-ttu-id="ee8c5-125">Der Ressourcengruppenname des Azure Data Share-Kontos.</span><span class="sxs-lookup"><span data-stu-id="ee8c5-125">The resource group name of the azure data share account.</span></span>

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

### <span data-ttu-id="ee8c5-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="ee8c5-126">-ResourceId</span></span>
<span data-ttu-id="ee8c5-127">Die Ressourcen-ID des Azure-Datensets.</span><span class="sxs-lookup"><span data-stu-id="ee8c5-127">The resource id of the azure data set.</span></span>

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

### <span data-ttu-id="ee8c5-128">-ShareName</span><span class="sxs-lookup"><span data-stu-id="ee8c5-128">-ShareName</span></span>
<span data-ttu-id="ee8c5-129">Name der Azure-Datenfreigabe.</span><span class="sxs-lookup"><span data-stu-id="ee8c5-129">Azure data share name.</span></span>

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

### <span data-ttu-id="ee8c5-130">-Confirm</span><span class="sxs-lookup"><span data-stu-id="ee8c5-130">-Confirm</span></span>
<span data-ttu-id="ee8c5-131">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="ee8c5-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ee8c5-132">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="ee8c5-132">-WhatIf</span></span>
<span data-ttu-id="ee8c5-133">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="ee8c5-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ee8c5-134">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="ee8c5-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ee8c5-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ee8c5-135">CommonParameters</span></span>
<span data-ttu-id="ee8c5-136">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ee8c5-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ee8c5-137">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="ee8c5-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ee8c5-138">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="ee8c5-138">INPUTS</span></span>

### <span data-ttu-id="ee8c5-139">System.String</span><span class="sxs-lookup"><span data-stu-id="ee8c5-139">System.String</span></span>

### <span data-ttu-id="ee8c5-140">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareDataSet</span><span class="sxs-lookup"><span data-stu-id="ee8c5-140">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareDataSet</span></span>

## <span data-ttu-id="ee8c5-141">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="ee8c5-141">OUTPUTS</span></span>

### <span data-ttu-id="ee8c5-142">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="ee8c5-142">System.Boolean</span></span>

## <span data-ttu-id="ee8c5-143">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="ee8c5-143">NOTES</span></span>

## <span data-ttu-id="ee8c5-144">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="ee8c5-144">RELATED LINKS</span></span>
