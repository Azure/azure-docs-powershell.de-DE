---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azfirewallpolicyapplicationrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzFirewallPolicyApplicationRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzFirewallPolicyApplicationRule.md
ms.openlocfilehash: 1b9fd10e11cb283f880979e7e4a5d703521c9a87
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/21/2020
ms.locfileid: "93844988"
---
# <span data-ttu-id="d2621-101">New-AzFirewallPolicyApplicationRule</span><span class="sxs-lookup"><span data-stu-id="d2621-101">New-AzFirewallPolicyApplicationRule</span></span>

## <span data-ttu-id="d2621-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="d2621-102">SYNOPSIS</span></span>
<span data-ttu-id="d2621-103">Erstellen einer neuen Azure Firewall-Richtlinien Anwendungsregel</span><span class="sxs-lookup"><span data-stu-id="d2621-103">Create a new Azure Firewall Policy Application Rule</span></span>

## <span data-ttu-id="d2621-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="d2621-104">SYNTAX</span></span>

### <span data-ttu-id="d2621-105">TargetFqdn (Standard)</span><span class="sxs-lookup"><span data-stu-id="d2621-105">TargetFqdn (Default)</span></span>
```
New-AzFirewallPolicyApplicationRule -Name <String> [-Description <String>] [-SourceAddress <String[]>]
 -TargetFqdn <String[]> -Protocol <String[]> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="d2621-106">FqdnTag</span><span class="sxs-lookup"><span data-stu-id="d2621-106">FqdnTag</span></span>
```
New-AzFirewallPolicyApplicationRule -Name <String> [-Description <String>] [-SourceAddress <String[]>]
 -FqdnTag <String[]> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d2621-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="d2621-107">DESCRIPTION</span></span>
<span data-ttu-id="d2621-108">Das Cmdlet **New-AzFirewallPolicyApplicationRule** erstellt eine Anwendungsregel für eine Azure-Firewall-Richtlinie.</span><span class="sxs-lookup"><span data-stu-id="d2621-108">The **New-AzFirewallPolicyApplicationRule** cmdlet creates an Application Rule for a Azure Firewall Policy.</span></span>

## <span data-ttu-id="d2621-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="d2621-109">EXAMPLES</span></span>

### <span data-ttu-id="d2621-110">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="d2621-110">Example 1</span></span>
```powershell
PS C:\> New-AzFirewallPolicyApplicationRule -Name AR1 -SourceAddress "192.168.0.0/16" -Protocol "http:80","https:443" -TargetFqdn "*.ro", "*.com"
```

<span data-ttu-id="d2621-111">In diesem Beispiel wird eine Anwendungsregel mit der Quelladresse, dem Protokoll und den Ziel-FQDNs erstellt.</span><span class="sxs-lookup"><span data-stu-id="d2621-111">This example creates an application rule with the source address, protocol and the target fqdns.</span></span>

## <span data-ttu-id="d2621-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="d2621-112">PARAMETERS</span></span>

### <span data-ttu-id="d2621-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d2621-113">-DefaultProfile</span></span>
<span data-ttu-id="d2621-114">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="d2621-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d2621-115">-Beschreibung</span><span class="sxs-lookup"><span data-stu-id="d2621-115">-Description</span></span>
<span data-ttu-id="d2621-116">Die Beschreibung der Regel</span><span class="sxs-lookup"><span data-stu-id="d2621-116">The description of the rule</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d2621-117">-FqdnTag</span><span class="sxs-lookup"><span data-stu-id="d2621-117">-FqdnTag</span></span>
<span data-ttu-id="d2621-118">Die FQDN-Tags der Regel</span><span class="sxs-lookup"><span data-stu-id="d2621-118">The FQDN Tags of the rule</span></span>

```yaml
Type: String[]
Parameter Sets: FqdnTag
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d2621-119">-Name</span><span class="sxs-lookup"><span data-stu-id="d2621-119">-Name</span></span>
<span data-ttu-id="d2621-120">Der Name der Anwendungsregel</span><span class="sxs-lookup"><span data-stu-id="d2621-120">The name of the Application Rule</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d2621-121">-Protokoll</span><span class="sxs-lookup"><span data-stu-id="d2621-121">-Protocol</span></span>
<span data-ttu-id="d2621-122">Die Protokolle der Regel</span><span class="sxs-lookup"><span data-stu-id="d2621-122">The protocols of the rule</span></span>

```yaml
Type: String[]
Parameter Sets: TargetFqdn
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d2621-123">-SourceAddress</span><span class="sxs-lookup"><span data-stu-id="d2621-123">-SourceAddress</span></span>
<span data-ttu-id="d2621-124">Die Quelladressen der Regel</span><span class="sxs-lookup"><span data-stu-id="d2621-124">The source addresses of the rule</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d2621-125">-TargetFqdn</span><span class="sxs-lookup"><span data-stu-id="d2621-125">-TargetFqdn</span></span>
<span data-ttu-id="d2621-126">Die Ziel-FQDNs der Regel</span><span class="sxs-lookup"><span data-stu-id="d2621-126">The target FQDNs of the rule</span></span>

```yaml
Type: String[]
Parameter Sets: TargetFqdn
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d2621-127">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="d2621-127">-Confirm</span></span>
<span data-ttu-id="d2621-128">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="d2621-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d2621-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d2621-129">-WhatIf</span></span>
<span data-ttu-id="d2621-130">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="d2621-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d2621-131">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="d2621-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d2621-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d2621-132">CommonParameters</span></span>
<span data-ttu-id="d2621-133">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d2621-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d2621-134">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="d2621-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d2621-135">Eingaben</span><span class="sxs-lookup"><span data-stu-id="d2621-135">INPUTS</span></span>

### <span data-ttu-id="d2621-136">Keine</span><span class="sxs-lookup"><span data-stu-id="d2621-136">None</span></span>

## <span data-ttu-id="d2621-137">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="d2621-137">OUTPUTS</span></span>

### <span data-ttu-id="d2621-138">Microsoft. Azure. Commands. Network. Models. PSAzureFirewallPolicyApplicationRule</span><span class="sxs-lookup"><span data-stu-id="d2621-138">Microsoft.Azure.Commands.Network.Models.PSAzureFirewallPolicyApplicationRule</span></span>

## <span data-ttu-id="d2621-139">Notizen</span><span class="sxs-lookup"><span data-stu-id="d2621-139">NOTES</span></span>

## <span data-ttu-id="d2621-140">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="d2621-140">RELATED LINKS</span></span>
