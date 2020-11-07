---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventHub.dll-Help.xml
Module Name: Az.EventHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.eventhub/set-azeventhubnamespace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Set-AzEventHubNamespace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Set-AzEventHubNamespace.md
ms.openlocfilehash: 99993a92179da1adaba068ae7bb525b5b2cca5df
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93651147"
---
# <span data-ttu-id="2e88e-101">Set-AzEventHubNamespace</span><span class="sxs-lookup"><span data-stu-id="2e88e-101">Set-AzEventHubNamespace</span></span>

## <span data-ttu-id="2e88e-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="2e88e-102">SYNOPSIS</span></span>
<span data-ttu-id="2e88e-103">Aktualisiert den angegebenen Event Hubs-Namespace.</span><span class="sxs-lookup"><span data-stu-id="2e88e-103">Updates the specified Event Hubs namespace.</span></span>

## <span data-ttu-id="2e88e-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="2e88e-104">SYNTAX</span></span>

### <span data-ttu-id="2e88e-105">NamespaceParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="2e88e-105">NamespaceParameterSet (Default)</span></span>
```
Set-AzEventHubNamespace [-ResourceGroupName] <String> [-Name] <String> [-Location] <String>
 [[-SkuName] <String>] [[-SkuCapacity] <Int32>] [[-State] <NamespaceState>] [[-Tag] <Hashtable>] [-EnableKafka] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2e88e-106">AutoInflateParameterSet</span><span class="sxs-lookup"><span data-stu-id="2e88e-106">AutoInflateParameterSet</span></span>
```
Set-AzEventHubNamespace [-ResourceGroupName] <String> [-Name] <String> [-Location] <String>
 [[-SkuName] <String>] [[-SkuCapacity] <Int32>] [[-State] <NamespaceState>] [[-Tag] <Hashtable>]
 [-EnableAutoInflate] [-MaximumThroughputUnits <Int32>] [-EnableKafka] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2e88e-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="2e88e-107">DESCRIPTION</span></span>
<span data-ttu-id="2e88e-108">Das Set-AzEventHubNamespace-Cmdlet aktualisiert die Eigenschaften des angegebenen Event Hubs-Namespace.</span><span class="sxs-lookup"><span data-stu-id="2e88e-108">The Set-AzEventHubNamespace cmdlet updates the properties of the specified Event Hubs namespace.</span></span>

## <span data-ttu-id="2e88e-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="2e88e-109">EXAMPLES</span></span>

### <span data-ttu-id="2e88e-110">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="2e88e-110">Example 1</span></span>
```
PS C:\> Set-AzEventHubNamespace -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName -Location "WestUS" -Tag @{Tag1='TagValue1'; Tag2='TagValue2'}

Name                   : MyNamespaceName
Id                     : /subscriptions/{subscriptionId}/resourceGroups/Default-EventHub-WestCentralUS/providers/Microsoft.EventHub/namespaces/MyNamespaceName
ResourceGroupName      : Default-EventHub-WestCentralUS
Location               : West US
Sku                    : Name : Standard , Capacity : 1 , Tier : Standard
Tags                   : {Tag2, TagValue2, Tag1, TagValue1}
ProvisioningState      : Succeeded
Status                 : Active
CreatedAt              : 5/24/2019 12:47:27 AM
UpdatedAt              : 5/24/2019 12:48:14 AM
ServiceBusEndpoint     : #########
Enabled                : True
KafkaEnabled           : True
IsAutoInflateEnabled   : True
MaximumThroughputUnits : 10

```

<span data-ttu-id="2e88e-111">Aktualisiert die Tags für Namespace \` mynamespacename \` auf created.</span><span class="sxs-lookup"><span data-stu-id="2e88e-111">Updates the Tags for namespace \`MyNamespaceName\` to Created .</span></span>

### <span data-ttu-id="2e88e-112">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="2e88e-112">Example 2</span></span>
```
PS C:\> Set-AzEventHubNamespace -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName -Location "WestUS" -State Created -EnableAutoInflate -MaximumThroughputUnits 10

Name                   : MyNamespaceName
Id                     : /subscriptions/{subscriptionId}/resourceGroups/Default-EventHub-WestCentralUS/providers/Microsoft.EventHub/namespaces/MyNamespaceName
ResourceGroup          : Default-EventHub-WestCentralUS
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
KafkaEnabled           : True
IsAutoInflateEnabled   : True
MaximumThroughputUnits : 10
```

<span data-ttu-id="2e88e-113">Aktualisiert den Zustand des Namespace \` mynamespacename \` mit autopump = Enabled und MaximumThroughputUnits = 10.</span><span class="sxs-lookup"><span data-stu-id="2e88e-113">Updates the state of namespace \`MyNamespaceName\` with AutoInflate = enabled and MaximumThroughputUnits = 10</span></span>

## <span data-ttu-id="2e88e-114">Parameter</span><span class="sxs-lookup"><span data-stu-id="2e88e-114">PARAMETERS</span></span>

### <span data-ttu-id="2e88e-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2e88e-115">-DefaultProfile</span></span>
<span data-ttu-id="2e88e-116">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="2e88e-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2e88e-117">-EnableAutoInflate</span><span class="sxs-lookup"><span data-stu-id="2e88e-117">-EnableAutoInflate</span></span>
<span data-ttu-id="2e88e-118">Gibt an, ob autopump aktiviert ist</span><span class="sxs-lookup"><span data-stu-id="2e88e-118">Indicates whether AutoInflate is enabled</span></span>

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

### <span data-ttu-id="2e88e-119">-EnableKafka</span><span class="sxs-lookup"><span data-stu-id="2e88e-119">-EnableKafka</span></span>
<span data-ttu-id="2e88e-120">Aktivieren oder Deaktivieren von Kafka für Namespace</span><span class="sxs-lookup"><span data-stu-id="2e88e-120">enabling or disabling Kafka for namespace</span></span>

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

### <span data-ttu-id="2e88e-121">-Standort</span><span class="sxs-lookup"><span data-stu-id="2e88e-121">-Location</span></span>
<span data-ttu-id="2e88e-122">Speicherort des EventHub-Namespaces.</span><span class="sxs-lookup"><span data-stu-id="2e88e-122">EventHub Namespace Location.</span></span>

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

### <span data-ttu-id="2e88e-123">-MaximumThroughputUnits</span><span class="sxs-lookup"><span data-stu-id="2e88e-123">-MaximumThroughputUnits</span></span>
<span data-ttu-id="2e88e-124">Obergrenze von Durchsatz Einheiten wenn autopump aktiviert ist, sollte der Wert innerhalb von 0 bis 20 Durchsatz Einheiten liegen.</span><span class="sxs-lookup"><span data-stu-id="2e88e-124">Upper limit of throughput units when AutoInflate is enabled, value should be within 0 to 20 throughput units.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: AutoInflateParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2e88e-125">-Name</span><span class="sxs-lookup"><span data-stu-id="2e88e-125">-Name</span></span>
<span data-ttu-id="2e88e-126">Name des EventHub-Namespaces.</span><span class="sxs-lookup"><span data-stu-id="2e88e-126">EventHub Namespace Name.</span></span>

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

### <span data-ttu-id="2e88e-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2e88e-127">-ResourceGroupName</span></span>
<span data-ttu-id="2e88e-128">Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="2e88e-128">Resource Group Name.</span></span>

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

### <span data-ttu-id="2e88e-129">-SkuCapacity</span><span class="sxs-lookup"><span data-stu-id="2e88e-129">-SkuCapacity</span></span>
<span data-ttu-id="2e88e-130">Die eventhub-Durchsatz Einheiten.</span><span class="sxs-lookup"><span data-stu-id="2e88e-130">The eventhub throughput units.</span></span>

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

### <span data-ttu-id="2e88e-131">-SkuName</span><span class="sxs-lookup"><span data-stu-id="2e88e-131">-SkuName</span></span>
<span data-ttu-id="2e88e-132">Namespace-SKU-Name.</span><span class="sxs-lookup"><span data-stu-id="2e88e-132">Namespace Sku Name.</span></span>

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

### <span data-ttu-id="2e88e-133">-Bundesland</span><span class="sxs-lookup"><span data-stu-id="2e88e-133">-State</span></span>
<span data-ttu-id="2e88e-134">Deaktivieren/Aktivieren von Namespace.</span><span class="sxs-lookup"><span data-stu-id="2e88e-134">Disable/Enable Namespace.</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Commands.EventHub.Models.NamespaceState]
Parameter Sets: (All)
Aliases:
Accepted values: Unknown, Active, Disabled

Required: False
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2e88e-135">-Tag</span><span class="sxs-lookup"><span data-stu-id="2e88e-135">-Tag</span></span>
<span data-ttu-id="2e88e-136">Hashtables, die das Ressourcen-Tag darstellen.</span><span class="sxs-lookup"><span data-stu-id="2e88e-136">Hashtables which represents resource Tag.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: 6
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2e88e-137">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="2e88e-137">-Confirm</span></span>
<span data-ttu-id="2e88e-138">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="2e88e-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2e88e-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2e88e-139">-WhatIf</span></span>
<span data-ttu-id="2e88e-140">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="2e88e-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2e88e-141">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="2e88e-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2e88e-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2e88e-142">CommonParameters</span></span>
<span data-ttu-id="2e88e-143">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2e88e-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2e88e-144">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2e88e-144">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2e88e-145">Eingaben</span><span class="sxs-lookup"><span data-stu-id="2e88e-145">INPUTS</span></span>

### <span data-ttu-id="2e88e-146">System. String</span><span class="sxs-lookup"><span data-stu-id="2e88e-146">System.String</span></span>

### <span data-ttu-id="2e88e-147">System. Nullable ' 1 [[System. Int32, mscorlib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="2e88e-147">System.Nullable\`1[[System.Int32, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

### <span data-ttu-id="2e88e-148">System. Nullable ' 1 [[Microsoft. Azure. Commands. EventHub. Models. NamespaceState, Microsoft. Azure. PowerShell. Cmdlets. EventHub, Version = 1.3.0.0, Culture = neutral, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="2e88e-148">System.Nullable\`1[[Microsoft.Azure.Commands.EventHub.Models.NamespaceState, Microsoft.Azure.PowerShell.Cmdlets.EventHub, Version=1.3.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

### <span data-ttu-id="2e88e-149">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="2e88e-149">System.Collections.Hashtable</span></span>

## <span data-ttu-id="2e88e-150">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="2e88e-150">OUTPUTS</span></span>

### <span data-ttu-id="2e88e-151">Microsoft. Azure. Commands. EventHub. Models. PSNamespaceAttributes</span><span class="sxs-lookup"><span data-stu-id="2e88e-151">Microsoft.Azure.Commands.EventHub.Models.PSNamespaceAttributes</span></span>

## <span data-ttu-id="2e88e-152">Notizen</span><span class="sxs-lookup"><span data-stu-id="2e88e-152">NOTES</span></span>

## <span data-ttu-id="2e88e-153">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="2e88e-153">RELATED LINKS</span></span>
