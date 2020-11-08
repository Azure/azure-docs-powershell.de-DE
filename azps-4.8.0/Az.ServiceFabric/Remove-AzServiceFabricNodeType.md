---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceFabric.dll-Help.xml
Module Name: Az.ServiceFabric
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicefabric/remove-azservicefabricnodetype
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Remove-AzServiceFabricNodeType.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Remove-AzServiceFabricNodeType.md
ms.openlocfilehash: 172a0a2eae2b50c99b3540b654b9490cc8ac6e51
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94166080"
---
# <span data-ttu-id="e751b-101">Remove-AzServiceFabricNodeType</span><span class="sxs-lookup"><span data-stu-id="e751b-101">Remove-AzServiceFabricNodeType</span></span>

## <span data-ttu-id="e751b-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="e751b-102">SYNOPSIS</span></span>
<span data-ttu-id="e751b-103">Entfernen eines vollständigen Knotentyps aus einem Cluster</span><span class="sxs-lookup"><span data-stu-id="e751b-103">Remove a complete node type from a cluster.</span></span>

## <span data-ttu-id="e751b-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="e751b-104">SYNTAX</span></span>

```
Remove-AzServiceFabricNodeType [-ResourceGroupName] <String> [-Name] <String> -NodeType <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e751b-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="e751b-105">DESCRIPTION</span></span>
<span data-ttu-id="e751b-106">Verwenden Sie **Remove-AzServiceFabricNodeType** , um alle Knoten aus einem bestimmten Knotentyp und dem Knotentyp aus einem Cluster zu entfernen.</span><span class="sxs-lookup"><span data-stu-id="e751b-106">Use the **Remove-AzServiceFabricNodeType** to remove all nodes from a specific node type and the node type from a cluster.</span></span> <span data-ttu-id="e751b-107">Dieser Befehl kann nicht zum Löschen des primären Knotentyps verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="e751b-107">This command cannot be used to delete the primary node type.</span></span>

## <span data-ttu-id="e751b-108">Beispiele</span><span class="sxs-lookup"><span data-stu-id="e751b-108">EXAMPLES</span></span>

### <span data-ttu-id="e751b-109">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="e751b-109">Example 1</span></span>
```powershell
PS c:> Remove-AzServiceFabricNodeType -ResourceGroupName 'Group1' -Name 'Contoso01SFCluster' -NodeTypeName 'nt1'
```

<span data-ttu-id="e751b-110">Mit diesem Befehl wird NodeType "NT1" aus dem Cluster entfernt.</span><span class="sxs-lookup"><span data-stu-id="e751b-110">This command will remove NodeType 'nt1' from the cluster.</span></span>

## <span data-ttu-id="e751b-111">Parameter</span><span class="sxs-lookup"><span data-stu-id="e751b-111">PARAMETERS</span></span>

### <span data-ttu-id="e751b-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e751b-112">-DefaultProfile</span></span>
<span data-ttu-id="e751b-113">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="e751b-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e751b-114">-Name</span><span class="sxs-lookup"><span data-stu-id="e751b-114">-Name</span></span>
<span data-ttu-id="e751b-115">Angeben des Namens des Clusters</span><span class="sxs-lookup"><span data-stu-id="e751b-115">Specify the name of the cluster</span></span>

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

### <span data-ttu-id="e751b-116">-NodeType</span><span class="sxs-lookup"><span data-stu-id="e751b-116">-NodeType</span></span>
<span data-ttu-id="e751b-117">Name des Knotentyps</span><span class="sxs-lookup"><span data-stu-id="e751b-117">The node type name</span></span>

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

### <span data-ttu-id="e751b-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e751b-118">-ResourceGroupName</span></span>
<span data-ttu-id="e751b-119">Geben Sie den Namen der Ressourcengruppe an.</span><span class="sxs-lookup"><span data-stu-id="e751b-119">Specify the name of the resource group.</span></span>

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

### <span data-ttu-id="e751b-120">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="e751b-120">-Confirm</span></span>
<span data-ttu-id="e751b-121">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="e751b-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e751b-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e751b-122">-WhatIf</span></span>
<span data-ttu-id="e751b-123">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="e751b-123">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e751b-124">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="e751b-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e751b-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e751b-125">CommonParameters</span></span>
<span data-ttu-id="e751b-126">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e751b-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e751b-127">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="e751b-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e751b-128">Eingaben</span><span class="sxs-lookup"><span data-stu-id="e751b-128">INPUTS</span></span>

### <span data-ttu-id="e751b-129">System. String</span><span class="sxs-lookup"><span data-stu-id="e751b-129">System.String</span></span>

## <span data-ttu-id="e751b-130">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="e751b-130">OUTPUTS</span></span>

### <span data-ttu-id="e751b-131">Microsoft. Azure. Commands. ServiceFabric. Models. PSCluster</span><span class="sxs-lookup"><span data-stu-id="e751b-131">Microsoft.Azure.Commands.ServiceFabric.Models.PSCluster</span></span>

## <span data-ttu-id="e751b-132">Notizen</span><span class="sxs-lookup"><span data-stu-id="e751b-132">NOTES</span></span>

## <span data-ttu-id="e751b-133">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="e751b-133">RELATED LINKS</span></span>
