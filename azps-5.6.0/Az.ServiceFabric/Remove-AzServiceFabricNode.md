---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceFabric.dll-Help.xml
Module Name: Az.ServiceFabric
online version: https://docs.microsoft.com/powershell/module/az.servicefabric/remove-azservicefabricnode
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Remove-AzServiceFabricNode.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Remove-AzServiceFabricNode.md
ms.openlocfilehash: ba5400a35939a221b19ba144b35b0f2a53f6dbe9
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101945623"
---
# <span data-ttu-id="2a09b-101">Remove-AzServiceFabricNode</span><span class="sxs-lookup"><span data-stu-id="2a09b-101">Remove-AzServiceFabricNode</span></span>

## <span data-ttu-id="2a09b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2a09b-102">SYNOPSIS</span></span>
<span data-ttu-id="2a09b-103">Entfernen Sie Knoten aus dem jeweiligen Knotentyp aus einem Cluster.</span><span class="sxs-lookup"><span data-stu-id="2a09b-103">Remove nodes from the specific node type from a cluster.</span></span>

## <span data-ttu-id="2a09b-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="2a09b-104">SYNTAX</span></span>

```
Remove-AzServiceFabricNode -NumberOfNodesToRemove <Int32> [-ResourceGroupName] <String> [-Name] <String>
 -NodeType <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2a09b-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="2a09b-105">DESCRIPTION</span></span>
<span data-ttu-id="2a09b-106">Verwenden **Sie Remove-AzServiceFabricNode,** um Knoten aus einem bestimmten Knotentyp aus einem Cluster zu entfernen.</span><span class="sxs-lookup"><span data-stu-id="2a09b-106">Use **Remove-AzServiceFabricNode** to remove nodes from a specific node type from a cluster.</span></span> <span data-ttu-id="2a09b-107">Das Entfernen wird nur fortgesetzt, wenn die Metriken für den Clusterzustand erfüllt sind.</span><span class="sxs-lookup"><span data-stu-id="2a09b-107">The removal proceeds only if it meets cluster health metrics.</span></span>

## <span data-ttu-id="2a09b-108">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="2a09b-108">EXAMPLES</span></span>

### <span data-ttu-id="2a09b-109">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="2a09b-109">Example 1</span></span>
```powershell
PS c:> Remove-AzServiceFabricNode -ResourceGroupName 'Group1' -Name 'Contoso01SFCluster' -NodeType 'nt1' -NumberOfNodesToRemove 2
```

<span data-ttu-id="2a09b-110">Mit diesem Befehl werden zwei Knoten aus dem NodeType "nt1" entfernt.</span><span class="sxs-lookup"><span data-stu-id="2a09b-110">This command will remove 2 nodes from the NodeType 'nt1'.</span></span>

## <span data-ttu-id="2a09b-111">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="2a09b-111">PARAMETERS</span></span>

### <span data-ttu-id="2a09b-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2a09b-112">-DefaultProfile</span></span>
<span data-ttu-id="2a09b-113">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="2a09b-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2a09b-114">-Name</span><span class="sxs-lookup"><span data-stu-id="2a09b-114">-Name</span></span>
<span data-ttu-id="2a09b-115">Angeben des Namens des Clusters</span><span class="sxs-lookup"><span data-stu-id="2a09b-115">Specify the name of the cluster</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ClusterName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2a09b-116">-NodeType</span><span class="sxs-lookup"><span data-stu-id="2a09b-116">-NodeType</span></span>
<span data-ttu-id="2a09b-117">Name des Knotentyps</span><span class="sxs-lookup"><span data-stu-id="2a09b-117">Node type name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="2a09b-118">-NumberOfNodesToRemove</span><span class="sxs-lookup"><span data-stu-id="2a09b-118">-NumberOfNodesToRemove</span></span>
<span data-ttu-id="2a09b-119">Die Anzahl der hinzuzufügende Knoten</span><span class="sxs-lookup"><span data-stu-id="2a09b-119">The number of nodes to add</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases: Number

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="2a09b-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2a09b-120">-ResourceGroupName</span></span>
<span data-ttu-id="2a09b-121">Geben Sie den Namen der Ressourcengruppe an.</span><span class="sxs-lookup"><span data-stu-id="2a09b-121">Specify the name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2a09b-122">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="2a09b-122">-Confirm</span></span>
<span data-ttu-id="2a09b-123">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="2a09b-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2a09b-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2a09b-124">-WhatIf</span></span>
<span data-ttu-id="2a09b-125">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="2a09b-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2a09b-126">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="2a09b-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2a09b-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2a09b-127">CommonParameters</span></span>
<span data-ttu-id="2a09b-128">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2a09b-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2a09b-129">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="2a09b-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2a09b-130">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="2a09b-130">INPUTS</span></span>

### <span data-ttu-id="2a09b-131">System.Int32</span><span class="sxs-lookup"><span data-stu-id="2a09b-131">System.Int32</span></span>

### <span data-ttu-id="2a09b-132">System.String</span><span class="sxs-lookup"><span data-stu-id="2a09b-132">System.String</span></span>

## <span data-ttu-id="2a09b-133">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="2a09b-133">OUTPUTS</span></span>

### <span data-ttu-id="2a09b-134">Microsoft.Azure.Commands.ServiceFabric.Models.PSCluster</span><span class="sxs-lookup"><span data-stu-id="2a09b-134">Microsoft.Azure.Commands.ServiceFabric.Models.PSCluster</span></span>

## <span data-ttu-id="2a09b-135">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="2a09b-135">NOTES</span></span>

## <span data-ttu-id="2a09b-136">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="2a09b-136">RELATED LINKS</span></span>

[<span data-ttu-id="2a09b-137">Add-AzServiceFabricNode</span><span class="sxs-lookup"><span data-stu-id="2a09b-137">Add-AzServiceFabricNode</span></span>](./Add-AzServiceFabricNode.md)
