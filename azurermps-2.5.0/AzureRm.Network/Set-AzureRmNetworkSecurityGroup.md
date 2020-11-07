---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 9F69DAEF-F2ED-449B-B75F-FCA7ED73D98F
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/set-azurermnetworksecuritygroup
schema: 2.0.0
ms.openlocfilehash: 348732794a0cf16233f9a139e86ed89658fc5ac2
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/15/2020
ms.locfileid: "93850296"
---
# <span data-ttu-id="cc419-101">Set-AzureRmNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="cc419-101">Set-AzureRmNetworkSecurityGroup</span></span>

## <span data-ttu-id="cc419-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="cc419-102">SYNOPSIS</span></span>
<span data-ttu-id="cc419-103">Legt den Zielstatus für eine Netzwerksicherheitsgruppe fest.</span><span class="sxs-lookup"><span data-stu-id="cc419-103">Sets the goal state for a network security group.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="cc419-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="cc419-104">SYNTAX</span></span>

```
Set-AzureRmNetworkSecurityGroup -NetworkSecurityGroup <PSNetworkSecurityGroup> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="cc419-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="cc419-105">DESCRIPTION</span></span>
<span data-ttu-id="cc419-106">Das Cmdlet " **Set-AzureRmNetworkSecurityGroup** " legt den Zielstatus für eine Azure Network Security-Gruppe fest.</span><span class="sxs-lookup"><span data-stu-id="cc419-106">The **Set-AzureRmNetworkSecurityGroup** cmdlet sets the goal state for an Azure network security group.</span></span>

## <span data-ttu-id="cc419-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="cc419-107">EXAMPLES</span></span>

### <span data-ttu-id="cc419-108">Beispiel 1: Festlegung des Zielstatus für eine Netzwerksicherheitsgruppe</span><span class="sxs-lookup"><span data-stu-id="cc419-108">Example 1: Set the goal state for a network security group</span></span>
```
PS C:\>Get-AzureRmNetworkSecurityGroup -Name "Nsg1" -ResourceGroupName "Rg1" | Add-AzureRmNetworkSecurityRuleConfig -Name "Rdp-Rule" -Description "Allow RDP" -Access "Allow" -Protocol "Tcp" -Direction "Inbound" -Priority 100 -SourceAddressPrefix "Internet" -SourcePortRange "*" -DestinationAddressPrefix "*" -DestinationPortRange "3389" | Set-AzureRmNetworkSecurityGroup
```

<span data-ttu-id="cc419-109">Dieser Befehl ruft die Azure Network Security-Gruppe mit dem Namen Nsg1 ab und fügt eine Netzwerk Sicherheitsregel mit dem Namen Rdp-Rule hinzu, um den Internet Datenverkehr auf Port 3389 dem abgerufenen Netzwerk Sicherheitsgruppenobjekt mithilfe von Add-AzureRmNetworkSecurityRuleConfig zu ermöglichen.</span><span class="sxs-lookup"><span data-stu-id="cc419-109">This command gets the Azure network security group named Nsg1, and adds a network security rule named Rdp-Rule to allow Internet traffic on port 3389 to the retrieved network security group object using Add-AzureRmNetworkSecurityRuleConfig.</span></span>
<span data-ttu-id="cc419-110">Der Befehl behält die geänderte Azure Network Security-Gruppe mithilfe von " **AzureRmNetworkSecurityGroup** " bei.</span><span class="sxs-lookup"><span data-stu-id="cc419-110">The command persists the modified Azure network security group using **Set-AzureRmNetworkSecurityGroup**.</span></span>

## <span data-ttu-id="cc419-111">Parameter</span><span class="sxs-lookup"><span data-stu-id="cc419-111">PARAMETERS</span></span>

### <span data-ttu-id="cc419-112">-AsJob</span><span class="sxs-lookup"><span data-stu-id="cc419-112">-AsJob</span></span>
<span data-ttu-id="cc419-113">Ausführen eines Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="cc419-113">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="cc419-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cc419-114">-DefaultProfile</span></span>
<span data-ttu-id="cc419-115">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="cc419-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="cc419-116">-NetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="cc419-116">-NetworkSecurityGroup</span></span>
<span data-ttu-id="cc419-117">Ein Netzwerk Sicherheitsgruppenobjekt, das den Zielstatus darstellt, zu dem das Cmdlet die Netzwerksicherheitsgruppe festlegt.</span><span class="sxs-lookup"><span data-stu-id="cc419-117">A network security group object representing the goal state to which the cmdlet sets the network security group.</span></span>

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

### <span data-ttu-id="cc419-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cc419-118">CommonParameters</span></span>
<span data-ttu-id="cc419-119">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cc419-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cc419-120">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="cc419-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cc419-121">Eingaben</span><span class="sxs-lookup"><span data-stu-id="cc419-121">INPUTS</span></span>

### <span data-ttu-id="cc419-122">PSNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="cc419-122">PSNetworkSecurityGroup</span></span>
<span data-ttu-id="cc419-123">Der Parameter "NetworkSecurityGroup" akzeptiert den Wert vom Typ "PSNetworkSecurityGroup" aus der Pipeline.</span><span class="sxs-lookup"><span data-stu-id="cc419-123">Parameter 'NetworkSecurityGroup' accepts value of type 'PSNetworkSecurityGroup' from the pipeline</span></span>

## <span data-ttu-id="cc419-124">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="cc419-124">OUTPUTS</span></span>

### <span data-ttu-id="cc419-125">Microsoft. Azure. Commands. Network. Models. PSNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="cc419-125">Microsoft.Azure.Commands.Network.Models.PSNetworkSecurityGroup</span></span>

## <span data-ttu-id="cc419-126">Notizen</span><span class="sxs-lookup"><span data-stu-id="cc419-126">NOTES</span></span>

## <span data-ttu-id="cc419-127">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="cc419-127">RELATED LINKS</span></span>

[<span data-ttu-id="cc419-128">Get-AzureRmNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="cc419-128">Get-AzureRmNetworkSecurityGroup</span></span>](./Get-AzureRmNetworkSecurityGroup.md)

[<span data-ttu-id="cc419-129">Neu – AzureRmNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="cc419-129">New-AzureRmNetworkSecurityGroup</span></span>](./New-AzureRmNetworkSecurityGroup.md)

[<span data-ttu-id="cc419-130">Remove-AzureRmNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="cc419-130">Remove-AzureRmNetworkSecurityGroup</span></span>](./Remove-AzureRmNetworkSecurityGroup.md)


