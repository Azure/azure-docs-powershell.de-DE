---
external help file: Microsoft.Azure.Commands.ServiceBus.dll-Help.xml
Module Name: AzureRM.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.servicebus/set-azurermservicebusnamespace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Set-AzureRmServiceBusNamespace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Set-AzureRmServiceBusNamespace.md
ms.openlocfilehash: 6ac46fc8b8f94480e11f00d44efc690d97ee56a9
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93664003"
---
# <span data-ttu-id="4d01e-101">Set-AzureRmServiceBusNamespace</span><span class="sxs-lookup"><span data-stu-id="4d01e-101">Set-AzureRmServiceBusNamespace</span></span>

## <span data-ttu-id="4d01e-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="4d01e-102">SYNOPSIS</span></span>
<span data-ttu-id="4d01e-103">Aktualisiert die Beschreibung eines vorhandenen Service Bus-Namespaces.</span><span class="sxs-lookup"><span data-stu-id="4d01e-103">Updates the description of an existing Service Bus namespace.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="4d01e-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="4d01e-104">SYNTAX</span></span>

```
Set-AzureRmServiceBusNamespace [-ResourceGroupName] <String> [-Location] <String> [-Name] <String>
 [-SkuName <String>] [-SkuCapacity <Int32>] [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4d01e-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="4d01e-105">DESCRIPTION</span></span>
<span data-ttu-id="4d01e-106">Das Cmdlet " **Satz-AzureRmServiceBusNamespace** " aktualisiert die Beschreibung des angegebenen ServiceBus-Namespaces innerhalb der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="4d01e-106">The **Set-AzureRmServiceBusNamespace** cmdlet updates the description of the specified Service Bus namespace within the resource group.</span></span>

## <span data-ttu-id="4d01e-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="4d01e-107">EXAMPLES</span></span>

### <span data-ttu-id="4d01e-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="4d01e-108">Example 1</span></span>
```
PS C:\> Set-AzureRmServiceBusNamespace -ResourceGroup Default-ServiceBus-WestUS -NamespaceName SB-Example1 -Location WestUs -SkuName Premium -SkuCapacity 1 -Tag @{Tag2="Tag2Value"}

Name               : SB-Example1
Id                 : /subscriptions/{subscription id}/resourceGroups/Default-ServiceBus-WestUS/providers/Microsoft.ServiceBus/namespaces/SB-Example1
ResourceGroup      : Default-ServiceBus-WestUS
Location           : West US
Tags               : {Tag2, Tag2Value}
Sku                : Name : Premium , Tier : Premium, Capacity : 1
ProvisioningState  : Succeeded
CreatedAt          :
UpdatedAt          :
ServiceBusEndpoint :
```

<span data-ttu-id="4d01e-109">Aktualisiert den ServiceBus-Namespace mit einer neuen Beschreibung.</span><span class="sxs-lookup"><span data-stu-id="4d01e-109">Updates the Service Bus namespace with a new description.</span></span>

## <span data-ttu-id="4d01e-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="4d01e-110">PARAMETERS</span></span>

### <span data-ttu-id="4d01e-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4d01e-111">-DefaultProfile</span></span>
<span data-ttu-id="4d01e-112">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="4d01e-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="4d01e-113">-Standort</span><span class="sxs-lookup"><span data-stu-id="4d01e-113">-Location</span></span>
<span data-ttu-id="4d01e-114">Der Speicherort des ServiceBus-Namespaces.</span><span class="sxs-lookup"><span data-stu-id="4d01e-114">The Service Bus namespace location.</span></span>

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

### <span data-ttu-id="4d01e-115">-Name</span><span class="sxs-lookup"><span data-stu-id="4d01e-115">-Name</span></span>
<span data-ttu-id="4d01e-116">Name des ServiceBus-Namespaces.</span><span class="sxs-lookup"><span data-stu-id="4d01e-116">ServiceBus Namespace Name.</span></span>

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

### <span data-ttu-id="4d01e-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4d01e-117">-ResourceGroupName</span></span>
<span data-ttu-id="4d01e-118">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="4d01e-118">The resource group name.</span></span>

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

### <span data-ttu-id="4d01e-119">-SkuCapacity</span><span class="sxs-lookup"><span data-stu-id="4d01e-119">-SkuCapacity</span></span>
<span data-ttu-id="4d01e-120">SKU-Kapazität des Namespaces.</span><span class="sxs-lookup"><span data-stu-id="4d01e-120">Namespace Sku Capacity.</span></span>

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

### <span data-ttu-id="4d01e-121">-SkuName</span><span class="sxs-lookup"><span data-stu-id="4d01e-121">-SkuName</span></span>
<span data-ttu-id="4d01e-122">Der Namespace-SKU-Name.</span><span class="sxs-lookup"><span data-stu-id="4d01e-122">The namespace SKU name.</span></span>

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

### <span data-ttu-id="4d01e-123">-Tag</span><span class="sxs-lookup"><span data-stu-id="4d01e-123">-Tag</span></span>
<span data-ttu-id="4d01e-124">Schlüssel-Wert-Paare in Form einer Hashtabelle</span><span class="sxs-lookup"><span data-stu-id="4d01e-124">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="4d01e-125">Beispiel: @ {Key0 = "value0"; key1 = $NULL; key2 = "Value2"}</span><span class="sxs-lookup"><span data-stu-id="4d01e-125">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="4d01e-126">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="4d01e-126">-Confirm</span></span>
<span data-ttu-id="4d01e-127">Aktualisiert den ServiceBus-Namespace mit den angegebenen Informationen.</span><span class="sxs-lookup"><span data-stu-id="4d01e-127">Updates the Service Bus namespace with the specified information.</span></span>

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

### <span data-ttu-id="4d01e-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4d01e-128">-WhatIf</span></span>
<span data-ttu-id="4d01e-129">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="4d01e-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4d01e-130">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="4d01e-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4d01e-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4d01e-131">CommonParameters</span></span>
<span data-ttu-id="4d01e-132">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4d01e-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4d01e-133">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4d01e-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4d01e-134">Eingaben</span><span class="sxs-lookup"><span data-stu-id="4d01e-134">INPUTS</span></span>

### <span data-ttu-id="4d01e-135">System. String</span><span class="sxs-lookup"><span data-stu-id="4d01e-135">System.String</span></span>

### <span data-ttu-id="4d01e-136">System. Nullable ' 1 [[System. Int32, mscorlib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="4d01e-136">System.Nullable\`1[[System.Int32, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

### <span data-ttu-id="4d01e-137">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="4d01e-137">System.Collections.Hashtable</span></span>

## <span data-ttu-id="4d01e-138">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="4d01e-138">OUTPUTS</span></span>

### <span data-ttu-id="4d01e-139">Microsoft. Azure. Commands. ServiceBus. Models. PSNamespaceAttributes</span><span class="sxs-lookup"><span data-stu-id="4d01e-139">Microsoft.Azure.Commands.ServiceBus.Models.PSNamespaceAttributes</span></span>

## <span data-ttu-id="4d01e-140">Notizen</span><span class="sxs-lookup"><span data-stu-id="4d01e-140">NOTES</span></span>

## <span data-ttu-id="4d01e-141">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="4d01e-141">RELATED LINKS</span></span>
