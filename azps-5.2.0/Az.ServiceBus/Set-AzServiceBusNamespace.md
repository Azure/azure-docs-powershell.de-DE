---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceBus.dll-Help.xml
Module Name: Az.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicebus/set-azservicebusnamespace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Set-AzServiceBusNamespace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Set-AzServiceBusNamespace.md
ms.openlocfilehash: e9f228b284b690681b2a4d55eb436e4062d7c861
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98291610"
---
# <span data-ttu-id="81b58-101">Set-AzServiceBusNamespace</span><span class="sxs-lookup"><span data-stu-id="81b58-101">Set-AzServiceBusNamespace</span></span>

## <span data-ttu-id="81b58-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="81b58-102">SYNOPSIS</span></span>
<span data-ttu-id="81b58-103">Aktualisiert die Beschreibung eines vorhandenen Service Bus-Namespaces.</span><span class="sxs-lookup"><span data-stu-id="81b58-103">Updates the description of an existing Service Bus namespace.</span></span>

## <span data-ttu-id="81b58-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="81b58-104">SYNTAX</span></span>

```
Set-AzServiceBusNamespace [-ResourceGroupName] <String> [-Location] <String> [-Name] <String>
 [-SkuName <String>] [-SkuCapacity <Int32>] [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="81b58-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="81b58-105">DESCRIPTION</span></span>
<span data-ttu-id="81b58-106">Das **Cmdlet "Set-AzServiceBusNamespace"** aktualisiert die Beschreibung des angegebenen Service Bus-Namespaces innerhalb der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="81b58-106">The **Set-AzServiceBusNamespace** cmdlet updates the description of the specified Service Bus namespace within the resource group.</span></span>

## <span data-ttu-id="81b58-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="81b58-107">EXAMPLES</span></span>

### <span data-ttu-id="81b58-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="81b58-108">Example 1</span></span>
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

<span data-ttu-id="81b58-109">Aktualisiert den Namespace "Service Bus" mit einer neuen Beschreibung.</span><span class="sxs-lookup"><span data-stu-id="81b58-109">Updates the Service Bus namespace with a new description.</span></span>

## <span data-ttu-id="81b58-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="81b58-110">PARAMETERS</span></span>

### <span data-ttu-id="81b58-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="81b58-111">-DefaultProfile</span></span>
<span data-ttu-id="81b58-112">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="81b58-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="81b58-113">-Location</span><span class="sxs-lookup"><span data-stu-id="81b58-113">-Location</span></span>
<span data-ttu-id="81b58-114">Der Namespacespeicherort des Service Bus.</span><span class="sxs-lookup"><span data-stu-id="81b58-114">The Service Bus namespace location.</span></span>

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

### <span data-ttu-id="81b58-115">-Name</span><span class="sxs-lookup"><span data-stu-id="81b58-115">-Name</span></span>
<span data-ttu-id="81b58-116">ServiceBus Namespacename.</span><span class="sxs-lookup"><span data-stu-id="81b58-116">ServiceBus Namespace Name.</span></span>

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

### <span data-ttu-id="81b58-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="81b58-117">-ResourceGroupName</span></span>
<span data-ttu-id="81b58-118">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="81b58-118">The resource group name.</span></span>

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

### <span data-ttu-id="81b58-119">-Sku1</span><span class="sxs-lookup"><span data-stu-id="81b58-119">-SkuCapacity</span></span>
<span data-ttu-id="81b58-120">Namespace-SKU-Kapazität.</span><span class="sxs-lookup"><span data-stu-id="81b58-120">Namespace Sku Capacity.</span></span>

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

### <span data-ttu-id="81b58-121">-SkuName</span><span class="sxs-lookup"><span data-stu-id="81b58-121">-SkuName</span></span>
<span data-ttu-id="81b58-122">Der Namespace-SKU-Name.</span><span class="sxs-lookup"><span data-stu-id="81b58-122">The namespace SKU name.</span></span>

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

### <span data-ttu-id="81b58-123">-Tag</span><span class="sxs-lookup"><span data-stu-id="81b58-123">-Tag</span></span>
<span data-ttu-id="81b58-124">Schlüssel-Wert-Paare in Form einer Hashtabelle.</span><span class="sxs-lookup"><span data-stu-id="81b58-124">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="81b58-125">Beispiel: @{key0="value0";key1=$null;key2="value2"}</span><span class="sxs-lookup"><span data-stu-id="81b58-125">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="81b58-126">-Confirm</span><span class="sxs-lookup"><span data-stu-id="81b58-126">-Confirm</span></span>
<span data-ttu-id="81b58-127">Aktualisiert den Namespace "Service Bus" mit den angegebenen Informationen.</span><span class="sxs-lookup"><span data-stu-id="81b58-127">Updates the Service Bus namespace with the specified information.</span></span>

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

### <span data-ttu-id="81b58-128">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="81b58-128">-WhatIf</span></span>
<span data-ttu-id="81b58-129">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="81b58-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="81b58-130">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="81b58-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="81b58-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="81b58-131">CommonParameters</span></span>
<span data-ttu-id="81b58-132">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="81b58-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="81b58-133">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="81b58-133">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="81b58-134">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="81b58-134">INPUTS</span></span>

### <span data-ttu-id="81b58-135">System.String</span><span class="sxs-lookup"><span data-stu-id="81b58-135">System.String</span></span>

### <span data-ttu-id="81b58-136">System.Nullable'1[[System.Int32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="81b58-136">System.Nullable\`1[[System.Int32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="81b58-137">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="81b58-137">System.Collections.Hashtable</span></span>

## <span data-ttu-id="81b58-138">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="81b58-138">OUTPUTS</span></span>

### <span data-ttu-id="81b58-139">Microsoft.Azure.Commands.ServiceBus.Models.PSNamespaceAttributes</span><span class="sxs-lookup"><span data-stu-id="81b58-139">Microsoft.Azure.Commands.ServiceBus.Models.PSNamespaceAttributes</span></span>

## <span data-ttu-id="81b58-140">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="81b58-140">NOTES</span></span>

## <span data-ttu-id="81b58-141">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="81b58-141">RELATED LINKS</span></span>
