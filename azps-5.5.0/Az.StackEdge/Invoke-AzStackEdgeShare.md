---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StackEdge.dll-Help.xml
Module Name: Az.StackEdge
online version: https://docs.microsoft.com/en-us/powershell/module/az.stackedge/invoke-azstackedgeshare
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/Invoke-AzStackEdgeShare.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/Invoke-AzStackEdgeShare.md
ms.openlocfilehash: 39e695ad33568ca88996428c3e3d972ae693b503
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100155121"
---
# <span data-ttu-id="43411-101">Invoke-AzStackEdgeShare</span><span class="sxs-lookup"><span data-stu-id="43411-101">Invoke-AzStackEdgeShare</span></span>

## <span data-ttu-id="43411-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="43411-102">SYNOPSIS</span></span>
<span data-ttu-id="43411-103">Ruft bestimmte Aktionen für eine Freigabe auf.</span><span class="sxs-lookup"><span data-stu-id="43411-103">Invokes specific actions on a share.</span></span>

## <span data-ttu-id="43411-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="43411-104">SYNTAX</span></span>

### <span data-ttu-id="43411-105">InvokeByNameParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="43411-105">InvokeByNameParameterSet (Default)</span></span>
```
Invoke-AzStackEdgeShare [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-RefreshData] [-PassThru] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="43411-106">InvokeByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="43411-106">InvokeByResourceIdParameterSet</span></span>
```
Invoke-AzStackEdgeShare -ResourceId <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-RefreshData]
 [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="43411-107">InvokeByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="43411-107">InvokeByInputObjectParameterSet</span></span>
```
Invoke-AzStackEdgeShare [-AsJob] [-DefaultProfile <IAzureContextContainer>] -InputObject <PSStackEdgeShare>
 [-RefreshData] [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="43411-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="43411-108">DESCRIPTION</span></span>
<span data-ttu-id="43411-109">Das **Cmdlet Invoke-AzStackEdgeShare** ruft eine Aktion auf, um Daten auf einer Freigabe auf einem Stack Edge-Gerät zu aktualisieren.</span><span class="sxs-lookup"><span data-stu-id="43411-109">The **Invoke-AzStackEdgeShare** cmdlet invokes action to refresh data on a share on a Stack Edge device.</span></span>

## <span data-ttu-id="43411-110">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="43411-110">EXAMPLES</span></span>

### <span data-ttu-id="43411-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="43411-111">Example 1</span></span>
```powershell
PS C:\> Invoke-AzStackEdgeShare -ResourceGroupName resourceGroupName -DeviceName deviceName -Name share1 -PassThru
PS C:\> true
```

### <span data-ttu-id="43411-112">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="43411-112">Example 2</span></span>
```powershell
PS C:\> Invoke-AzStackEdgeShare -ResourceGroupName resourceGroupName -DeviceName deviceName -Name share1 | Invoke-AzStackEdgeShare
```

## <span data-ttu-id="43411-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="43411-113">PARAMETERS</span></span>

### <span data-ttu-id="43411-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="43411-114">-AsJob</span></span>
<span data-ttu-id="43411-115">Ausführen des Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="43411-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="43411-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="43411-116">-DefaultProfile</span></span>
<span data-ttu-id="43411-117">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="43411-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="43411-118">-DeviceName</span><span class="sxs-lookup"><span data-stu-id="43411-118">-DeviceName</span></span>
<span data-ttu-id="43411-119">Gerätename</span><span class="sxs-lookup"><span data-stu-id="43411-119">Device Name</span></span>

```yaml
Type: System.String
Parameter Sets: InvokeByNameParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="43411-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="43411-120">-InputObject</span></span>
<span data-ttu-id="43411-121">Eingabeobjekt</span><span class="sxs-lookup"><span data-stu-id="43411-121">Input Object</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeShare
Parameter Sets: InvokeByInputObjectParameterSet
Aliases: EdgeShare

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="43411-122">-Name</span><span class="sxs-lookup"><span data-stu-id="43411-122">-Name</span></span>
<span data-ttu-id="43411-123">Ressourcenname</span><span class="sxs-lookup"><span data-stu-id="43411-123">Resource Name</span></span>

```yaml
Type: System.String
Parameter Sets: InvokeByNameParameterSet
Aliases: EdgeShareName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="43411-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="43411-124">-PassThru</span></span>
<span data-ttu-id="43411-125">gibt "true" zurück, wenn dies erfolgreich ist.</span><span class="sxs-lookup"><span data-stu-id="43411-125">returns true if successful</span></span>

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

### <span data-ttu-id="43411-126">-RefreshData</span><span class="sxs-lookup"><span data-stu-id="43411-126">-RefreshData</span></span>
<span data-ttu-id="43411-127">Aktualisieren der Freigabemetadaten mit den Daten aus der Cloud</span><span class="sxs-lookup"><span data-stu-id="43411-127">Refresh Share Metadata with the data from the cloud</span></span>

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

### <span data-ttu-id="43411-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="43411-128">-ResourceGroupName</span></span>
<span data-ttu-id="43411-129">Ressourcengruppenname</span><span class="sxs-lookup"><span data-stu-id="43411-129">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: InvokeByNameParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="43411-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="43411-130">-ResourceId</span></span>
<span data-ttu-id="43411-131">Azure ResourceId</span><span class="sxs-lookup"><span data-stu-id="43411-131">Azure ResourceId</span></span>

```yaml
Type: System.String
Parameter Sets: InvokeByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="43411-132">-Confirm</span><span class="sxs-lookup"><span data-stu-id="43411-132">-Confirm</span></span>
<span data-ttu-id="43411-133">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="43411-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="43411-134">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="43411-134">-WhatIf</span></span>
<span data-ttu-id="43411-135">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="43411-135">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="43411-136">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="43411-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="43411-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="43411-137">CommonParameters</span></span>
<span data-ttu-id="43411-138">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="43411-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="43411-139">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="43411-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="43411-140">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="43411-140">INPUTS</span></span>

### <span data-ttu-id="43411-141">System.String</span><span class="sxs-lookup"><span data-stu-id="43411-141">System.String</span></span>

### <span data-ttu-id="43411-142">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeShare</span><span class="sxs-lookup"><span data-stu-id="43411-142">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeShare</span></span>

## <span data-ttu-id="43411-143">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="43411-143">OUTPUTS</span></span>

### <span data-ttu-id="43411-144">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="43411-144">System.Boolean</span></span>

## <span data-ttu-id="43411-145">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="43411-145">NOTES</span></span>

## <span data-ttu-id="43411-146">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="43411-146">RELATED LINKS</span></span>
