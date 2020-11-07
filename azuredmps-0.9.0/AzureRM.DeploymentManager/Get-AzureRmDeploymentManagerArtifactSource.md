---
external help file: Microsoft.Azure.Commands.DeploymentManager.dll-Help.xml
Module Name: AzureRM.DeploymentManager
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.deploymentmanager/get-azurermdeploymentmanagerartifactsource
schema: 2.0.0
ms.openlocfilehash: baf5059d3a952e90422f3e16d83634291aa87614
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93661988"
---
# <span data-ttu-id="c9326-101">Get-AzureRmDeploymentManagerArtifactSource</span><span class="sxs-lookup"><span data-stu-id="c9326-101">Get-AzureRmDeploymentManagerArtifactSource</span></span>

## <span data-ttu-id="c9326-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="c9326-102">SYNOPSIS</span></span>
<span data-ttu-id="c9326-103">Ruft eine Artefakt-Quelle ab.</span><span class="sxs-lookup"><span data-stu-id="c9326-103">Gets an artifact source.</span></span>

## <span data-ttu-id="c9326-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="c9326-104">SYNTAX</span></span>

### <span data-ttu-id="c9326-105">Interaktiv (Standard)</span><span class="sxs-lookup"><span data-stu-id="c9326-105">Interactive (Default)</span></span>
```
Get-AzureRmDeploymentManagerArtifactSource [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c9326-106">ResourceId</span><span class="sxs-lookup"><span data-stu-id="c9326-106">ResourceId</span></span>
```
Get-AzureRmDeploymentManagerArtifactSource [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="c9326-107">InputObject</span><span class="sxs-lookup"><span data-stu-id="c9326-107">InputObject</span></span>
```
Get-AzureRmDeploymentManagerArtifactSource [-ArtifactSource] <PSArtifactSource>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c9326-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="c9326-108">DESCRIPTION</span></span>
<span data-ttu-id="c9326-109">Das Cmdlet " **Get-AzureRmDeploymentManagerArtifactSource** " Ruft eine Artefakt-Quelle ab und gibt ein Objekt zurück, das diese Artefakt-Quelle darstellt.</span><span class="sxs-lookup"><span data-stu-id="c9326-109">The **Get-AzureRmDeploymentManagerArtifactSource** cmdlet gets an artifact source, and returns an object that represents that artifact source.</span></span>
<span data-ttu-id="c9326-110">Geben Sie die Artefakt-Quelle anhand des Namens und des Ressourcengruppen namens an.</span><span class="sxs-lookup"><span data-stu-id="c9326-110">Specify the artifact source by its name and resource group name.</span></span> <span data-ttu-id="c9326-111">Alternativ können Sie das ArtifactSource-Objekt oder die resourcecode-Objekt bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="c9326-111">Alternately, you can provide the ArtifactSource object or the ResourceId.</span></span>

<span data-ttu-id="c9326-112">Sie können dieses Objekt lokal ändern und dann mithilfe des Set-AzureRmDeploymentManagerArtifactSource-Cmdlets Änderungen an der Artefakt-Quelle übernehmen.</span><span class="sxs-lookup"><span data-stu-id="c9326-112">You can modify this object locally, and then apply changes to the artifact source by using the Set-AzureRmDeploymentManagerArtifactSource cmdlet.</span></span>

## <span data-ttu-id="c9326-113">Beispiele</span><span class="sxs-lookup"><span data-stu-id="c9326-113">EXAMPLES</span></span>

### <span data-ttu-id="c9326-114">Beispiel 1: Abrufen einer Artefakt-Quelle</span><span class="sxs-lookup"><span data-stu-id="c9326-114">Example 1: Get an artifact source</span></span>
```powershell
PS C:\> Get-AzureRmDeploymentManagerArtifactSource -ResourceGroupName "ContosoResourceGroup" -Name "ContosoArtifactSource"
```

<span data-ttu-id="c9326-115">Dieser Befehl ruft eine Artefakt-Quelle mit dem Namen ContosoArtifactSource in ContosoResourceGroup ab.</span><span class="sxs-lookup"><span data-stu-id="c9326-115">This command gets an artifact source named ContosoArtifactSource in ContosoResourceGroup.</span></span>

### <span data-ttu-id="c9326-116">Beispiel 2: Abrufen einer Artefakt-Quelle mit dem Ressourcenbezeichner</span><span class="sxs-lookup"><span data-stu-id="c9326-116">Example 2: Get an artifact source using the resource identifier</span></span>
```powershell
PS C:\> Get-AzureRmDeploymentManagerArtifactSource -ResourceId "/subscriptions/subscriptionId/resourcegroups/ContosoResourceGroup/providers/Microsoft.DeploymentManager/artifactSources/ContosoArtifactSource"
```

<span data-ttu-id="c9326-117">Dieser Befehl ruft eine Artefakt-Quelle mit dem Namen ContosoArtifactSource in ContosoResourceGroup ab.</span><span class="sxs-lookup"><span data-stu-id="c9326-117">This command gets an artifact source named ContosoArtifactSource in ContosoResourceGroup.</span></span>

### <span data-ttu-id="c9326-118">Beispiel 3: Abrufen einer Artefakt-Quelle mit einem von New-AzureRmDeploymentManagerArtifactSource zurückgegebenen Objekt</span><span class="sxs-lookup"><span data-stu-id="c9326-118">Example 3: Get an artifact source using an object returned by New-AzureRmDeploymentManagerArtifactSource</span></span>
```powershell
PS C:\> Get-AzureRmDeploymentManagerArtifactSource -ArtifactSource $artifactSourceObject
```

<span data-ttu-id="c9326-119">Dieser Befehl ruft eine Artefakt-Quelle ab, deren Name und ResourceGroup den Namen-und ResourceGroupName-Eigenschaften der $artifactSourceObject entsprechen.</span><span class="sxs-lookup"><span data-stu-id="c9326-119">This command gets an artifact source whose name and ResourceGroup match the Name and ResourceGroupName properties of the $artifactSourceObject, respectively.</span></span>

## <span data-ttu-id="c9326-120">Parameter</span><span class="sxs-lookup"><span data-stu-id="c9326-120">PARAMETERS</span></span>

### <span data-ttu-id="c9326-121">-ArtifactSource</span><span class="sxs-lookup"><span data-stu-id="c9326-121">-ArtifactSource</span></span>
<span data-ttu-id="c9326-122">Artefakt-Quellobjekt.</span><span class="sxs-lookup"><span data-stu-id="c9326-122">Artifact Source object.</span></span>

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

### <span data-ttu-id="c9326-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c9326-123">-DefaultProfile</span></span>
<span data-ttu-id="c9326-124">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="c9326-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c9326-125">-Name</span><span class="sxs-lookup"><span data-stu-id="c9326-125">-Name</span></span>
<span data-ttu-id="c9326-126">Der Name der Artefakt-Quelle.</span><span class="sxs-lookup"><span data-stu-id="c9326-126">The name of the artifact source.</span></span>

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

### <span data-ttu-id="c9326-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c9326-127">-ResourceGroupName</span></span>
<span data-ttu-id="c9326-128">Die Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="c9326-128">The resource group.</span></span>

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

### <span data-ttu-id="c9326-129">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="c9326-129">-ResourceId</span></span>
<span data-ttu-id="c9326-130">Der Ressourcenbezeichner.</span><span class="sxs-lookup"><span data-stu-id="c9326-130">The resource identifier.</span></span>

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

### <span data-ttu-id="c9326-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c9326-131">CommonParameters</span></span>
<span data-ttu-id="c9326-132">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c9326-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c9326-133">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c9326-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c9326-134">Eingaben</span><span class="sxs-lookup"><span data-stu-id="c9326-134">INPUTS</span></span>

### <span data-ttu-id="c9326-135">Keine</span><span class="sxs-lookup"><span data-stu-id="c9326-135">None</span></span>

## <span data-ttu-id="c9326-136">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="c9326-136">OUTPUTS</span></span>

### <span data-ttu-id="c9326-137">Microsoft. Azure. Commands. deploymentmanager. Models. PSArtifactSource</span><span class="sxs-lookup"><span data-stu-id="c9326-137">Microsoft.Azure.Commands.DeploymentManager.Models.PSArtifactSource</span></span>

## <span data-ttu-id="c9326-138">Notizen</span><span class="sxs-lookup"><span data-stu-id="c9326-138">NOTES</span></span>

## <span data-ttu-id="c9326-139">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="c9326-139">RELATED LINKS</span></span>

[<span data-ttu-id="c9326-140">Neu – AzureRmDeploymentManagerArtifactSource</span><span class="sxs-lookup"><span data-stu-id="c9326-140">New-AzureRmDeploymentManagerArtifactSource</span></span>](./New-AzureRmDeploymentManagerArtifactSource.md)

[<span data-ttu-id="c9326-141">Remove-AzureRmDeploymentManagerArtifactSource</span><span class="sxs-lookup"><span data-stu-id="c9326-141">Remove-AzureRmDeploymentManagerArtifactSource</span></span>](./Remove-AzureRmDeploymentManagerArtifactSource.md)

[<span data-ttu-id="c9326-142">Satz-AzureRmDeploymentManagerArtifactSource</span><span class="sxs-lookup"><span data-stu-id="c9326-142">Set-AzureRmDeploymentManagerArtifactSource</span></span>](./Set-AzureRmDeploymentManagerArtifactSource.md)