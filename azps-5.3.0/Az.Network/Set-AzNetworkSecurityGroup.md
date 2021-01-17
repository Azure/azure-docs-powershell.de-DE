---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 9F69DAEF-F2ED-449B-B75F-FCA7ED73D98F
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-aznetworksecuritygroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzNetworkSecurityGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzNetworkSecurityGroup.md
ms.openlocfilehash: d7a13c27550b206bc1c8d8fa909cb5135df0db55
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98473376"
---
# <span data-ttu-id="466d0-101">Set-AzNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="466d0-101">Set-AzNetworkSecurityGroup</span></span>

## <span data-ttu-id="466d0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="466d0-102">SYNOPSIS</span></span>
<span data-ttu-id="466d0-103">Aktualisiert eine Netzwerksicherheitsgruppe.</span><span class="sxs-lookup"><span data-stu-id="466d0-103">Updates a network security group.</span></span>

## <span data-ttu-id="466d0-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="466d0-104">SYNTAX</span></span>

```
Set-AzNetworkSecurityGroup -NetworkSecurityGroup <PSNetworkSecurityGroup> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="466d0-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="466d0-105">DESCRIPTION</span></span>
<span data-ttu-id="466d0-106">Das **Cmdlet Set-AzNetworkSecurityGroup** aktualisiert eine Netzwerksicherheitsgruppe.</span><span class="sxs-lookup"><span data-stu-id="466d0-106">The **Set-AzNetworkSecurityGroup** cmdlet updates a network security group.</span></span>

## <span data-ttu-id="466d0-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="466d0-107">EXAMPLES</span></span>

### <span data-ttu-id="466d0-108">Beispiel 1: Aktualisieren einer vorhandenen Netzwerksicherheitsgruppe</span><span class="sxs-lookup"><span data-stu-id="466d0-108">Example 1: Update an existing network security group</span></span>
```
PS C:\>Get-AzNetworkSecurityGroup -Name "Nsg1" -ResourceGroupName "Rg1" | Add-AzNetworkSecurityRuleConfig -Name "Rdp-Rule" -Description "Allow RDP" -Access "Allow" -Protocol "Tcp" -Direction "Inbound" -Priority 100 -SourceAddressPrefix "Internet" -SourcePortRange "*" -DestinationAddressPrefix "*" -DestinationPortRange "3389" | Set-AzNetworkSecurityGroup
```

<span data-ttu-id="466d0-109">Dieser Befehl ruft die Azure-Netzwerksicherheitsgruppe namens "Nsg1" ab und fügt eine Netzwerksicherheitsregel namens Rdp-Rule hinzu, um Internetdatenverkehr auf Port 3389 zu dem abgerufenen Netzwerksicherheitsgruppeobjekt mit Add-AzNetworkSecurityRuleConfig zu erlauben.</span><span class="sxs-lookup"><span data-stu-id="466d0-109">This command gets the Azure network security group named Nsg1, and adds a network security rule named Rdp-Rule to allow Internet traffic on port 3389 to the retrieved network security group object using Add-AzNetworkSecurityRuleConfig.</span></span>
<span data-ttu-id="466d0-110">Der Befehl behält die geänderte Azure-Netzwerksicherheitsgruppe mit **Set-AzNetworkSecurityGroup.**</span><span class="sxs-lookup"><span data-stu-id="466d0-110">The command persists the modified Azure network security group using **Set-AzNetworkSecurityGroup**.</span></span>

## <span data-ttu-id="466d0-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="466d0-111">PARAMETERS</span></span>

### <span data-ttu-id="466d0-112">-AsJob</span><span class="sxs-lookup"><span data-stu-id="466d0-112">-AsJob</span></span>
<span data-ttu-id="466d0-113">Ausführen des Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="466d0-113">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="466d0-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="466d0-114">-DefaultProfile</span></span>
<span data-ttu-id="466d0-115">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="466d0-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="466d0-116">-NetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="466d0-116">-NetworkSecurityGroup</span></span>
<span data-ttu-id="466d0-117">Gibt ein Netzwerksicherheitsgruppeobjekt an, das den Zustand darstellt, auf den die Netzwerksicherheitsgruppe festgelegt werden soll.</span><span class="sxs-lookup"><span data-stu-id="466d0-117">Specifies a network security group object representing the state to which the network security group should be set.</span></span>

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

### <span data-ttu-id="466d0-118">-Confirm</span><span class="sxs-lookup"><span data-stu-id="466d0-118">-Confirm</span></span>
<span data-ttu-id="466d0-119">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="466d0-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="466d0-120">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="466d0-120">-WhatIf</span></span>
<span data-ttu-id="466d0-121">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="466d0-121">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="466d0-122">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="466d0-122">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="466d0-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="466d0-123">CommonParameters</span></span>
<span data-ttu-id="466d0-124">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="466d0-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="466d0-125">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="466d0-125">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="466d0-126">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="466d0-126">INPUTS</span></span>

### <span data-ttu-id="466d0-127">Microsoft.Azure.Commands.Network.Models.PSNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="466d0-127">Microsoft.Azure.Commands.Network.Models.PSNetworkSecurityGroup</span></span>

## <span data-ttu-id="466d0-128">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="466d0-128">OUTPUTS</span></span>

### <span data-ttu-id="466d0-129">Microsoft.Azure.Commands.Network.Models.PSNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="466d0-129">Microsoft.Azure.Commands.Network.Models.PSNetworkSecurityGroup</span></span>

## <span data-ttu-id="466d0-130">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="466d0-130">NOTES</span></span>

## <span data-ttu-id="466d0-131">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="466d0-131">RELATED LINKS</span></span>

[<span data-ttu-id="466d0-132">Get-AzNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="466d0-132">Get-AzNetworkSecurityGroup</span></span>](./Get-AzNetworkSecurityGroup.md)

[<span data-ttu-id="466d0-133">New-AzNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="466d0-133">New-AzNetworkSecurityGroup</span></span>](./New-AzNetworkSecurityGroup.md)

[<span data-ttu-id="466d0-134">Remove-AzNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="466d0-134">Remove-AzNetworkSecurityGroup</span></span>](./Remove-AzNetworkSecurityGroup.md)


