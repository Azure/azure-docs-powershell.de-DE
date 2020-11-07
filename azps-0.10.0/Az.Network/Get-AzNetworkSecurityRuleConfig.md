---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 5A0D9326-3A8A-4156-8372-EBA93C1BB4E4
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-aznetworksecurityruleconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Get-AzNetworkSecurityRuleConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Get-AzNetworkSecurityRuleConfig.md
ms.openlocfilehash: 184e1291f134b52ee57a239327bb45da4a4481ff
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/16/2020
ms.locfileid: "93841596"
---
# <span data-ttu-id="cf8a5-101">Get-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="cf8a5-101">Get-AzNetworkSecurityRuleConfig</span></span>

## <span data-ttu-id="cf8a5-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="cf8a5-102">SYNOPSIS</span></span>
<span data-ttu-id="cf8a5-103">Besorgen Sie sich eine Netzwerk Sicherheitsregel Konfiguration für eine Netzwerksicherheitsgruppe.</span><span class="sxs-lookup"><span data-stu-id="cf8a5-103">Get a network security rule configuration for a network security group.</span></span>

## <span data-ttu-id="cf8a5-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="cf8a5-104">SYNTAX</span></span>

```
Get-AzNetworkSecurityRuleConfig [-Name <String>] -NetworkSecurityGroup <PSNetworkSecurityGroup>
 [-DefaultRules] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="cf8a5-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="cf8a5-105">DESCRIPTION</span></span>
<span data-ttu-id="cf8a5-106">Das Cmdlet " **Get-AzNetworkSecurityRuleConfig** " Ruft eine Netzwerk Sicherheitsregel-Konfiguration für eine Azure Network Security-Gruppe ab.</span><span class="sxs-lookup"><span data-stu-id="cf8a5-106">The **Get-AzNetworkSecurityRuleConfig** cmdlet gets a network security rule configuration for an Azure network security group.</span></span>

## <span data-ttu-id="cf8a5-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="cf8a5-107">EXAMPLES</span></span>

### <span data-ttu-id="cf8a5-108">1: Abrufen einer Netzwerk Sicherheitsregel-Konfiguration</span><span class="sxs-lookup"><span data-stu-id="cf8a5-108">1: Retrieving a network security rule config</span></span>
```
Get-AzNetworkSecurityGroup -Name  nsg1 -ResourceGroupName rg1 
    | Get-AzNetworkSecurityRuleConfig -Name AllowInternetOutBound -DefaultRules
```

<span data-ttu-id="cf8a5-109">Dieser Befehl ruft die Standardregel mit dem Namen "AllowInternetOutBound" aus der Azure Network Security-Gruppe mit dem Namen "nsg1" in der Ressourcengruppe "RG1" ab.</span><span class="sxs-lookup"><span data-stu-id="cf8a5-109">This command retrieves the default rule named "AllowInternetOutBound" from Azure network security group named "nsg1" in resource group "rg1"</span></span>

### <span data-ttu-id="cf8a5-110">2: Abrufen einer config-Datei für die Netzwerksicherheit nur mit dem Namen</span><span class="sxs-lookup"><span data-stu-id="cf8a5-110">2: Retrieving a network security rule config using only the name</span></span>
```
Get-AzNetworkSecurityGroup -Name  nsg1 -ResourceGroupName rg1 
    | Get-AzNetworkSecurityRuleConfig -Name "rdp-rule"
```

<span data-ttu-id="cf8a5-111">Dieser Befehl ruft die benutzerdefinierte Regel mit dem Namen "RDP-Regel" aus der Azure Network Security-Gruppe mit dem Namen "nsg1" in der Ressourcengruppe "RG1" ab.</span><span class="sxs-lookup"><span data-stu-id="cf8a5-111">This command retrieves user defined rule named "rdp-rule" from Azure network security group named "nsg1" in resource group "rg1"</span></span>

## <span data-ttu-id="cf8a5-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="cf8a5-112">PARAMETERS</span></span>

### <span data-ttu-id="cf8a5-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cf8a5-113">-DefaultProfile</span></span>
<span data-ttu-id="cf8a5-114">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="cf8a5-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cf8a5-115">-DefaultRules</span><span class="sxs-lookup"><span data-stu-id="cf8a5-115">-DefaultRules</span></span>
<span data-ttu-id="cf8a5-116">Gibt an, ob dieses Cmdlet eine vom Benutzer erstellte Regelkonfiguration oder eine Standardregelkonfiguration erhält.</span><span class="sxs-lookup"><span data-stu-id="cf8a5-116">Indicates whether this cmdlet gets a user-created rule configuration or a default rule configuration.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cf8a5-117">-Name</span><span class="sxs-lookup"><span data-stu-id="cf8a5-117">-Name</span></span>
<span data-ttu-id="cf8a5-118">Gibt den Namen der Netzwerk Sicherheitsregel-Konfiguration an, die abgerufen werden soll.</span><span class="sxs-lookup"><span data-stu-id="cf8a5-118">Specifies the name of the network security rule configuration to get.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cf8a5-119">-NetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="cf8a5-119">-NetworkSecurityGroup</span></span>
<span data-ttu-id="cf8a5-120">Gibt ein **NetworkSecurityGroup** -Objekt an, das die zu erhaltende Netzwerk Sicherheitsregel Konfiguration enthält.</span><span class="sxs-lookup"><span data-stu-id="cf8a5-120">Specifies a **NetworkSecurityGroup** object that contains the network security rule configuration to get.</span></span>

```yaml
Type: PSNetworkSecurityGroup
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="cf8a5-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cf8a5-121">CommonParameters</span></span>
<span data-ttu-id="cf8a5-122">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cf8a5-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cf8a5-123">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="cf8a5-123">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cf8a5-124">Eingaben</span><span class="sxs-lookup"><span data-stu-id="cf8a5-124">INPUTS</span></span>

### <span data-ttu-id="cf8a5-125">PSNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="cf8a5-125">PSNetworkSecurityGroup</span></span>
<span data-ttu-id="cf8a5-126">Der Parameter "NetworkSecurityGroup" akzeptiert den Wert vom Typ "PSNetworkSecurityGroup" aus der Pipeline.</span><span class="sxs-lookup"><span data-stu-id="cf8a5-126">Parameter 'NetworkSecurityGroup' accepts value of type 'PSNetworkSecurityGroup' from the pipeline</span></span>

## <span data-ttu-id="cf8a5-127">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="cf8a5-127">OUTPUTS</span></span>

### <span data-ttu-id="cf8a5-128">Microsoft. Azure. Commands. Network. Models. PSSecurityRule</span><span class="sxs-lookup"><span data-stu-id="cf8a5-128">Microsoft.Azure.Commands.Network.Models.PSSecurityRule</span></span>

## <span data-ttu-id="cf8a5-129">Notizen</span><span class="sxs-lookup"><span data-stu-id="cf8a5-129">NOTES</span></span>

## <span data-ttu-id="cf8a5-130">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="cf8a5-130">RELATED LINKS</span></span>

[<span data-ttu-id="cf8a5-131">Add-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="cf8a5-131">Add-AzNetworkSecurityRuleConfig</span></span>](./Add-AzNetworkSecurityRuleConfig.md)

[<span data-ttu-id="cf8a5-132">Neu – AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="cf8a5-132">New-AzNetworkSecurityRuleConfig</span></span>](./New-AzNetworkSecurityRuleConfig.md)

[<span data-ttu-id="cf8a5-133">Remove-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="cf8a5-133">Remove-AzNetworkSecurityRuleConfig</span></span>](./Remove-AzNetworkSecurityRuleConfig.md)

[<span data-ttu-id="cf8a5-134">Satz-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="cf8a5-134">Set-AzNetworkSecurityRuleConfig</span></span>](./Set-AzNetworkSecurityRuleConfig.md)


