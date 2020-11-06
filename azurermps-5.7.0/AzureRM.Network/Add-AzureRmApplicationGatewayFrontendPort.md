---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 40198C86-A4EB-494A-86D5-DF632518EB95
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/add-azurermapplicationgatewayfrontendport
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Add-AzureRmApplicationGatewayFrontendPort.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Add-AzureRmApplicationGatewayFrontendPort.md
ms.openlocfilehash: c9be5f69fc210f68ceb90cfe2e21f5afab164b6d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93500537"
---
# <span data-ttu-id="7ec26-101">Add-AzureRmApplicationGatewayFrontendPort</span><span class="sxs-lookup"><span data-stu-id="7ec26-101">Add-AzureRmApplicationGatewayFrontendPort</span></span>

## <span data-ttu-id="7ec26-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="7ec26-102">SYNOPSIS</span></span>
<span data-ttu-id="7ec26-103">Fügt einen Front-End-Port zu einem Anwendungsgateway hinzu.</span><span class="sxs-lookup"><span data-stu-id="7ec26-103">Adds a front-end port to an application gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="7ec26-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="7ec26-104">SYNTAX</span></span>

```
Add-AzureRmApplicationGatewayFrontendPort -ApplicationGateway <PSApplicationGateway> -Name <String>
 -Port <Int32> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="7ec26-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="7ec26-105">DESCRIPTION</span></span>
<span data-ttu-id="7ec26-106">Mit dem Cmdlet **Add-AzureRmApplicationGatewayFrontendPort** wird ein Front-End-Port zu einem Anwendungsgateway hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="7ec26-106">The **Add-AzureRmApplicationGatewayFrontendPort** cmdlet adds a front-end port to an application gateway.</span></span>

## <span data-ttu-id="7ec26-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="7ec26-107">EXAMPLES</span></span>

### <span data-ttu-id="7ec26-108">Beispiel 1: Hinzufügen eines Front-End-Ports zu einem Anwendungsgateway</span><span class="sxs-lookup"><span data-stu-id="7ec26-108">Example 1: Add a front-end port to an application gateway</span></span>
```
PS C:\>$AppGw = Get-AzureRmApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $ AppGw = Add-AzureRmApplicationGatewayFrontendPort -ApplicationGateway $AppGw -Name "FrontEndPort01" -Port 80
```

<span data-ttu-id="7ec26-109">Der erste Befehl ruft das Anwendungsgateway mit dem Namen ApplicationGateway01 ab, das zur Ressourcengruppe mit dem Namen ResourceGroup01 gehört, und speichert es in der $AppGw Variablen.</span><span class="sxs-lookup"><span data-stu-id="7ec26-109">The first command gets the application gateway named ApplicationGateway01 that belongs to the resource group named ResourceGroup01 and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="7ec26-110">Der zweite Befehl fügt Port 80 als Front-End-Port für das in $AppGw gespeicherte Anwendungsgateway hinzu und benennt den Port FrontEndPort01.</span><span class="sxs-lookup"><span data-stu-id="7ec26-110">The second command adds port 80 as a front-end port for the application gateway stored in $AppGw and names the port FrontEndPort01.</span></span>

## <span data-ttu-id="7ec26-111">Parameter</span><span class="sxs-lookup"><span data-stu-id="7ec26-111">PARAMETERS</span></span>

### <span data-ttu-id="7ec26-112">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="7ec26-112">-ApplicationGateway</span></span>
<span data-ttu-id="7ec26-113">Gibt das Anwendungsgateway an, dem dieses Cmdlet einen Front-End-Port hinzufügt.</span><span class="sxs-lookup"><span data-stu-id="7ec26-113">Specifies the application gateway to which this cmdlet adds a front-end port.</span></span>

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

### <span data-ttu-id="7ec26-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7ec26-114">-DefaultProfile</span></span>
<span data-ttu-id="7ec26-115">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="7ec26-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="7ec26-116">-Name</span><span class="sxs-lookup"><span data-stu-id="7ec26-116">-Name</span></span>
<span data-ttu-id="7ec26-117">Gibt den Namen des Front-End-Ports an.</span><span class="sxs-lookup"><span data-stu-id="7ec26-117">Specifies the name of the front-end port.</span></span>

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

### <span data-ttu-id="7ec26-118">-Port</span><span class="sxs-lookup"><span data-stu-id="7ec26-118">-Port</span></span>
<span data-ttu-id="7ec26-119">Gibt die Portnummer an.</span><span class="sxs-lookup"><span data-stu-id="7ec26-119">Specifies the port number.</span></span>

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

### <span data-ttu-id="7ec26-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7ec26-120">CommonParameters</span></span>
<span data-ttu-id="7ec26-121">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7ec26-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7ec26-122">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7ec26-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7ec26-123">Eingaben</span><span class="sxs-lookup"><span data-stu-id="7ec26-123">INPUTS</span></span>

### <span data-ttu-id="7ec26-124">System. String</span><span class="sxs-lookup"><span data-stu-id="7ec26-124">System.String</span></span>

## <span data-ttu-id="7ec26-125">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="7ec26-125">OUTPUTS</span></span>

### <span data-ttu-id="7ec26-126">Microsoft. Azure. Commands. Network. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="7ec26-126">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="7ec26-127">Notizen</span><span class="sxs-lookup"><span data-stu-id="7ec26-127">NOTES</span></span>

## <span data-ttu-id="7ec26-128">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="7ec26-128">RELATED LINKS</span></span>

[<span data-ttu-id="7ec26-129">Get-AzureRmApplicationGatewayFrontendPort</span><span class="sxs-lookup"><span data-stu-id="7ec26-129">Get-AzureRmApplicationGatewayFrontendPort</span></span>](./Get-AzureRmApplicationGatewayFrontendPort.md)

[<span data-ttu-id="7ec26-130">Neu – AzureRmApplicationGatewayFrontendPort</span><span class="sxs-lookup"><span data-stu-id="7ec26-130">New-AzureRmApplicationGatewayFrontendPort</span></span>](./New-AzureRmApplicationGatewayFrontendPort.md)

[<span data-ttu-id="7ec26-131">Remove-AzureRmApplicationGatewayFrontendPort</span><span class="sxs-lookup"><span data-stu-id="7ec26-131">Remove-AzureRmApplicationGatewayFrontendPort</span></span>](./Remove-AzureRmApplicationGatewayFrontendPort.md)

[<span data-ttu-id="7ec26-132">Satz-AzureRmApplicationGatewayFrontendPort</span><span class="sxs-lookup"><span data-stu-id="7ec26-132">Set-AzureRmApplicationGatewayFrontendPort</span></span>](./Set-AzureRmApplicationGatewayFrontendPort.md)


