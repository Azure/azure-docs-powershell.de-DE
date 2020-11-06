---
external help file: Microsoft.Azure.Commands.ServiceBus.dll-Help.xml
Module Name: AzureRM.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.servicebus/new-azurermservicebusnamespace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/New-AzureRmServiceBusNamespace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/New-AzureRmServiceBusNamespace.md
ms.openlocfilehash: 532135578418a90e9ce6887602723c2165f28aa3
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93499402"
---
# <span data-ttu-id="4f5b6-101">New-AzureRmServiceBusNamespace</span><span class="sxs-lookup"><span data-stu-id="4f5b6-101">New-AzureRmServiceBusNamespace</span></span>

## <span data-ttu-id="4f5b6-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="4f5b6-102">SYNOPSIS</span></span>
<span data-ttu-id="4f5b6-103">Erstellt einen neuen ServiceBus-Namespace.</span><span class="sxs-lookup"><span data-stu-id="4f5b6-103">Creates a new Service Bus namespace.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="4f5b6-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="4f5b6-104">SYNTAX</span></span>

```
New-AzureRmServiceBusNamespace [-ResourceGroupName] <String> [-Location] <String> [-Name] <String>
 [-SkuName <String>] [-SkuCapacity <Int32>] [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4f5b6-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="4f5b6-105">DESCRIPTION</span></span>
<span data-ttu-id="4f5b6-106">Das Cmdlet **New-AzureRmServiceBusNamespace** erstellt einen neuen ServiceBus-Namespace.</span><span class="sxs-lookup"><span data-stu-id="4f5b6-106">The **New-AzureRmServiceBusNamespace** cmdlet creates a new Service Bus namespace.</span></span> <span data-ttu-id="4f5b6-107">Nach der Erstellung ist das Namespace-Ressourcen Manifest unveränderlich.</span><span class="sxs-lookup"><span data-stu-id="4f5b6-107">Once created, the namespace resource manifest is immutable.</span></span> <span data-ttu-id="4f5b6-108">Dieser Vorgang ist idempotent.</span><span class="sxs-lookup"><span data-stu-id="4f5b6-108">This operation is idempotent.</span></span>

## <span data-ttu-id="4f5b6-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="4f5b6-109">EXAMPLES</span></span>

### <span data-ttu-id="4f5b6-110">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="4f5b6-110">Example 1</span></span>
```
PS C:\> New-AzureRmServiceBusNamespace -ResourceGroup Default-ServiceBus-WestUS -NamespaceName SB-Example1 -Location WestUS -SkuName "Standard" -Tag @{Tag1="Tag1Value"}

Name               : SB-Example1
Id                 : /subscriptions/{SubscriptionId}/resourceGroups/Default-ServiceBus-WestUS/providers/Microsoft.ServiceBus/namespaces/SB-Example1
ResourceGroup      : Default-ServiceBus-WestUS
Location           : West US
Tags               : {TesttingTags, TestingTagValue, TestTag, TestTagValue}
Sku                : Name : Premium , Tier : Premium
ProvisioningState  : Succeeded
CreatedAt          : 1/20/2017 2:07:33 AM
UpdatedAt          : 1/20/2017 2:07:56 AM
ServiceBusEndpoint : https://SB-Example1.servicebus.windows.net:443/
```

<span data-ttu-id="4f5b6-111">Erstellt einen neuen ServiceBus-Namespace innerhalb der angegebenen Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="4f5b6-111">Creates a new Service Bus namespace within the specified resource group.</span></span>

## <span data-ttu-id="4f5b6-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="4f5b6-112">PARAMETERS</span></span>

### <span data-ttu-id="4f5b6-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4f5b6-113">-DefaultProfile</span></span>
<span data-ttu-id="4f5b6-114">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="4f5b6-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="4f5b6-115">-Standort</span><span class="sxs-lookup"><span data-stu-id="4f5b6-115">-Location</span></span>
<span data-ttu-id="4f5b6-116">Der Speicherort des ServiceBus-Namespaces.</span><span class="sxs-lookup"><span data-stu-id="4f5b6-116">The Service Bus namespace location.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4f5b6-117">-Name</span><span class="sxs-lookup"><span data-stu-id="4f5b6-117">-Name</span></span>
<span data-ttu-id="4f5b6-118">Name des ServiceBus-Namespaces.</span><span class="sxs-lookup"><span data-stu-id="4f5b6-118">ServiceBus Namespace Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: NamespaceName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4f5b6-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4f5b6-119">-ResourceGroupName</span></span>
<span data-ttu-id="4f5b6-120">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="4f5b6-120">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceGroup

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4f5b6-121">-SkuCapacity</span><span class="sxs-lookup"><span data-stu-id="4f5b6-121">-SkuCapacity</span></span>
<span data-ttu-id="4f5b6-122">Die Service Bus Premium-Namespace-Durchsatz Einheiten, zulässige Werte 1 oder 2 oder 4</span><span class="sxs-lookup"><span data-stu-id="4f5b6-122">The Service Bus premium namespace throughput units, allowed values 1 or 2 or 4</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4f5b6-123">-SkuName</span><span class="sxs-lookup"><span data-stu-id="4f5b6-123">-SkuName</span></span>
<span data-ttu-id="4f5b6-124">Der Service Bus-Namespace-SKU-Name.</span><span class="sxs-lookup"><span data-stu-id="4f5b6-124">The Service Bus namespace SKU name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Basic, Standard, Premium

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4f5b6-125">-Tag</span><span class="sxs-lookup"><span data-stu-id="4f5b6-125">-Tag</span></span>
<span data-ttu-id="4f5b6-126">Schlüssel-Wert-Paare in Form einer Hashtabelle, die als Tags auf dem Server definiert ist.</span><span class="sxs-lookup"><span data-stu-id="4f5b6-126">Key-value pairs in the form of a hash table set as tags on the server.</span></span> <span data-ttu-id="4f5b6-127">Beispiel: @ {Key0 = "value0"; key1 = $NULL; key2 = "Value2"}</span><span class="sxs-lookup"><span data-stu-id="4f5b6-127">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4f5b6-128">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="4f5b6-128">-Confirm</span></span>
<span data-ttu-id="4f5b6-129">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="4f5b6-129">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4f5b6-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4f5b6-130">-WhatIf</span></span>
<span data-ttu-id="4f5b6-131">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="4f5b6-131">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="4f5b6-132">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="4f5b6-132">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4f5b6-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4f5b6-133">CommonParameters</span></span>
<span data-ttu-id="4f5b6-134">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4f5b6-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4f5b6-135">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4f5b6-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4f5b6-136">Eingaben</span><span class="sxs-lookup"><span data-stu-id="4f5b6-136">INPUTS</span></span>

### <span data-ttu-id="4f5b6-137">System. String</span><span class="sxs-lookup"><span data-stu-id="4f5b6-137">System.String</span></span>

### <span data-ttu-id="4f5b6-138">System. Nullable ' 1 [[System. Int32, mscorlib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="4f5b6-138">System.Nullable\`1[[System.Int32, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

### <span data-ttu-id="4f5b6-139">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="4f5b6-139">System.Collections.Hashtable</span></span>

## <span data-ttu-id="4f5b6-140">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="4f5b6-140">OUTPUTS</span></span>

### <span data-ttu-id="4f5b6-141">Microsoft. Azure. Commands. ServiceBus. Models. PSNamespaceAttributes</span><span class="sxs-lookup"><span data-stu-id="4f5b6-141">Microsoft.Azure.Commands.ServiceBus.Models.PSNamespaceAttributes</span></span>

## <span data-ttu-id="4f5b6-142">Notizen</span><span class="sxs-lookup"><span data-stu-id="4f5b6-142">NOTES</span></span>

## <span data-ttu-id="4f5b6-143">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="4f5b6-143">RELATED LINKS</span></span>
