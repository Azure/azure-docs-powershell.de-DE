---
external help file: Microsoft.Azure.Commands.EventHub.dll-Help.xml
Module Name: AzureRM.EventHub
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.eventhub/new-azurermeventhubnamespace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/New-AzureRmEventHubNamespace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/New-AzureRmEventHubNamespace.md
ms.openlocfilehash: 0fb90529f4157bf627e43477e3db41764040e5c6
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93663146"
---
# <span data-ttu-id="3b7d7-101">New-AzureRmEventHubNamespace</span><span class="sxs-lookup"><span data-stu-id="3b7d7-101">New-AzureRmEventHubNamespace</span></span>

## <span data-ttu-id="3b7d7-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="3b7d7-102">SYNOPSIS</span></span>
<span data-ttu-id="3b7d7-103">Erstellt einen Event Hubs-Namespace.</span><span class="sxs-lookup"><span data-stu-id="3b7d7-103">Creates an Event Hubs namespace.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="3b7d7-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="3b7d7-104">SYNTAX</span></span>

### <span data-ttu-id="3b7d7-105">NamespaceParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="3b7d7-105">NamespaceParameterSet (Default)</span></span>
```
New-AzureRmEventHubNamespace [-ResourceGroupName] <String> [-Name] <String> [-Location] <String>
 [[-SkuName] <String>] [[-SkuCapacity] <Int32>] [[-Tag] <Hashtable>] [-EnableKafka] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3b7d7-106">AutoInflateParameterSet</span><span class="sxs-lookup"><span data-stu-id="3b7d7-106">AutoInflateParameterSet</span></span>
```
New-AzureRmEventHubNamespace [-ResourceGroupName] <String> [-Name] <String> [-Location] <String>
 [[-SkuName] <String>] [[-SkuCapacity] <Int32>] [[-Tag] <Hashtable>] [-EnableAutoInflate]
 [[-MaximumThroughputUnits] <Int32>] [-EnableKafka] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="3b7d7-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="3b7d7-107">DESCRIPTION</span></span>
<span data-ttu-id="3b7d7-108">Das New-AzureRmEventHubNamespace-Cmdlet erstellt einen neuen Namespace vom Typ Event Hubs.</span><span class="sxs-lookup"><span data-stu-id="3b7d7-108">The New-AzureRmEventHubNamespace cmdlet creates a new namespace of type Event Hubs.</span></span>

## <span data-ttu-id="3b7d7-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="3b7d7-109">EXAMPLES</span></span>

### <span data-ttu-id="3b7d7-110">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="3b7d7-110">Example 1</span></span>                                              
```
PS C:\> New-AzureRmEventHubNamespace -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName -Location MyLocation
```

<span data-ttu-id="3b7d7-111">Erstellt einen Event Hubs \` -Namespace mynamespacename am \` angegebenen geografischen Standort \` mylocation \` in der Ressourcengruppe \` MyResourceGroupName \` .</span><span class="sxs-lookup"><span data-stu-id="3b7d7-111">Creates an Event Hubs namespace \`MyNamespaceName\` in the specified geographic location \`MyLocation\`, in resource group \`MyResourceGroupName\`.</span></span>

### <span data-ttu-id="3b7d7-112">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="3b7d7-112">Example 2</span></span>
```
PS C:\> New-AzureRmEventHubNamespace -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName -Location MyLocation -EnableAutoInflate -MaximumThroughputUnits 10
```

<span data-ttu-id="3b7d7-113">Erstellt einen Event Hubs-Namespace \` mynamespacename am \` angegebenen geografischen Standort \` mylocation \` , in der Ressourcengruppe \` MyResourceGroupName \` und autopump ist mit MaximumThroughputUnits 10 aktiviert.</span><span class="sxs-lookup"><span data-stu-id="3b7d7-113">Creates an Event Hubs namespace \`MyNamespaceName\` in the specified geographic location \`MyLocation\`, in resource group \`MyResourceGroupName\` and AutoInflate is enabled with MaximumThroughputUnits 10.</span></span>

### <span data-ttu-id="3b7d7-114">Beispiel für 3-Kafka-aktivierter Namespace</span><span class="sxs-lookup"><span data-stu-id="3b7d7-114">Example 3 - Kafka enabled namespace</span></span>
```
PS C:\> New-AzureRmEventHubNamespace -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName -Location MyLocation -EnableAutoInflate -EnableKafka
```

<span data-ttu-id="3b7d7-115">Erstellt einen Event Hubs \` -Namespace mynamespacename am \` angegebenen geografischen Standort \` mylocation \` , in der Ressourcengruppe \` MyResourceGroupName \` mit Kafka und autopump aktiviert.</span><span class="sxs-lookup"><span data-stu-id="3b7d7-115">Creates an Event Hubs namespace \`MyNamespaceName\` in the specified geographic location \`MyLocation\`, in resource group \`MyResourceGroupName\` with Kafka and  AutoInflate enabled.</span></span>

## <span data-ttu-id="3b7d7-116">Parameter</span><span class="sxs-lookup"><span data-stu-id="3b7d7-116">PARAMETERS</span></span>

### <span data-ttu-id="3b7d7-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3b7d7-117">-DefaultProfile</span></span>
<span data-ttu-id="3b7d7-118">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="3b7d7-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3b7d7-119">-EnableAutoInflate</span><span class="sxs-lookup"><span data-stu-id="3b7d7-119">-EnableAutoInflate</span></span>
<span data-ttu-id="3b7d7-120">Gibt an, ob autopump aktiviert ist</span><span class="sxs-lookup"><span data-stu-id="3b7d7-120">Indicates whether AutoInflate is enabled</span></span>

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

### <span data-ttu-id="3b7d7-121">-EnableKafka</span><span class="sxs-lookup"><span data-stu-id="3b7d7-121">-EnableKafka</span></span>
<span data-ttu-id="3b7d7-122">Aktivieren oder Deaktivieren von Kafka für Namespace</span><span class="sxs-lookup"><span data-stu-id="3b7d7-122">enabling or disabling Kafka for namespace</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: AutoInflateParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```         

### <span data-ttu-id="3b7d7-123">-Standort</span><span class="sxs-lookup"><span data-stu-id="3b7d7-123">-Location</span></span>
<span data-ttu-id="3b7d7-124">Speicherort des EventHub-Namespaces.</span><span class="sxs-lookup"><span data-stu-id="3b7d7-124">EventHub Namespace Location.</span></span>

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

### <span data-ttu-id="3b7d7-125">-MaximumThroughputUnits</span><span class="sxs-lookup"><span data-stu-id="3b7d7-125">-MaximumThroughputUnits</span></span>
<span data-ttu-id="3b7d7-126">Obergrenze von Durchsatz Einheiten wenn autopump aktiviert ist, sollte der Wert innerhalb von 0 bis 20 Durchsatz Einheiten liegen.</span><span class="sxs-lookup"><span data-stu-id="3b7d7-126">Upper limit of throughput units when AutoInflate is enabled, value should be within 0 to 20 throughput units.</span></span>

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

### <span data-ttu-id="3b7d7-127">-Name</span><span class="sxs-lookup"><span data-stu-id="3b7d7-127">-Name</span></span>
<span data-ttu-id="3b7d7-128">Name des EventHub-Namespaces.</span><span class="sxs-lookup"><span data-stu-id="3b7d7-128">EventHub Namespace Name.</span></span>

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

### <span data-ttu-id="3b7d7-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3b7d7-129">-ResourceGroupName</span></span>
<span data-ttu-id="3b7d7-130">Ressourcengruppen Name</span><span class="sxs-lookup"><span data-stu-id="3b7d7-130">Resource Group Name</span></span>

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

### <span data-ttu-id="3b7d7-131">-SkuCapacity</span><span class="sxs-lookup"><span data-stu-id="3b7d7-131">-SkuCapacity</span></span>
<span data-ttu-id="3b7d7-132">Die eventhub-Durchsatz Einheiten.</span><span class="sxs-lookup"><span data-stu-id="3b7d7-132">The eventhub throughput units.</span></span>

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

### <span data-ttu-id="3b7d7-133">-SkuName</span><span class="sxs-lookup"><span data-stu-id="3b7d7-133">-SkuName</span></span>
<span data-ttu-id="3b7d7-134">Namespace-SKU-Name.</span><span class="sxs-lookup"><span data-stu-id="3b7d7-134">Namespace Sku Name.</span></span>

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

### <span data-ttu-id="3b7d7-135">-Tag</span><span class="sxs-lookup"><span data-stu-id="3b7d7-135">-Tag</span></span>
<span data-ttu-id="3b7d7-136">Hashtables, die Ressourcen Tags darstellen.</span><span class="sxs-lookup"><span data-stu-id="3b7d7-136">Hashtables which represents resource Tags.</span></span>

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

### <span data-ttu-id="3b7d7-137">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="3b7d7-137">-Confirm</span></span>
<span data-ttu-id="3b7d7-138">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="3b7d7-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3b7d7-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3b7d7-139">-WhatIf</span></span>
<span data-ttu-id="3b7d7-140">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="3b7d7-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3b7d7-141">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="3b7d7-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3b7d7-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3b7d7-142">CommonParameters</span></span>
<span data-ttu-id="3b7d7-143">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3b7d7-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="3b7d7-144">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3b7d7-144">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3b7d7-145">Eingaben</span><span class="sxs-lookup"><span data-stu-id="3b7d7-145">INPUTS</span></span>


## <span data-ttu-id="3b7d7-146">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="3b7d7-146">OUTPUTS</span></span>

### <span data-ttu-id="3b7d7-147">Microsoft. Azure. Commands. EventHub. Models. PSNamespaceAttributes</span><span class="sxs-lookup"><span data-stu-id="3b7d7-147">Microsoft.Azure.Commands.EventHub.Models.PSNamespaceAttributes</span></span>


## <span data-ttu-id="3b7d7-148">Notizen</span><span class="sxs-lookup"><span data-stu-id="3b7d7-148">NOTES</span></span>

## <span data-ttu-id="3b7d7-149">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="3b7d7-149">RELATED LINKS</span></span>
