---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DeploymentManager.dll-Help.xml
Module Name: Az.DeploymentManager
online version: https://docs.microsoft.com/powershell/module/az.deploymentmanager/set-azdeploymentmanagerartifactsource
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeploymentManager/DeploymentManager/help/Set-AzDeploymentManagerArtifactSource.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeploymentManager/DeploymentManager/help/Set-AzDeploymentManagerArtifactSource.md
ms.openlocfilehash: 9d5d79f65adbcab7ce61ad125e78189d0f84f9a7
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101932912"
---
# <span data-ttu-id="329cd-101">Set-AzDeploymentManagerArtifactSource</span><span class="sxs-lookup"><span data-stu-id="329cd-101">Set-AzDeploymentManagerArtifactSource</span></span>

## <span data-ttu-id="329cd-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="329cd-102">SYNOPSIS</span></span>
<span data-ttu-id="329cd-103">Aktualisiert die Artefaktquelle.</span><span class="sxs-lookup"><span data-stu-id="329cd-103">Updates the artifacts source.</span></span>

## <span data-ttu-id="329cd-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="329cd-104">SYNTAX</span></span>

```
Set-AzDeploymentManagerArtifactSource [-InputObject] <PSArtifactSource>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="329cd-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="329cd-105">DESCRIPTION</span></span>
<span data-ttu-id="329cd-106">Das **Cmdlet Set-AzDeploymentManagerArtifactSource** aktualisiert eine Artefaktquelle mit dem angegebenen Artefaktquelleobjekt.</span><span class="sxs-lookup"><span data-stu-id="329cd-106">The **Set-AzDeploymentManagerArtifactSource** cmdlet updates an artifact source with the specified artifact source object.</span></span>
<span data-ttu-id="329cd-107">Das Cmdlet gibt das aktualisierte ArtifactSource-Objekt zurück.</span><span class="sxs-lookup"><span data-stu-id="329cd-107">The cmdlet returns the updated ArtifactSource object.</span></span>

## <span data-ttu-id="329cd-108">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="329cd-108">EXAMPLES</span></span>

### <span data-ttu-id="329cd-109">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="329cd-109">Example 1</span></span>
```powershell
PS C:\> Get-AzDeploymentManagerArtifactSource -InputObject $artifactSourceObject
```

<span data-ttu-id="329cd-110">Mit diesem Befehl wird eine Artefaktquelle aktualisiert, deren Name und Ressourcengruppe den Eigenschaften Name und ResourceGroupName des $artifactSourceObject entsprechen.</span><span class="sxs-lookup"><span data-stu-id="329cd-110">This command updates an artifact source whose name and ResourceGroup match the Name and ResourceGroupName properties of the $artifactSourceObject, respectively.</span></span>
<span data-ttu-id="329cd-111">Die Artefaktquelle wird auf die Eigenschaften aktualisiert, die in der Liste $artifactSourceObject.</span><span class="sxs-lookup"><span data-stu-id="329cd-111">The artifact source would be updated to the properties set in the $artifactSourceObject.</span></span>

## <span data-ttu-id="329cd-112">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="329cd-112">PARAMETERS</span></span>

### <span data-ttu-id="329cd-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="329cd-113">-DefaultProfile</span></span>
<span data-ttu-id="329cd-114">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="329cd-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="329cd-115">-InputObject</span><span class="sxs-lookup"><span data-stu-id="329cd-115">-InputObject</span></span>
<span data-ttu-id="329cd-116">Das Artefaktquelleobjekt.</span><span class="sxs-lookup"><span data-stu-id="329cd-116">The artifact source object.</span></span>

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

### <span data-ttu-id="329cd-117">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="329cd-117">-Confirm</span></span>
<span data-ttu-id="329cd-118">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="329cd-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="329cd-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="329cd-119">-WhatIf</span></span>
<span data-ttu-id="329cd-120">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="329cd-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="329cd-121">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="329cd-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="329cd-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="329cd-122">CommonParameters</span></span>
<span data-ttu-id="329cd-123">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="329cd-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="329cd-124">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="329cd-124">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="329cd-125">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="329cd-125">INPUTS</span></span>

### <span data-ttu-id="329cd-126">Microsoft.Azure.Commands.DeploymentManager.Models.PSArtifactSource</span><span class="sxs-lookup"><span data-stu-id="329cd-126">Microsoft.Azure.Commands.DeploymentManager.Models.PSArtifactSource</span></span>

## <span data-ttu-id="329cd-127">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="329cd-127">OUTPUTS</span></span>

### <span data-ttu-id="329cd-128">Microsoft.Azure.Commands.DeploymentManager.Models.PSArtifactSource</span><span class="sxs-lookup"><span data-stu-id="329cd-128">Microsoft.Azure.Commands.DeploymentManager.Models.PSArtifactSource</span></span>

## <span data-ttu-id="329cd-129">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="329cd-129">NOTES</span></span>

## <span data-ttu-id="329cd-130">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="329cd-130">RELATED LINKS</span></span>
