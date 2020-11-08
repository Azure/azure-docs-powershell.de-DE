---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 2E43D0D8-EF93-443B-AA8F-58C992026E95
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-aznetworksecurityruleconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzNetworkSecurityRuleConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzNetworkSecurityRuleConfig.md
ms.openlocfilehash: 7f5d41774af2f5ee74c5d343fa9b143801c139f2
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/21/2020
ms.locfileid: "94004217"
---
# <span data-ttu-id="c4798-101">Remove-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="c4798-101">Remove-AzNetworkSecurityRuleConfig</span></span>

## <span data-ttu-id="c4798-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="c4798-102">SYNOPSIS</span></span>
<span data-ttu-id="c4798-103">Entfernt eine Netzwerk Sicherheitsregel aus einer Netzwerksicherheitsgruppe.</span><span class="sxs-lookup"><span data-stu-id="c4798-103">Removes a network security rule from a network security group.</span></span>

## <span data-ttu-id="c4798-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="c4798-104">SYNTAX</span></span>

```
Remove-AzNetworkSecurityRuleConfig [-Name <String>] -NetworkSecurityGroup <PSNetworkSecurityGroup>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c4798-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="c4798-105">DESCRIPTION</span></span>
<span data-ttu-id="c4798-106">Das Cmdlet **Remove-AzNetworkSecurityRuleConfig** entfernt eine Netzwerk Sicherheitsregel-Konfiguration aus einer Azure Network Security-Gruppe.</span><span class="sxs-lookup"><span data-stu-id="c4798-106">The **Remove-AzNetworkSecurityRuleConfig** cmdlet removes a network security rule configuration from an Azure network security group.</span></span>

## <span data-ttu-id="c4798-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="c4798-107">EXAMPLES</span></span>

### <span data-ttu-id="c4798-108">Beispiel 1: Entfernen einer Netzwerk Sicherheitsregel-Konfiguration</span><span class="sxs-lookup"><span data-stu-id="c4798-108">Example 1: Remove a network security rule configuration</span></span>
```
PS C:\>$rule1 = New-AzNetworkSecurityRuleConfig -Name "rdp-rule" -Description "Allow RDP" -Access "Allow" -Protocol "Tcp" -Direction "Inbound" -Priority 100 -SourceAddressPrefix "Internet" -SourcePortRange * -DestinationAddressPrefix * -DestinationPortRange 3389
PS C:\> $nsg = New-AzNetworkSecurityGroup -ResourceGroupName "TestRG" -Location "westus" -Name "NSG-FrontEnd" -SecurityRules $rule1
PS C:\> Remove-AzNetworkSecurityRuleConfig -Name "rdp-rule" -NetworkSecurityGroup $nsg
PS C:\> $nsg | Set-AzNetworkSecurityGroup
```

<span data-ttu-id="c4798-109">Der erste Befehl erstellt eine Netzwerk Sicherheitsregel-Konfiguration mit dem Namen RDP-Rule und speichert Sie dann in der $Rule 1-Variablen.</span><span class="sxs-lookup"><span data-stu-id="c4798-109">The first command creates a network security rule configuration named rdp-rule, and then stores it in the $rule1 variable.</span></span>
<span data-ttu-id="c4798-110">Der zweite Befehl erstellt eine Netzwerksicherheitsgruppe mithilfe der Regel in $Rule 1 und speichert dann die Netzwerksicherheitsgruppe in der $NSG Variablen.</span><span class="sxs-lookup"><span data-stu-id="c4798-110">The second command creates a network security group using the rule in $rule1, and then stores the network security group in the $nsg variable.</span></span>
<span data-ttu-id="c4798-111">Der dritte Befehl entfernt die Netzwerk Sicherheitsregel-Konfiguration mit dem Namen RDP-Rule aus der Gruppe Netzwerksicherheit in $NSG.</span><span class="sxs-lookup"><span data-stu-id="c4798-111">The third command removes the network security rule configuration named rdp-rule from the network security group in $nsg.</span></span>
<span data-ttu-id="c4798-112">Der Befehl Forth speichert die Änderung.</span><span class="sxs-lookup"><span data-stu-id="c4798-112">The forth command saves the change.</span></span>

## <span data-ttu-id="c4798-113">Parameter</span><span class="sxs-lookup"><span data-stu-id="c4798-113">PARAMETERS</span></span>

### <span data-ttu-id="c4798-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c4798-114">-DefaultProfile</span></span>
<span data-ttu-id="c4798-115">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="c4798-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c4798-116">-Name</span><span class="sxs-lookup"><span data-stu-id="c4798-116">-Name</span></span>
<span data-ttu-id="c4798-117">Gibt den Namen der Netzwerk Sicherheitsregel Konfiguration an, die vom Cmdlet entfernt wird.</span><span class="sxs-lookup"><span data-stu-id="c4798-117">Specifies the name of the network security rule configuration that this cmdlet removes.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c4798-118">-NetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="c4798-118">-NetworkSecurityGroup</span></span>
<span data-ttu-id="c4798-119">Gibt ein **NetworkSecurityGroup** -Objekt an.</span><span class="sxs-lookup"><span data-stu-id="c4798-119">Specifies a **NetworkSecurityGroup** object.</span></span>
<span data-ttu-id="c4798-120">Dieses Objekt enthält die zu entfernende Netzwerk Sicherheitsregel-Konfiguration.</span><span class="sxs-lookup"><span data-stu-id="c4798-120">This object contains the network security rule configuration to remove.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSNetworkSecurityGroup
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c4798-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c4798-121">CommonParameters</span></span>
<span data-ttu-id="c4798-122">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c4798-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c4798-123">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c4798-123">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c4798-124">Eingaben</span><span class="sxs-lookup"><span data-stu-id="c4798-124">INPUTS</span></span>

### <span data-ttu-id="c4798-125">Microsoft. Azure. Commands. Network. Models. PSNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="c4798-125">Microsoft.Azure.Commands.Network.Models.PSNetworkSecurityGroup</span></span>

## <span data-ttu-id="c4798-126">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="c4798-126">OUTPUTS</span></span>

### <span data-ttu-id="c4798-127">Microsoft. Azure. Commands. Network. Models. PSNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="c4798-127">Microsoft.Azure.Commands.Network.Models.PSNetworkSecurityGroup</span></span>

## <span data-ttu-id="c4798-128">Notizen</span><span class="sxs-lookup"><span data-stu-id="c4798-128">NOTES</span></span>

## <span data-ttu-id="c4798-129">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="c4798-129">RELATED LINKS</span></span>

[<span data-ttu-id="c4798-130">Add-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="c4798-130">Add-AzNetworkSecurityRuleConfig</span></span>](./Add-AzNetworkSecurityRuleConfig.md)

[<span data-ttu-id="c4798-131">Get-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="c4798-131">Get-AzNetworkSecurityRuleConfig</span></span>](./Get-AzNetworkSecurityRuleConfig.md)

[<span data-ttu-id="c4798-132">Neu – AzNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="c4798-132">New-AzNetworkSecurityGroup</span></span>](./New-AzNetworkSecurityGroup.md)

[<span data-ttu-id="c4798-133">Neu – AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="c4798-133">New-AzNetworkSecurityRuleConfig</span></span>](./New-AzNetworkSecurityRuleConfig.md)

[<span data-ttu-id="c4798-134">Satz-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="c4798-134">Set-AzNetworkSecurityRuleConfig</span></span>](./Set-AzNetworkSecurityRuleConfig.md)


