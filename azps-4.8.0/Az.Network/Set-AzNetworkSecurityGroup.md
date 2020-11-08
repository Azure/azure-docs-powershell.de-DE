---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 9F69DAEF-F2ED-449B-B75F-FCA7ED73D98F
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-aznetworksecuritygroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzNetworkSecurityGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzNetworkSecurityGroup.md
ms.openlocfilehash: d7a13c27550b206bc1c8d8fa909cb5135df0db55
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94166221"
---
# <span data-ttu-id="0504f-101">Set-AzNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="0504f-101">Set-AzNetworkSecurityGroup</span></span>

## <span data-ttu-id="0504f-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="0504f-102">SYNOPSIS</span></span>
<span data-ttu-id="0504f-103">Aktualisiert eine Netzwerksicherheitsgruppe.</span><span class="sxs-lookup"><span data-stu-id="0504f-103">Updates a network security group.</span></span>

## <span data-ttu-id="0504f-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="0504f-104">SYNTAX</span></span>

```
Set-AzNetworkSecurityGroup -NetworkSecurityGroup <PSNetworkSecurityGroup> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0504f-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="0504f-105">DESCRIPTION</span></span>
<span data-ttu-id="0504f-106">Das Cmdlet " **Satz-AzNetworkSecurityGroup** " aktualisiert eine Netzwerksicherheitsgruppe.</span><span class="sxs-lookup"><span data-stu-id="0504f-106">The **Set-AzNetworkSecurityGroup** cmdlet updates a network security group.</span></span>

## <span data-ttu-id="0504f-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="0504f-107">EXAMPLES</span></span>

### <span data-ttu-id="0504f-108">Beispiel 1: Aktualisieren einer vorhandenen Netzwerksicherheitsgruppe</span><span class="sxs-lookup"><span data-stu-id="0504f-108">Example 1: Update an existing network security group</span></span>
```
PS C:\>Get-AzNetworkSecurityGroup -Name "Nsg1" -ResourceGroupName "Rg1" | Add-AzNetworkSecurityRuleConfig -Name "Rdp-Rule" -Description "Allow RDP" -Access "Allow" -Protocol "Tcp" -Direction "Inbound" -Priority 100 -SourceAddressPrefix "Internet" -SourcePortRange "*" -DestinationAddressPrefix "*" -DestinationPortRange "3389" | Set-AzNetworkSecurityGroup
```

<span data-ttu-id="0504f-109">Dieser Befehl ruft die Azure Network Security-Gruppe mit dem Namen Nsg1 ab und fügt eine Netzwerk Sicherheitsregel mit dem Namen Rdp-Rule hinzu, um den Internet Datenverkehr auf Port 3389 dem abgerufenen Netzwerk Sicherheitsgruppenobjekt mithilfe von Add-AzNetworkSecurityRuleConfig zu ermöglichen.</span><span class="sxs-lookup"><span data-stu-id="0504f-109">This command gets the Azure network security group named Nsg1, and adds a network security rule named Rdp-Rule to allow Internet traffic on port 3389 to the retrieved network security group object using Add-AzNetworkSecurityRuleConfig.</span></span>
<span data-ttu-id="0504f-110">Der Befehl behält die geänderte Azure Network Security-Gruppe mithilfe von " **AzNetworkSecurityGroup** " bei.</span><span class="sxs-lookup"><span data-stu-id="0504f-110">The command persists the modified Azure network security group using **Set-AzNetworkSecurityGroup**.</span></span>

## <span data-ttu-id="0504f-111">Parameter</span><span class="sxs-lookup"><span data-stu-id="0504f-111">PARAMETERS</span></span>

### <span data-ttu-id="0504f-112">-AsJob</span><span class="sxs-lookup"><span data-stu-id="0504f-112">-AsJob</span></span>
<span data-ttu-id="0504f-113">Ausführen eines Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="0504f-113">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="0504f-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0504f-114">-DefaultProfile</span></span>
<span data-ttu-id="0504f-115">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="0504f-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="0504f-116">-NetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="0504f-116">-NetworkSecurityGroup</span></span>
<span data-ttu-id="0504f-117">Gibt ein Netzwerk Sicherheitsgruppenobjekt an, das den Zustand darstellt, in dem die Netzwerksicherheitsgruppe festgelegt werden soll.</span><span class="sxs-lookup"><span data-stu-id="0504f-117">Specifies a network security group object representing the state to which the network security group should be set.</span></span>

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

### <span data-ttu-id="0504f-118">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="0504f-118">-Confirm</span></span>
<span data-ttu-id="0504f-119">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="0504f-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0504f-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0504f-120">-WhatIf</span></span>
<span data-ttu-id="0504f-121">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="0504f-121">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="0504f-122">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="0504f-122">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0504f-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0504f-123">CommonParameters</span></span>
<span data-ttu-id="0504f-124">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0504f-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0504f-125">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0504f-125">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0504f-126">Eingaben</span><span class="sxs-lookup"><span data-stu-id="0504f-126">INPUTS</span></span>

### <span data-ttu-id="0504f-127">Microsoft. Azure. Commands. Network. Models. PSNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="0504f-127">Microsoft.Azure.Commands.Network.Models.PSNetworkSecurityGroup</span></span>

## <span data-ttu-id="0504f-128">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="0504f-128">OUTPUTS</span></span>

### <span data-ttu-id="0504f-129">Microsoft. Azure. Commands. Network. Models. PSNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="0504f-129">Microsoft.Azure.Commands.Network.Models.PSNetworkSecurityGroup</span></span>

## <span data-ttu-id="0504f-130">Notizen</span><span class="sxs-lookup"><span data-stu-id="0504f-130">NOTES</span></span>

## <span data-ttu-id="0504f-131">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="0504f-131">RELATED LINKS</span></span>

[<span data-ttu-id="0504f-132">Get-AzNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="0504f-132">Get-AzNetworkSecurityGroup</span></span>](./Get-AzNetworkSecurityGroup.md)

[<span data-ttu-id="0504f-133">Neu – AzNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="0504f-133">New-AzNetworkSecurityGroup</span></span>](./New-AzNetworkSecurityGroup.md)

[<span data-ttu-id="0504f-134">Remove-AzNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="0504f-134">Remove-AzNetworkSecurityGroup</span></span>](./Remove-AzNetworkSecurityGroup.md)


