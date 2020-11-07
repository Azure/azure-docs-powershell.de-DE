---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 9CBF592E-734B-4A0C-A45D-358C226D08C7
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azvirtualnetworkgateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Get-AzVirtualNetworkGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Get-AzVirtualNetworkGateway.md
ms.openlocfilehash: 490e61142bdbc0bcdd64f18aeeb2fa527e5180b9
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/16/2020
ms.locfileid: "93841516"
---
# <span data-ttu-id="ed7ae-101">Get-AzVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="ed7ae-101">Get-AzVirtualNetworkGateway</span></span>

## <span data-ttu-id="ed7ae-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="ed7ae-102">SYNOPSIS</span></span>
<span data-ttu-id="ed7ae-103">Ruft ein virtuelles Netzwerk Gateway ab</span><span class="sxs-lookup"><span data-stu-id="ed7ae-103">Gets a Virtual Network Gateway</span></span>

## <span data-ttu-id="ed7ae-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="ed7ae-104">SYNTAX</span></span>

```
Get-AzVirtualNetworkGateway [-Name <String>] -ResourceGroupName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ed7ae-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="ed7ae-105">DESCRIPTION</span></span>
<span data-ttu-id="ed7ae-106">Das virtuelle Netzwerkgateway ist das Objekt, das Ihr Gateway in Azure darstellt.</span><span class="sxs-lookup"><span data-stu-id="ed7ae-106">The Virtual Network Gateway is the object representing your gateway in Azure.</span></span>

<span data-ttu-id="ed7ae-107">Das Cmdlet " **Get-AzVirtualNetworkGateway** " gibt das Objekt Ihres Gateways in Azure basierend auf Name und Ressourcengruppennamen zurück.</span><span class="sxs-lookup"><span data-stu-id="ed7ae-107">The **Get-AzVirtualNetworkGateway** cmdlet returns the object of your gateway in Azure based on Name and Resource Group Name.</span></span>

## <span data-ttu-id="ed7ae-108">Beispiele</span><span class="sxs-lookup"><span data-stu-id="ed7ae-108">EXAMPLES</span></span>

### <span data-ttu-id="ed7ae-109">1: Abrufen eines virtuellen Netzwerkgateways</span><span class="sxs-lookup"><span data-stu-id="ed7ae-109">1: Get a Virtual Network Gateway</span></span>
```
Get-AzVirtualNetworkGateway -Name myGateway -ResourceGroupName myRG
```

<span data-ttu-id="ed7ae-110">Gibt das Objekt des virtuellen Netzwerkgateways mit dem Namen "mygateway" innerhalb der Ressourcengruppe "myRG" zurück.</span><span class="sxs-lookup"><span data-stu-id="ed7ae-110">Returns the object of the Virtual Network Gateway with the name "myGateway" within the resource group "myRG"</span></span>

## <span data-ttu-id="ed7ae-111">Parameter</span><span class="sxs-lookup"><span data-stu-id="ed7ae-111">PARAMETERS</span></span>

### <span data-ttu-id="ed7ae-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ed7ae-112">-DefaultProfile</span></span>
<span data-ttu-id="ed7ae-113">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="ed7ae-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ed7ae-114">-Name</span><span class="sxs-lookup"><span data-stu-id="ed7ae-114">-Name</span></span>
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

### <span data-ttu-id="ed7ae-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ed7ae-115">-ResourceGroupName</span></span>
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

### <span data-ttu-id="ed7ae-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ed7ae-116">CommonParameters</span></span>
<span data-ttu-id="ed7ae-117">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ed7ae-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ed7ae-118">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ed7ae-118">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ed7ae-119">Eingaben</span><span class="sxs-lookup"><span data-stu-id="ed7ae-119">INPUTS</span></span>

## <span data-ttu-id="ed7ae-120">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="ed7ae-120">OUTPUTS</span></span>

### <span data-ttu-id="ed7ae-121">Microsoft. Azure. Commands. Network. Models. PSVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="ed7ae-121">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway</span></span>

## <span data-ttu-id="ed7ae-122">Notizen</span><span class="sxs-lookup"><span data-stu-id="ed7ae-122">NOTES</span></span>

## <span data-ttu-id="ed7ae-123">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="ed7ae-123">RELATED LINKS</span></span>

