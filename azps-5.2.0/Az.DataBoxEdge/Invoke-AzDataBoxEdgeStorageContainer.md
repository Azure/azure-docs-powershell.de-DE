---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.dll-Help.xml
Module Name: Az.DataBoxEdge
online version: https://docs.microsoft.com/en-us/powershell/module/az.databoxedge/invoke-azdataboxedgestoragecontainer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBoxEdge/DataBoxEdge/help/Invoke-AzDataBoxEdgeStorageContainer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBoxEdge/DataBoxEdge/help/Invoke-AzDataBoxEdgeStorageContainer.md
ms.openlocfilehash: f897c2adfe4154aeff5bd370437ea8b23e4efd36
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98360491"
---
# <span data-ttu-id="22cb5-101">Invoke-AzDataBoxEdgeStorageContainer</span><span class="sxs-lookup"><span data-stu-id="22cb5-101">Invoke-AzDataBoxEdgeStorageContainer</span></span>

## <span data-ttu-id="22cb5-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="22cb5-102">SYNOPSIS</span></span>
<span data-ttu-id="22cb5-103">Aufruf bestimmter Aktionen für einen Speichercontainer</span><span class="sxs-lookup"><span data-stu-id="22cb5-103">Invokes specific actions on a storage container</span></span>

## <span data-ttu-id="22cb5-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="22cb5-104">SYNTAX</span></span>

### <span data-ttu-id="22cb5-105">InvokeByNameParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="22cb5-105">InvokeByNameParameterSet (Default)</span></span>
```
Invoke-AzDataBoxEdgeStorageContainer [-ResourceGroupName] <String> [-DeviceName] <String>
 [-EdgeStorageAccountName] <String> [-Name] <String> [-RefreshData] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="22cb5-106">InvokeByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="22cb5-106">InvokeByResourceIdParameterSet</span></span>
```
Invoke-AzDataBoxEdgeStorageContainer [-ResourceId] <String> [-RefreshData] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="22cb5-107">InvokeByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="22cb5-107">InvokeByInputObjectParameterSet</span></span>
```
Invoke-AzDataBoxEdgeStorageContainer [-RefreshData] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 -InputObject <PSDataBoxEdgeStorageContainer> [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="22cb5-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="22cb5-108">DESCRIPTION</span></span>
<span data-ttu-id="22cb5-109">Das **Cmdlet Invoke-AzDataBoxEdgeStorageContainer** ruft Aktionen auf, um die Daten in einem Speichercontainer auf einem Data Box Edgegerät zu aktualisieren.</span><span class="sxs-lookup"><span data-stu-id="22cb5-109">The **Invoke-AzDataBoxEdgeStorageContainer** cmdlet invokes actions to refresh the data on a storage container on a Data Box Edge device.</span></span> 

## <span data-ttu-id="22cb5-110">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="22cb5-110">EXAMPLES</span></span>

### <span data-ttu-id="22cb5-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="22cb5-111">Example 1</span></span>
```powershell
PS C:\> Invoke-AzDataBoxEdgeStorageContainer -ResourceGroupName resourceGroupName -DeviceName deviceName -EdgeStorageAccountName edgestorageaccount1 -Name container1 -PassThru
PS C:\> true
```

### <span data-ttu-id="22cb5-112">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="22cb5-112">Example 2</span></span>
```powershell
PS C:\> Get-AzDataBoxEdgeStorageContainer -ResourceGroupName resourceGroupName -DeviceName deviceName -EdgeStorageAccountName edgestorageaccount1 -Name container1 | Invoke-AzDataBoxEdgeStorageContainer
```

## <span data-ttu-id="22cb5-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="22cb5-113">PARAMETERS</span></span>

### <span data-ttu-id="22cb5-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="22cb5-114">-AsJob</span></span>
<span data-ttu-id="22cb5-115">Ausführen des Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="22cb5-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="22cb5-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="22cb5-116">-DefaultProfile</span></span>
<span data-ttu-id="22cb5-117">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="22cb5-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="22cb5-118">-DeviceName</span><span class="sxs-lookup"><span data-stu-id="22cb5-118">-DeviceName</span></span>
<span data-ttu-id="22cb5-119">Gerätename</span><span class="sxs-lookup"><span data-stu-id="22cb5-119">Device Name</span></span>

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

### <span data-ttu-id="22cb5-120">-EdgeStorageAccountName</span><span class="sxs-lookup"><span data-stu-id="22cb5-120">-EdgeStorageAccountName</span></span>
<span data-ttu-id="22cb5-121">Ressourcenname</span><span class="sxs-lookup"><span data-stu-id="22cb5-121">Resource Name</span></span>

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

### <span data-ttu-id="22cb5-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="22cb5-122">-InputObject</span></span>
<span data-ttu-id="22cb5-123">Bereitstellen eines vorhandenen EdgeStorageAccount-Objekts</span><span class="sxs-lookup"><span data-stu-id="22cb5-123">Provide existing EdgeStorageAccount Object</span></span>

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

### <span data-ttu-id="22cb5-124">-Name</span><span class="sxs-lookup"><span data-stu-id="22cb5-124">-Name</span></span>
<span data-ttu-id="22cb5-125">Ressourcenname</span><span class="sxs-lookup"><span data-stu-id="22cb5-125">Resource Name</span></span>

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

### <span data-ttu-id="22cb5-126">-PassThru</span><span class="sxs-lookup"><span data-stu-id="22cb5-126">-PassThru</span></span>
<span data-ttu-id="22cb5-127">gibt "true" zurück, wenn dies erfolgreich ist.</span><span class="sxs-lookup"><span data-stu-id="22cb5-127">returns true if successful</span></span>

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

### <span data-ttu-id="22cb5-128">-RefreshData</span><span class="sxs-lookup"><span data-stu-id="22cb5-128">-RefreshData</span></span>
<span data-ttu-id="22cb5-129">Aktualisieren von Containermetadaten mit den Daten aus der Cloud</span><span class="sxs-lookup"><span data-stu-id="22cb5-129">Refresh Container Metadata with the data from the cloud</span></span>

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

### <span data-ttu-id="22cb5-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="22cb5-130">-ResourceGroupName</span></span>
<span data-ttu-id="22cb5-131">Ressourcengruppenname</span><span class="sxs-lookup"><span data-stu-id="22cb5-131">Resource Group Name</span></span>

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

### <span data-ttu-id="22cb5-132">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="22cb5-132">-ResourceId</span></span>
<span data-ttu-id="22cb5-133">Azure ResourceId</span><span class="sxs-lookup"><span data-stu-id="22cb5-133">Azure ResourceId</span></span>

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

### <span data-ttu-id="22cb5-134">-Confirm</span><span class="sxs-lookup"><span data-stu-id="22cb5-134">-Confirm</span></span>
<span data-ttu-id="22cb5-135">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="22cb5-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="22cb5-136">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="22cb5-136">-WhatIf</span></span>
<span data-ttu-id="22cb5-137">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="22cb5-137">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="22cb5-138">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="22cb5-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="22cb5-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="22cb5-139">CommonParameters</span></span>
<span data-ttu-id="22cb5-140">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="22cb5-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="22cb5-141">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="22cb5-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="22cb5-142">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="22cb5-142">INPUTS</span></span>

### <span data-ttu-id="22cb5-143">System.String</span><span class="sxs-lookup"><span data-stu-id="22cb5-143">System.String</span></span>

### <span data-ttu-id="22cb5-144">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeStorageContainer</span><span class="sxs-lookup"><span data-stu-id="22cb5-144">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeStorageContainer</span></span>

## <span data-ttu-id="22cb5-145">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="22cb5-145">OUTPUTS</span></span>

### <span data-ttu-id="22cb5-146">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeStorageContainer</span><span class="sxs-lookup"><span data-stu-id="22cb5-146">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeStorageContainer</span></span>

## <span data-ttu-id="22cb5-147">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="22cb5-147">NOTES</span></span>

## <span data-ttu-id="22cb5-148">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="22cb5-148">RELATED LINKS</span></span>
