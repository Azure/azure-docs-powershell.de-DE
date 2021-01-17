---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceBus.dll-Help.xml
Module Name: Az.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicebus/new-azservicebusnamespace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/New-AzServiceBusNamespace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/New-AzServiceBusNamespace.md
ms.openlocfilehash: 9ef77d9a02f2337aac2886cf033cfa752463e8d2
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98471897"
---
# <span data-ttu-id="1e6b9-101">New-AzServiceBusNamespace</span><span class="sxs-lookup"><span data-stu-id="1e6b9-101">New-AzServiceBusNamespace</span></span>

## <span data-ttu-id="1e6b9-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1e6b9-102">SYNOPSIS</span></span>
<span data-ttu-id="1e6b9-103">Erstellt einen neuen Service Bus-Namespace.</span><span class="sxs-lookup"><span data-stu-id="1e6b9-103">Creates a new Service Bus namespace.</span></span>

## <span data-ttu-id="1e6b9-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="1e6b9-104">SYNTAX</span></span>

```
New-AzServiceBusNamespace [-ResourceGroupName] <String> [-Location] <String> [-Name] <String>
 [-SkuName <String>] [-SkuCapacity <Int32>] [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1e6b9-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="1e6b9-105">DESCRIPTION</span></span>
<span data-ttu-id="1e6b9-106">Das **Cmdlet "New-AzServiceBusNamespace"** erstellt einen neuen Service Bus-Namespace.</span><span class="sxs-lookup"><span data-stu-id="1e6b9-106">The **New-AzServiceBusNamespace** cmdlet creates a new Service Bus namespace.</span></span> <span data-ttu-id="1e6b9-107">Nachdem das Namespaceressourcenmanifest erstellt wurde, kann es unveränderlich sein.</span><span class="sxs-lookup"><span data-stu-id="1e6b9-107">Once created, the namespace resource manifest is immutable.</span></span> <span data-ttu-id="1e6b9-108">Dieser Vorgang ist "idempotent".</span><span class="sxs-lookup"><span data-stu-id="1e6b9-108">This operation is idempotent.</span></span>

## <span data-ttu-id="1e6b9-109">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="1e6b9-109">EXAMPLES</span></span>

### <span data-ttu-id="1e6b9-110">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="1e6b9-110">Example 1</span></span>
```
PS C:\> New-AzServiceBusNamespace -ResourceGroupName Default-ServiceBus-WestUS -Name SB-Example1 -Location WestUS -SkuName "Standard" -Tag @{Tag1="Tag1Value"}

Name               : SB-Example1
Id                 : /subscriptions/{SubscriptionId}/resourceGroups/Default-ServiceBus-WestUS/providers/Microsoft.ServiceBus/namespaces/SB-Example1
ResourceGroupName  : Default-ServiceBus-WestUS
Location           : West US
Tags               : {TesttingTags, TestingTagValue, TestTag, TestTagValue}
Sku                : Name : Premium , Tier : Premium
ProvisioningState  : Succeeded
CreatedAt          : 1/20/2017 2:07:33 AM
UpdatedAt          : 1/20/2017 2:07:56 AM
ServiceBusEndpoint : https://SB-Example1.servicebus.windows.net:443/
```

<span data-ttu-id="1e6b9-111">Erstellt einen neuen Service Bus-Namespace innerhalb der angegebenen Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="1e6b9-111">Creates a new Service Bus namespace within the specified resource group.</span></span>

## <span data-ttu-id="1e6b9-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="1e6b9-112">PARAMETERS</span></span>

### <span data-ttu-id="1e6b9-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1e6b9-113">-DefaultProfile</span></span>
<span data-ttu-id="1e6b9-114">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="1e6b9-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="1e6b9-115">-Location</span><span class="sxs-lookup"><span data-stu-id="1e6b9-115">-Location</span></span>
<span data-ttu-id="1e6b9-116">Der Namespacespeicherort des Service Bus.</span><span class="sxs-lookup"><span data-stu-id="1e6b9-116">The Service Bus namespace location.</span></span>

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

### <span data-ttu-id="1e6b9-117">-Name</span><span class="sxs-lookup"><span data-stu-id="1e6b9-117">-Name</span></span>
<span data-ttu-id="1e6b9-118">ServiceBus Namespacename.</span><span class="sxs-lookup"><span data-stu-id="1e6b9-118">ServiceBus Namespace Name.</span></span>

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

### <span data-ttu-id="1e6b9-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1e6b9-119">-ResourceGroupName</span></span>
<span data-ttu-id="1e6b9-120">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="1e6b9-120">The resource group name.</span></span>

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

### <span data-ttu-id="1e6b9-121">-Sku1</span><span class="sxs-lookup"><span data-stu-id="1e6b9-121">-SkuCapacity</span></span>
<span data-ttu-id="1e6b9-122">Die Service Bus Premium-Namespacedurchsatzeinheiten, zulässige Werte 1 oder 2 oder 4</span><span class="sxs-lookup"><span data-stu-id="1e6b9-122">The Service Bus premium namespace throughput units, allowed values 1 or 2 or 4</span></span>

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

### <span data-ttu-id="1e6b9-123">-SkuName</span><span class="sxs-lookup"><span data-stu-id="1e6b9-123">-SkuName</span></span>
<span data-ttu-id="1e6b9-124">Der Name der Service Bus-SKU.</span><span class="sxs-lookup"><span data-stu-id="1e6b9-124">The Service Bus namespace SKU name.</span></span>

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

### <span data-ttu-id="1e6b9-125">-Tag</span><span class="sxs-lookup"><span data-stu-id="1e6b9-125">-Tag</span></span>
<span data-ttu-id="1e6b9-126">Schlüssel-Wert-Paare in Form einer Hashtabelle, die als Tags auf dem Server festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="1e6b9-126">Key-value pairs in the form of a hash table set as tags on the server.</span></span> <span data-ttu-id="1e6b9-127">Beispiel: @{key0="value0";key1=$null;key2="value2"}</span><span class="sxs-lookup"><span data-stu-id="1e6b9-127">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="1e6b9-128">-Confirm</span><span class="sxs-lookup"><span data-stu-id="1e6b9-128">-Confirm</span></span>
<span data-ttu-id="1e6b9-129">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="1e6b9-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1e6b9-130">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="1e6b9-130">-WhatIf</span></span>
<span data-ttu-id="1e6b9-131">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="1e6b9-131">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="1e6b9-132">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="1e6b9-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1e6b9-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1e6b9-133">CommonParameters</span></span>
<span data-ttu-id="1e6b9-134">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1e6b9-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1e6b9-135">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1e6b9-135">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1e6b9-136">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="1e6b9-136">INPUTS</span></span>

### <span data-ttu-id="1e6b9-137">System.String</span><span class="sxs-lookup"><span data-stu-id="1e6b9-137">System.String</span></span>

### <span data-ttu-id="1e6b9-138">System.Nullable'1[[System.Int32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="1e6b9-138">System.Nullable\`1[[System.Int32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="1e6b9-139">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="1e6b9-139">System.Collections.Hashtable</span></span>

## <span data-ttu-id="1e6b9-140">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="1e6b9-140">OUTPUTS</span></span>

### <span data-ttu-id="1e6b9-141">Microsoft.Azure.Commands.ServiceBus.Models.PSNamespaceAttributes</span><span class="sxs-lookup"><span data-stu-id="1e6b9-141">Microsoft.Azure.Commands.ServiceBus.Models.PSNamespaceAttributes</span></span>

## <span data-ttu-id="1e6b9-142">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="1e6b9-142">NOTES</span></span>

## <span data-ttu-id="1e6b9-143">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="1e6b9-143">RELATED LINKS</span></span>
