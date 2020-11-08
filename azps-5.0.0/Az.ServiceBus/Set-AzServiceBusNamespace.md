---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceBus.dll-Help.xml
Module Name: Az.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicebus/set-azservicebusnamespace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Set-AzServiceBusNamespace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Set-AzServiceBusNamespace.md
ms.openlocfilehash: e9f228b284b690681b2a4d55eb436e4062d7c861
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94176919"
---
# <span data-ttu-id="f5360-101">Set-AzServiceBusNamespace</span><span class="sxs-lookup"><span data-stu-id="f5360-101">Set-AzServiceBusNamespace</span></span>

## <span data-ttu-id="f5360-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="f5360-102">SYNOPSIS</span></span>
<span data-ttu-id="f5360-103">Aktualisiert die Beschreibung eines vorhandenen Service Bus-Namespaces.</span><span class="sxs-lookup"><span data-stu-id="f5360-103">Updates the description of an existing Service Bus namespace.</span></span>

## <span data-ttu-id="f5360-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="f5360-104">SYNTAX</span></span>

```
Set-AzServiceBusNamespace [-ResourceGroupName] <String> [-Location] <String> [-Name] <String>
 [-SkuName <String>] [-SkuCapacity <Int32>] [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f5360-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="f5360-105">DESCRIPTION</span></span>
<span data-ttu-id="f5360-106">Das Cmdlet " **Satz-AzServiceBusNamespace** " aktualisiert die Beschreibung des angegebenen ServiceBus-Namespaces innerhalb der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="f5360-106">The **Set-AzServiceBusNamespace** cmdlet updates the description of the specified Service Bus namespace within the resource group.</span></span>

## <span data-ttu-id="f5360-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="f5360-107">EXAMPLES</span></span>

### <span data-ttu-id="f5360-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="f5360-108">Example 1</span></span>
```
PS C:\> Set-AzServiceBusNamespace -ResourceGroup Default-ServiceBus-WestUS -NamespaceName SB-Example1 -Location WestUs -SkuName Premium -SkuCapacity 1 -Tag @{Tag2="Tag2Value"}

Name               : SB-Example1
Id                 : /subscriptions/{subscription id}/resourceGroups/Default-ServiceBus-WestUS/providers/Microsoft.ServiceBus/namespaces/SB-Example1
ResourceGroupName  : Default-ServiceBus-WestUS
Location           : West US
Tags               : {Tag2, Tag2Value}
Sku                : Name : Premium , Tier : Premium, Capacity : 1
ProvisioningState  : Succeeded
CreatedAt          :
UpdatedAt          :
ServiceBusEndpoint :
```

<span data-ttu-id="f5360-109">Aktualisiert den ServiceBus-Namespace mit einer neuen Beschreibung.</span><span class="sxs-lookup"><span data-stu-id="f5360-109">Updates the Service Bus namespace with a new description.</span></span>

## <span data-ttu-id="f5360-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="f5360-110">PARAMETERS</span></span>

### <span data-ttu-id="f5360-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f5360-111">-DefaultProfile</span></span>
<span data-ttu-id="f5360-112">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="f5360-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f5360-113">-Standort</span><span class="sxs-lookup"><span data-stu-id="f5360-113">-Location</span></span>
<span data-ttu-id="f5360-114">Der Speicherort des ServiceBus-Namespaces.</span><span class="sxs-lookup"><span data-stu-id="f5360-114">The Service Bus namespace location.</span></span>

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

### <span data-ttu-id="f5360-115">-Name</span><span class="sxs-lookup"><span data-stu-id="f5360-115">-Name</span></span>
<span data-ttu-id="f5360-116">Name des ServiceBus-Namespaces.</span><span class="sxs-lookup"><span data-stu-id="f5360-116">ServiceBus Namespace Name.</span></span>

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

### <span data-ttu-id="f5360-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f5360-117">-ResourceGroupName</span></span>
<span data-ttu-id="f5360-118">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="f5360-118">The resource group name.</span></span>

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

### <span data-ttu-id="f5360-119">-SkuCapacity</span><span class="sxs-lookup"><span data-stu-id="f5360-119">-SkuCapacity</span></span>
<span data-ttu-id="f5360-120">SKU-Kapazität des Namespaces.</span><span class="sxs-lookup"><span data-stu-id="f5360-120">Namespace Sku Capacity.</span></span>

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

### <span data-ttu-id="f5360-121">-SkuName</span><span class="sxs-lookup"><span data-stu-id="f5360-121">-SkuName</span></span>
<span data-ttu-id="f5360-122">Der Namespace-SKU-Name.</span><span class="sxs-lookup"><span data-stu-id="f5360-122">The namespace SKU name.</span></span>

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

### <span data-ttu-id="f5360-123">-Tag</span><span class="sxs-lookup"><span data-stu-id="f5360-123">-Tag</span></span>
<span data-ttu-id="f5360-124">Schlüssel-Wert-Paare in Form einer Hashtabelle</span><span class="sxs-lookup"><span data-stu-id="f5360-124">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="f5360-125">Beispiel: @ {Key0 = "value0"; key1 = $NULL; key2 = "Value2"}</span><span class="sxs-lookup"><span data-stu-id="f5360-125">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="f5360-126">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="f5360-126">-Confirm</span></span>
<span data-ttu-id="f5360-127">Aktualisiert den ServiceBus-Namespace mit den angegebenen Informationen.</span><span class="sxs-lookup"><span data-stu-id="f5360-127">Updates the Service Bus namespace with the specified information.</span></span>

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

### <span data-ttu-id="f5360-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f5360-128">-WhatIf</span></span>
<span data-ttu-id="f5360-129">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="f5360-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f5360-130">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="f5360-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f5360-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f5360-131">CommonParameters</span></span>
<span data-ttu-id="f5360-132">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f5360-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f5360-133">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f5360-133">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f5360-134">Eingaben</span><span class="sxs-lookup"><span data-stu-id="f5360-134">INPUTS</span></span>

### <span data-ttu-id="f5360-135">System. String</span><span class="sxs-lookup"><span data-stu-id="f5360-135">System.String</span></span>

### <span data-ttu-id="f5360-136">System. Nullable ' 1 [[System. Int32, System. private. CoreLib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="f5360-136">System.Nullable\`1[[System.Int32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="f5360-137">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="f5360-137">System.Collections.Hashtable</span></span>

## <span data-ttu-id="f5360-138">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="f5360-138">OUTPUTS</span></span>

### <span data-ttu-id="f5360-139">Microsoft. Azure. Commands. ServiceBus. Models. PSNamespaceAttributes</span><span class="sxs-lookup"><span data-stu-id="f5360-139">Microsoft.Azure.Commands.ServiceBus.Models.PSNamespaceAttributes</span></span>

## <span data-ttu-id="f5360-140">Notizen</span><span class="sxs-lookup"><span data-stu-id="f5360-140">NOTES</span></span>

## <span data-ttu-id="f5360-141">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="f5360-141">RELATED LINKS</span></span>
