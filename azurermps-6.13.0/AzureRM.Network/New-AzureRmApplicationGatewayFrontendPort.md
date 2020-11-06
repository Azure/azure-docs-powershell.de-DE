---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 3C046A0A-A2B6-413C-8D3B-8991A1FC4926
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/new-azurermapplicationgatewayfrontendport
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmApplicationGatewayFrontendPort.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmApplicationGatewayFrontendPort.md
ms.openlocfilehash: 656067c89adbcead5dd24e08d45147eb7f019e80
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93500217"
---
# <span data-ttu-id="de1db-101">New-AzureRmApplicationGatewayFrontendPort</span><span class="sxs-lookup"><span data-stu-id="de1db-101">New-AzureRmApplicationGatewayFrontendPort</span></span>

## <span data-ttu-id="de1db-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="de1db-102">SYNOPSIS</span></span>
<span data-ttu-id="de1db-103">Erstellt einen Front-End-Port für ein Anwendungsgateway.</span><span class="sxs-lookup"><span data-stu-id="de1db-103">Creates a front-end port for an application gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="de1db-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="de1db-104">SYNTAX</span></span>

```
New-AzureRmApplicationGatewayFrontendPort -Name <String> -Port <Int32>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="de1db-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="de1db-105">DESCRIPTION</span></span>
<span data-ttu-id="de1db-106">Das Cmdlet **New-AzureRmApplicationGatewayFrontendPort** erstellt einen Front-End-Port für ein Azure Application Gateway.</span><span class="sxs-lookup"><span data-stu-id="de1db-106">The **New-AzureRmApplicationGatewayFrontendPort** cmdlet creates a front-end port for an Azure application gateway.</span></span>

## <span data-ttu-id="de1db-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="de1db-107">EXAMPLES</span></span>

### <span data-ttu-id="de1db-108">Beispiel1: Erstellen eines Front-End-Ports</span><span class="sxs-lookup"><span data-stu-id="de1db-108">Example1: Create a front-end port</span></span>
```
PS C:\>$FrontEndPort = New-AzureRmApplicationGatewayFrontendPort -Name "FrontEndPort01" -Port 80
```

<span data-ttu-id="de1db-109">Dieser Befehl erstellt einen Front-End-Port mit dem Namen FrontEndPort01 auf Port 80 und speichert das Ergebnis in der Variablen mit dem Namen $FrontEndPort.</span><span class="sxs-lookup"><span data-stu-id="de1db-109">This command creates a front-end port named FrontEndPort01 on port 80 and stores the result in the variable named $FrontEndPort.</span></span>

## <span data-ttu-id="de1db-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="de1db-110">PARAMETERS</span></span>

### <span data-ttu-id="de1db-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="de1db-111">-DefaultProfile</span></span>
<span data-ttu-id="de1db-112">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="de1db-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="de1db-113">-Name</span><span class="sxs-lookup"><span data-stu-id="de1db-113">-Name</span></span>
<span data-ttu-id="de1db-114">Gibt den Namen des Front-End-Ports an, der vom Cmdlet erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="de1db-114">Specifies the name of the front-end port that this cmdlet creates.</span></span>

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

### <span data-ttu-id="de1db-115">-Port</span><span class="sxs-lookup"><span data-stu-id="de1db-115">-Port</span></span>
<span data-ttu-id="de1db-116">Gibt die Portnummer des Front-End-Ports an.</span><span class="sxs-lookup"><span data-stu-id="de1db-116">Specifies the port number of the front-end port.</span></span>

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

### <span data-ttu-id="de1db-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="de1db-117">CommonParameters</span></span>
<span data-ttu-id="de1db-118">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="de1db-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="de1db-119">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="de1db-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="de1db-120">Eingaben</span><span class="sxs-lookup"><span data-stu-id="de1db-120">INPUTS</span></span>

### <span data-ttu-id="de1db-121">Keine</span><span class="sxs-lookup"><span data-stu-id="de1db-121">None</span></span>

## <span data-ttu-id="de1db-122">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="de1db-122">OUTPUTS</span></span>

### <span data-ttu-id="de1db-123">Microsoft. Azure. Commands. Network. Models. PSApplicationGatewayFrontendPort</span><span class="sxs-lookup"><span data-stu-id="de1db-123">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayFrontendPort</span></span>

## <span data-ttu-id="de1db-124">Notizen</span><span class="sxs-lookup"><span data-stu-id="de1db-124">NOTES</span></span>

## <span data-ttu-id="de1db-125">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="de1db-125">RELATED LINKS</span></span>

[<span data-ttu-id="de1db-126">Add-AzureRmApplicationGatewayFrontendPort</span><span class="sxs-lookup"><span data-stu-id="de1db-126">Add-AzureRmApplicationGatewayFrontendPort</span></span>](./Add-AzureRmApplicationGatewayFrontendPort.md)

[<span data-ttu-id="de1db-127">Get-AzureRmApplicationGatewayFrontendPort</span><span class="sxs-lookup"><span data-stu-id="de1db-127">Get-AzureRmApplicationGatewayFrontendPort</span></span>](./Get-AzureRmApplicationGatewayFrontendPort.md)

[<span data-ttu-id="de1db-128">Remove-AzureRmApplicationGatewayFrontendPort</span><span class="sxs-lookup"><span data-stu-id="de1db-128">Remove-AzureRmApplicationGatewayFrontendPort</span></span>](./Remove-AzureRmApplicationGatewayFrontendPort.md)

[<span data-ttu-id="de1db-129">Satz-AzureRmApplicationGatewayFrontendPort</span><span class="sxs-lookup"><span data-stu-id="de1db-129">Set-AzureRmApplicationGatewayFrontendPort</span></span>](./Set-AzureRmApplicationGatewayFrontendPort.md)


