---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceFabric.dll-Help.xml
Module Name: Az.ServiceFabric
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicefabric/update-azservicefabricdurability
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Update-AzServiceFabricDurability.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Update-AzServiceFabricDurability.md
ms.openlocfilehash: 283ca228ba44d2ec87cd926d23e0217eb67434eb
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93659306"
---
# <span data-ttu-id="c4eb4-101">Update-AzServiceFabricDurability</span><span class="sxs-lookup"><span data-stu-id="c4eb4-101">Update-AzServiceFabricDurability</span></span>

## <span data-ttu-id="c4eb4-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="c4eb4-102">SYNOPSIS</span></span>
<span data-ttu-id="c4eb4-103">Aktualisieren Sie die Haltbarkeits-oder VmSku eines Knotentyps im Cluster.</span><span class="sxs-lookup"><span data-stu-id="c4eb4-103">Update the durability tier or VmSku of a node type in the cluster.</span></span>

## <span data-ttu-id="c4eb4-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="c4eb4-104">SYNTAX</span></span>

```
Update-AzServiceFabricDurability [-ResourceGroupName] <String> [-Name] <String> -NodeType <String>
 -DurabilityLevel <DurabilityLevel> [-Sku <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c4eb4-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="c4eb4-105">DESCRIPTION</span></span>
<span data-ttu-id="c4eb4-106">Verwenden Sie **Update-AzServiceFabricDurability** , um die Lebensdauer oder SKU des Clusters zu aktualisieren.</span><span class="sxs-lookup"><span data-stu-id="c4eb4-106">Use **Update-AzServiceFabricDurability** to update durability or SKU of the cluster.</span></span>

## <span data-ttu-id="c4eb4-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="c4eb4-107">EXAMPLES</span></span>

### <span data-ttu-id="c4eb4-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="c4eb4-108">Example 1</span></span>
```
PS c:> Update-AzServiceFabricDurability -ResourceGroupName 'Group1' -Name 'Contoso01SFCluster' -DurabilityLevel Silver -NodeType nt1
```

<span data-ttu-id="c4eb4-109">Mit diesem Befehl wird die Haltbarkeits Stufe des NodeType "NT1" in Silver geändert.</span><span class="sxs-lookup"><span data-stu-id="c4eb4-109">This command changes durability tier of the NodeType 'nt1' to silver.</span></span>

## <span data-ttu-id="c4eb4-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="c4eb4-110">PARAMETERS</span></span>

### <span data-ttu-id="c4eb4-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c4eb4-111">-DefaultProfile</span></span>
<span data-ttu-id="c4eb4-112">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="c4eb4-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c4eb4-113">-DurabilityLevel</span><span class="sxs-lookup"><span data-stu-id="c4eb4-113">-DurabilityLevel</span></span>
<span data-ttu-id="c4eb4-114">Geben Sie den Haltbarkeits Grad an.</span><span class="sxs-lookup"><span data-stu-id="c4eb4-114">Specify durability level.</span></span>

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

### <span data-ttu-id="c4eb4-115">-Name</span><span class="sxs-lookup"><span data-stu-id="c4eb4-115">-Name</span></span>
<span data-ttu-id="c4eb4-116">Geben Sie den Namen des Clusters an.</span><span class="sxs-lookup"><span data-stu-id="c4eb4-116">Specify the name of the cluster.</span></span>

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

### <span data-ttu-id="c4eb4-117">-NodeType</span><span class="sxs-lookup"><span data-stu-id="c4eb4-117">-NodeType</span></span>
<span data-ttu-id="c4eb4-118">Geben Sie den Namen des Service Fabric-Knotentyps an.</span><span class="sxs-lookup"><span data-stu-id="c4eb4-118">Specify Service Fabric node type name.</span></span>

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

### <span data-ttu-id="c4eb4-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c4eb4-119">-ResourceGroupName</span></span>
<span data-ttu-id="c4eb4-120">Gibt den Namen der Ressourcengruppe an.</span><span class="sxs-lookup"><span data-stu-id="c4eb4-120">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="c4eb4-121">-SKU</span><span class="sxs-lookup"><span data-stu-id="c4eb4-121">-Sku</span></span>
<span data-ttu-id="c4eb4-122">Geben Sie die SKU des Knotentyps an.</span><span class="sxs-lookup"><span data-stu-id="c4eb4-122">Specify the SKU of the node type.</span></span>

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

### <span data-ttu-id="c4eb4-123">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="c4eb4-123">-Confirm</span></span>
<span data-ttu-id="c4eb4-124">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="c4eb4-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c4eb4-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c4eb4-125">-WhatIf</span></span>
<span data-ttu-id="c4eb4-126">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="c4eb4-126">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="c4eb4-127">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="c4eb4-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c4eb4-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c4eb4-128">CommonParameters</span></span>
<span data-ttu-id="c4eb4-129">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c4eb4-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c4eb4-130">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c4eb4-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c4eb4-131">Eingaben</span><span class="sxs-lookup"><span data-stu-id="c4eb4-131">INPUTS</span></span>

### <span data-ttu-id="c4eb4-132">System. String</span><span class="sxs-lookup"><span data-stu-id="c4eb4-132">System.String</span></span>

### <span data-ttu-id="c4eb4-133">Microsoft. Azure. Commands. ServiceFabric. Models. DurabilityLevel</span><span class="sxs-lookup"><span data-stu-id="c4eb4-133">Microsoft.Azure.Commands.ServiceFabric.Models.DurabilityLevel</span></span>

## <span data-ttu-id="c4eb4-134">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="c4eb4-134">OUTPUTS</span></span>

### <span data-ttu-id="c4eb4-135">Microsoft. Azure. Commands. ServiceFabric. Models. PSCluster</span><span class="sxs-lookup"><span data-stu-id="c4eb4-135">Microsoft.Azure.Commands.ServiceFabric.Models.PSCluster</span></span>

## <span data-ttu-id="c4eb4-136">Notizen</span><span class="sxs-lookup"><span data-stu-id="c4eb4-136">NOTES</span></span>

## <span data-ttu-id="c4eb4-137">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="c4eb4-137">RELATED LINKS</span></span>
