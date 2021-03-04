---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceFabric.dll-Help.xml
Module Name: Az.ServiceFabric
online version: https://docs.microsoft.com/powershell/module/az.servicefabric/add-azservicefabricnode
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Add-AzServiceFabricNode.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Add-AzServiceFabricNode.md
ms.openlocfilehash: 34b55a5da226a3985cb6fe3bede244ee1e054726
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101934648"
---
# <span data-ttu-id="cdd71-101">Add-AzServiceFabricNode</span><span class="sxs-lookup"><span data-stu-id="cdd71-101">Add-AzServiceFabricNode</span></span>

## <span data-ttu-id="cdd71-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="cdd71-102">SYNOPSIS</span></span>
<span data-ttu-id="cdd71-103">Fügen Sie dem bestimmten Knotentyp im Cluster Knoten hinzu.</span><span class="sxs-lookup"><span data-stu-id="cdd71-103">Add nodes to the specific node type in the cluster.</span></span>

## <span data-ttu-id="cdd71-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="cdd71-104">SYNTAX</span></span>

```
Add-AzServiceFabricNode -NumberOfNodesToAdd <Int32> [-ResourceGroupName] <String> [-Name] <String>
 -NodeType <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="cdd71-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="cdd71-105">DESCRIPTION</span></span>
<span data-ttu-id="cdd71-106">Verwenden **Sie Add-AzServiceFabricNode,** um dem jeweiligen Knotentyp Knoten hinzuzufügen.</span><span class="sxs-lookup"><span data-stu-id="cdd71-106">Use **Add-AzServiceFabricNode** to add nodes to the specific node type.</span></span> <span data-ttu-id="cdd71-107">Sie müssen nur die Anzahl der Knoten angeben, die Sie einem Knotentyp hinzufügen möchten.</span><span class="sxs-lookup"><span data-stu-id="cdd71-107">You just need to specify the number of nodes you want to add to a node type.</span></span>

## <span data-ttu-id="cdd71-108">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="cdd71-108">EXAMPLES</span></span>

### <span data-ttu-id="cdd71-109">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="cdd71-109">Example 1</span></span>
```powershell
PS c:> Add-AzServiceFabricNode -ResourceGroupName 'Group1' -Name 'Contoso01SFCluster' -NumberOfNodesToAdd 2 -NodeTypeName 'nt1'
```

<span data-ttu-id="cdd71-110">Mit diesem Befehl werden dem Knotentyp "n1" zwei Knoten hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="cdd71-110">This command will add 2 nodes to the node type 'n1'.</span></span>

## <span data-ttu-id="cdd71-111">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="cdd71-111">PARAMETERS</span></span>

### <span data-ttu-id="cdd71-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cdd71-112">-DefaultProfile</span></span>
<span data-ttu-id="cdd71-113">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="cdd71-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="cdd71-114">-Name</span><span class="sxs-lookup"><span data-stu-id="cdd71-114">-Name</span></span>
<span data-ttu-id="cdd71-115">Angeben des Namens des Clusters</span><span class="sxs-lookup"><span data-stu-id="cdd71-115">Specify the name of the cluster</span></span>

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

### <span data-ttu-id="cdd71-116">-NodeType</span><span class="sxs-lookup"><span data-stu-id="cdd71-116">-NodeType</span></span>
<span data-ttu-id="cdd71-117">Name des Knotentyps</span><span class="sxs-lookup"><span data-stu-id="cdd71-117">Node type name</span></span>

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

### <span data-ttu-id="cdd71-118">-NumberOfNodesToAdd</span><span class="sxs-lookup"><span data-stu-id="cdd71-118">-NumberOfNodesToAdd</span></span>
<span data-ttu-id="cdd71-119">Die Anzahl der hinzuzufügende Knoten</span><span class="sxs-lookup"><span data-stu-id="cdd71-119">The number of nodes to add</span></span>

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

### <span data-ttu-id="cdd71-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cdd71-120">-ResourceGroupName</span></span>
<span data-ttu-id="cdd71-121">Geben Sie den Namen der Ressourcengruppe an.</span><span class="sxs-lookup"><span data-stu-id="cdd71-121">Specify the name of the resource group.</span></span>

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

### <span data-ttu-id="cdd71-122">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="cdd71-122">-Confirm</span></span>
<span data-ttu-id="cdd71-123">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="cdd71-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="cdd71-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="cdd71-124">-WhatIf</span></span>
<span data-ttu-id="cdd71-125">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="cdd71-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="cdd71-126">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="cdd71-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="cdd71-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cdd71-127">CommonParameters</span></span>
<span data-ttu-id="cdd71-128">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cdd71-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cdd71-129">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="cdd71-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cdd71-130">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="cdd71-130">INPUTS</span></span>

### <span data-ttu-id="cdd71-131">System.Int32</span><span class="sxs-lookup"><span data-stu-id="cdd71-131">System.Int32</span></span>

### <span data-ttu-id="cdd71-132">System.String</span><span class="sxs-lookup"><span data-stu-id="cdd71-132">System.String</span></span>

## <span data-ttu-id="cdd71-133">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="cdd71-133">OUTPUTS</span></span>

### <span data-ttu-id="cdd71-134">Microsoft.Azure.Commands.ServiceFabric.Models.PSCluster</span><span class="sxs-lookup"><span data-stu-id="cdd71-134">Microsoft.Azure.Commands.ServiceFabric.Models.PSCluster</span></span>

## <span data-ttu-id="cdd71-135">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="cdd71-135">NOTES</span></span>

## <span data-ttu-id="cdd71-136">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="cdd71-136">RELATED LINKS</span></span>

[<span data-ttu-id="cdd71-137">Remove-AzServiceFabricNode</span><span class="sxs-lookup"><span data-stu-id="cdd71-137">Remove-AzServiceFabricNode</span></span>](./Remove-AzServiceFabricNode.md)
