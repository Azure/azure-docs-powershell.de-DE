---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DeploymentManager.dll-Help.xml
Module Name: Az.DeploymentManager
online version: https://docs.microsoft.com/en-us/powershell/module/az.deploymentmanager/get-azdeploymentmanagerartifactsource
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeploymentManager/DeploymentManager/help/Get-AzDeploymentManagerArtifactSource.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeploymentManager/DeploymentManager/help/Get-AzDeploymentManagerArtifactSource.md
ms.openlocfilehash: 54cccbedc45977505b10526d4806b64c8118380e
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93661217"
---
# <span data-ttu-id="cebc0-101">Get-AzDeploymentManagerArtifactSource</span><span class="sxs-lookup"><span data-stu-id="cebc0-101">Get-AzDeploymentManagerArtifactSource</span></span>

## <span data-ttu-id="cebc0-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="cebc0-102">SYNOPSIS</span></span>

<span data-ttu-id="cebc0-103">Ruft die Artefakt-Quelle ab.</span><span class="sxs-lookup"><span data-stu-id="cebc0-103">Gets the Artifact source.</span></span>

## <span data-ttu-id="cebc0-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="cebc0-104">SYNTAX</span></span>

### <span data-ttu-id="cebc0-105">Interaktiv (Standard)</span><span class="sxs-lookup"><span data-stu-id="cebc0-105">Interactive (Default)</span></span>
```
Get-AzDeploymentManagerArtifactSource [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="cebc0-106">ResourceId</span><span class="sxs-lookup"><span data-stu-id="cebc0-106">ResourceId</span></span>
```
Get-AzDeploymentManagerArtifactSource [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="cebc0-107">InputObject</span><span class="sxs-lookup"><span data-stu-id="cebc0-107">InputObject</span></span>
```
Get-AzDeploymentManagerArtifactSource [-InputObject] <PSArtifactSource>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="cebc0-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="cebc0-108">DESCRIPTION</span></span>
<span data-ttu-id="cebc0-109">Das Cmdlet " **Get-AzDeploymentManagerArtifactSource** " Ruft eine Artefakt-Quelle ab und gibt ein Objekt zurück, das diese Artefakt-Quelle darstellt.</span><span class="sxs-lookup"><span data-stu-id="cebc0-109">The **Get-AzDeploymentManagerArtifactSource** cmdlet gets an artifact source, and returns an object that represents that artifact source.</span></span>
<span data-ttu-id="cebc0-110">Geben Sie die Artefakt-Quelle anhand des Namens und des Ressourcengruppen namens an.</span><span class="sxs-lookup"><span data-stu-id="cebc0-110">Specify the artifact source by its name and resource group name.</span></span> <span data-ttu-id="cebc0-111">Alternativ können Sie das ArtifactSource-Objekt oder die resourcecode-Objekt bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="cebc0-111">Alternately, you can provide the ArtifactSource object or the ResourceId.</span></span>

## <span data-ttu-id="cebc0-112">Beispiele</span><span class="sxs-lookup"><span data-stu-id="cebc0-112">EXAMPLES</span></span>

### <span data-ttu-id="cebc0-113">Beispiel 1: Abrufen einer Artefakt-Quelle</span><span class="sxs-lookup"><span data-stu-id="cebc0-113">Example 1: Get an artifact source</span></span>
```powershell
PS C:\> Get-AzDeploymentManagerArtifactSource -ResourceGroupName "ContosoResourceGroup" -Name "ContosoArtifactSource"
```

<span data-ttu-id="cebc0-114">Dieser Befehl ruft eine Artefakt-Quelle mit dem Namen ContosoArtifactSource in ContosoResourceGroup ab.</span><span class="sxs-lookup"><span data-stu-id="cebc0-114">This command gets an artifact source named ContosoArtifactSource in ContosoResourceGroup.</span></span>

### <span data-ttu-id="cebc0-115">Beispiel 2: Abrufen einer Artefakt-Quelle mit dem Ressourcenbezeichner</span><span class="sxs-lookup"><span data-stu-id="cebc0-115">Example 2: Get an artifact source using the resource identifier</span></span>
```powershell
PS C:\> Get-AzDeploymentManagerArtifactSource -ResourceId "/subscriptions/subscriptionId/resourcegroups/ContosoResourceGroup/providers/Microsoft.DeploymentManager/artifactSources/ContosoArtifactSource"
```

<span data-ttu-id="cebc0-116">Dieser Befehl ruft eine Artefakt-Quelle mit dem Namen ContosoArtifactSource in ContosoResourceGroup ab.</span><span class="sxs-lookup"><span data-stu-id="cebc0-116">This command gets an artifact source named ContosoArtifactSource in ContosoResourceGroup.</span></span>

### <span data-ttu-id="cebc0-117">Beispiel 3: Abrufen einer Artefakt-Quelle mit einem von New-AzDeploymentManagerArtifactSource zurückgegebenen Objekt</span><span class="sxs-lookup"><span data-stu-id="cebc0-117">Example 3: Get an artifact source using an object returned by New-AzDeploymentManagerArtifactSource</span></span>
```powershell
PS C:\> Get-AzDeploymentManagerArtifactSource -InputObject $artifactSourceObject
```

<span data-ttu-id="cebc0-118">Dieser Befehl ruft eine Artefakt-Quelle ab, deren Name und ResourceGroup den Namen-und ResourceGroupName-Eigenschaften der $artifactSourceObject entsprechen.</span><span class="sxs-lookup"><span data-stu-id="cebc0-118">This command gets an artifact source whose name and ResourceGroup match the Name and ResourceGroupName properties of the $artifactSourceObject, respectively.</span></span>

## <span data-ttu-id="cebc0-119">Parameter</span><span class="sxs-lookup"><span data-stu-id="cebc0-119">PARAMETERS</span></span>

### <span data-ttu-id="cebc0-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cebc0-120">-DefaultProfile</span></span>
<span data-ttu-id="cebc0-121">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="cebc0-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="cebc0-122">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="cebc0-122">-InputObject</span></span>
<span data-ttu-id="cebc0-123">Artefakt-Quellobjekt.</span><span class="sxs-lookup"><span data-stu-id="cebc0-123">Artifact Source object.</span></span>

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

### <span data-ttu-id="cebc0-124">-Name</span><span class="sxs-lookup"><span data-stu-id="cebc0-124">-Name</span></span>
<span data-ttu-id="cebc0-125">Der Name der Artefakt-Quelle.</span><span class="sxs-lookup"><span data-stu-id="cebc0-125">The name of the artifact source.</span></span>

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

### <span data-ttu-id="cebc0-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cebc0-126">-ResourceGroupName</span></span>
<span data-ttu-id="cebc0-127">Die Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="cebc0-127">The resource group.</span></span>

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

### <span data-ttu-id="cebc0-128">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="cebc0-128">-ResourceId</span></span>
<span data-ttu-id="cebc0-129">Der Ressourcenbezeichner.</span><span class="sxs-lookup"><span data-stu-id="cebc0-129">The resource identifier.</span></span>

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

### <span data-ttu-id="cebc0-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cebc0-130">CommonParameters</span></span>
<span data-ttu-id="cebc0-131">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cebc0-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cebc0-132">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="cebc0-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cebc0-133">Eingaben</span><span class="sxs-lookup"><span data-stu-id="cebc0-133">INPUTS</span></span>

### <span data-ttu-id="cebc0-134">System. String</span><span class="sxs-lookup"><span data-stu-id="cebc0-134">System.String</span></span>

### <span data-ttu-id="cebc0-135">Microsoft. Azure. Commands. deploymentmanager. Models. PSArtifactSource</span><span class="sxs-lookup"><span data-stu-id="cebc0-135">Microsoft.Azure.Commands.DeploymentManager.Models.PSArtifactSource</span></span>

## <span data-ttu-id="cebc0-136">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="cebc0-136">OUTPUTS</span></span>

### <span data-ttu-id="cebc0-137">Microsoft. Azure. Commands. deploymentmanager. Models. PSArtifactSource</span><span class="sxs-lookup"><span data-stu-id="cebc0-137">Microsoft.Azure.Commands.DeploymentManager.Models.PSArtifactSource</span></span>

## <span data-ttu-id="cebc0-138">Notizen</span><span class="sxs-lookup"><span data-stu-id="cebc0-138">NOTES</span></span>

## <span data-ttu-id="cebc0-139">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="cebc0-139">RELATED LINKS</span></span>
