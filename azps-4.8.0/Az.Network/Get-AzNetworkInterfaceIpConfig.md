---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 1B39809C-90DA-4ECB-B949-D4A9A54ED982
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-aznetworkinterfaceipconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzNetworkInterfaceIpConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzNetworkInterfaceIpConfig.md
ms.openlocfilehash: 8152cf778cabed1c4a8a346ac86b708266058fc6
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94165268"
---
# <span data-ttu-id="12bb8-101">Get-AzNetworkInterfaceIpConfig</span><span class="sxs-lookup"><span data-stu-id="12bb8-101">Get-AzNetworkInterfaceIpConfig</span></span>

## <span data-ttu-id="12bb8-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="12bb8-102">SYNOPSIS</span></span>
<span data-ttu-id="12bb8-103">Ruft eine Netzwerkschnittstellen-IP-Konfiguration für eine Netzwerkschnittstelle ab.</span><span class="sxs-lookup"><span data-stu-id="12bb8-103">Gets a network interface IP configuration for a network interface.</span></span>

## <span data-ttu-id="12bb8-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="12bb8-104">SYNTAX</span></span>

```
Get-AzNetworkInterfaceIpConfig [-Name <String>] -NetworkInterface <PSNetworkInterface>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="12bb8-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="12bb8-105">DESCRIPTION</span></span>
<span data-ttu-id="12bb8-106">Das Cmdlet " **Get-AzNetworkInterfaceIPConfig** " Ruft eine Netzwerkschnittstellen-IP-Konfiguration über eine Azure-Netzwerkschnittstelle ab.</span><span class="sxs-lookup"><span data-stu-id="12bb8-106">The **Get-AzNetworkInterfaceIPConfig** cmdlet gets a network interface IP configuration from an Azure network interface.</span></span>

## <span data-ttu-id="12bb8-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="12bb8-107">EXAMPLES</span></span>

### <span data-ttu-id="12bb8-108">1: Abrufen einer IP-Konfiguration einer Netzwerkschnittstelle</span><span class="sxs-lookup"><span data-stu-id="12bb8-108">1: Get an IP configuration of a network interface</span></span>
```
$nic1 = Get-AzNetworkInterface -Name mynic -ResourceGroupName $myrg
Get-AzNetworkInterfaceIpConfig -Name ipconfig1 -NetworkInterface $nic1
```

<span data-ttu-id="12bb8-109">Der erste Befehl ruft eine vorhandene Netzwerkschnittstelle namens mynic ab und speichert Sie in der Variablen $NIC 1.</span><span class="sxs-lookup"><span data-stu-id="12bb8-109">The first command gets an existing network interface called mynic and stores it in the variable $nic1.</span></span> <span data-ttu-id="12bb8-110">Der zweite Befehl ruft die IP-Konfiguration mit dem Namen ipconfig1 dieser Netzwerkschnittstelle ab.</span><span class="sxs-lookup"><span data-stu-id="12bb8-110">The second command gets the IP configuration called ipconfig1 of this network interface.</span></span>
    

## <span data-ttu-id="12bb8-111">Parameter</span><span class="sxs-lookup"><span data-stu-id="12bb8-111">PARAMETERS</span></span>

### <span data-ttu-id="12bb8-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="12bb8-112">-DefaultProfile</span></span>
<span data-ttu-id="12bb8-113">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="12bb8-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="12bb8-114">-Name</span><span class="sxs-lookup"><span data-stu-id="12bb8-114">-Name</span></span>
<span data-ttu-id="12bb8-115">Gibt den Namen der Netzwerk-IP-Konfiguration an, die dieses Cmdlet erhält.</span><span class="sxs-lookup"><span data-stu-id="12bb8-115">Specifies the name of the network IP configuration that this cmdlet gets.</span></span>

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

### <span data-ttu-id="12bb8-116">-Network Interface</span><span class="sxs-lookup"><span data-stu-id="12bb8-116">-NetworkInterface</span></span>
<span data-ttu-id="12bb8-117">Gibt ein **Network Interface** -Objekt an, das die Netzwerk-IP-Konfiguration enthält, die dieses Cmdlet erhält.</span><span class="sxs-lookup"><span data-stu-id="12bb8-117">Specifies a **NetworkInterface** object that contains the network IP configuration that this cmdlet gets.</span></span>

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

### <span data-ttu-id="12bb8-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="12bb8-118">CommonParameters</span></span>
<span data-ttu-id="12bb8-119">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="12bb8-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="12bb8-120">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="12bb8-120">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="12bb8-121">Eingaben</span><span class="sxs-lookup"><span data-stu-id="12bb8-121">INPUTS</span></span>

### <span data-ttu-id="12bb8-122">Microsoft. Azure. Commands. Network. Models. PSNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="12bb8-122">Microsoft.Azure.Commands.Network.Models.PSNetworkInterface</span></span>

## <span data-ttu-id="12bb8-123">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="12bb8-123">OUTPUTS</span></span>

### <span data-ttu-id="12bb8-124">Microsoft. Azure. Commands. Network. Models. PSNetworkInterfaceIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="12bb8-124">Microsoft.Azure.Commands.Network.Models.PSNetworkInterfaceIPConfiguration</span></span>

## <span data-ttu-id="12bb8-125">Notizen</span><span class="sxs-lookup"><span data-stu-id="12bb8-125">NOTES</span></span>
* <span data-ttu-id="12bb8-126">Schlüsselwörter: Azure, azurerm, arm, Resource, Management, Manager, Netzwerk, Netzwerke</span><span class="sxs-lookup"><span data-stu-id="12bb8-126">Keywords: azure, azurerm, arm, resource, management, manager, network, networking</span></span>

## <span data-ttu-id="12bb8-127">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="12bb8-127">RELATED LINKS</span></span>

[<span data-ttu-id="12bb8-128">Add-AzNetworkInterfaceIpConfig</span><span class="sxs-lookup"><span data-stu-id="12bb8-128">Add-AzNetworkInterfaceIpConfig</span></span>](./Add-AzNetworkInterfaceIpConfig.md)

[<span data-ttu-id="12bb8-129">Neu – AzNetworkInterfaceIpConfig</span><span class="sxs-lookup"><span data-stu-id="12bb8-129">New-AzNetworkInterfaceIpConfig</span></span>](./New-AzNetworkInterfaceIpConfig.md)

[<span data-ttu-id="12bb8-130">Remove-AzNetworkInterfaceIpConfig</span><span class="sxs-lookup"><span data-stu-id="12bb8-130">Remove-AzNetworkInterfaceIpConfig</span></span>](./Remove-AzNetworkInterfaceIpConfig.md)

[<span data-ttu-id="12bb8-131">Satz-AzNetworkInterfaceIpConfig</span><span class="sxs-lookup"><span data-stu-id="12bb8-131">Set-AzNetworkInterfaceIpConfig</span></span>](./Set-AzNetworkInterfaceIpConfig.md)


