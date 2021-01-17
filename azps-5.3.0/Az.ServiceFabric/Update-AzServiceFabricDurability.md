---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceFabric.dll-Help.xml
Module Name: Az.ServiceFabric
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicefabric/update-azservicefabricdurability
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Update-AzServiceFabricDurability.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Update-AzServiceFabricDurability.md
ms.openlocfilehash: 1a406ad937a545c9b2599966909809c7552ad7db
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98471763"
---
# <span data-ttu-id="1d5f8-101">Update-AzServiceFabricDurability</span><span class="sxs-lookup"><span data-stu-id="1d5f8-101">Update-AzServiceFabricDurability</span></span>

## <span data-ttu-id="1d5f8-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1d5f8-102">SYNOPSIS</span></span>
<span data-ttu-id="1d5f8-103">Aktualisieren Sie das kontingente Tier oder vmSku eines Knotentyps im Cluster.</span><span class="sxs-lookup"><span data-stu-id="1d5f8-103">Update the durability tier or VmSku of a node type in the cluster.</span></span>

## <span data-ttu-id="1d5f8-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="1d5f8-104">SYNTAX</span></span>

```
Update-AzServiceFabricDurability [-ResourceGroupName] <String> [-Name] <String> -NodeType <String>
 -DurabilityLevel <DurabilityLevel> [-Sku <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1d5f8-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="1d5f8-105">DESCRIPTION</span></span>
<span data-ttu-id="1d5f8-106">Verwenden **Sie "Update-AzServiceFabricDurability",** um Verdingungs- oder SKU des Clusters zu aktualisieren.</span><span class="sxs-lookup"><span data-stu-id="1d5f8-106">Use **Update-AzServiceFabricDurability** to update durability or SKU of the cluster.</span></span>

## <span data-ttu-id="1d5f8-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="1d5f8-107">EXAMPLES</span></span>

### <span data-ttu-id="1d5f8-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="1d5f8-108">Example 1</span></span>
```
PS c:> Update-AzServiceFabricDurability -ResourceGroupName 'Group1' -Name 'Contoso01SFCluster' -DurabilityLevel Silver -NodeType nt1
```

<span data-ttu-id="1d5f8-109">Mit diesem Befehl wird die Gestuftstufe des NodeType 'nt1' in Silver geändert.</span><span class="sxs-lookup"><span data-stu-id="1d5f8-109">This command changes durability tier of the NodeType 'nt1' to silver.</span></span>

## <span data-ttu-id="1d5f8-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="1d5f8-110">PARAMETERS</span></span>

### <span data-ttu-id="1d5f8-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1d5f8-111">-DefaultProfile</span></span>
<span data-ttu-id="1d5f8-112">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="1d5f8-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="1d5f8-113">-DurabilityLevel</span><span class="sxs-lookup"><span data-stu-id="1d5f8-113">-DurabilityLevel</span></span>
<span data-ttu-id="1d5f8-114">Legen Sie einen Wert für die Lebensdauer fest.</span><span class="sxs-lookup"><span data-stu-id="1d5f8-114">Specify durability level.</span></span>

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

### <span data-ttu-id="1d5f8-115">-Name</span><span class="sxs-lookup"><span data-stu-id="1d5f8-115">-Name</span></span>
<span data-ttu-id="1d5f8-116">Geben Sie den Namen des Cluster an.</span><span class="sxs-lookup"><span data-stu-id="1d5f8-116">Specify the name of the cluster.</span></span>

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

### <span data-ttu-id="1d5f8-117">-NodeType</span><span class="sxs-lookup"><span data-stu-id="1d5f8-117">-NodeType</span></span>
<span data-ttu-id="1d5f8-118">Specify Service Fabric node type name.</span><span class="sxs-lookup"><span data-stu-id="1d5f8-118">Specify Service Fabric node type name.</span></span>

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

### <span data-ttu-id="1d5f8-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1d5f8-119">-ResourceGroupName</span></span>
<span data-ttu-id="1d5f8-120">Gibt den Namen der Ressourcengruppe an.</span><span class="sxs-lookup"><span data-stu-id="1d5f8-120">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="1d5f8-121">-SKU</span><span class="sxs-lookup"><span data-stu-id="1d5f8-121">-Sku</span></span>
<span data-ttu-id="1d5f8-122">Geben Sie die SKU des Knotentyps an.</span><span class="sxs-lookup"><span data-stu-id="1d5f8-122">Specify the SKU of the node type.</span></span>

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

### <span data-ttu-id="1d5f8-123">-Confirm</span><span class="sxs-lookup"><span data-stu-id="1d5f8-123">-Confirm</span></span>
<span data-ttu-id="1d5f8-124">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="1d5f8-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1d5f8-125">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="1d5f8-125">-WhatIf</span></span>
<span data-ttu-id="1d5f8-126">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="1d5f8-126">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="1d5f8-127">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="1d5f8-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1d5f8-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1d5f8-128">CommonParameters</span></span>
<span data-ttu-id="1d5f8-129">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1d5f8-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1d5f8-130">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="1d5f8-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1d5f8-131">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="1d5f8-131">INPUTS</span></span>

### <span data-ttu-id="1d5f8-132">System.String</span><span class="sxs-lookup"><span data-stu-id="1d5f8-132">System.String</span></span>

### <span data-ttu-id="1d5f8-133">Microsoft.Azure.Commands.ServiceFabric.Models.222</span><span class="sxs-lookup"><span data-stu-id="1d5f8-133">Microsoft.Azure.Commands.ServiceFabric.Models.DurabilityLevel</span></span>

## <span data-ttu-id="1d5f8-134">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="1d5f8-134">OUTPUTS</span></span>

### <span data-ttu-id="1d5f8-135">Microsoft.Azure.Commands.ServiceFabric.Models.PSCluster</span><span class="sxs-lookup"><span data-stu-id="1d5f8-135">Microsoft.Azure.Commands.ServiceFabric.Models.PSCluster</span></span>

## <span data-ttu-id="1d5f8-136">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="1d5f8-136">NOTES</span></span>

## <span data-ttu-id="1d5f8-137">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="1d5f8-137">RELATED LINKS</span></span>
