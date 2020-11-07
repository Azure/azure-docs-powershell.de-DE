---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 40198C86-A4EB-494A-86D5-DF632518EB95
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/add-azapplicationgatewayfrontendport
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzApplicationGatewayFrontendPort.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzApplicationGatewayFrontendPort.md
ms.openlocfilehash: 9eaaa8ae6ec4be7a1096bfd9de4a3e20c0cb5ff1
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93660950"
---
# <span data-ttu-id="d2c64-101">Add-AzApplicationGatewayFrontendPort</span><span class="sxs-lookup"><span data-stu-id="d2c64-101">Add-AzApplicationGatewayFrontendPort</span></span>

## <span data-ttu-id="d2c64-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="d2c64-102">SYNOPSIS</span></span>
<span data-ttu-id="d2c64-103">Fügt einen Front-End-Port zu einem Anwendungsgateway hinzu.</span><span class="sxs-lookup"><span data-stu-id="d2c64-103">Adds a front-end port to an application gateway.</span></span>

## <span data-ttu-id="d2c64-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="d2c64-104">SYNTAX</span></span>

```
Add-AzApplicationGatewayFrontendPort -ApplicationGateway <PSApplicationGateway> -Name <String> -Port <Int32>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d2c64-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="d2c64-105">DESCRIPTION</span></span>
<span data-ttu-id="d2c64-106">Mit dem Cmdlet **Add-AzApplicationGatewayFrontendPort** wird ein Front-End-Port zu einem Anwendungsgateway hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="d2c64-106">The **Add-AzApplicationGatewayFrontendPort** cmdlet adds a front-end port to an application gateway.</span></span>

## <span data-ttu-id="d2c64-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="d2c64-107">EXAMPLES</span></span>

### <span data-ttu-id="d2c64-108">Beispiel 1: Hinzufügen eines Front-End-Ports zu einem Anwendungsgateway</span><span class="sxs-lookup"><span data-stu-id="d2c64-108">Example 1: Add a front-end port to an application gateway</span></span>
```
PS C:\>$AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $AppGw = Add-AzApplicationGatewayFrontendPort -ApplicationGateway $AppGw -Name "FrontEndPort01" -Port 80
```

<span data-ttu-id="d2c64-109">Der erste Befehl ruft das Anwendungsgateway mit dem Namen ApplicationGateway01 ab, das zur Ressourcengruppe mit dem Namen ResourceGroup01 gehört, und speichert es in der $AppGw Variablen.</span><span class="sxs-lookup"><span data-stu-id="d2c64-109">The first command gets the application gateway named ApplicationGateway01 that belongs to the resource group named ResourceGroup01 and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="d2c64-110">Der zweite Befehl fügt Port 80 als Front-End-Port für das in $AppGw gespeicherte Anwendungsgateway hinzu und benennt den Port FrontEndPort01.</span><span class="sxs-lookup"><span data-stu-id="d2c64-110">The second command adds port 80 as a front-end port for the application gateway stored in $AppGw and names the port FrontEndPort01.</span></span>

## <span data-ttu-id="d2c64-111">Parameter</span><span class="sxs-lookup"><span data-stu-id="d2c64-111">PARAMETERS</span></span>

### <span data-ttu-id="d2c64-112">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="d2c64-112">-ApplicationGateway</span></span>
<span data-ttu-id="d2c64-113">Gibt das Anwendungsgateway an, dem dieses Cmdlet einen Front-End-Port hinzufügt.</span><span class="sxs-lookup"><span data-stu-id="d2c64-113">Specifies the application gateway to which this cmdlet adds a front-end port.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGateway
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d2c64-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d2c64-114">-DefaultProfile</span></span>
<span data-ttu-id="d2c64-115">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="d2c64-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d2c64-116">-Name</span><span class="sxs-lookup"><span data-stu-id="d2c64-116">-Name</span></span>
<span data-ttu-id="d2c64-117">Gibt den Namen des Front-End-Ports an.</span><span class="sxs-lookup"><span data-stu-id="d2c64-117">Specifies the name of the front-end port.</span></span>

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

### <span data-ttu-id="d2c64-118">-Port</span><span class="sxs-lookup"><span data-stu-id="d2c64-118">-Port</span></span>
<span data-ttu-id="d2c64-119">Gibt die Portnummer an.</span><span class="sxs-lookup"><span data-stu-id="d2c64-119">Specifies the port number.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d2c64-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d2c64-120">CommonParameters</span></span>
<span data-ttu-id="d2c64-121">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d2c64-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d2c64-122">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d2c64-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d2c64-123">Eingaben</span><span class="sxs-lookup"><span data-stu-id="d2c64-123">INPUTS</span></span>

### <span data-ttu-id="d2c64-124">Microsoft. Azure. Commands. Network. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="d2c64-124">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="d2c64-125">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="d2c64-125">OUTPUTS</span></span>

### <span data-ttu-id="d2c64-126">Microsoft. Azure. Commands. Network. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="d2c64-126">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="d2c64-127">Notizen</span><span class="sxs-lookup"><span data-stu-id="d2c64-127">NOTES</span></span>

## <span data-ttu-id="d2c64-128">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="d2c64-128">RELATED LINKS</span></span>

[<span data-ttu-id="d2c64-129">Get-AzApplicationGatewayFrontendPort</span><span class="sxs-lookup"><span data-stu-id="d2c64-129">Get-AzApplicationGatewayFrontendPort</span></span>](./Get-AzApplicationGatewayFrontendPort.md)

[<span data-ttu-id="d2c64-130">Neu – AzApplicationGatewayFrontendPort</span><span class="sxs-lookup"><span data-stu-id="d2c64-130">New-AzApplicationGatewayFrontendPort</span></span>](./New-AzApplicationGatewayFrontendPort.md)

[<span data-ttu-id="d2c64-131">Remove-AzApplicationGatewayFrontendPort</span><span class="sxs-lookup"><span data-stu-id="d2c64-131">Remove-AzApplicationGatewayFrontendPort</span></span>](./Remove-AzApplicationGatewayFrontendPort.md)

[<span data-ttu-id="d2c64-132">Satz-AzApplicationGatewayFrontendPort</span><span class="sxs-lookup"><span data-stu-id="d2c64-132">Set-AzApplicationGatewayFrontendPort</span></span>](./Set-AzApplicationGatewayFrontendPort.md)


