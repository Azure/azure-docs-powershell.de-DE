---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 85C0A1C3-FC6D-496A-B6B5-8DC2A73B8032
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/set-azurermapplicationgatewayfrontendport
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmApplicationGatewayFrontendPort.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmApplicationGatewayFrontendPort.md
ms.openlocfilehash: 7f373993c65bea695be254901a4981a37c40cdac
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93664627"
---
# <span data-ttu-id="2bcfb-101">Set-AzureRmApplicationGatewayFrontendPort</span><span class="sxs-lookup"><span data-stu-id="2bcfb-101">Set-AzureRmApplicationGatewayFrontendPort</span></span>

## <span data-ttu-id="2bcfb-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="2bcfb-102">SYNOPSIS</span></span>
<span data-ttu-id="2bcfb-103">Ändert einen Front-End-Port für ein Anwendungsgateway.</span><span class="sxs-lookup"><span data-stu-id="2bcfb-103">Modifies a front-end port for an application gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="2bcfb-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="2bcfb-104">SYNTAX</span></span>

```
Set-AzureRmApplicationGatewayFrontendPort -ApplicationGateway <PSApplicationGateway> -Name <String>
 -Port <Int32> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="2bcfb-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="2bcfb-105">DESCRIPTION</span></span>
<span data-ttu-id="2bcfb-106">Das Cmdlet " **Satz-AzureRmApplicationGatewayFrontendPort** " ändert einen Front-End-Port für ein Anwendungsgateway.</span><span class="sxs-lookup"><span data-stu-id="2bcfb-106">The **Set-AzureRmApplicationGatewayFrontendPort** cmdlet modifies a front-end port for an application gateway.</span></span>

## <span data-ttu-id="2bcfb-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="2bcfb-107">EXAMPLES</span></span>

### <span data-ttu-id="2bcfb-108">Beispiel 1: Einrichten eines Front-End-Ports für Application Gateway auf 80</span><span class="sxs-lookup"><span data-stu-id="2bcfb-108">Example 1: Set an application gateway front-end port to 80</span></span>
```
PS C:\> $AppGw = Get-AzureRmApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $AppGw = Set-AzureRmApplicationGatewayFrontendPort -ApplicationGateway $AppGw -Name "FrontEndPort01" -Port 80
```

<span data-ttu-id="2bcfb-109">Der erste Befehl ruft das Anwendungsgateway mit dem Namen ApplicationGateway01 ab, das zur Ressourcengruppe mit dem Namen ResourceGroup01 gehört, und speichert es in der $AppGw Variablen.</span><span class="sxs-lookup"><span data-stu-id="2bcfb-109">The first command gets the application gateway named ApplicationGateway01 that belongs to the resource group named ResourceGroup01 and stores it in the $AppGw variable.</span></span>

<span data-ttu-id="2bcfb-110">Der zweite Befehl ändert das Gateway in $AppGw, um Port 80 für den Front-End-Port mit dem Namen FrontEndPort01 zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="2bcfb-110">The second command modifies the gateway in $AppGw to use port 80 for the front-end port named FrontEndPort01.</span></span>

## <span data-ttu-id="2bcfb-111">Parameter</span><span class="sxs-lookup"><span data-stu-id="2bcfb-111">PARAMETERS</span></span>

### <span data-ttu-id="2bcfb-112">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="2bcfb-112">-ApplicationGateway</span></span>
<span data-ttu-id="2bcfb-113">Gibt das Application Gateway-Objekt an, mit dem dieses Cmdlet den Front-End-Port verknüpft.</span><span class="sxs-lookup"><span data-stu-id="2bcfb-113">Specifies the application gateway object with which this cmdlet associates the front-end port.</span></span>

```yaml
Type: PSApplicationGateway
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="2bcfb-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2bcfb-114">-DefaultProfile</span></span>
<span data-ttu-id="2bcfb-115">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="2bcfb-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="2bcfb-116">-Name</span><span class="sxs-lookup"><span data-stu-id="2bcfb-116">-Name</span></span>
<span data-ttu-id="2bcfb-117">Gibt den Namen des zu ändernden Front-End-Ports an.</span><span class="sxs-lookup"><span data-stu-id="2bcfb-117">Specifies the name of the front-end port to modify.</span></span>

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

### <span data-ttu-id="2bcfb-118">-Port</span><span class="sxs-lookup"><span data-stu-id="2bcfb-118">-Port</span></span>
<span data-ttu-id="2bcfb-119">Gibt die Portnummer an, die für den Front-End-Port verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="2bcfb-119">Specifies the port number to use for the front-end port.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2bcfb-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2bcfb-120">CommonParameters</span></span>
<span data-ttu-id="2bcfb-121">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2bcfb-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2bcfb-122">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2bcfb-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2bcfb-123">Eingaben</span><span class="sxs-lookup"><span data-stu-id="2bcfb-123">INPUTS</span></span>

### <span data-ttu-id="2bcfb-124">PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="2bcfb-124">PSApplicationGateway</span></span>
<span data-ttu-id="2bcfb-125">Der Parameter "ApplicationGateway" akzeptiert den Wert vom Typ "PSApplicationGateway" aus der Pipeline.</span><span class="sxs-lookup"><span data-stu-id="2bcfb-125">Parameter 'ApplicationGateway' accepts value of type 'PSApplicationGateway' from the pipeline</span></span>

## <span data-ttu-id="2bcfb-126">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="2bcfb-126">OUTPUTS</span></span>

### <span data-ttu-id="2bcfb-127">Microsoft. Azure. Commands. Network. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="2bcfb-127">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="2bcfb-128">Notizen</span><span class="sxs-lookup"><span data-stu-id="2bcfb-128">NOTES</span></span>

## <span data-ttu-id="2bcfb-129">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="2bcfb-129">RELATED LINKS</span></span>

[<span data-ttu-id="2bcfb-130">Add-AzureRmApplicationGatewayFrontendPort</span><span class="sxs-lookup"><span data-stu-id="2bcfb-130">Add-AzureRmApplicationGatewayFrontendPort</span></span>](./Add-AzureRmApplicationGatewayFrontendPort.md)

[<span data-ttu-id="2bcfb-131">Get-AzureRmApplicationGatewayFrontendPort</span><span class="sxs-lookup"><span data-stu-id="2bcfb-131">Get-AzureRmApplicationGatewayFrontendPort</span></span>](./Get-AzureRmApplicationGatewayFrontendPort.md)

[<span data-ttu-id="2bcfb-132">Neu – AzureRmApplicationGatewayFrontendPort</span><span class="sxs-lookup"><span data-stu-id="2bcfb-132">New-AzureRmApplicationGatewayFrontendPort</span></span>](./New-AzureRmApplicationGatewayFrontendPort.md)

[<span data-ttu-id="2bcfb-133">Remove-AzureRmApplicationGatewayFrontendPort</span><span class="sxs-lookup"><span data-stu-id="2bcfb-133">Remove-AzureRmApplicationGatewayFrontendPort</span></span>](./Remove-AzureRmApplicationGatewayFrontendPort.md)
