---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 8D41EDAC-17D9-494B-8336-67906F4E1E81
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azapplicationgatewayhttplistener
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Get-AzApplicationGatewayHttpListener.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Get-AzApplicationGatewayHttpListener.md
ms.openlocfilehash: 67652681b5a0cf5468fa42fb9090446f2a11158e
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/16/2020
ms.locfileid: "93841727"
---
# <span data-ttu-id="5ebcb-101">Get-AzApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="5ebcb-101">Get-AzApplicationGatewayHttpListener</span></span>

## <span data-ttu-id="5ebcb-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="5ebcb-102">SYNOPSIS</span></span>
<span data-ttu-id="5ebcb-103">Ruft den HTTP-Listener eines Anwendungs Gateways ab.</span><span class="sxs-lookup"><span data-stu-id="5ebcb-103">Gets the HTTP listener of an application gateway.</span></span>

## <span data-ttu-id="5ebcb-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="5ebcb-104">SYNTAX</span></span>

```
Get-AzApplicationGatewayHttpListener [-Name <String>] -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="5ebcb-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="5ebcb-105">DESCRIPTION</span></span>
<span data-ttu-id="5ebcb-106">Das Cmdlet " **Get-AzApplicationGatewayHttpListener** " Ruft den HTTP-Listener eines Anwendungs Gateways ab.</span><span class="sxs-lookup"><span data-stu-id="5ebcb-106">The **Get-AzApplicationGatewayHttpListener** cmdlet gets the HTTP listener of an application gateway.</span></span>

## <span data-ttu-id="5ebcb-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="5ebcb-107">EXAMPLES</span></span>

### <span data-ttu-id="5ebcb-108">Beispiel 1: Abrufen eines bestimmten HTTP-Listeners</span><span class="sxs-lookup"><span data-stu-id="5ebcb-108">Example 1: Get a specific HTTP listener</span></span>
```
PS C:\>$Appgw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $Listener = Get-AzApplicationGatewayHttpListener -Name "Listener01" -ApplicationGateway $Appgw
```

<span data-ttu-id="5ebcb-109">Dieser Befehl ruft einen HTTP-Listener mit dem Namen Listener01 ab.</span><span class="sxs-lookup"><span data-stu-id="5ebcb-109">This command gets an HTTP listener named Listener01.</span></span>

### <span data-ttu-id="5ebcb-110">Beispiel 2: Abrufen einer Liste mit http-Listenern</span><span class="sxs-lookup"><span data-stu-id="5ebcb-110">Example 2: Get a list of HTTP listeners</span></span>
```
PS C:\>$Appgw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $Listeners = Get-AzApplicationGatewayHttpListener -ApplicationGateway $Appgw
```

<span data-ttu-id="5ebcb-111">Dieser Befehl ruft eine Liste der HTTP-Listener ab.</span><span class="sxs-lookup"><span data-stu-id="5ebcb-111">This command gets a list of HTTP listeners.</span></span>

## <span data-ttu-id="5ebcb-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="5ebcb-112">PARAMETERS</span></span>

### <span data-ttu-id="5ebcb-113">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="5ebcb-113">-ApplicationGateway</span></span>
<span data-ttu-id="5ebcb-114">Gibt das Application Gateway-Objekt an, das den HTTP-Listener enthält.</span><span class="sxs-lookup"><span data-stu-id="5ebcb-114">Specifies the application gateway object that contains the HTTP listener.</span></span>

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

### <span data-ttu-id="5ebcb-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5ebcb-115">-DefaultProfile</span></span>
<span data-ttu-id="5ebcb-116">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="5ebcb-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="5ebcb-117">-Name</span><span class="sxs-lookup"><span data-stu-id="5ebcb-117">-Name</span></span>
<span data-ttu-id="5ebcb-118">Gibt den Namen des HTTP-Listener an, den dieses Cmdlet erhält.</span><span class="sxs-lookup"><span data-stu-id="5ebcb-118">Specifies the name of the HTTP listener which this cmdlet gets.</span></span>

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

### <span data-ttu-id="5ebcb-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5ebcb-119">CommonParameters</span></span>
<span data-ttu-id="5ebcb-120">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5ebcb-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5ebcb-121">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5ebcb-121">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5ebcb-122">Eingaben</span><span class="sxs-lookup"><span data-stu-id="5ebcb-122">INPUTS</span></span>

### <span data-ttu-id="5ebcb-123">System. String</span><span class="sxs-lookup"><span data-stu-id="5ebcb-123">System.String</span></span>

## <span data-ttu-id="5ebcb-124">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="5ebcb-124">OUTPUTS</span></span>

### <span data-ttu-id="5ebcb-125">Microsoft. Azure. Commands. Network. Models. PSApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="5ebcb-125">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayHttpListener</span></span>

## <span data-ttu-id="5ebcb-126">Notizen</span><span class="sxs-lookup"><span data-stu-id="5ebcb-126">NOTES</span></span>

## <span data-ttu-id="5ebcb-127">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="5ebcb-127">RELATED LINKS</span></span>

[<span data-ttu-id="5ebcb-128">Add-AzApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="5ebcb-128">Add-AzApplicationGatewayHttpListener</span></span>](./Add-AzApplicationGatewayHttpListener.md)

[<span data-ttu-id="5ebcb-129">Neu – AzApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="5ebcb-129">New-AzApplicationGatewayHttpListener</span></span>](./New-AzApplicationGatewayHttpListener.md)

[<span data-ttu-id="5ebcb-130">Remove-AzApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="5ebcb-130">Remove-AzApplicationGatewayHttpListener</span></span>](./Remove-AzApplicationGatewayHttpListener.md)

[<span data-ttu-id="5ebcb-131">Satz-AzApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="5ebcb-131">Set-AzApplicationGatewayHttpListener</span></span>](./Set-AzApplicationGatewayHttpListener.md)


