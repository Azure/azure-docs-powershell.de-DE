---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Relay.dll-Help.xml
Module Name: Az.Relay
online version: https://docs.microsoft.com/en-us/powershell/module/az.relay/new-azrelaynamespace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Relay/Relay/help/New-AzRelayNamespace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Relay/Relay/help/New-AzRelayNamespace.md
ms.openlocfilehash: c99bea4bb2f5ce9a404f828a3694136882cbefde
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/21/2020
ms.locfileid: "93846864"
---
# <span data-ttu-id="9c5ab-101">New-AzRelayNamespace</span><span class="sxs-lookup"><span data-stu-id="9c5ab-101">New-AzRelayNamespace</span></span>

## <span data-ttu-id="9c5ab-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="9c5ab-102">SYNOPSIS</span></span>
<span data-ttu-id="9c5ab-103">Erstellt einen neuen Relay-Namespace.</span><span class="sxs-lookup"><span data-stu-id="9c5ab-103">Creates a new Relay namespace.</span></span>

## <span data-ttu-id="9c5ab-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="9c5ab-104">SYNTAX</span></span>

```
New-AzRelayNamespace [-ResourceGroupName] <String> [-Name] <String> [-Location] <String> [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9c5ab-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="9c5ab-105">DESCRIPTION</span></span>
<span data-ttu-id="9c5ab-106">Das Cmdlet **New-AzRelayNamespace** erstellt einen neuen Relay-Namespace.</span><span class="sxs-lookup"><span data-stu-id="9c5ab-106">The **New-AzRelayNamespace** cmdlet creates a new Relay namespace.</span></span> <span data-ttu-id="9c5ab-107">Nach der Erstellung ist das Namespace-Ressourcen Manifest unveränderlich.</span><span class="sxs-lookup"><span data-stu-id="9c5ab-107">Once created, the namespace resource manifest is immutable.</span></span>

## <span data-ttu-id="9c5ab-108">Beispiele</span><span class="sxs-lookup"><span data-stu-id="9c5ab-108">EXAMPLES</span></span>

### <span data-ttu-id="9c5ab-109">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="9c5ab-109">Example 1</span></span>
```
PS C:\> New-AzRelayNamespace -ResourceGroupName Default-ServiceBus-WestUS -Name TestNameSpace-Relay1 -Location "West US" -Tag @{Tag1="Tag1Value"}

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

<span data-ttu-id="9c5ab-110">Erstellt einen neuen Relay-Namespace innerhalb der angegebenen Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="9c5ab-110">Creates a new Relay namespace within the specified resource group.</span></span>

## <span data-ttu-id="9c5ab-111">Parameter</span><span class="sxs-lookup"><span data-stu-id="9c5ab-111">PARAMETERS</span></span>

### <span data-ttu-id="9c5ab-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9c5ab-112">-DefaultProfile</span></span>
<span data-ttu-id="9c5ab-113">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="9c5ab-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9c5ab-114">-Standort</span><span class="sxs-lookup"><span data-stu-id="9c5ab-114">-Location</span></span>
<span data-ttu-id="9c5ab-115">Speicherort des Relay-Namespaces.</span><span class="sxs-lookup"><span data-stu-id="9c5ab-115">Relay Namespace Location.</span></span>

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

### <span data-ttu-id="9c5ab-116">-Name</span><span class="sxs-lookup"><span data-stu-id="9c5ab-116">-Name</span></span>
<span data-ttu-id="9c5ab-117">Name des Relay-Namespaces.</span><span class="sxs-lookup"><span data-stu-id="9c5ab-117">Relay Namespace Name.</span></span>

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

### <span data-ttu-id="9c5ab-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9c5ab-118">-ResourceGroupName</span></span>
<span data-ttu-id="9c5ab-119">Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="9c5ab-119">Resource Group Name.</span></span>

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

### <span data-ttu-id="9c5ab-120">-Tag</span><span class="sxs-lookup"><span data-stu-id="9c5ab-120">-Tag</span></span>
<span data-ttu-id="9c5ab-121">Hashtables, die Ressourcen Tags darstellen.</span><span class="sxs-lookup"><span data-stu-id="9c5ab-121">Hashtables which represents resource Tags.</span></span>

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

### <span data-ttu-id="9c5ab-122">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="9c5ab-122">-Confirm</span></span>
<span data-ttu-id="9c5ab-123">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="9c5ab-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9c5ab-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9c5ab-124">-WhatIf</span></span>
<span data-ttu-id="9c5ab-125">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="9c5ab-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9c5ab-126">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="9c5ab-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9c5ab-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9c5ab-127">CommonParameters</span></span>
<span data-ttu-id="9c5ab-128">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9c5ab-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9c5ab-129">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9c5ab-129">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9c5ab-130">Eingaben</span><span class="sxs-lookup"><span data-stu-id="9c5ab-130">INPUTS</span></span>

### <span data-ttu-id="9c5ab-131">System. String</span><span class="sxs-lookup"><span data-stu-id="9c5ab-131">System.String</span></span>

### <span data-ttu-id="9c5ab-132">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="9c5ab-132">System.Collections.Hashtable</span></span>

## <span data-ttu-id="9c5ab-133">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="9c5ab-133">OUTPUTS</span></span>

### <span data-ttu-id="9c5ab-134">Microsoft. Azure. Commands. Relay. Models. PSRelayNamespaceAttributes</span><span class="sxs-lookup"><span data-stu-id="9c5ab-134">Microsoft.Azure.Commands.Relay.Models.PSRelayNamespaceAttributes</span></span>

## <span data-ttu-id="9c5ab-135">Notizen</span><span class="sxs-lookup"><span data-stu-id="9c5ab-135">NOTES</span></span>

## <span data-ttu-id="9c5ab-136">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="9c5ab-136">RELATED LINKS</span></span>
