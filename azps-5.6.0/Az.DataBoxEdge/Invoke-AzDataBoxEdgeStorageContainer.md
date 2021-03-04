---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.dll-Help.xml
Module Name: Az.DataBoxEdge
online version: https://docs.microsoft.com/powershell/module/az.databoxedge/invoke-azdataboxedgestoragecontainer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBoxEdge/DataBoxEdge/help/Invoke-AzDataBoxEdgeStorageContainer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBoxEdge/DataBoxEdge/help/Invoke-AzDataBoxEdgeStorageContainer.md
ms.openlocfilehash: f6607f59e2cc29557c41bf07014c3604fdb1bf47
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101942627"
---
# <span data-ttu-id="a3941-101">Invoke-AzDataBoxEdgeStorageContainer</span><span class="sxs-lookup"><span data-stu-id="a3941-101">Invoke-AzDataBoxEdgeStorageContainer</span></span>

## <span data-ttu-id="a3941-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a3941-102">SYNOPSIS</span></span>
<span data-ttu-id="a3941-103">Aufruf bestimmter Aktionen für einen Speichercontainer</span><span class="sxs-lookup"><span data-stu-id="a3941-103">Invokes specific actions on a storage container</span></span>

## <span data-ttu-id="a3941-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="a3941-104">SYNTAX</span></span>

### <span data-ttu-id="a3941-105">InvokeByNameParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="a3941-105">InvokeByNameParameterSet (Default)</span></span>
```
Invoke-AzDataBoxEdgeStorageContainer [-ResourceGroupName] <String> [-DeviceName] <String>
 [-EdgeStorageAccountName] <String> [-Name] <String> [-RefreshData] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a3941-106">InvokeByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="a3941-106">InvokeByResourceIdParameterSet</span></span>
```
Invoke-AzDataBoxEdgeStorageContainer [-ResourceId] <String> [-RefreshData] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a3941-107">InvokeByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="a3941-107">InvokeByInputObjectParameterSet</span></span>
```
Invoke-AzDataBoxEdgeStorageContainer [-RefreshData] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 -InputObject <PSDataBoxEdgeStorageContainer> [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a3941-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="a3941-108">DESCRIPTION</span></span>
<span data-ttu-id="a3941-109">Das **Cmdlet Invoke-AzDataBoxEdgeStorageContainer** ruft Aktionen auf, um die Daten in einem Speichercontainer auf einem Data Box Edge-Gerät zu aktualisieren.</span><span class="sxs-lookup"><span data-stu-id="a3941-109">The **Invoke-AzDataBoxEdgeStorageContainer** cmdlet invokes actions to refresh the data on a storage container on a Data Box Edge device.</span></span> 

## <span data-ttu-id="a3941-110">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="a3941-110">EXAMPLES</span></span>

### <span data-ttu-id="a3941-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="a3941-111">Example 1</span></span>
```powershell
PS C:\> Invoke-AzDataBoxEdgeStorageContainer -ResourceGroupName resourceGroupName -DeviceName deviceName -EdgeStorageAccountName edgestorageaccount1 -Name container1 -PassThru
PS C:\> true
```

### <span data-ttu-id="a3941-112">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="a3941-112">Example 2</span></span>
```powershell
PS C:\> Get-AzDataBoxEdgeStorageContainer -ResourceGroupName resourceGroupName -DeviceName deviceName -EdgeStorageAccountName edgestorageaccount1 -Name container1 | Invoke-AzDataBoxEdgeStorageContainer
```

## <span data-ttu-id="a3941-113">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="a3941-113">PARAMETERS</span></span>

### <span data-ttu-id="a3941-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="a3941-114">-AsJob</span></span>
<span data-ttu-id="a3941-115">Ausführen des Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="a3941-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="a3941-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a3941-116">-DefaultProfile</span></span>
<span data-ttu-id="a3941-117">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="a3941-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a3941-118">-DeviceName</span><span class="sxs-lookup"><span data-stu-id="a3941-118">-DeviceName</span></span>
<span data-ttu-id="a3941-119">Gerätename</span><span class="sxs-lookup"><span data-stu-id="a3941-119">Device Name</span></span>

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

### <span data-ttu-id="a3941-120">-EdgeStorageAccountName</span><span class="sxs-lookup"><span data-stu-id="a3941-120">-EdgeStorageAccountName</span></span>
<span data-ttu-id="a3941-121">Ressourcenname</span><span class="sxs-lookup"><span data-stu-id="a3941-121">Resource Name</span></span>

```yaml
Type: System.String
Parameter Sets: InvokeByNameParameterSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a3941-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="a3941-122">-InputObject</span></span>
<span data-ttu-id="a3941-123">Bereitstellen eines vorhandenen EdgeStorageAccount-Objekts</span><span class="sxs-lookup"><span data-stu-id="a3941-123">Provide existing EdgeStorageAccount Object</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeStorageContainer
Parameter Sets: InvokeByInputObjectParameterSet
Aliases: EdgeContainer

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a3941-124">-Name</span><span class="sxs-lookup"><span data-stu-id="a3941-124">-Name</span></span>
<span data-ttu-id="a3941-125">Ressourcenname</span><span class="sxs-lookup"><span data-stu-id="a3941-125">Resource Name</span></span>

```yaml
Type: System.String
Parameter Sets: InvokeByNameParameterSet
Aliases: EdgeContainerName

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a3941-126">-PassThru</span><span class="sxs-lookup"><span data-stu-id="a3941-126">-PassThru</span></span>
<span data-ttu-id="a3941-127">gibt "true" zurück, wenn dies erfolgreich ist</span><span class="sxs-lookup"><span data-stu-id="a3941-127">returns true if successful</span></span>

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

### <span data-ttu-id="a3941-128">-RefreshData</span><span class="sxs-lookup"><span data-stu-id="a3941-128">-RefreshData</span></span>
<span data-ttu-id="a3941-129">Aktualisieren von Containermetadaten mit den Daten aus der Cloud</span><span class="sxs-lookup"><span data-stu-id="a3941-129">Refresh Container Metadata with the data from the cloud</span></span>

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

### <span data-ttu-id="a3941-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a3941-130">-ResourceGroupName</span></span>
<span data-ttu-id="a3941-131">Ressourcengruppenname</span><span class="sxs-lookup"><span data-stu-id="a3941-131">Resource Group Name</span></span>

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

### <span data-ttu-id="a3941-132">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="a3941-132">-ResourceId</span></span>
<span data-ttu-id="a3941-133">Azure ResourceId</span><span class="sxs-lookup"><span data-stu-id="a3941-133">Azure ResourceId</span></span>

```yaml
Type: System.String
Parameter Sets: InvokeByResourceIdParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a3941-134">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="a3941-134">-Confirm</span></span>
<span data-ttu-id="a3941-135">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="a3941-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a3941-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a3941-136">-WhatIf</span></span>
<span data-ttu-id="a3941-137">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="a3941-137">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="a3941-138">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="a3941-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a3941-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a3941-139">CommonParameters</span></span>
<span data-ttu-id="a3941-140">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a3941-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a3941-141">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="a3941-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a3941-142">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="a3941-142">INPUTS</span></span>

### <span data-ttu-id="a3941-143">System.String</span><span class="sxs-lookup"><span data-stu-id="a3941-143">System.String</span></span>

### <span data-ttu-id="a3941-144">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeStorageContainer</span><span class="sxs-lookup"><span data-stu-id="a3941-144">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeStorageContainer</span></span>

## <span data-ttu-id="a3941-145">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="a3941-145">OUTPUTS</span></span>

### <span data-ttu-id="a3941-146">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeStorageContainer</span><span class="sxs-lookup"><span data-stu-id="a3941-146">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeStorageContainer</span></span>

## <span data-ttu-id="a3941-147">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="a3941-147">NOTES</span></span>

## <span data-ttu-id="a3941-148">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="a3941-148">RELATED LINKS</span></span>
