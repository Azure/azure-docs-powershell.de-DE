---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 1B39809C-90DA-4ECB-B949-D4A9A54ED982
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermnetworkinterfaceipconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmNetworkInterfaceIpConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmNetworkInterfaceIpConfig.md
ms.openlocfilehash: 3d3185762c6bb60d59ef15a129b4055939b49213
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93505466"
---
# <span data-ttu-id="9ad3e-101">Get-AzureRmNetworkInterfaceIpConfig</span><span class="sxs-lookup"><span data-stu-id="9ad3e-101">Get-AzureRmNetworkInterfaceIpConfig</span></span>

## <span data-ttu-id="9ad3e-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="9ad3e-102">SYNOPSIS</span></span>
<span data-ttu-id="9ad3e-103">Ruft eine Netzwerkschnittstellen-IP-Konfiguration für eine Netzwerkschnittstelle ab.</span><span class="sxs-lookup"><span data-stu-id="9ad3e-103">Gets a network interface IP configuration for a network interface.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="9ad3e-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="9ad3e-104">SYNTAX</span></span>

```
Get-AzureRmNetworkInterfaceIpConfig [-Name <String>] -NetworkInterface <PSNetworkInterface>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="9ad3e-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="9ad3e-105">DESCRIPTION</span></span>
<span data-ttu-id="9ad3e-106">Das Cmdlet " **Get-AzureRmNetworkInterfaceIPConfig** " Ruft eine Netzwerkschnittstellen-IP-Konfiguration über eine Azure-Netzwerkschnittstelle ab.</span><span class="sxs-lookup"><span data-stu-id="9ad3e-106">The **Get-AzureRmNetworkInterfaceIPConfig** cmdlet gets a network interface IP configuration from an Azure network interface.</span></span>

## <span data-ttu-id="9ad3e-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="9ad3e-107">EXAMPLES</span></span>

### <span data-ttu-id="9ad3e-108">1: Abrufen einer IP-Konfiguration einer Netzwerkschnittstelle</span><span class="sxs-lookup"><span data-stu-id="9ad3e-108">1: Get an IP configuration of a network interface</span></span>
```
$nic1 = Get-AzureRmNetworkInterface -Name mynic -ResourceGroupName $myrg
Get-AzureRmNetworkInterfaceIpConfig -Name ipconfig1 -NetworkInterface $nic1
```

<span data-ttu-id="9ad3e-109">Der erste Befehl ruft eine vorhandene Netzwerkschnittstelle namens mynic ab und speichert Sie in der Variablen $NIC 1.</span><span class="sxs-lookup"><span data-stu-id="9ad3e-109">The first command gets an existing network interface called mynic and stores it in the variable $nic1.</span></span> <span data-ttu-id="9ad3e-110">Der zweite Befehl ruft die IP-Konfiguration mit dem Namen ipconfig1 dieser Netzwerkschnittstelle ab.</span><span class="sxs-lookup"><span data-stu-id="9ad3e-110">The second command gets the IP configuration called ipconfig1 of this network interface.</span></span>
    

## <span data-ttu-id="9ad3e-111">Parameter</span><span class="sxs-lookup"><span data-stu-id="9ad3e-111">PARAMETERS</span></span>

### <span data-ttu-id="9ad3e-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9ad3e-112">-DefaultProfile</span></span>
<span data-ttu-id="9ad3e-113">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="9ad3e-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="9ad3e-114">-Name</span><span class="sxs-lookup"><span data-stu-id="9ad3e-114">-Name</span></span>
<span data-ttu-id="9ad3e-115">Gibt den Namen der Netzwerk-IP-Konfiguration an, die dieses Cmdlet erhält.</span><span class="sxs-lookup"><span data-stu-id="9ad3e-115">Specifies the name of the network IP configuration that this cmdlet gets.</span></span>

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

### <span data-ttu-id="9ad3e-116">-Network Interface</span><span class="sxs-lookup"><span data-stu-id="9ad3e-116">-NetworkInterface</span></span>
<span data-ttu-id="9ad3e-117">Gibt ein **Network Interface** -Objekt an, das die Netzwerk-IP-Konfiguration enthält, die dieses Cmdlet erhält.</span><span class="sxs-lookup"><span data-stu-id="9ad3e-117">Specifies a **NetworkInterface** object that contains the network IP configuration that this cmdlet gets.</span></span>

```yaml
Type: PSNetworkInterface
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="9ad3e-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9ad3e-118">CommonParameters</span></span>
<span data-ttu-id="9ad3e-119">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9ad3e-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9ad3e-120">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9ad3e-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9ad3e-121">Eingaben</span><span class="sxs-lookup"><span data-stu-id="9ad3e-121">INPUTS</span></span>

### <span data-ttu-id="9ad3e-122">PSNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="9ad3e-122">PSNetworkInterface</span></span>
<span data-ttu-id="9ad3e-123">Der Parameter "Network Interface" akzeptiert den Wert vom Typ "PSNetworkInterface" aus der Pipeline.</span><span class="sxs-lookup"><span data-stu-id="9ad3e-123">Parameter 'NetworkInterface' accepts value of type 'PSNetworkInterface' from the pipeline</span></span>

## <span data-ttu-id="9ad3e-124">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="9ad3e-124">OUTPUTS</span></span>

### <span data-ttu-id="9ad3e-125">Microsoft. Azure. Commands. Network. Models. PSNetworkInterfaceIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="9ad3e-125">Microsoft.Azure.Commands.Network.Models.PSNetworkInterfaceIPConfiguration</span></span>

## <span data-ttu-id="9ad3e-126">Notizen</span><span class="sxs-lookup"><span data-stu-id="9ad3e-126">NOTES</span></span>
* <span data-ttu-id="9ad3e-127">Schlüsselwörter: Azure, azurerm, arm, Resource, Management, Manager, Netzwerk, Netzwerke</span><span class="sxs-lookup"><span data-stu-id="9ad3e-127">Keywords: azure, azurerm, arm, resource, management, manager, network, networking</span></span>

## <span data-ttu-id="9ad3e-128">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="9ad3e-128">RELATED LINKS</span></span>

[<span data-ttu-id="9ad3e-129">Add-AzureRmNetworkInterfaceIpConfig</span><span class="sxs-lookup"><span data-stu-id="9ad3e-129">Add-AzureRmNetworkInterfaceIpConfig</span></span>](./Add-AzureRmNetworkInterfaceIpConfig.md)

[<span data-ttu-id="9ad3e-130">Neu – AzureRmNetworkInterfaceIpConfig</span><span class="sxs-lookup"><span data-stu-id="9ad3e-130">New-AzureRmNetworkInterfaceIpConfig</span></span>](./New-AzureRmNetworkInterfaceIpConfig.md)

[<span data-ttu-id="9ad3e-131">Remove-AzureRmNetworkInterfaceIpConfig</span><span class="sxs-lookup"><span data-stu-id="9ad3e-131">Remove-AzureRmNetworkInterfaceIpConfig</span></span>](./Remove-AzureRmNetworkInterfaceIpConfig.md)

[<span data-ttu-id="9ad3e-132">Satz-AzureRmNetworkInterfaceIpConfig</span><span class="sxs-lookup"><span data-stu-id="9ad3e-132">Set-AzureRmNetworkInterfaceIpConfig</span></span>](./Set-AzureRmNetworkInterfaceIpConfig.md)


