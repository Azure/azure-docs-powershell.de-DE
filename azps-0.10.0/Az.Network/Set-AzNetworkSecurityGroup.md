---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 9F69DAEF-F2ED-449B-B75F-FCA7ED73D98F
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-aznetworksecuritygroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Set-AzNetworkSecurityGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Set-AzNetworkSecurityGroup.md
ms.openlocfilehash: 1c61af223b97ac60dd74f55504ce623b26b5233e
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/16/2020
ms.locfileid: "93843612"
---
# <span data-ttu-id="3eecd-101">Set-AzNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="3eecd-101">Set-AzNetworkSecurityGroup</span></span>

## <span data-ttu-id="3eecd-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="3eecd-102">SYNOPSIS</span></span>
<span data-ttu-id="3eecd-103">Legt den Zielstatus für eine Netzwerksicherheitsgruppe fest.</span><span class="sxs-lookup"><span data-stu-id="3eecd-103">Sets the goal state for a network security group.</span></span>

## <span data-ttu-id="3eecd-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="3eecd-104">SYNTAX</span></span>

```
Set-AzNetworkSecurityGroup -NetworkSecurityGroup <PSNetworkSecurityGroup> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="3eecd-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="3eecd-105">DESCRIPTION</span></span>
<span data-ttu-id="3eecd-106">Das Cmdlet " **Set-AzNetworkSecurityGroup** " legt den Zielstatus für eine Azure Network Security-Gruppe fest.</span><span class="sxs-lookup"><span data-stu-id="3eecd-106">The **Set-AzNetworkSecurityGroup** cmdlet sets the goal state for an Azure network security group.</span></span>

## <span data-ttu-id="3eecd-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="3eecd-107">EXAMPLES</span></span>

### <span data-ttu-id="3eecd-108">Beispiel 1: Festlegung des Zielstatus für eine Netzwerksicherheitsgruppe</span><span class="sxs-lookup"><span data-stu-id="3eecd-108">Example 1: Set the goal state for a network security group</span></span>
```
PS C:\>Get-AzNetworkSecurityGroup -Name "Nsg1" -ResourceGroupName "Rg1" | Add-AzNetworkSecurityRuleConfig -Name "Rdp-Rule" -Description "Allow RDP" -Access "Allow" -Protocol "Tcp" -Direction "Inbound" -Priority 100 -SourceAddressPrefix "Internet" -SourcePortRange "*" -DestinationAddressPrefix "*" -DestinationPortRange "3389" | Set-AzNetworkSecurityGroup
```

<span data-ttu-id="3eecd-109">Dieser Befehl ruft die Azure Network Security-Gruppe mit dem Namen Nsg1 ab und fügt eine Netzwerk Sicherheitsregel mit dem Namen Rdp-Rule hinzu, um den Internet Datenverkehr auf Port 3389 dem abgerufenen Netzwerk Sicherheitsgruppenobjekt mithilfe von Add-AzNetworkSecurityRuleConfig zu ermöglichen.</span><span class="sxs-lookup"><span data-stu-id="3eecd-109">This command gets the Azure network security group named Nsg1, and adds a network security rule named Rdp-Rule to allow Internet traffic on port 3389 to the retrieved network security group object using Add-AzNetworkSecurityRuleConfig.</span></span>
<span data-ttu-id="3eecd-110">Der Befehl behält die geänderte Azure Network Security-Gruppe mithilfe von " **AzNetworkSecurityGroup** " bei.</span><span class="sxs-lookup"><span data-stu-id="3eecd-110">The command persists the modified Azure network security group using **Set-AzNetworkSecurityGroup**.</span></span>

## <span data-ttu-id="3eecd-111">Parameter</span><span class="sxs-lookup"><span data-stu-id="3eecd-111">PARAMETERS</span></span>

### <span data-ttu-id="3eecd-112">-AsJob</span><span class="sxs-lookup"><span data-stu-id="3eecd-112">-AsJob</span></span>
<span data-ttu-id="3eecd-113">Ausführen eines Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="3eecd-113">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="3eecd-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3eecd-114">-DefaultProfile</span></span>
<span data-ttu-id="3eecd-115">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="3eecd-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="3eecd-116">-NetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="3eecd-116">-NetworkSecurityGroup</span></span>
<span data-ttu-id="3eecd-117">Ein Netzwerk Sicherheitsgruppenobjekt, das den Zielstatus darstellt, zu dem das Cmdlet die Netzwerksicherheitsgruppe festlegt.</span><span class="sxs-lookup"><span data-stu-id="3eecd-117">A network security group object representing the goal state to which the cmdlet sets the network security group.</span></span>

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

### <span data-ttu-id="3eecd-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3eecd-118">CommonParameters</span></span>
<span data-ttu-id="3eecd-119">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3eecd-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3eecd-120">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3eecd-120">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3eecd-121">Eingaben</span><span class="sxs-lookup"><span data-stu-id="3eecd-121">INPUTS</span></span>

### <span data-ttu-id="3eecd-122">PSNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="3eecd-122">PSNetworkSecurityGroup</span></span>
<span data-ttu-id="3eecd-123">Der Parameter "NetworkSecurityGroup" akzeptiert den Wert vom Typ "PSNetworkSecurityGroup" aus der Pipeline.</span><span class="sxs-lookup"><span data-stu-id="3eecd-123">Parameter 'NetworkSecurityGroup' accepts value of type 'PSNetworkSecurityGroup' from the pipeline</span></span>

## <span data-ttu-id="3eecd-124">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="3eecd-124">OUTPUTS</span></span>

### <span data-ttu-id="3eecd-125">Microsoft. Azure. Commands. Network. Models. PSNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="3eecd-125">Microsoft.Azure.Commands.Network.Models.PSNetworkSecurityGroup</span></span>

## <span data-ttu-id="3eecd-126">Notizen</span><span class="sxs-lookup"><span data-stu-id="3eecd-126">NOTES</span></span>

## <span data-ttu-id="3eecd-127">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="3eecd-127">RELATED LINKS</span></span>

[<span data-ttu-id="3eecd-128">Get-AzNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="3eecd-128">Get-AzNetworkSecurityGroup</span></span>](./Get-AzNetworkSecurityGroup.md)

[<span data-ttu-id="3eecd-129">Neu – AzNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="3eecd-129">New-AzNetworkSecurityGroup</span></span>](./New-AzNetworkSecurityGroup.md)

[<span data-ttu-id="3eecd-130">Remove-AzNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="3eecd-130">Remove-AzNetworkSecurityGroup</span></span>](./Remove-AzNetworkSecurityGroup.md)


