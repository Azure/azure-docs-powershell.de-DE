---
external help file: Microsoft.Azure.Commands.EventHub.dll-Help.xml
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/New-AzureRmEventHubNamespace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/New-AzureRmEventHubNamespace.md
gitcommit: https://github.com/Azure/azure-powershell/blob/28baa4a53a4efceb1197c032a8db08e199f0858d
ms.openlocfilehash: 07b5de12e042c81bb5f27c844d1fc8962453310a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93665060"
---
# <span data-ttu-id="306c7-101">New-AzureRmEventHubNamespace</span><span class="sxs-lookup"><span data-stu-id="306c7-101">New-AzureRmEventHubNamespace</span></span>

## <span data-ttu-id="306c7-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="306c7-102">SYNOPSIS</span></span>
<span data-ttu-id="306c7-103">Erstellt einen Event Hubs-Namespace.</span><span class="sxs-lookup"><span data-stu-id="306c7-103">Creates an Event Hubs namespace.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="306c7-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="306c7-104">SYNTAX</span></span>

### <span data-ttu-id="306c7-105">NamespaceParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="306c7-105">NamespaceParameterSet (Default)</span></span>
```
New-AzureRmEventHubNamespace [-ResourceGroupName] <String> [-Name] <String> [-Location] <String>
 [[-SkuName] <String>] [[-SkuCapacity] <Int32>] [[-Tag] <Hashtable>] [-EnableAutoInflate]
 [[-MaximumThroughputUnits] <Int32>] [-WhatIf] [-Confirm]
```

### <span data-ttu-id="306c7-106">AutoInflateParameterSet</span><span class="sxs-lookup"><span data-stu-id="306c7-106">AutoInflateParameterSet</span></span>
```
New-AzureRmEventHubNamespace [-ResourceGroupName] <String> [-EnableAutoInflate]
 [-MaximumThroughputUnits] <Int32> [-WhatIf] [-Confirm]
```

## <span data-ttu-id="306c7-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="306c7-107">DESCRIPTION</span></span>
<span data-ttu-id="306c7-108">Das New-AzureRmEventHubNamespace-Cmdlet erstellt einen neuen Namespace vom Typ Event Hubs.</span><span class="sxs-lookup"><span data-stu-id="306c7-108">The New-AzureRmEventHubNamespace cmdlet creates a new namespace of type Event Hubs.</span></span>

## <span data-ttu-id="306c7-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="306c7-109">EXAMPLES</span></span>

### <span data-ttu-id="306c7-110">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="306c7-110">Example 1</span></span>
```
PS C:\> New-AzureRmEventHubNamespace -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName -Location MyLocation 
```

<span data-ttu-id="306c7-111">Erstellt einen Event Hubs \` -Namespace mynamespacename am \` angegebenen geografischen Standort \` mylocation \` in der Ressourcengruppe \` MyResourceGroupName \` .</span><span class="sxs-lookup"><span data-stu-id="306c7-111">Creates an Event Hubs namespace \`MyNamespaceName\` in the specified geographic location \`MyLocation\`, in resource group \`MyResourceGroupName\`.</span></span>

### <span data-ttu-id="306c7-112">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="306c7-112">Example 2</span></span>
```
PS C:\> New-AzureRmEventHubNamespace -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName -Location MyLocation -EnableAutoInflate -MaximumThroughputUnits 10
```

<span data-ttu-id="306c7-113">Erstellt einen Event Hubs-Namespace \` mynamespacename am \` angegebenen geografischen Standort \` mylocation \` , in der Ressourcengruppe \` MyResourceGroupName \` und autopump ist mit MaximumThroughputUnits 10 aktiviert.</span><span class="sxs-lookup"><span data-stu-id="306c7-113">Creates an Event Hubs namespace \`MyNamespaceName\` in the specified geographic location \`MyLocation\`, in resource group \`MyResourceGroupName\` and AutoInflate is enabled with MaximumThroughputUnits 10.</span></span>

## <span data-ttu-id="306c7-114">Parameter</span><span class="sxs-lookup"><span data-stu-id="306c7-114">PARAMETERS</span></span>

### <span data-ttu-id="306c7-115">-Standort</span><span class="sxs-lookup"><span data-stu-id="306c7-115">-Location</span></span>
<span data-ttu-id="306c7-116">Event Hubs-Namespace Geo-Standort.</span><span class="sxs-lookup"><span data-stu-id="306c7-116">Event Hubs namespace geo-location.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="306c7-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="306c7-117">-ResourceGroupName</span></span>
<span data-ttu-id="306c7-118">Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="306c7-118">Resource group name.</span></span>

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

### <span data-ttu-id="306c7-119">-SkuCapacity</span><span class="sxs-lookup"><span data-stu-id="306c7-119">-SkuCapacity</span></span>
<span data-ttu-id="306c7-120">Die Ereignis-Hub-Durchsatz Einheiten.</span><span class="sxs-lookup"><span data-stu-id="306c7-120">The Event Hub throughput units.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="306c7-121">-SkuName</span><span class="sxs-lookup"><span data-stu-id="306c7-121">-SkuName</span></span>
<span data-ttu-id="306c7-122">Namespace-SKU-Name.</span><span class="sxs-lookup"><span data-stu-id="306c7-122">Namespace Sku name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: Basic, Standard, Premium

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="306c7-123">-Tag</span><span class="sxs-lookup"><span data-stu-id="306c7-123">-Tag</span></span>
<span data-ttu-id="306c7-124">Hashtables, die Ressourcenkategorien darstellen.</span><span class="sxs-lookup"><span data-stu-id="306c7-124">Hashtables that represent resource tags.</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="306c7-125">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="306c7-125">-Confirm</span></span>
<span data-ttu-id="306c7-126">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="306c7-126">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="306c7-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="306c7-127">-WhatIf</span></span>
<span data-ttu-id="306c7-128">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="306c7-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="306c7-129">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="306c7-129">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="306c7-130">-EnableAutoInflate</span><span class="sxs-lookup"><span data-stu-id="306c7-130">-EnableAutoInflate</span></span>
<span data-ttu-id="306c7-131">Gibt an, ob autopump aktiviert ist</span><span class="sxs-lookup"><span data-stu-id="306c7-131">Indicates whether AutoInflate is enabled</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: NamespaceParameterSet
Aliases: 

Required: False
Position: 6
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="306c7-132">-MaximumThroughputUnits</span><span class="sxs-lookup"><span data-stu-id="306c7-132">-MaximumThroughputUnits</span></span>
<span data-ttu-id="306c7-133">Obergrenze von Durchsatz Einheiten wenn autopump aktiviert ist, sollte sich Vaule innerhalb von 0 bis 20 Durchsatz Einheiten befinden.</span><span class="sxs-lookup"><span data-stu-id="306c7-133">Upper limit of throughput units when AutoInflate is enabled, vaule should be within 0 to 20 throughput units.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="306c7-134">-Name</span><span class="sxs-lookup"><span data-stu-id="306c7-134">-Name</span></span>
<span data-ttu-id="306c7-135">Name des EventHub-Namespaces.</span><span class="sxs-lookup"><span data-stu-id="306c7-135">EventHub Namespace Name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: NamespaceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

## <span data-ttu-id="306c7-136">Eingaben</span><span class="sxs-lookup"><span data-stu-id="306c7-136">INPUTS</span></span>

### <span data-ttu-id="306c7-137">System. String</span><span class="sxs-lookup"><span data-stu-id="306c7-137">System.String</span></span>
<span data-ttu-id="306c7-138">System. Nullable \` 1 \[ \[ System. Int32, mscorlib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = b77a5c561934e089 \] \] System. Nullable \` 1 \[ \[ System. Boolean, mscorlib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = b77a5c561934e089 \] \] System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="306c7-138">System.Nullable\`1\[\[System.Int32, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089\]\] System.Nullable\`1\[\[System.Boolean, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089\]\] System.Collections.Hashtable</span></span>

## <span data-ttu-id="306c7-139">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="306c7-139">OUTPUTS</span></span>

### <span data-ttu-id="306c7-140">Microsoft. Azure. Commands. EventHub. Models. NamespaceAttributes</span><span class="sxs-lookup"><span data-stu-id="306c7-140">Microsoft.Azure.Commands.EventHub.Models.NamespaceAttributes</span></span>

## <span data-ttu-id="306c7-141">Notizen</span><span class="sxs-lookup"><span data-stu-id="306c7-141">NOTES</span></span>

## <span data-ttu-id="306c7-142">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="306c7-142">RELATED LINKS</span></span>

