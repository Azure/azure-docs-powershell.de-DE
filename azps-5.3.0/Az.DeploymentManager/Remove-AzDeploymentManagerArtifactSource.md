---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DeploymentManager.dll-Help.xml
Module Name: Az.DeploymentManager
online version: https://docs.microsoft.com/en-us/powershell/module/az.deploymentmanager/remove-azdeploymentmanagerartifactsource
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeploymentManager/DeploymentManager/help/Remove-AzDeploymentManagerArtifactSource.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeploymentManager/DeploymentManager/help/Remove-AzDeploymentManagerArtifactSource.md
ms.openlocfilehash: fa9dc4f8234e9c6e709d59f3945b05eeceef4316
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98387426"
---
# <span data-ttu-id="848ae-101">Remove-AzDeploymentManagerArtifactSource</span><span class="sxs-lookup"><span data-stu-id="848ae-101">Remove-AzDeploymentManagerArtifactSource</span></span>

## <span data-ttu-id="848ae-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="848ae-102">SYNOPSIS</span></span>
<span data-ttu-id="848ae-103">Löscht die angegebene Artefaktquelle.</span><span class="sxs-lookup"><span data-stu-id="848ae-103">Deletes the specified artifact source.</span></span>

## <span data-ttu-id="848ae-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="848ae-104">SYNTAX</span></span>

### <span data-ttu-id="848ae-105">Interaktiv (Standard)</span><span class="sxs-lookup"><span data-stu-id="848ae-105">Interactive (Default)</span></span>
```
Remove-AzDeploymentManagerArtifactSource [-ResourceGroupName] <String> [-Name] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="848ae-106">ResourceId</span><span class="sxs-lookup"><span data-stu-id="848ae-106">ResourceId</span></span>
```
Remove-AzDeploymentManagerArtifactSource [-ResourceId] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="848ae-107">InputObject</span><span class="sxs-lookup"><span data-stu-id="848ae-107">InputObject</span></span>
```
Remove-AzDeploymentManagerArtifactSource [-InputObject] <PSArtifactSource> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="848ae-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="848ae-108">DESCRIPTION</span></span>
<span data-ttu-id="848ae-109">Das **Cmdlet "Remove-AzDeploymentManagerArtifactSource"** löscht eine Artefaktquelle. Geben Sie die Artefaktquelle durch den Namen und den Namen der Ressourcengruppe an.</span><span class="sxs-lookup"><span data-stu-id="848ae-109">The **Remove-AzDeploymentManagerArtifactSource** cmdlet deletes an artifact source Specify the artifact source by its name and resource group name.</span></span> <span data-ttu-id="848ae-110">Alternativ können Sie das ArtifactSource-Objekt oder die ResourceId bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="848ae-110">Alternately, you can provide the ArtifactSource object or the ResourceId.</span></span>

## <span data-ttu-id="848ae-111">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="848ae-111">EXAMPLES</span></span>

### <span data-ttu-id="848ae-112">Beispiel 1: Löschen einer Artefaktquelle</span><span class="sxs-lookup"><span data-stu-id="848ae-112">Example 1: Delete an artifact source</span></span>
### <span data-ttu-id="848ae-113">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="848ae-113">Example 1</span></span>
```powershell
PS C:\> Remove-AzDeploymentManagerArtifactSource -ResourceGroupName "ContosoResourceGroup" -Name "ContosoArtifactSource"
```

<span data-ttu-id="848ae-114">Mit diesem Befehl wird eine Artefaktquelle namens "ContosoArtifactSource" in "ContosoResourceGroup" gelöscht.</span><span class="sxs-lookup"><span data-stu-id="848ae-114">This command deletes an artifact source named ContosoArtifactSource in ContosoResourceGroup.</span></span>

### <span data-ttu-id="848ae-115">Beispiel 2: Löschen einer Artefaktquelle mithilfe des Ressourcenbezeichners</span><span class="sxs-lookup"><span data-stu-id="848ae-115">Example 2: Delete an artifact source using the resource identifier</span></span>
```powershell
PS C:\> Remove-AzDeploymentManagerArtifactSource -ResourceId "/subscriptions/subscriptionId/resourcegroups/ContosoResourceGroup/providers/Microsoft.DeploymentManager/artifactSources/ContosoArtifactSource"
```

<span data-ttu-id="848ae-116">Mit diesem Befehl wird eine Artefaktquelle namens "ContosoArtifactSource" in "ContosoResourceGroup" gelöscht.</span><span class="sxs-lookup"><span data-stu-id="848ae-116">This command deletes an artifact source named ContosoArtifactSource in ContosoResourceGroup.</span></span>

### <span data-ttu-id="848ae-117">Beispiel 3: Löschen einer Artefaktquelle mithilfe eines Objekts</span><span class="sxs-lookup"><span data-stu-id="848ae-117">Example 3: Delete an artifact source using an object</span></span>
```powershell
PS C:\> Remove-AzDeploymentManagerArtifactSource -InputObject $artifactSourceObject
```

<span data-ttu-id="848ae-118">Mit diesem Befehl wird eine Artefaktquelle gelöscht, deren Name und Ressourcengruppe mit den Eigenschaften "Name" bzw. "ResourceGroupName" des $artifactSourceObject übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="848ae-118">This command deletes an artifact source whose name and ResourceGroup match the Name and ResourceGroupName properties of the $artifactSourceObject, respectively.</span></span>

## <span data-ttu-id="848ae-119">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="848ae-119">PARAMETERS</span></span>

### <span data-ttu-id="848ae-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="848ae-120">-DefaultProfile</span></span>
<span data-ttu-id="848ae-121">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="848ae-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="848ae-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="848ae-122">-InputObject</span></span>
<span data-ttu-id="848ae-123">Die zu entfernende Artefaktquelle.</span><span class="sxs-lookup"><span data-stu-id="848ae-123">The artifact source to be removed.</span></span>

```yaml
Type: Microsoft.Azure.Commands.DeploymentManager.Models.PSArtifactSource
Parameter Sets: InputObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="848ae-124">-Name</span><span class="sxs-lookup"><span data-stu-id="848ae-124">-Name</span></span>
<span data-ttu-id="848ae-125">Der Name der Artefaktquelle.</span><span class="sxs-lookup"><span data-stu-id="848ae-125">The name of the artifact source.</span></span>

```yaml
Type: System.String
Parameter Sets: Interactive
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="848ae-126">-PassThru</span><span class="sxs-lookup"><span data-stu-id="848ae-126">-PassThru</span></span>
<span data-ttu-id="848ae-127">{{Fill PassThru Description}}</span><span class="sxs-lookup"><span data-stu-id="848ae-127">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="848ae-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="848ae-128">-ResourceGroupName</span></span>
<span data-ttu-id="848ae-129">Die Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="848ae-129">The resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: Interactive
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="848ae-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="848ae-130">-ResourceId</span></span>
<span data-ttu-id="848ae-131">Der Ressourcenbezeichner.</span><span class="sxs-lookup"><span data-stu-id="848ae-131">The resource identifier.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceId
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="848ae-132">-Confirm</span><span class="sxs-lookup"><span data-stu-id="848ae-132">-Confirm</span></span>
<span data-ttu-id="848ae-133">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="848ae-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="848ae-134">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="848ae-134">-WhatIf</span></span>
<span data-ttu-id="848ae-135">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="848ae-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="848ae-136">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="848ae-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="848ae-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="848ae-137">CommonParameters</span></span>
<span data-ttu-id="848ae-138">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="848ae-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="848ae-139">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="848ae-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="848ae-140">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="848ae-140">INPUTS</span></span>

### <span data-ttu-id="848ae-141">System.String</span><span class="sxs-lookup"><span data-stu-id="848ae-141">System.String</span></span>

### <span data-ttu-id="848ae-142">Microsoft.Azure.Commands.DeploymentManager.Models.PSArtifactSource</span><span class="sxs-lookup"><span data-stu-id="848ae-142">Microsoft.Azure.Commands.DeploymentManager.Models.PSArtifactSource</span></span>

## <span data-ttu-id="848ae-143">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="848ae-143">OUTPUTS</span></span>

### <span data-ttu-id="848ae-144">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="848ae-144">System.Boolean</span></span>

## <span data-ttu-id="848ae-145">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="848ae-145">NOTES</span></span>

## <span data-ttu-id="848ae-146">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="848ae-146">RELATED LINKS</span></span>
