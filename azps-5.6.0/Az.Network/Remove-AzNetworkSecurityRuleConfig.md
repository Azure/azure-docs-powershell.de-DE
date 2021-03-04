---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 2E43D0D8-EF93-443B-AA8F-58C992026E95
online version: https://docs.microsoft.com/powershell/module/az.network/remove-aznetworksecurityruleconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzNetworkSecurityRuleConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzNetworkSecurityRuleConfig.md
ms.openlocfilehash: a60fa0e305d05ae5d944a69705c3cb3f392b28f0
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101940083"
---
# <span data-ttu-id="39193-101">Remove-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="39193-101">Remove-AzNetworkSecurityRuleConfig</span></span>

## <span data-ttu-id="39193-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="39193-102">SYNOPSIS</span></span>
<span data-ttu-id="39193-103">Entfernt eine Netzwerksicherheitsregel aus einer Netzwerksicherheitsgruppe.</span><span class="sxs-lookup"><span data-stu-id="39193-103">Removes a network security rule from a network security group.</span></span>

## <span data-ttu-id="39193-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="39193-104">SYNTAX</span></span>

```
Remove-AzNetworkSecurityRuleConfig [-Name <String>] -NetworkSecurityGroup <PSNetworkSecurityGroup>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="39193-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="39193-105">DESCRIPTION</span></span>
<span data-ttu-id="39193-106">Das **Cmdlet Remove-AzNetworkSecurityRuleConfig** entfernt eine Netzwerksicherheitsregelkonfiguration aus einer Azure-Netzwerksicherheitsgruppe.</span><span class="sxs-lookup"><span data-stu-id="39193-106">The **Remove-AzNetworkSecurityRuleConfig** cmdlet removes a network security rule configuration from an Azure network security group.</span></span>

## <span data-ttu-id="39193-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="39193-107">EXAMPLES</span></span>

### <span data-ttu-id="39193-108">Beispiel 1: Entfernen einer Netzwerksicherheitsregelkonfiguration</span><span class="sxs-lookup"><span data-stu-id="39193-108">Example 1: Remove a network security rule configuration</span></span>
```
PS C:\>$rule1 = New-AzNetworkSecurityRuleConfig -Name "rdp-rule" -Description "Allow RDP" -Access "Allow" -Protocol "Tcp" -Direction "Inbound" -Priority 100 -SourceAddressPrefix "Internet" -SourcePortRange * -DestinationAddressPrefix * -DestinationPortRange 3389
PS C:\> $nsg = New-AzNetworkSecurityGroup -ResourceGroupName "TestRG" -Location "westus" -Name "NSG-FrontEnd" -SecurityRules $rule1
PS C:\> Remove-AzNetworkSecurityRuleConfig -Name "rdp-rule" -NetworkSecurityGroup $nsg
PS C:\> $nsg | Set-AzNetworkSecurityGroup
```

<span data-ttu-id="39193-109">Mit dem ersten Befehl wird eine Netzwerksicherheitsregelkonfiguration namens rdp-rule erstellt und dann in der $rule 1-Variable gespeichert.</span><span class="sxs-lookup"><span data-stu-id="39193-109">The first command creates a network security rule configuration named rdp-rule, and then stores it in the $rule1 variable.</span></span>
<span data-ttu-id="39193-110">Mit dem zweiten Befehl wird mithilfe der Regel in $rule 1 eine Netzwerksicherheitsgruppe erstellt und dann die Netzwerksicherheitsgruppe in der $nsg gespeichert.</span><span class="sxs-lookup"><span data-stu-id="39193-110">The second command creates a network security group using the rule in $rule1, and then stores the network security group in the $nsg variable.</span></span>
<span data-ttu-id="39193-111">Mit dem dritten Befehl wird die Netzwerksicherheitsregelkonfiguration namens rdp-rule aus der Netzwerksicherheitsgruppe in $nsg.</span><span class="sxs-lookup"><span data-stu-id="39193-111">The third command removes the network security rule configuration named rdp-rule from the network security group in $nsg.</span></span>
<span data-ttu-id="39193-112">Der vierte Befehl speichert die Änderung.</span><span class="sxs-lookup"><span data-stu-id="39193-112">The forth command saves the change.</span></span>

## <span data-ttu-id="39193-113">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="39193-113">PARAMETERS</span></span>

### <span data-ttu-id="39193-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="39193-114">-DefaultProfile</span></span>
<span data-ttu-id="39193-115">Die Anmeldeinformationen, das Konto, der Mandant und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="39193-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="39193-116">-Name</span><span class="sxs-lookup"><span data-stu-id="39193-116">-Name</span></span>
<span data-ttu-id="39193-117">Gibt den Namen der Netzwerksicherheitsregelkonfiguration an, die von diesem Cmdlet entfernt wird.</span><span class="sxs-lookup"><span data-stu-id="39193-117">Specifies the name of the network security rule configuration that this cmdlet removes.</span></span>

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

### <span data-ttu-id="39193-118">-NetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="39193-118">-NetworkSecurityGroup</span></span>
<span data-ttu-id="39193-119">Gibt ein **NetworkSecurityGroup-Objekt** an.</span><span class="sxs-lookup"><span data-stu-id="39193-119">Specifies a **NetworkSecurityGroup** object.</span></span>
<span data-ttu-id="39193-120">Dieses Objekt enthält die Netzwerksicherheitsregelkonfiguration, die entfernt werden soll.</span><span class="sxs-lookup"><span data-stu-id="39193-120">This object contains the network security rule configuration to remove.</span></span>

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

### <span data-ttu-id="39193-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="39193-121">CommonParameters</span></span>
<span data-ttu-id="39193-122">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="39193-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="39193-123">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="39193-123">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="39193-124">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="39193-124">INPUTS</span></span>

### <span data-ttu-id="39193-125">Microsoft.Azure.Commands.Network.Models.PSNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="39193-125">Microsoft.Azure.Commands.Network.Models.PSNetworkSecurityGroup</span></span>

## <span data-ttu-id="39193-126">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="39193-126">OUTPUTS</span></span>

### <span data-ttu-id="39193-127">Microsoft.Azure.Commands.Network.Models.PSNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="39193-127">Microsoft.Azure.Commands.Network.Models.PSNetworkSecurityGroup</span></span>

## <span data-ttu-id="39193-128">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="39193-128">NOTES</span></span>

## <span data-ttu-id="39193-129">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="39193-129">RELATED LINKS</span></span>

[<span data-ttu-id="39193-130">Add-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="39193-130">Add-AzNetworkSecurityRuleConfig</span></span>](./Add-AzNetworkSecurityRuleConfig.md)

[<span data-ttu-id="39193-131">Get-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="39193-131">Get-AzNetworkSecurityRuleConfig</span></span>](./Get-AzNetworkSecurityRuleConfig.md)

[<span data-ttu-id="39193-132">New-AzNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="39193-132">New-AzNetworkSecurityGroup</span></span>](./New-AzNetworkSecurityGroup.md)

[<span data-ttu-id="39193-133">New-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="39193-133">New-AzNetworkSecurityRuleConfig</span></span>](./New-AzNetworkSecurityRuleConfig.md)

[<span data-ttu-id="39193-134">Set-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="39193-134">Set-AzNetworkSecurityRuleConfig</span></span>](./Set-AzNetworkSecurityRuleConfig.md)


