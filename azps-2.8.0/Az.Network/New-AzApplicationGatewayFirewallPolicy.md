---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azapplicationgatewayfirewallpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayFirewallPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayFirewallPolicy.md
ms.openlocfilehash: dc6005c77a72b3965f2fca670c1d729fc7c7bd07
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93822192"
---
# <span data-ttu-id="6f791-101">New-AzApplicationGatewayFirewallPolicy</span><span class="sxs-lookup"><span data-stu-id="6f791-101">New-AzApplicationGatewayFirewallPolicy</span></span>

## <span data-ttu-id="6f791-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="6f791-102">SYNOPSIS</span></span>
<span data-ttu-id="6f791-103">Erstellt eine Firewall-Richtlinie für Application Gateway.</span><span class="sxs-lookup"><span data-stu-id="6f791-103">Creates a application gateway firewall policy.</span></span>

## <span data-ttu-id="6f791-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="6f791-104">SYNTAX</span></span>

```
New-AzApplicationGatewayFirewallPolicy -Name <String> -ResourceGroupName <String> -Location <String>
 [-CustomRule <PSApplicationGatewayFirewallCustomRule[]>] [-Tag <Hashtable>] [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6f791-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="6f791-105">DESCRIPTION</span></span>
<span data-ttu-id="6f791-106">Das Cmdlet **New-AzApplicationGatewayFirewallPolicy** erstellt eine Firewall-Richtlinie für Application Gateway.</span><span class="sxs-lookup"><span data-stu-id="6f791-106">The **New-AzApplicationGatewayFirewallPolicy** cmdlet creates a application gateway firewall policy.</span></span>

## <span data-ttu-id="6f791-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="6f791-107">EXAMPLES</span></span>

### <span data-ttu-id="6f791-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="6f791-108">Example 1</span></span>
```powershell
PS C:\> $firewallPolicy = New-AzApplicationGatewayFirewallPolicy -Name wafResource1 -ResourceGroupName "rg1"  -Location  "westus" -CustomRules $customRule
```

<span data-ttu-id="6f791-109">Dieser Befehl erstellt eine neue Azure Application Gateway-Firewallrichtlinie mit dem Namen "wafResource1" in der Ressourcengruppe "RG1" an Ort "westus" mit benutzerdefinierten Regeln, die in der $CustomRule Variablen definiert sind.</span><span class="sxs-lookup"><span data-stu-id="6f791-109">This command creates a new Azure application gateway firewall policy named "wafResource1" in resource group "rg1" in location "westus" with custom rules defined in the $customRule variable</span></span>

## <span data-ttu-id="6f791-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="6f791-110">PARAMETERS</span></span>

### <span data-ttu-id="6f791-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="6f791-111">-AsJob</span></span>
<span data-ttu-id="6f791-112">Ausführen eines Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="6f791-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="6f791-113">-CustomRule</span><span class="sxs-lookup"><span data-stu-id="6f791-113">-CustomRule</span></span>
<span data-ttu-id="6f791-114">Die Liste der customrules</span><span class="sxs-lookup"><span data-stu-id="6f791-114">The list of CustomRules</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayFirewallCustomRule[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6f791-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6f791-115">-DefaultProfile</span></span>
<span data-ttu-id="6f791-116">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="6f791-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6f791-117">-Force</span><span class="sxs-lookup"><span data-stu-id="6f791-117">-Force</span></span>
<span data-ttu-id="6f791-118">Keine Bestätigung anfordern, wenn Sie eine Ressource überschreiben möchten</span><span class="sxs-lookup"><span data-stu-id="6f791-118">Do not ask for confirmation if you want to overwrite a resource</span></span>

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

### <span data-ttu-id="6f791-119">-Standort</span><span class="sxs-lookup"><span data-stu-id="6f791-119">-Location</span></span>
<span data-ttu-id="6f791-120">Lage.</span><span class="sxs-lookup"><span data-stu-id="6f791-120">location.</span></span>

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

### <span data-ttu-id="6f791-121">-Name</span><span class="sxs-lookup"><span data-stu-id="6f791-121">-Name</span></span>
<span data-ttu-id="6f791-122">Der Ressourcenname.</span><span class="sxs-lookup"><span data-stu-id="6f791-122">The resource name.</span></span>

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

### <span data-ttu-id="6f791-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6f791-123">-ResourceGroupName</span></span>
<span data-ttu-id="6f791-124">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="6f791-124">The resource group name.</span></span>

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

### <span data-ttu-id="6f791-125">-Tag</span><span class="sxs-lookup"><span data-stu-id="6f791-125">-Tag</span></span>
<span data-ttu-id="6f791-126">Eine Hashtable, die Ressourcen Tags darstellt.</span><span class="sxs-lookup"><span data-stu-id="6f791-126">A hashtable which represents resource tags.</span></span>

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

### <span data-ttu-id="6f791-127">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="6f791-127">-Confirm</span></span>
<span data-ttu-id="6f791-128">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="6f791-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6f791-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6f791-129">-WhatIf</span></span>
<span data-ttu-id="6f791-130">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="6f791-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6f791-131">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="6f791-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6f791-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6f791-132">CommonParameters</span></span>
<span data-ttu-id="6f791-133">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6f791-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6f791-134">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6f791-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6f791-135">Eingaben</span><span class="sxs-lookup"><span data-stu-id="6f791-135">INPUTS</span></span>

### <span data-ttu-id="6f791-136">System. String</span><span class="sxs-lookup"><span data-stu-id="6f791-136">System.String</span></span>

### <span data-ttu-id="6f791-137">Microsoft. Azure. Commands. Network. Models. PSApplicationGatewayFirewallCustomRule []</span><span class="sxs-lookup"><span data-stu-id="6f791-137">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayFirewallCustomRule[]</span></span>

### <span data-ttu-id="6f791-138">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="6f791-138">System.Collections.Hashtable</span></span>

## <span data-ttu-id="6f791-139">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="6f791-139">OUTPUTS</span></span>

### <span data-ttu-id="6f791-140">Microsoft. Azure. Commands. Network. Models. PSApplicationGatewayWebApplicationFirewallPolicy</span><span class="sxs-lookup"><span data-stu-id="6f791-140">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayWebApplicationFirewallPolicy</span></span>

## <span data-ttu-id="6f791-141">Notizen</span><span class="sxs-lookup"><span data-stu-id="6f791-141">NOTES</span></span>

## <span data-ttu-id="6f791-142">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="6f791-142">RELATED LINKS</span></span>
