---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DeploymentManager.dll-Help.xml
Module Name: Az.DeploymentManager
online version: https://docs.microsoft.com/powershell/module/az.deploymentmanager/get-azdeploymentmanagerartifactsource
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeploymentManager/DeploymentManager/help/Get-AzDeploymentManagerArtifactSource.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeploymentManager/DeploymentManager/help/Get-AzDeploymentManagerArtifactSource.md
ms.openlocfilehash: 819fb3427ae59291c6b6d78a9ce93ee4e519ee13
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101925800"
---
# <span data-ttu-id="7e137-101">Get-AzDeploymentManagerArtifactSource</span><span class="sxs-lookup"><span data-stu-id="7e137-101">Get-AzDeploymentManagerArtifactSource</span></span>

## <span data-ttu-id="7e137-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7e137-102">SYNOPSIS</span></span>

<span data-ttu-id="7e137-103">Ruft die Artefaktquelle ab.</span><span class="sxs-lookup"><span data-stu-id="7e137-103">Gets the Artifact source.</span></span>

## <span data-ttu-id="7e137-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="7e137-104">SYNTAX</span></span>

### <span data-ttu-id="7e137-105">Interaktiv (Standard)</span><span class="sxs-lookup"><span data-stu-id="7e137-105">Interactive (Default)</span></span>
```
Get-AzDeploymentManagerArtifactSource [-ResourceGroupName] <String> [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="7e137-106">ResourceId</span><span class="sxs-lookup"><span data-stu-id="7e137-106">ResourceId</span></span>
```
Get-AzDeploymentManagerArtifactSource [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="7e137-107">InputObject</span><span class="sxs-lookup"><span data-stu-id="7e137-107">InputObject</span></span>
```
Get-AzDeploymentManagerArtifactSource [-InputObject] <PSArtifactSource>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="7e137-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="7e137-108">DESCRIPTION</span></span>
<span data-ttu-id="7e137-109">Das **Get-AzDeploymentManagerArtifactSource-Cmdlet** ruft eine Artefaktquelle ab und gibt ein Objekt zurück, das diese Artefaktquelle darstellt.</span><span class="sxs-lookup"><span data-stu-id="7e137-109">The **Get-AzDeploymentManagerArtifactSource** cmdlet gets an artifact source, and returns an object that represents that artifact source.</span></span>
<span data-ttu-id="7e137-110">Geben Sie die Artefaktquelle nach dem Namen und dem Ressourcengruppennamen an.</span><span class="sxs-lookup"><span data-stu-id="7e137-110">Specify the artifact source by its name and resource group name.</span></span> <span data-ttu-id="7e137-111">Alternativ können Sie das ArtifactSource-Objekt oder die ResourceId bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="7e137-111">Alternately, you can provide the ArtifactSource object or the ResourceId.</span></span>

## <span data-ttu-id="7e137-112">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="7e137-112">EXAMPLES</span></span>

### <span data-ttu-id="7e137-113">Beispiel 1: Erhalten einer Artefaktquelle</span><span class="sxs-lookup"><span data-stu-id="7e137-113">Example 1: Get an artifact source</span></span>
```powershell
PS C:\> Get-AzDeploymentManagerArtifactSource -ResourceGroupName "ContosoResourceGroup" -Name "ContosoArtifactSource"
```

<span data-ttu-id="7e137-114">Dieser Befehl ruft eine Artefaktquelle mit dem Namen ContosoArtifactSource in ContosoResourceGroup ab.</span><span class="sxs-lookup"><span data-stu-id="7e137-114">This command gets an artifact source named ContosoArtifactSource in ContosoResourceGroup.</span></span>

### <span data-ttu-id="7e137-115">Beispiel 2: Erhalten einer Artefaktquelle mithilfe des Ressourcenbezeichners</span><span class="sxs-lookup"><span data-stu-id="7e137-115">Example 2: Get an artifact source using the resource identifier</span></span>
```powershell
PS C:\> Get-AzDeploymentManagerArtifactSource -ResourceId "/subscriptions/subscriptionId/resourcegroups/ContosoResourceGroup/providers/Microsoft.DeploymentManager/artifactSources/ContosoArtifactSource"
```

<span data-ttu-id="7e137-116">Dieser Befehl ruft eine Artefaktquelle mit dem Namen ContosoArtifactSource in ContosoResourceGroup ab.</span><span class="sxs-lookup"><span data-stu-id="7e137-116">This command gets an artifact source named ContosoArtifactSource in ContosoResourceGroup.</span></span>

### <span data-ttu-id="7e137-117">Beispiel 3: Erhalten einer Artefaktquelle mithilfe eines objekts, das von der New-AzDeploymentManagerArtifactSource</span><span class="sxs-lookup"><span data-stu-id="7e137-117">Example 3: Get an artifact source using an object returned by New-AzDeploymentManagerArtifactSource</span></span>
```powershell
PS C:\> Get-AzDeploymentManagerArtifactSource -InputObject $artifactSourceObject
```

<span data-ttu-id="7e137-118">Dieser Befehl ruft eine Artefaktquelle ab, deren Name und Ressourcengruppe den Eigenschaften Name und ResourceGroupName des $artifactSourceObject entsprechen.</span><span class="sxs-lookup"><span data-stu-id="7e137-118">This command gets an artifact source whose name and ResourceGroup match the Name and ResourceGroupName properties of the $artifactSourceObject, respectively.</span></span>

## <span data-ttu-id="7e137-119">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="7e137-119">PARAMETERS</span></span>

### <span data-ttu-id="7e137-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7e137-120">-DefaultProfile</span></span>
<span data-ttu-id="7e137-121">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="7e137-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7e137-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="7e137-122">-InputObject</span></span>
<span data-ttu-id="7e137-123">Artefaktquelle-Objekt.</span><span class="sxs-lookup"><span data-stu-id="7e137-123">Artifact Source object.</span></span>

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

### <span data-ttu-id="7e137-124">-Name</span><span class="sxs-lookup"><span data-stu-id="7e137-124">-Name</span></span>
<span data-ttu-id="7e137-125">Der Name der Artefaktquelle.</span><span class="sxs-lookup"><span data-stu-id="7e137-125">The name of the artifact source.</span></span>

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

### <span data-ttu-id="7e137-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7e137-126">-ResourceGroupName</span></span>
<span data-ttu-id="7e137-127">Die Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="7e137-127">The resource group.</span></span>

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

### <span data-ttu-id="7e137-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="7e137-128">-ResourceId</span></span>
<span data-ttu-id="7e137-129">Der Ressourcenbezeichner.</span><span class="sxs-lookup"><span data-stu-id="7e137-129">The resource identifier.</span></span>

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

### <span data-ttu-id="7e137-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7e137-130">CommonParameters</span></span>
<span data-ttu-id="7e137-131">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7e137-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7e137-132">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="7e137-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7e137-133">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="7e137-133">INPUTS</span></span>

### <span data-ttu-id="7e137-134">System.String</span><span class="sxs-lookup"><span data-stu-id="7e137-134">System.String</span></span>

### <span data-ttu-id="7e137-135">Microsoft.Azure.Commands.DeploymentManager.Models.PSArtifactSource</span><span class="sxs-lookup"><span data-stu-id="7e137-135">Microsoft.Azure.Commands.DeploymentManager.Models.PSArtifactSource</span></span>

## <span data-ttu-id="7e137-136">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="7e137-136">OUTPUTS</span></span>

### <span data-ttu-id="7e137-137">Microsoft.Azure.Commands.DeploymentManager.Models.PSArtifactSource</span><span class="sxs-lookup"><span data-stu-id="7e137-137">Microsoft.Azure.Commands.DeploymentManager.Models.PSArtifactSource</span></span>

## <span data-ttu-id="7e137-138">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="7e137-138">NOTES</span></span>

## <span data-ttu-id="7e137-139">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="7e137-139">RELATED LINKS</span></span>
