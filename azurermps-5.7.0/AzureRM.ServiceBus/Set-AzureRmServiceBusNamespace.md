---
external help file: Microsoft.Azure.Commands.ServiceBus.dll-Help.xml
Module Name: AzureRM.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.servicebus/set-azurermservicebusnamespace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Set-AzureRmServiceBusNamespace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Set-AzureRmServiceBusNamespace.md
ms.openlocfilehash: f4a94823ba0ff615a68a9e17703ba7e8193b0a84
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93498797"
---
# <span data-ttu-id="fc54c-101">Set-AzureRmServiceBusNamespace</span><span class="sxs-lookup"><span data-stu-id="fc54c-101">Set-AzureRmServiceBusNamespace</span></span>

## <span data-ttu-id="fc54c-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="fc54c-102">SYNOPSIS</span></span>
<span data-ttu-id="fc54c-103">Aktualisiert die Beschreibung eines vorhandenen Service Bus-Namespaces.</span><span class="sxs-lookup"><span data-stu-id="fc54c-103">Updates the description of an existing Service Bus namespace.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="fc54c-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="fc54c-104">SYNTAX</span></span>

```
Set-AzureRmServiceBusNamespace [-ResourceGroupName] <String> [-Location] <String> [-Name] <String>
 [-SkuName <String>] [-SkuCapacity <Int32>] [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="fc54c-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="fc54c-105">DESCRIPTION</span></span>
<span data-ttu-id="fc54c-106">Das Cmdlet " **Satz-AzureRmServiceBusNamespace** " aktualisiert die Beschreibung des angegebenen ServiceBus-Namespaces innerhalb der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="fc54c-106">The **Set-AzureRmServiceBusNamespace** cmdlet updates the description of the specified Service Bus namespace within the resource group.</span></span>

## <span data-ttu-id="fc54c-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="fc54c-107">EXAMPLES</span></span>

### <span data-ttu-id="fc54c-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="fc54c-108">Example 1</span></span>
```
PS C:\> Set-AzureRmServiceBusNamespace -ResourceGroup Default-ServiceBus-WestUS -NamespaceName SB-Example1 -Location WestUs -SkuName Premium -SkuCapacity 10 -Tag @{Tag2="Tag2Value"}

Name               : SB-Example1
Id                 : /subscriptions/{subscription id}/resourceGroups/Default-ServiceBus-WestUS/providers/Microsoft.ServiceBus/namespaces/SB-Example1
Location           : West US
Sku                : Name : Standard , Capacity : 10 , Tier : Standard
ProvisioningState  : Succeeded
CreatedAt          :
UpdatedAt          :
ServiceBusEndpoint :
```

<span data-ttu-id="fc54c-109">Aktualisiert den ServiceBus-Namespace mit einer neuen Beschreibung.</span><span class="sxs-lookup"><span data-stu-id="fc54c-109">Updates the Service Bus namespace with a new description.</span></span>

## <span data-ttu-id="fc54c-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="fc54c-110">PARAMETERS</span></span>

### <span data-ttu-id="fc54c-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fc54c-111">-DefaultProfile</span></span>
<span data-ttu-id="fc54c-112">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="fc54c-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="fc54c-113">-Standort</span><span class="sxs-lookup"><span data-stu-id="fc54c-113">-Location</span></span>
<span data-ttu-id="fc54c-114">Der Speicherort des ServiceBus-Namespaces.</span><span class="sxs-lookup"><span data-stu-id="fc54c-114">The Service Bus namespace location.</span></span>

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

### <span data-ttu-id="fc54c-115">-Name</span><span class="sxs-lookup"><span data-stu-id="fc54c-115">-Name</span></span>
<span data-ttu-id="fc54c-116">Name des ServiceBus-Namespaces.</span><span class="sxs-lookup"><span data-stu-id="fc54c-116">ServiceBus Namespace Name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: NamespaceName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fc54c-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fc54c-117">-ResourceGroupName</span></span>
<span data-ttu-id="fc54c-118">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="fc54c-118">The resource group name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ResourceGroup

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fc54c-119">-SkuCapacity</span><span class="sxs-lookup"><span data-stu-id="fc54c-119">-SkuCapacity</span></span>
<span data-ttu-id="fc54c-120">SKU-Kapazität des Namespaces.</span><span class="sxs-lookup"><span data-stu-id="fc54c-120">Namespace Sku Capacity.</span></span>

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

### <span data-ttu-id="fc54c-121">-SkuName</span><span class="sxs-lookup"><span data-stu-id="fc54c-121">-SkuName</span></span>
<span data-ttu-id="fc54c-122">Der Namespace-SKU-Name.</span><span class="sxs-lookup"><span data-stu-id="fc54c-122">The namespace SKU name.</span></span>

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

### <span data-ttu-id="fc54c-123">-Tag</span><span class="sxs-lookup"><span data-stu-id="fc54c-123">-Tag</span></span>
<span data-ttu-id="fc54c-124">Schlüssel-Wert-Paare in Form einer Hashtabelle</span><span class="sxs-lookup"><span data-stu-id="fc54c-124">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="fc54c-125">Zum Beispiel:</span><span class="sxs-lookup"><span data-stu-id="fc54c-125">For example:</span></span>

<span data-ttu-id="fc54c-126">@ {KEY0 = "value0"; key1 = $NULL; key2 = "Value2"}</span><span class="sxs-lookup"><span data-stu-id="fc54c-126">@{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="fc54c-127">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="fc54c-127">-Confirm</span></span>
<span data-ttu-id="fc54c-128">Aktualisiert den ServiceBus-Namespace mit den angegebenen Informationen.</span><span class="sxs-lookup"><span data-stu-id="fc54c-128">Updates the Service Bus namespace with the specified information.</span></span>

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

### <span data-ttu-id="fc54c-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fc54c-129">-WhatIf</span></span>
<span data-ttu-id="fc54c-130">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="fc54c-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="fc54c-131">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="fc54c-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="fc54c-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fc54c-132">CommonParameters</span></span>
<span data-ttu-id="fc54c-133">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fc54c-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fc54c-134">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fc54c-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fc54c-135">Eingaben</span><span class="sxs-lookup"><span data-stu-id="fc54c-135">INPUTS</span></span>

### <span data-ttu-id="fc54c-136">-ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="fc54c-136">-ResourceGroup</span></span>
 <span data-ttu-id="fc54c-137">System. String</span><span class="sxs-lookup"><span data-stu-id="fc54c-137">System.String</span></span>

### <span data-ttu-id="fc54c-138">-Namespacename</span><span class="sxs-lookup"><span data-stu-id="fc54c-138">-NamespaceName</span></span>
 <span data-ttu-id="fc54c-139">System. String</span><span class="sxs-lookup"><span data-stu-id="fc54c-139">System.String</span></span>

### <span data-ttu-id="fc54c-140">-Standort</span><span class="sxs-lookup"><span data-stu-id="fc54c-140">-Location</span></span>
 <span data-ttu-id="fc54c-141">System. String</span><span class="sxs-lookup"><span data-stu-id="fc54c-141">System.String</span></span>

### <span data-ttu-id="fc54c-142">-SkuName</span><span class="sxs-lookup"><span data-stu-id="fc54c-142">-SkuName</span></span>
 <span data-ttu-id="fc54c-143">System. String</span><span class="sxs-lookup"><span data-stu-id="fc54c-143">System.String</span></span>

### <span data-ttu-id="fc54c-144">-Tag</span><span class="sxs-lookup"><span data-stu-id="fc54c-144">-Tag</span></span>
 <span data-ttu-id="fc54c-145">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="fc54c-145">System.Collections.Hashtable</span></span>

## <span data-ttu-id="fc54c-146">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="fc54c-146">OUTPUTS</span></span>

### <span data-ttu-id="fc54c-147">Microsoft. Azure. Commands. ServiceBus. Models. PSNamespaceAttributes</span><span class="sxs-lookup"><span data-stu-id="fc54c-147">Microsoft.Azure.Commands.ServiceBus.Models.PSNamespaceAttributes</span></span>

## <span data-ttu-id="fc54c-148">Notizen</span><span class="sxs-lookup"><span data-stu-id="fc54c-148">NOTES</span></span>


## <span data-ttu-id="fc54c-149">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="fc54c-149">RELATED LINKS</span></span>

