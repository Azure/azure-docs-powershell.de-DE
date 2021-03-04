---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventHub.dll-Help.xml
Module Name: Az.EventHub
online version: https://docs.microsoft.com/powershell/module/az.eventhub/remove-azeventhubcluster
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Remove-AzEventHubCluster.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Remove-AzEventHubCluster.md
ms.openlocfilehash: 7ba6a5f95c1cc37f7cdef7d8ead7a2514927e089
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101939576"
---
# <span data-ttu-id="78e2a-101">Remove-AzEventHubCluster</span><span class="sxs-lookup"><span data-stu-id="78e2a-101">Remove-AzEventHubCluster</span></span>

## <span data-ttu-id="78e2a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="78e2a-102">SYNOPSIS</span></span>
<span data-ttu-id="78e2a-103">Löscht den angegebenen dedizierten Ereignishubcluster aus der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="78e2a-103">Deletes the specified Dedicated Eventhub Cluster from the ResourceGroup</span></span>

## <span data-ttu-id="78e2a-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="78e2a-104">SYNTAX</span></span>

### <span data-ttu-id="78e2a-105">ClusterPropertiesSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="78e2a-105">ClusterPropertiesSet (Default)</span></span>
```
Remove-AzEventHubCluster [-ResourceGroupName] <String> [-Name] <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="78e2a-106">ClusterInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="78e2a-106">ClusterInputObjectSet</span></span>
```
Remove-AzEventHubCluster [-InputObject] <PSEventHubAttributes> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="78e2a-107">ClusterResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="78e2a-107">ClusterResourceIdParameterSet</span></span>
```
Remove-AzEventHubCluster [-ResourceId] <String> [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="78e2a-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="78e2a-108">DESCRIPTION</span></span>
<span data-ttu-id="78e2a-109">Das Remove-AzEventHubCluster-Cmdlet löscht den angegebenen dedizierten Ereignishub-Clusternamen aus der angegebenen Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="78e2a-109">The Remove-AzEventHubCluster cmdlet deletes the given dedicated eventhub Cluster name from the given resourcegroup</span></span>

## <span data-ttu-id="78e2a-110">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="78e2a-110">EXAMPLES</span></span>

### <span data-ttu-id="78e2a-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="78e2a-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzEventHubCluster -ResourceGroupName RSG-Cluster27651 -Name Eventhub-Cluster-5557
```

<span data-ttu-id="78e2a-112">Löscht Eventhub-Cluster-5557-Cluster aus RSG-Cluster27651 Ressourcengruppe</span><span class="sxs-lookup"><span data-stu-id="78e2a-112">Deletes Eventhub-Cluster-5557 Cluster from RSG-Cluster27651 resourcegroup</span></span>

## <span data-ttu-id="78e2a-113">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="78e2a-113">PARAMETERS</span></span>

### <span data-ttu-id="78e2a-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="78e2a-114">-AsJob</span></span>
<span data-ttu-id="78e2a-115">Ausführen des Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="78e2a-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="78e2a-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="78e2a-116">-DefaultProfile</span></span>
<span data-ttu-id="78e2a-117">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="78e2a-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="78e2a-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="78e2a-118">-InputObject</span></span>
<span data-ttu-id="78e2a-119">Clusterobjekt</span><span class="sxs-lookup"><span data-stu-id="78e2a-119">Cluster Object</span></span>

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

### <span data-ttu-id="78e2a-120">-Name</span><span class="sxs-lookup"><span data-stu-id="78e2a-120">-Name</span></span>
<span data-ttu-id="78e2a-121">Clustername</span><span class="sxs-lookup"><span data-stu-id="78e2a-121">Cluster Name</span></span>

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

### <span data-ttu-id="78e2a-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="78e2a-122">-PassThru</span></span>
<span data-ttu-id="78e2a-123">{{ Fill PassThru Description }}</span><span class="sxs-lookup"><span data-stu-id="78e2a-123">{{ Fill PassThru Description }}</span></span>

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

### <span data-ttu-id="78e2a-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="78e2a-124">-ResourceGroupName</span></span>
<span data-ttu-id="78e2a-125">Ressourcengruppenname</span><span class="sxs-lookup"><span data-stu-id="78e2a-125">Resource Group Name</span></span>

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

### <span data-ttu-id="78e2a-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="78e2a-126">-ResourceId</span></span>
<span data-ttu-id="78e2a-127">Clusterressourcen-ID</span><span class="sxs-lookup"><span data-stu-id="78e2a-127">Cluster Resource Id</span></span>

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

### <span data-ttu-id="78e2a-128">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="78e2a-128">-Confirm</span></span>
<span data-ttu-id="78e2a-129">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="78e2a-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="78e2a-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="78e2a-130">-WhatIf</span></span>
<span data-ttu-id="78e2a-131">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="78e2a-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="78e2a-132">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="78e2a-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="78e2a-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="78e2a-133">CommonParameters</span></span>
<span data-ttu-id="78e2a-134">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="78e2a-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="78e2a-135">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="78e2a-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="78e2a-136">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="78e2a-136">INPUTS</span></span>

### <span data-ttu-id="78e2a-137">System.String</span><span class="sxs-lookup"><span data-stu-id="78e2a-137">System.String</span></span>

### <span data-ttu-id="78e2a-138">Microsoft.Azure.Commands.EventHub.Models.PSEventHubAttributes</span><span class="sxs-lookup"><span data-stu-id="78e2a-138">Microsoft.Azure.Commands.EventHub.Models.PSEventHubAttributes</span></span>

## <span data-ttu-id="78e2a-139">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="78e2a-139">OUTPUTS</span></span>

### <span data-ttu-id="78e2a-140">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="78e2a-140">System.Boolean</span></span>

## <span data-ttu-id="78e2a-141">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="78e2a-141">NOTES</span></span>

## <span data-ttu-id="78e2a-142">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="78e2a-142">RELATED LINKS</span></span>
