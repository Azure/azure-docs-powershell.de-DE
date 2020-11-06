---
external help file: Microsoft.Azure.Commands.EventHub.dll-Help.xml
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/Set-AzureRmEventHubNamespace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/Set-AzureRmEventHubNamespace.md
gitcommit: https://github.com/Azure/azure-powershell/blob/6911f050bfba3248a3fd992fbc2645e3a1a8641d
ms.openlocfilehash: 05f0c3cd3947a1955689a7359b40d59052863ce1
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93479234"
---
# <span data-ttu-id="ad8ad-101">Set-AzureRmEventHubNamespace</span><span class="sxs-lookup"><span data-stu-id="ad8ad-101">Set-AzureRmEventHubNamespace</span></span>

## <span data-ttu-id="ad8ad-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="ad8ad-102">SYNOPSIS</span></span>
<span data-ttu-id="ad8ad-103">Aktualisiert den angegebenen Event Hubs-Namespace.</span><span class="sxs-lookup"><span data-stu-id="ad8ad-103">Updates the specified Event Hubs namespace.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ad8ad-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="ad8ad-104">SYNTAX</span></span>

### <span data-ttu-id="ad8ad-105">NamespaceParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="ad8ad-105">NamespaceParameterSet (Default)</span></span>
```
Set-AzureRmEventHubNamespace [-ResourceGroupName] <String> [-Name] <String> [-Location] <String>
 [[-SkuName] <String>] [[-SkuCapacity] <Int32>] [[-State] <NamespaceState>] [[-Tag] <Hashtable>]
 [-EnableAutoInflate] [[-MaximumThroughputUnits] <Int32>] [-WhatIf] [-Confirm]
```

### <span data-ttu-id="ad8ad-106">AutoInflateParameterSet</span><span class="sxs-lookup"><span data-stu-id="ad8ad-106">AutoInflateParameterSet</span></span>
```
Set-AzureRmEventHubNamespace [-ResourceGroupName] <String> [-Name] <String> [-Location] <String>
 [[-SkuName] <String>] [[-SkuCapacity] <Int32>] [[-State] <NamespaceState>] [[-Tag] <Hashtable>]
 [-EnableAutoInflate] [[-MaximumThroughputUnits] <Int32>] [-WhatIf] [-Confirm]
```

## <span data-ttu-id="ad8ad-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="ad8ad-107">DESCRIPTION</span></span>
<span data-ttu-id="ad8ad-108">Das Set-AzureRmEventHubNamespace-Cmdlet aktualisiert die Eigenschaften des angegebenen Event Hubs-Namespace.</span><span class="sxs-lookup"><span data-stu-id="ad8ad-108">The Set-AzureRmEventHubNamespace cmdlet updates the properties of the specified Event Hubs namespace.</span></span>

## <span data-ttu-id="ad8ad-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="ad8ad-109">EXAMPLES</span></span>

### <span data-ttu-id="ad8ad-110">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="ad8ad-110">Example 1</span></span>
```
PS C:\> Set-AzureRmEventHubNamespace -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName -Location "WestUS" -State Created
```

<span data-ttu-id="ad8ad-111">Aktualisiert den Zustand des Namespaces \` mynamespacename \` auf created.</span><span class="sxs-lookup"><span data-stu-id="ad8ad-111">Updates the state of namespace \`MyNamespaceName\` to Created .</span></span>

### <span data-ttu-id="ad8ad-112">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="ad8ad-112">Example 2</span></span>
```
PS C:\> Set-AzureRmEventHubNamespace -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName -Location "WestUS" -State Created -EnableAutoInflate -MaximumThroughputUnits 10
```

<span data-ttu-id="ad8ad-113">Aktualisiert den Zustand des Namespace \` mynamespacename \` mit autopump = Enabled und MaximumThroughputUnits = 10.</span><span class="sxs-lookup"><span data-stu-id="ad8ad-113">Updates the state of namespace \`MyNamespaceName\` with AutoInflate = enabled and MaximumThroughputUnits = 10</span></span>

## <span data-ttu-id="ad8ad-114">Parameter</span><span class="sxs-lookup"><span data-stu-id="ad8ad-114">PARAMETERS</span></span>

### <span data-ttu-id="ad8ad-115">-Standort</span><span class="sxs-lookup"><span data-stu-id="ad8ad-115">-Location</span></span>
<span data-ttu-id="ad8ad-116">Event Hubs-Namespace Geo-Standort.</span><span class="sxs-lookup"><span data-stu-id="ad8ad-116">Event Hubs namespace geo-location.</span></span>

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

### <span data-ttu-id="ad8ad-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ad8ad-117">-ResourceGroupName</span></span>
<span data-ttu-id="ad8ad-118">Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="ad8ad-118">Resource group name.</span></span>

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

### <span data-ttu-id="ad8ad-119">-SkuCapacity</span><span class="sxs-lookup"><span data-stu-id="ad8ad-119">-SkuCapacity</span></span>
<span data-ttu-id="ad8ad-120">Die Ereignis-Hub-Durchsatz Einheiten.</span><span class="sxs-lookup"><span data-stu-id="ad8ad-120">The Event Hub throughput units.</span></span>

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

### <span data-ttu-id="ad8ad-121">-SkuName</span><span class="sxs-lookup"><span data-stu-id="ad8ad-121">-SkuName</span></span>
<span data-ttu-id="ad8ad-122">Namespace-SKU-Name.</span><span class="sxs-lookup"><span data-stu-id="ad8ad-122">Namespace Sku name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: Basic, Standard, Premium

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ad8ad-123">-Bundesland</span><span class="sxs-lookup"><span data-stu-id="ad8ad-123">-State</span></span>
<span data-ttu-id="ad8ad-124">Gibt den Zustand (deaktiviert oder aktiviert) des Namespaces an.</span><span class="sxs-lookup"><span data-stu-id="ad8ad-124">Specifies the state (disabled or enabled) of the namespace.</span></span>

```yaml
Type: NamespaceState
Parameter Sets: (All)
Aliases: 
Accepted values: Unknown, Creating, Created, Activating, Enabling, Active, Disabling, Disabled, SoftDeleting, SoftDeleted, Removing, Removed, Failed

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ad8ad-125">-Tag</span><span class="sxs-lookup"><span data-stu-id="ad8ad-125">-Tag</span></span>
<span data-ttu-id="ad8ad-126">Hashtables, die Ressourcenkategorien darstellen.</span><span class="sxs-lookup"><span data-stu-id="ad8ad-126">Hashtables that represent resource tags.</span></span>

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

### <span data-ttu-id="ad8ad-127">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="ad8ad-127">-Confirm</span></span>
<span data-ttu-id="ad8ad-128">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="ad8ad-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ad8ad-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ad8ad-129">-WhatIf</span></span>
<span data-ttu-id="ad8ad-130">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="ad8ad-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ad8ad-131">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="ad8ad-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ad8ad-132">-EnableAutoInflate</span><span class="sxs-lookup"><span data-stu-id="ad8ad-132">-EnableAutoInflate</span></span>
<span data-ttu-id="ad8ad-133">Gibt an, ob autopump aktiviert ist</span><span class="sxs-lookup"><span data-stu-id="ad8ad-133">Indicates whether AutoInflate is enabled</span></span>

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

### <span data-ttu-id="ad8ad-134">-MaximumThroughputUnits</span><span class="sxs-lookup"><span data-stu-id="ad8ad-134">-MaximumThroughputUnits</span></span>
<span data-ttu-id="ad8ad-135">Obergrenze von Durchsatz Einheiten wenn autopump aktiviert ist, sollte sich Vaule innerhalb von 0 bis 20 Durchsatz Einheiten befinden.</span><span class="sxs-lookup"><span data-stu-id="ad8ad-135">Upper limit of throughput units when AutoInflate is enabled, vaule should be within 0 to 20 throughput units.</span></span>

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

### <span data-ttu-id="ad8ad-136">-Name</span><span class="sxs-lookup"><span data-stu-id="ad8ad-136">-Name</span></span>
<span data-ttu-id="ad8ad-137">Name des EventHub-Namespaces.</span><span class="sxs-lookup"><span data-stu-id="ad8ad-137">EventHub Namespace Name.</span></span>

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

## <span data-ttu-id="ad8ad-138">Eingaben</span><span class="sxs-lookup"><span data-stu-id="ad8ad-138">INPUTS</span></span>

### <span data-ttu-id="ad8ad-139">System. String</span><span class="sxs-lookup"><span data-stu-id="ad8ad-139">System.String</span></span>

### <span data-ttu-id="ad8ad-140">System. Int32</span><span class="sxs-lookup"><span data-stu-id="ad8ad-140">System.Int32</span></span>

### <span data-ttu-id="ad8ad-141">Microsoft. Azure. Management. EventHub. Models. NamespaceState</span><span class="sxs-lookup"><span data-stu-id="ad8ad-141">Microsoft.Azure.Management.EventHub.Models.NamespaceState</span></span>

### <span data-ttu-id="ad8ad-142">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="ad8ad-142">System.Collections.Hashtable</span></span>

## <span data-ttu-id="ad8ad-143">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="ad8ad-143">OUTPUTS</span></span>

### <span data-ttu-id="ad8ad-144">Microsoft. Azure. Commands. EventHub. Models. NamespaceAttributes</span><span class="sxs-lookup"><span data-stu-id="ad8ad-144">Microsoft.Azure.Commands.EventHub.Models.NamespaceAttributes</span></span>

## <span data-ttu-id="ad8ad-145">Notizen</span><span class="sxs-lookup"><span data-stu-id="ad8ad-145">NOTES</span></span>

## <span data-ttu-id="ad8ad-146">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="ad8ad-146">RELATED LINKS</span></span>

