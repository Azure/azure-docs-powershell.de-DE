---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 3C046A0A-A2B6-413C-8D3B-8991A1FC4926
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azapplicationgatewayfrontendport
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayFrontendPort.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayFrontendPort.md
ms.openlocfilehash: 26b6bc0128929efda2baf52979e1b6c2ecdbd714
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93660614"
---
# <span data-ttu-id="c2cdc-101">New-AzApplicationGatewayFrontendPort</span><span class="sxs-lookup"><span data-stu-id="c2cdc-101">New-AzApplicationGatewayFrontendPort</span></span>

## <span data-ttu-id="c2cdc-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="c2cdc-102">SYNOPSIS</span></span>
<span data-ttu-id="c2cdc-103">Erstellt einen Front-End-Port für ein Anwendungsgateway.</span><span class="sxs-lookup"><span data-stu-id="c2cdc-103">Creates a front-end port for an application gateway.</span></span>

## <span data-ttu-id="c2cdc-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="c2cdc-104">SYNTAX</span></span>

```
New-AzApplicationGatewayFrontendPort -Name <String> -Port <Int32> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="c2cdc-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="c2cdc-105">DESCRIPTION</span></span>
<span data-ttu-id="c2cdc-106">Das Cmdlet **New-AzApplicationGatewayFrontendPort** erstellt einen Front-End-Port für ein Azure Application Gateway.</span><span class="sxs-lookup"><span data-stu-id="c2cdc-106">The **New-AzApplicationGatewayFrontendPort** cmdlet creates a front-end port for an Azure application gateway.</span></span>

## <span data-ttu-id="c2cdc-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="c2cdc-107">EXAMPLES</span></span>

### <span data-ttu-id="c2cdc-108">Beispiel1: Erstellen eines Front-End-Ports</span><span class="sxs-lookup"><span data-stu-id="c2cdc-108">Example1: Create a front-end port</span></span>
```
PS C:\>$FrontEndPort = New-AzApplicationGatewayFrontendPort -Name "FrontEndPort01" -Port 80
```

<span data-ttu-id="c2cdc-109">Dieser Befehl erstellt einen Front-End-Port mit dem Namen FrontEndPort01 auf Port 80 und speichert das Ergebnis in der Variablen mit dem Namen $FrontEndPort.</span><span class="sxs-lookup"><span data-stu-id="c2cdc-109">This command creates a front-end port named FrontEndPort01 on port 80 and stores the result in the variable named $FrontEndPort.</span></span>

## <span data-ttu-id="c2cdc-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="c2cdc-110">PARAMETERS</span></span>

### <span data-ttu-id="c2cdc-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c2cdc-111">-DefaultProfile</span></span>
<span data-ttu-id="c2cdc-112">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="c2cdc-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c2cdc-113">-Name</span><span class="sxs-lookup"><span data-stu-id="c2cdc-113">-Name</span></span>
<span data-ttu-id="c2cdc-114">Gibt den Namen des Front-End-Ports an, der vom Cmdlet erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="c2cdc-114">Specifies the name of the front-end port that this cmdlet creates.</span></span>

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

### <span data-ttu-id="c2cdc-115">-Port</span><span class="sxs-lookup"><span data-stu-id="c2cdc-115">-Port</span></span>
<span data-ttu-id="c2cdc-116">Gibt die Portnummer des Front-End-Ports an.</span><span class="sxs-lookup"><span data-stu-id="c2cdc-116">Specifies the port number of the front-end port.</span></span>

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

### <span data-ttu-id="c2cdc-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c2cdc-117">CommonParameters</span></span>
<span data-ttu-id="c2cdc-118">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c2cdc-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c2cdc-119">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c2cdc-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c2cdc-120">Eingaben</span><span class="sxs-lookup"><span data-stu-id="c2cdc-120">INPUTS</span></span>

### <span data-ttu-id="c2cdc-121">Keine</span><span class="sxs-lookup"><span data-stu-id="c2cdc-121">None</span></span>

## <span data-ttu-id="c2cdc-122">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="c2cdc-122">OUTPUTS</span></span>

### <span data-ttu-id="c2cdc-123">Microsoft. Azure. Commands. Network. Models. PSApplicationGatewayFrontendPort</span><span class="sxs-lookup"><span data-stu-id="c2cdc-123">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayFrontendPort</span></span>

## <span data-ttu-id="c2cdc-124">Notizen</span><span class="sxs-lookup"><span data-stu-id="c2cdc-124">NOTES</span></span>

## <span data-ttu-id="c2cdc-125">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="c2cdc-125">RELATED LINKS</span></span>

[<span data-ttu-id="c2cdc-126">Add-AzApplicationGatewayFrontendPort</span><span class="sxs-lookup"><span data-stu-id="c2cdc-126">Add-AzApplicationGatewayFrontendPort</span></span>](./Add-AzApplicationGatewayFrontendPort.md)

[<span data-ttu-id="c2cdc-127">Get-AzApplicationGatewayFrontendPort</span><span class="sxs-lookup"><span data-stu-id="c2cdc-127">Get-AzApplicationGatewayFrontendPort</span></span>](./Get-AzApplicationGatewayFrontendPort.md)

[<span data-ttu-id="c2cdc-128">Remove-AzApplicationGatewayFrontendPort</span><span class="sxs-lookup"><span data-stu-id="c2cdc-128">Remove-AzApplicationGatewayFrontendPort</span></span>](./Remove-AzApplicationGatewayFrontendPort.md)

[<span data-ttu-id="c2cdc-129">Satz-AzApplicationGatewayFrontendPort</span><span class="sxs-lookup"><span data-stu-id="c2cdc-129">Set-AzApplicationGatewayFrontendPort</span></span>](./Set-AzApplicationGatewayFrontendPort.md)


