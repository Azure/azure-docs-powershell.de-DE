---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DeploymentManager.dll-Help.xml
Module Name: Az.DeploymentManager
online version: https://docs.microsoft.com/powershell/module/az.deploymentmanager/new-azdeploymentmanagerartifactsource
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeploymentManager/DeploymentManager/help/New-AzDeploymentManagerArtifactSource.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeploymentManager/DeploymentManager/help/New-AzDeploymentManagerArtifactSource.md
ms.openlocfilehash: 8aab061d7f61605273bd7147dc5a85ca45bf8ad0
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101925776"
---
# <span data-ttu-id="d66c1-101">New-AzDeploymentManagerArtifactSource</span><span class="sxs-lookup"><span data-stu-id="d66c1-101">New-AzDeploymentManagerArtifactSource</span></span>

## <span data-ttu-id="d66c1-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d66c1-102">SYNOPSIS</span></span>
<span data-ttu-id="d66c1-103">Erstellt eine Artefaktquelle.</span><span class="sxs-lookup"><span data-stu-id="d66c1-103">Creates an artifact source.</span></span>

## <span data-ttu-id="d66c1-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="d66c1-104">SYNTAX</span></span>

```
New-AzDeploymentManagerArtifactSource -ResourceGroupName <String> -Name <String> -Location <String>
 -SasUri <String> [-Tag <Hashtable>] [-ArtifactRoot <String>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d66c1-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="d66c1-105">DESCRIPTION</span></span>
<span data-ttu-id="d66c1-106">Das **Cmdlet New-AzDeploymentManagerArtifactSource** erstellt eine Artefaktquelle.</span><span class="sxs-lookup"><span data-stu-id="d66c1-106">The **New-AzDeploymentManagerArtifactSource** cmdlet creates an artifact source.</span></span>
<span data-ttu-id="d66c1-107">Geben Sie *die Eigenschaften Name*, *ResourceGroupName* und erforderliche Eigenschaften an.</span><span class="sxs-lookup"><span data-stu-id="d66c1-107">Specify the *Name*, *ResourceGroupName* and required properties.</span></span>

<span data-ttu-id="d66c1-108">Sie können das zurückgegebene Objekt lokal ändern und dann die Änderungen auf die Artefaktquelle anwenden, indem Sie das cmdlet Set-AzDeploymentManagerArtifactSource verwenden.</span><span class="sxs-lookup"><span data-stu-id="d66c1-108">You can modify the returned object locally and then apply the changes to the artifact source by using the Set-AzDeploymentManagerArtifactSource cmdlet.</span></span>

<span data-ttu-id="d66c1-109">Das Cmdlet gibt ein ArtifactSource-Objekt zurück, das über eine ResourceId verfügt, auf die im cmdlet New-AzDeploymentManagerServiceTopology verwiesen werden kann, damit von diesem Speicherort aus auf Artefakte verwiesen werden kann, die für eine ServiceUnit-Ressource, die Vorlagen- und Parameterdateien erforderlich sind.</span><span class="sxs-lookup"><span data-stu-id="d66c1-109">The cmdlet returns an ArtifactSource object that has a ResourceId which can be referenced in the New-AzDeploymentManagerServiceTopology cmdlet so that artifacts required for a ServiceUnit resource, the Template and Parameters files, can be referenced from this location.</span></span>

## <span data-ttu-id="d66c1-110">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="d66c1-110">EXAMPLES</span></span>

### <span data-ttu-id="d66c1-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="d66c1-111">Example 1</span></span>
```powershell
PS C:\> New-AzDeploymentManagerArtifactSource -ResourceGroupName ContosoResourceGroup -Name ContosoArtifactSource -Location "Central US" -SasUri "https://ContosoStorage.blob.core.windows.net/ContosoArtifacts?sasParameters"
```

<span data-ttu-id="d66c1-112">Erstellt eine Artefaktquelle in der ContosoResourceGroup mit dem Namen ContosoArtifactSource mit Central US als Speicherort der Ressource.</span><span class="sxs-lookup"><span data-stu-id="d66c1-112">Creates an artifact source in the ContosoResourceGroup with the name ContosoArtifactSource with Central US as the location of the resource.</span></span> <span data-ttu-id="d66c1-113">Die SasUri-Eigenschaft stellt einen Azure Storage SAS-Uri für den Speichercontainer bereit, in dem die Artefakte gespeichert werden.</span><span class="sxs-lookup"><span data-stu-id="d66c1-113">The SasUri property provides an Azure Storage SAS Uri to the storage container where the artifacts are stored.</span></span>

## <span data-ttu-id="d66c1-114">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="d66c1-114">PARAMETERS</span></span>

### <span data-ttu-id="d66c1-115">-ArtifactRoot</span><span class="sxs-lookup"><span data-stu-id="d66c1-115">-ArtifactRoot</span></span>
<span data-ttu-id="d66c1-116">Der optionale Verzeichnisoffset unter dem Speichercontainer für die Artefakte.</span><span class="sxs-lookup"><span data-stu-id="d66c1-116">The optional directory offset under the storage container for the artifacts.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d66c1-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d66c1-117">-DefaultProfile</span></span>
<span data-ttu-id="d66c1-118">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="d66c1-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d66c1-119">-Location</span><span class="sxs-lookup"><span data-stu-id="d66c1-119">-Location</span></span>
<span data-ttu-id="d66c1-120">Der Speicherort der Ressource.</span><span class="sxs-lookup"><span data-stu-id="d66c1-120">The location of the resource.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d66c1-121">-Name</span><span class="sxs-lookup"><span data-stu-id="d66c1-121">-Name</span></span>
<span data-ttu-id="d66c1-122">Der Name der Artefaktquelle.</span><span class="sxs-lookup"><span data-stu-id="d66c1-122">The name of the artifact source.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d66c1-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d66c1-123">-ResourceGroupName</span></span>
<span data-ttu-id="d66c1-124">Die Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="d66c1-124">The resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d66c1-125">-SasUri</span><span class="sxs-lookup"><span data-stu-id="d66c1-125">-SasUri</span></span>
<span data-ttu-id="d66c1-126">Der SAS-Uri für den Azure-Speichercontainer, in dem die Artefakte gespeichert werden.</span><span class="sxs-lookup"><span data-stu-id="d66c1-126">The SAS Uri to the Azure storage container where the artifacts are stored.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d66c1-127">-Tag</span><span class="sxs-lookup"><span data-stu-id="d66c1-127">-Tag</span></span>
<span data-ttu-id="d66c1-128">Eine Hashtabelle, die Ressourcentags darstellt.</span><span class="sxs-lookup"><span data-stu-id="d66c1-128">A hash table which represents resource tags.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d66c1-129">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="d66c1-129">-Confirm</span></span>
<span data-ttu-id="d66c1-130">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="d66c1-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d66c1-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d66c1-131">-WhatIf</span></span>
<span data-ttu-id="d66c1-132">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="d66c1-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d66c1-133">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="d66c1-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d66c1-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d66c1-134">CommonParameters</span></span>
<span data-ttu-id="d66c1-135">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d66c1-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d66c1-136">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="d66c1-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d66c1-137">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="d66c1-137">INPUTS</span></span>

### <span data-ttu-id="d66c1-138">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="d66c1-138">System.Collections.Hashtable</span></span>

## <span data-ttu-id="d66c1-139">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="d66c1-139">OUTPUTS</span></span>

### <span data-ttu-id="d66c1-140">Microsoft.Azure.Commands.DeploymentManager.Models.PSArtifactSource</span><span class="sxs-lookup"><span data-stu-id="d66c1-140">Microsoft.Azure.Commands.DeploymentManager.Models.PSArtifactSource</span></span>

## <span data-ttu-id="d66c1-141">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="d66c1-141">NOTES</span></span>

## <span data-ttu-id="d66c1-142">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="d66c1-142">RELATED LINKS</span></span>
