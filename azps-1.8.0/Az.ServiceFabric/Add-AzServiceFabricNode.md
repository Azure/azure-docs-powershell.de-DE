---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceFabric.dll-Help.xml
Module Name: Az.ServiceFabric
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicefabric/add-azservicefabricnode
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Add-AzServiceFabricNode.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Add-AzServiceFabricNode.md
ms.openlocfilehash: 698dfcb55a7a8039f0e4c56036946ccbfa8e9ba0
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93659327"
---
# <span data-ttu-id="71280-101">Add-AzServiceFabricNode</span><span class="sxs-lookup"><span data-stu-id="71280-101">Add-AzServiceFabricNode</span></span>

## <span data-ttu-id="71280-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="71280-102">SYNOPSIS</span></span>
<span data-ttu-id="71280-103">Fügen Sie dem jeweiligen Knotentyp im Clusterknoten hinzu.</span><span class="sxs-lookup"><span data-stu-id="71280-103">Add nodes to the specific node type in the cluster.</span></span>

## <span data-ttu-id="71280-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="71280-104">SYNTAX</span></span>

```
Add-AzServiceFabricNode -NumberOfNodesToAdd <Int32> [-ResourceGroupName] <String> [-Name] <String>
 -NodeType <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="71280-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="71280-105">DESCRIPTION</span></span>
<span data-ttu-id="71280-106">Verwenden **Sie Add-AzServiceFabricNode** , um dem jeweiligen Knotentyp Knoten hinzuzufügen.</span><span class="sxs-lookup"><span data-stu-id="71280-106">Use **Add-AzServiceFabricNode** to add nodes to the specific node type.</span></span> <span data-ttu-id="71280-107">Sie müssen lediglich die Anzahl der Knoten angeben, die Sie einem Knotentyp hinzufügen möchten.</span><span class="sxs-lookup"><span data-stu-id="71280-107">You just need to specify the number of nodes you want to add to a node type.</span></span>

## <span data-ttu-id="71280-108">Beispiele</span><span class="sxs-lookup"><span data-stu-id="71280-108">EXAMPLES</span></span>

### <span data-ttu-id="71280-109">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="71280-109">Example 1</span></span>
```
PS c:> Add-AzServiceFabricNode -ResourceGroupName 'Group1' -Name 'Contoso01SFCluster' -NumberOfNodesToAdd 2 -NodeTypeName 'nt1'
```

<span data-ttu-id="71280-110">Mit diesem Befehl werden dem Knotentyp "N1" 2 Knoten hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="71280-110">This command will add 2 nodes to the node type 'n1'.</span></span>

## <span data-ttu-id="71280-111">Parameter</span><span class="sxs-lookup"><span data-stu-id="71280-111">PARAMETERS</span></span>

### <span data-ttu-id="71280-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="71280-112">-DefaultProfile</span></span>
<span data-ttu-id="71280-113">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="71280-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="71280-114">-Name</span><span class="sxs-lookup"><span data-stu-id="71280-114">-Name</span></span>
<span data-ttu-id="71280-115">Geben Sie den Namen des Clusters an.</span><span class="sxs-lookup"><span data-stu-id="71280-115">Specify the name of the cluster.</span></span>

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

### <span data-ttu-id="71280-116">-NodeType</span><span class="sxs-lookup"><span data-stu-id="71280-116">-NodeType</span></span>
<span data-ttu-id="71280-117">Name des Knotentyps</span><span class="sxs-lookup"><span data-stu-id="71280-117">Node type name.</span></span>

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

### <span data-ttu-id="71280-118">-NumberOfNodesToAdd</span><span class="sxs-lookup"><span data-stu-id="71280-118">-NumberOfNodesToAdd</span></span>
<span data-ttu-id="71280-119">VM-Instanzennummer</span><span class="sxs-lookup"><span data-stu-id="71280-119">VM instance number.</span></span>

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

### <span data-ttu-id="71280-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="71280-120">-ResourceGroupName</span></span>
<span data-ttu-id="71280-121">Gibt den Namen der Ressourcengruppe an.</span><span class="sxs-lookup"><span data-stu-id="71280-121">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="71280-122">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="71280-122">-Confirm</span></span>
<span data-ttu-id="71280-123">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="71280-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="71280-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="71280-124">-WhatIf</span></span>
<span data-ttu-id="71280-125">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="71280-125">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="71280-126">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="71280-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="71280-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="71280-127">CommonParameters</span></span>
<span data-ttu-id="71280-128">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="71280-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="71280-129">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="71280-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="71280-130">Eingaben</span><span class="sxs-lookup"><span data-stu-id="71280-130">INPUTS</span></span>

### <span data-ttu-id="71280-131">System. Int32</span><span class="sxs-lookup"><span data-stu-id="71280-131">System.Int32</span></span>

### <span data-ttu-id="71280-132">System. String</span><span class="sxs-lookup"><span data-stu-id="71280-132">System.String</span></span>

## <span data-ttu-id="71280-133">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="71280-133">OUTPUTS</span></span>

### <span data-ttu-id="71280-134">Microsoft. Azure. Commands. ServiceFabric. Models. PSCluster</span><span class="sxs-lookup"><span data-stu-id="71280-134">Microsoft.Azure.Commands.ServiceFabric.Models.PSCluster</span></span>

## <span data-ttu-id="71280-135">Notizen</span><span class="sxs-lookup"><span data-stu-id="71280-135">NOTES</span></span>

## <span data-ttu-id="71280-136">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="71280-136">RELATED LINKS</span></span>

[<span data-ttu-id="71280-137">Remove-AzServiceFabricNode</span><span class="sxs-lookup"><span data-stu-id="71280-137">Remove-AzServiceFabricNode</span></span>](./Remove-AzServiceFabricNode.md)
