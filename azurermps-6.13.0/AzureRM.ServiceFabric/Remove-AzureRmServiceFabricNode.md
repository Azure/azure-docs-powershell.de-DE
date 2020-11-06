---
external help file: Microsoft.Azure.Commands.ServiceFabric.dll-Help.xml
Module Name: AzureRM.ServiceFabric
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.servicefabric/remove-azurermservicefabricnode
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceFabric/Commands.ServiceFabric/help/Remove-AzureRmServiceFabricNode.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceFabric/Commands.ServiceFabric/help/Remove-AzureRmServiceFabricNode.md
ms.openlocfilehash: 578210490d92e272e3e4867fb7f96f40a1a39782
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93502901"
---
# <span data-ttu-id="46e67-101">Remove-AzureRmServiceFabricNode</span><span class="sxs-lookup"><span data-stu-id="46e67-101">Remove-AzureRmServiceFabricNode</span></span>

## <span data-ttu-id="46e67-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="46e67-102">SYNOPSIS</span></span>
<span data-ttu-id="46e67-103">Entfernen von Knoten aus dem bestimmten Knotentyp aus einem Cluster</span><span class="sxs-lookup"><span data-stu-id="46e67-103">Remove nodes from the specific node type from a cluster.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="46e67-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="46e67-104">SYNTAX</span></span>

```
Remove-AzureRmServiceFabricNode -NumberOfNodesToRemove <Int32> [-ResourceGroupName] <String> [-Name] <String>
 -NodeType <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="46e67-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="46e67-105">DESCRIPTION</span></span>
<span data-ttu-id="46e67-106">Verwenden **Sie Remove-AzureRmServiceFabricNode** , um Knoten aus einem bestimmten Knotentyp aus einem Cluster zu entfernen.</span><span class="sxs-lookup"><span data-stu-id="46e67-106">Use **Remove-AzureRmServiceFabricNode** to remove nodes from a specific node type from a cluster.</span></span> <span data-ttu-id="46e67-107">Die Entfernung wird nur fortgesetzt, wenn Sie den Kriterien des Cluster Zustands entspricht.</span><span class="sxs-lookup"><span data-stu-id="46e67-107">The removal proceeds only if it meets cluster health metrics.</span></span>

## <span data-ttu-id="46e67-108">Beispiele</span><span class="sxs-lookup"><span data-stu-id="46e67-108">EXAMPLES</span></span>

### <span data-ttu-id="46e67-109">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="46e67-109">Example 1</span></span>
```
PS c:> Remove-AzureRmServiceFabricNode -ResourceGroupName 'Group1' -Name 'Contoso01SFCluster' -NodeTypeName 'nt1' -NumberOfNodesToRemove 2
```

<span data-ttu-id="46e67-110">Mit diesem Befehl werden 2 Knoten vom NodeType "NT1" entfernt.</span><span class="sxs-lookup"><span data-stu-id="46e67-110">This command will remove 2 nodes from the NodeType 'nt1'.</span></span>

## <span data-ttu-id="46e67-111">Parameter</span><span class="sxs-lookup"><span data-stu-id="46e67-111">PARAMETERS</span></span>

### <span data-ttu-id="46e67-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="46e67-112">-DefaultProfile</span></span>
<span data-ttu-id="46e67-113">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="46e67-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="46e67-114">-Name</span><span class="sxs-lookup"><span data-stu-id="46e67-114">-Name</span></span>
<span data-ttu-id="46e67-115">Geben Sie den Namen des Clusters an.</span><span class="sxs-lookup"><span data-stu-id="46e67-115">Specify the name of the cluster.</span></span>

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

### <span data-ttu-id="46e67-116">-NodeType</span><span class="sxs-lookup"><span data-stu-id="46e67-116">-NodeType</span></span>
<span data-ttu-id="46e67-117">Name des Knotentyps</span><span class="sxs-lookup"><span data-stu-id="46e67-117">Node type name.</span></span>

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

### <span data-ttu-id="46e67-118">-NumberOfNodesToRemove</span><span class="sxs-lookup"><span data-stu-id="46e67-118">-NumberOfNodesToRemove</span></span>
<span data-ttu-id="46e67-119">Die Anzahl der zu entfernenden Knoten.</span><span class="sxs-lookup"><span data-stu-id="46e67-119">Number of nodes to remove.</span></span>

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

### <span data-ttu-id="46e67-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="46e67-120">-ResourceGroupName</span></span>
<span data-ttu-id="46e67-121">Gibt den Namen der Ressourcengruppe an.</span><span class="sxs-lookup"><span data-stu-id="46e67-121">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="46e67-122">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="46e67-122">-Confirm</span></span>
<span data-ttu-id="46e67-123">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="46e67-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="46e67-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="46e67-124">-WhatIf</span></span>
<span data-ttu-id="46e67-125">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="46e67-125">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="46e67-126">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="46e67-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="46e67-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="46e67-127">CommonParameters</span></span>
<span data-ttu-id="46e67-128">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="46e67-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="46e67-129">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="46e67-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="46e67-130">Eingaben</span><span class="sxs-lookup"><span data-stu-id="46e67-130">INPUTS</span></span>

### <span data-ttu-id="46e67-131">System. Int32</span><span class="sxs-lookup"><span data-stu-id="46e67-131">System.Int32</span></span>
<span data-ttu-id="46e67-132">Parameter: NumberOfNodesToRemove (ByValue)</span><span class="sxs-lookup"><span data-stu-id="46e67-132">Parameters: NumberOfNodesToRemove (ByValue)</span></span>

### <span data-ttu-id="46e67-133">System. String</span><span class="sxs-lookup"><span data-stu-id="46e67-133">System.String</span></span>
<span data-ttu-id="46e67-134">Parameter: NodeType (ByValue)</span><span class="sxs-lookup"><span data-stu-id="46e67-134">Parameters: NodeType (ByValue)</span></span>

## <span data-ttu-id="46e67-135">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="46e67-135">OUTPUTS</span></span>

### <span data-ttu-id="46e67-136">Microsoft. Azure. Commands. ServiceFabric. Models. PSCluster</span><span class="sxs-lookup"><span data-stu-id="46e67-136">Microsoft.Azure.Commands.ServiceFabric.Models.PSCluster</span></span>

## <span data-ttu-id="46e67-137">Notizen</span><span class="sxs-lookup"><span data-stu-id="46e67-137">NOTES</span></span>

## <span data-ttu-id="46e67-138">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="46e67-138">RELATED LINKS</span></span>

[<span data-ttu-id="46e67-139">Add-AzureRmServiceFabricNode</span><span class="sxs-lookup"><span data-stu-id="46e67-139">Add-AzureRmServiceFabricNode</span></span>](./Add-AzureRmServiceFabricNode.md) 
