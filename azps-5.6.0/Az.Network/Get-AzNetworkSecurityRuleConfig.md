---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 5A0D9326-3A8A-4156-8372-EBA93C1BB4E4
online version: https://docs.microsoft.com/powershell/module/az.network/get-aznetworksecurityruleconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzNetworkSecurityRuleConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzNetworkSecurityRuleConfig.md
ms.openlocfilehash: c45df01f86abcd7a2f475b62b517765f3045cb10
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101945958"
---
# <span data-ttu-id="9e1cd-101">Get-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="9e1cd-101">Get-AzNetworkSecurityRuleConfig</span></span>

## <span data-ttu-id="9e1cd-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9e1cd-102">SYNOPSIS</span></span>
<span data-ttu-id="9e1cd-103">Holen Sie sich eine Netzwerksicherheitsregelkonfiguration für eine Netzwerksicherheitsgruppe.</span><span class="sxs-lookup"><span data-stu-id="9e1cd-103">Get a network security rule configuration for a network security group.</span></span>

## <span data-ttu-id="9e1cd-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="9e1cd-104">SYNTAX</span></span>

```
Get-AzNetworkSecurityRuleConfig [-Name <String>] -NetworkSecurityGroup <PSNetworkSecurityGroup> [-DefaultRules]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="9e1cd-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="9e1cd-105">DESCRIPTION</span></span>
<span data-ttu-id="9e1cd-106">Das **Get-AzNetworkSecurityRuleConfig-Cmdlet** ruft eine Netzwerksicherheitsregelkonfiguration für eine Azure-Netzwerksicherheitsgruppe ab.</span><span class="sxs-lookup"><span data-stu-id="9e1cd-106">The **Get-AzNetworkSecurityRuleConfig** cmdlet gets a network security rule configuration for an Azure network security group.</span></span>

## <span data-ttu-id="9e1cd-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="9e1cd-107">EXAMPLES</span></span>

### <span data-ttu-id="9e1cd-108">1: Abrufen einer Konfiguration einer Netzwerksicherheitsregel</span><span class="sxs-lookup"><span data-stu-id="9e1cd-108">1: Retrieving a network security rule config</span></span>
```
Get-AzNetworkSecurityGroup -Name nsg1 -ResourceGroupName rg1 
    | Get-AzNetworkSecurityRuleConfig -Name AllowInternetOutBound -DefaultRules
```

<span data-ttu-id="9e1cd-109">Dieser Befehl ruft die Standardregel mit dem Namen "AllowInternetOutBound" aus der Azure-Netzwerksicherheitsgruppe mit dem Namen "nsg1" in der Ressourcengruppe "rg1" ab.</span><span class="sxs-lookup"><span data-stu-id="9e1cd-109">This command retrieves the default rule named "AllowInternetOutBound" from Azure network security group named "nsg1" in resource group "rg1"</span></span>

### <span data-ttu-id="9e1cd-110">2: Abrufen einer Konfiguration für Netzwerksicherheitsregel nur mit dem Namen</span><span class="sxs-lookup"><span data-stu-id="9e1cd-110">2: Retrieving a network security rule config using only the name</span></span>
```
Get-AzNetworkSecurityGroup -Name nsg1 -ResourceGroupName rg1 
    | Get-AzNetworkSecurityRuleConfig -Name "rdp-rule"
```

<span data-ttu-id="9e1cd-111">Mit diesem Befehl wird die benutzerdefinierte Regel mit dem Namen "rdp-rule" aus der Azure-Netzwerksicherheitsgruppe "nsg1" in der Ressourcengruppe "rg1" abgerufen.</span><span class="sxs-lookup"><span data-stu-id="9e1cd-111">This command retrieves user defined rule named "rdp-rule" from Azure network security group named "nsg1" in resource group "rg1"</span></span>

## <span data-ttu-id="9e1cd-112">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="9e1cd-112">PARAMETERS</span></span>

### <span data-ttu-id="9e1cd-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9e1cd-113">-DefaultProfile</span></span>
<span data-ttu-id="9e1cd-114">Die Anmeldeinformationen, das Konto, der Mandant und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="9e1cd-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="9e1cd-115">-DefaultRules</span><span class="sxs-lookup"><span data-stu-id="9e1cd-115">-DefaultRules</span></span>
<span data-ttu-id="9e1cd-116">Gibt an, ob dieses Cmdlet eine vom Benutzer erstellte Regelkonfiguration oder eine Standardregelkonfiguration erhält.</span><span class="sxs-lookup"><span data-stu-id="9e1cd-116">Indicates whether this cmdlet gets a user-created rule configuration or a default rule configuration.</span></span>

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

### <span data-ttu-id="9e1cd-117">-Name</span><span class="sxs-lookup"><span data-stu-id="9e1cd-117">-Name</span></span>
<span data-ttu-id="9e1cd-118">Gibt den Namen der Netzwerksicherheitsregelkonfiguration an, die sie erhalten soll.</span><span class="sxs-lookup"><span data-stu-id="9e1cd-118">Specifies the name of the network security rule configuration to get.</span></span>

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

### <span data-ttu-id="9e1cd-119">-NetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="9e1cd-119">-NetworkSecurityGroup</span></span>
<span data-ttu-id="9e1cd-120">Gibt ein **NetworkSecurityGroup-Objekt** an, das die Netzwerksicherheitsregelkonfiguration enthält, die sie erhalten soll.</span><span class="sxs-lookup"><span data-stu-id="9e1cd-120">Specifies a **NetworkSecurityGroup** object that contains the network security rule configuration to get.</span></span>

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

### <span data-ttu-id="9e1cd-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9e1cd-121">CommonParameters</span></span>
<span data-ttu-id="9e1cd-122">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9e1cd-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9e1cd-123">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="9e1cd-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9e1cd-124">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="9e1cd-124">INPUTS</span></span>

### <span data-ttu-id="9e1cd-125">Microsoft.Azure.Commands.Network.Models.PSNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="9e1cd-125">Microsoft.Azure.Commands.Network.Models.PSNetworkSecurityGroup</span></span>

## <span data-ttu-id="9e1cd-126">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="9e1cd-126">OUTPUTS</span></span>

### <span data-ttu-id="9e1cd-127">Microsoft.Azure.Commands.Network.Models.PSSecurityRule</span><span class="sxs-lookup"><span data-stu-id="9e1cd-127">Microsoft.Azure.Commands.Network.Models.PSSecurityRule</span></span>

## <span data-ttu-id="9e1cd-128">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="9e1cd-128">NOTES</span></span>

## <span data-ttu-id="9e1cd-129">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="9e1cd-129">RELATED LINKS</span></span>

[<span data-ttu-id="9e1cd-130">Add-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="9e1cd-130">Add-AzNetworkSecurityRuleConfig</span></span>](./Add-AzNetworkSecurityRuleConfig.md)

[<span data-ttu-id="9e1cd-131">New-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="9e1cd-131">New-AzNetworkSecurityRuleConfig</span></span>](./New-AzNetworkSecurityRuleConfig.md)

[<span data-ttu-id="9e1cd-132">Remove-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="9e1cd-132">Remove-AzNetworkSecurityRuleConfig</span></span>](./Remove-AzNetworkSecurityRuleConfig.md)

[<span data-ttu-id="9e1cd-133">Set-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="9e1cd-133">Set-AzNetworkSecurityRuleConfig</span></span>](./Set-AzNetworkSecurityRuleConfig.md)


