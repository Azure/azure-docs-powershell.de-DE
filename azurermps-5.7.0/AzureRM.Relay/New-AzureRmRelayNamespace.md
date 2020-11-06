---
external help file: Microsoft.Azure.Commands.Relay.dll-Help.xml
Module Name: AzureRM
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.relay/new-azurermrelaynamespace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Relay/Commands.Relay/help/New-AzureRmRelayNamespace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Relay/Commands.Relay/help/New-AzureRmRelayNamespace.md
ms.openlocfilehash: 1eed6f722487e3c37d9d12785b07e90516406f8f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93498874"
---
# <span data-ttu-id="2f2f3-101">New-AzureRmRelayNamespace</span><span class="sxs-lookup"><span data-stu-id="2f2f3-101">New-AzureRmRelayNamespace</span></span>

## <span data-ttu-id="2f2f3-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="2f2f3-102">SYNOPSIS</span></span>
<span data-ttu-id="2f2f3-103">Erstellt einen neuen Relay-Namespace.</span><span class="sxs-lookup"><span data-stu-id="2f2f3-103">Creates a new Relay namespace.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="2f2f3-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="2f2f3-104">SYNTAX</span></span>

```
New-AzureRmRelayNamespace [-ResourceGroupName] <String> [-Name] <String> [-Location] <String>
 [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2f2f3-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="2f2f3-105">DESCRIPTION</span></span>
<span data-ttu-id="2f2f3-106">Das Cmdlet **New-AzureRmRelayNamespace** erstellt einen neuen Relay-Namespace.</span><span class="sxs-lookup"><span data-stu-id="2f2f3-106">The **New-AzureRmRelayNamespace** cmdlet creates a new Relay namespace.</span></span> <span data-ttu-id="2f2f3-107">Nach der Erstellung ist das Namespace-Ressourcen Manifest unveränderlich.</span><span class="sxs-lookup"><span data-stu-id="2f2f3-107">Once created, the namespace resource manifest is immutable.</span></span>

## <span data-ttu-id="2f2f3-108">Beispiele</span><span class="sxs-lookup"><span data-stu-id="2f2f3-108">EXAMPLES</span></span>

### <span data-ttu-id="2f2f3-109">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="2f2f3-109">Example 1</span></span>
```
PS C:\> New-AzureRmRelayNamespace -ResourceGroupName Default-ServiceBus-WestUS -NamespaceName TestNameSpace-Relay1 -Location "West US" -Tag @{Tag1="Tag1Value"}

ProvisioningState  : Succeeded
CreatedAt          : 4/12/2017 12:38:47 AM
UpdatedAt          : 4/12/2017 12:39:10 AM
ServiceBusEndpoint : https://TestNameSpace-Relay1.servicebus.windows.net:443/
MetricId           : XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX:testnamespace-relay1
Location           : West US
Tags               : {[tag1, Tag1Value]}
Id                 : /subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/Default-ServiceBus-WestUS/providers/Microsoft.Relay/namespaces/TestNameSpace-Relay1
Name               : TestNameSpace-Relay1
Type               : Microsoft.Relay/namespaces
```

<span data-ttu-id="2f2f3-110">Erstellt einen neuen Relay-Namespace innerhalb der angegebenen Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="2f2f3-110">Creates a new Relay namespace within the specified resource group.</span></span>

## <span data-ttu-id="2f2f3-111">Parameter</span><span class="sxs-lookup"><span data-stu-id="2f2f3-111">PARAMETERS</span></span>

### <span data-ttu-id="2f2f3-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2f2f3-112">-DefaultProfile</span></span>
<span data-ttu-id="2f2f3-113">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="2f2f3-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="2f2f3-114">-Standort</span><span class="sxs-lookup"><span data-stu-id="2f2f3-114">-Location</span></span>
<span data-ttu-id="2f2f3-115">Speicherort des Relay-Namespaces.</span><span class="sxs-lookup"><span data-stu-id="2f2f3-115">Relay Namespace Location.</span></span>

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

### <span data-ttu-id="2f2f3-116">-Name</span><span class="sxs-lookup"><span data-stu-id="2f2f3-116">-Name</span></span>
<span data-ttu-id="2f2f3-117">Name des Relay-Namespaces</span><span class="sxs-lookup"><span data-stu-id="2f2f3-117">Relay Namespace Name</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2f2f3-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2f2f3-118">-ResourceGroupName</span></span>
<span data-ttu-id="2f2f3-119">Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="2f2f3-119">Resource Group Name.</span></span>

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

### <span data-ttu-id="2f2f3-120">-Tag</span><span class="sxs-lookup"><span data-stu-id="2f2f3-120">-Tag</span></span>
<span data-ttu-id="2f2f3-121">Schlüssel-Wert-Paare in Form einer Hashtabelle</span><span class="sxs-lookup"><span data-stu-id="2f2f3-121">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="2f2f3-122">Zum Beispiel:</span><span class="sxs-lookup"><span data-stu-id="2f2f3-122">For example:</span></span>

<span data-ttu-id="2f2f3-123">@ {KEY0 = "value0"; key1 = $NULL; key2 = "Value2"}</span><span class="sxs-lookup"><span data-stu-id="2f2f3-123">@{key0="value0";key1=$null;key2="value2"}</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2f2f3-124">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="2f2f3-124">-Confirm</span></span>
<span data-ttu-id="2f2f3-125">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="2f2f3-125">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2f2f3-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2f2f3-126">-WhatIf</span></span>
<span data-ttu-id="2f2f3-127">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="2f2f3-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2f2f3-128">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="2f2f3-128">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2f2f3-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2f2f3-129">CommonParameters</span></span>
<span data-ttu-id="2f2f3-130">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2f2f3-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2f2f3-131">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2f2f3-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2f2f3-132">Eingaben</span><span class="sxs-lookup"><span data-stu-id="2f2f3-132">INPUTS</span></span>

### <span data-ttu-id="2f2f3-133">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2f2f3-133">-ResourceGroupName</span></span>
 <span data-ttu-id="2f2f3-134">System. String</span><span class="sxs-lookup"><span data-stu-id="2f2f3-134">System.String</span></span>

### <span data-ttu-id="2f2f3-135">-Namespacename</span><span class="sxs-lookup"><span data-stu-id="2f2f3-135">-NamespaceName</span></span>
 <span data-ttu-id="2f2f3-136">System. String</span><span class="sxs-lookup"><span data-stu-id="2f2f3-136">System.String</span></span>

### <span data-ttu-id="2f2f3-137">-Standort</span><span class="sxs-lookup"><span data-stu-id="2f2f3-137">-Location</span></span>
 <span data-ttu-id="2f2f3-138">System. String</span><span class="sxs-lookup"><span data-stu-id="2f2f3-138">System.String</span></span>

### <span data-ttu-id="2f2f3-139">-SkuName</span><span class="sxs-lookup"><span data-stu-id="2f2f3-139">-SkuName</span></span>
 <span data-ttu-id="2f2f3-140">System. String</span><span class="sxs-lookup"><span data-stu-id="2f2f3-140">System.String</span></span>

### <span data-ttu-id="2f2f3-141">-Tag</span><span class="sxs-lookup"><span data-stu-id="2f2f3-141">-Tag</span></span>
 <span data-ttu-id="2f2f3-142">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="2f2f3-142">System.Collections.Hashtable</span></span>

## <span data-ttu-id="2f2f3-143">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="2f2f3-143">OUTPUTS</span></span>

### <span data-ttu-id="2f2f3-144">Microsoft. Azure. Commands. Relay. Models. RelayNamespaceAttributes</span><span class="sxs-lookup"><span data-stu-id="2f2f3-144">Microsoft.Azure.Commands.Relay.Models.RelayNamespaceAttributes</span></span>

## <span data-ttu-id="2f2f3-145">Notizen</span><span class="sxs-lookup"><span data-stu-id="2f2f3-145">NOTES</span></span>

## <span data-ttu-id="2f2f3-146">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="2f2f3-146">RELATED LINKS</span></span>

