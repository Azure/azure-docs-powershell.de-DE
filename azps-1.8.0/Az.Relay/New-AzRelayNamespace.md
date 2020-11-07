---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Relay.dll-Help.xml
Module Name: Az.Relay
online version: https://docs.microsoft.com/en-us/powershell/module/az.relay/new-azrelaynamespace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Relay/Relay/help/New-AzRelayNamespace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Relay/Relay/help/New-AzRelayNamespace.md
ms.openlocfilehash: 37e641516ffc21a0984f97cb84f94d2564033fe9
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93659710"
---
# <span data-ttu-id="2c10b-101">New-AzRelayNamespace</span><span class="sxs-lookup"><span data-stu-id="2c10b-101">New-AzRelayNamespace</span></span>

## <span data-ttu-id="2c10b-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="2c10b-102">SYNOPSIS</span></span>
<span data-ttu-id="2c10b-103">Erstellt einen neuen Relay-Namespace.</span><span class="sxs-lookup"><span data-stu-id="2c10b-103">Creates a new Relay namespace.</span></span>

## <span data-ttu-id="2c10b-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="2c10b-104">SYNTAX</span></span>

```
New-AzRelayNamespace [-ResourceGroupName] <String> [-Name] <String> [-Location] <String> [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2c10b-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="2c10b-105">DESCRIPTION</span></span>
<span data-ttu-id="2c10b-106">Das Cmdlet **New-AzRelayNamespace** erstellt einen neuen Relay-Namespace.</span><span class="sxs-lookup"><span data-stu-id="2c10b-106">The **New-AzRelayNamespace** cmdlet creates a new Relay namespace.</span></span> <span data-ttu-id="2c10b-107">Nach der Erstellung ist das Namespace-Ressourcen Manifest unveränderlich.</span><span class="sxs-lookup"><span data-stu-id="2c10b-107">Once created, the namespace resource manifest is immutable.</span></span>

## <span data-ttu-id="2c10b-108">Beispiele</span><span class="sxs-lookup"><span data-stu-id="2c10b-108">EXAMPLES</span></span>

### <span data-ttu-id="2c10b-109">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="2c10b-109">Example 1</span></span>
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

<span data-ttu-id="2c10b-110">Erstellt einen neuen Relay-Namespace innerhalb der angegebenen Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="2c10b-110">Creates a new Relay namespace within the specified resource group.</span></span>

## <span data-ttu-id="2c10b-111">Parameter</span><span class="sxs-lookup"><span data-stu-id="2c10b-111">PARAMETERS</span></span>

### <span data-ttu-id="2c10b-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2c10b-112">-DefaultProfile</span></span>
<span data-ttu-id="2c10b-113">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="2c10b-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2c10b-114">-Standort</span><span class="sxs-lookup"><span data-stu-id="2c10b-114">-Location</span></span>
<span data-ttu-id="2c10b-115">Speicherort des Relay-Namespaces.</span><span class="sxs-lookup"><span data-stu-id="2c10b-115">Relay Namespace Location.</span></span>

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

### <span data-ttu-id="2c10b-116">-Name</span><span class="sxs-lookup"><span data-stu-id="2c10b-116">-Name</span></span>
<span data-ttu-id="2c10b-117">Name des Relay-Namespaces.</span><span class="sxs-lookup"><span data-stu-id="2c10b-117">Relay Namespace Name.</span></span>

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

### <span data-ttu-id="2c10b-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2c10b-118">-ResourceGroupName</span></span>
<span data-ttu-id="2c10b-119">Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="2c10b-119">Resource Group Name.</span></span>

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

### <span data-ttu-id="2c10b-120">-Tag</span><span class="sxs-lookup"><span data-stu-id="2c10b-120">-Tag</span></span>
<span data-ttu-id="2c10b-121">Hashtables, die Ressourcen Tags darstellen.</span><span class="sxs-lookup"><span data-stu-id="2c10b-121">Hashtables which represents resource Tags.</span></span>

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

### <span data-ttu-id="2c10b-122">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="2c10b-122">-Confirm</span></span>
<span data-ttu-id="2c10b-123">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="2c10b-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2c10b-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2c10b-124">-WhatIf</span></span>
<span data-ttu-id="2c10b-125">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="2c10b-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2c10b-126">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="2c10b-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2c10b-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2c10b-127">CommonParameters</span></span>
<span data-ttu-id="2c10b-128">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2c10b-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2c10b-129">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2c10b-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2c10b-130">Eingaben</span><span class="sxs-lookup"><span data-stu-id="2c10b-130">INPUTS</span></span>

### <span data-ttu-id="2c10b-131">System. String</span><span class="sxs-lookup"><span data-stu-id="2c10b-131">System.String</span></span>

### <span data-ttu-id="2c10b-132">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="2c10b-132">System.Collections.Hashtable</span></span>

## <span data-ttu-id="2c10b-133">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="2c10b-133">OUTPUTS</span></span>

### <span data-ttu-id="2c10b-134">Microsoft. Azure. Commands. Relay. Models. PSRelayNamespaceAttributes</span><span class="sxs-lookup"><span data-stu-id="2c10b-134">Microsoft.Azure.Commands.Relay.Models.PSRelayNamespaceAttributes</span></span>

## <span data-ttu-id="2c10b-135">Notizen</span><span class="sxs-lookup"><span data-stu-id="2c10b-135">NOTES</span></span>

## <span data-ttu-id="2c10b-136">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="2c10b-136">RELATED LINKS</span></span>
