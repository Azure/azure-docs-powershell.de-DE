---
external help file: Microsoft.Azure.Commands.EventHub.dll-Help.xml
Module Name: AzureRM.EventHub
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.eventhub/set-azurermeventhubnamespace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/Set-AzureRmEventHubNamespace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/Set-AzureRmEventHubNamespace.md
ms.openlocfilehash: 739d027d095810ae33f90a7b5cc1ad7caf148081
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93482962"
---
# <span data-ttu-id="fb4d4-101">Set-AzureRmEventHubNamespace</span><span class="sxs-lookup"><span data-stu-id="fb4d4-101">Set-AzureRmEventHubNamespace</span></span>

## <span data-ttu-id="fb4d4-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="fb4d4-102">SYNOPSIS</span></span>
<span data-ttu-id="fb4d4-103">Aktualisiert den angegebenen Event Hubs-Namespace.</span><span class="sxs-lookup"><span data-stu-id="fb4d4-103">Updates the specified Event Hubs namespace.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="fb4d4-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="fb4d4-104">SYNTAX</span></span>

### <span data-ttu-id="fb4d4-105">NamespaceParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="fb4d4-105">NamespaceParameterSet (Default)</span></span>
```
Set-AzureRmEventHubNamespace [-ResourceGroupName] <String> [-Name] <String> [-Location] <String>
 [[-SkuName] <String>] [[-SkuCapacity] <Int32>] [[-State] <NamespaceState>] [[-Tag] <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fb4d4-106">AutoInflateParameterSet</span><span class="sxs-lookup"><span data-stu-id="fb4d4-106">AutoInflateParameterSet</span></span>
```
Set-AzureRmEventHubNamespace [-ResourceGroupName] <String> [-Name] <String> [-Location] <String>
 [[-SkuName] <String>] [[-SkuCapacity] <Int32>] [[-State] <NamespaceState>] [[-Tag] <Hashtable>]
 [-EnableAutoInflate] [-MaximumThroughputUnits <Int32>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="fb4d4-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="fb4d4-107">DESCRIPTION</span></span>
<span data-ttu-id="fb4d4-108">Das Set-AzureRmEventHubNamespace-Cmdlet aktualisiert die Eigenschaften des angegebenen Event Hubs-Namespace.</span><span class="sxs-lookup"><span data-stu-id="fb4d4-108">The Set-AzureRmEventHubNamespace cmdlet updates the properties of the specified Event Hubs namespace.</span></span>

## <span data-ttu-id="fb4d4-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="fb4d4-109">EXAMPLES</span></span>

### <span data-ttu-id="fb4d4-110">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="fb4d4-110">Example 1</span></span>
```
PS C:\> Set-AzureRmEventHubNamespace -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName -Location "WestUS" -State Created
```

<span data-ttu-id="fb4d4-111">Aktualisiert den Zustand des Namespaces \` mynamespacename \` auf created.</span><span class="sxs-lookup"><span data-stu-id="fb4d4-111">Updates the state of namespace \`MyNamespaceName\` to Created .</span></span>

### <span data-ttu-id="fb4d4-112">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="fb4d4-112">Example 2</span></span>
```
PS C:\> Set-AzureRmEventHubNamespace -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName -Location "WestUS" -State Created -EnableAutoInflate -MaximumThroughputUnits 10
```

<span data-ttu-id="fb4d4-113">Aktualisiert den Zustand des Namespace \` mynamespacename \` mit autopump = Enabled und MaximumThroughputUnits = 10.</span><span class="sxs-lookup"><span data-stu-id="fb4d4-113">Updates the state of namespace \`MyNamespaceName\` with AutoInflate = enabled and MaximumThroughputUnits = 10</span></span>

## <span data-ttu-id="fb4d4-114">Parameter</span><span class="sxs-lookup"><span data-stu-id="fb4d4-114">PARAMETERS</span></span>

### <span data-ttu-id="fb4d4-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fb4d4-115">-DefaultProfile</span></span>
<span data-ttu-id="fb4d4-116">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="fb4d4-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fb4d4-117">-EnableAutoInflate</span><span class="sxs-lookup"><span data-stu-id="fb4d4-117">-EnableAutoInflate</span></span>
<span data-ttu-id="fb4d4-118">Gibt an, ob autopump aktiviert ist</span><span class="sxs-lookup"><span data-stu-id="fb4d4-118">Indicates whether AutoInflate is enabled</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: AutoInflateParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fb4d4-119">-Standort</span><span class="sxs-lookup"><span data-stu-id="fb4d4-119">-Location</span></span>
<span data-ttu-id="fb4d4-120">Speicherort des EventHub-Namespaces.</span><span class="sxs-lookup"><span data-stu-id="fb4d4-120">EventHub Namespace Location.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fb4d4-121">-MaximumThroughputUnits</span><span class="sxs-lookup"><span data-stu-id="fb4d4-121">-MaximumThroughputUnits</span></span>
<span data-ttu-id="fb4d4-122">Obergrenze von Durchsatz Einheiten wenn autopump aktiviert ist, sollte der Wert innerhalb von 0 bis 20 Durchsatz Einheiten liegen.</span><span class="sxs-lookup"><span data-stu-id="fb4d4-122">Upper limit of throughput units when AutoInflate is enabled, value should be within 0 to 20 throughput units.</span></span>

```yaml
Type: Int32
Parameter Sets: AutoInflateParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fb4d4-123">-Name</span><span class="sxs-lookup"><span data-stu-id="fb4d4-123">-Name</span></span>
<span data-ttu-id="fb4d4-124">Name des EventHub-Namespaces.</span><span class="sxs-lookup"><span data-stu-id="fb4d4-124">EventHub Namespace Name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: NamespaceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fb4d4-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fb4d4-125">-ResourceGroupName</span></span>
<span data-ttu-id="fb4d4-126">Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="fb4d4-126">Resource Group Name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fb4d4-127">-SkuCapacity</span><span class="sxs-lookup"><span data-stu-id="fb4d4-127">-SkuCapacity</span></span>
<span data-ttu-id="fb4d4-128">Die eventhub-Durchsatz Einheiten.</span><span class="sxs-lookup"><span data-stu-id="fb4d4-128">The eventhub throughput units.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fb4d4-129">-SkuName</span><span class="sxs-lookup"><span data-stu-id="fb4d4-129">-SkuName</span></span>
<span data-ttu-id="fb4d4-130">Namespace-SKU-Name.</span><span class="sxs-lookup"><span data-stu-id="fb4d4-130">Namespace Sku Name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:
Accepted values: Basic, Standard, Premium

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fb4d4-131">-Bundesland</span><span class="sxs-lookup"><span data-stu-id="fb4d4-131">-State</span></span>
<span data-ttu-id="fb4d4-132">Deaktivieren/Aktivieren von Namespace.</span><span class="sxs-lookup"><span data-stu-id="fb4d4-132">Disable/Enable Namespace.</span></span>

```yaml
Type: NamespaceState
Parameter Sets: (All)
Aliases:
Accepted values: Unknown, Active, Disabled

Required: False
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fb4d4-133">-Tag</span><span class="sxs-lookup"><span data-stu-id="fb4d4-133">-Tag</span></span>
<span data-ttu-id="fb4d4-134">Hashtables, die das Ressourcen-Tag darstellen.</span><span class="sxs-lookup"><span data-stu-id="fb4d4-134">Hashtables which represents resource Tag.</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: 6
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fb4d4-135">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="fb4d4-135">-Confirm</span></span>
<span data-ttu-id="fb4d4-136">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="fb4d4-136">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fb4d4-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fb4d4-137">-WhatIf</span></span>
<span data-ttu-id="fb4d4-138">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="fb4d4-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="fb4d4-139">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="fb4d4-139">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fb4d4-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fb4d4-140">CommonParameters</span></span>
<span data-ttu-id="fb4d4-141">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fb4d4-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="fb4d4-142">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fb4d4-142">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fb4d4-143">Eingaben</span><span class="sxs-lookup"><span data-stu-id="fb4d4-143">INPUTS</span></span>

### <span data-ttu-id="fb4d4-144">System. String</span><span class="sxs-lookup"><span data-stu-id="fb4d4-144">System.String</span></span>
<span data-ttu-id="fb4d4-145">System. Nullable `1[[System.Int32, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]
System.Nullable` 1 [[Microsoft. Azure. Commands. EventHub. Models. NamespaceState, Microsoft. Azure. Commands. EventHub, Version = 0.5.0.0, Culture = neutral, PublicKeyToken = null]] System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="fb4d4-145">System.Nullable`1[[System.Int32, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]
System.Nullable`1[[Microsoft.Azure.Commands.EventHub.Models.NamespaceState, Microsoft.Azure.Commands.EventHub, Version=0.5.0.0, Culture=neutral, PublicKeyToken=null]] System.Collections.Hashtable</span></span>


## <span data-ttu-id="fb4d4-146">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="fb4d4-146">OUTPUTS</span></span>

### <span data-ttu-id="fb4d4-147">Microsoft. Azure. Commands. EventHub. Models. PSNamespaceAttributes</span><span class="sxs-lookup"><span data-stu-id="fb4d4-147">Microsoft.Azure.Commands.EventHub.Models.PSNamespaceAttributes</span></span>


## <span data-ttu-id="fb4d4-148">Notizen</span><span class="sxs-lookup"><span data-stu-id="fb4d4-148">NOTES</span></span>

## <span data-ttu-id="fb4d4-149">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="fb4d4-149">RELATED LINKS</span></span>
