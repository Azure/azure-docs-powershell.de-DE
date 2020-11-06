---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 015C7DB7-2B08-4033-9B6E-1738D4DDACDA
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/remove-azurermnetworkinterfaceipconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmNetworkInterfaceIpConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmNetworkInterfaceIpConfig.md
ms.openlocfilehash: c912d32c39380ee3d653fa228632a4d01f0e3049
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93495885"
---
# <span data-ttu-id="800ea-101">Remove-AzureRmNetworkInterfaceIpConfig</span><span class="sxs-lookup"><span data-stu-id="800ea-101">Remove-AzureRmNetworkInterfaceIpConfig</span></span>

## <span data-ttu-id="800ea-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="800ea-102">SYNOPSIS</span></span>
<span data-ttu-id="800ea-103">Entfernt eine Netzwerkschnittstellen-IP-Konfiguration von einer Netzwerkschnittstelle.</span><span class="sxs-lookup"><span data-stu-id="800ea-103">Removes a network interface IP configuration from a network interface.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="800ea-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="800ea-104">SYNTAX</span></span>

```
Remove-AzureRmNetworkInterfaceIpConfig -Name <String> -NetworkInterface <PSNetworkInterface>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="800ea-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="800ea-105">DESCRIPTION</span></span>
<span data-ttu-id="800ea-106">Das Cmdlet **Remove-AzureRmNetworkInterfaceIpConfig** entfernt eine Netzwerkschnittstellen-IP-Konfiguration über eine Azure-Netzwerkschnittstelle.</span><span class="sxs-lookup"><span data-stu-id="800ea-106">The **Remove-AzureRmNetworkInterfaceIpConfig** cmdlet removes a network interface IP configuration from an Azure network interface.</span></span>

## <span data-ttu-id="800ea-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="800ea-107">EXAMPLES</span></span>

### <span data-ttu-id="800ea-108">1: Löschen einer IP-Konfiguration über eine Netzwerkschnittstelle</span><span class="sxs-lookup"><span data-stu-id="800ea-108">1: Delete an IP configuration from a network interface</span></span>
```
$nic = Get-AzureRmNetworkInterface -Name mynic -ResourceGroupName myrg

Remove-AzureRmNetworkInterfaceIpConfig -Name IPConfig-1 -NetworkInterface $nic
```

<span data-ttu-id="800ea-109">Der erste Befehl ruft eine Netzwerkschnittstelle mit dem Namen mynic ab und speichert Sie in der Variablen $NIC.</span><span class="sxs-lookup"><span data-stu-id="800ea-109">The first command gets a network interface called mynic and stores it in the variable $nic.</span></span> <span data-ttu-id="800ea-110">Der zweite Befehl entfernt die IP-Konfiguration mit dem Namen ipconfig-1, die dieser Netzwerkschnittstelle zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="800ea-110">The second command removes the IP configuration called IPConfig-1 associated with this network interface.</span></span>

## <span data-ttu-id="800ea-111">Parameter</span><span class="sxs-lookup"><span data-stu-id="800ea-111">PARAMETERS</span></span>

### <span data-ttu-id="800ea-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="800ea-112">-DefaultProfile</span></span>
<span data-ttu-id="800ea-113">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="800ea-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="800ea-114">-Name</span><span class="sxs-lookup"><span data-stu-id="800ea-114">-Name</span></span>
<span data-ttu-id="800ea-115">Gibt den Namen der zu entfernenden Netzwerkschnittstellen-IP-Konfiguration an.</span><span class="sxs-lookup"><span data-stu-id="800ea-115">Specifies the name of the network interface IP configuration to remove.</span></span>

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

### <span data-ttu-id="800ea-116">-Network Interface</span><span class="sxs-lookup"><span data-stu-id="800ea-116">-NetworkInterface</span></span>
<span data-ttu-id="800ea-117">Gibt ein **Network Interface** -Objekt an.</span><span class="sxs-lookup"><span data-stu-id="800ea-117">Specifies a **NetworkInterface** object.</span></span>
<span data-ttu-id="800ea-118">Dieses Objekt enthält die zu entfernende Netzwerkschnittstellen-IP-Konfiguration.</span><span class="sxs-lookup"><span data-stu-id="800ea-118">This object contains the network interface IP configuration to remove.</span></span>

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

### <span data-ttu-id="800ea-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="800ea-119">CommonParameters</span></span>
<span data-ttu-id="800ea-120">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="800ea-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="800ea-121">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="800ea-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="800ea-122">Eingaben</span><span class="sxs-lookup"><span data-stu-id="800ea-122">INPUTS</span></span>

### <span data-ttu-id="800ea-123">Microsoft. Azure. Commands. Network. Models. PSNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="800ea-123">Microsoft.Azure.Commands.Network.Models.PSNetworkInterface</span></span>
<span data-ttu-id="800ea-124">Parameter: Network Interface (ByValue)</span><span class="sxs-lookup"><span data-stu-id="800ea-124">Parameters: NetworkInterface (ByValue)</span></span>

## <span data-ttu-id="800ea-125">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="800ea-125">OUTPUTS</span></span>

### <span data-ttu-id="800ea-126">Microsoft. Azure. Commands. Network. Models. PSNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="800ea-126">Microsoft.Azure.Commands.Network.Models.PSNetworkInterface</span></span>

## <span data-ttu-id="800ea-127">Notizen</span><span class="sxs-lookup"><span data-stu-id="800ea-127">NOTES</span></span>
* <span data-ttu-id="800ea-128">Schlüsselwörter: Azure, azurerm, arm, Resource, Management, Manager, Netzwerk, Netzwerke</span><span class="sxs-lookup"><span data-stu-id="800ea-128">Keywords: azure, azurerm, arm, resource, management, manager, network, networking</span></span>

## <span data-ttu-id="800ea-129">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="800ea-129">RELATED LINKS</span></span>

[<span data-ttu-id="800ea-130">Add-AzureRmNetworkInterfaceIpConfig</span><span class="sxs-lookup"><span data-stu-id="800ea-130">Add-AzureRmNetworkInterfaceIpConfig</span></span>](./Add-AzureRmNetworkInterfaceIpConfig.md)

[<span data-ttu-id="800ea-131">Get-AzureRmNetworkInterfaceIpConfig</span><span class="sxs-lookup"><span data-stu-id="800ea-131">Get-AzureRmNetworkInterfaceIpConfig</span></span>](./Get-AzureRmNetworkInterfaceIpConfig.md)

[<span data-ttu-id="800ea-132">Neu – AzureRmNetworkInterfaceIpConfig</span><span class="sxs-lookup"><span data-stu-id="800ea-132">New-AzureRmNetworkInterfaceIpConfig</span></span>](./New-AzureRmNetworkInterfaceIpConfig.md)

[<span data-ttu-id="800ea-133">Satz-AzureRmNetworkInterfaceIpConfig</span><span class="sxs-lookup"><span data-stu-id="800ea-133">Set-AzureRmNetworkInterfaceIpConfig</span></span>](./Set-AzureRmNetworkInterfaceIpConfig.md)


