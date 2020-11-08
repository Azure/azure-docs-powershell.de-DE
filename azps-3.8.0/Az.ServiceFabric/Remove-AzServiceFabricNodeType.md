---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceFabric.dll-Help.xml
Module Name: Az.ServiceFabric
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicefabric/remove-azservicefabricnodetype
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Remove-AzServiceFabricNodeType.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Remove-AzServiceFabricNodeType.md
ms.openlocfilehash: bc21812003ca7e71b9f7fa726aea766e924d2519
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/21/2020
ms.locfileid: "93996373"
---
# <span data-ttu-id="beca7-101">Remove-AzServiceFabricNodeType</span><span class="sxs-lookup"><span data-stu-id="beca7-101">Remove-AzServiceFabricNodeType</span></span>

## <span data-ttu-id="beca7-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="beca7-102">SYNOPSIS</span></span>
<span data-ttu-id="beca7-103">Entfernen eines vollständigen Knotentyps aus einem Cluster</span><span class="sxs-lookup"><span data-stu-id="beca7-103">Remove a complete node type from a cluster.</span></span>

## <span data-ttu-id="beca7-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="beca7-104">SYNTAX</span></span>

```
Remove-AzServiceFabricNodeType [-ResourceGroupName] <String> [-Name] <String> -NodeType <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="beca7-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="beca7-105">DESCRIPTION</span></span>
<span data-ttu-id="beca7-106">Verwenden Sie **Remove-AzServiceFabricNodeType** , um alle Knoten aus einem bestimmten Knotentyp und dem Knotentyp aus einem Cluster zu entfernen.</span><span class="sxs-lookup"><span data-stu-id="beca7-106">Use the **Remove-AzServiceFabricNodeType** to remove all nodes from a specific node type and the node type from a cluster.</span></span> <span data-ttu-id="beca7-107">Dieser Befehl kann nicht zum Löschen des primären Knotentyps verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="beca7-107">This command cannot be used to delete the primary node type.</span></span>

## <span data-ttu-id="beca7-108">Beispiele</span><span class="sxs-lookup"><span data-stu-id="beca7-108">EXAMPLES</span></span>

### <span data-ttu-id="beca7-109">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="beca7-109">Example 1</span></span>
```powershell
PS c:> Remove-AzServiceFabricNodeType -ResourceGroupName 'Group1' -Name 'Contoso01SFCluster' -NodeTypeName 'nt1'
```

<span data-ttu-id="beca7-110">Mit diesem Befehl wird NodeType "NT1" aus dem Cluster entfernt.</span><span class="sxs-lookup"><span data-stu-id="beca7-110">This command will remove NodeType 'nt1' from the cluster.</span></span>

## <span data-ttu-id="beca7-111">Parameter</span><span class="sxs-lookup"><span data-stu-id="beca7-111">PARAMETERS</span></span>

### <span data-ttu-id="beca7-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="beca7-112">-DefaultProfile</span></span>
<span data-ttu-id="beca7-113">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="beca7-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="beca7-114">-Name</span><span class="sxs-lookup"><span data-stu-id="beca7-114">-Name</span></span>
<span data-ttu-id="beca7-115">Angeben des Namens des Clusters</span><span class="sxs-lookup"><span data-stu-id="beca7-115">Specify the name of the cluster</span></span>

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

### <span data-ttu-id="beca7-116">-NodeType</span><span class="sxs-lookup"><span data-stu-id="beca7-116">-NodeType</span></span>
<span data-ttu-id="beca7-117">Name des Knotentyps</span><span class="sxs-lookup"><span data-stu-id="beca7-117">The node type name</span></span>

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

### <span data-ttu-id="beca7-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="beca7-118">-ResourceGroupName</span></span>
<span data-ttu-id="beca7-119">Geben Sie den Namen der Ressourcengruppe an.</span><span class="sxs-lookup"><span data-stu-id="beca7-119">Specify the name of the resource group.</span></span>

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

### <span data-ttu-id="beca7-120">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="beca7-120">-Confirm</span></span>
<span data-ttu-id="beca7-121">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="beca7-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="beca7-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="beca7-122">-WhatIf</span></span>
<span data-ttu-id="beca7-123">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="beca7-123">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="beca7-124">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="beca7-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="beca7-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="beca7-125">CommonParameters</span></span>
<span data-ttu-id="beca7-126">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="beca7-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="beca7-127">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="beca7-127">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="beca7-128">Eingaben</span><span class="sxs-lookup"><span data-stu-id="beca7-128">INPUTS</span></span>

### <span data-ttu-id="beca7-129">System. String</span><span class="sxs-lookup"><span data-stu-id="beca7-129">System.String</span></span>

## <span data-ttu-id="beca7-130">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="beca7-130">OUTPUTS</span></span>

### <span data-ttu-id="beca7-131">Microsoft. Azure. Commands. ServiceFabric. Models. PSCluster</span><span class="sxs-lookup"><span data-stu-id="beca7-131">Microsoft.Azure.Commands.ServiceFabric.Models.PSCluster</span></span>

## <span data-ttu-id="beca7-132">Notizen</span><span class="sxs-lookup"><span data-stu-id="beca7-132">NOTES</span></span>

## <span data-ttu-id="beca7-133">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="beca7-133">RELATED LINKS</span></span>
