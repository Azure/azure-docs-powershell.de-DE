---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 2E43D0D8-EF93-443B-AA8F-58C992026E95
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/remove-azurermnetworksecurityruleconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmNetworkSecurityRuleConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmNetworkSecurityRuleConfig.md
ms.openlocfilehash: d6ca2ac1e091e3576af51ba8f1a2f50676994ce1
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93503526"
---
# <span data-ttu-id="4ca71-101">Remove-AzureRmNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="4ca71-101">Remove-AzureRmNetworkSecurityRuleConfig</span></span>

## <span data-ttu-id="4ca71-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="4ca71-102">SYNOPSIS</span></span>
<span data-ttu-id="4ca71-103">Entfernt eine Netzwerk Sicherheitsregel aus einer Netzwerksicherheitsgruppe.</span><span class="sxs-lookup"><span data-stu-id="4ca71-103">Removes a network security rule from a network security group.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="4ca71-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="4ca71-104">SYNTAX</span></span>

```
Remove-AzureRmNetworkSecurityRuleConfig [-Name <String>] -NetworkSecurityGroup <PSNetworkSecurityGroup>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="4ca71-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="4ca71-105">DESCRIPTION</span></span>
<span data-ttu-id="4ca71-106">Das Cmdlet **Remove-AzureRmNetworkSecurityRuleConfig** entfernt eine Netzwerk Sicherheitsregel-Konfiguration aus einer Azure Network Security-Gruppe.</span><span class="sxs-lookup"><span data-stu-id="4ca71-106">The **Remove-AzureRmNetworkSecurityRuleConfig** cmdlet removes a network security rule configuration from an Azure network security group.</span></span>

## <span data-ttu-id="4ca71-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="4ca71-107">EXAMPLES</span></span>

### <span data-ttu-id="4ca71-108">Beispiel 1: Entfernen einer Netzwerk Sicherheitsregel-Konfiguration</span><span class="sxs-lookup"><span data-stu-id="4ca71-108">Example 1: Remove a network security rule configuration</span></span>
```
PS C:\>$rule1 = New-AzureRmNetworkSecurityRuleConfig -Name "rdp-rule" -Description "Allow RDP" -Access "Allow" -Protocol "Tcp" -Direction "Inbound" -Priority 100 -SourceAddressPrefix "Internet" -SourcePortRange * -DestinationAddressPrefix * -DestinationPortRange 3389
PS C:\> $nsg = New-AzureRmNetworkSecurityGroup -ResourceGroupName "TestRG" -Location "westus" -Name "NSG-FrontEnd" -SecurityRules $rule1
PS C:\> Remove-AzureRmNetworkSecurityRuleConfig -Name "rdp-rule" -NetworkSecurityGroup $nsg
```

<span data-ttu-id="4ca71-109">Der erste Befehl erstellt eine Netzwerk Sicherheitsregel-Konfiguration mit dem Namen RDP-Rule und speichert Sie dann in der $Rule 1-Variablen.</span><span class="sxs-lookup"><span data-stu-id="4ca71-109">The first command creates a network security rule configuration named rdp-rule, and then stores it in the $rule1 variable.</span></span>
<span data-ttu-id="4ca71-110">Der zweite Befehl erstellt eine Netzwerksicherheitsgruppe mithilfe der Regel in $Rule 1 und speichert dann die Netzwerksicherheitsgruppe in der $NSG Variablen.</span><span class="sxs-lookup"><span data-stu-id="4ca71-110">The second command creates a network security group using the rule in $rule1, and then stores the network security group in the $nsg variable.</span></span>
<span data-ttu-id="4ca71-111">Der dritte Befehl entfernt die Netzwerk Sicherheitsregel-Konfiguration mit dem Namen RDP-Rule aus der Gruppe Netzwerksicherheit in $NSG.</span><span class="sxs-lookup"><span data-stu-id="4ca71-111">The third command removes the network security rule configuration named rdp-rule from the network security group in $nsg.</span></span>

## <span data-ttu-id="4ca71-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="4ca71-112">PARAMETERS</span></span>

### <span data-ttu-id="4ca71-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4ca71-113">-DefaultProfile</span></span>
<span data-ttu-id="4ca71-114">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="4ca71-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4ca71-115">-Name</span><span class="sxs-lookup"><span data-stu-id="4ca71-115">-Name</span></span>
<span data-ttu-id="4ca71-116">Gibt den Namen der Netzwerk Sicherheitsregel Konfiguration an, die vom Cmdlet entfernt wird.</span><span class="sxs-lookup"><span data-stu-id="4ca71-116">Specifies the name of the network security rule configuration that this cmdlet removes.</span></span>

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

### <span data-ttu-id="4ca71-117">-NetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="4ca71-117">-NetworkSecurityGroup</span></span>
<span data-ttu-id="4ca71-118">Gibt ein **NetworkSecurityGroup** -Objekt an.</span><span class="sxs-lookup"><span data-stu-id="4ca71-118">Specifies a **NetworkSecurityGroup** object.</span></span>
<span data-ttu-id="4ca71-119">Dieses Objekt enthält die zu entfernende Netzwerk Sicherheitsregel-Konfiguration.</span><span class="sxs-lookup"><span data-stu-id="4ca71-119">This object contains the network security rule configuration to remove.</span></span>

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

### <span data-ttu-id="4ca71-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4ca71-120">CommonParameters</span></span>
<span data-ttu-id="4ca71-121">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4ca71-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4ca71-122">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4ca71-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4ca71-123">Eingaben</span><span class="sxs-lookup"><span data-stu-id="4ca71-123">INPUTS</span></span>

### <span data-ttu-id="4ca71-124">Microsoft. Azure. Commands. Network. Models. PSNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="4ca71-124">Microsoft.Azure.Commands.Network.Models.PSNetworkSecurityGroup</span></span>
<span data-ttu-id="4ca71-125">Parameter: NetworkSecurityGroup (ByValue)</span><span class="sxs-lookup"><span data-stu-id="4ca71-125">Parameters: NetworkSecurityGroup (ByValue)</span></span>

## <span data-ttu-id="4ca71-126">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="4ca71-126">OUTPUTS</span></span>

### <span data-ttu-id="4ca71-127">Microsoft. Azure. Commands. Network. Models. PSNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="4ca71-127">Microsoft.Azure.Commands.Network.Models.PSNetworkSecurityGroup</span></span>

## <span data-ttu-id="4ca71-128">Notizen</span><span class="sxs-lookup"><span data-stu-id="4ca71-128">NOTES</span></span>

## <span data-ttu-id="4ca71-129">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="4ca71-129">RELATED LINKS</span></span>

[<span data-ttu-id="4ca71-130">Add-AzureRmNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="4ca71-130">Add-AzureRmNetworkSecurityRuleConfig</span></span>](./Add-AzureRmNetworkSecurityRuleConfig.md)

[<span data-ttu-id="4ca71-131">Get-AzureRmNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="4ca71-131">Get-AzureRmNetworkSecurityRuleConfig</span></span>](./Get-AzureRmNetworkSecurityRuleConfig.md)

[<span data-ttu-id="4ca71-132">Neu – AzureRmNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="4ca71-132">New-AzureRmNetworkSecurityGroup</span></span>](./New-AzureRmNetworkSecurityGroup.md)

[<span data-ttu-id="4ca71-133">Neu – AzureRmNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="4ca71-133">New-AzureRmNetworkSecurityRuleConfig</span></span>](./New-AzureRmNetworkSecurityRuleConfig.md)

[<span data-ttu-id="4ca71-134">Satz-AzureRmNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="4ca71-134">Set-AzureRmNetworkSecurityRuleConfig</span></span>](./Set-AzureRmNetworkSecurityRuleConfig.md)


