---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StackEdge.dll-Help.xml
Module Name: Az.StackEdge
online version: https://docs.microsoft.com/en-us/powershell/module/az.stackedge/invoke-azstackedgeshare
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/Invoke-AzStackEdgeShare.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/Invoke-AzStackEdgeShare.md
ms.openlocfilehash: 39e695ad33568ca88996428c3e3d972ae693b503
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98302955"
---
# <span data-ttu-id="f00ac-101">Invoke-AzStackEdgeShare</span><span class="sxs-lookup"><span data-stu-id="f00ac-101">Invoke-AzStackEdgeShare</span></span>

## <span data-ttu-id="f00ac-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f00ac-102">SYNOPSIS</span></span>
<span data-ttu-id="f00ac-103">Ruft bestimmte Aktionen für eine Freigabe auf.</span><span class="sxs-lookup"><span data-stu-id="f00ac-103">Invokes specific actions on a share.</span></span>

## <span data-ttu-id="f00ac-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="f00ac-104">SYNTAX</span></span>

### <span data-ttu-id="f00ac-105">InvokeByNameParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="f00ac-105">InvokeByNameParameterSet (Default)</span></span>
```
Invoke-AzStackEdgeShare [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-RefreshData] [-PassThru] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="f00ac-106">InvokeByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="f00ac-106">InvokeByResourceIdParameterSet</span></span>
```
Invoke-AzStackEdgeShare -ResourceId <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-RefreshData]
 [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f00ac-107">InvokeByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="f00ac-107">InvokeByInputObjectParameterSet</span></span>
```
Invoke-AzStackEdgeShare [-AsJob] [-DefaultProfile <IAzureContextContainer>] -InputObject <PSStackEdgeShare>
 [-RefreshData] [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f00ac-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="f00ac-108">DESCRIPTION</span></span>
<span data-ttu-id="f00ac-109">Das **Cmdlet Invoke-AzStackEdgeShare** ruft eine Aktion auf, um Daten auf einer Freigabe auf einem Stack Edge-Gerät zu aktualisieren.</span><span class="sxs-lookup"><span data-stu-id="f00ac-109">The **Invoke-AzStackEdgeShare** cmdlet invokes action to refresh data on a share on a Stack Edge device.</span></span>

## <span data-ttu-id="f00ac-110">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="f00ac-110">EXAMPLES</span></span>

### <span data-ttu-id="f00ac-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="f00ac-111">Example 1</span></span>
```powershell
PS C:\> Invoke-AzStackEdgeShare -ResourceGroupName resourceGroupName -DeviceName deviceName -Name share1 -PassThru
PS C:\> true
```

### <span data-ttu-id="f00ac-112">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="f00ac-112">Example 2</span></span>
```powershell
PS C:\> Invoke-AzStackEdgeShare -ResourceGroupName resourceGroupName -DeviceName deviceName -Name share1 | Invoke-AzStackEdgeShare
```

## <span data-ttu-id="f00ac-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="f00ac-113">PARAMETERS</span></span>

### <span data-ttu-id="f00ac-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="f00ac-114">-AsJob</span></span>
<span data-ttu-id="f00ac-115">Ausführen des Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="f00ac-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="f00ac-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f00ac-116">-DefaultProfile</span></span>
<span data-ttu-id="f00ac-117">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="f00ac-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f00ac-118">-DeviceName</span><span class="sxs-lookup"><span data-stu-id="f00ac-118">-DeviceName</span></span>
<span data-ttu-id="f00ac-119">Gerätename</span><span class="sxs-lookup"><span data-stu-id="f00ac-119">Device Name</span></span>

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

### <span data-ttu-id="f00ac-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="f00ac-120">-InputObject</span></span>
<span data-ttu-id="f00ac-121">Eingabeobjekt</span><span class="sxs-lookup"><span data-stu-id="f00ac-121">Input Object</span></span>

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

### <span data-ttu-id="f00ac-122">-Name</span><span class="sxs-lookup"><span data-stu-id="f00ac-122">-Name</span></span>
<span data-ttu-id="f00ac-123">Ressourcenname</span><span class="sxs-lookup"><span data-stu-id="f00ac-123">Resource Name</span></span>

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

### <span data-ttu-id="f00ac-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="f00ac-124">-PassThru</span></span>
<span data-ttu-id="f00ac-125">gibt "true" zurück, wenn dies erfolgreich ist.</span><span class="sxs-lookup"><span data-stu-id="f00ac-125">returns true if successful</span></span>

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

### <span data-ttu-id="f00ac-126">-RefreshData</span><span class="sxs-lookup"><span data-stu-id="f00ac-126">-RefreshData</span></span>
<span data-ttu-id="f00ac-127">Aktualisieren der Freigabemetadaten mit den Daten aus der Cloud</span><span class="sxs-lookup"><span data-stu-id="f00ac-127">Refresh Share Metadata with the data from the cloud</span></span>

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

### <span data-ttu-id="f00ac-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f00ac-128">-ResourceGroupName</span></span>
<span data-ttu-id="f00ac-129">Ressourcengruppenname</span><span class="sxs-lookup"><span data-stu-id="f00ac-129">Resource Group Name</span></span>

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

### <span data-ttu-id="f00ac-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="f00ac-130">-ResourceId</span></span>
<span data-ttu-id="f00ac-131">Azure ResourceId</span><span class="sxs-lookup"><span data-stu-id="f00ac-131">Azure ResourceId</span></span>

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

### <span data-ttu-id="f00ac-132">-Confirm</span><span class="sxs-lookup"><span data-stu-id="f00ac-132">-Confirm</span></span>
<span data-ttu-id="f00ac-133">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="f00ac-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f00ac-134">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="f00ac-134">-WhatIf</span></span>
<span data-ttu-id="f00ac-135">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="f00ac-135">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="f00ac-136">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="f00ac-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f00ac-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f00ac-137">CommonParameters</span></span>
<span data-ttu-id="f00ac-138">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f00ac-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f00ac-139">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="f00ac-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f00ac-140">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="f00ac-140">INPUTS</span></span>

### <span data-ttu-id="f00ac-141">System.String</span><span class="sxs-lookup"><span data-stu-id="f00ac-141">System.String</span></span>

### <span data-ttu-id="f00ac-142">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeShare</span><span class="sxs-lookup"><span data-stu-id="f00ac-142">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeShare</span></span>

## <span data-ttu-id="f00ac-143">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="f00ac-143">OUTPUTS</span></span>

### <span data-ttu-id="f00ac-144">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="f00ac-144">System.Boolean</span></span>

## <span data-ttu-id="f00ac-145">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="f00ac-145">NOTES</span></span>

## <span data-ttu-id="f00ac-146">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="f00ac-146">RELATED LINKS</span></span>
