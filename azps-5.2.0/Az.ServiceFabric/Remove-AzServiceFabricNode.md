---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceFabric.dll-Help.xml
Module Name: Az.ServiceFabric
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicefabric/remove-azservicefabricnode
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Remove-AzServiceFabricNode.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Remove-AzServiceFabricNode.md
ms.openlocfilehash: fd38b68c8133cbc498bbc50ffea84b48e58198a9
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98357900"
---
# <span data-ttu-id="4c051-101">Remove-AzServiceFabricNode</span><span class="sxs-lookup"><span data-stu-id="4c051-101">Remove-AzServiceFabricNode</span></span>

## <span data-ttu-id="4c051-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4c051-102">SYNOPSIS</span></span>
<span data-ttu-id="4c051-103">Entfernen Sie Knoten aus dem jeweiligen Knotentyp aus einem Cluster.</span><span class="sxs-lookup"><span data-stu-id="4c051-103">Remove nodes from the specific node type from a cluster.</span></span>

## <span data-ttu-id="4c051-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="4c051-104">SYNTAX</span></span>

```
Remove-AzServiceFabricNode -NumberOfNodesToRemove <Int32> [-ResourceGroupName] <String> [-Name] <String>
 -NodeType <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4c051-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="4c051-105">DESCRIPTION</span></span>
<span data-ttu-id="4c051-106">Verwenden **Sie Remove-AzServiceFabricNode,** um Knoten aus einem bestimmten Knotentyp aus einem Cluster zu entfernen.</span><span class="sxs-lookup"><span data-stu-id="4c051-106">Use **Remove-AzServiceFabricNode** to remove nodes from a specific node type from a cluster.</span></span> <span data-ttu-id="4c051-107">Das Entfernen wird nur fortgesetzt, wenn es die Metriken für den Clusterzustand erfüllt.</span><span class="sxs-lookup"><span data-stu-id="4c051-107">The removal proceeds only if it meets cluster health metrics.</span></span>

## <span data-ttu-id="4c051-108">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="4c051-108">EXAMPLES</span></span>

### <span data-ttu-id="4c051-109">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="4c051-109">Example 1</span></span>
```powershell
PS c:> Remove-AzServiceFabricNode -ResourceGroupName 'Group1' -Name 'Contoso01SFCluster' -NodeType 'nt1' -NumberOfNodesToRemove 2
```

<span data-ttu-id="4c051-110">Mit diesem Befehl werden zwei Knoten aus dem NodeType 'nt1' entfernt.</span><span class="sxs-lookup"><span data-stu-id="4c051-110">This command will remove 2 nodes from the NodeType 'nt1'.</span></span>

## <span data-ttu-id="4c051-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="4c051-111">PARAMETERS</span></span>

### <span data-ttu-id="4c051-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4c051-112">-DefaultProfile</span></span>
<span data-ttu-id="4c051-113">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="4c051-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4c051-114">-Name</span><span class="sxs-lookup"><span data-stu-id="4c051-114">-Name</span></span>
<span data-ttu-id="4c051-115">Angeben des Namens des Clusters</span><span class="sxs-lookup"><span data-stu-id="4c051-115">Specify the name of the cluster</span></span>

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

### <span data-ttu-id="4c051-116">-NodeType</span><span class="sxs-lookup"><span data-stu-id="4c051-116">-NodeType</span></span>
<span data-ttu-id="4c051-117">Name des Knotentyps</span><span class="sxs-lookup"><span data-stu-id="4c051-117">Node type name</span></span>

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

### <span data-ttu-id="4c051-118">-NumberOfNodesToRemove</span><span class="sxs-lookup"><span data-stu-id="4c051-118">-NumberOfNodesToRemove</span></span>
<span data-ttu-id="4c051-119">Die Anzahl der hinzuzufügende Knoten</span><span class="sxs-lookup"><span data-stu-id="4c051-119">The number of nodes to add</span></span>

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

### <span data-ttu-id="4c051-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4c051-120">-ResourceGroupName</span></span>
<span data-ttu-id="4c051-121">Geben Sie den Namen der Ressourcengruppe an.</span><span class="sxs-lookup"><span data-stu-id="4c051-121">Specify the name of the resource group.</span></span>

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

### <span data-ttu-id="4c051-122">-Confirm</span><span class="sxs-lookup"><span data-stu-id="4c051-122">-Confirm</span></span>
<span data-ttu-id="4c051-123">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="4c051-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4c051-124">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="4c051-124">-WhatIf</span></span>
<span data-ttu-id="4c051-125">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="4c051-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4c051-126">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="4c051-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4c051-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4c051-127">CommonParameters</span></span>
<span data-ttu-id="4c051-128">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4c051-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4c051-129">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="4c051-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4c051-130">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="4c051-130">INPUTS</span></span>

### <span data-ttu-id="4c051-131">System.Int32</span><span class="sxs-lookup"><span data-stu-id="4c051-131">System.Int32</span></span>

### <span data-ttu-id="4c051-132">System.String</span><span class="sxs-lookup"><span data-stu-id="4c051-132">System.String</span></span>

## <span data-ttu-id="4c051-133">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="4c051-133">OUTPUTS</span></span>

### <span data-ttu-id="4c051-134">Microsoft.Azure.Commands.ServiceFabric.Models.PSCluster</span><span class="sxs-lookup"><span data-stu-id="4c051-134">Microsoft.Azure.Commands.ServiceFabric.Models.PSCluster</span></span>

## <span data-ttu-id="4c051-135">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="4c051-135">NOTES</span></span>

## <span data-ttu-id="4c051-136">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="4c051-136">RELATED LINKS</span></span>

[<span data-ttu-id="4c051-137">Add-AzServiceFabricNode</span><span class="sxs-lookup"><span data-stu-id="4c051-137">Add-AzServiceFabricNode</span></span>](./Add-AzServiceFabricNode.md)
