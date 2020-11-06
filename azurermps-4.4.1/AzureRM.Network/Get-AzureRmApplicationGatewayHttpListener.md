---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 8D41EDAC-17D9-494B-8336-67906F4E1E81
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmApplicationGatewayHttpListener.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmApplicationGatewayHttpListener.md
ms.openlocfilehash: 564c586218297b8a22f0763a6747b6b451018a5e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93479106"
---
# <span data-ttu-id="0d87a-101">Get-AzureRmApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="0d87a-101">Get-AzureRmApplicationGatewayHttpListener</span></span>

## <span data-ttu-id="0d87a-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="0d87a-102">SYNOPSIS</span></span>
<span data-ttu-id="0d87a-103">Ruft den HTTP-Listener eines Anwendungs Gateways ab.</span><span class="sxs-lookup"><span data-stu-id="0d87a-103">Gets the HTTP listener of an application gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="0d87a-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="0d87a-104">SYNTAX</span></span>

```
Get-AzureRmApplicationGatewayHttpListener [-Name <String>] -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="0d87a-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="0d87a-105">DESCRIPTION</span></span>
<span data-ttu-id="0d87a-106">Das Cmdlet " **Get-AzureRmApplicationGatewayHttpListener** " Ruft den HTTP-Listener eines Anwendungs Gateways ab.</span><span class="sxs-lookup"><span data-stu-id="0d87a-106">The **Get-AzureRmApplicationGatewayHttpListener** cmdlet gets the HTTP listener of an application gateway.</span></span>

## <span data-ttu-id="0d87a-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="0d87a-107">EXAMPLES</span></span>

### <span data-ttu-id="0d87a-108">Beispiel 1: Abrufen eines bestimmten HTTP-Listeners</span><span class="sxs-lookup"><span data-stu-id="0d87a-108">Example 1: Get a specific HTTP listener</span></span>
```
PS C:\>$Appgw = Get-AzureRmApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $Listener = Get-AzureRmApplicationGatewayHttpListener -Name "Listener01" -ApplicationGateway $Appgw
```

<span data-ttu-id="0d87a-109">Dieser Befehl ruft einen HTTP-Listener mit dem Namen Listener01 ab.</span><span class="sxs-lookup"><span data-stu-id="0d87a-109">This command gets an HTTP listener named Listener01.</span></span>

### <span data-ttu-id="0d87a-110">Beispiel 2: Abrufen einer Liste mit http-Listenern</span><span class="sxs-lookup"><span data-stu-id="0d87a-110">Example 2: Get a list of HTTP listeners</span></span>
```
PS C:\>$Appgw = Get-AzureRmApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $Listeners = Get-AzureRmApplicationGatewayHttpListener -ApplicationGateway $Appgw
```

<span data-ttu-id="0d87a-111">Dieser Befehl ruft eine Liste der HTTP-Listener ab.</span><span class="sxs-lookup"><span data-stu-id="0d87a-111">This command gets a list of HTTP listeners.</span></span>

## <span data-ttu-id="0d87a-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="0d87a-112">PARAMETERS</span></span>

### <span data-ttu-id="0d87a-113">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="0d87a-113">-ApplicationGateway</span></span>
<span data-ttu-id="0d87a-114">Gibt das Application Gateway-Objekt an, das den HTTP-Listener enthält.</span><span class="sxs-lookup"><span data-stu-id="0d87a-114">Specifies the application gateway object that contains the HTTP listener.</span></span>

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

### <span data-ttu-id="0d87a-115">-Name</span><span class="sxs-lookup"><span data-stu-id="0d87a-115">-Name</span></span>
<span data-ttu-id="0d87a-116">Gibt den Namen des HTTP-Listener an, den dieses Cmdlet erhält.</span><span class="sxs-lookup"><span data-stu-id="0d87a-116">Specifies the name of the HTTP listener which this cmdlet gets.</span></span>

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

### <span data-ttu-id="0d87a-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0d87a-117">-DefaultProfile</span></span>
<span data-ttu-id="0d87a-118">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="0d87a-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="0d87a-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0d87a-119">CommonParameters</span></span>
<span data-ttu-id="0d87a-120">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0d87a-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0d87a-121">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0d87a-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0d87a-122">Eingaben</span><span class="sxs-lookup"><span data-stu-id="0d87a-122">INPUTS</span></span>

### <span data-ttu-id="0d87a-123">System. String</span><span class="sxs-lookup"><span data-stu-id="0d87a-123">System.String</span></span>

## <span data-ttu-id="0d87a-124">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="0d87a-124">OUTPUTS</span></span>

### <span data-ttu-id="0d87a-125">Microsoft. Azure. Commands. Network. Models. PSApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="0d87a-125">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayHttpListener</span></span>

## <span data-ttu-id="0d87a-126">Notizen</span><span class="sxs-lookup"><span data-stu-id="0d87a-126">NOTES</span></span>

## <span data-ttu-id="0d87a-127">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="0d87a-127">RELATED LINKS</span></span>

[<span data-ttu-id="0d87a-128">Add-AzureRmApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="0d87a-128">Add-AzureRmApplicationGatewayHttpListener</span></span>](./Add-AzureRmApplicationGatewayHttpListener.md)

[<span data-ttu-id="0d87a-129">Neu – AzureRmApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="0d87a-129">New-AzureRmApplicationGatewayHttpListener</span></span>](./New-AzureRmApplicationGatewayHttpListener.md)

[<span data-ttu-id="0d87a-130">Remove-AzureRmApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="0d87a-130">Remove-AzureRmApplicationGatewayHttpListener</span></span>](./Remove-AzureRmApplicationGatewayHttpListener.md)

[<span data-ttu-id="0d87a-131">Satz-AzureRmApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="0d87a-131">Set-AzureRmApplicationGatewayHttpListener</span></span>](./Set-AzureRmApplicationGatewayHttpListener.md)


