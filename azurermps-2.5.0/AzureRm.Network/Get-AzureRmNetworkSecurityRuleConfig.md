---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 5A0D9326-3A8A-4156-8372-EBA93C1BB4E4
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermnetworksecurityruleconfig
schema: 2.0.0
ms.openlocfilehash: 55f2ad108b6392a2f17c7b1539c5ebe7cccc3c19
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/15/2020
ms.locfileid: "93850703"
---
# <span data-ttu-id="e2cde-101">Get-AzureRmNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="e2cde-101">Get-AzureRmNetworkSecurityRuleConfig</span></span>

## <span data-ttu-id="e2cde-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="e2cde-102">SYNOPSIS</span></span>
<span data-ttu-id="e2cde-103">Besorgen Sie sich eine Netzwerk Sicherheitsregel Konfiguration für eine Netzwerksicherheitsgruppe.</span><span class="sxs-lookup"><span data-stu-id="e2cde-103">Get a network security rule configuration for a network security group.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e2cde-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="e2cde-104">SYNTAX</span></span>

```
Get-AzureRmNetworkSecurityRuleConfig [-Name <String>] -NetworkSecurityGroup <PSNetworkSecurityGroup>
 [-DefaultRules] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e2cde-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="e2cde-105">DESCRIPTION</span></span>
<span data-ttu-id="e2cde-106">Das Cmdlet " **Get-AzureRmNetworkSecurityRuleConfig** " Ruft eine Netzwerk Sicherheitsregel-Konfiguration für eine Azure Network Security-Gruppe ab.</span><span class="sxs-lookup"><span data-stu-id="e2cde-106">The **Get-AzureRmNetworkSecurityRuleConfig** cmdlet gets a network security rule configuration for an Azure network security group.</span></span>

## <span data-ttu-id="e2cde-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="e2cde-107">EXAMPLES</span></span>

### <span data-ttu-id="e2cde-108">1: Abrufen einer Netzwerk Sicherheitsregel-Konfiguration</span><span class="sxs-lookup"><span data-stu-id="e2cde-108">1: Retrieving a network security rule config</span></span>
```
Get-AzureRmNetworkSecurityGroup -Name  nsg1 -ResourceGroupName rg1 
    | Get-AzureRmNetworkSecurityRuleConfig -Name AllowInternetOutBound -DefaultRules
```

<span data-ttu-id="e2cde-109">Dieser Befehl ruft die Standardregel mit dem Namen "AllowInternetOutBound" aus der Azure Network Security-Gruppe mit dem Namen "nsg1" in der Ressourcengruppe "RG1" ab.</span><span class="sxs-lookup"><span data-stu-id="e2cde-109">This command retrieves the default rule named "AllowInternetOutBound" from Azure network security group named "nsg1" in resource group "rg1"</span></span>

### <span data-ttu-id="e2cde-110">2: Abrufen einer config-Datei für die Netzwerksicherheit nur mit dem Namen</span><span class="sxs-lookup"><span data-stu-id="e2cde-110">2: Retrieving a network security rule config using only the name</span></span>
```
Get-AzureRmNetworkSecurityGroup -Name  nsg1 -ResourceGroupName rg1 
    | Get-AzureRmNetworkSecurityRuleConfig -Name "rdp-rule"
```

<span data-ttu-id="e2cde-111">Dieser Befehl ruft die benutzerdefinierte Regel mit dem Namen "RDP-Regel" aus der Azure Network Security-Gruppe mit dem Namen "nsg1" in der Ressourcengruppe "RG1" ab.</span><span class="sxs-lookup"><span data-stu-id="e2cde-111">This command retrieves user defined rule named "rdp-rule" from Azure network security group named "nsg1" in resource group "rg1"</span></span>

## <span data-ttu-id="e2cde-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="e2cde-112">PARAMETERS</span></span>

### <span data-ttu-id="e2cde-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e2cde-113">-DefaultProfile</span></span>
<span data-ttu-id="e2cde-114">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="e2cde-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e2cde-115">-DefaultRules</span><span class="sxs-lookup"><span data-stu-id="e2cde-115">-DefaultRules</span></span>
<span data-ttu-id="e2cde-116">Gibt an, ob dieses Cmdlet eine vom Benutzer erstellte Regelkonfiguration oder eine Standardregelkonfiguration erhält.</span><span class="sxs-lookup"><span data-stu-id="e2cde-116">Indicates whether this cmdlet gets a user-created rule configuration or a default rule configuration.</span></span>

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

### <span data-ttu-id="e2cde-117">-Name</span><span class="sxs-lookup"><span data-stu-id="e2cde-117">-Name</span></span>
<span data-ttu-id="e2cde-118">Gibt den Namen der Netzwerk Sicherheitsregel-Konfiguration an, die abgerufen werden soll.</span><span class="sxs-lookup"><span data-stu-id="e2cde-118">Specifies the name of the network security rule configuration to get.</span></span>

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

### <span data-ttu-id="e2cde-119">-NetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="e2cde-119">-NetworkSecurityGroup</span></span>
<span data-ttu-id="e2cde-120">Gibt ein **NetworkSecurityGroup** -Objekt an, das die zu erhaltende Netzwerk Sicherheitsregel Konfiguration enthält.</span><span class="sxs-lookup"><span data-stu-id="e2cde-120">Specifies a **NetworkSecurityGroup** object that contains the network security rule configuration to get.</span></span>

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

### <span data-ttu-id="e2cde-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e2cde-121">CommonParameters</span></span>
<span data-ttu-id="e2cde-122">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e2cde-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e2cde-123">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e2cde-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e2cde-124">Eingaben</span><span class="sxs-lookup"><span data-stu-id="e2cde-124">INPUTS</span></span>

### <span data-ttu-id="e2cde-125">PSNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="e2cde-125">PSNetworkSecurityGroup</span></span>
<span data-ttu-id="e2cde-126">Der Parameter "NetworkSecurityGroup" akzeptiert den Wert vom Typ "PSNetworkSecurityGroup" aus der Pipeline.</span><span class="sxs-lookup"><span data-stu-id="e2cde-126">Parameter 'NetworkSecurityGroup' accepts value of type 'PSNetworkSecurityGroup' from the pipeline</span></span>

## <span data-ttu-id="e2cde-127">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="e2cde-127">OUTPUTS</span></span>

### <span data-ttu-id="e2cde-128">Microsoft. Azure. Commands. Network. Models. PSSecurityRule</span><span class="sxs-lookup"><span data-stu-id="e2cde-128">Microsoft.Azure.Commands.Network.Models.PSSecurityRule</span></span>

## <span data-ttu-id="e2cde-129">Notizen</span><span class="sxs-lookup"><span data-stu-id="e2cde-129">NOTES</span></span>

## <span data-ttu-id="e2cde-130">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="e2cde-130">RELATED LINKS</span></span>

[<span data-ttu-id="e2cde-131">Add-AzureRmNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="e2cde-131">Add-AzureRmNetworkSecurityRuleConfig</span></span>](./Add-AzureRmNetworkSecurityRuleConfig.md)

[<span data-ttu-id="e2cde-132">Neu – AzureRmNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="e2cde-132">New-AzureRmNetworkSecurityRuleConfig</span></span>](./New-AzureRmNetworkSecurityRuleConfig.md)

[<span data-ttu-id="e2cde-133">Remove-AzureRmNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="e2cde-133">Remove-AzureRmNetworkSecurityRuleConfig</span></span>](./Remove-AzureRmNetworkSecurityRuleConfig.md)

[<span data-ttu-id="e2cde-134">Satz-AzureRmNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="e2cde-134">Set-AzureRmNetworkSecurityRuleConfig</span></span>](./Set-AzureRmNetworkSecurityRuleConfig.md)


