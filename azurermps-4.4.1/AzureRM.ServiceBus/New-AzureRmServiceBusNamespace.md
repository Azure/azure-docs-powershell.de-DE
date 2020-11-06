---
external help file: Microsoft.Azure.Commands.ServiceBus.dll-Help.xml
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/New-AzureRmServiceBusNamespace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/New-AzureRmServiceBusNamespace.md
ms.openlocfilehash: 79b55b62c3f4add24e52a36756f83bd16466edbd
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93503198"
---
# <span data-ttu-id="d1141-101">New-AzureRmServiceBusNamespace</span><span class="sxs-lookup"><span data-stu-id="d1141-101">New-AzureRmServiceBusNamespace</span></span>

## <span data-ttu-id="d1141-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="d1141-102">SYNOPSIS</span></span>
<span data-ttu-id="d1141-103">Erstellt einen neuen ServiceBus-Namespace.</span><span class="sxs-lookup"><span data-stu-id="d1141-103">Creates a new Service Bus namespace.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d1141-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="d1141-104">SYNTAX</span></span>

```
New-AzureRmServiceBusNamespace [-ResourceGroupName] <String> [-Location] <String> [-NamespaceName] <String>
 [-SkuName <String>] [-Tag <Hashtable>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d1141-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="d1141-105">DESCRIPTION</span></span>
<span data-ttu-id="d1141-106">Das Cmdlet **New-AzureRmServiceBusNamespace** erstellt einen neuen ServiceBus-Namespace.</span><span class="sxs-lookup"><span data-stu-id="d1141-106">The **New-AzureRmServiceBusNamespace** cmdlet creates a new Service Bus namespace.</span></span> <span data-ttu-id="d1141-107">Nach der Erstellung ist das Namespace-Ressourcen Manifest unveränderlich.</span><span class="sxs-lookup"><span data-stu-id="d1141-107">Once created, the namespace resource manifest is immutable.</span></span> <span data-ttu-id="d1141-108">Dieser Vorgang ist idempotent.</span><span class="sxs-lookup"><span data-stu-id="d1141-108">This operation is idempotent.</span></span>

## <span data-ttu-id="d1141-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="d1141-109">EXAMPLES</span></span>

### <span data-ttu-id="d1141-110">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="d1141-110">Example 1</span></span>
```
PS C:\> New-AzureRmServiceBusNamespace -ResourceGroup Default-ServiceBus-WestUS -NamespaceName SB-Example1 -Location WestUS -SkuName "Standard" -Tag @{Tag1="Tag1Value"}

Name               : SB-Example1
Id                 : /subscriptions/854d368f-1828-428f-8f3c-f2affa9b2f7d/resourceGroups/Default-ServiceBus-WestUS/providers/Microsoft.ServiceBus/namespaces/SB-Example1
Location           : West US
Sku                : Name : Standard , Capacity : 1 , Tier : Standard
ProvisioningState  : Succeeded
Status             : Active
CreatedAt          : 1/20/2017 2:07:33 AM
UpdatedAt          : 1/20/2017 2:07:56 AM
ServiceBusEndpoint : https://SB-Example1.servicebus.windows.net:443/
Enabled            : True
```

<span data-ttu-id="d1141-111">Erstellt einen neuen ServiceBus-Namespace innerhalb der angegebenen Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="d1141-111">Creates a new Service Bus namespace within the specified resource group.</span></span>

## <span data-ttu-id="d1141-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="d1141-112">PARAMETERS</span></span>

### <span data-ttu-id="d1141-113">-Standort</span><span class="sxs-lookup"><span data-stu-id="d1141-113">-Location</span></span>
<span data-ttu-id="d1141-114">Der Speicherort des ServiceBus-Namespaces.</span><span class="sxs-lookup"><span data-stu-id="d1141-114">The Service Bus namespace location.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d1141-115">-Namespacename</span><span class="sxs-lookup"><span data-stu-id="d1141-115">-NamespaceName</span></span>
<span data-ttu-id="d1141-116">Der Name des ServiceBus-Namespaces.</span><span class="sxs-lookup"><span data-stu-id="d1141-116">The Service Bus namespace name.</span></span>

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

### <span data-ttu-id="d1141-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d1141-117">-ResourceGroupName</span></span>
<span data-ttu-id="d1141-118">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="d1141-118">The resource group name.</span></span>

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

### <span data-ttu-id="d1141-119">-SkuName</span><span class="sxs-lookup"><span data-stu-id="d1141-119">-SkuName</span></span>
<span data-ttu-id="d1141-120">Der Service Bus-Namespace-SKU-Name.</span><span class="sxs-lookup"><span data-stu-id="d1141-120">The Service Bus namespace SKU name.</span></span>

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

### <span data-ttu-id="d1141-121">-Tag</span><span class="sxs-lookup"><span data-stu-id="d1141-121">-Tag</span></span>
<span data-ttu-id="d1141-122">Schlüssel-Wert-Paare in Form einer Hashtabelle, die als Tags auf dem Server definiert ist.</span><span class="sxs-lookup"><span data-stu-id="d1141-122">Key-value pairs in the form of a hash table set as tags on the server.</span></span> <span data-ttu-id="d1141-123">Zum Beispiel:</span><span class="sxs-lookup"><span data-stu-id="d1141-123">For example:</span></span>

<span data-ttu-id="d1141-124">@ {KEY0 = "value0"; key1 = $NULL; key2 = "Value2"}</span><span class="sxs-lookup"><span data-stu-id="d1141-124">@{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="d1141-125">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="d1141-125">-Confirm</span></span>
<span data-ttu-id="d1141-126">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="d1141-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d1141-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d1141-127">-WhatIf</span></span>
<span data-ttu-id="d1141-128">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="d1141-128">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="d1141-129">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="d1141-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d1141-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d1141-130">CommonParameters</span></span>
<span data-ttu-id="d1141-131">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d1141-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d1141-132">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d1141-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d1141-133">Eingaben</span><span class="sxs-lookup"><span data-stu-id="d1141-133">INPUTS</span></span>

### <span data-ttu-id="d1141-134">-ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="d1141-134">-ResourceGroup</span></span>
 <span data-ttu-id="d1141-135">System. String</span><span class="sxs-lookup"><span data-stu-id="d1141-135">System.String</span></span>

### <span data-ttu-id="d1141-136">-Namespacename</span><span class="sxs-lookup"><span data-stu-id="d1141-136">-NamespaceName</span></span>
 <span data-ttu-id="d1141-137">System. String</span><span class="sxs-lookup"><span data-stu-id="d1141-137">System.String</span></span>

### <span data-ttu-id="d1141-138">-Standort</span><span class="sxs-lookup"><span data-stu-id="d1141-138">-Location</span></span>
 <span data-ttu-id="d1141-139">System. String</span><span class="sxs-lookup"><span data-stu-id="d1141-139">System.String</span></span>

### <span data-ttu-id="d1141-140">-SkuName</span><span class="sxs-lookup"><span data-stu-id="d1141-140">-SkuName</span></span>
 <span data-ttu-id="d1141-141">System. String</span><span class="sxs-lookup"><span data-stu-id="d1141-141">System.String</span></span>

### <span data-ttu-id="d1141-142">-Tag</span><span class="sxs-lookup"><span data-stu-id="d1141-142">-Tag</span></span>
 <span data-ttu-id="d1141-143">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="d1141-143">System.Collections.Hashtable</span></span>

## <span data-ttu-id="d1141-144">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="d1141-144">OUTPUTS</span></span>

### <span data-ttu-id="d1141-145">Microsoft. Azure. Commands. ServiceBus. Models. NamespaceAttributes</span><span class="sxs-lookup"><span data-stu-id="d1141-145">Microsoft.Azure.Commands.ServiceBus.Models.NamespaceAttributes</span></span>

## <span data-ttu-id="d1141-146">Notizen</span><span class="sxs-lookup"><span data-stu-id="d1141-146">NOTES</span></span>

## <span data-ttu-id="d1141-147">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="d1141-147">RELATED LINKS</span></span>
