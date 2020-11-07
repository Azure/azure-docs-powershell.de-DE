---
external help file: Microsoft.Azure.Commands.Relay.dll-Help.xml
Module Name: AzureRM.Relay
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Relay/Commands.Relay/help/New-AzureRmRelayNamespace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Relay/Commands.Relay/help/New-AzureRmRelayNamespace.md
ms.openlocfilehash: 365a80e1ddf5673be5c45c5d17b24490c277a365
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93663842"
---
# <span data-ttu-id="824e7-101">New-AzureRmRelayNamespace</span><span class="sxs-lookup"><span data-stu-id="824e7-101">New-AzureRmRelayNamespace</span></span>

## <span data-ttu-id="824e7-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="824e7-102">SYNOPSIS</span></span>
<span data-ttu-id="824e7-103">Erstellt einen neuen Relay-Namespace.</span><span class="sxs-lookup"><span data-stu-id="824e7-103">Creates a new Relay namespace.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="824e7-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="824e7-104">SYNTAX</span></span>

```
New-AzureRmRelayNamespace [-ResourceGroupName] <String> -Name <String> [-Location] <String> [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="824e7-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="824e7-105">DESCRIPTION</span></span>
<span data-ttu-id="824e7-106">Das Cmdlet **New-AzureRmRelayNamespace** erstellt einen neuen Relay-Namespace.</span><span class="sxs-lookup"><span data-stu-id="824e7-106">The **New-AzureRmRelayNamespace** cmdlet creates a new Relay namespace.</span></span> <span data-ttu-id="824e7-107">Nach der Erstellung ist das Namespace-Ressourcen Manifest unveränderlich.</span><span class="sxs-lookup"><span data-stu-id="824e7-107">Once created, the namespace resource manifest is immutable.</span></span>

## <span data-ttu-id="824e7-108">Beispiele</span><span class="sxs-lookup"><span data-stu-id="824e7-108">EXAMPLES</span></span>

### <span data-ttu-id="824e7-109">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="824e7-109">Example 1</span></span>
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

<span data-ttu-id="824e7-110">Erstellt einen neuen Relay-Namespace innerhalb der angegebenen Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="824e7-110">Creates a new Relay namespace within the specified resource group.</span></span>

## <span data-ttu-id="824e7-111">Parameter</span><span class="sxs-lookup"><span data-stu-id="824e7-111">PARAMETERS</span></span>

### <span data-ttu-id="824e7-112">-Standort</span><span class="sxs-lookup"><span data-stu-id="824e7-112">-Location</span></span>
<span data-ttu-id="824e7-113">Speicherort des Relay-Namespaces.</span><span class="sxs-lookup"><span data-stu-id="824e7-113">Relay Namespace Location.</span></span>

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

### <span data-ttu-id="824e7-114">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="824e7-114">-ResourceGroupName</span></span>
<span data-ttu-id="824e7-115">Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="824e7-115">Resource Group Name.</span></span>

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

### <span data-ttu-id="824e7-116">-Tag</span><span class="sxs-lookup"><span data-stu-id="824e7-116">-Tag</span></span>
<span data-ttu-id="824e7-117">Schlüssel-Wert-Paare in Form einer Hashtabelle</span><span class="sxs-lookup"><span data-stu-id="824e7-117">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="824e7-118">Zum Beispiel:</span><span class="sxs-lookup"><span data-stu-id="824e7-118">For example:</span></span>

<span data-ttu-id="824e7-119">@ {KEY0 = "value0"; key1 = $NULL; key2 = "Value2"}</span><span class="sxs-lookup"><span data-stu-id="824e7-119">@{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="824e7-120">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="824e7-120">-Confirm</span></span>
<span data-ttu-id="824e7-121">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="824e7-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="824e7-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="824e7-122">-WhatIf</span></span>
<span data-ttu-id="824e7-123">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="824e7-123">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="824e7-124">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="824e7-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="824e7-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="824e7-125">-DefaultProfile</span></span>
<span data-ttu-id="824e7-126">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="824e7-126">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="824e7-127">-Name</span><span class="sxs-lookup"><span data-stu-id="824e7-127">-Name</span></span>
<span data-ttu-id="824e7-128">Name des Relay-Namespaces.</span><span class="sxs-lookup"><span data-stu-id="824e7-128">Relay Namespace Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="824e7-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="824e7-129">CommonParameters</span></span>
<span data-ttu-id="824e7-130">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="824e7-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="824e7-131">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="824e7-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="824e7-132">Eingaben</span><span class="sxs-lookup"><span data-stu-id="824e7-132">INPUTS</span></span>

### <span data-ttu-id="824e7-133">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="824e7-133">-ResourceGroupName</span></span>
 <span data-ttu-id="824e7-134">System. String</span><span class="sxs-lookup"><span data-stu-id="824e7-134">System.String</span></span>

### <span data-ttu-id="824e7-135">-Namespacename</span><span class="sxs-lookup"><span data-stu-id="824e7-135">-NamespaceName</span></span>
 <span data-ttu-id="824e7-136">System. String</span><span class="sxs-lookup"><span data-stu-id="824e7-136">System.String</span></span>

### <span data-ttu-id="824e7-137">-Standort</span><span class="sxs-lookup"><span data-stu-id="824e7-137">-Location</span></span>
 <span data-ttu-id="824e7-138">System. String</span><span class="sxs-lookup"><span data-stu-id="824e7-138">System.String</span></span>

### <span data-ttu-id="824e7-139">-SkuName</span><span class="sxs-lookup"><span data-stu-id="824e7-139">-SkuName</span></span>
 <span data-ttu-id="824e7-140">System. String</span><span class="sxs-lookup"><span data-stu-id="824e7-140">System.String</span></span>

### <span data-ttu-id="824e7-141">-Tag</span><span class="sxs-lookup"><span data-stu-id="824e7-141">-Tag</span></span>
 <span data-ttu-id="824e7-142">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="824e7-142">System.Collections.Hashtable</span></span>

## <span data-ttu-id="824e7-143">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="824e7-143">OUTPUTS</span></span>

### <span data-ttu-id="824e7-144">Microsoft. Azure. Commands. Relay. Models. RelayNamespaceAttributes</span><span class="sxs-lookup"><span data-stu-id="824e7-144">Microsoft.Azure.Commands.Relay.Models.RelayNamespaceAttributes</span></span>

## <span data-ttu-id="824e7-145">Notizen</span><span class="sxs-lookup"><span data-stu-id="824e7-145">NOTES</span></span>

## <span data-ttu-id="824e7-146">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="824e7-146">RELATED LINKS</span></span>

