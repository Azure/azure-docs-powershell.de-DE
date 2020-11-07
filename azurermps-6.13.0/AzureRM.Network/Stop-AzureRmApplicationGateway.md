---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 2C9609E8-0D8B-471B-9F0E-672BF55C3A0E
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/stop-azurermapplicationgateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Stop-AzureRmApplicationGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Stop-AzureRmApplicationGateway.md
ms.openlocfilehash: a235ae8ad4467e135e85599300869bcb36805a30
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93662994"
---
# <span data-ttu-id="22b82-101">Stop-AzureRmApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="22b82-101">Stop-AzureRmApplicationGateway</span></span>

## <span data-ttu-id="22b82-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="22b82-102">SYNOPSIS</span></span>
<span data-ttu-id="22b82-103">Beenden eines Anwendungs Gateways</span><span class="sxs-lookup"><span data-stu-id="22b82-103">Stops an application gateway</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="22b82-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="22b82-104">SYNTAX</span></span>

```
Stop-AzureRmApplicationGateway -ApplicationGateway <PSApplicationGateway> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="22b82-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="22b82-105">DESCRIPTION</span></span>
<span data-ttu-id="22b82-106">Das Cmdlet **Stop-AzureRmApplicationGateway** beendet ein Anwendungsgateway.</span><span class="sxs-lookup"><span data-stu-id="22b82-106">The **Stop-AzureRmApplicationGateway** cmdlet stops an application gateway.</span></span>

## <span data-ttu-id="22b82-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="22b82-107">EXAMPLES</span></span>

### <span data-ttu-id="22b82-108">Beispiel 1: Beenden eines Anwendungs Gateways</span><span class="sxs-lookup"><span data-stu-id="22b82-108">Example 1: Stop an application gateway</span></span>
```
PS C:\>Stop-AzureRmApplicationGateway -ApplicationGateway $AppGw
```

<span data-ttu-id="22b82-109">Mit diesem Befehl wird das in der $AppGw-Variable gespeicherte Anwendungsgateway angehalten.</span><span class="sxs-lookup"><span data-stu-id="22b82-109">This command stops the application gateway stored in the $AppGw variable.</span></span>

## <span data-ttu-id="22b82-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="22b82-110">PARAMETERS</span></span>

### <span data-ttu-id="22b82-111">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="22b82-111">-ApplicationGateway</span></span>
<span data-ttu-id="22b82-112">Gibt das Anwendungsgateway an, das mit diesem Cmdlet beendet wird.</span><span class="sxs-lookup"><span data-stu-id="22b82-112">Specifies the application gateway that this cmdlet stops.</span></span>

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

### <span data-ttu-id="22b82-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="22b82-113">-AsJob</span></span>
<span data-ttu-id="22b82-114">Ausführen eines Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="22b82-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="22b82-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="22b82-115">-DefaultProfile</span></span>
<span data-ttu-id="22b82-116">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="22b82-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="22b82-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="22b82-117">CommonParameters</span></span>
<span data-ttu-id="22b82-118">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="22b82-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="22b82-119">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="22b82-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="22b82-120">Eingaben</span><span class="sxs-lookup"><span data-stu-id="22b82-120">INPUTS</span></span>

### <span data-ttu-id="22b82-121">Microsoft. Azure. Commands. Network. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="22b82-121">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>
<span data-ttu-id="22b82-122">Parameter: ApplicationGateway (ByValue)</span><span class="sxs-lookup"><span data-stu-id="22b82-122">Parameters: ApplicationGateway (ByValue)</span></span>

## <span data-ttu-id="22b82-123">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="22b82-123">OUTPUTS</span></span>

### <span data-ttu-id="22b82-124">Microsoft. Azure. Commands. Network. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="22b82-124">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="22b82-125">Notizen</span><span class="sxs-lookup"><span data-stu-id="22b82-125">NOTES</span></span>

## <span data-ttu-id="22b82-126">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="22b82-126">RELATED LINKS</span></span>

[<span data-ttu-id="22b82-127">Get-AzureRmApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="22b82-127">Get-AzureRmApplicationGateway</span></span>](./Get-AzureRmApplicationGateway.md)

[<span data-ttu-id="22b82-128">Neu – AzureRmApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="22b82-128">New-AzureRmApplicationGateway</span></span>](./New-AzureRmApplicationGateway.md)

[<span data-ttu-id="22b82-129">Remove-AzureRmApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="22b82-129">Remove-AzureRmApplicationGateway</span></span>](./Remove-AzureRmApplicationGateway.md)

[<span data-ttu-id="22b82-130">Satz-AzureRmApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="22b82-130">Set-AzureRmApplicationGateway</span></span>](./Set-AzureRmApplicationGateway.md)

[<span data-ttu-id="22b82-131">Anfang-AzureRmApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="22b82-131">Start-AzureRmApplicationGateway</span></span>](./Start-AzureRmApplicationGateway.md)


