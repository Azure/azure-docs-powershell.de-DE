---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceBus.dll-Help.xml
Module Name: Az.ServiceBus
online version: https://docs.microsoft.com/powershell/module/az.servicebus/set-azservicebusnamespace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Set-AzServiceBusNamespace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Set-AzServiceBusNamespace.md
ms.openlocfilehash: f1edc3f65747203a587de82c9f03ce79b258cd36
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101933443"
---
# <span data-ttu-id="58498-101">Set-AzServiceBusNamespace</span><span class="sxs-lookup"><span data-stu-id="58498-101">Set-AzServiceBusNamespace</span></span>

## <span data-ttu-id="58498-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="58498-102">SYNOPSIS</span></span>
<span data-ttu-id="58498-103">Aktualisiert die Beschreibung eines vorhandenen Service Bus-Namespaces.</span><span class="sxs-lookup"><span data-stu-id="58498-103">Updates the description of an existing Service Bus namespace.</span></span>

## <span data-ttu-id="58498-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="58498-104">SYNTAX</span></span>

```
Set-AzServiceBusNamespace [-ResourceGroupName] <String> [-Location] <String> [-Name] <String>
 [-SkuName <String>] [-SkuCapacity <Int32>] [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="58498-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="58498-105">DESCRIPTION</span></span>
<span data-ttu-id="58498-106">Das **Cmdlet Set-AzServiceBusNamespace** aktualisiert die Beschreibung des angegebenen Service Bus-Namespaces innerhalb der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="58498-106">The **Set-AzServiceBusNamespace** cmdlet updates the description of the specified Service Bus namespace within the resource group.</span></span>

## <span data-ttu-id="58498-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="58498-107">EXAMPLES</span></span>

### <span data-ttu-id="58498-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="58498-108">Example 1</span></span>
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

<span data-ttu-id="58498-109">Aktualisiert den Service Bus-Namespace mit einer neuen Beschreibung.</span><span class="sxs-lookup"><span data-stu-id="58498-109">Updates the Service Bus namespace with a new description.</span></span>

## <span data-ttu-id="58498-110">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="58498-110">PARAMETERS</span></span>

### <span data-ttu-id="58498-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="58498-111">-DefaultProfile</span></span>
<span data-ttu-id="58498-112">Die Anmeldeinformationen, das Konto, der Mandant und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="58498-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="58498-113">-Location</span><span class="sxs-lookup"><span data-stu-id="58498-113">-Location</span></span>
<span data-ttu-id="58498-114">Der Namespacespeicherort des Dienstbuss.</span><span class="sxs-lookup"><span data-stu-id="58498-114">The Service Bus namespace location.</span></span>

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

### <span data-ttu-id="58498-115">-Name</span><span class="sxs-lookup"><span data-stu-id="58498-115">-Name</span></span>
<span data-ttu-id="58498-116">Namespacename von ServiceBus.</span><span class="sxs-lookup"><span data-stu-id="58498-116">ServiceBus Namespace Name.</span></span>

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

### <span data-ttu-id="58498-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="58498-117">-ResourceGroupName</span></span>
<span data-ttu-id="58498-118">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="58498-118">The resource group name.</span></span>

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

### <span data-ttu-id="58498-119">-SkuCapacity</span><span class="sxs-lookup"><span data-stu-id="58498-119">-SkuCapacity</span></span>
<span data-ttu-id="58498-120">Namespace-Sku-Kapazität.</span><span class="sxs-lookup"><span data-stu-id="58498-120">Namespace Sku Capacity.</span></span>

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

### <span data-ttu-id="58498-121">-SkuName</span><span class="sxs-lookup"><span data-stu-id="58498-121">-SkuName</span></span>
<span data-ttu-id="58498-122">Namespace-SKU-Name.</span><span class="sxs-lookup"><span data-stu-id="58498-122">The namespace SKU name.</span></span>

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

### <span data-ttu-id="58498-123">-Tag</span><span class="sxs-lookup"><span data-stu-id="58498-123">-Tag</span></span>
<span data-ttu-id="58498-124">Schlüssel-Wert-Paare in Form einer Hashtabelle.</span><span class="sxs-lookup"><span data-stu-id="58498-124">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="58498-125">Beispiel: @{key0="value0";key1=$null;key2="value2"}</span><span class="sxs-lookup"><span data-stu-id="58498-125">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="58498-126">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="58498-126">-Confirm</span></span>
<span data-ttu-id="58498-127">Aktualisiert den Service Bus-Namespace mit den angegebenen Informationen.</span><span class="sxs-lookup"><span data-stu-id="58498-127">Updates the Service Bus namespace with the specified information.</span></span>

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

### <span data-ttu-id="58498-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="58498-128">-WhatIf</span></span>
<span data-ttu-id="58498-129">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="58498-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="58498-130">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="58498-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="58498-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="58498-131">CommonParameters</span></span>
<span data-ttu-id="58498-132">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="58498-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="58498-133">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="58498-133">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="58498-134">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="58498-134">INPUTS</span></span>

### <span data-ttu-id="58498-135">System.String</span><span class="sxs-lookup"><span data-stu-id="58498-135">System.String</span></span>

### <span data-ttu-id="58498-136">System.Nullable'1[[System.Int32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="58498-136">System.Nullable\`1[[System.Int32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="58498-137">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="58498-137">System.Collections.Hashtable</span></span>

## <span data-ttu-id="58498-138">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="58498-138">OUTPUTS</span></span>

### <span data-ttu-id="58498-139">Microsoft.Azure.Commands.ServiceBus.Models.PSNamespaceAttributes</span><span class="sxs-lookup"><span data-stu-id="58498-139">Microsoft.Azure.Commands.ServiceBus.Models.PSNamespaceAttributes</span></span>

## <span data-ttu-id="58498-140">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="58498-140">NOTES</span></span>

## <span data-ttu-id="58498-141">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="58498-141">RELATED LINKS</span></span>
