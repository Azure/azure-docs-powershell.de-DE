---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DeploymentManager.dll-Help.xml
Module Name: Az.DeploymentManager
online version: https://docs.microsoft.com/en-us/powershell/module/az.deploymentmanager/get-azdeploymentmanagerartifactsource
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeploymentManager/DeploymentManager/help/Get-AzDeploymentManagerArtifactSource.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeploymentManager/DeploymentManager/help/Get-AzDeploymentManagerArtifactSource.md
ms.openlocfilehash: 5b330b2f20fb0611d4bfdea37756b4d62e3bbd69
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100163753"
---
# <span data-ttu-id="201fc-101">Get-AzDeploymentManagerArtifactSource</span><span class="sxs-lookup"><span data-stu-id="201fc-101">Get-AzDeploymentManagerArtifactSource</span></span>

## <span data-ttu-id="201fc-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="201fc-102">SYNOPSIS</span></span>

<span data-ttu-id="201fc-103">Ruft die Artefaktquelle ab.</span><span class="sxs-lookup"><span data-stu-id="201fc-103">Gets the Artifact source.</span></span>

## <span data-ttu-id="201fc-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="201fc-104">SYNTAX</span></span>

### <span data-ttu-id="201fc-105">Interaktiv (Standard)</span><span class="sxs-lookup"><span data-stu-id="201fc-105">Interactive (Default)</span></span>
```
Get-AzDeploymentManagerArtifactSource [-ResourceGroupName] <String> [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="201fc-106">ResourceId</span><span class="sxs-lookup"><span data-stu-id="201fc-106">ResourceId</span></span>
```
Get-AzDeploymentManagerArtifactSource [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="201fc-107">InputObject</span><span class="sxs-lookup"><span data-stu-id="201fc-107">InputObject</span></span>
```
Get-AzDeploymentManagerArtifactSource [-InputObject] <PSArtifactSource>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="201fc-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="201fc-108">DESCRIPTION</span></span>
<span data-ttu-id="201fc-109">Das **Cmdlet "Get-AzDeploymentManagerArtifactSource"** ruft eine Artefaktquelle ab und gibt ein Objekt zurück, das diese Artefaktquelle darstellt.</span><span class="sxs-lookup"><span data-stu-id="201fc-109">The **Get-AzDeploymentManagerArtifactSource** cmdlet gets an artifact source, and returns an object that represents that artifact source.</span></span>
<span data-ttu-id="201fc-110">Geben Sie die Artefaktquelle durch ihren Namen und den Namen der Ressourcengruppe an.</span><span class="sxs-lookup"><span data-stu-id="201fc-110">Specify the artifact source by its name and resource group name.</span></span> <span data-ttu-id="201fc-111">Alternativ können Sie das ArtifactSource-Objekt oder die ResourceId bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="201fc-111">Alternately, you can provide the ArtifactSource object or the ResourceId.</span></span>

## <span data-ttu-id="201fc-112">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="201fc-112">EXAMPLES</span></span>

### <span data-ttu-id="201fc-113">Beispiel 1: Erhalten einer Artefaktquelle</span><span class="sxs-lookup"><span data-stu-id="201fc-113">Example 1: Get an artifact source</span></span>
```powershell
PS C:\> Get-AzDeploymentManagerArtifactSource -ResourceGroupName "ContosoResourceGroup" -Name "ContosoArtifactSource"
```

<span data-ttu-id="201fc-114">Dieser Befehl ruft eine Artefaktquelle namens "ContosoArtifactSource" in "ContosoResourceGroup" ab.</span><span class="sxs-lookup"><span data-stu-id="201fc-114">This command gets an artifact source named ContosoArtifactSource in ContosoResourceGroup.</span></span>

### <span data-ttu-id="201fc-115">Beispiel 2: Erhalten einer Artefaktquelle mithilfe des Ressourcenbezeichners</span><span class="sxs-lookup"><span data-stu-id="201fc-115">Example 2: Get an artifact source using the resource identifier</span></span>
```powershell
PS C:\> Get-AzDeploymentManagerArtifactSource -ResourceId "/subscriptions/subscriptionId/resourcegroups/ContosoResourceGroup/providers/Microsoft.DeploymentManager/artifactSources/ContosoArtifactSource"
```

<span data-ttu-id="201fc-116">Dieser Befehl ruft eine Artefaktquelle namens "ContosoArtifactSource" in "ContosoResourceGroup" ab.</span><span class="sxs-lookup"><span data-stu-id="201fc-116">This command gets an artifact source named ContosoArtifactSource in ContosoResourceGroup.</span></span>

### <span data-ttu-id="201fc-117">Beispiel 3: Erhalten einer Artefaktquelle mithilfe eines objekts, das von einer New-AzDeploymentManagerArtifactSource</span><span class="sxs-lookup"><span data-stu-id="201fc-117">Example 3: Get an artifact source using an object returned by New-AzDeploymentManagerArtifactSource</span></span>
```powershell
PS C:\> Get-AzDeploymentManagerArtifactSource -InputObject $artifactSourceObject
```

<span data-ttu-id="201fc-118">Dieser Befehl ruft eine Artefaktquelle ab, deren Name und Ressourcengruppe mit den Eigenschaften "Name" bzw. "ResourceGroupName" des $artifactSourceObject übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="201fc-118">This command gets an artifact source whose name and ResourceGroup match the Name and ResourceGroupName properties of the $artifactSourceObject, respectively.</span></span>

## <span data-ttu-id="201fc-119">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="201fc-119">PARAMETERS</span></span>

### <span data-ttu-id="201fc-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="201fc-120">-DefaultProfile</span></span>
<span data-ttu-id="201fc-121">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="201fc-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="201fc-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="201fc-122">-InputObject</span></span>
<span data-ttu-id="201fc-123">Artefaktquellenobjekt.</span><span class="sxs-lookup"><span data-stu-id="201fc-123">Artifact Source object.</span></span>

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

### <span data-ttu-id="201fc-124">-Name</span><span class="sxs-lookup"><span data-stu-id="201fc-124">-Name</span></span>
<span data-ttu-id="201fc-125">Der Name der Artefaktquelle.</span><span class="sxs-lookup"><span data-stu-id="201fc-125">The name of the artifact source.</span></span>

```yaml
Type: System.String
Parameter Sets: Interactive
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="201fc-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="201fc-126">-ResourceGroupName</span></span>
<span data-ttu-id="201fc-127">Die Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="201fc-127">The resource group.</span></span>

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

### <span data-ttu-id="201fc-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="201fc-128">-ResourceId</span></span>
<span data-ttu-id="201fc-129">Der Ressourcenbezeichner.</span><span class="sxs-lookup"><span data-stu-id="201fc-129">The resource identifier.</span></span>

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

### <span data-ttu-id="201fc-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="201fc-130">CommonParameters</span></span>
<span data-ttu-id="201fc-131">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="201fc-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="201fc-132">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="201fc-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="201fc-133">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="201fc-133">INPUTS</span></span>

### <span data-ttu-id="201fc-134">System.String</span><span class="sxs-lookup"><span data-stu-id="201fc-134">System.String</span></span>

### <span data-ttu-id="201fc-135">Microsoft.Azure.Commands.DeploymentManager.Models.PSArtifactSource</span><span class="sxs-lookup"><span data-stu-id="201fc-135">Microsoft.Azure.Commands.DeploymentManager.Models.PSArtifactSource</span></span>

## <span data-ttu-id="201fc-136">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="201fc-136">OUTPUTS</span></span>

### <span data-ttu-id="201fc-137">Microsoft.Azure.Commands.DeploymentManager.Models.PSArtifactSource</span><span class="sxs-lookup"><span data-stu-id="201fc-137">Microsoft.Azure.Commands.DeploymentManager.Models.PSArtifactSource</span></span>

## <span data-ttu-id="201fc-138">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="201fc-138">NOTES</span></span>

## <span data-ttu-id="201fc-139">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="201fc-139">RELATED LINKS</span></span>
