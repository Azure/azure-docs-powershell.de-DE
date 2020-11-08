---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 015C7DB7-2B08-4033-9B6E-1738D4DDACDA
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-aznetworkinterfaceipconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzNetworkInterfaceIpConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzNetworkInterfaceIpConfig.md
ms.openlocfilehash: 784374b620af09b00f460ff5c50d0a08baa46233
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/21/2020
ms.locfileid: "94004225"
---
# <span data-ttu-id="edd3f-101">Remove-AzNetworkInterfaceIpConfig</span><span class="sxs-lookup"><span data-stu-id="edd3f-101">Remove-AzNetworkInterfaceIpConfig</span></span>

## <span data-ttu-id="edd3f-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="edd3f-102">SYNOPSIS</span></span>
<span data-ttu-id="edd3f-103">Entfernt eine Netzwerkschnittstellen-IP-Konfiguration von einer Netzwerkschnittstelle.</span><span class="sxs-lookup"><span data-stu-id="edd3f-103">Removes a network interface IP configuration from a network interface.</span></span>

## <span data-ttu-id="edd3f-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="edd3f-104">SYNTAX</span></span>

```
Remove-AzNetworkInterfaceIpConfig -Name <String> -NetworkInterface <PSNetworkInterface>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="edd3f-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="edd3f-105">DESCRIPTION</span></span>
<span data-ttu-id="edd3f-106">Das Cmdlet **Remove-AzNetworkInterfaceIpConfig** entfernt eine Netzwerkschnittstellen-IP-Konfiguration über eine Azure-Netzwerkschnittstelle.</span><span class="sxs-lookup"><span data-stu-id="edd3f-106">The **Remove-AzNetworkInterfaceIpConfig** cmdlet removes a network interface IP configuration from an Azure network interface.</span></span>

## <span data-ttu-id="edd3f-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="edd3f-107">EXAMPLES</span></span>

### <span data-ttu-id="edd3f-108">1: Löschen einer IP-Konfiguration über eine Netzwerkschnittstelle</span><span class="sxs-lookup"><span data-stu-id="edd3f-108">1: Delete an IP configuration from a network interface</span></span>
```
$nic = Get-AzNetworkInterface -Name mynic -ResourceGroupName myrg

Remove-AzNetworkInterfaceIpConfig -Name IPConfig-1 -NetworkInterface $nic
```

<span data-ttu-id="edd3f-109">Der erste Befehl ruft eine Netzwerkschnittstelle mit dem Namen mynic ab und speichert Sie in der Variablen $NIC.</span><span class="sxs-lookup"><span data-stu-id="edd3f-109">The first command gets a network interface called mynic and stores it in the variable $nic.</span></span> <span data-ttu-id="edd3f-110">Der zweite Befehl entfernt die IP-Konfiguration mit dem Namen ipconfig-1, die dieser Netzwerkschnittstelle zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="edd3f-110">The second command removes the IP configuration called IPConfig-1 associated with this network interface.</span></span>

## <span data-ttu-id="edd3f-111">Parameter</span><span class="sxs-lookup"><span data-stu-id="edd3f-111">PARAMETERS</span></span>

### <span data-ttu-id="edd3f-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="edd3f-112">-DefaultProfile</span></span>
<span data-ttu-id="edd3f-113">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="edd3f-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="edd3f-114">-Name</span><span class="sxs-lookup"><span data-stu-id="edd3f-114">-Name</span></span>
<span data-ttu-id="edd3f-115">Gibt den Namen der zu entfernenden Netzwerkschnittstellen-IP-Konfiguration an.</span><span class="sxs-lookup"><span data-stu-id="edd3f-115">Specifies the name of the network interface IP configuration to remove.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="edd3f-116">-Network Interface</span><span class="sxs-lookup"><span data-stu-id="edd3f-116">-NetworkInterface</span></span>
<span data-ttu-id="edd3f-117">Gibt ein **Network Interface** -Objekt an.</span><span class="sxs-lookup"><span data-stu-id="edd3f-117">Specifies a **NetworkInterface** object.</span></span>
<span data-ttu-id="edd3f-118">Dieses Objekt enthält die zu entfernende Netzwerkschnittstellen-IP-Konfiguration.</span><span class="sxs-lookup"><span data-stu-id="edd3f-118">This object contains the network interface IP configuration to remove.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSNetworkInterface
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="edd3f-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="edd3f-119">CommonParameters</span></span>
<span data-ttu-id="edd3f-120">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="edd3f-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="edd3f-121">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="edd3f-121">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="edd3f-122">Eingaben</span><span class="sxs-lookup"><span data-stu-id="edd3f-122">INPUTS</span></span>

### <span data-ttu-id="edd3f-123">Microsoft. Azure. Commands. Network. Models. PSNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="edd3f-123">Microsoft.Azure.Commands.Network.Models.PSNetworkInterface</span></span>

## <span data-ttu-id="edd3f-124">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="edd3f-124">OUTPUTS</span></span>

### <span data-ttu-id="edd3f-125">Microsoft. Azure. Commands. Network. Models. PSNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="edd3f-125">Microsoft.Azure.Commands.Network.Models.PSNetworkInterface</span></span>

## <span data-ttu-id="edd3f-126">Notizen</span><span class="sxs-lookup"><span data-stu-id="edd3f-126">NOTES</span></span>
* <span data-ttu-id="edd3f-127">Schlüsselwörter: Azure, azurerm, arm, Resource, Management, Manager, Netzwerk, Netzwerke</span><span class="sxs-lookup"><span data-stu-id="edd3f-127">Keywords: azure, azurerm, arm, resource, management, manager, network, networking</span></span>

## <span data-ttu-id="edd3f-128">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="edd3f-128">RELATED LINKS</span></span>

[<span data-ttu-id="edd3f-129">Add-AzNetworkInterfaceIpConfig</span><span class="sxs-lookup"><span data-stu-id="edd3f-129">Add-AzNetworkInterfaceIpConfig</span></span>](./Add-AzNetworkInterfaceIpConfig.md)

[<span data-ttu-id="edd3f-130">Get-AzNetworkInterfaceIpConfig</span><span class="sxs-lookup"><span data-stu-id="edd3f-130">Get-AzNetworkInterfaceIpConfig</span></span>](./Get-AzNetworkInterfaceIpConfig.md)

[<span data-ttu-id="edd3f-131">Neu – AzNetworkInterfaceIpConfig</span><span class="sxs-lookup"><span data-stu-id="edd3f-131">New-AzNetworkInterfaceIpConfig</span></span>](./New-AzNetworkInterfaceIpConfig.md)

[<span data-ttu-id="edd3f-132">Satz-AzNetworkInterfaceIpConfig</span><span class="sxs-lookup"><span data-stu-id="edd3f-132">Set-AzNetworkInterfaceIpConfig</span></span>](./Set-AzNetworkInterfaceIpConfig.md)


