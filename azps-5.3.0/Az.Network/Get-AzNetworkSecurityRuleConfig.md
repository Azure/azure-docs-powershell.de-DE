---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 5A0D9326-3A8A-4156-8372-EBA93C1BB4E4
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-aznetworksecurityruleconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzNetworkSecurityRuleConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzNetworkSecurityRuleConfig.md
ms.openlocfilehash: 3d8b2445d6bb1c92d7246f1d9f33a06dfef3c58b
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98379964"
---
# <span data-ttu-id="12eae-101">Get-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="12eae-101">Get-AzNetworkSecurityRuleConfig</span></span>

## <span data-ttu-id="12eae-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="12eae-102">SYNOPSIS</span></span>
<span data-ttu-id="12eae-103">Erhalten Sie eine Netzwerksicherheitsregelkonfiguration für eine Netzwerksicherheitsgruppe.</span><span class="sxs-lookup"><span data-stu-id="12eae-103">Get a network security rule configuration for a network security group.</span></span>

## <span data-ttu-id="12eae-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="12eae-104">SYNTAX</span></span>

```
Get-AzNetworkSecurityRuleConfig [-Name <String>] -NetworkSecurityGroup <PSNetworkSecurityGroup> [-DefaultRules]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="12eae-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="12eae-105">DESCRIPTION</span></span>
<span data-ttu-id="12eae-106">Das **Cmdlet "Get-AzNetworkSecurityRuleConfig"** ruft eine Netzwerksicherheitsregelkonfiguration für eine Azure-Netzwerksicherheitsgruppe ab.</span><span class="sxs-lookup"><span data-stu-id="12eae-106">The **Get-AzNetworkSecurityRuleConfig** cmdlet gets a network security rule configuration for an Azure network security group.</span></span>

## <span data-ttu-id="12eae-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="12eae-107">EXAMPLES</span></span>

### <span data-ttu-id="12eae-108">1: Abrufen einer Konfiguration für Netzwerksicherheitsregel</span><span class="sxs-lookup"><span data-stu-id="12eae-108">1: Retrieving a network security rule config</span></span>
```
Get-AzNetworkSecurityGroup -Name nsg1 -ResourceGroupName rg1 
    | Get-AzNetworkSecurityRuleConfig -Name AllowInternetOutBound -DefaultRules
```

<span data-ttu-id="12eae-109">Mit diesem Befehl wird die Standardregel mit dem Namen "AllowInternetOutBound" aus der Azure-Netzwerksicherheitsgruppe namens "nsg1" in der Ressourcengruppe "rg1" abgerufen.</span><span class="sxs-lookup"><span data-stu-id="12eae-109">This command retrieves the default rule named "AllowInternetOutBound" from Azure network security group named "nsg1" in resource group "rg1"</span></span>

### <span data-ttu-id="12eae-110">2: Abrufen einer Konfiguration für Netzwerksicherheitsregel nur mit dem Namen</span><span class="sxs-lookup"><span data-stu-id="12eae-110">2: Retrieving a network security rule config using only the name</span></span>
```
Get-AzNetworkSecurityGroup -Name nsg1 -ResourceGroupName rg1 
    | Get-AzNetworkSecurityRuleConfig -Name "rdp-rule"
```

<span data-ttu-id="12eae-111">Dieser Befehl ruft die benutzerdefinierte Regel mit dem Namen "rdp-rule" aus der Azure-Netzwerksicherheitsgruppe namens "nsg1" in der Ressourcengruppe "rg1" ab.</span><span class="sxs-lookup"><span data-stu-id="12eae-111">This command retrieves user defined rule named "rdp-rule" from Azure network security group named "nsg1" in resource group "rg1"</span></span>

## <span data-ttu-id="12eae-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="12eae-112">PARAMETERS</span></span>

### <span data-ttu-id="12eae-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="12eae-113">-DefaultProfile</span></span>
<span data-ttu-id="12eae-114">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="12eae-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="12eae-115">-DefaultRules</span><span class="sxs-lookup"><span data-stu-id="12eae-115">-DefaultRules</span></span>
<span data-ttu-id="12eae-116">Gibt an, ob dieses Cmdlet eine vom Benutzer erstellte Regelkonfiguration oder eine Standardregelkonfiguration erhält.</span><span class="sxs-lookup"><span data-stu-id="12eae-116">Indicates whether this cmdlet gets a user-created rule configuration or a default rule configuration.</span></span>

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

### <span data-ttu-id="12eae-117">-Name</span><span class="sxs-lookup"><span data-stu-id="12eae-117">-Name</span></span>
<span data-ttu-id="12eae-118">Gibt den Namen der Netzwerksicherheitsregelkonfiguration an, die sie erhalten soll.</span><span class="sxs-lookup"><span data-stu-id="12eae-118">Specifies the name of the network security rule configuration to get.</span></span>

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

### <span data-ttu-id="12eae-119">-NetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="12eae-119">-NetworkSecurityGroup</span></span>
<span data-ttu-id="12eae-120">Gibt ein **NetworkSecurityGroup-Objekt** an, das die Konfiguration der Netzwerksicherheitsregel enthält, die sie erhalten soll.</span><span class="sxs-lookup"><span data-stu-id="12eae-120">Specifies a **NetworkSecurityGroup** object that contains the network security rule configuration to get.</span></span>

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

### <span data-ttu-id="12eae-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="12eae-121">CommonParameters</span></span>
<span data-ttu-id="12eae-122">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="12eae-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="12eae-123">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="12eae-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="12eae-124">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="12eae-124">INPUTS</span></span>

### <span data-ttu-id="12eae-125">Microsoft.Azure.Commands.Network.Models.PSNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="12eae-125">Microsoft.Azure.Commands.Network.Models.PSNetworkSecurityGroup</span></span>

## <span data-ttu-id="12eae-126">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="12eae-126">OUTPUTS</span></span>

### <span data-ttu-id="12eae-127">Microsoft.Azure.Commands.Network.Models.PSSecurityRule</span><span class="sxs-lookup"><span data-stu-id="12eae-127">Microsoft.Azure.Commands.Network.Models.PSSecurityRule</span></span>

## <span data-ttu-id="12eae-128">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="12eae-128">NOTES</span></span>

## <span data-ttu-id="12eae-129">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="12eae-129">RELATED LINKS</span></span>

[<span data-ttu-id="12eae-130">Add-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="12eae-130">Add-AzNetworkSecurityRuleConfig</span></span>](./Add-AzNetworkSecurityRuleConfig.md)

[<span data-ttu-id="12eae-131">New-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="12eae-131">New-AzNetworkSecurityRuleConfig</span></span>](./New-AzNetworkSecurityRuleConfig.md)

[<span data-ttu-id="12eae-132">Remove-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="12eae-132">Remove-AzNetworkSecurityRuleConfig</span></span>](./Remove-AzNetworkSecurityRuleConfig.md)

[<span data-ttu-id="12eae-133">Set-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="12eae-133">Set-AzNetworkSecurityRuleConfig</span></span>](./Set-AzNetworkSecurityRuleConfig.md)


