---
external help file: Microsoft.Azure.Commands.EventHub.dll-Help.xml
Module Name: AzureRM.EventHub
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.eventhub/new-azurermeventhubnamespace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/New-AzureRmEventHubNamespace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/New-AzureRmEventHubNamespace.md
ms.openlocfilehash: 2d944b629a72a8b97bf1bd639ced79d9bd1eab02
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93499853"
---
# <span data-ttu-id="92de2-101">New-AzureRmEventHubNamespace</span><span class="sxs-lookup"><span data-stu-id="92de2-101">New-AzureRmEventHubNamespace</span></span>

## <span data-ttu-id="92de2-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="92de2-102">SYNOPSIS</span></span>
<span data-ttu-id="92de2-103">Erstellt einen Event Hubs-Namespace.</span><span class="sxs-lookup"><span data-stu-id="92de2-103">Creates an Event Hubs namespace.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="92de2-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="92de2-104">SYNTAX</span></span>

### <span data-ttu-id="92de2-105">NamespaceParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="92de2-105">NamespaceParameterSet (Default)</span></span>
```
New-AzureRmEventHubNamespace [-ResourceGroupName] <String> [-Name] <String> [-Location] <String>
 [[-SkuName] <String>] [[-SkuCapacity] <Int32>] [[-Tag] <Hashtable>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="92de2-106">AutoInflateParameterSet</span><span class="sxs-lookup"><span data-stu-id="92de2-106">AutoInflateParameterSet</span></span>
```
New-AzureRmEventHubNamespace [-ResourceGroupName] <String> [-Name] <String> [-Location] <String>
 [[-SkuName] <String>] [[-SkuCapacity] <Int32>] [[-Tag] <Hashtable>] [-EnableAutoInflate]
 [[-MaximumThroughputUnits] <Int32>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="92de2-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="92de2-107">DESCRIPTION</span></span>
<span data-ttu-id="92de2-108">Das New-AzureRmEventHubNamespace-Cmdlet erstellt einen neuen Namespace vom Typ Event Hubs.</span><span class="sxs-lookup"><span data-stu-id="92de2-108">The New-AzureRmEventHubNamespace cmdlet creates a new namespace of type Event Hubs.</span></span>

## <span data-ttu-id="92de2-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="92de2-109">EXAMPLES</span></span>

### <span data-ttu-id="92de2-110">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="92de2-110">Example 1</span></span>
```
PS C:\> New-AzureRmEventHubNamespace -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName -Location MyLocation
```

<span data-ttu-id="92de2-111">Erstellt einen Event Hubs \` -Namespace mynamespacename am \` angegebenen geografischen Standort \` mylocation \` in der Ressourcengruppe \` MyResourceGroupName \` .</span><span class="sxs-lookup"><span data-stu-id="92de2-111">Creates an Event Hubs namespace \`MyNamespaceName\` in the specified geographic location \`MyLocation\`, in resource group \`MyResourceGroupName\`.</span></span>

### <span data-ttu-id="92de2-112">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="92de2-112">Example 2</span></span>
```
PS C:\> New-AzureRmEventHubNamespace -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName -Location MyLocation -EnableAutoInflate -MaximumThroughputUnits 10
```

<span data-ttu-id="92de2-113">Erstellt einen Event Hubs-Namespace \` mynamespacename am \` angegebenen geografischen Standort \` mylocation \` , in der Ressourcengruppe \` MyResourceGroupName \` und autopump ist mit MaximumThroughputUnits 10 aktiviert.</span><span class="sxs-lookup"><span data-stu-id="92de2-113">Creates an Event Hubs namespace \`MyNamespaceName\` in the specified geographic location \`MyLocation\`, in resource group \`MyResourceGroupName\` and AutoInflate is enabled with MaximumThroughputUnits 10.</span></span>

## <span data-ttu-id="92de2-114">Parameter</span><span class="sxs-lookup"><span data-stu-id="92de2-114">PARAMETERS</span></span>

### <span data-ttu-id="92de2-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="92de2-115">-DefaultProfile</span></span>
<span data-ttu-id="92de2-116">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="92de2-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="92de2-117">-EnableAutoInflate</span><span class="sxs-lookup"><span data-stu-id="92de2-117">-EnableAutoInflate</span></span>
<span data-ttu-id="92de2-118">Gibt an, ob autopump aktiviert ist</span><span class="sxs-lookup"><span data-stu-id="92de2-118">Indicates whether AutoInflate is enabled</span></span>

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

### <span data-ttu-id="92de2-119">-Standort</span><span class="sxs-lookup"><span data-stu-id="92de2-119">-Location</span></span>
<span data-ttu-id="92de2-120">Speicherort des EventHub-Namespaces.</span><span class="sxs-lookup"><span data-stu-id="92de2-120">EventHub Namespace Location.</span></span>

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

### <span data-ttu-id="92de2-121">-MaximumThroughputUnits</span><span class="sxs-lookup"><span data-stu-id="92de2-121">-MaximumThroughputUnits</span></span>
<span data-ttu-id="92de2-122">Obergrenze von Durchsatz Einheiten wenn autopump aktiviert ist, sollte der Wert innerhalb von 0 bis 20 Durchsatz Einheiten liegen.</span><span class="sxs-lookup"><span data-stu-id="92de2-122">Upper limit of throughput units when AutoInflate is enabled, value should be within 0 to 20 throughput units.</span></span>

```yaml
Type: Int32
Parameter Sets: AutoInflateParameterSet
Aliases:

Required: False
Position: 7
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="92de2-123">-Name</span><span class="sxs-lookup"><span data-stu-id="92de2-123">-Name</span></span>
<span data-ttu-id="92de2-124">Name des EventHub-Namespaces.</span><span class="sxs-lookup"><span data-stu-id="92de2-124">EventHub Namespace Name.</span></span>

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

### <span data-ttu-id="92de2-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="92de2-125">-ResourceGroupName</span></span>
<span data-ttu-id="92de2-126">Ressourcengruppen Name</span><span class="sxs-lookup"><span data-stu-id="92de2-126">Resource Group Name</span></span>

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

### <span data-ttu-id="92de2-127">-SkuCapacity</span><span class="sxs-lookup"><span data-stu-id="92de2-127">-SkuCapacity</span></span>
<span data-ttu-id="92de2-128">Die eventhub-Durchsatz Einheiten.</span><span class="sxs-lookup"><span data-stu-id="92de2-128">The eventhub throughput units.</span></span>

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

### <span data-ttu-id="92de2-129">-SkuName</span><span class="sxs-lookup"><span data-stu-id="92de2-129">-SkuName</span></span>
<span data-ttu-id="92de2-130">Namespace-SKU-Name.</span><span class="sxs-lookup"><span data-stu-id="92de2-130">Namespace Sku Name.</span></span>

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

### <span data-ttu-id="92de2-131">-Tag</span><span class="sxs-lookup"><span data-stu-id="92de2-131">-Tag</span></span>
<span data-ttu-id="92de2-132">Hashtables, die Ressourcen Tags darstellen.</span><span class="sxs-lookup"><span data-stu-id="92de2-132">Hashtables which represents resource Tags.</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="92de2-133">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="92de2-133">-Confirm</span></span>
<span data-ttu-id="92de2-134">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="92de2-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="92de2-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="92de2-135">-WhatIf</span></span>
<span data-ttu-id="92de2-136">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="92de2-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="92de2-137">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="92de2-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="92de2-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="92de2-138">CommonParameters</span></span>
<span data-ttu-id="92de2-139">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="92de2-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="92de2-140">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="92de2-140">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="92de2-141">Eingaben</span><span class="sxs-lookup"><span data-stu-id="92de2-141">INPUTS</span></span>

### <span data-ttu-id="92de2-142">System. String</span><span class="sxs-lookup"><span data-stu-id="92de2-142">System.String</span></span>
<span data-ttu-id="92de2-143">System. Nullable ' 1 [[System. Int32, mscorlib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = b77a5c561934e089]] System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="92de2-143">System.Nullable\`1[[System.Int32, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]] System.Collections.Hashtable</span></span>


## <span data-ttu-id="92de2-144">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="92de2-144">OUTPUTS</span></span>

### <span data-ttu-id="92de2-145">Microsoft. Azure. Commands. EventHub. Models. PSNamespaceAttributes</span><span class="sxs-lookup"><span data-stu-id="92de2-145">Microsoft.Azure.Commands.EventHub.Models.PSNamespaceAttributes</span></span>


## <span data-ttu-id="92de2-146">Notizen</span><span class="sxs-lookup"><span data-stu-id="92de2-146">NOTES</span></span>

## <span data-ttu-id="92de2-147">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="92de2-147">RELATED LINKS</span></span>
