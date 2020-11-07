---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceBus.dll-Help.xml
Module Name: Az.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicebus/set-azservicebusnamespace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Set-AzServiceBusNamespace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Set-AzServiceBusNamespace.md
ms.openlocfilehash: 8f2651e2bfc0271964b055244995aead1b93a172
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93659354"
---
# <span data-ttu-id="5d658-101">Set-AzServiceBusNamespace</span><span class="sxs-lookup"><span data-stu-id="5d658-101">Set-AzServiceBusNamespace</span></span>

## <span data-ttu-id="5d658-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="5d658-102">SYNOPSIS</span></span>
<span data-ttu-id="5d658-103">Aktualisiert die Beschreibung eines vorhandenen Service Bus-Namespaces.</span><span class="sxs-lookup"><span data-stu-id="5d658-103">Updates the description of an existing Service Bus namespace.</span></span>

## <span data-ttu-id="5d658-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="5d658-104">SYNTAX</span></span>

```
Set-AzServiceBusNamespace [-ResourceGroupName] <String> [-Location] <String> [-Name] <String>
 [-SkuName <String>] [-SkuCapacity <Int32>] [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5d658-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="5d658-105">DESCRIPTION</span></span>
<span data-ttu-id="5d658-106">Das Cmdlet " **Satz-AzServiceBusNamespace** " aktualisiert die Beschreibung des angegebenen ServiceBus-Namespaces innerhalb der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="5d658-106">The **Set-AzServiceBusNamespace** cmdlet updates the description of the specified Service Bus namespace within the resource group.</span></span>

## <span data-ttu-id="5d658-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="5d658-107">EXAMPLES</span></span>

### <span data-ttu-id="5d658-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="5d658-108">Example 1</span></span>
```
PS C:\> Set-AzServiceBusNamespace -ResourceGroup Default-ServiceBus-WestUS -NamespaceName SB-Example1 -Location WestUs -SkuName Premium -SkuCapacity 1 -Tag @{Tag2="Tag2Value"}

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

<span data-ttu-id="5d658-109">Aktualisiert den ServiceBus-Namespace mit einer neuen Beschreibung.</span><span class="sxs-lookup"><span data-stu-id="5d658-109">Updates the Service Bus namespace with a new description.</span></span>

## <span data-ttu-id="5d658-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="5d658-110">PARAMETERS</span></span>

### <span data-ttu-id="5d658-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5d658-111">-DefaultProfile</span></span>
<span data-ttu-id="5d658-112">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="5d658-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="5d658-113">-Standort</span><span class="sxs-lookup"><span data-stu-id="5d658-113">-Location</span></span>
<span data-ttu-id="5d658-114">Der Speicherort des ServiceBus-Namespaces.</span><span class="sxs-lookup"><span data-stu-id="5d658-114">The Service Bus namespace location.</span></span>

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

### <span data-ttu-id="5d658-115">-Name</span><span class="sxs-lookup"><span data-stu-id="5d658-115">-Name</span></span>
<span data-ttu-id="5d658-116">Name des ServiceBus-Namespaces.</span><span class="sxs-lookup"><span data-stu-id="5d658-116">ServiceBus Namespace Name.</span></span>

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

### <span data-ttu-id="5d658-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5d658-117">-ResourceGroupName</span></span>
<span data-ttu-id="5d658-118">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="5d658-118">The resource group name.</span></span>

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

### <span data-ttu-id="5d658-119">-SkuCapacity</span><span class="sxs-lookup"><span data-stu-id="5d658-119">-SkuCapacity</span></span>
<span data-ttu-id="5d658-120">SKU-Kapazität des Namespaces.</span><span class="sxs-lookup"><span data-stu-id="5d658-120">Namespace Sku Capacity.</span></span>

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

### <span data-ttu-id="5d658-121">-SkuName</span><span class="sxs-lookup"><span data-stu-id="5d658-121">-SkuName</span></span>
<span data-ttu-id="5d658-122">Der Namespace-SKU-Name.</span><span class="sxs-lookup"><span data-stu-id="5d658-122">The namespace SKU name.</span></span>

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

### <span data-ttu-id="5d658-123">-Tag</span><span class="sxs-lookup"><span data-stu-id="5d658-123">-Tag</span></span>
<span data-ttu-id="5d658-124">Schlüssel-Wert-Paare in Form einer Hashtabelle</span><span class="sxs-lookup"><span data-stu-id="5d658-124">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="5d658-125">Beispiel: @ {Key0 = "value0"; key1 = $NULL; key2 = "Value2"}</span><span class="sxs-lookup"><span data-stu-id="5d658-125">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="5d658-126">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="5d658-126">-Confirm</span></span>
<span data-ttu-id="5d658-127">Aktualisiert den ServiceBus-Namespace mit den angegebenen Informationen.</span><span class="sxs-lookup"><span data-stu-id="5d658-127">Updates the Service Bus namespace with the specified information.</span></span>

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

### <span data-ttu-id="5d658-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5d658-128">-WhatIf</span></span>
<span data-ttu-id="5d658-129">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="5d658-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5d658-130">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="5d658-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5d658-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5d658-131">CommonParameters</span></span>
<span data-ttu-id="5d658-132">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5d658-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5d658-133">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5d658-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5d658-134">Eingaben</span><span class="sxs-lookup"><span data-stu-id="5d658-134">INPUTS</span></span>

### <span data-ttu-id="5d658-135">System. String</span><span class="sxs-lookup"><span data-stu-id="5d658-135">System.String</span></span>

### <span data-ttu-id="5d658-136">System. Nullable ' 1 [[System. Int32, System. private. CoreLib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="5d658-136">System.Nullable\`1[[System.Int32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="5d658-137">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="5d658-137">System.Collections.Hashtable</span></span>

## <span data-ttu-id="5d658-138">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="5d658-138">OUTPUTS</span></span>

### <span data-ttu-id="5d658-139">Microsoft. Azure. Commands. ServiceBus. Models. PSNamespaceAttributes</span><span class="sxs-lookup"><span data-stu-id="5d658-139">Microsoft.Azure.Commands.ServiceBus.Models.PSNamespaceAttributes</span></span>

## <span data-ttu-id="5d658-140">Notizen</span><span class="sxs-lookup"><span data-stu-id="5d658-140">NOTES</span></span>

## <span data-ttu-id="5d658-141">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="5d658-141">RELATED LINKS</span></span>
