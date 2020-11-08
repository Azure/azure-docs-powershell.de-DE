---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DeploymentManager.dll-Help.xml
Module Name: Az.DeploymentManager
online version: https://docs.microsoft.com/en-us/powershell/module/az.deploymentmanager/set-azdeploymentmanagerartifactsource
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeploymentManager/DeploymentManager/help/Set-AzDeploymentManagerArtifactSource.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeploymentManager/DeploymentManager/help/Set-AzDeploymentManagerArtifactSource.md
ms.openlocfilehash: ee69c178d48775a870b229e652a1584c413bd7ca
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/21/2020
ms.locfileid: "94004581"
---
# <span data-ttu-id="4f062-101">Set-AzDeploymentManagerArtifactSource</span><span class="sxs-lookup"><span data-stu-id="4f062-101">Set-AzDeploymentManagerArtifactSource</span></span>

## <span data-ttu-id="4f062-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="4f062-102">SYNOPSIS</span></span>
<span data-ttu-id="4f062-103">Aktualisiert die Artefakte-Quelle.</span><span class="sxs-lookup"><span data-stu-id="4f062-103">Updates the artifacts source.</span></span>

## <span data-ttu-id="4f062-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="4f062-104">SYNTAX</span></span>

```
Set-AzDeploymentManagerArtifactSource [-InputObject] <PSArtifactSource>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4f062-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="4f062-105">DESCRIPTION</span></span>
<span data-ttu-id="4f062-106">Das Cmdlet " **Satz-AzDeploymentManagerArtifactSource** " aktualisiert eine Artefakt-Quelle mit dem angegebenen Artefakt-Quellobjekt.</span><span class="sxs-lookup"><span data-stu-id="4f062-106">The **Set-AzDeploymentManagerArtifactSource** cmdlet updates an artifact source with the specified artifact source object.</span></span>
<span data-ttu-id="4f062-107">Das Cmdlet gibt das aktualisierte ArtifactSource-Objekt zurück.</span><span class="sxs-lookup"><span data-stu-id="4f062-107">The cmdlet returns the updated ArtifactSource object.</span></span>

## <span data-ttu-id="4f062-108">Beispiele</span><span class="sxs-lookup"><span data-stu-id="4f062-108">EXAMPLES</span></span>

### <span data-ttu-id="4f062-109">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="4f062-109">Example 1</span></span>
```powershell
PS C:\> Get-AzDeploymentManagerArtifactSource -InputObject $artifactSourceObject
```

<span data-ttu-id="4f062-110">Mit diesem Befehl wird eine Artefakt-Quelle aktualisiert, deren Name und ResourceGroup den Namen-und ResourceGroupName-Eigenschaften der $artifactSourceObject entsprechen.</span><span class="sxs-lookup"><span data-stu-id="4f062-110">This command updates an artifact source whose name and ResourceGroup match the Name and ResourceGroupName properties of the $artifactSourceObject, respectively.</span></span>
<span data-ttu-id="4f062-111">Die Artefakt-Quelle würde auf die Eigenschaften aktualisiert, die im $artifactSourceObject gesetzt sind.</span><span class="sxs-lookup"><span data-stu-id="4f062-111">The artifact source would be updated to the properties set in the $artifactSourceObject.</span></span>

## <span data-ttu-id="4f062-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="4f062-112">PARAMETERS</span></span>

### <span data-ttu-id="4f062-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4f062-113">-DefaultProfile</span></span>
<span data-ttu-id="4f062-114">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="4f062-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4f062-115">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="4f062-115">-InputObject</span></span>
<span data-ttu-id="4f062-116">Das Artefakt-Quellobjekt.</span><span class="sxs-lookup"><span data-stu-id="4f062-116">The artifact source object.</span></span>

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

### <span data-ttu-id="4f062-117">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="4f062-117">-Confirm</span></span>
<span data-ttu-id="4f062-118">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="4f062-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4f062-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4f062-119">-WhatIf</span></span>
<span data-ttu-id="4f062-120">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="4f062-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4f062-121">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="4f062-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4f062-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4f062-122">CommonParameters</span></span>
<span data-ttu-id="4f062-123">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4f062-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4f062-124">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="4f062-124">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4f062-125">Eingaben</span><span class="sxs-lookup"><span data-stu-id="4f062-125">INPUTS</span></span>

### <span data-ttu-id="4f062-126">Microsoft. Azure. Commands. deploymentmanager. Models. PSArtifactSource</span><span class="sxs-lookup"><span data-stu-id="4f062-126">Microsoft.Azure.Commands.DeploymentManager.Models.PSArtifactSource</span></span>

## <span data-ttu-id="4f062-127">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="4f062-127">OUTPUTS</span></span>

### <span data-ttu-id="4f062-128">Microsoft. Azure. Commands. deploymentmanager. Models. PSArtifactSource</span><span class="sxs-lookup"><span data-stu-id="4f062-128">Microsoft.Azure.Commands.DeploymentManager.Models.PSArtifactSource</span></span>

## <span data-ttu-id="4f062-129">Notizen</span><span class="sxs-lookup"><span data-stu-id="4f062-129">NOTES</span></span>

## <span data-ttu-id="4f062-130">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="4f062-130">RELATED LINKS</span></span>
