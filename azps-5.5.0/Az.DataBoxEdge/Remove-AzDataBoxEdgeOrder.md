---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.dll-Help.xml
Module Name: Az.DataBoxEdge
online version: https://docs.microsoft.com/en-us/powershell/module/az.databoxedge/remove-azdataboxedgeorder
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBoxEdge/DataBoxEdge/help/Remove-AzDataBoxEdgeOrder.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBoxEdge/DataBoxEdge/help/Remove-AzDataBoxEdgeOrder.md
ms.openlocfilehash: 84e17ac36e446d784715c2de38944f7b44d1337d
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100148305"
---
# <span data-ttu-id="8f966-101">Remove-AzDataBoxEdgeOrder</span><span class="sxs-lookup"><span data-stu-id="8f966-101">Remove-AzDataBoxEdgeOrder</span></span>

## <span data-ttu-id="8f966-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8f966-102">SYNOPSIS</span></span>
<span data-ttu-id="8f966-103">Entfernt die Bestellung für ein Gerät.</span><span class="sxs-lookup"><span data-stu-id="8f966-103">Removes the order for a device.</span></span>

## <span data-ttu-id="8f966-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="8f966-104">SYNTAX</span></span>

### <span data-ttu-id="8f966-105">DeleteByNameParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="8f966-105">DeleteByNameParameterSet (Default)</span></span>
```
Remove-AzDataBoxEdgeOrder [-ResourceGroupName] <String> [-DeviceName] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8f966-106">DeleteByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="8f966-106">DeleteByResourceIdParameterSet</span></span>
```
Remove-AzDataBoxEdgeOrder -ResourceId <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-PassThru]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8f966-107">DeleteByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="8f966-107">DeleteByInputObjectParameterSet</span></span>
```
Remove-AzDataBoxEdgeOrder -InputObject <PSDataBoxEdgeOrder> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8f966-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="8f966-108">DESCRIPTION</span></span>
<span data-ttu-id="8f966-109">Das **Cmdlet "Remove-AzDataBoxEdgeOrder"** löscht eine vorhandene Bestellung für ein Datenfeld-Edgegerät.</span><span class="sxs-lookup"><span data-stu-id="8f966-109">The **Remove-AzDataBoxEdgeOrder** cmdlet deletes an existing order for a Data Box Edge device.</span></span>

## <span data-ttu-id="8f966-110">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="8f966-110">EXAMPLES</span></span>

### <span data-ttu-id="8f966-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="8f966-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzDataBoxEdgeOrder -ResourceGroupName resourceGroupName -DeviceName deviceName
```

## <span data-ttu-id="8f966-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="8f966-112">PARAMETERS</span></span>

### <span data-ttu-id="8f966-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="8f966-113">-AsJob</span></span>
<span data-ttu-id="8f966-114">Ausführen des Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="8f966-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="8f966-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8f966-115">-DefaultProfile</span></span>
<span data-ttu-id="8f966-116">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="8f966-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8f966-117">-DeviceName</span><span class="sxs-lookup"><span data-stu-id="8f966-117">-DeviceName</span></span>
<span data-ttu-id="8f966-118">Gerätename</span><span class="sxs-lookup"><span data-stu-id="8f966-118">Device Name</span></span>

```yaml
Type: System.String
Parameter Sets: DeleteByNameParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8f966-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="8f966-119">-InputObject</span></span>
<span data-ttu-id="8f966-120">Eingabeobjekt</span><span class="sxs-lookup"><span data-stu-id="8f966-120">Input Object</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeOrder
Parameter Sets: DeleteByInputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="8f966-121">-PassThru</span><span class="sxs-lookup"><span data-stu-id="8f966-121">-PassThru</span></span>
<span data-ttu-id="8f966-122">gibt "true" zurück, wenn dies erfolgreich ist.</span><span class="sxs-lookup"><span data-stu-id="8f966-122">returns true if successful</span></span>

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

### <span data-ttu-id="8f966-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8f966-123">-ResourceGroupName</span></span>
<span data-ttu-id="8f966-124">Ressourcengruppenname</span><span class="sxs-lookup"><span data-stu-id="8f966-124">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: DeleteByNameParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8f966-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="8f966-125">-ResourceId</span></span>
<span data-ttu-id="8f966-126">Azure ResourceId</span><span class="sxs-lookup"><span data-stu-id="8f966-126">Azure ResourceId</span></span>

```yaml
Type: System.String
Parameter Sets: DeleteByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8f966-127">-Confirm</span><span class="sxs-lookup"><span data-stu-id="8f966-127">-Confirm</span></span>
<span data-ttu-id="8f966-128">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="8f966-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8f966-129">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="8f966-129">-WhatIf</span></span>
<span data-ttu-id="8f966-130">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="8f966-130">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="8f966-131">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="8f966-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8f966-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8f966-132">CommonParameters</span></span>
<span data-ttu-id="8f966-133">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8f966-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8f966-134">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="8f966-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8f966-135">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="8f966-135">INPUTS</span></span>

### <span data-ttu-id="8f966-136">System.String</span><span class="sxs-lookup"><span data-stu-id="8f966-136">System.String</span></span>

### <span data-ttu-id="8f966-137">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeOrder</span><span class="sxs-lookup"><span data-stu-id="8f966-137">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeOrder</span></span>

## <span data-ttu-id="8f966-138">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="8f966-138">OUTPUTS</span></span>

### <span data-ttu-id="8f966-139">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeOrder</span><span class="sxs-lookup"><span data-stu-id="8f966-139">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeOrder</span></span>

## <span data-ttu-id="8f966-140">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="8f966-140">NOTES</span></span>

## <span data-ttu-id="8f966-141">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="8f966-141">RELATED LINKS</span></span>
