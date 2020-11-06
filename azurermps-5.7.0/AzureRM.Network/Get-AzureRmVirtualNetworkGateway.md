---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 9CBF592E-734B-4A0C-A45D-358C226D08C7
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermvirtualnetworkgateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmVirtualNetworkGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmVirtualNetworkGateway.md
ms.openlocfilehash: 29d5ad86d9df7bddec8be600d8b7c680c7bcd7fa
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93479706"
---
# <span data-ttu-id="23609-101">Get-AzureRmVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="23609-101">Get-AzureRmVirtualNetworkGateway</span></span>

## <span data-ttu-id="23609-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="23609-102">SYNOPSIS</span></span>
<span data-ttu-id="23609-103">Ruft ein virtuelles Netzwerk Gateway ab</span><span class="sxs-lookup"><span data-stu-id="23609-103">Gets a Virtual Network Gateway</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="23609-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="23609-104">SYNTAX</span></span>

```
Get-AzureRmVirtualNetworkGateway [-Name <String>] -ResourceGroupName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="23609-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="23609-105">DESCRIPTION</span></span>
<span data-ttu-id="23609-106">Das virtuelle Netzwerkgateway ist das Objekt, das Ihr Gateway in Azure darstellt.</span><span class="sxs-lookup"><span data-stu-id="23609-106">The Virtual Network Gateway is the object representing your gateway in Azure.</span></span>

<span data-ttu-id="23609-107">Das Cmdlet " **Get-AzureRmVirtualNetworkGateway** " gibt das Objekt Ihres Gateways in Azure basierend auf Name und Ressourcengruppennamen zurück.</span><span class="sxs-lookup"><span data-stu-id="23609-107">The **Get-AzureRmVirtualNetworkGateway** cmdlet returns the object of your gateway in Azure based on Name and Resource Group Name.</span></span>

## <span data-ttu-id="23609-108">Beispiele</span><span class="sxs-lookup"><span data-stu-id="23609-108">EXAMPLES</span></span>

### <span data-ttu-id="23609-109">1: Abrufen eines virtuellen Netzwerkgateways</span><span class="sxs-lookup"><span data-stu-id="23609-109">1: Get a Virtual Network Gateway</span></span>
```
Get-AzureRmVirtualNetworkGateway -Name myGateway -ResourceGroupName myRG
```

<span data-ttu-id="23609-110">Gibt das Objekt des virtuellen Netzwerkgateways mit dem Namen "mygateway" innerhalb der Ressourcengruppe "myRG" zurück.</span><span class="sxs-lookup"><span data-stu-id="23609-110">Returns the object of the Virtual Network Gateway with the name "myGateway" within the resource group "myRG"</span></span>

## <span data-ttu-id="23609-111">Parameter</span><span class="sxs-lookup"><span data-stu-id="23609-111">PARAMETERS</span></span>

### <span data-ttu-id="23609-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="23609-112">-DefaultProfile</span></span>
<span data-ttu-id="23609-113">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="23609-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="23609-114">-Name</span><span class="sxs-lookup"><span data-stu-id="23609-114">-Name</span></span>
```yaml
Type: String
Parameter Sets: (All)
Aliases: ResourceName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="23609-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="23609-115">-ResourceGroupName</span></span>
```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="23609-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="23609-116">CommonParameters</span></span>
<span data-ttu-id="23609-117">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="23609-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="23609-118">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="23609-118">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="23609-119">Eingaben</span><span class="sxs-lookup"><span data-stu-id="23609-119">INPUTS</span></span>

### <span data-ttu-id="23609-120">Keine</span><span class="sxs-lookup"><span data-stu-id="23609-120">None</span></span>
<span data-ttu-id="23609-121">Dieses Cmdlet akzeptiert keine Eingaben.</span><span class="sxs-lookup"><span data-stu-id="23609-121">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="23609-122">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="23609-122">OUTPUTS</span></span>

### <span data-ttu-id="23609-123">Microsoft. Azure. Commands. Network. Models. PSVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="23609-123">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway</span></span>

## <span data-ttu-id="23609-124">Notizen</span><span class="sxs-lookup"><span data-stu-id="23609-124">NOTES</span></span>

## <span data-ttu-id="23609-125">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="23609-125">RELATED LINKS</span></span>

