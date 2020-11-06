---
external help file: Microsoft.Azure.Commands.ServiceFabric.dll-Help.xml
Module Name: AzureRM.ServiceFabric
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.servicefabric/update-azurermservicefabricdurability
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceFabric/Commands.ServiceFabric/help/Update-AzureRmServiceFabricDurability.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceFabric/Commands.ServiceFabric/help/Update-AzureRmServiceFabricDurability.md
ms.openlocfilehash: 56a6afff6551ae0191ac1f17d3a52c47940e045a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93497290"
---
# <span data-ttu-id="b5ee0-101">Update-AzureRmServiceFabricDurability</span><span class="sxs-lookup"><span data-stu-id="b5ee0-101">Update-AzureRmServiceFabricDurability</span></span>

## <span data-ttu-id="b5ee0-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="b5ee0-102">SYNOPSIS</span></span>
<span data-ttu-id="b5ee0-103">Aktualisieren Sie die Haltbarkeits-oder VmSku eines Knotentyps im Cluster.</span><span class="sxs-lookup"><span data-stu-id="b5ee0-103">Update the durability tier or VmSku of a node type in the cluster.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b5ee0-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="b5ee0-104">SYNTAX</span></span>

```
Update-AzureRmServiceFabricDurability [-ResourceGroupName] <String> [-Name] <String> -NodeType <String>
 -DurabilityLevel <DurabilityLevel> [-Sku <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b5ee0-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="b5ee0-105">DESCRIPTION</span></span>
<span data-ttu-id="b5ee0-106">Verwenden Sie **Update-AzureRmServiceFabricDurability** , um die Lebensdauer oder SKU des Clusters zu aktualisieren.</span><span class="sxs-lookup"><span data-stu-id="b5ee0-106">Use **Update-AzureRmServiceFabricDurability** to update durability or SKU of the cluster.</span></span>

## <span data-ttu-id="b5ee0-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="b5ee0-107">EXAMPLES</span></span>

### <span data-ttu-id="b5ee0-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="b5ee0-108">Example 1</span></span>
```
PS c:> Update-AzureRmServiceFabricDurability -ResourceGroupName 'Group1' -Name 'Contoso01SFCluster' -DurabilityLevel Silver -NodeType nt1
```

<span data-ttu-id="b5ee0-109">Mit diesem Befehl wird die Haltbarkeits Stufe des NodeType "NT1" in Silver geändert.</span><span class="sxs-lookup"><span data-stu-id="b5ee0-109">This command changes durability tier of the NodeType 'nt1' to silver.</span></span>

## <span data-ttu-id="b5ee0-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="b5ee0-110">PARAMETERS</span></span>

### <span data-ttu-id="b5ee0-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b5ee0-111">-DefaultProfile</span></span>
<span data-ttu-id="b5ee0-112">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="b5ee0-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b5ee0-113">-DurabilityLevel</span><span class="sxs-lookup"><span data-stu-id="b5ee0-113">-DurabilityLevel</span></span>
<span data-ttu-id="b5ee0-114">Geben Sie den Haltbarkeits Grad an.</span><span class="sxs-lookup"><span data-stu-id="b5ee0-114">Specify durability level.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ServiceFabric.Models.DurabilityLevel
Parameter Sets: (All)
Aliases: Level
Accepted values: Bronze, Silver, Gold

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b5ee0-115">-Name</span><span class="sxs-lookup"><span data-stu-id="b5ee0-115">-Name</span></span>
<span data-ttu-id="b5ee0-116">Geben Sie den Namen des Clusters an.</span><span class="sxs-lookup"><span data-stu-id="b5ee0-116">Specify the name of the cluster.</span></span>

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

### <span data-ttu-id="b5ee0-117">-NodeType</span><span class="sxs-lookup"><span data-stu-id="b5ee0-117">-NodeType</span></span>
<span data-ttu-id="b5ee0-118">Geben Sie den Namen des Service Fabric-Knotentyps an.</span><span class="sxs-lookup"><span data-stu-id="b5ee0-118">Specify Service Fabric node type name.</span></span>

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

### <span data-ttu-id="b5ee0-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b5ee0-119">-ResourceGroupName</span></span>
<span data-ttu-id="b5ee0-120">Gibt den Namen der Ressourcengruppe an.</span><span class="sxs-lookup"><span data-stu-id="b5ee0-120">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="b5ee0-121">-SKU</span><span class="sxs-lookup"><span data-stu-id="b5ee0-121">-Sku</span></span>
<span data-ttu-id="b5ee0-122">Geben Sie die SKU des Knotentyps an.</span><span class="sxs-lookup"><span data-stu-id="b5ee0-122">Specify the SKU of the node type.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b5ee0-123">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="b5ee0-123">-Confirm</span></span>
<span data-ttu-id="b5ee0-124">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="b5ee0-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b5ee0-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b5ee0-125">-WhatIf</span></span>
<span data-ttu-id="b5ee0-126">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="b5ee0-126">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="b5ee0-127">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="b5ee0-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b5ee0-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b5ee0-128">CommonParameters</span></span>
<span data-ttu-id="b5ee0-129">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b5ee0-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b5ee0-130">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b5ee0-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b5ee0-131">Eingaben</span><span class="sxs-lookup"><span data-stu-id="b5ee0-131">INPUTS</span></span>

### <span data-ttu-id="b5ee0-132">System. String</span><span class="sxs-lookup"><span data-stu-id="b5ee0-132">System.String</span></span>
<span data-ttu-id="b5ee0-133">Parameter: NodeType (ByValue), SKU (ByValue)</span><span class="sxs-lookup"><span data-stu-id="b5ee0-133">Parameters: NodeType (ByValue), Sku (ByValue)</span></span>

### <span data-ttu-id="b5ee0-134">Microsoft. Azure. Commands. ServiceFabric. Models. DurabilityLevel</span><span class="sxs-lookup"><span data-stu-id="b5ee0-134">Microsoft.Azure.Commands.ServiceFabric.Models.DurabilityLevel</span></span>
<span data-ttu-id="b5ee0-135">Parameter: DurabilityLevel (ByValue)</span><span class="sxs-lookup"><span data-stu-id="b5ee0-135">Parameters: DurabilityLevel (ByValue)</span></span>

## <span data-ttu-id="b5ee0-136">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="b5ee0-136">OUTPUTS</span></span>

### <span data-ttu-id="b5ee0-137">Microsoft. Azure. Commands. ServiceFabric. Models. PSCluster</span><span class="sxs-lookup"><span data-stu-id="b5ee0-137">Microsoft.Azure.Commands.ServiceFabric.Models.PSCluster</span></span>

## <span data-ttu-id="b5ee0-138">Notizen</span><span class="sxs-lookup"><span data-stu-id="b5ee0-138">NOTES</span></span>

## <span data-ttu-id="b5ee0-139">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="b5ee0-139">RELATED LINKS</span></span>
