---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventHub.dll-Help.xml
Module Name: Az.EventHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.eventhub/remove-azeventhubcluster
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Remove-AzEventHubCluster.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Remove-AzEventHubCluster.md
ms.openlocfilehash: e67d70f91e523cd46755035abe951682b1764cbc
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94175664"
---
# <span data-ttu-id="7db10-101">Remove-AzEventHubCluster</span><span class="sxs-lookup"><span data-stu-id="7db10-101">Remove-AzEventHubCluster</span></span>

## <span data-ttu-id="7db10-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="7db10-102">SYNOPSIS</span></span>
<span data-ttu-id="7db10-103">Löscht den angegebenen dedizierten Eventhub-Cluster aus der ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="7db10-103">Deletes the specified Dedicated Eventhub Cluster from the ResourceGroup</span></span>

## <span data-ttu-id="7db10-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="7db10-104">SYNTAX</span></span>

### <span data-ttu-id="7db10-105">ClusterPropertiesSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="7db10-105">ClusterPropertiesSet (Default)</span></span>
```
Remove-AzEventHubCluster [-ResourceGroupName] <String> [-Name] <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7db10-106">ClusterInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="7db10-106">ClusterInputObjectSet</span></span>
```
Remove-AzEventHubCluster [-InputObject] <PSEventHubAttributes> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7db10-107">ClusterResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="7db10-107">ClusterResourceIdParameterSet</span></span>
```
Remove-AzEventHubCluster [-ResourceId] <String> [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7db10-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="7db10-108">DESCRIPTION</span></span>
<span data-ttu-id="7db10-109">Das Cmdlet "Remove-AzEventHubCluster" löscht den angegebenen dedizierten eventhub-Cluster Namen aus der angegebenen ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="7db10-109">The Remove-AzEventHubCluster cmdlet deletes the given dedicated eventhub Cluster name from the given resourcegroup</span></span>

## <span data-ttu-id="7db10-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="7db10-110">EXAMPLES</span></span>

### <span data-ttu-id="7db10-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="7db10-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzEventHubCluster -ResourceGroupName RSG-Cluster27651 -Name Eventhub-Cluster-5557
```

<span data-ttu-id="7db10-112">Löschen des Eventhub-Cluster-5557-Clusters aus RSG-Cluster27651 ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="7db10-112">Deletes Eventhub-Cluster-5557 Cluster from RSG-Cluster27651 resourcegroup</span></span>

## <span data-ttu-id="7db10-113">Parameter</span><span class="sxs-lookup"><span data-stu-id="7db10-113">PARAMETERS</span></span>

### <span data-ttu-id="7db10-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="7db10-114">-AsJob</span></span>
<span data-ttu-id="7db10-115">Ausführen eines Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="7db10-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="7db10-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7db10-116">-DefaultProfile</span></span>
<span data-ttu-id="7db10-117">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="7db10-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7db10-118">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="7db10-118">-InputObject</span></span>
<span data-ttu-id="7db10-119">Cluster Objekt</span><span class="sxs-lookup"><span data-stu-id="7db10-119">Cluster Object</span></span>

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

### <span data-ttu-id="7db10-120">-Name</span><span class="sxs-lookup"><span data-stu-id="7db10-120">-Name</span></span>
<span data-ttu-id="7db10-121">Cluster Name</span><span class="sxs-lookup"><span data-stu-id="7db10-121">Cluster Name</span></span>

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

### <span data-ttu-id="7db10-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="7db10-122">-PassThru</span></span>
<span data-ttu-id="7db10-123">{{Fill passthru Description}}</span><span class="sxs-lookup"><span data-stu-id="7db10-123">{{ Fill PassThru Description }}</span></span>

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

### <span data-ttu-id="7db10-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7db10-124">-ResourceGroupName</span></span>
<span data-ttu-id="7db10-125">Ressourcengruppen Name</span><span class="sxs-lookup"><span data-stu-id="7db10-125">Resource Group Name</span></span>

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

### <span data-ttu-id="7db10-126">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="7db10-126">-ResourceId</span></span>
<span data-ttu-id="7db10-127">Cluster-Ressourcen-ID</span><span class="sxs-lookup"><span data-stu-id="7db10-127">Cluster Resource Id</span></span>

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

### <span data-ttu-id="7db10-128">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="7db10-128">-Confirm</span></span>
<span data-ttu-id="7db10-129">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="7db10-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7db10-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7db10-130">-WhatIf</span></span>
<span data-ttu-id="7db10-131">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="7db10-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7db10-132">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="7db10-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7db10-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7db10-133">CommonParameters</span></span>
<span data-ttu-id="7db10-134">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7db10-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7db10-135">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="7db10-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7db10-136">Eingaben</span><span class="sxs-lookup"><span data-stu-id="7db10-136">INPUTS</span></span>

### <span data-ttu-id="7db10-137">System. String</span><span class="sxs-lookup"><span data-stu-id="7db10-137">System.String</span></span>

### <span data-ttu-id="7db10-138">Microsoft. Azure. Commands. EventHub. Models. PSEventHubAttributes</span><span class="sxs-lookup"><span data-stu-id="7db10-138">Microsoft.Azure.Commands.EventHub.Models.PSEventHubAttributes</span></span>

## <span data-ttu-id="7db10-139">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="7db10-139">OUTPUTS</span></span>

### <span data-ttu-id="7db10-140">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="7db10-140">System.Boolean</span></span>

## <span data-ttu-id="7db10-141">Notizen</span><span class="sxs-lookup"><span data-stu-id="7db10-141">NOTES</span></span>

## <span data-ttu-id="7db10-142">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="7db10-142">RELATED LINKS</span></span>
