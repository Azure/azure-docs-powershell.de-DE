---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 2C9609E8-0D8B-471B-9F0E-672BF55C3A0E
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/stop-azapplicationgateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Stop-AzApplicationGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Stop-AzApplicationGateway.md
ms.openlocfilehash: 921c770cce5d1f597fa0af96dd30014f9dacb2fc
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93823740"
---
# <span data-ttu-id="fda42-101">Stop-AzApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="fda42-101">Stop-AzApplicationGateway</span></span>

## <span data-ttu-id="fda42-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="fda42-102">SYNOPSIS</span></span>
<span data-ttu-id="fda42-103">Beenden eines Anwendungs Gateways</span><span class="sxs-lookup"><span data-stu-id="fda42-103">Stops an application gateway</span></span>

## <span data-ttu-id="fda42-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="fda42-104">SYNTAX</span></span>

```
Stop-AzApplicationGateway -ApplicationGateway <PSApplicationGateway> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="fda42-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="fda42-105">DESCRIPTION</span></span>
<span data-ttu-id="fda42-106">Das Cmdlet **Stop-AzApplicationGateway** beendet ein Anwendungsgateway.</span><span class="sxs-lookup"><span data-stu-id="fda42-106">The **Stop-AzApplicationGateway** cmdlet stops an application gateway.</span></span>

## <span data-ttu-id="fda42-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="fda42-107">EXAMPLES</span></span>

### <span data-ttu-id="fda42-108">Beispiel 1: Beenden eines Anwendungs Gateways</span><span class="sxs-lookup"><span data-stu-id="fda42-108">Example 1: Stop an application gateway</span></span>
```
PS C:\>Stop-AzApplicationGateway -ApplicationGateway $AppGw
```

<span data-ttu-id="fda42-109">Mit diesem Befehl wird das in der $AppGw-Variable gespeicherte Anwendungsgateway angehalten.</span><span class="sxs-lookup"><span data-stu-id="fda42-109">This command stops the application gateway stored in the $AppGw variable.</span></span>

## <span data-ttu-id="fda42-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="fda42-110">PARAMETERS</span></span>

### <span data-ttu-id="fda42-111">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="fda42-111">-ApplicationGateway</span></span>
<span data-ttu-id="fda42-112">Gibt das Anwendungsgateway an, das mit diesem Cmdlet beendet wird.</span><span class="sxs-lookup"><span data-stu-id="fda42-112">Specifies the application gateway that this cmdlet stops.</span></span>

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

### <span data-ttu-id="fda42-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="fda42-113">-AsJob</span></span>
<span data-ttu-id="fda42-114">Ausführen eines Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="fda42-114">Run cmdlet in the background</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fda42-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fda42-115">-DefaultProfile</span></span>
<span data-ttu-id="fda42-116">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="fda42-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="fda42-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fda42-117">CommonParameters</span></span>
<span data-ttu-id="fda42-118">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fda42-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fda42-119">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fda42-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fda42-120">Eingaben</span><span class="sxs-lookup"><span data-stu-id="fda42-120">INPUTS</span></span>

### <span data-ttu-id="fda42-121">Microsoft. Azure. Commands. Network. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="fda42-121">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="fda42-122">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="fda42-122">OUTPUTS</span></span>

### <span data-ttu-id="fda42-123">Microsoft. Azure. Commands. Network. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="fda42-123">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="fda42-124">Notizen</span><span class="sxs-lookup"><span data-stu-id="fda42-124">NOTES</span></span>

## <span data-ttu-id="fda42-125">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="fda42-125">RELATED LINKS</span></span>

[<span data-ttu-id="fda42-126">Get-AzApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="fda42-126">Get-AzApplicationGateway</span></span>](./Get-AzApplicationGateway.md)

[<span data-ttu-id="fda42-127">Neu – AzApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="fda42-127">New-AzApplicationGateway</span></span>](./New-AzApplicationGateway.md)

[<span data-ttu-id="fda42-128">Remove-AzApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="fda42-128">Remove-AzApplicationGateway</span></span>](./Remove-AzApplicationGateway.md)

[<span data-ttu-id="fda42-129">Satz-AzApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="fda42-129">Set-AzApplicationGateway</span></span>](./Set-AzApplicationGateway.md)

[<span data-ttu-id="fda42-130">Anfang-AzApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="fda42-130">Start-AzApplicationGateway</span></span>](./Start-AzApplicationGateway.md)


