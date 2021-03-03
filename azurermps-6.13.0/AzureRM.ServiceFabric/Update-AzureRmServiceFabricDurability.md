---
external help file: Microsoft.Azure.Commands.ServiceFabric.dll-Help.xml
Module Name: AzureRM.ServiceFabric
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.servicefabric/update-azurermservicefabricdurability
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceFabric/Commands.ServiceFabric/help/Update-AzureRmServiceFabricDurability.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceFabric/Commands.ServiceFabric/help/Update-AzureRmServiceFabricDurability.md
ms.openlocfilehash: 7bc55521f04cf4d6e2bff18a01bfbdf4d76410f2
ms.sourcegitcommit: 608289d079b819df2b8d1a2f7935cc500367a312
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/03/2021
ms.locfileid: "101684998"
---
# <span data-ttu-id="ee0f7-101">Update-AzureRmServiceFabricDurability</span><span class="sxs-lookup"><span data-stu-id="ee0f7-101">Update-AzureRmServiceFabricDurability</span></span>

## <span data-ttu-id="ee0f7-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ee0f7-102">SYNOPSIS</span></span>
<span data-ttu-id="ee0f7-103">Aktualisieren Sie die Lebensdauerebene oder vmSku eines Knotentyps im Cluster.</span><span class="sxs-lookup"><span data-stu-id="ee0f7-103">Update the durability tier or VmSku of a node type in the cluster.</span></span> <span data-ttu-id="ee0f7-104">Außerdem wird die Dauerhaftigkeitsebene in der Service Fabric-VM-Erweiterung im zugeordneten Skalierungssatz für virtuelle Computer aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="ee0f7-104">It will also update the durability tier in the Service Fabric VM extension on the associated Virtual Machine Scale Set.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ee0f7-105">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="ee0f7-105">SYNTAX</span></span>

```
Update-AzureRmServiceFabricDurability [-ResourceGroupName] <String> [-Name] <String> -NodeType <String>
 -DurabilityLevel <DurabilityLevel> [-Sku <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ee0f7-106">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="ee0f7-106">DESCRIPTION</span></span>
<span data-ttu-id="ee0f7-107">Verwenden **Sie Update-AzureRmServiceFabricDurability,** um die Dauerhaftigkeit oder SKU des Clusters zu aktualisieren.</span><span class="sxs-lookup"><span data-stu-id="ee0f7-107">Use **Update-AzureRmServiceFabricDurability** to update durability or SKU of the cluster.</span></span>

## <span data-ttu-id="ee0f7-108">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="ee0f7-108">EXAMPLES</span></span>

### <span data-ttu-id="ee0f7-109">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="ee0f7-109">Example 1</span></span>
```
PS c:> Update-AzureRmServiceFabricDurability -ResourceGroupName 'Group1' -Name 'Contoso01SFCluster' -DurabilityLevel Silver -NodeType nt1
```

<span data-ttu-id="ee0f7-110">Mit diesem Befehl wird die Dauerhaftigkeitsebene des NodeType 'nt1' in Silver geändert.</span><span class="sxs-lookup"><span data-stu-id="ee0f7-110">This command changes durability tier of the NodeType 'nt1' to silver.</span></span>

## <span data-ttu-id="ee0f7-111">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="ee0f7-111">PARAMETERS</span></span>

### <span data-ttu-id="ee0f7-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ee0f7-112">-DefaultProfile</span></span>
<span data-ttu-id="ee0f7-113">Die Anmeldeinformationen, das Konto, der Mandant und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="ee0f7-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ee0f7-114">-DurabilityLevel</span><span class="sxs-lookup"><span data-stu-id="ee0f7-114">-DurabilityLevel</span></span>
<span data-ttu-id="ee0f7-115">Geben Sie den Dauerhaftigkeitsgrad an.</span><span class="sxs-lookup"><span data-stu-id="ee0f7-115">Specify durability level.</span></span>

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

### <span data-ttu-id="ee0f7-116">-Name</span><span class="sxs-lookup"><span data-stu-id="ee0f7-116">-Name</span></span>
<span data-ttu-id="ee0f7-117">Geben Sie den Namen des Clusters an.</span><span class="sxs-lookup"><span data-stu-id="ee0f7-117">Specify the name of the cluster.</span></span>

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

### <span data-ttu-id="ee0f7-118">-NodeType</span><span class="sxs-lookup"><span data-stu-id="ee0f7-118">-NodeType</span></span>
<span data-ttu-id="ee0f7-119">Geben Sie den Namen des Knotentyps "Service Fabric" an.</span><span class="sxs-lookup"><span data-stu-id="ee0f7-119">Specify Service Fabric node type name.</span></span>

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

### <span data-ttu-id="ee0f7-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ee0f7-120">-ResourceGroupName</span></span>
<span data-ttu-id="ee0f7-121">Gibt den Namen der Ressourcengruppe an.</span><span class="sxs-lookup"><span data-stu-id="ee0f7-121">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="ee0f7-122">-Sku</span><span class="sxs-lookup"><span data-stu-id="ee0f7-122">-Sku</span></span>
<span data-ttu-id="ee0f7-123">Geben Sie die SKU des Knotentyps an.</span><span class="sxs-lookup"><span data-stu-id="ee0f7-123">Specify the SKU of the node type.</span></span>

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

### <span data-ttu-id="ee0f7-124">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="ee0f7-124">-Confirm</span></span>
<span data-ttu-id="ee0f7-125">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="ee0f7-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ee0f7-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ee0f7-126">-WhatIf</span></span>
<span data-ttu-id="ee0f7-127">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="ee0f7-127">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="ee0f7-128">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="ee0f7-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ee0f7-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ee0f7-129">CommonParameters</span></span>
<span data-ttu-id="ee0f7-130">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ee0f7-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ee0f7-131">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ee0f7-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ee0f7-132">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="ee0f7-132">INPUTS</span></span>

### <span data-ttu-id="ee0f7-133">System.String</span><span class="sxs-lookup"><span data-stu-id="ee0f7-133">System.String</span></span>
<span data-ttu-id="ee0f7-134">Parameter: NodeType (ByValue), Sku (ByValue)</span><span class="sxs-lookup"><span data-stu-id="ee0f7-134">Parameters: NodeType (ByValue), Sku (ByValue)</span></span>

### <span data-ttu-id="ee0f7-135">Microsoft.Azure.Commands.ServiceFabric.Models.DurabilityLevel</span><span class="sxs-lookup"><span data-stu-id="ee0f7-135">Microsoft.Azure.Commands.ServiceFabric.Models.DurabilityLevel</span></span>
<span data-ttu-id="ee0f7-136">Parameter: DurabilityLevel (ByValue)</span><span class="sxs-lookup"><span data-stu-id="ee0f7-136">Parameters: DurabilityLevel (ByValue)</span></span>

## <span data-ttu-id="ee0f7-137">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="ee0f7-137">OUTPUTS</span></span>

### <span data-ttu-id="ee0f7-138">Microsoft.Azure.Commands.ServiceFabric.Models.PSCluster</span><span class="sxs-lookup"><span data-stu-id="ee0f7-138">Microsoft.Azure.Commands.ServiceFabric.Models.PSCluster</span></span>

## <span data-ttu-id="ee0f7-139">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="ee0f7-139">NOTES</span></span>

## <span data-ttu-id="ee0f7-140">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="ee0f7-140">RELATED LINKS</span></span>
