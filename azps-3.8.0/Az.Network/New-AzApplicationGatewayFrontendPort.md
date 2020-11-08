---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 3C046A0A-A2B6-413C-8D3B-8991A1FC4926
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azapplicationgatewayfrontendport
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayFrontendPort.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayFrontendPort.md
ms.openlocfilehash: 3770b17a2bee9509f2b69d0e29c146b0b84ced8e
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/21/2020
ms.locfileid: "94005006"
---
# <span data-ttu-id="f292f-101">New-AzApplicationGatewayFrontendPort</span><span class="sxs-lookup"><span data-stu-id="f292f-101">New-AzApplicationGatewayFrontendPort</span></span>

## <span data-ttu-id="f292f-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="f292f-102">SYNOPSIS</span></span>
<span data-ttu-id="f292f-103">Erstellt einen Front-End-Port für ein Anwendungsgateway.</span><span class="sxs-lookup"><span data-stu-id="f292f-103">Creates a front-end port for an application gateway.</span></span>

## <span data-ttu-id="f292f-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="f292f-104">SYNTAX</span></span>

```
New-AzApplicationGatewayFrontendPort -Name <String> -Port <Int32> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="f292f-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="f292f-105">DESCRIPTION</span></span>
<span data-ttu-id="f292f-106">Das Cmdlet **New-AzApplicationGatewayFrontendPort** erstellt einen Front-End-Port für ein Azure Application Gateway.</span><span class="sxs-lookup"><span data-stu-id="f292f-106">The **New-AzApplicationGatewayFrontendPort** cmdlet creates a front-end port for an Azure application gateway.</span></span>

## <span data-ttu-id="f292f-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="f292f-107">EXAMPLES</span></span>

### <span data-ttu-id="f292f-108">Beispiel1: Erstellen eines Front-End-Ports</span><span class="sxs-lookup"><span data-stu-id="f292f-108">Example1: Create a front-end port</span></span>
```
PS C:\>$FrontEndPort = New-AzApplicationGatewayFrontendPort -Name "FrontEndPort01" -Port 80
```

<span data-ttu-id="f292f-109">Dieser Befehl erstellt einen Front-End-Port mit dem Namen FrontEndPort01 auf Port 80 und speichert das Ergebnis in der Variablen mit dem Namen $FrontEndPort.</span><span class="sxs-lookup"><span data-stu-id="f292f-109">This command creates a front-end port named FrontEndPort01 on port 80 and stores the result in the variable named $FrontEndPort.</span></span>

## <span data-ttu-id="f292f-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="f292f-110">PARAMETERS</span></span>

### <span data-ttu-id="f292f-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f292f-111">-DefaultProfile</span></span>
<span data-ttu-id="f292f-112">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="f292f-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f292f-113">-Name</span><span class="sxs-lookup"><span data-stu-id="f292f-113">-Name</span></span>
<span data-ttu-id="f292f-114">Gibt den Namen des Front-End-Ports an, der vom Cmdlet erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="f292f-114">Specifies the name of the front-end port that this cmdlet creates.</span></span>

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

### <span data-ttu-id="f292f-115">-Port</span><span class="sxs-lookup"><span data-stu-id="f292f-115">-Port</span></span>
<span data-ttu-id="f292f-116">Gibt die Portnummer des Front-End-Ports an.</span><span class="sxs-lookup"><span data-stu-id="f292f-116">Specifies the port number of the front-end port.</span></span>

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

### <span data-ttu-id="f292f-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f292f-117">CommonParameters</span></span>
<span data-ttu-id="f292f-118">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f292f-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f292f-119">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f292f-119">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f292f-120">Eingaben</span><span class="sxs-lookup"><span data-stu-id="f292f-120">INPUTS</span></span>

### <span data-ttu-id="f292f-121">Keine</span><span class="sxs-lookup"><span data-stu-id="f292f-121">None</span></span>

## <span data-ttu-id="f292f-122">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="f292f-122">OUTPUTS</span></span>

### <span data-ttu-id="f292f-123">Microsoft. Azure. Commands. Network. Models. PSApplicationGatewayFrontendPort</span><span class="sxs-lookup"><span data-stu-id="f292f-123">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayFrontendPort</span></span>

## <span data-ttu-id="f292f-124">Notizen</span><span class="sxs-lookup"><span data-stu-id="f292f-124">NOTES</span></span>

## <span data-ttu-id="f292f-125">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="f292f-125">RELATED LINKS</span></span>

[<span data-ttu-id="f292f-126">Add-AzApplicationGatewayFrontendPort</span><span class="sxs-lookup"><span data-stu-id="f292f-126">Add-AzApplicationGatewayFrontendPort</span></span>](./Add-AzApplicationGatewayFrontendPort.md)

[<span data-ttu-id="f292f-127">Get-AzApplicationGatewayFrontendPort</span><span class="sxs-lookup"><span data-stu-id="f292f-127">Get-AzApplicationGatewayFrontendPort</span></span>](./Get-AzApplicationGatewayFrontendPort.md)

[<span data-ttu-id="f292f-128">Remove-AzApplicationGatewayFrontendPort</span><span class="sxs-lookup"><span data-stu-id="f292f-128">Remove-AzApplicationGatewayFrontendPort</span></span>](./Remove-AzApplicationGatewayFrontendPort.md)

[<span data-ttu-id="f292f-129">Satz-AzApplicationGatewayFrontendPort</span><span class="sxs-lookup"><span data-stu-id="f292f-129">Set-AzApplicationGatewayFrontendPort</span></span>](./Set-AzApplicationGatewayFrontendPort.md)


