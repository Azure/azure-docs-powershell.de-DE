---
external help file: Microsoft.Azure.Commands.ServiceFabric.dll-Help.xml
Module Name: AzureRM.ServiceFabric
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceFabric/Commands.ServiceFabric/help/Remove-AzureRmServiceFabricNode.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceFabric/Commands.ServiceFabric/help/Remove-AzureRmServiceFabricNode.md
ms.openlocfilehash: cbf23af4c98e8174091b467e6e05ed5de6ae20c4
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93481553"
---
# <span data-ttu-id="835a6-101">Remove-AzureRmServiceFabricNode</span><span class="sxs-lookup"><span data-stu-id="835a6-101">Remove-AzureRmServiceFabricNode</span></span>

## <span data-ttu-id="835a6-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="835a6-102">SYNOPSIS</span></span>
<span data-ttu-id="835a6-103">Entfernen von Knoten aus dem bestimmten Knotentyp aus einem Cluster</span><span class="sxs-lookup"><span data-stu-id="835a6-103">Remove nodes from the specific node type from a cluster.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="835a6-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="835a6-104">SYNTAX</span></span>

```
Remove-AzureRmServiceFabricNode [-ResourceGroupName] <String> [-Name] <String> -NodeType <String>
 -NumberOfNodesToRemove <Int32> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="835a6-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="835a6-105">DESCRIPTION</span></span>
<span data-ttu-id="835a6-106">Verwenden **Sie Remove-AzureRmServiceFabricNode** , um Knoten aus einem bestimmten Knotentyp aus einem Cluster zu entfernen.</span><span class="sxs-lookup"><span data-stu-id="835a6-106">Use **Remove-AzureRmServiceFabricNode** to remove nodes from a specific node type from a cluster.</span></span> <span data-ttu-id="835a6-107">Die Entfernung wird nur fortgesetzt, wenn Sie den Kriterien des Cluster Zustands entspricht.</span><span class="sxs-lookup"><span data-stu-id="835a6-107">The removal proceeds only if it meets cluster health metrics.</span></span>

## <span data-ttu-id="835a6-108">Beispiele</span><span class="sxs-lookup"><span data-stu-id="835a6-108">EXAMPLES</span></span>

### <span data-ttu-id="835a6-109">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="835a6-109">Example 1</span></span>
```
PS c:> Remove-AzureRmServiceFabricNode -ResourceGroupName 'Group1' -Name 'Contoso01SFCluster' -NodeTypeName 'nt1' -NumberOfNodesToRemove 2
```

<span data-ttu-id="835a6-110">Mit diesem Befehl werden 2 Knoten vom NodeType "NT1" entfernt.</span><span class="sxs-lookup"><span data-stu-id="835a6-110">This command will remove 2 nodes from the NodeType 'nt1'.</span></span>

## <span data-ttu-id="835a6-111">Parameter</span><span class="sxs-lookup"><span data-stu-id="835a6-111">PARAMETERS</span></span>

### <span data-ttu-id="835a6-112">-Name</span><span class="sxs-lookup"><span data-stu-id="835a6-112">-Name</span></span>
<span data-ttu-id="835a6-113">Geben Sie den Namen des Clusters an.</span><span class="sxs-lookup"><span data-stu-id="835a6-113">Specify the name of the cluster.</span></span>

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

### <span data-ttu-id="835a6-114">-NodeType</span><span class="sxs-lookup"><span data-stu-id="835a6-114">-NodeType</span></span>
<span data-ttu-id="835a6-115">Name des Knotentyps</span><span class="sxs-lookup"><span data-stu-id="835a6-115">Node type name.</span></span>

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

### <span data-ttu-id="835a6-116">-NumberOfNodesToRemove</span><span class="sxs-lookup"><span data-stu-id="835a6-116">-NumberOfNodesToRemove</span></span>
<span data-ttu-id="835a6-117">Die Anzahl der zu entfernenden Knoten.</span><span class="sxs-lookup"><span data-stu-id="835a6-117">Number of nodes to remove.</span></span>

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

### <span data-ttu-id="835a6-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="835a6-118">-ResourceGroupName</span></span>
<span data-ttu-id="835a6-119">Gibt den Namen der Ressourcengruppe an.</span><span class="sxs-lookup"><span data-stu-id="835a6-119">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="835a6-120">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="835a6-120">-Confirm</span></span>
<span data-ttu-id="835a6-121">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="835a6-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="835a6-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="835a6-122">-WhatIf</span></span>
<span data-ttu-id="835a6-123">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="835a6-123">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="835a6-124">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="835a6-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="835a6-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="835a6-125">-DefaultProfile</span></span>
<span data-ttu-id="835a6-126">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="835a6-126">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="835a6-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="835a6-127">CommonParameters</span></span>
<span data-ttu-id="835a6-128">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="835a6-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="835a6-129">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="835a6-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="835a6-130">Eingaben</span><span class="sxs-lookup"><span data-stu-id="835a6-130">INPUTS</span></span>

### <span data-ttu-id="835a6-131">System. Int32</span><span class="sxs-lookup"><span data-stu-id="835a6-131">System.Int32</span></span>
<span data-ttu-id="835a6-132">System. String</span><span class="sxs-lookup"><span data-stu-id="835a6-132">System.String</span></span>

## <span data-ttu-id="835a6-133">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="835a6-133">OUTPUTS</span></span>

### <span data-ttu-id="835a6-134">System. Object</span><span class="sxs-lookup"><span data-stu-id="835a6-134">System.Object</span></span>

## <span data-ttu-id="835a6-135">Notizen</span><span class="sxs-lookup"><span data-stu-id="835a6-135">NOTES</span></span>

## <span data-ttu-id="835a6-136">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="835a6-136">RELATED LINKS</span></span>

[<span data-ttu-id="835a6-137">Add-AzureRmServiceFabricNode</span><span class="sxs-lookup"><span data-stu-id="835a6-137">Add-AzureRmServiceFabricNode</span></span>](./Add-AzureRmServiceFabricNode.md) 
