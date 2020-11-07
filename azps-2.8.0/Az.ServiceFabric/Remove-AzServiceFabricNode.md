---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceFabric.dll-Help.xml
Module Name: Az.ServiceFabric
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicefabric/remove-azservicefabricnode
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Remove-AzServiceFabricNode.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Remove-AzServiceFabricNode.md
ms.openlocfilehash: 10adef91eab42f49459ba6fb9ad9130b42d74e01
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93823163"
---
# <span data-ttu-id="7bd51-101">Remove-AzServiceFabricNode</span><span class="sxs-lookup"><span data-stu-id="7bd51-101">Remove-AzServiceFabricNode</span></span>

## <span data-ttu-id="7bd51-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="7bd51-102">SYNOPSIS</span></span>
<span data-ttu-id="7bd51-103">Entfernen von Knoten aus dem bestimmten Knotentyp aus einem Cluster</span><span class="sxs-lookup"><span data-stu-id="7bd51-103">Remove nodes from the specific node type from a cluster.</span></span>

## <span data-ttu-id="7bd51-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="7bd51-104">SYNTAX</span></span>

```
Remove-AzServiceFabricNode -NumberOfNodesToRemove <Int32> [-ResourceGroupName] <String> [-Name] <String>
 -NodeType <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7bd51-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="7bd51-105">DESCRIPTION</span></span>
<span data-ttu-id="7bd51-106">Verwenden **Sie Remove-AzServiceFabricNode** , um Knoten aus einem bestimmten Knotentyp aus einem Cluster zu entfernen.</span><span class="sxs-lookup"><span data-stu-id="7bd51-106">Use **Remove-AzServiceFabricNode** to remove nodes from a specific node type from a cluster.</span></span> <span data-ttu-id="7bd51-107">Die Entfernung wird nur fortgesetzt, wenn Sie den Kriterien des Cluster Zustands entspricht.</span><span class="sxs-lookup"><span data-stu-id="7bd51-107">The removal proceeds only if it meets cluster health metrics.</span></span>

## <span data-ttu-id="7bd51-108">Beispiele</span><span class="sxs-lookup"><span data-stu-id="7bd51-108">EXAMPLES</span></span>

### <span data-ttu-id="7bd51-109">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="7bd51-109">Example 1</span></span>
```powershell
PS c:> Remove-AzServiceFabricNode -ResourceGroupName 'Group1' -Name 'Contoso01SFCluster' -NodeTypeName 'nt1' -NumberOfNodesToRemove 2
```

<span data-ttu-id="7bd51-110">Mit diesem Befehl werden 2 Knoten vom NodeType "NT1" entfernt.</span><span class="sxs-lookup"><span data-stu-id="7bd51-110">This command will remove 2 nodes from the NodeType 'nt1'.</span></span>

## <span data-ttu-id="7bd51-111">Parameter</span><span class="sxs-lookup"><span data-stu-id="7bd51-111">PARAMETERS</span></span>

### <span data-ttu-id="7bd51-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7bd51-112">-DefaultProfile</span></span>
<span data-ttu-id="7bd51-113">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="7bd51-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7bd51-114">-Name</span><span class="sxs-lookup"><span data-stu-id="7bd51-114">-Name</span></span>
<span data-ttu-id="7bd51-115">Angeben des Namens des Clusters</span><span class="sxs-lookup"><span data-stu-id="7bd51-115">Specify the name of the cluster</span></span>

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

### <span data-ttu-id="7bd51-116">-NodeType</span><span class="sxs-lookup"><span data-stu-id="7bd51-116">-NodeType</span></span>
<span data-ttu-id="7bd51-117">Name des Knotentyps</span><span class="sxs-lookup"><span data-stu-id="7bd51-117">Node type name</span></span>

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

### <span data-ttu-id="7bd51-118">-NumberOfNodesToRemove</span><span class="sxs-lookup"><span data-stu-id="7bd51-118">-NumberOfNodesToRemove</span></span>
<span data-ttu-id="7bd51-119">Die Anzahl der hinzuzufügenden Knoten</span><span class="sxs-lookup"><span data-stu-id="7bd51-119">The number of nodes to add</span></span>

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

### <span data-ttu-id="7bd51-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7bd51-120">-ResourceGroupName</span></span>
<span data-ttu-id="7bd51-121">Geben Sie den Namen der Ressourcengruppe an.</span><span class="sxs-lookup"><span data-stu-id="7bd51-121">Specify the name of the resource group.</span></span>

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

### <span data-ttu-id="7bd51-122">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="7bd51-122">-Confirm</span></span>
<span data-ttu-id="7bd51-123">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="7bd51-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7bd51-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7bd51-124">-WhatIf</span></span>
<span data-ttu-id="7bd51-125">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="7bd51-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7bd51-126">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="7bd51-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7bd51-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7bd51-127">CommonParameters</span></span>
<span data-ttu-id="7bd51-128">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7bd51-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7bd51-129">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7bd51-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7bd51-130">Eingaben</span><span class="sxs-lookup"><span data-stu-id="7bd51-130">INPUTS</span></span>

### <span data-ttu-id="7bd51-131">System. Int32</span><span class="sxs-lookup"><span data-stu-id="7bd51-131">System.Int32</span></span>

### <span data-ttu-id="7bd51-132">System. String</span><span class="sxs-lookup"><span data-stu-id="7bd51-132">System.String</span></span>

## <span data-ttu-id="7bd51-133">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="7bd51-133">OUTPUTS</span></span>

### <span data-ttu-id="7bd51-134">Microsoft. Azure. Commands. ServiceFabric. Models. PSCluster</span><span class="sxs-lookup"><span data-stu-id="7bd51-134">Microsoft.Azure.Commands.ServiceFabric.Models.PSCluster</span></span>

## <span data-ttu-id="7bd51-135">Notizen</span><span class="sxs-lookup"><span data-stu-id="7bd51-135">NOTES</span></span>

## <span data-ttu-id="7bd51-136">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="7bd51-136">RELATED LINKS</span></span>

[<span data-ttu-id="7bd51-137">Add-AzServiceFabricNode</span><span class="sxs-lookup"><span data-stu-id="7bd51-137">Add-AzServiceFabricNode</span></span>](./Add-AzServiceFabricNode.md)
