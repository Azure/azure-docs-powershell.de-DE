---
external help file: Microsoft.Azure.Commands.ServiceFabric.dll-Help.xml
Module Name: AzureRM.ServiceFabric
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.servicefabric/add-azurermservicefabricnode
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceFabric/Commands.ServiceFabric/help/Add-AzureRmServiceFabricNode.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceFabric/Commands.ServiceFabric/help/Add-AzureRmServiceFabricNode.md
ms.openlocfilehash: 687be1ddd20c431e5226fe7f0516cc480e79fce8
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93662650"
---
# <span data-ttu-id="c8f02-101">Add-AzureRmServiceFabricNode</span><span class="sxs-lookup"><span data-stu-id="c8f02-101">Add-AzureRmServiceFabricNode</span></span>

## <span data-ttu-id="c8f02-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="c8f02-102">SYNOPSIS</span></span>
<span data-ttu-id="c8f02-103">Fügen Sie dem jeweiligen Knotentyp im Clusterknoten hinzu.</span><span class="sxs-lookup"><span data-stu-id="c8f02-103">Add nodes to the specific node type in the cluster.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c8f02-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="c8f02-104">SYNTAX</span></span>

```
Add-AzureRmServiceFabricNode -NumberOfNodesToAdd <Int32> [-ResourceGroupName] <String> [-Name] <String>
 -NodeType <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c8f02-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="c8f02-105">DESCRIPTION</span></span>
<span data-ttu-id="c8f02-106">Verwenden **Sie Add-AzureRmServiceFabricNode** , um dem jeweiligen Knotentyp Knoten hinzuzufügen.</span><span class="sxs-lookup"><span data-stu-id="c8f02-106">Use **Add-AzureRmServiceFabricNode** to add nodes to the specific node type.</span></span> <span data-ttu-id="c8f02-107">Sie müssen lediglich die Anzahl der Knoten angeben, die Sie einem Knotentyp hinzufügen möchten.</span><span class="sxs-lookup"><span data-stu-id="c8f02-107">You just need to specify the number of nodes you want to add to a node type.</span></span>

## <span data-ttu-id="c8f02-108">Beispiele</span><span class="sxs-lookup"><span data-stu-id="c8f02-108">EXAMPLES</span></span>

### <span data-ttu-id="c8f02-109">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="c8f02-109">Example 1</span></span>
```
PS c:> Add-AzureRmServiceFabricNode -ResourceGroupName 'Group1' -Name 'Contoso01SFCluster' -NumberOfNodesToAdd 2 -NodeTypeName 'nt1'
```

<span data-ttu-id="c8f02-110">Mit diesem Befehl werden dem Knotentyp "N1" 2 Knoten hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="c8f02-110">This command will add 2 nodes to the node type 'n1'.</span></span>

## <span data-ttu-id="c8f02-111">Parameter</span><span class="sxs-lookup"><span data-stu-id="c8f02-111">PARAMETERS</span></span>

### <span data-ttu-id="c8f02-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c8f02-112">-DefaultProfile</span></span>
<span data-ttu-id="c8f02-113">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="c8f02-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c8f02-114">-Name</span><span class="sxs-lookup"><span data-stu-id="c8f02-114">-Name</span></span>
<span data-ttu-id="c8f02-115">Geben Sie den Namen des Clusters an.</span><span class="sxs-lookup"><span data-stu-id="c8f02-115">Specify the name of the cluster.</span></span>

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

### <span data-ttu-id="c8f02-116">-NodeType</span><span class="sxs-lookup"><span data-stu-id="c8f02-116">-NodeType</span></span>
<span data-ttu-id="c8f02-117">Name des Knotentyps</span><span class="sxs-lookup"><span data-stu-id="c8f02-117">Node type name.</span></span>

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

### <span data-ttu-id="c8f02-118">-NumberOfNodesToAdd</span><span class="sxs-lookup"><span data-stu-id="c8f02-118">-NumberOfNodesToAdd</span></span>
<span data-ttu-id="c8f02-119">VM-Instanzennummer</span><span class="sxs-lookup"><span data-stu-id="c8f02-119">VM instance number.</span></span>

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

### <span data-ttu-id="c8f02-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c8f02-120">-ResourceGroupName</span></span>
<span data-ttu-id="c8f02-121">Gibt den Namen der Ressourcengruppe an.</span><span class="sxs-lookup"><span data-stu-id="c8f02-121">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="c8f02-122">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="c8f02-122">-Confirm</span></span>
<span data-ttu-id="c8f02-123">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="c8f02-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c8f02-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c8f02-124">-WhatIf</span></span>
<span data-ttu-id="c8f02-125">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="c8f02-125">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="c8f02-126">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="c8f02-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c8f02-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c8f02-127">CommonParameters</span></span>
<span data-ttu-id="c8f02-128">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c8f02-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c8f02-129">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c8f02-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c8f02-130">Eingaben</span><span class="sxs-lookup"><span data-stu-id="c8f02-130">INPUTS</span></span>

### <span data-ttu-id="c8f02-131">System. Int32</span><span class="sxs-lookup"><span data-stu-id="c8f02-131">System.Int32</span></span>
<span data-ttu-id="c8f02-132">Parameter: NumberOfNodesToAdd (ByValue)</span><span class="sxs-lookup"><span data-stu-id="c8f02-132">Parameters: NumberOfNodesToAdd (ByValue)</span></span>

### <span data-ttu-id="c8f02-133">System. String</span><span class="sxs-lookup"><span data-stu-id="c8f02-133">System.String</span></span>
<span data-ttu-id="c8f02-134">Parameter: NodeType (ByValue)</span><span class="sxs-lookup"><span data-stu-id="c8f02-134">Parameters: NodeType (ByValue)</span></span>

## <span data-ttu-id="c8f02-135">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="c8f02-135">OUTPUTS</span></span>

### <span data-ttu-id="c8f02-136">Microsoft. Azure. Commands. ServiceFabric. Models. PSCluster</span><span class="sxs-lookup"><span data-stu-id="c8f02-136">Microsoft.Azure.Commands.ServiceFabric.Models.PSCluster</span></span>

## <span data-ttu-id="c8f02-137">Notizen</span><span class="sxs-lookup"><span data-stu-id="c8f02-137">NOTES</span></span>

## <span data-ttu-id="c8f02-138">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="c8f02-138">RELATED LINKS</span></span>

[<span data-ttu-id="c8f02-139">Remove-AzureRmServiceFabricNode</span><span class="sxs-lookup"><span data-stu-id="c8f02-139">Remove-AzureRmServiceFabricNode</span></span>](./Remove-AzureRmServiceFabricNode.md)
