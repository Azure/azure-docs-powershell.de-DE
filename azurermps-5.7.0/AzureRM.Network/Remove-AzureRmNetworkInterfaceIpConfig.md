---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 015C7DB7-2B08-4033-9B6E-1738D4DDACDA
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/remove-azurermnetworkinterfaceipconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmNetworkInterfaceIpConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmNetworkInterfaceIpConfig.md
ms.openlocfilehash: 9cbb814fde6d81449228a18913254cf807d5502c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93478401"
---
# <span data-ttu-id="0f7cc-101">Remove-AzureRmNetworkInterfaceIpConfig</span><span class="sxs-lookup"><span data-stu-id="0f7cc-101">Remove-AzureRmNetworkInterfaceIpConfig</span></span>

## <span data-ttu-id="0f7cc-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="0f7cc-102">SYNOPSIS</span></span>
<span data-ttu-id="0f7cc-103">Entfernt eine Netzwerkschnittstellen-IP-Konfiguration von einer Netzwerkschnittstelle.</span><span class="sxs-lookup"><span data-stu-id="0f7cc-103">Removes a network interface IP configuration from a network interface.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="0f7cc-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="0f7cc-104">SYNTAX</span></span>

```
Remove-AzureRmNetworkInterfaceIpConfig -Name <String> -NetworkInterface <PSNetworkInterface>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="0f7cc-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="0f7cc-105">DESCRIPTION</span></span>
<span data-ttu-id="0f7cc-106">Das Cmdlet **Remove-AzureRmNetworkInterfaceIpConfig** entfernt eine Netzwerkschnittstellen-IP-Konfiguration über eine Azure-Netzwerkschnittstelle.</span><span class="sxs-lookup"><span data-stu-id="0f7cc-106">The **Remove-AzureRmNetworkInterfaceIpConfig** cmdlet removes a network interface IP configuration from an Azure network interface.</span></span>

## <span data-ttu-id="0f7cc-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="0f7cc-107">EXAMPLES</span></span>

### <span data-ttu-id="0f7cc-108">1: Löschen einer IP-Konfiguration über eine Netzwerkschnittstelle</span><span class="sxs-lookup"><span data-stu-id="0f7cc-108">1: Delete an IP configuration from a network interface</span></span>
```
$nic = Get-AzureRmNetworkInterface -Name mynic -ResourceGroupName myrg

Remove-AzureRmNetworkInterfaceIpConfig -Name IPConfig-1 -NetworkInterface $nic
```

<span data-ttu-id="0f7cc-109">Der erste Befehl ruft eine Netzwerkschnittstelle mit dem Namen mynic ab und speichert Sie in der Variablen $NIC.</span><span class="sxs-lookup"><span data-stu-id="0f7cc-109">The first command gets a network interface called mynic and stores it in the variable $nic.</span></span> <span data-ttu-id="0f7cc-110">Der zweite Befehl entfernt die IP-Konfiguration mit dem Namen ipconfig-1, die dieser Netzwerkschnittstelle zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="0f7cc-110">The second command removes the IP configuration called IPConfig-1 associated with this network interface.</span></span>

## <span data-ttu-id="0f7cc-111">Parameter</span><span class="sxs-lookup"><span data-stu-id="0f7cc-111">PARAMETERS</span></span>

### <span data-ttu-id="0f7cc-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0f7cc-112">-DefaultProfile</span></span>
<span data-ttu-id="0f7cc-113">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="0f7cc-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="0f7cc-114">-Name</span><span class="sxs-lookup"><span data-stu-id="0f7cc-114">-Name</span></span>
<span data-ttu-id="0f7cc-115">Gibt den Namen der zu entfernenden Netzwerkschnittstellen-IP-Konfiguration an.</span><span class="sxs-lookup"><span data-stu-id="0f7cc-115">Specifies the name of the network interface IP configuration to remove.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0f7cc-116">-Network Interface</span><span class="sxs-lookup"><span data-stu-id="0f7cc-116">-NetworkInterface</span></span>
<span data-ttu-id="0f7cc-117">Gibt ein **Network Interface** -Objekt an.</span><span class="sxs-lookup"><span data-stu-id="0f7cc-117">Specifies a **NetworkInterface** object.</span></span>
<span data-ttu-id="0f7cc-118">Dieses Objekt enthält die zu entfernende Netzwerkschnittstellen-IP-Konfiguration.</span><span class="sxs-lookup"><span data-stu-id="0f7cc-118">This object contains the network interface IP configuration to remove.</span></span>

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

### <span data-ttu-id="0f7cc-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0f7cc-119">CommonParameters</span></span>
<span data-ttu-id="0f7cc-120">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0f7cc-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0f7cc-121">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0f7cc-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0f7cc-122">Eingaben</span><span class="sxs-lookup"><span data-stu-id="0f7cc-122">INPUTS</span></span>

### <span data-ttu-id="0f7cc-123">PSNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="0f7cc-123">PSNetworkInterface</span></span>
<span data-ttu-id="0f7cc-124">Der Parameter "Network Interface" akzeptiert den Wert vom Typ "PSNetworkInterface" aus der Pipeline.</span><span class="sxs-lookup"><span data-stu-id="0f7cc-124">Parameter 'NetworkInterface' accepts value of type 'PSNetworkInterface' from the pipeline</span></span>

## <span data-ttu-id="0f7cc-125">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="0f7cc-125">OUTPUTS</span></span>

### <span data-ttu-id="0f7cc-126">Microsoft. Azure. Commands. Network. Models. PSNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="0f7cc-126">Microsoft.Azure.Commands.Network.Models.PSNetworkInterface</span></span>

## <span data-ttu-id="0f7cc-127">Notizen</span><span class="sxs-lookup"><span data-stu-id="0f7cc-127">NOTES</span></span>
* <span data-ttu-id="0f7cc-128">Schlüsselwörter: Azure, azurerm, arm, Resource, Management, Manager, Netzwerk, Netzwerke</span><span class="sxs-lookup"><span data-stu-id="0f7cc-128">Keywords: azure, azurerm, arm, resource, management, manager, network, networking</span></span>

## <span data-ttu-id="0f7cc-129">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="0f7cc-129">RELATED LINKS</span></span>

[<span data-ttu-id="0f7cc-130">Add-AzureRmNetworkInterfaceIpConfig</span><span class="sxs-lookup"><span data-stu-id="0f7cc-130">Add-AzureRmNetworkInterfaceIpConfig</span></span>](./Add-AzureRmNetworkInterfaceIpConfig.md)

[<span data-ttu-id="0f7cc-131">Get-AzureRmNetworkInterfaceIpConfig</span><span class="sxs-lookup"><span data-stu-id="0f7cc-131">Get-AzureRmNetworkInterfaceIpConfig</span></span>](./Get-AzureRmNetworkInterfaceIpConfig.md)

[<span data-ttu-id="0f7cc-132">Neu – AzureRmNetworkInterfaceIpConfig</span><span class="sxs-lookup"><span data-stu-id="0f7cc-132">New-AzureRmNetworkInterfaceIpConfig</span></span>](./New-AzureRmNetworkInterfaceIpConfig.md)

[<span data-ttu-id="0f7cc-133">Satz-AzureRmNetworkInterfaceIpConfig</span><span class="sxs-lookup"><span data-stu-id="0f7cc-133">Set-AzureRmNetworkInterfaceIpConfig</span></span>](./Set-AzureRmNetworkInterfaceIpConfig.md)


