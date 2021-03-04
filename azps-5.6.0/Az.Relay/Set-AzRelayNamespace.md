---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Relay.dll-Help.xml
Module Name: Az.Relay
online version: https://docs.microsoft.com/powershell/module/az.relay/set-azrelaynamespace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Relay/Relay/help/Set-AzRelayNamespace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Relay/Relay/help/Set-AzRelayNamespace.md
ms.openlocfilehash: 25c633c2929967a5fb580addb78639bff8b6197f
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101943726"
---
# <span data-ttu-id="3b297-101">Set-AzRelayNamespace</span><span class="sxs-lookup"><span data-stu-id="3b297-101">Set-AzRelayNamespace</span></span>

## <span data-ttu-id="3b297-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3b297-102">SYNOPSIS</span></span>
<span data-ttu-id="3b297-103">Aktualisiert die Beschreibung eines vorhandenen Relay-Namespaces.</span><span class="sxs-lookup"><span data-stu-id="3b297-103">Updates the description of an existing Relay namespace.</span></span>

## <span data-ttu-id="3b297-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="3b297-104">SYNTAX</span></span>

```
Set-AzRelayNamespace [-ResourceGroupName] <String> [-Name] <String> [-Tag <Hashtable>]
 [-InputObject <RelayNamespaceAttirbutesUpdateParameter>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3b297-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="3b297-105">DESCRIPTION</span></span>
<span data-ttu-id="3b297-106">Das **Set-AzRelayNamespace-Cmdlet** aktualisiert die Beschreibung des angegebenen Relay-Namespaces innerhalb der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="3b297-106">The **Set-AzRelayNamespace** cmdlet updates the description of the specified Relay namespace within the resource group.</span></span>

## <span data-ttu-id="3b297-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="3b297-107">EXAMPLES</span></span>

### <span data-ttu-id="3b297-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="3b297-108">Example 1</span></span>
```
PS C:\> Set-AzRelayNamespace -ResourceGroupName Default-ServiceBus-WestUS -Name TestNameSpace-Relay1 -Tag @{Tag2="Tag2Value"}

ProvisioningState  :
CreatedAt          : 4/12/2017 12:38:47 AM
UpdatedAt          : 4/12/2017 12:39:10 AM
ServiceBusEndpoint : https://TestNameSpace-Relay1.servicebus.windows.net:443/
MetricId           :
Location           :
Tags               : {[tag2, Tag2Value]}
Id                 :
Name               :
Type               :
```

<span data-ttu-id="3b297-109">Aktualisiert den Relay-Namespace mit einer neuen Beschreibung.</span><span class="sxs-lookup"><span data-stu-id="3b297-109">Updates the Relay namespace with a new description.</span></span>

## <span data-ttu-id="3b297-110">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="3b297-110">PARAMETERS</span></span>

### <span data-ttu-id="3b297-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3b297-111">-DefaultProfile</span></span>
<span data-ttu-id="3b297-112">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="3b297-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3b297-113">-InputObject</span><span class="sxs-lookup"><span data-stu-id="3b297-113">-InputObject</span></span>
<span data-ttu-id="3b297-114">Relay Namespace-Objekt.</span><span class="sxs-lookup"><span data-stu-id="3b297-114">Relay Namespace object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Relay.Models.RelayNamespaceAttirbutesUpdateParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="3b297-115">-Name</span><span class="sxs-lookup"><span data-stu-id="3b297-115">-Name</span></span>
<span data-ttu-id="3b297-116">Name des Relay-Namespaces.</span><span class="sxs-lookup"><span data-stu-id="3b297-116">Relay Namespace Name.</span></span>

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

### <span data-ttu-id="3b297-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3b297-117">-ResourceGroupName</span></span>
<span data-ttu-id="3b297-118">Ressourcengruppenname.</span><span class="sxs-lookup"><span data-stu-id="3b297-118">Resource Group Name.</span></span>

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

### <span data-ttu-id="3b297-119">-Tag</span><span class="sxs-lookup"><span data-stu-id="3b297-119">-Tag</span></span>
<span data-ttu-id="3b297-120">Hashtables, die das Ressourcentag darstellt.</span><span class="sxs-lookup"><span data-stu-id="3b297-120">Hashtables which represents resource Tag.</span></span>

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

### <span data-ttu-id="3b297-121">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="3b297-121">-Confirm</span></span>
<span data-ttu-id="3b297-122">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="3b297-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3b297-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3b297-123">-WhatIf</span></span>
<span data-ttu-id="3b297-124">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="3b297-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3b297-125">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="3b297-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3b297-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3b297-126">CommonParameters</span></span>
<span data-ttu-id="3b297-127">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3b297-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3b297-128">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3b297-128">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3b297-129">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="3b297-129">INPUTS</span></span>

### <span data-ttu-id="3b297-130">System.String</span><span class="sxs-lookup"><span data-stu-id="3b297-130">System.String</span></span>

### <span data-ttu-id="3b297-131">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="3b297-131">System.Collections.Hashtable</span></span>

### <span data-ttu-id="3b297-132">Microsoft.Azure.Commands.Relay.Models.RelayNamespaceAttirbutesUpdateParameter</span><span class="sxs-lookup"><span data-stu-id="3b297-132">Microsoft.Azure.Commands.Relay.Models.RelayNamespaceAttirbutesUpdateParameter</span></span>

## <span data-ttu-id="3b297-133">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="3b297-133">OUTPUTS</span></span>

### <span data-ttu-id="3b297-134">Microsoft.Azure.Commands.Relay.Models.PSRelayNamespaceAttributes</span><span class="sxs-lookup"><span data-stu-id="3b297-134">Microsoft.Azure.Commands.Relay.Models.PSRelayNamespaceAttributes</span></span>

## <span data-ttu-id="3b297-135">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="3b297-135">NOTES</span></span>

## <span data-ttu-id="3b297-136">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="3b297-136">RELATED LINKS</span></span>
