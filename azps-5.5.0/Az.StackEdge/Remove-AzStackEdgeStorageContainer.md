---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StackEdge.dll-Help.xml
Module Name: Az.StackEdge
online version: https://docs.microsoft.com/en-us/powershell/module/az.stackedge/remove-azstackedgestoragecontainer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/Remove-AzStackEdgeStorageContainer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/Remove-AzStackEdgeStorageContainer.md
ms.openlocfilehash: c1e76da1fc01ea1698c56e40fd3bd46f6378ea07
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100145505"
---
# <span data-ttu-id="5c892-101">Remove-AzStackEdgeStorageContainer</span><span class="sxs-lookup"><span data-stu-id="5c892-101">Remove-AzStackEdgeStorageContainer</span></span>

## <span data-ttu-id="5c892-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5c892-102">SYNOPSIS</span></span>
<span data-ttu-id="5c892-103">Entfernt einen Speichercontainer für das Edgespeicherkonto auf einem Gerät.</span><span class="sxs-lookup"><span data-stu-id="5c892-103">Removes a storage container for the Edge Storage account on a device.</span></span>

## <span data-ttu-id="5c892-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="5c892-104">SYNTAX</span></span>

### <span data-ttu-id="5c892-105">DeleteByNameParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="5c892-105">DeleteByNameParameterSet (Default)</span></span>
```
Remove-AzStackEdgeStorageContainer [-ResourceGroupName] <String> [-DeviceName] <String>
 [-EdgeStorageAccountName] <String> [-Name] <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5c892-106">DeleteByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="5c892-106">DeleteByResourceIdParameterSet</span></span>
```
Remove-AzStackEdgeStorageContainer -ResourceId <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5c892-107">DeleteByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="5c892-107">DeleteByInputObjectParameterSet</span></span>
```
Remove-AzStackEdgeStorageContainer -InputObject <PSStackEdgeStorageContainer> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5c892-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="5c892-108">DESCRIPTION</span></span>
<span data-ttu-id="5c892-109">Das **Cmdlet "Remove-AzStackEdgeStorageContainer"** entfernt einen zugeordneten Speichercontainer für das Edgespeicherkonto auf einem Stack Edge-Gerät.</span><span class="sxs-lookup"><span data-stu-id="5c892-109">The **Remove-AzStackEdgeStorageContainer** cmdlet removes an associated storage container for the Edge Storage account on a Stack Edge device.</span></span> <span data-ttu-id="5c892-110">Sie können den Namen des Speichercontainers angeben, der als Parameter entfernt werden soll.</span><span class="sxs-lookup"><span data-stu-id="5c892-110">You can specify the name of the storage container to be removed as a parameter.</span></span>

## <span data-ttu-id="5c892-111">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="5c892-111">EXAMPLES</span></span>

### <span data-ttu-id="5c892-112">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="5c892-112">Example 1</span></span>
```powershell
PS C:\> Remove-AzStackEdgeStorageContainer -ResourceGroupName resourceGroupName -DeviceName deviceName -EdgeStorageAccountName edgestorageaccountname -Name container1
```

## <span data-ttu-id="5c892-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="5c892-113">PARAMETERS</span></span>

### <span data-ttu-id="5c892-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="5c892-114">-AsJob</span></span>
<span data-ttu-id="5c892-115">Ausführen des Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="5c892-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="5c892-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5c892-116">-DefaultProfile</span></span>
<span data-ttu-id="5c892-117">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="5c892-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5c892-118">-DeviceName</span><span class="sxs-lookup"><span data-stu-id="5c892-118">-DeviceName</span></span>
<span data-ttu-id="5c892-119">Gerätename</span><span class="sxs-lookup"><span data-stu-id="5c892-119">Device Name</span></span>

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

### <span data-ttu-id="5c892-120">-EdgeStorageAccountName</span><span class="sxs-lookup"><span data-stu-id="5c892-120">-EdgeStorageAccountName</span></span>
<span data-ttu-id="5c892-121">Bereitstellen des vorhandenen EdgeStorageAccount-Namens</span><span class="sxs-lookup"><span data-stu-id="5c892-121">Provide existing EdgeStorageAccount's Name</span></span>

```yaml
Type: System.String
Parameter Sets: DeleteByNameParameterSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5c892-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="5c892-122">-InputObject</span></span>
<span data-ttu-id="5c892-123">Eingabeobjekt</span><span class="sxs-lookup"><span data-stu-id="5c892-123">Input Object</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeStorageContainer
Parameter Sets: DeleteByInputObjectParameterSet
Aliases: EdgeStorageContainer

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="5c892-124">-Name</span><span class="sxs-lookup"><span data-stu-id="5c892-124">-Name</span></span>
<span data-ttu-id="5c892-125">Ressourcenname</span><span class="sxs-lookup"><span data-stu-id="5c892-125">Resource Name</span></span>

```yaml
Type: System.String
Parameter Sets: DeleteByNameParameterSet
Aliases: EdgeContainerName

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5c892-126">-PassThru</span><span class="sxs-lookup"><span data-stu-id="5c892-126">-PassThru</span></span>
<span data-ttu-id="5c892-127">gibt "true" zurück, wenn dies erfolgreich ist.</span><span class="sxs-lookup"><span data-stu-id="5c892-127">returns true if successful</span></span>

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

### <span data-ttu-id="5c892-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5c892-128">-ResourceGroupName</span></span>
<span data-ttu-id="5c892-129">Ressourcengruppenname</span><span class="sxs-lookup"><span data-stu-id="5c892-129">Resource Group Name</span></span>

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

### <span data-ttu-id="5c892-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="5c892-130">-ResourceId</span></span>
<span data-ttu-id="5c892-131">Azure ResourceId</span><span class="sxs-lookup"><span data-stu-id="5c892-131">Azure ResourceId</span></span>

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

### <span data-ttu-id="5c892-132">-Confirm</span><span class="sxs-lookup"><span data-stu-id="5c892-132">-Confirm</span></span>
<span data-ttu-id="5c892-133">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="5c892-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5c892-134">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="5c892-134">-WhatIf</span></span>
<span data-ttu-id="5c892-135">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="5c892-135">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="5c892-136">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="5c892-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5c892-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5c892-137">CommonParameters</span></span>
<span data-ttu-id="5c892-138">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5c892-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5c892-139">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="5c892-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5c892-140">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="5c892-140">INPUTS</span></span>

### <span data-ttu-id="5c892-141">System.String</span><span class="sxs-lookup"><span data-stu-id="5c892-141">System.String</span></span>

### <span data-ttu-id="5c892-142">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeStorageContainer</span><span class="sxs-lookup"><span data-stu-id="5c892-142">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeStorageContainer</span></span>

## <span data-ttu-id="5c892-143">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="5c892-143">OUTPUTS</span></span>

### <span data-ttu-id="5c892-144">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="5c892-144">System.Boolean</span></span>

## <span data-ttu-id="5c892-145">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="5c892-145">NOTES</span></span>

## <span data-ttu-id="5c892-146">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="5c892-146">RELATED LINKS</span></span>
