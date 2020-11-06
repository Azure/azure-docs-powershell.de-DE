---
external help file: Microsoft.Azure.Commands.DeploymentManager.dll-Help.xml
Module Name: AzureRM.DeploymentManager
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.deploymentmanager/set-azurermdeploymentmanagerartifactsource
schema: 2.0.0
ms.openlocfilehash: 230e443fad4740b6bf9896164f02ae9b382e3ed2
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93474989"
---
# <span data-ttu-id="0590b-101">Set-AzureRmDeploymentManagerArtifactSource</span><span class="sxs-lookup"><span data-stu-id="0590b-101">Set-AzureRmDeploymentManagerArtifactSource</span></span>

## <span data-ttu-id="0590b-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="0590b-102">SYNOPSIS</span></span>
<span data-ttu-id="0590b-103">Aktualisiert eine Artefakt-Quelle.</span><span class="sxs-lookup"><span data-stu-id="0590b-103">Updates an artifact source.</span></span>

## <span data-ttu-id="0590b-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="0590b-104">SYNTAX</span></span>

```
Set-AzureRmDeploymentManagerArtifactSource [-ArtifactSource] <PSArtifactSource>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0590b-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="0590b-105">DESCRIPTION</span></span>
<span data-ttu-id="0590b-106">Das Cmdlet " **Satz-AzureRmDeploymentManagerArtifactSource** " aktualisiert eine Artefakt-Quelle mit dem angegebenen Artefakt-Quellobjekt.</span><span class="sxs-lookup"><span data-stu-id="0590b-106">The **Set-AzureRmDeploymentManagerArtifactSource** cmdlet updates an artifact source with the specified artifact source object.</span></span>
<span data-ttu-id="0590b-107">Das Cmdlet gibt das aktualisierte ArtifactSource-Objekt zurück.</span><span class="sxs-lookup"><span data-stu-id="0590b-107">The cmdlet returns the updated ArtifactSource object.</span></span>

## <span data-ttu-id="0590b-108">Beispiele</span><span class="sxs-lookup"><span data-stu-id="0590b-108">EXAMPLES</span></span>

### <span data-ttu-id="0590b-109">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="0590b-109">Example 1</span></span>
```powershell
PS C:\> Get-AzureRmDeploymentManagerArtifactSource -ArtifactSource $artifactSourceObject
```

<span data-ttu-id="0590b-110">Mit diesem Befehl wird eine Artefakt-Quelle aktualisiert, deren Name und ResourceGroup den Namen-und ResourceGroupName-Eigenschaften der $artifactSourceObject entsprechen.</span><span class="sxs-lookup"><span data-stu-id="0590b-110">This command updates an artifact source whose name and ResourceGroup match the Name and ResourceGroupName properties of the $artifactSourceObject, respectively.</span></span>
<span data-ttu-id="0590b-111">Die Artefakt-Quelle würde auf die Eigenschaften aktualisiert, die im $artifactSourceObject gesetzt sind.</span><span class="sxs-lookup"><span data-stu-id="0590b-111">The artifact source would be updated to the properties set in the $artifactSourceObject.</span></span>

## <span data-ttu-id="0590b-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="0590b-112">PARAMETERS</span></span>

### <span data-ttu-id="0590b-113">-ArtifactSource</span><span class="sxs-lookup"><span data-stu-id="0590b-113">-ArtifactSource</span></span>
<span data-ttu-id="0590b-114">Das Artefakt-Quellobjekt.</span><span class="sxs-lookup"><span data-stu-id="0590b-114">The artifact source object.</span></span>

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

### <span data-ttu-id="0590b-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0590b-115">-DefaultProfile</span></span>
<span data-ttu-id="0590b-116">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="0590b-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0590b-117">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="0590b-117">-Confirm</span></span>
<span data-ttu-id="0590b-118">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="0590b-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0590b-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0590b-119">-WhatIf</span></span>
<span data-ttu-id="0590b-120">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="0590b-120">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="0590b-121">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="0590b-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0590b-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0590b-122">CommonParameters</span></span>
<span data-ttu-id="0590b-123">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0590b-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0590b-124">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0590b-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0590b-125">Eingaben</span><span class="sxs-lookup"><span data-stu-id="0590b-125">INPUTS</span></span>

### <span data-ttu-id="0590b-126">Microsoft. Azure. Commands. deploymentmanager. Models. PSArtifactSource</span><span class="sxs-lookup"><span data-stu-id="0590b-126">Microsoft.Azure.Commands.DeploymentManager.Models.PSArtifactSource</span></span>

## <span data-ttu-id="0590b-127">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="0590b-127">OUTPUTS</span></span>

### <span data-ttu-id="0590b-128">Microsoft. Azure. Commands. deploymentmanager. Models. PSArtifactSource</span><span class="sxs-lookup"><span data-stu-id="0590b-128">Microsoft.Azure.Commands.DeploymentManager.Models.PSArtifactSource</span></span>

## <span data-ttu-id="0590b-129">Notizen</span><span class="sxs-lookup"><span data-stu-id="0590b-129">NOTES</span></span>

## <span data-ttu-id="0590b-130">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="0590b-130">RELATED LINKS</span></span>

[<span data-ttu-id="0590b-131">Neu – AzureRmDeploymentManagerArtifactSource</span><span class="sxs-lookup"><span data-stu-id="0590b-131">New-AzureRmDeploymentManagerArtifactSource</span></span>](./New-AzureRmDeploymentManagerArtifactSource.md)

[<span data-ttu-id="0590b-132">Get-AzureRmDeploymentManagerArtifactSource</span><span class="sxs-lookup"><span data-stu-id="0590b-132">Get-AzureRmDeploymentManagerArtifactSource</span></span>](./Get-AzureRmDeploymentManagerArtifactSource.md)

[<span data-ttu-id="0590b-133">Remove-AzureRmDeploymentManagerArtifactSource</span><span class="sxs-lookup"><span data-stu-id="0590b-133">Remove-AzureRmDeploymentManagerArtifactSource</span></span>](./Remove-AzureRmDeploymentManagerArtifactSource.md)