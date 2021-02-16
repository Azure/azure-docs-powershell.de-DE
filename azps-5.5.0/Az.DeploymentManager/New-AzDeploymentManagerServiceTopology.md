---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DeploymentManager.dll-Help.xml
Module Name: Az.DeploymentManager
online version: https://docs.microsoft.com/en-us/powershell/module/az.deploymentmanager/new-azdeploymentmanagerservicetopology
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeploymentManager/DeploymentManager/help/New-AzDeploymentManagerServiceTopology.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeploymentManager/DeploymentManager/help/New-AzDeploymentManagerServiceTopology.md
ms.openlocfilehash: c104f074b972e42aaa21ce4e85c6076294ec5aa2
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100163745"
---
# <span data-ttu-id="01392-101">New-AzDeploymentManagerServiceTopology</span><span class="sxs-lookup"><span data-stu-id="01392-101">New-AzDeploymentManagerServiceTopology</span></span>

## <span data-ttu-id="01392-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="01392-102">SYNOPSIS</span></span>
<span data-ttu-id="01392-103">Erstellt eine Diensttopologie.</span><span class="sxs-lookup"><span data-stu-id="01392-103">Creates a service topology.</span></span>

## <span data-ttu-id="01392-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="01392-104">SYNTAX</span></span>

```
New-AzDeploymentManagerServiceTopology -ResourceGroupName <String> -Name <String> -Location <String>
 [-ArtifactSourceId <String>] [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="01392-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="01392-105">DESCRIPTION</span></span>
<span data-ttu-id="01392-106">Das **Cmdlet "New-AzDeploymentManagerServiceTopology"** erstellt eine Diensttopologie.</span><span class="sxs-lookup"><span data-stu-id="01392-106">The **New-AzDeploymentManagerServiceTopology** cmdlet creates a service topology.</span></span>

<span data-ttu-id="01392-107">Sie können das zurückgegebene "ServiceTopology"-Objekt lokal ändern und dann Änderungen an der Topologie mithilfe des Set-AzDeploymentManagerServiceTopology anwenden.</span><span class="sxs-lookup"><span data-stu-id="01392-107">You can modify the returned ServiceTopology object locally, and then apply changes to the topology by using the Set-AzDeploymentManagerServiceTopology cmdlet.</span></span>
<span data-ttu-id="01392-108">Das zurückgegebene Objekt</span><span class="sxs-lookup"><span data-stu-id="01392-108">The returned object</span></span> 

<span data-ttu-id="01392-109">Das zurückgegebene Objekt hat ein Feld "ResourceId", auf das in einer Rolloutressource verwiesen werden kann, um anzugeben, dass die in dieser Diensttopologie deklarierten Dienste beim Rollout bereitgestellt werden.</span><span class="sxs-lookup"><span data-stu-id="01392-109">The returned object has a ResourceId field which can be referenced in a rollout resource to indicate that the services declared in this service topology would be deployed in the rollout.</span></span>

## <span data-ttu-id="01392-110">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="01392-110">EXAMPLES</span></span>

### <span data-ttu-id="01392-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="01392-111">Example 1</span></span>
```powershell
PS C:\> New-AzDeploymentManagerServiceTopology -ResourceGroupName ContosoResourceGroup -Name ContosoServiceTopology -Location "Central US" -ArtifactSourceId "/subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourcegroups/ContosoResourceGroup/providers/Microsoft.DeploymentManager/artifactSources/ContosoArtifactSource"
```

<span data-ttu-id="01392-112">Dieses Cmdlet erstellt eine neue Diensttopologie in der Ressourcengruppe "ContosoResourceGroup" mit dem Namen "ContosoServiceTopology" und dem Speicherort "USA, Mitte".</span><span class="sxs-lookup"><span data-stu-id="01392-112">This cmdlet creates a new service topology in the resource group ContosoResourceGroup with the name ContosoServiceTopology and in location Central US.</span></span> <span data-ttu-id="01392-113">Die Artefaktquelle "ResourceId" gibt an, dass die Artefakte, die für die Definitionen der Diensteinheiten in dieser Topologie erforderlich sind, aus der angegebenen Artefaktquelle gelesen werden müssen.</span><span class="sxs-lookup"><span data-stu-id="01392-113">The artifact source ResourceId indicates that the artifacts required for the service unit definitions in this topology need to be read from the specified artifact source.</span></span>

### <span data-ttu-id="01392-114">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="01392-114">Example 2</span></span>
```powershell
PS C:\> New-AzDeploymentManagerServiceTopology -ResourceGroupName ContosoResourceGroup -Name ContosoServiceTopology -Location "Central US"
```

<span data-ttu-id="01392-115">Dieses Cmdlet erstellt eine neue Diensttopologie in der Ressourcengruppe "ContosoResourceGroup" mit dem Namen "ContosoServiceTopology" und dem Speicherort "USA, Mitte".</span><span class="sxs-lookup"><span data-stu-id="01392-115">This cmdlet creates a new service topology in the resource group ContosoResourceGroup with the name ContosoServiceTopology and in location Central US.</span></span> <span data-ttu-id="01392-116">Das Fehlen eines Artefaktquellenverweises deutet darauf hin, dass die für die Diensteinheitsdefinitionen in dieser Topologie erforderlichen Artefakte als absolute SAS-URIs in der Diensteinheit bereitgestellt werden.</span><span class="sxs-lookup"><span data-stu-id="01392-116">The absence of an artifact source reference indicates that the artifacts required for the service unit definitions in this topology would be provided as absolute SAS URIs in the service unit.</span></span>

## <span data-ttu-id="01392-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="01392-117">PARAMETERS</span></span>

### <span data-ttu-id="01392-118">-ArtifactSourceId</span><span class="sxs-lookup"><span data-stu-id="01392-118">-ArtifactSourceId</span></span>
<span data-ttu-id="01392-119">Der Bezeichner der Artefaktquelle, in der die Artefakte gespeichert werden, aus denen die Topologie stammt.</span><span class="sxs-lookup"><span data-stu-id="01392-119">The identifier of the artifact source, where the artifacts that make up the topology are stored.</span></span>

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

### <span data-ttu-id="01392-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="01392-120">-DefaultProfile</span></span>
<span data-ttu-id="01392-121">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="01392-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="01392-122">-Location</span><span class="sxs-lookup"><span data-stu-id="01392-122">-Location</span></span>
<span data-ttu-id="01392-123">Die Position der Topologie.</span><span class="sxs-lookup"><span data-stu-id="01392-123">The location of the topology.</span></span>

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

### <span data-ttu-id="01392-124">-Name</span><span class="sxs-lookup"><span data-stu-id="01392-124">-Name</span></span>
<span data-ttu-id="01392-125">Der Name der Topologie.</span><span class="sxs-lookup"><span data-stu-id="01392-125">The name of the topology.</span></span>

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

### <span data-ttu-id="01392-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="01392-126">-ResourceGroupName</span></span>
<span data-ttu-id="01392-127">Die Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="01392-127">The resource group.</span></span>

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

### <span data-ttu-id="01392-128">-Tag</span><span class="sxs-lookup"><span data-stu-id="01392-128">-Tag</span></span>
<span data-ttu-id="01392-129">Eine Hashtabelle, die Ressourcentags darstellt.</span><span class="sxs-lookup"><span data-stu-id="01392-129">A hash table which represents resource tags.</span></span>

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

### <span data-ttu-id="01392-130">-Confirm</span><span class="sxs-lookup"><span data-stu-id="01392-130">-Confirm</span></span>
<span data-ttu-id="01392-131">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="01392-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="01392-132">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="01392-132">-WhatIf</span></span>
<span data-ttu-id="01392-133">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="01392-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="01392-134">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="01392-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="01392-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="01392-135">CommonParameters</span></span>
<span data-ttu-id="01392-136">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="01392-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="01392-137">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="01392-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="01392-138">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="01392-138">INPUTS</span></span>

### <span data-ttu-id="01392-139">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="01392-139">System.Collections.Hashtable</span></span>

## <span data-ttu-id="01392-140">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="01392-140">OUTPUTS</span></span>

### <span data-ttu-id="01392-141">Microsoft.Azure.Commands.DeploymentManager.Models.PSServiceTopologyResource</span><span class="sxs-lookup"><span data-stu-id="01392-141">Microsoft.Azure.Commands.DeploymentManager.Models.PSServiceTopologyResource</span></span>

## <span data-ttu-id="01392-142">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="01392-142">NOTES</span></span>

## <span data-ttu-id="01392-143">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="01392-143">RELATED LINKS</span></span>
