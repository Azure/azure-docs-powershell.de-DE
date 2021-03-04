---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 3C046A0A-A2B6-413C-8D3B-8991A1FC4926
online version: https://docs.microsoft.com/powershell/module/az.network/new-azapplicationgatewayfrontendport
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayFrontendPort.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayFrontendPort.md
ms.openlocfilehash: bcc7335076a0f74c89cede8c6fed66f55d88ec9d
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101919587"
---
# <span data-ttu-id="a4cf4-101">New-AzApplicationGatewayFrontendPort</span><span class="sxs-lookup"><span data-stu-id="a4cf4-101">New-AzApplicationGatewayFrontendPort</span></span>

## <span data-ttu-id="a4cf4-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a4cf4-102">SYNOPSIS</span></span>
<span data-ttu-id="a4cf4-103">Erstellt einen Front-End-Port für ein Anwendungsgateway.</span><span class="sxs-lookup"><span data-stu-id="a4cf4-103">Creates a front-end port for an application gateway.</span></span>

## <span data-ttu-id="a4cf4-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="a4cf4-104">SYNTAX</span></span>

```
New-AzApplicationGatewayFrontendPort -Name <String> -Port <Int32> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="a4cf4-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="a4cf4-105">DESCRIPTION</span></span>
<span data-ttu-id="a4cf4-106">Das **Cmdlet New-AzApplicationGatewayFrontendPort** erstellt einen Front-End-Port für ein Azure-Anwendungsgateway.</span><span class="sxs-lookup"><span data-stu-id="a4cf4-106">The **New-AzApplicationGatewayFrontendPort** cmdlet creates a front-end port for an Azure application gateway.</span></span>

## <span data-ttu-id="a4cf4-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="a4cf4-107">EXAMPLES</span></span>

### <span data-ttu-id="a4cf4-108">Beispiel 1: Beispiel1: Erstellen eines Front-End-Ports</span><span class="sxs-lookup"><span data-stu-id="a4cf4-108">Example 1: Example1: Create a front-end port</span></span>
```powershell
PS C:\>$FrontEndPort = New-AzApplicationGatewayFrontendPort -Name "FrontEndPort01" -Port 80
```

<span data-ttu-id="a4cf4-109">Mit diesem Befehl wird ein Front-End-Port namens FrontEndPort01 für Port 80 erstellt und das Ergebnis in der Variablen namens $FrontEndPort.</span><span class="sxs-lookup"><span data-stu-id="a4cf4-109">This command creates a front-end port named FrontEndPort01 on port 80 and stores the result in the variable named $FrontEndPort.</span></span>

## <span data-ttu-id="a4cf4-110">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="a4cf4-110">PARAMETERS</span></span>

### <span data-ttu-id="a4cf4-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a4cf4-111">-DefaultProfile</span></span>
<span data-ttu-id="a4cf4-112">Die Anmeldeinformationen, das Konto, der Mandant und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="a4cf4-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a4cf4-113">-Name</span><span class="sxs-lookup"><span data-stu-id="a4cf4-113">-Name</span></span>
<span data-ttu-id="a4cf4-114">Gibt den Namen des Front-End-Ports an, den dieses Cmdlet erstellt.</span><span class="sxs-lookup"><span data-stu-id="a4cf4-114">Specifies the name of the front-end port that this cmdlet creates.</span></span>

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

### <span data-ttu-id="a4cf4-115">-Port</span><span class="sxs-lookup"><span data-stu-id="a4cf4-115">-Port</span></span>
<span data-ttu-id="a4cf4-116">Gibt die Portnummer des Front-End-Ports an.</span><span class="sxs-lookup"><span data-stu-id="a4cf4-116">Specifies the port number of the front-end port.</span></span>

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

### <span data-ttu-id="a4cf4-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a4cf4-117">CommonParameters</span></span>
<span data-ttu-id="a4cf4-118">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a4cf4-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a4cf4-119">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a4cf4-119">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a4cf4-120">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="a4cf4-120">INPUTS</span></span>

### <span data-ttu-id="a4cf4-121">Keine</span><span class="sxs-lookup"><span data-stu-id="a4cf4-121">None</span></span>

## <span data-ttu-id="a4cf4-122">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="a4cf4-122">OUTPUTS</span></span>

### <span data-ttu-id="a4cf4-123">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayFrontendPort</span><span class="sxs-lookup"><span data-stu-id="a4cf4-123">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayFrontendPort</span></span>

## <span data-ttu-id="a4cf4-124">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="a4cf4-124">NOTES</span></span>

## <span data-ttu-id="a4cf4-125">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="a4cf4-125">RELATED LINKS</span></span>

[<span data-ttu-id="a4cf4-126">Add-AzApplicationGatewayFrontendPort</span><span class="sxs-lookup"><span data-stu-id="a4cf4-126">Add-AzApplicationGatewayFrontendPort</span></span>](./Add-AzApplicationGatewayFrontendPort.md)

[<span data-ttu-id="a4cf4-127">Get-AzApplicationGatewayFrontendPort</span><span class="sxs-lookup"><span data-stu-id="a4cf4-127">Get-AzApplicationGatewayFrontendPort</span></span>](./Get-AzApplicationGatewayFrontendPort.md)

[<span data-ttu-id="a4cf4-128">Remove-AzApplicationGatewayFrontendPort</span><span class="sxs-lookup"><span data-stu-id="a4cf4-128">Remove-AzApplicationGatewayFrontendPort</span></span>](./Remove-AzApplicationGatewayFrontendPort.md)

[<span data-ttu-id="a4cf4-129">Set-AzApplicationGatewayFrontendPort</span><span class="sxs-lookup"><span data-stu-id="a4cf4-129">Set-AzApplicationGatewayFrontendPort</span></span>](./Set-AzApplicationGatewayFrontendPort.md)


