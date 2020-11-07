---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azfirewallpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzFirewallPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzFirewallPolicy.md
ms.openlocfilehash: 5c432224891de6c2fcadc42ae308e9607bc3e432
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/21/2020
ms.locfileid: "93845011"
---
# <span data-ttu-id="63629-101">New-AzFirewallPolicy</span><span class="sxs-lookup"><span data-stu-id="63629-101">New-AzFirewallPolicy</span></span>

## <span data-ttu-id="63629-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="63629-102">SYNOPSIS</span></span>
<span data-ttu-id="63629-103">Erstellt eine neue Azure Firewall-Richtlinie</span><span class="sxs-lookup"><span data-stu-id="63629-103">Creates a new Azure Firewall Policy</span></span>

## <span data-ttu-id="63629-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="63629-104">SYNTAX</span></span>

```
New-AzFirewallPolicy -Name <String> -ResourceGroupName <String> -Location <String> [-ThreatIntelMode <String>]
 [-BasePolicy <String>] [-Tag <Hashtable>] [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="63629-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="63629-105">DESCRIPTION</span></span>
<span data-ttu-id="63629-106">Das Cmdlet **New-AzFirewallPolicy** erstellt eine Azure-Firewall-Richtlinie.</span><span class="sxs-lookup"><span data-stu-id="63629-106">The **New-AzFirewallPolicy** cmdlet creates an Azure Firewall Policy.</span></span>

## <span data-ttu-id="63629-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="63629-107">EXAMPLES</span></span>

### <span data-ttu-id="63629-108">1. Erstellen einer leeren Richtlinie</span><span class="sxs-lookup"><span data-stu-id="63629-108">1. Create an empty policy</span></span>
```powershell
PS C:\> New-AzFirewallPolicy -Name fp1 -ResourceGroupName TestRg
```

<span data-ttu-id="63629-109">In diesem Beispiel wird eine Azure Firewall-Richtlinie erstellt.</span><span class="sxs-lookup"><span data-stu-id="63629-109">This example creates an azure firewall policy</span></span>

### <span data-ttu-id="63629-110">2. Erstellen einer leeren Richtlinie mit dem ThreatIntel-Modus</span><span class="sxs-lookup"><span data-stu-id="63629-110">2. Create an empty policy with ThreatIntel Mode</span></span>
```powershell
PS C:\> New-AzFirewallPolicy -Name fp1 -ResourceGroupName TestRg -ThreatIntelMode "Deny"
```

<span data-ttu-id="63629-111">In diesem Beispiel wird eine Azure-Firewall-Richtlinie mit dem Intel-Modus "Bedrohung" erstellt.</span><span class="sxs-lookup"><span data-stu-id="63629-111">This example creates an azure firewall policy with a threat intel mode</span></span>

## <span data-ttu-id="63629-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="63629-112">PARAMETERS</span></span>

### <span data-ttu-id="63629-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="63629-113">-AsJob</span></span>
<span data-ttu-id="63629-114">Ausführen eines Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="63629-114">Run cmdlet in the background</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="63629-115">-BasePolicy</span><span class="sxs-lookup"><span data-stu-id="63629-115">-BasePolicy</span></span>
<span data-ttu-id="63629-116">Der Vorgangsmodus für Threat Intelligence.</span><span class="sxs-lookup"><span data-stu-id="63629-116">The operation mode for Threat Intelligence.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="63629-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="63629-117">-DefaultProfile</span></span>
<span data-ttu-id="63629-118">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="63629-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="63629-119">-Force</span><span class="sxs-lookup"><span data-stu-id="63629-119">-Force</span></span>
<span data-ttu-id="63629-120">Keine Bestätigung anfordern, wenn Sie eine Ressource überschreiben möchten</span><span class="sxs-lookup"><span data-stu-id="63629-120">Do not ask for confirmation if you want to overwrite a resource</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="63629-121">-Standort</span><span class="sxs-lookup"><span data-stu-id="63629-121">-Location</span></span>
<span data-ttu-id="63629-122">Lage.</span><span class="sxs-lookup"><span data-stu-id="63629-122">location.</span></span>

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

### <span data-ttu-id="63629-123">-Name</span><span class="sxs-lookup"><span data-stu-id="63629-123">-Name</span></span>
<span data-ttu-id="63629-124">Der Ressourcenname.</span><span class="sxs-lookup"><span data-stu-id="63629-124">The resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="63629-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="63629-125">-ResourceGroupName</span></span>
<span data-ttu-id="63629-126">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="63629-126">The resource group name.</span></span>

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

### <span data-ttu-id="63629-127">-Tag</span><span class="sxs-lookup"><span data-stu-id="63629-127">-Tag</span></span>
<span data-ttu-id="63629-128">Eine Hashtable, die Ressourcen Tags darstellt.</span><span class="sxs-lookup"><span data-stu-id="63629-128">A hashtable which represents resource tags.</span></span>

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

### <span data-ttu-id="63629-129">-ThreatIntelMode</span><span class="sxs-lookup"><span data-stu-id="63629-129">-ThreatIntelMode</span></span>
<span data-ttu-id="63629-130">Der Vorgangsmodus für Threat Intelligence.</span><span class="sxs-lookup"><span data-stu-id="63629-130">The operation mode for Threat Intelligence.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Alert, Deny, Off

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="63629-131">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="63629-131">-Confirm</span></span>
<span data-ttu-id="63629-132">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="63629-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="63629-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="63629-133">-WhatIf</span></span>
<span data-ttu-id="63629-134">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="63629-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="63629-135">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="63629-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="63629-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="63629-136">CommonParameters</span></span>
<span data-ttu-id="63629-137">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="63629-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="63629-138">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="63629-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="63629-139">Eingaben</span><span class="sxs-lookup"><span data-stu-id="63629-139">INPUTS</span></span>

### <span data-ttu-id="63629-140">System. String</span><span class="sxs-lookup"><span data-stu-id="63629-140">System.String</span></span>

### <span data-ttu-id="63629-141">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="63629-141">System.Collections.Hashtable</span></span>

## <span data-ttu-id="63629-142">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="63629-142">OUTPUTS</span></span>

### <span data-ttu-id="63629-143">Microsoft. Azure. Commands. Network. Models. PSAzureFirewall</span><span class="sxs-lookup"><span data-stu-id="63629-143">Microsoft.Azure.Commands.Network.Models.PSAzureFirewall</span></span>

## <span data-ttu-id="63629-144">Notizen</span><span class="sxs-lookup"><span data-stu-id="63629-144">NOTES</span></span>

## <span data-ttu-id="63629-145">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="63629-145">RELATED LINKS</span></span>
