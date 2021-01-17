---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DeploymentManager.dll-Help.xml
Module Name: Az.DeploymentManager
online version: https://docs.microsoft.com/en-us/powershell/module/az.deploymentmanager/set-azdeploymentmanagerartifactsource
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeploymentManager/DeploymentManager/help/Set-AzDeploymentManagerArtifactSource.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeploymentManager/DeploymentManager/help/Set-AzDeploymentManagerArtifactSource.md
ms.openlocfilehash: ee69c178d48775a870b229e652a1584c413bd7ca
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98467923"
---
# <span data-ttu-id="24a02-101">Set-AzDeploymentManagerArtifactSource</span><span class="sxs-lookup"><span data-stu-id="24a02-101">Set-AzDeploymentManagerArtifactSource</span></span>

## <span data-ttu-id="24a02-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="24a02-102">SYNOPSIS</span></span>
<span data-ttu-id="24a02-103">Aktualisiert die Artefaktquelle.</span><span class="sxs-lookup"><span data-stu-id="24a02-103">Updates the artifacts source.</span></span>

## <span data-ttu-id="24a02-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="24a02-104">SYNTAX</span></span>

```
Set-AzDeploymentManagerArtifactSource [-InputObject] <PSArtifactSource>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="24a02-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="24a02-105">DESCRIPTION</span></span>
<span data-ttu-id="24a02-106">Das **Cmdlet "Set-AzDeploymentManagerArtifactSource"** aktualisiert eine Artefaktquelle mit dem angegebenen Artefaktquellenobjekt.</span><span class="sxs-lookup"><span data-stu-id="24a02-106">The **Set-AzDeploymentManagerArtifactSource** cmdlet updates an artifact source with the specified artifact source object.</span></span>
<span data-ttu-id="24a02-107">Das Cmdlet gibt das aktualisierte Artefaktsource-Objekt zurück.</span><span class="sxs-lookup"><span data-stu-id="24a02-107">The cmdlet returns the updated ArtifactSource object.</span></span>

## <span data-ttu-id="24a02-108">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="24a02-108">EXAMPLES</span></span>

### <span data-ttu-id="24a02-109">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="24a02-109">Example 1</span></span>
```powershell
PS C:\> Get-AzDeploymentManagerArtifactSource -InputObject $artifactSourceObject
```

<span data-ttu-id="24a02-110">Mit diesem Befehl wird eine Artefaktquelle aktualisiert, deren Name und Ressourcengruppe mit den Eigenschaften "Name" bzw. "ResourceGroupName" des $artifactSourceObject übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="24a02-110">This command updates an artifact source whose name and ResourceGroup match the Name and ResourceGroupName properties of the $artifactSourceObject, respectively.</span></span>
<span data-ttu-id="24a02-111">Die Artefaktquelle wurde auf die Eigenschaften aktualisiert, die in der Liste $artifactSourceObject.</span><span class="sxs-lookup"><span data-stu-id="24a02-111">The artifact source would be updated to the properties set in the $artifactSourceObject.</span></span>

## <span data-ttu-id="24a02-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="24a02-112">PARAMETERS</span></span>

### <span data-ttu-id="24a02-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="24a02-113">-DefaultProfile</span></span>
<span data-ttu-id="24a02-114">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="24a02-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="24a02-115">-InputObject</span><span class="sxs-lookup"><span data-stu-id="24a02-115">-InputObject</span></span>
<span data-ttu-id="24a02-116">Das Artefaktquellenobjekt.</span><span class="sxs-lookup"><span data-stu-id="24a02-116">The artifact source object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.DeploymentManager.Models.PSArtifactSource
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="24a02-117">-Confirm</span><span class="sxs-lookup"><span data-stu-id="24a02-117">-Confirm</span></span>
<span data-ttu-id="24a02-118">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="24a02-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="24a02-119">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="24a02-119">-WhatIf</span></span>
<span data-ttu-id="24a02-120">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="24a02-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="24a02-121">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="24a02-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="24a02-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="24a02-122">CommonParameters</span></span>
<span data-ttu-id="24a02-123">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="24a02-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="24a02-124">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="24a02-124">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="24a02-125">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="24a02-125">INPUTS</span></span>

### <span data-ttu-id="24a02-126">Microsoft.Azure.Commands.DeploymentManager.Models.PSArtifactSource</span><span class="sxs-lookup"><span data-stu-id="24a02-126">Microsoft.Azure.Commands.DeploymentManager.Models.PSArtifactSource</span></span>

## <span data-ttu-id="24a02-127">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="24a02-127">OUTPUTS</span></span>

### <span data-ttu-id="24a02-128">Microsoft.Azure.Commands.DeploymentManager.Models.PSArtifactSource</span><span class="sxs-lookup"><span data-stu-id="24a02-128">Microsoft.Azure.Commands.DeploymentManager.Models.PSArtifactSource</span></span>

## <span data-ttu-id="24a02-129">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="24a02-129">NOTES</span></span>

## <span data-ttu-id="24a02-130">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="24a02-130">RELATED LINKS</span></span>
