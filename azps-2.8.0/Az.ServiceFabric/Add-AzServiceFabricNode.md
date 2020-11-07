---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceFabric.dll-Help.xml
Module Name: Az.ServiceFabric
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicefabric/add-azservicefabricnode
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Add-AzServiceFabricNode.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Add-AzServiceFabricNode.md
ms.openlocfilehash: fdcc8946070994cd172514f8da1578328ae61db2
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93823199"
---
# <span data-ttu-id="fca7e-101">Add-AzServiceFabricNode</span><span class="sxs-lookup"><span data-stu-id="fca7e-101">Add-AzServiceFabricNode</span></span>

## <span data-ttu-id="fca7e-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="fca7e-102">SYNOPSIS</span></span>
<span data-ttu-id="fca7e-103">Fügen Sie dem jeweiligen Knotentyp im Clusterknoten hinzu.</span><span class="sxs-lookup"><span data-stu-id="fca7e-103">Add nodes to the specific node type in the cluster.</span></span>

## <span data-ttu-id="fca7e-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="fca7e-104">SYNTAX</span></span>

```
Add-AzServiceFabricNode -NumberOfNodesToAdd <Int32> [-ResourceGroupName] <String> [-Name] <String>
 -NodeType <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="fca7e-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="fca7e-105">DESCRIPTION</span></span>
<span data-ttu-id="fca7e-106">Verwenden **Sie Add-AzServiceFabricNode** , um dem jeweiligen Knotentyp Knoten hinzuzufügen.</span><span class="sxs-lookup"><span data-stu-id="fca7e-106">Use **Add-AzServiceFabricNode** to add nodes to the specific node type.</span></span> <span data-ttu-id="fca7e-107">Sie müssen lediglich die Anzahl der Knoten angeben, die Sie einem Knotentyp hinzufügen möchten.</span><span class="sxs-lookup"><span data-stu-id="fca7e-107">You just need to specify the number of nodes you want to add to a node type.</span></span>

## <span data-ttu-id="fca7e-108">Beispiele</span><span class="sxs-lookup"><span data-stu-id="fca7e-108">EXAMPLES</span></span>

### <span data-ttu-id="fca7e-109">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="fca7e-109">Example 1</span></span>
```powershell
PS c:> Add-AzServiceFabricNode -ResourceGroupName 'Group1' -Name 'Contoso01SFCluster' -NumberOfNodesToAdd 2 -NodeTypeName 'nt1'
```

<span data-ttu-id="fca7e-110">Mit diesem Befehl werden dem Knotentyp "N1" 2 Knoten hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="fca7e-110">This command will add 2 nodes to the node type 'n1'.</span></span>

## <span data-ttu-id="fca7e-111">Parameter</span><span class="sxs-lookup"><span data-stu-id="fca7e-111">PARAMETERS</span></span>

### <span data-ttu-id="fca7e-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fca7e-112">-DefaultProfile</span></span>
<span data-ttu-id="fca7e-113">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="fca7e-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="fca7e-114">-Name</span><span class="sxs-lookup"><span data-stu-id="fca7e-114">-Name</span></span>
<span data-ttu-id="fca7e-115">Angeben des Namens des Clusters</span><span class="sxs-lookup"><span data-stu-id="fca7e-115">Specify the name of the cluster</span></span>

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

### <span data-ttu-id="fca7e-116">-NodeType</span><span class="sxs-lookup"><span data-stu-id="fca7e-116">-NodeType</span></span>
<span data-ttu-id="fca7e-117">Name des Knotentyps</span><span class="sxs-lookup"><span data-stu-id="fca7e-117">Node type name</span></span>

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

### <span data-ttu-id="fca7e-118">-NumberOfNodesToAdd</span><span class="sxs-lookup"><span data-stu-id="fca7e-118">-NumberOfNodesToAdd</span></span>
<span data-ttu-id="fca7e-119">Die Anzahl der hinzuzufügenden Knoten</span><span class="sxs-lookup"><span data-stu-id="fca7e-119">The number of nodes to add</span></span>

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

### <span data-ttu-id="fca7e-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fca7e-120">-ResourceGroupName</span></span>
<span data-ttu-id="fca7e-121">Geben Sie den Namen der Ressourcengruppe an.</span><span class="sxs-lookup"><span data-stu-id="fca7e-121">Specify the name of the resource group.</span></span>

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

### <span data-ttu-id="fca7e-122">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="fca7e-122">-Confirm</span></span>
<span data-ttu-id="fca7e-123">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="fca7e-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fca7e-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fca7e-124">-WhatIf</span></span>
<span data-ttu-id="fca7e-125">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="fca7e-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="fca7e-126">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="fca7e-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="fca7e-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fca7e-127">CommonParameters</span></span>
<span data-ttu-id="fca7e-128">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fca7e-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fca7e-129">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fca7e-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fca7e-130">Eingaben</span><span class="sxs-lookup"><span data-stu-id="fca7e-130">INPUTS</span></span>

### <span data-ttu-id="fca7e-131">System. Int32</span><span class="sxs-lookup"><span data-stu-id="fca7e-131">System.Int32</span></span>

### <span data-ttu-id="fca7e-132">System. String</span><span class="sxs-lookup"><span data-stu-id="fca7e-132">System.String</span></span>

## <span data-ttu-id="fca7e-133">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="fca7e-133">OUTPUTS</span></span>

### <span data-ttu-id="fca7e-134">Microsoft. Azure. Commands. ServiceFabric. Models. PSCluster</span><span class="sxs-lookup"><span data-stu-id="fca7e-134">Microsoft.Azure.Commands.ServiceFabric.Models.PSCluster</span></span>

## <span data-ttu-id="fca7e-135">Notizen</span><span class="sxs-lookup"><span data-stu-id="fca7e-135">NOTES</span></span>

## <span data-ttu-id="fca7e-136">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="fca7e-136">RELATED LINKS</span></span>

[<span data-ttu-id="fca7e-137">Remove-AzServiceFabricNode</span><span class="sxs-lookup"><span data-stu-id="fca7e-137">Remove-AzServiceFabricNode</span></span>](./Remove-AzServiceFabricNode.md)
