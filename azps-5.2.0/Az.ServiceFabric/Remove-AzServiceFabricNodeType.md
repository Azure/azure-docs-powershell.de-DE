---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceFabric.dll-Help.xml
Module Name: Az.ServiceFabric
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicefabric/remove-azservicefabricnodetype
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Remove-AzServiceFabricNodeType.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Remove-AzServiceFabricNodeType.md
ms.openlocfilehash: 172a0a2eae2b50c99b3540b654b9490cc8ac6e51
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98357901"
---
# <span data-ttu-id="8260b-101">Remove-AzServiceFabricNodeType</span><span class="sxs-lookup"><span data-stu-id="8260b-101">Remove-AzServiceFabricNodeType</span></span>

## <span data-ttu-id="8260b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8260b-102">SYNOPSIS</span></span>
<span data-ttu-id="8260b-103">Entfernen eines vollständigen Knotentyps aus einem Cluster</span><span class="sxs-lookup"><span data-stu-id="8260b-103">Remove a complete node type from a cluster.</span></span>

## <span data-ttu-id="8260b-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="8260b-104">SYNTAX</span></span>

```
Remove-AzServiceFabricNodeType [-ResourceGroupName] <String> [-Name] <String> -NodeType <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8260b-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="8260b-105">DESCRIPTION</span></span>
<span data-ttu-id="8260b-106">Verwenden Sie **den Remove-AzServiceFabricNodeType,** um alle Knoten von einem bestimmten Knotentyp und vom Knotentyp aus einem Cluster zu entfernen.</span><span class="sxs-lookup"><span data-stu-id="8260b-106">Use the **Remove-AzServiceFabricNodeType** to remove all nodes from a specific node type and the node type from a cluster.</span></span> <span data-ttu-id="8260b-107">Dieser Befehl kann nicht zum Löschen des primären Knotentyps verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="8260b-107">This command cannot be used to delete the primary node type.</span></span>

## <span data-ttu-id="8260b-108">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="8260b-108">EXAMPLES</span></span>

### <span data-ttu-id="8260b-109">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="8260b-109">Example 1</span></span>
```powershell
PS c:> Remove-AzServiceFabricNodeType -ResourceGroupName 'Group1' -Name 'Contoso01SFCluster' -NodeTypeName 'nt1'
```

<span data-ttu-id="8260b-110">Mit diesem Befehl wird NodeType 'nt1' aus dem Cluster entfernt.</span><span class="sxs-lookup"><span data-stu-id="8260b-110">This command will remove NodeType 'nt1' from the cluster.</span></span>

## <span data-ttu-id="8260b-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="8260b-111">PARAMETERS</span></span>

### <span data-ttu-id="8260b-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8260b-112">-DefaultProfile</span></span>
<span data-ttu-id="8260b-113">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="8260b-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8260b-114">-Name</span><span class="sxs-lookup"><span data-stu-id="8260b-114">-Name</span></span>
<span data-ttu-id="8260b-115">Angeben des Namens des Clusters</span><span class="sxs-lookup"><span data-stu-id="8260b-115">Specify the name of the cluster</span></span>

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

### <span data-ttu-id="8260b-116">-NodeType</span><span class="sxs-lookup"><span data-stu-id="8260b-116">-NodeType</span></span>
<span data-ttu-id="8260b-117">Der Name des Knotentyps</span><span class="sxs-lookup"><span data-stu-id="8260b-117">The node type name</span></span>

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

### <span data-ttu-id="8260b-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8260b-118">-ResourceGroupName</span></span>
<span data-ttu-id="8260b-119">Geben Sie den Namen der Ressourcengruppe an.</span><span class="sxs-lookup"><span data-stu-id="8260b-119">Specify the name of the resource group.</span></span>

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

### <span data-ttu-id="8260b-120">-Confirm</span><span class="sxs-lookup"><span data-stu-id="8260b-120">-Confirm</span></span>
<span data-ttu-id="8260b-121">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="8260b-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8260b-122">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="8260b-122">-WhatIf</span></span>
<span data-ttu-id="8260b-123">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="8260b-123">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8260b-124">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="8260b-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8260b-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8260b-125">CommonParameters</span></span>
<span data-ttu-id="8260b-126">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8260b-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8260b-127">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="8260b-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8260b-128">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="8260b-128">INPUTS</span></span>

### <span data-ttu-id="8260b-129">System.String</span><span class="sxs-lookup"><span data-stu-id="8260b-129">System.String</span></span>

## <span data-ttu-id="8260b-130">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="8260b-130">OUTPUTS</span></span>

### <span data-ttu-id="8260b-131">Microsoft.Azure.Commands.ServiceFabric.Models.PSCluster</span><span class="sxs-lookup"><span data-stu-id="8260b-131">Microsoft.Azure.Commands.ServiceFabric.Models.PSCluster</span></span>

## <span data-ttu-id="8260b-132">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="8260b-132">NOTES</span></span>

## <span data-ttu-id="8260b-133">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="8260b-133">RELATED LINKS</span></span>
