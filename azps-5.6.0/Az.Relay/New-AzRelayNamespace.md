---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Relay.dll-Help.xml
Module Name: Az.Relay
online version: https://docs.microsoft.com/powershell/module/az.relay/new-azrelaynamespace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Relay/Relay/help/New-AzRelayNamespace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Relay/Relay/help/New-AzRelayNamespace.md
ms.openlocfilehash: c6f0fc3d8a0ef96a8b54b954e07fb1a9d1c644e3
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101943775"
---
# <span data-ttu-id="f441c-101">New-AzRelayNamespace</span><span class="sxs-lookup"><span data-stu-id="f441c-101">New-AzRelayNamespace</span></span>

## <span data-ttu-id="f441c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f441c-102">SYNOPSIS</span></span>
<span data-ttu-id="f441c-103">Erstellt einen neuen Relay-Namespace.</span><span class="sxs-lookup"><span data-stu-id="f441c-103">Creates a new Relay namespace.</span></span>

## <span data-ttu-id="f441c-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="f441c-104">SYNTAX</span></span>

```
New-AzRelayNamespace [-ResourceGroupName] <String> [-Name] <String> [-Location] <String> [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f441c-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="f441c-105">DESCRIPTION</span></span>
<span data-ttu-id="f441c-106">Das **Cmdlet New-AzRelayNamespace** erstellt einen neuen Relay-Namespace.</span><span class="sxs-lookup"><span data-stu-id="f441c-106">The **New-AzRelayNamespace** cmdlet creates a new Relay namespace.</span></span> <span data-ttu-id="f441c-107">Nach dem Erstellen ist das Namespaceressourcenmanifest unveränderlich.</span><span class="sxs-lookup"><span data-stu-id="f441c-107">Once created, the namespace resource manifest is immutable.</span></span>

## <span data-ttu-id="f441c-108">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="f441c-108">EXAMPLES</span></span>

### <span data-ttu-id="f441c-109">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="f441c-109">Example 1</span></span>
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

<span data-ttu-id="f441c-110">Erstellt einen neuen Relay-Namespace innerhalb der angegebenen Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="f441c-110">Creates a new Relay namespace within the specified resource group.</span></span>

## <span data-ttu-id="f441c-111">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="f441c-111">PARAMETERS</span></span>

### <span data-ttu-id="f441c-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f441c-112">-DefaultProfile</span></span>
<span data-ttu-id="f441c-113">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="f441c-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f441c-114">-Location</span><span class="sxs-lookup"><span data-stu-id="f441c-114">-Location</span></span>
<span data-ttu-id="f441c-115">Relay Namespace Location.</span><span class="sxs-lookup"><span data-stu-id="f441c-115">Relay Namespace Location.</span></span>

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

### <span data-ttu-id="f441c-116">-Name</span><span class="sxs-lookup"><span data-stu-id="f441c-116">-Name</span></span>
<span data-ttu-id="f441c-117">Name des Relay-Namespaces.</span><span class="sxs-lookup"><span data-stu-id="f441c-117">Relay Namespace Name.</span></span>

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

### <span data-ttu-id="f441c-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f441c-118">-ResourceGroupName</span></span>
<span data-ttu-id="f441c-119">Ressourcengruppenname.</span><span class="sxs-lookup"><span data-stu-id="f441c-119">Resource Group Name.</span></span>

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

### <span data-ttu-id="f441c-120">-Tag</span><span class="sxs-lookup"><span data-stu-id="f441c-120">-Tag</span></span>
<span data-ttu-id="f441c-121">Hashtables, die Ressourcentags darstellt.</span><span class="sxs-lookup"><span data-stu-id="f441c-121">Hashtables which represents resource Tags.</span></span>

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

### <span data-ttu-id="f441c-122">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="f441c-122">-Confirm</span></span>
<span data-ttu-id="f441c-123">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="f441c-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f441c-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f441c-124">-WhatIf</span></span>
<span data-ttu-id="f441c-125">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="f441c-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f441c-126">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="f441c-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f441c-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f441c-127">CommonParameters</span></span>
<span data-ttu-id="f441c-128">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f441c-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f441c-129">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f441c-129">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f441c-130">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="f441c-130">INPUTS</span></span>

### <span data-ttu-id="f441c-131">System.String</span><span class="sxs-lookup"><span data-stu-id="f441c-131">System.String</span></span>

### <span data-ttu-id="f441c-132">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="f441c-132">System.Collections.Hashtable</span></span>

## <span data-ttu-id="f441c-133">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="f441c-133">OUTPUTS</span></span>

### <span data-ttu-id="f441c-134">Microsoft.Azure.Commands.Relay.Models.PSRelayNamespaceAttributes</span><span class="sxs-lookup"><span data-stu-id="f441c-134">Microsoft.Azure.Commands.Relay.Models.PSRelayNamespaceAttributes</span></span>

## <span data-ttu-id="f441c-135">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="f441c-135">NOTES</span></span>

## <span data-ttu-id="f441c-136">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="f441c-136">RELATED LINKS</span></span>
