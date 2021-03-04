---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 9F69DAEF-F2ED-449B-B75F-FCA7ED73D98F
online version: https://docs.microsoft.com/powershell/module/az.network/set-aznetworksecuritygroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzNetworkSecurityGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzNetworkSecurityGroup.md
ms.openlocfilehash: 91144275806c5e3a6913d39990ad68644c71b244
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101944825"
---
# <span data-ttu-id="a43a1-101">Set-AzNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="a43a1-101">Set-AzNetworkSecurityGroup</span></span>

## <span data-ttu-id="a43a1-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a43a1-102">SYNOPSIS</span></span>
<span data-ttu-id="a43a1-103">Aktualisiert eine Netzwerksicherheitsgruppe.</span><span class="sxs-lookup"><span data-stu-id="a43a1-103">Updates a network security group.</span></span>

## <span data-ttu-id="a43a1-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="a43a1-104">SYNTAX</span></span>

```
Set-AzNetworkSecurityGroup -NetworkSecurityGroup <PSNetworkSecurityGroup> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a43a1-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="a43a1-105">DESCRIPTION</span></span>
<span data-ttu-id="a43a1-106">Das **Cmdlet Set-AzNetworkSecurityGroup** aktualisiert eine Netzwerksicherheitsgruppe.</span><span class="sxs-lookup"><span data-stu-id="a43a1-106">The **Set-AzNetworkSecurityGroup** cmdlet updates a network security group.</span></span>

## <span data-ttu-id="a43a1-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="a43a1-107">EXAMPLES</span></span>

### <span data-ttu-id="a43a1-108">Beispiel 1: Aktualisieren einer vorhandenen Netzwerksicherheitsgruppe</span><span class="sxs-lookup"><span data-stu-id="a43a1-108">Example 1: Update an existing network security group</span></span>
```
PS C:\>Get-AzNetworkSecurityGroup -Name "Nsg1" -ResourceGroupName "Rg1" | Add-AzNetworkSecurityRuleConfig -Name "Rdp-Rule" -Description "Allow RDP" -Access "Allow" -Protocol "Tcp" -Direction "Inbound" -Priority 100 -SourceAddressPrefix "Internet" -SourcePortRange "*" -DestinationAddressPrefix "*" -DestinationPortRange "3389" | Set-AzNetworkSecurityGroup
```

<span data-ttu-id="a43a1-109">Dieser Befehl ruft die Azure-Netzwerksicherheitsgruppe mit dem Namen Nsg1 ab und fügt eine Netzwerksicherheitsregel mit dem Namen Rdp-Rule hinzu, um Internetdatenverkehr über Port 3389 zum abgerufenen Netzwerksicherheitsgruppeobjekt mithilfe von Add-AzNetworkSecurityRuleConfig zu ermöglichen.</span><span class="sxs-lookup"><span data-stu-id="a43a1-109">This command gets the Azure network security group named Nsg1, and adds a network security rule named Rdp-Rule to allow Internet traffic on port 3389 to the retrieved network security group object using Add-AzNetworkSecurityRuleConfig.</span></span>
<span data-ttu-id="a43a1-110">Mit dem Befehl wird die geänderte Azure-Netzwerksicherheitsgruppe mit **Set-AzNetworkSecurityGroup beibehalten.**</span><span class="sxs-lookup"><span data-stu-id="a43a1-110">The command persists the modified Azure network security group using **Set-AzNetworkSecurityGroup**.</span></span>

## <span data-ttu-id="a43a1-111">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="a43a1-111">PARAMETERS</span></span>

### <span data-ttu-id="a43a1-112">-AsJob</span><span class="sxs-lookup"><span data-stu-id="a43a1-112">-AsJob</span></span>
<span data-ttu-id="a43a1-113">Ausführen des Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="a43a1-113">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="a43a1-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a43a1-114">-DefaultProfile</span></span>
<span data-ttu-id="a43a1-115">Die Anmeldeinformationen, das Konto, der Mandant und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="a43a1-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a43a1-116">-NetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="a43a1-116">-NetworkSecurityGroup</span></span>
<span data-ttu-id="a43a1-117">Gibt ein Netzwerksicherheitsgruppeobjekt an, das den Zustand darstellt, auf den die Netzwerksicherheitsgruppe festgelegt werden soll.</span><span class="sxs-lookup"><span data-stu-id="a43a1-117">Specifies a network security group object representing the state to which the network security group should be set.</span></span>

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

### <span data-ttu-id="a43a1-118">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="a43a1-118">-Confirm</span></span>
<span data-ttu-id="a43a1-119">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="a43a1-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a43a1-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a43a1-120">-WhatIf</span></span>
<span data-ttu-id="a43a1-121">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="a43a1-121">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="a43a1-122">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="a43a1-122">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a43a1-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a43a1-123">CommonParameters</span></span>
<span data-ttu-id="a43a1-124">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a43a1-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a43a1-125">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a43a1-125">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a43a1-126">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="a43a1-126">INPUTS</span></span>

### <span data-ttu-id="a43a1-127">Microsoft.Azure.Commands.Network.Models.PSNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="a43a1-127">Microsoft.Azure.Commands.Network.Models.PSNetworkSecurityGroup</span></span>

## <span data-ttu-id="a43a1-128">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="a43a1-128">OUTPUTS</span></span>

### <span data-ttu-id="a43a1-129">Microsoft.Azure.Commands.Network.Models.PSNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="a43a1-129">Microsoft.Azure.Commands.Network.Models.PSNetworkSecurityGroup</span></span>

## <span data-ttu-id="a43a1-130">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="a43a1-130">NOTES</span></span>

## <span data-ttu-id="a43a1-131">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="a43a1-131">RELATED LINKS</span></span>

[<span data-ttu-id="a43a1-132">Get-AzNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="a43a1-132">Get-AzNetworkSecurityGroup</span></span>](./Get-AzNetworkSecurityGroup.md)

[<span data-ttu-id="a43a1-133">New-AzNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="a43a1-133">New-AzNetworkSecurityGroup</span></span>](./New-AzNetworkSecurityGroup.md)

[<span data-ttu-id="a43a1-134">Remove-AzNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="a43a1-134">Remove-AzNetworkSecurityGroup</span></span>](./Remove-AzNetworkSecurityGroup.md)


