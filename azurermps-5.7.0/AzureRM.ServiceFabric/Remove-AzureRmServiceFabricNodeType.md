---
external help file: Microsoft.Azure.Commands.ServiceFabric.dll-Help.xml
Module Name: AzureRM.ServiceFabric
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.servicefabric/remove-azurermservicefabricnodetype
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceFabric/Commands.ServiceFabric/help/Remove-AzureRmServiceFabricNodeType.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceFabric/Commands.ServiceFabric/help/Remove-AzureRmServiceFabricNodeType.md
ms.openlocfilehash: f825d1ba1621a00be6196219d99dc188496ea5da
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93478226"
---
# <span data-ttu-id="70646-101">Remove-AzureRmServiceFabricNodeType</span><span class="sxs-lookup"><span data-stu-id="70646-101">Remove-AzureRmServiceFabricNodeType</span></span>

## <span data-ttu-id="70646-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="70646-102">SYNOPSIS</span></span>
<span data-ttu-id="70646-103">Entfernen eines vollständigen Knotentyps aus einem Cluster</span><span class="sxs-lookup"><span data-stu-id="70646-103">Remove a complete node type from a cluster.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="70646-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="70646-104">SYNTAX</span></span>

```
Remove-AzureRmServiceFabricNodeType [-ResourceGroupName] <String> [-Name] <String> -NodeType <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="70646-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="70646-105">DESCRIPTION</span></span>
<span data-ttu-id="70646-106">Verwenden Sie **Remove-AzureRmServiceFabricNodeType** , um alle Knoten aus einem bestimmten Knotentyp und dem Knotentyp aus einem Cluster zu entfernen.</span><span class="sxs-lookup"><span data-stu-id="70646-106">Use the **Remove-AzureRmServiceFabricNodeType** to remove all nodes from a specific node type and the node type from a cluster.</span></span> <span data-ttu-id="70646-107">Dieser Befehl kann nicht zum Löschen des primären Knotentyps verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="70646-107">This command cannot be used to delete the primary node type.</span></span>

## <span data-ttu-id="70646-108">Beispiele</span><span class="sxs-lookup"><span data-stu-id="70646-108">EXAMPLES</span></span>

### <span data-ttu-id="70646-109">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="70646-109">Example 1</span></span>
```
PS c:> Remove-AzureRmServiceFabricNodeType -ResourceGroupName 'Group1' -Name 'Contoso01SFCluster' -NodeTypeName 'nt1'
```

<span data-ttu-id="70646-110">Mit diesem Befehl wird NodeType "NT1" aus dem Cluster entfernt.</span><span class="sxs-lookup"><span data-stu-id="70646-110">This command will remove NodeType 'nt1' from the cluster.</span></span>

## <span data-ttu-id="70646-111">Parameter</span><span class="sxs-lookup"><span data-stu-id="70646-111">PARAMETERS</span></span>

### <span data-ttu-id="70646-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="70646-112">-DefaultProfile</span></span>
<span data-ttu-id="70646-113">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="70646-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="70646-114">-Name</span><span class="sxs-lookup"><span data-stu-id="70646-114">-Name</span></span>
<span data-ttu-id="70646-115">Geben Sie den Namen des Clusters an.</span><span class="sxs-lookup"><span data-stu-id="70646-115">Specify the name of the cluster.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ClusterName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="70646-116">-NodeType</span><span class="sxs-lookup"><span data-stu-id="70646-116">-NodeType</span></span>
<span data-ttu-id="70646-117">Der Name des Knotentyps.</span><span class="sxs-lookup"><span data-stu-id="70646-117">The node type name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="70646-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="70646-118">-ResourceGroupName</span></span>
<span data-ttu-id="70646-119">Gibt den Namen der Ressourcengruppe an.</span><span class="sxs-lookup"><span data-stu-id="70646-119">Specifies the name of the resource group.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="70646-120">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="70646-120">-Confirm</span></span>
<span data-ttu-id="70646-121">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="70646-121">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="70646-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="70646-122">-WhatIf</span></span>
<span data-ttu-id="70646-123">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="70646-123">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="70646-124">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="70646-124">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="70646-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="70646-125">CommonParameters</span></span>
<span data-ttu-id="70646-126">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="70646-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="70646-127">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="70646-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="70646-128">Eingaben</span><span class="sxs-lookup"><span data-stu-id="70646-128">INPUTS</span></span>

### <span data-ttu-id="70646-129">System. String</span><span class="sxs-lookup"><span data-stu-id="70646-129">System.String</span></span>

## <span data-ttu-id="70646-130">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="70646-130">OUTPUTS</span></span>

### <span data-ttu-id="70646-131">System. Object</span><span class="sxs-lookup"><span data-stu-id="70646-131">System.Object</span></span>

## <span data-ttu-id="70646-132">Notizen</span><span class="sxs-lookup"><span data-stu-id="70646-132">NOTES</span></span>

## <span data-ttu-id="70646-133">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="70646-133">RELATED LINKS</span></span>

