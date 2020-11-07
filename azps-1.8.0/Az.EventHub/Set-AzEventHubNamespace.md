---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventHub.dll-Help.xml
Module Name: Az.EventHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.eventhub/set-azeventhubnamespace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Set-AzEventHubNamespace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Set-AzEventHubNamespace.md
ms.openlocfilehash: c75b456021368ea72a72bd0b0fea07a0f13d06dd
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93661015"
---
# <span data-ttu-id="1f99d-101">Set-AzEventHubNamespace</span><span class="sxs-lookup"><span data-stu-id="1f99d-101">Set-AzEventHubNamespace</span></span>

## <span data-ttu-id="1f99d-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="1f99d-102">SYNOPSIS</span></span>
<span data-ttu-id="1f99d-103">Aktualisiert den angegebenen Event Hubs-Namespace.</span><span class="sxs-lookup"><span data-stu-id="1f99d-103">Updates the specified Event Hubs namespace.</span></span>

## <span data-ttu-id="1f99d-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="1f99d-104">SYNTAX</span></span>

### <span data-ttu-id="1f99d-105">NamespaceParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="1f99d-105">NamespaceParameterSet (Default)</span></span>
```
Set-AzEventHubNamespace [-ResourceGroupName] <String> [-Name] <String> [-Location] <String>
 [[-SkuName] <String>] [[-SkuCapacity] <Int32>] [[-State] <NamespaceState>] [[-Tag] <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1f99d-106">AutoInflateParameterSet</span><span class="sxs-lookup"><span data-stu-id="1f99d-106">AutoInflateParameterSet</span></span>
```
Set-AzEventHubNamespace [-ResourceGroupName] <String> [-Name] <String> [-Location] <String>
 [[-SkuName] <String>] [[-SkuCapacity] <Int32>] [[-State] <NamespaceState>] [[-Tag] <Hashtable>]
 [-EnableAutoInflate] [-MaximumThroughputUnits <Int32>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1f99d-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="1f99d-107">DESCRIPTION</span></span>
<span data-ttu-id="1f99d-108">Das Set-AzEventHubNamespace-Cmdlet aktualisiert die Eigenschaften des angegebenen Event Hubs-Namespace.</span><span class="sxs-lookup"><span data-stu-id="1f99d-108">The Set-AzEventHubNamespace cmdlet updates the properties of the specified Event Hubs namespace.</span></span>

## <span data-ttu-id="1f99d-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="1f99d-109">EXAMPLES</span></span>

### <span data-ttu-id="1f99d-110">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="1f99d-110">Example 1</span></span>
```
PS C:\> Set-AzEventHubNamespace -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName -Location "WestUS" -State Created
```

<span data-ttu-id="1f99d-111">Aktualisiert den Zustand des Namespaces \` mynamespacename \` auf created.</span><span class="sxs-lookup"><span data-stu-id="1f99d-111">Updates the state of namespace \`MyNamespaceName\` to Created .</span></span>

### <span data-ttu-id="1f99d-112">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="1f99d-112">Example 2</span></span>
```
PS C:\> Set-AzEventHubNamespace -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName -Location "WestUS" -State Created -EnableAutoInflate -MaximumThroughputUnits 10
```

<span data-ttu-id="1f99d-113">Aktualisiert den Zustand des Namespace \` mynamespacename \` mit autopump = Enabled und MaximumThroughputUnits = 10.</span><span class="sxs-lookup"><span data-stu-id="1f99d-113">Updates the state of namespace \`MyNamespaceName\` with AutoInflate = enabled and MaximumThroughputUnits = 10</span></span>

## <span data-ttu-id="1f99d-114">Parameter</span><span class="sxs-lookup"><span data-stu-id="1f99d-114">PARAMETERS</span></span>

### <span data-ttu-id="1f99d-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1f99d-115">-DefaultProfile</span></span>
<span data-ttu-id="1f99d-116">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="1f99d-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1f99d-117">-EnableAutoInflate</span><span class="sxs-lookup"><span data-stu-id="1f99d-117">-EnableAutoInflate</span></span>
<span data-ttu-id="1f99d-118">Gibt an, ob autopump aktiviert ist</span><span class="sxs-lookup"><span data-stu-id="1f99d-118">Indicates whether AutoInflate is enabled</span></span>

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

### <span data-ttu-id="1f99d-119">-Standort</span><span class="sxs-lookup"><span data-stu-id="1f99d-119">-Location</span></span>
<span data-ttu-id="1f99d-120">Speicherort des EventHub-Namespaces.</span><span class="sxs-lookup"><span data-stu-id="1f99d-120">EventHub Namespace Location.</span></span>

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

### <span data-ttu-id="1f99d-121">-MaximumThroughputUnits</span><span class="sxs-lookup"><span data-stu-id="1f99d-121">-MaximumThroughputUnits</span></span>
<span data-ttu-id="1f99d-122">Obergrenze von Durchsatz Einheiten wenn autopump aktiviert ist, sollte der Wert innerhalb von 0 bis 20 Durchsatz Einheiten liegen.</span><span class="sxs-lookup"><span data-stu-id="1f99d-122">Upper limit of throughput units when AutoInflate is enabled, value should be within 0 to 20 throughput units.</span></span>

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

### <span data-ttu-id="1f99d-123">-Name</span><span class="sxs-lookup"><span data-stu-id="1f99d-123">-Name</span></span>
<span data-ttu-id="1f99d-124">Name des EventHub-Namespaces.</span><span class="sxs-lookup"><span data-stu-id="1f99d-124">EventHub Namespace Name.</span></span>

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

### <span data-ttu-id="1f99d-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1f99d-125">-ResourceGroupName</span></span>
<span data-ttu-id="1f99d-126">Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="1f99d-126">Resource Group Name.</span></span>

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

### <span data-ttu-id="1f99d-127">-SkuCapacity</span><span class="sxs-lookup"><span data-stu-id="1f99d-127">-SkuCapacity</span></span>
<span data-ttu-id="1f99d-128">Die eventhub-Durchsatz Einheiten.</span><span class="sxs-lookup"><span data-stu-id="1f99d-128">The eventhub throughput units.</span></span>

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

### <span data-ttu-id="1f99d-129">-SkuName</span><span class="sxs-lookup"><span data-stu-id="1f99d-129">-SkuName</span></span>
<span data-ttu-id="1f99d-130">Namespace-SKU-Name.</span><span class="sxs-lookup"><span data-stu-id="1f99d-130">Namespace Sku Name.</span></span>

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

### <span data-ttu-id="1f99d-131">-Bundesland</span><span class="sxs-lookup"><span data-stu-id="1f99d-131">-State</span></span>
<span data-ttu-id="1f99d-132">Deaktivieren/Aktivieren von Namespace.</span><span class="sxs-lookup"><span data-stu-id="1f99d-132">Disable/Enable Namespace.</span></span>

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

### <span data-ttu-id="1f99d-133">-Tag</span><span class="sxs-lookup"><span data-stu-id="1f99d-133">-Tag</span></span>
<span data-ttu-id="1f99d-134">Hashtables, die das Ressourcen-Tag darstellen.</span><span class="sxs-lookup"><span data-stu-id="1f99d-134">Hashtables which represents resource Tag.</span></span>

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

### <span data-ttu-id="1f99d-135">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="1f99d-135">-Confirm</span></span>
<span data-ttu-id="1f99d-136">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="1f99d-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1f99d-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1f99d-137">-WhatIf</span></span>
<span data-ttu-id="1f99d-138">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="1f99d-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1f99d-139">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="1f99d-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1f99d-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1f99d-140">CommonParameters</span></span>
<span data-ttu-id="1f99d-141">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1f99d-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1f99d-142">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1f99d-142">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1f99d-143">Eingaben</span><span class="sxs-lookup"><span data-stu-id="1f99d-143">INPUTS</span></span>

### <span data-ttu-id="1f99d-144">System. String</span><span class="sxs-lookup"><span data-stu-id="1f99d-144">System.String</span></span>

### <span data-ttu-id="1f99d-145">System. Nullable ' 1 [[System. Int32, System. private. CoreLib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="1f99d-145">System.Nullable\`1[[System.Int32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="1f99d-146">System. Nullable ' 1 [[Microsoft. Azure. Commands. EventHub. Models. NamespaceState, Microsoft. Azure. PowerShell. Cmdlets. EventHub, Version = 1.0.0.0, Culture = neutral, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="1f99d-146">System.Nullable\`1[[Microsoft.Azure.Commands.EventHub.Models.NamespaceState, Microsoft.Azure.PowerShell.Cmdlets.EventHub, Version=1.0.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

### <span data-ttu-id="1f99d-147">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="1f99d-147">System.Collections.Hashtable</span></span>

## <span data-ttu-id="1f99d-148">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="1f99d-148">OUTPUTS</span></span>

### <span data-ttu-id="1f99d-149">Microsoft. Azure. Commands. EventHub. Models. PSNamespaceAttributes</span><span class="sxs-lookup"><span data-stu-id="1f99d-149">Microsoft.Azure.Commands.EventHub.Models.PSNamespaceAttributes</span></span>

## <span data-ttu-id="1f99d-150">Notizen</span><span class="sxs-lookup"><span data-stu-id="1f99d-150">NOTES</span></span>

## <span data-ttu-id="1f99d-151">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="1f99d-151">RELATED LINKS</span></span>
