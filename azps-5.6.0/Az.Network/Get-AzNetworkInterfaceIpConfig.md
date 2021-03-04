---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 1B39809C-90DA-4ECB-B949-D4A9A54ED982
online version: https://docs.microsoft.com/powershell/module/az.network/get-aznetworkinterfaceipconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzNetworkInterfaceIpConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzNetworkInterfaceIpConfig.md
ms.openlocfilehash: 572ea4aac029068e3b7e4fbcf12f3b240129d585
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101945965"
---
# <span data-ttu-id="02e8a-101">Get-AzNetworkInterfaceIpConfig</span><span class="sxs-lookup"><span data-stu-id="02e8a-101">Get-AzNetworkInterfaceIpConfig</span></span>

## <span data-ttu-id="02e8a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="02e8a-102">SYNOPSIS</span></span>
<span data-ttu-id="02e8a-103">Ruft eine NETZWERKSCHNITTSTELLEN-IP-Konfiguration für eine Netzwerkschnittstelle ab.</span><span class="sxs-lookup"><span data-stu-id="02e8a-103">Gets a network interface IP configuration for a network interface.</span></span>

## <span data-ttu-id="02e8a-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="02e8a-104">SYNTAX</span></span>

```
Get-AzNetworkInterfaceIpConfig [-Name <String>] -NetworkInterface <PSNetworkInterface>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="02e8a-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="02e8a-105">DESCRIPTION</span></span>
<span data-ttu-id="02e8a-106">Das **Get-AzNetworkInterfaceIPConfig-Cmdlet** ruft eine NETZWERKSCHNITTSTELLEN-IP-Konfiguration von einer Azure-Netzwerkschnittstelle ab.</span><span class="sxs-lookup"><span data-stu-id="02e8a-106">The **Get-AzNetworkInterfaceIPConfig** cmdlet gets a network interface IP configuration from an Azure network interface.</span></span>

## <span data-ttu-id="02e8a-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="02e8a-107">EXAMPLES</span></span>

### <span data-ttu-id="02e8a-108">1: Erhalten einer IP-Konfiguration einer Netzwerkschnittstelle</span><span class="sxs-lookup"><span data-stu-id="02e8a-108">1: Get an IP configuration of a network interface</span></span>
```
$nic1 = Get-AzNetworkInterface -Name mynic -ResourceGroupName $myrg
Get-AzNetworkInterfaceIpConfig -Name ipconfig1 -NetworkInterface $nic1
```

<span data-ttu-id="02e8a-109">Der erste Befehl ruft eine vorhandene Netzwerkschnittstelle namens mynic ab und speichert sie in der Variablen $nic 1.</span><span class="sxs-lookup"><span data-stu-id="02e8a-109">The first command gets an existing network interface called mynic and stores it in the variable $nic1.</span></span> <span data-ttu-id="02e8a-110">Der zweite Befehl ruft die IP-Konfiguration "ipconfig1" dieser Netzwerkschnittstelle ab.</span><span class="sxs-lookup"><span data-stu-id="02e8a-110">The second command gets the IP configuration called ipconfig1 of this network interface.</span></span>
    

## <span data-ttu-id="02e8a-111">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="02e8a-111">PARAMETERS</span></span>

### <span data-ttu-id="02e8a-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="02e8a-112">-DefaultProfile</span></span>
<span data-ttu-id="02e8a-113">Die Anmeldeinformationen, das Konto, der Mandant und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="02e8a-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="02e8a-114">-Name</span><span class="sxs-lookup"><span data-stu-id="02e8a-114">-Name</span></span>
<span data-ttu-id="02e8a-115">Gibt den Namen der Netzwerk-IP-Konfiguration an, die dieses Cmdlet erhält.</span><span class="sxs-lookup"><span data-stu-id="02e8a-115">Specifies the name of the network IP configuration that this cmdlet gets.</span></span>

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

### <span data-ttu-id="02e8a-116">-NetworkInterface</span><span class="sxs-lookup"><span data-stu-id="02e8a-116">-NetworkInterface</span></span>
<span data-ttu-id="02e8a-117">Gibt ein **NetworkInterface-Objekt** an, das die Netzwerk-IP-Konfiguration enthält, die dieses Cmdlet erhält.</span><span class="sxs-lookup"><span data-stu-id="02e8a-117">Specifies a **NetworkInterface** object that contains the network IP configuration that this cmdlet gets.</span></span>

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

### <span data-ttu-id="02e8a-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="02e8a-118">CommonParameters</span></span>
<span data-ttu-id="02e8a-119">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="02e8a-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="02e8a-120">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="02e8a-120">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="02e8a-121">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="02e8a-121">INPUTS</span></span>

### <span data-ttu-id="02e8a-122">Microsoft.Azure.Commands.Network.Models.PSNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="02e8a-122">Microsoft.Azure.Commands.Network.Models.PSNetworkInterface</span></span>

## <span data-ttu-id="02e8a-123">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="02e8a-123">OUTPUTS</span></span>

### <span data-ttu-id="02e8a-124">Microsoft.Azure.Commands.Network.Models.PSNetworkInterfaceIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="02e8a-124">Microsoft.Azure.Commands.Network.Models.PSNetworkInterfaceIPConfiguration</span></span>

## <span data-ttu-id="02e8a-125">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="02e8a-125">NOTES</span></span>
* <span data-ttu-id="02e8a-126">Schlüsselwörter: azure, azurerm, arm, resource, management, manager, network, networking</span><span class="sxs-lookup"><span data-stu-id="02e8a-126">Keywords: azure, azurerm, arm, resource, management, manager, network, networking</span></span>

## <span data-ttu-id="02e8a-127">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="02e8a-127">RELATED LINKS</span></span>

[<span data-ttu-id="02e8a-128">Add-AzNetworkInterfaceIpConfig</span><span class="sxs-lookup"><span data-stu-id="02e8a-128">Add-AzNetworkInterfaceIpConfig</span></span>](./Add-AzNetworkInterfaceIpConfig.md)

[<span data-ttu-id="02e8a-129">New-AzNetworkInterfaceIpConfig</span><span class="sxs-lookup"><span data-stu-id="02e8a-129">New-AzNetworkInterfaceIpConfig</span></span>](./New-AzNetworkInterfaceIpConfig.md)

[<span data-ttu-id="02e8a-130">Remove-AzNetworkInterfaceIpConfig</span><span class="sxs-lookup"><span data-stu-id="02e8a-130">Remove-AzNetworkInterfaceIpConfig</span></span>](./Remove-AzNetworkInterfaceIpConfig.md)

[<span data-ttu-id="02e8a-131">Set-AzNetworkInterfaceIpConfig</span><span class="sxs-lookup"><span data-stu-id="02e8a-131">Set-AzNetworkInterfaceIpConfig</span></span>](./Set-AzNetworkInterfaceIpConfig.md)


