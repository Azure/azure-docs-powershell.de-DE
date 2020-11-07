---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventHub.dll-Help.xml
Module Name: Az.EventHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.eventhub/new-azeventhubnamespace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/New-AzEventHubNamespace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/New-AzEventHubNamespace.md
ms.openlocfilehash: bbe0f406232086fc0441281ae150f95e2c8eb0a4
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/21/2020
ms.locfileid: "93845619"
---
# <span data-ttu-id="a1043-101">New-AzEventHubNamespace</span><span class="sxs-lookup"><span data-stu-id="a1043-101">New-AzEventHubNamespace</span></span>

## <span data-ttu-id="a1043-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="a1043-102">SYNOPSIS</span></span>
<span data-ttu-id="a1043-103">Erstellt einen Event Hubs-Namespace.</span><span class="sxs-lookup"><span data-stu-id="a1043-103">Creates an Event Hubs namespace.</span></span>

## <span data-ttu-id="a1043-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="a1043-104">SYNTAX</span></span>

### <span data-ttu-id="a1043-105">NamespaceParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="a1043-105">NamespaceParameterSet (Default)</span></span>
```
New-AzEventHubNamespace [-ResourceGroupName] <String> [-Name] <String> [-Location] <String>
 [[-SkuName] <String>] [[-SkuCapacity] <Int32>] [[-Tag] <Hashtable>] [-EnableKafka]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a1043-106">AutoInflateParameterSet</span><span class="sxs-lookup"><span data-stu-id="a1043-106">AutoInflateParameterSet</span></span>
```
New-AzEventHubNamespace [-ResourceGroupName] <String> [-Name] <String> [-Location] <String>
 [[-SkuName] <String>] [[-SkuCapacity] <Int32>] [[-Tag] <Hashtable>] [-EnableAutoInflate]
 [[-MaximumThroughputUnits] <Int32>] [-EnableKafka] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a1043-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="a1043-107">DESCRIPTION</span></span>
<span data-ttu-id="a1043-108">Das New-AzEventHubNamespace-Cmdlet erstellt einen neuen Namespace vom Typ Event Hubs.</span><span class="sxs-lookup"><span data-stu-id="a1043-108">The New-AzEventHubNamespace cmdlet creates a new namespace of type Event Hubs.</span></span>

## <span data-ttu-id="a1043-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="a1043-109">EXAMPLES</span></span>

### <span data-ttu-id="a1043-110">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="a1043-110">Example 1</span></span>                                           
```
PS C:\> New-AzEventHubNamespace -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName -Location MyLocation

Name                   : MyNamespaceName
Id                     : /subscriptions/{subscriptionId}/resourceGroups/Default-EventHub-WestCentralUS/providers/Microsoft.EventHub/namespaces/MyNamespaceName
ResourceGroupName      : Default-EventHub-WestCentralUS
Location               : West US
Sku                    : Name : Standard , Capacity : 1 , Tier : Standard
Tags                   :
ProvisioningState      : Succeeded
Status                 : Active
CreatedAt              : 5/24/2019 12:47:27 AM
UpdatedAt              : 5/24/2019 12:48:14 AM
ServiceBusEndpoint     : #########
Enabled                : True
IsAutoInflateEnabled   : False
MaximumThroughputUnits : 0
```

<span data-ttu-id="a1043-111">Erstellt einen Event Hubs \` -Namespace mynamespacename am \` angegebenen geografischen Standort \` mylocation \` in der Ressourcengruppe \` MyResourceGroupName \` .</span><span class="sxs-lookup"><span data-stu-id="a1043-111">Creates an Event Hubs namespace \`MyNamespaceName\` in the specified geographic location \`MyLocation\`, in resource group \`MyResourceGroupName\`.</span></span>

### <span data-ttu-id="a1043-112">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="a1043-112">Example 2</span></span>
```
PS C:\> New-AzEventHubNamespace -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName -Location MyLocation -EnableAutoInflate -MaximumThroughputUnits 10

Name                   : MyNamespaceName
Id                     : /subscriptions/{subscriptionId}/resourceGroups/Default-EventHub-WestCentralUS/providers/Microsoft.EventHub/namespaces/MyNamespaceName
ResourceGroupName      : Default-EventHub-WestCentralUS
Location               : West US
Sku                    : Name : Standard , Capacity : 1 , Tier : Standard
Tags                   :
ProvisioningState      : Succeeded
Status                 : Active
CreatedAt              : 5/24/2019 12:47:27 AM
UpdatedAt              : 5/24/2019 12:48:14 AM
ServiceBusEndpoint     : #########
Enabled                : True
IsAutoInflateEnabled   : True
MaximumThroughputUnits : 10
```

<span data-ttu-id="a1043-113">Erstellt einen Event Hubs-Namespace \` mynamespacename am \` angegebenen geografischen Standort \` mylocation \` , in der Ressourcengruppe \` MyResourceGroupName \` und autopump ist mit MaximumThroughputUnits 10 aktiviert.</span><span class="sxs-lookup"><span data-stu-id="a1043-113">Creates an Event Hubs namespace \`MyNamespaceName\` in the specified geographic location \`MyLocation\`, in resource group \`MyResourceGroupName\` and AutoInflate is enabled with MaximumThroughputUnits 10.</span></span>

### <span data-ttu-id="a1043-114">Beispiel für 3-Kafka-aktivierter Namespace</span><span class="sxs-lookup"><span data-stu-id="a1043-114">Example 3 - Kafka enabled namespace</span></span>
```
PS C:\> New-AzEventHubNamespace -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName -Location MyLocation -EnableAutoInflate -EnableKafka

Name                   : MyNamespaceName
Id                     : /subscriptions/{subscriptionId}/resourceGroups/Default-EventHub-WestCentralUS/providers/Microsoft.EventHub/namespaces/MyNamespaceName
ResourceGroupName      : Default-EventHub-WestCentralUS
Location               : West US
Sku                    : Name : Standard , Capacity : 1 , Tier : Standard
Tags                   :
ProvisioningState      : Succeeded
Status                 : Active
CreatedAt              : 5/24/2019 12:47:27 AM
UpdatedAt              : 5/24/2019 12:48:14 AM
ServiceBusEndpoint     : #########
Enabled                : True
IsAutoInflateEnabled   : True
MaximumThroughputUnits : 12
```

<span data-ttu-id="a1043-115">Erstellt einen Event Hubs \` -Namespace mynamespacename am \` angegebenen geografischen Standort \` mylocation \` , in der Ressourcengruppe \` MyResourceGroupName \` mit Kafka und autopump aktiviert.</span><span class="sxs-lookup"><span data-stu-id="a1043-115">Creates an Event Hubs namespace \`MyNamespaceName\` in the specified geographic location \`MyLocation\`, in resource group \`MyResourceGroupName\` with Kafka and  AutoInflate enabled.</span></span>

## <span data-ttu-id="a1043-116">Parameter</span><span class="sxs-lookup"><span data-stu-id="a1043-116">PARAMETERS</span></span>

### <span data-ttu-id="a1043-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a1043-117">-DefaultProfile</span></span>
<span data-ttu-id="a1043-118">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="a1043-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a1043-119">-EnableAutoInflate</span><span class="sxs-lookup"><span data-stu-id="a1043-119">-EnableAutoInflate</span></span>
<span data-ttu-id="a1043-120">Gibt an, ob autopump aktiviert ist</span><span class="sxs-lookup"><span data-stu-id="a1043-120">Indicates whether AutoInflate is enabled</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: AutoInflateParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a1043-121">-EnableKafka</span><span class="sxs-lookup"><span data-stu-id="a1043-121">-EnableKafka</span></span>
<span data-ttu-id="a1043-122">Aktivieren oder Deaktivieren von Kafka für Namespace</span><span class="sxs-lookup"><span data-stu-id="a1043-122">enabling or disabling Kafka for namespace</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a1043-123">-Standort</span><span class="sxs-lookup"><span data-stu-id="a1043-123">-Location</span></span>
<span data-ttu-id="a1043-124">Speicherort des EventHub-Namespaces.</span><span class="sxs-lookup"><span data-stu-id="a1043-124">EventHub Namespace Location.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a1043-125">-MaximumThroughputUnits</span><span class="sxs-lookup"><span data-stu-id="a1043-125">-MaximumThroughputUnits</span></span>
<span data-ttu-id="a1043-126">Obergrenze von Durchsatz Einheiten wenn autopump aktiviert ist, sollte der Wert innerhalb von 0 bis 20 Durchsatz Einheiten liegen.</span><span class="sxs-lookup"><span data-stu-id="a1043-126">Upper limit of throughput units when AutoInflate is enabled, value should be within 0 to 20 throughput units.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: AutoInflateParameterSet
Aliases:

Required: False
Position: 7
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a1043-127">-Name</span><span class="sxs-lookup"><span data-stu-id="a1043-127">-Name</span></span>
<span data-ttu-id="a1043-128">Name des EventHub-Namespaces.</span><span class="sxs-lookup"><span data-stu-id="a1043-128">EventHub Namespace Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: NamespaceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a1043-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a1043-129">-ResourceGroupName</span></span>
<span data-ttu-id="a1043-130">Ressourcengruppen Name</span><span class="sxs-lookup"><span data-stu-id="a1043-130">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a1043-131">-SkuCapacity</span><span class="sxs-lookup"><span data-stu-id="a1043-131">-SkuCapacity</span></span>
<span data-ttu-id="a1043-132">Die eventhub-Durchsatz Einheiten.</span><span class="sxs-lookup"><span data-stu-id="a1043-132">The eventhub throughput units.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a1043-133">-SkuName</span><span class="sxs-lookup"><span data-stu-id="a1043-133">-SkuName</span></span>
<span data-ttu-id="a1043-134">Namespace-SKU-Name.</span><span class="sxs-lookup"><span data-stu-id="a1043-134">Namespace Sku Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Basic, Standard, Premium

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a1043-135">-Tag</span><span class="sxs-lookup"><span data-stu-id="a1043-135">-Tag</span></span>
<span data-ttu-id="a1043-136">Hashtables, die Ressourcen Tags darstellen.</span><span class="sxs-lookup"><span data-stu-id="a1043-136">Hashtables which represents resource Tags.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a1043-137">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="a1043-137">-Confirm</span></span>
<span data-ttu-id="a1043-138">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="a1043-138">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a1043-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a1043-139">-WhatIf</span></span>
<span data-ttu-id="a1043-140">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="a1043-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a1043-141">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="a1043-141">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a1043-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a1043-142">CommonParameters</span></span>
<span data-ttu-id="a1043-143">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a1043-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a1043-144">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a1043-144">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a1043-145">Eingaben</span><span class="sxs-lookup"><span data-stu-id="a1043-145">INPUTS</span></span>

### <span data-ttu-id="a1043-146">System. String</span><span class="sxs-lookup"><span data-stu-id="a1043-146">System.String</span></span>

### <span data-ttu-id="a1043-147">System. Nullable ' 1 [[System. Int32, System. private. CoreLib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="a1043-147">System.Nullable\`1[[System.Int32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="a1043-148">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="a1043-148">System.Collections.Hashtable</span></span>

## <span data-ttu-id="a1043-149">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="a1043-149">OUTPUTS</span></span>

### <span data-ttu-id="a1043-150">Microsoft. Azure. Commands. EventHub. Models. PSNamespaceAttributes</span><span class="sxs-lookup"><span data-stu-id="a1043-150">Microsoft.Azure.Commands.EventHub.Models.PSNamespaceAttributes</span></span>

## <span data-ttu-id="a1043-151">Notizen</span><span class="sxs-lookup"><span data-stu-id="a1043-151">NOTES</span></span>

## <span data-ttu-id="a1043-152">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="a1043-152">RELATED LINKS</span></span>
