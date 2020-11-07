---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DeploymentManager.dll-Help.xml
Module Name: Az.DeploymentManager
online version: https://docs.microsoft.com/en-us/powershell/module/az.deploymentmanager/new-azdeploymentmanagerservicetopology
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeploymentManager/DeploymentManager/help/New-AzDeploymentManagerServiceTopology.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeploymentManager/DeploymentManager/help/New-AzDeploymentManagerServiceTopology.md
ms.openlocfilehash: 2ffae1a1d12b503e478e18d57a31fffddd9c10a9
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93651360"
---
# <span data-ttu-id="0c3df-101">New-AzDeploymentManagerServiceTopology</span><span class="sxs-lookup"><span data-stu-id="0c3df-101">New-AzDeploymentManagerServiceTopology</span></span>

## <span data-ttu-id="0c3df-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="0c3df-102">SYNOPSIS</span></span>
<span data-ttu-id="0c3df-103">Erstellt eine Dienst Topologie.</span><span class="sxs-lookup"><span data-stu-id="0c3df-103">Creates a service topology.</span></span>

## <span data-ttu-id="0c3df-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="0c3df-104">SYNTAX</span></span>

```
New-AzDeploymentManagerServiceTopology -ResourceGroupName <String> -Name <String> -Location <String>
 [-ArtifactSourceId <String>] [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0c3df-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="0c3df-105">DESCRIPTION</span></span>
<span data-ttu-id="0c3df-106">Das Cmdlet **New-AzDeploymentManagerServiceTopology** erstellt eine Dienst Topologie.</span><span class="sxs-lookup"><span data-stu-id="0c3df-106">The **New-AzDeploymentManagerServiceTopology** cmdlet creates a service topology.</span></span>

<span data-ttu-id="0c3df-107">Sie können das zurückgegebene ServiceTopology-Objekt lokal ändern und dann mithilfe des Set-AzDeploymentManagerServiceTopology-Cmdlets Änderungen an der Topologie vornehmen.</span><span class="sxs-lookup"><span data-stu-id="0c3df-107">You can modify the returned ServiceTopology object locally, and then apply changes to the topology by using the Set-AzDeploymentManagerServiceTopology cmdlet.</span></span>
<span data-ttu-id="0c3df-108">Das zurückgegebene Objekt</span><span class="sxs-lookup"><span data-stu-id="0c3df-108">The returned object</span></span> 

<span data-ttu-id="0c3df-109">Das zurückgegebene Objekt verfügt über ein Feld "resourcecode", auf das in einer Rollout Ressource verwiesen werden kann, um anzugeben, dass die in dieser Dienst Topologie deklarierten Dienste im Rollout bereitgestellt werden.</span><span class="sxs-lookup"><span data-stu-id="0c3df-109">The returned object has a ResourceId field which can be referenced in a rollout resource to indicate that the services declared in this service topology would be deployed in the rollout.</span></span>

## <span data-ttu-id="0c3df-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="0c3df-110">EXAMPLES</span></span>

### <span data-ttu-id="0c3df-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="0c3df-111">Example 1</span></span>
```powershell
PS C:\> New-AzDeploymentManagerServiceTopology -ResourceGroupName ContosoResourceGroup -Name ContosoServiceTopology -Location "Central US" -ArtifactSourceId "/subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourcegroups/ContosoResourceGroup/providers/Microsoft.DeploymentManager/artifactSources/ContosoArtifactSource"
```

<span data-ttu-id="0c3df-112">Mit diesem Cmdlet wird eine neue Dienst Topologie in der Ressourcengruppe ContosoResourceGroup mit dem Namen ContosoServiceTopology und in Location Central US erstellt.</span><span class="sxs-lookup"><span data-stu-id="0c3df-112">This cmdlet creates a new service topology in the resource group ContosoResourceGroup with the name ContosoServiceTopology and in location Central US.</span></span> <span data-ttu-id="0c3df-113">Die Artefakt-Quell-Resource-Funktion gibt an, dass die für die Dienst Einheits Definitionen in dieser Topologie erforderlichen Artefakte aus der angegebenen Artefakt-Quelle gelesen werden müssen.</span><span class="sxs-lookup"><span data-stu-id="0c3df-113">The artifact source ResourceId indicates that the artifacts required for the service unit definitions in this topology need to be read from the specified artifact source.</span></span>

### <span data-ttu-id="0c3df-114">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="0c3df-114">Example 2</span></span>
```powershell
PS C:\> New-AzDeploymentManagerServiceTopology -ResourceGroupName ContosoResourceGroup -Name ContosoServiceTopology -Location "Central US"
```

<span data-ttu-id="0c3df-115">Mit diesem Cmdlet wird eine neue Dienst Topologie in der Ressourcengruppe ContosoResourceGroup mit dem Namen ContosoServiceTopology und in Location Central US erstellt.</span><span class="sxs-lookup"><span data-stu-id="0c3df-115">This cmdlet creates a new service topology in the resource group ContosoResourceGroup with the name ContosoServiceTopology and in location Central US.</span></span> <span data-ttu-id="0c3df-116">Das Fehlen eines Artefakt-Quellen Verweises gibt an, dass die für die Dienst Einheits Definitionen in dieser Topologie erforderlichen Artefakte als absolute SAS-URIs in der Diensteinheit bereitgestellt werden.</span><span class="sxs-lookup"><span data-stu-id="0c3df-116">The absence of an artifact source reference indicates that the artifacts required for the service unit definitions in this topology would be provided as absolute SAS URIs in the service unit.</span></span>

## <span data-ttu-id="0c3df-117">Parameter</span><span class="sxs-lookup"><span data-stu-id="0c3df-117">PARAMETERS</span></span>

### <span data-ttu-id="0c3df-118">-ArtifactSourceId</span><span class="sxs-lookup"><span data-stu-id="0c3df-118">-ArtifactSourceId</span></span>
<span data-ttu-id="0c3df-119">Der Bezeichner der Artefakt-Quelle, in der die Artefakte, aus denen sich die Topologie befindet, gespeichert werden.</span><span class="sxs-lookup"><span data-stu-id="0c3df-119">The identifier of the artifact source, where the artifacts that make up the topology are stored.</span></span>

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

### <span data-ttu-id="0c3df-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0c3df-120">-DefaultProfile</span></span>
<span data-ttu-id="0c3df-121">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="0c3df-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0c3df-122">-Standort</span><span class="sxs-lookup"><span data-stu-id="0c3df-122">-Location</span></span>
<span data-ttu-id="0c3df-123">Der Speicherort der Topologie.</span><span class="sxs-lookup"><span data-stu-id="0c3df-123">The location of the topology.</span></span>

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

### <span data-ttu-id="0c3df-124">-Name</span><span class="sxs-lookup"><span data-stu-id="0c3df-124">-Name</span></span>
<span data-ttu-id="0c3df-125">Der Name der Topologie.</span><span class="sxs-lookup"><span data-stu-id="0c3df-125">The name of the topology.</span></span>

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

### <span data-ttu-id="0c3df-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0c3df-126">-ResourceGroupName</span></span>
<span data-ttu-id="0c3df-127">Die Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="0c3df-127">The resource group.</span></span>

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

### <span data-ttu-id="0c3df-128">-Tag</span><span class="sxs-lookup"><span data-stu-id="0c3df-128">-Tag</span></span>
<span data-ttu-id="0c3df-129">Eine Hashtabelle, die Ressourcenkategorien darstellt.</span><span class="sxs-lookup"><span data-stu-id="0c3df-129">A hash table which represents resource tags.</span></span>

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

### <span data-ttu-id="0c3df-130">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="0c3df-130">-Confirm</span></span>
<span data-ttu-id="0c3df-131">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="0c3df-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0c3df-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0c3df-132">-WhatIf</span></span>
<span data-ttu-id="0c3df-133">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="0c3df-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0c3df-134">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="0c3df-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0c3df-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0c3df-135">CommonParameters</span></span>
<span data-ttu-id="0c3df-136">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0c3df-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0c3df-137">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0c3df-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0c3df-138">Eingaben</span><span class="sxs-lookup"><span data-stu-id="0c3df-138">INPUTS</span></span>

### <span data-ttu-id="0c3df-139">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="0c3df-139">System.Collections.Hashtable</span></span>

## <span data-ttu-id="0c3df-140">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="0c3df-140">OUTPUTS</span></span>

### <span data-ttu-id="0c3df-141">Microsoft. Azure. Commands. deploymentmanager. Models. PSServiceTopologyResource</span><span class="sxs-lookup"><span data-stu-id="0c3df-141">Microsoft.Azure.Commands.DeploymentManager.Models.PSServiceTopologyResource</span></span>

## <span data-ttu-id="0c3df-142">Notizen</span><span class="sxs-lookup"><span data-stu-id="0c3df-142">NOTES</span></span>

## <span data-ttu-id="0c3df-143">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="0c3df-143">RELATED LINKS</span></span>
