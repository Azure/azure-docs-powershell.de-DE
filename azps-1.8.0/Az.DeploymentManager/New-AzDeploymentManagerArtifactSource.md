---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DeploymentManager.dll-Help.xml
Module Name: Az.DeploymentManager
online version: https://docs.microsoft.com/en-us/powershell/module/az.deploymentmanager/new-azdeploymentmanagerartifactsource
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeploymentManager/DeploymentManager/help/New-AzDeploymentManagerArtifactSource.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeploymentManager/DeploymentManager/help/New-AzDeploymentManagerArtifactSource.md
ms.openlocfilehash: 09feb94b046ef6a41130c26ae5e7b996ecbd8771
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93661206"
---
# <span data-ttu-id="bc15f-101">New-AzDeploymentManagerArtifactSource</span><span class="sxs-lookup"><span data-stu-id="bc15f-101">New-AzDeploymentManagerArtifactSource</span></span>

## <span data-ttu-id="bc15f-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="bc15f-102">SYNOPSIS</span></span>
<span data-ttu-id="bc15f-103">Erstellt eine Artefakt-Quelle.</span><span class="sxs-lookup"><span data-stu-id="bc15f-103">Creates an artifact source.</span></span>

## <span data-ttu-id="bc15f-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="bc15f-104">SYNTAX</span></span>

```
New-AzDeploymentManagerArtifactSource -ResourceGroupName <String> -Name <String> -Location <String>
 -SasUri <String> [-Tag <Hashtable>] [-ArtifactRoot <String>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="bc15f-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="bc15f-105">DESCRIPTION</span></span>
<span data-ttu-id="bc15f-106">Das Cmdlet **New-AzDeploymentManagerArtifactSource** erstellt eine Artefakt-Quelle.</span><span class="sxs-lookup"><span data-stu-id="bc15f-106">The **New-AzDeploymentManagerArtifactSource** cmdlet creates an artifact source.</span></span>
<span data-ttu-id="bc15f-107">Geben Sie den *Namen* , die *ResourceGroupName* und die erforderlichen Eigenschaften an.</span><span class="sxs-lookup"><span data-stu-id="bc15f-107">Specify the *Name* , *ResourceGroupName* and required properties.</span></span>

<span data-ttu-id="bc15f-108">Sie können das zurückgegebene Objekt lokal ändern und dann mithilfe des Set-AzDeploymentManagerArtifactSource-Cmdlets die Änderungen auf die Artefakt-Quelle anwenden.</span><span class="sxs-lookup"><span data-stu-id="bc15f-108">You can modify the returned object locally and then apply the changes to the artifact source by using the Set-AzDeploymentManagerArtifactSource cmdlet.</span></span>

<span data-ttu-id="bc15f-109">Das Cmdlet gibt ein ArtifactSource-Objekt zurück, auf das im New-AzDeloymentManagerServiceTopology-Cmdlet verwiesen werden kann, damit Artefakte, die für eine Serviceunit-Ressource, die Vorlagen-und Parameterdateien, benötigt werden, von diesem Speicherort referenziert werden können.</span><span class="sxs-lookup"><span data-stu-id="bc15f-109">The cmdlet returns an ArtifactSource object that has a ResourceId which can be referenced in the New-AzDeloymentManagerServiceTopology cmdlet so that artifacts required for a ServiceUnit resource, the Template and Parameters files, can be referenced from this location.</span></span>

## <span data-ttu-id="bc15f-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="bc15f-110">EXAMPLES</span></span>

### <span data-ttu-id="bc15f-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="bc15f-111">Example 1</span></span>
```powershell
PS C:\> New-AzDeploymentManagerArtifactSource -ResourceGroupName ContosoResourceGroup -Name ContosoArtifactSource -Location "Central US" -SasUri "https://ContosoStorage.blob.core.windows.net/ContosoArtifacts?sasParameters"
```

<span data-ttu-id="bc15f-112">Erstellt eine Artefakt-Quelle im ContosoResourceGroup mit dem Namen ContosoArtifactSource mit dem zentralen US-Code als Speicherort der Ressource.</span><span class="sxs-lookup"><span data-stu-id="bc15f-112">Creates an artifact source in the ContosoResourceGroup with the name ContosoArtifactSource with Central US as the location of the resource.</span></span> <span data-ttu-id="bc15f-113">Die SasUri-Eigenschaft stellt einen Azure-Speicher-SAS-URI für den Speichercontainer bereit, in dem die Artefakte gespeichert werden.</span><span class="sxs-lookup"><span data-stu-id="bc15f-113">The SasUri property provides an Azure Storage SAS Uri to the storage container where the artifacts are stored.</span></span>

## <span data-ttu-id="bc15f-114">Parameter</span><span class="sxs-lookup"><span data-stu-id="bc15f-114">PARAMETERS</span></span>

### <span data-ttu-id="bc15f-115">-ArtifactRoot</span><span class="sxs-lookup"><span data-stu-id="bc15f-115">-ArtifactRoot</span></span>
<span data-ttu-id="bc15f-116">Der optionale Verzeichnis Offset unter dem Speichercontainer für die Artefakte.</span><span class="sxs-lookup"><span data-stu-id="bc15f-116">The optional directory offset under the storage container for the artifacts.</span></span>

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

### <span data-ttu-id="bc15f-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bc15f-117">-DefaultProfile</span></span>
<span data-ttu-id="bc15f-118">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="bc15f-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="bc15f-119">-Standort</span><span class="sxs-lookup"><span data-stu-id="bc15f-119">-Location</span></span>
<span data-ttu-id="bc15f-120">Der Speicherort der Ressource.</span><span class="sxs-lookup"><span data-stu-id="bc15f-120">The location of the resource.</span></span>

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

### <span data-ttu-id="bc15f-121">-Name</span><span class="sxs-lookup"><span data-stu-id="bc15f-121">-Name</span></span>
<span data-ttu-id="bc15f-122">Der Name der Artefakt-Quelle.</span><span class="sxs-lookup"><span data-stu-id="bc15f-122">The name of the artifact source.</span></span>

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

### <span data-ttu-id="bc15f-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bc15f-123">-ResourceGroupName</span></span>
<span data-ttu-id="bc15f-124">Die Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="bc15f-124">The resource group.</span></span>

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

### <span data-ttu-id="bc15f-125">-SasUri</span><span class="sxs-lookup"><span data-stu-id="bc15f-125">-SasUri</span></span>
<span data-ttu-id="bc15f-126">Der SAS-URI für den Azure-Speichercontainer, in dem die Artefakte gespeichert werden.</span><span class="sxs-lookup"><span data-stu-id="bc15f-126">The SAS Uri to the Azure storage container where the artifacts are stored.</span></span>

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

### <span data-ttu-id="bc15f-127">-Tag</span><span class="sxs-lookup"><span data-stu-id="bc15f-127">-Tag</span></span>
<span data-ttu-id="bc15f-128">Eine Hashtabelle, die Ressourcenkategorien darstellt.</span><span class="sxs-lookup"><span data-stu-id="bc15f-128">A hash table which represents resource tags.</span></span>

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

### <span data-ttu-id="bc15f-129">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="bc15f-129">-Confirm</span></span>
<span data-ttu-id="bc15f-130">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="bc15f-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="bc15f-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="bc15f-131">-WhatIf</span></span>
<span data-ttu-id="bc15f-132">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="bc15f-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="bc15f-133">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="bc15f-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="bc15f-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bc15f-134">CommonParameters</span></span>
<span data-ttu-id="bc15f-135">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bc15f-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bc15f-136">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bc15f-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bc15f-137">Eingaben</span><span class="sxs-lookup"><span data-stu-id="bc15f-137">INPUTS</span></span>

### <span data-ttu-id="bc15f-138">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="bc15f-138">System.Collections.Hashtable</span></span>

## <span data-ttu-id="bc15f-139">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="bc15f-139">OUTPUTS</span></span>

### <span data-ttu-id="bc15f-140">Microsoft. Azure. Commands. deploymentmanager. Models. PSArtifactSource</span><span class="sxs-lookup"><span data-stu-id="bc15f-140">Microsoft.Azure.Commands.DeploymentManager.Models.PSArtifactSource</span></span>

## <span data-ttu-id="bc15f-141">Notizen</span><span class="sxs-lookup"><span data-stu-id="bc15f-141">NOTES</span></span>

## <span data-ttu-id="bc15f-142">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="bc15f-142">RELATED LINKS</span></span>
