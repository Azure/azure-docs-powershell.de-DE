---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DeploymentManager.dll-Help.xml
Module Name: Az.DeploymentManager
online version: https://docs.microsoft.com/en-us/powershell/module/az.deploymentmanager/remove-azdeploymentmanagerartifactsource
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeploymentManager/DeploymentManager/help/Remove-AzDeploymentManagerArtifactSource.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeploymentManager/DeploymentManager/help/Remove-AzDeploymentManagerArtifactSource.md
ms.openlocfilehash: fa9dc4f8234e9c6e709d59f3945b05eeceef4316
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94008009"
---
# <span data-ttu-id="46744-101">Remove-AzDeploymentManagerArtifactSource</span><span class="sxs-lookup"><span data-stu-id="46744-101">Remove-AzDeploymentManagerArtifactSource</span></span>

## <span data-ttu-id="46744-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="46744-102">SYNOPSIS</span></span>
<span data-ttu-id="46744-103">Löscht die angegebene Artefakt-Quelle.</span><span class="sxs-lookup"><span data-stu-id="46744-103">Deletes the specified artifact source.</span></span>

## <span data-ttu-id="46744-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="46744-104">SYNTAX</span></span>

### <span data-ttu-id="46744-105">Interaktiv (Standard)</span><span class="sxs-lookup"><span data-stu-id="46744-105">Interactive (Default)</span></span>
```
Remove-AzDeploymentManagerArtifactSource [-ResourceGroupName] <String> [-Name] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="46744-106">ResourceId</span><span class="sxs-lookup"><span data-stu-id="46744-106">ResourceId</span></span>
```
Remove-AzDeploymentManagerArtifactSource [-ResourceId] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="46744-107">InputObject</span><span class="sxs-lookup"><span data-stu-id="46744-107">InputObject</span></span>
```
Remove-AzDeploymentManagerArtifactSource [-InputObject] <PSArtifactSource> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="46744-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="46744-108">DESCRIPTION</span></span>
<span data-ttu-id="46744-109">Das Cmdlet " **Remove-AzDeploymentManagerArtifactSource** " löscht eine Artefakt-Quelle mit dem Namen und dem Namen der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="46744-109">The **Remove-AzDeploymentManagerArtifactSource** cmdlet deletes an artifact source Specify the artifact source by its name and resource group name.</span></span> <span data-ttu-id="46744-110">Alternativ können Sie das ArtifactSource-Objekt oder die resourcecode-Objekt bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="46744-110">Alternately, you can provide the ArtifactSource object or the ResourceId.</span></span>

## <span data-ttu-id="46744-111">Beispiele</span><span class="sxs-lookup"><span data-stu-id="46744-111">EXAMPLES</span></span>

### <span data-ttu-id="46744-112">Beispiel 1: Löschen einer Artefakt-Quelle</span><span class="sxs-lookup"><span data-stu-id="46744-112">Example 1: Delete an artifact source</span></span>
### <span data-ttu-id="46744-113">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="46744-113">Example 1</span></span>
```powershell
PS C:\> Remove-AzDeploymentManagerArtifactSource -ResourceGroupName "ContosoResourceGroup" -Name "ContosoArtifactSource"
```

<span data-ttu-id="46744-114">Dieser Befehl löscht eine Artefakt-Quelle namens ContosoArtifactSource in ContosoResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="46744-114">This command deletes an artifact source named ContosoArtifactSource in ContosoResourceGroup.</span></span>

### <span data-ttu-id="46744-115">Beispiel 2: Löschen einer Artefakt-Quelle mit dem Ressourcenbezeichner</span><span class="sxs-lookup"><span data-stu-id="46744-115">Example 2: Delete an artifact source using the resource identifier</span></span>
```powershell
PS C:\> Remove-AzDeploymentManagerArtifactSource -ResourceId "/subscriptions/subscriptionId/resourcegroups/ContosoResourceGroup/providers/Microsoft.DeploymentManager/artifactSources/ContosoArtifactSource"
```

<span data-ttu-id="46744-116">Dieser Befehl löscht eine Artefakt-Quelle namens ContosoArtifactSource in ContosoResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="46744-116">This command deletes an artifact source named ContosoArtifactSource in ContosoResourceGroup.</span></span>

### <span data-ttu-id="46744-117">Beispiel 3: Löschen einer Artefakt-Quelle mit einem Objekt</span><span class="sxs-lookup"><span data-stu-id="46744-117">Example 3: Delete an artifact source using an object</span></span>
```powershell
PS C:\> Remove-AzDeploymentManagerArtifactSource -InputObject $artifactSourceObject
```

<span data-ttu-id="46744-118">Dieser Befehl löscht eine Artefakt-Quelle, deren Name und ResourceGroup den Namen-und ResourceGroupName-Eigenschaften der $artifactSourceObject entsprechen.</span><span class="sxs-lookup"><span data-stu-id="46744-118">This command deletes an artifact source whose name and ResourceGroup match the Name and ResourceGroupName properties of the $artifactSourceObject, respectively.</span></span>

## <span data-ttu-id="46744-119">Parameter</span><span class="sxs-lookup"><span data-stu-id="46744-119">PARAMETERS</span></span>

### <span data-ttu-id="46744-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="46744-120">-DefaultProfile</span></span>
<span data-ttu-id="46744-121">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="46744-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="46744-122">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="46744-122">-InputObject</span></span>
<span data-ttu-id="46744-123">Die Artefakt-Quelle, die entfernt werden soll.</span><span class="sxs-lookup"><span data-stu-id="46744-123">The artifact source to be removed.</span></span>

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

### <span data-ttu-id="46744-124">-Name</span><span class="sxs-lookup"><span data-stu-id="46744-124">-Name</span></span>
<span data-ttu-id="46744-125">Der Name der Artefakt-Quelle.</span><span class="sxs-lookup"><span data-stu-id="46744-125">The name of the artifact source.</span></span>

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

### <span data-ttu-id="46744-126">-PassThru</span><span class="sxs-lookup"><span data-stu-id="46744-126">-PassThru</span></span>
<span data-ttu-id="46744-127">{{Fill passthru Description}}</span><span class="sxs-lookup"><span data-stu-id="46744-127">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="46744-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="46744-128">-ResourceGroupName</span></span>
<span data-ttu-id="46744-129">Die Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="46744-129">The resource group.</span></span>

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

### <span data-ttu-id="46744-130">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="46744-130">-ResourceId</span></span>
<span data-ttu-id="46744-131">Der Ressourcenbezeichner.</span><span class="sxs-lookup"><span data-stu-id="46744-131">The resource identifier.</span></span>

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

### <span data-ttu-id="46744-132">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="46744-132">-Confirm</span></span>
<span data-ttu-id="46744-133">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="46744-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="46744-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="46744-134">-WhatIf</span></span>
<span data-ttu-id="46744-135">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="46744-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="46744-136">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="46744-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="46744-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="46744-137">CommonParameters</span></span>
<span data-ttu-id="46744-138">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="46744-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="46744-139">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="46744-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="46744-140">Eingaben</span><span class="sxs-lookup"><span data-stu-id="46744-140">INPUTS</span></span>

### <span data-ttu-id="46744-141">System. String</span><span class="sxs-lookup"><span data-stu-id="46744-141">System.String</span></span>

### <span data-ttu-id="46744-142">Microsoft. Azure. Commands. deploymentmanager. Models. PSArtifactSource</span><span class="sxs-lookup"><span data-stu-id="46744-142">Microsoft.Azure.Commands.DeploymentManager.Models.PSArtifactSource</span></span>

## <span data-ttu-id="46744-143">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="46744-143">OUTPUTS</span></span>

### <span data-ttu-id="46744-144">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="46744-144">System.Boolean</span></span>

## <span data-ttu-id="46744-145">Notizen</span><span class="sxs-lookup"><span data-stu-id="46744-145">NOTES</span></span>

## <span data-ttu-id="46744-146">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="46744-146">RELATED LINKS</span></span>
