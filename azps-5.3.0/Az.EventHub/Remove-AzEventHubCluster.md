---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventHub.dll-Help.xml
Module Name: Az.EventHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.eventhub/remove-azeventhubcluster
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Remove-AzEventHubCluster.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Remove-AzEventHubCluster.md
ms.openlocfilehash: e67d70f91e523cd46755035abe951682b1764cbc
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98386936"
---
# <span data-ttu-id="b85fc-101">Remove-AzEventHubCluster</span><span class="sxs-lookup"><span data-stu-id="b85fc-101">Remove-AzEventHubCluster</span></span>

## <span data-ttu-id="b85fc-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b85fc-102">SYNOPSIS</span></span>
<span data-ttu-id="b85fc-103">Löscht den angegebenen dedizierten Eventhub-Cluster aus der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="b85fc-103">Deletes the specified Dedicated Eventhub Cluster from the ResourceGroup</span></span>

## <span data-ttu-id="b85fc-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="b85fc-104">SYNTAX</span></span>

### <span data-ttu-id="b85fc-105">ClusterPropertiesSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="b85fc-105">ClusterPropertiesSet (Default)</span></span>
```
Remove-AzEventHubCluster [-ResourceGroupName] <String> [-Name] <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b85fc-106">ClusterInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="b85fc-106">ClusterInputObjectSet</span></span>
```
Remove-AzEventHubCluster [-InputObject] <PSEventHubAttributes> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b85fc-107">ClusterResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="b85fc-107">ClusterResourceIdParameterSet</span></span>
```
Remove-AzEventHubCluster [-ResourceId] <String> [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b85fc-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="b85fc-108">DESCRIPTION</span></span>
<span data-ttu-id="b85fc-109">Das Remove-AzEventHubCluster cmdlet löscht den angegebenen dedizierten Ereignishubclusternamen aus der angegebenen Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="b85fc-109">The Remove-AzEventHubCluster cmdlet deletes the given dedicated eventhub Cluster name from the given resourcegroup</span></span>

## <span data-ttu-id="b85fc-110">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="b85fc-110">EXAMPLES</span></span>

### <span data-ttu-id="b85fc-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="b85fc-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzEventHubCluster -ResourceGroupName RSG-Cluster27651 -Name Eventhub-Cluster-5557
```

<span data-ttu-id="b85fc-112">Löscht Eventhub-Cluster-5557 Cluster aus RSG-Cluster27651 Ressourcengruppe</span><span class="sxs-lookup"><span data-stu-id="b85fc-112">Deletes Eventhub-Cluster-5557 Cluster from RSG-Cluster27651 resourcegroup</span></span>

## <span data-ttu-id="b85fc-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="b85fc-113">PARAMETERS</span></span>

### <span data-ttu-id="b85fc-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="b85fc-114">-AsJob</span></span>
<span data-ttu-id="b85fc-115">Ausführen des Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="b85fc-115">Run cmdlet in the background</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b85fc-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b85fc-116">-DefaultProfile</span></span>
<span data-ttu-id="b85fc-117">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="b85fc-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b85fc-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="b85fc-118">-InputObject</span></span>
<span data-ttu-id="b85fc-119">Clusterobjekt</span><span class="sxs-lookup"><span data-stu-id="b85fc-119">Cluster Object</span></span>

```yaml
Type: Microsoft.Azure.Commands.EventHub.Models.PSEventHubAttributes
Parameter Sets: ClusterInputObjectSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b85fc-120">-Name</span><span class="sxs-lookup"><span data-stu-id="b85fc-120">-Name</span></span>
<span data-ttu-id="b85fc-121">Clustername</span><span class="sxs-lookup"><span data-stu-id="b85fc-121">Cluster Name</span></span>

```yaml
Type: System.String
Parameter Sets: ClusterPropertiesSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b85fc-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="b85fc-122">-PassThru</span></span>
<span data-ttu-id="b85fc-123">{{ Fill PassThru Description }}</span><span class="sxs-lookup"><span data-stu-id="b85fc-123">{{ Fill PassThru Description }}</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b85fc-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b85fc-124">-ResourceGroupName</span></span>
<span data-ttu-id="b85fc-125">Ressourcengruppenname</span><span class="sxs-lookup"><span data-stu-id="b85fc-125">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: ClusterPropertiesSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b85fc-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="b85fc-126">-ResourceId</span></span>
<span data-ttu-id="b85fc-127">Clusterressourcen-ID</span><span class="sxs-lookup"><span data-stu-id="b85fc-127">Cluster Resource Id</span></span>

```yaml
Type: System.String
Parameter Sets: ClusterResourceIdParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b85fc-128">-Confirm</span><span class="sxs-lookup"><span data-stu-id="b85fc-128">-Confirm</span></span>
<span data-ttu-id="b85fc-129">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="b85fc-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b85fc-130">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="b85fc-130">-WhatIf</span></span>
<span data-ttu-id="b85fc-131">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="b85fc-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b85fc-132">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="b85fc-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b85fc-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b85fc-133">CommonParameters</span></span>
<span data-ttu-id="b85fc-134">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b85fc-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b85fc-135">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="b85fc-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b85fc-136">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="b85fc-136">INPUTS</span></span>

### <span data-ttu-id="b85fc-137">System.String</span><span class="sxs-lookup"><span data-stu-id="b85fc-137">System.String</span></span>

### <span data-ttu-id="b85fc-138">Microsoft.Azure.Commands.EventHub.Models.PSEventHubAttributes</span><span class="sxs-lookup"><span data-stu-id="b85fc-138">Microsoft.Azure.Commands.EventHub.Models.PSEventHubAttributes</span></span>

## <span data-ttu-id="b85fc-139">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="b85fc-139">OUTPUTS</span></span>

### <span data-ttu-id="b85fc-140">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="b85fc-140">System.Boolean</span></span>

## <span data-ttu-id="b85fc-141">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="b85fc-141">NOTES</span></span>

## <span data-ttu-id="b85fc-142">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="b85fc-142">RELATED LINKS</span></span>
