---
external help file: Microsoft.Azure.Commands.DeploymentManager.dll-Help.xml
Module Name: AzureRM.DeploymentManager
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.deploymentmanager/remove-azurermdeploymentmanagerartifactsource
schema: 2.0.0
ms.openlocfilehash: 7473f125511995efb1f6273d3b8adb675a58d06d
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93474733"
---
# <span data-ttu-id="59510-101">Remove-AzureRmDeploymentManagerArtifactSource</span><span class="sxs-lookup"><span data-stu-id="59510-101">Remove-AzureRmDeploymentManagerArtifactSource</span></span>

## <span data-ttu-id="59510-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="59510-102">SYNOPSIS</span></span>
<span data-ttu-id="59510-103">Löscht eine Artefakt-Quelle.</span><span class="sxs-lookup"><span data-stu-id="59510-103">Deletes an artifact source.</span></span>

## <span data-ttu-id="59510-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="59510-104">SYNTAX</span></span>

### <span data-ttu-id="59510-105">Interaktiv (Standard)</span><span class="sxs-lookup"><span data-stu-id="59510-105">Interactive (Default)</span></span>
```
Remove-AzureRmDeploymentManagerArtifactSource [-ResourceGroupName] <String> [-Name] <String> [-Force]
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="59510-106">ResourceId</span><span class="sxs-lookup"><span data-stu-id="59510-106">ResourceId</span></span>
```
Remove-AzureRmDeploymentManagerArtifactSource [-ResourceId] <String> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="59510-107">InputObject</span><span class="sxs-lookup"><span data-stu-id="59510-107">InputObject</span></span>
```
Remove-AzureRmDeploymentManagerArtifactSource [-ArtifactSource] <PSArtifactSource> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="59510-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="59510-108">DESCRIPTION</span></span>
<span data-ttu-id="59510-109">Das Cmdlet " **Remove-AzureRmDeploymentManagerArtifactSource** " löscht eine Artefakt-Quelle mit dem Namen und dem Namen der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="59510-109">The **Remove-AzureRmDeploymentManagerArtifactSource** cmdlet deletes an artifact source Specify the artifact source by its name and resource group name.</span></span> <span data-ttu-id="59510-110">Alternativ können Sie das ArtifactSource-Objekt oder die resourcecode-Objekt bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="59510-110">Alternately, you can provide the ArtifactSource object or the ResourceId.</span></span>

## <span data-ttu-id="59510-111">Beispiele</span><span class="sxs-lookup"><span data-stu-id="59510-111">EXAMPLES</span></span>

### <span data-ttu-id="59510-112">Beispiel 1: Löschen einer Artefakt-Quelle</span><span class="sxs-lookup"><span data-stu-id="59510-112">Example 1: Delete an artifact source</span></span>
```powershell
PS C:\> Remove-AzureRmDeploymentManagerArtifactSource -ResourceGroupName "ContosoResourceGroup" -Name "ContosoArtifactSource"
```

<span data-ttu-id="59510-113">Dieser Befehl löscht eine Artefakt-Quelle namens ContosoArtifactSource in ContosoResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="59510-113">This command deletes an artifact source named ContosoArtifactSource in ContosoResourceGroup.</span></span>

### <span data-ttu-id="59510-114">Beispiel 2: Löschen einer Artefakt-Quelle mit dem Ressourcenbezeichner</span><span class="sxs-lookup"><span data-stu-id="59510-114">Example 2: Delete an artifact source using the resource identifier</span></span>
```powershell
PS C:\> Remove-AzureRmDeploymentManagerArtifactSource -ResourceId "/subscriptions/subscriptionId/resourcegroups/ContosoResourceGroup/providers/Microsoft.DeploymentManager/artifactSources/ContosoArtifactSource"
```

<span data-ttu-id="59510-115">Dieser Befehl löscht eine Artefakt-Quelle namens ContosoArtifactSource in ContosoResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="59510-115">This command deletes an artifact source named ContosoArtifactSource in ContosoResourceGroup.</span></span>

### <span data-ttu-id="59510-116">Beispiel 3: Löschen einer Artefakt-Quelle mit einem Objekt</span><span class="sxs-lookup"><span data-stu-id="59510-116">Example 3: Delete an artifact source using an object</span></span>
```powershell
PS C:\> Remove-AzureRmDeploymentManagerArtifactSource -ArtifactSource $artifactSourceObject
```

<span data-ttu-id="59510-117">Dieser Befehl löscht eine Artefakt-Quelle, deren Name und ResourceGroup den Namen-und ResourceGroupName-Eigenschaften der $artifactSourceObject entsprechen.</span><span class="sxs-lookup"><span data-stu-id="59510-117">This command deletes an artifact source whose name and ResourceGroup match the Name and ResourceGroupName properties of the $artifactSourceObject, respectively.</span></span>

## <span data-ttu-id="59510-118">Parameter</span><span class="sxs-lookup"><span data-stu-id="59510-118">PARAMETERS</span></span>

### <span data-ttu-id="59510-119">-ArtifactSource</span><span class="sxs-lookup"><span data-stu-id="59510-119">-ArtifactSource</span></span>
<span data-ttu-id="59510-120">Der artefaktspeicher, der entfernt werden soll.</span><span class="sxs-lookup"><span data-stu-id="59510-120">The artifact store to be removed.</span></span>

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

### <span data-ttu-id="59510-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="59510-121">-DefaultProfile</span></span>
<span data-ttu-id="59510-122">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="59510-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="59510-123">-Force</span><span class="sxs-lookup"><span data-stu-id="59510-123">-Force</span></span>
<span data-ttu-id="59510-124">Keine Bestätigung anfordern.</span><span class="sxs-lookup"><span data-stu-id="59510-124">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="59510-125">-Name</span><span class="sxs-lookup"><span data-stu-id="59510-125">-Name</span></span>
<span data-ttu-id="59510-126">Der Name der Artefakt-Quelle.</span><span class="sxs-lookup"><span data-stu-id="59510-126">The name of the artifact source.</span></span>

```yaml
Type: System.String
Parameter Sets: Interactive
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="59510-127">-PassThru</span><span class="sxs-lookup"><span data-stu-id="59510-127">-PassThru</span></span>
<span data-ttu-id="59510-128">{{Fill passthru Description}}</span><span class="sxs-lookup"><span data-stu-id="59510-128">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="59510-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="59510-129">-ResourceGroupName</span></span>
<span data-ttu-id="59510-130">Die Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="59510-130">The resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: Interactive
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="59510-131">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="59510-131">-ResourceId</span></span>
<span data-ttu-id="59510-132">Der Ressourcenbezeichner.</span><span class="sxs-lookup"><span data-stu-id="59510-132">The resource identifier.</span></span>

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

### <span data-ttu-id="59510-133">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="59510-133">-Confirm</span></span>
<span data-ttu-id="59510-134">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="59510-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="59510-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="59510-135">-WhatIf</span></span>
<span data-ttu-id="59510-136">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="59510-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="59510-137">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="59510-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="59510-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="59510-138">CommonParameters</span></span>
<span data-ttu-id="59510-139">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="59510-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="59510-140">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="59510-140">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="59510-141">Eingaben</span><span class="sxs-lookup"><span data-stu-id="59510-141">INPUTS</span></span>

### <span data-ttu-id="59510-142">Microsoft. Azure. Commands. deploymentmanager. Models. PSArtifactSource</span><span class="sxs-lookup"><span data-stu-id="59510-142">Microsoft.Azure.Commands.DeploymentManager.Models.PSArtifactSource</span></span>

## <span data-ttu-id="59510-143">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="59510-143">OUTPUTS</span></span>

### <span data-ttu-id="59510-144">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="59510-144">System.Boolean</span></span>

## <span data-ttu-id="59510-145">Notizen</span><span class="sxs-lookup"><span data-stu-id="59510-145">NOTES</span></span>

## <span data-ttu-id="59510-146">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="59510-146">RELATED LINKS</span></span>

[<span data-ttu-id="59510-147">Neu – AzureRmDeploymentManagerArtifactSource</span><span class="sxs-lookup"><span data-stu-id="59510-147">New-AzureRmDeploymentManagerArtifactSource</span></span>](./New-AzureRmDeploymentManagerArtifactSource.md)

[<span data-ttu-id="59510-148">Get-AzureRmDeploymentManagerArtifactSource</span><span class="sxs-lookup"><span data-stu-id="59510-148">Get-AzureRmDeploymentManagerArtifactSource</span></span>](./Get-AzureRmDeploymentManagerArtifactSource.md)

[<span data-ttu-id="59510-149">Satz-AzureRmDeploymentManagerArtifactSource</span><span class="sxs-lookup"><span data-stu-id="59510-149">Set-AzureRmDeploymentManagerArtifactSource</span></span>](./Set-AzureRmDeploymentManagerArtifactSource.md)