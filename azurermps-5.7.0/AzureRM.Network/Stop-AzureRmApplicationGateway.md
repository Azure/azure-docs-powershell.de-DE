---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 2C9609E8-0D8B-471B-9F0E-672BF55C3A0E
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/stop-azurermapplicationgateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Stop-AzureRmApplicationGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Stop-AzureRmApplicationGateway.md
ms.openlocfilehash: cf8a639b6ebbe2b5ea7c0e07f212de3c742e7556
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93496382"
---
# <span data-ttu-id="3c96e-101">Stop-AzureRmApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="3c96e-101">Stop-AzureRmApplicationGateway</span></span>

## <span data-ttu-id="3c96e-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="3c96e-102">SYNOPSIS</span></span>
<span data-ttu-id="3c96e-103">Beenden eines Anwendungs Gateways</span><span class="sxs-lookup"><span data-stu-id="3c96e-103">Stops an application gateway</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="3c96e-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="3c96e-104">SYNTAX</span></span>

```
Stop-AzureRmApplicationGateway -ApplicationGateway <PSApplicationGateway> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="3c96e-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="3c96e-105">DESCRIPTION</span></span>
<span data-ttu-id="3c96e-106">Das Cmdlet **Stop-AzureRmApplicationGateway** beendet ein Anwendungsgateway.</span><span class="sxs-lookup"><span data-stu-id="3c96e-106">The **Stop-AzureRmApplicationGateway** cmdlet stops an application gateway.</span></span>

## <span data-ttu-id="3c96e-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="3c96e-107">EXAMPLES</span></span>

### <span data-ttu-id="3c96e-108">Beispiel 1: Beenden eines Anwendungs Gateways</span><span class="sxs-lookup"><span data-stu-id="3c96e-108">Example 1: Stop an application gateway</span></span>
```
PS C:\>Stop-AzureRmApplicationGateway -ApplicationGateway $AppGw
```

<span data-ttu-id="3c96e-109">Mit diesem Befehl wird das in der $AppGw-Variable gespeicherte Anwendungsgateway angehalten.</span><span class="sxs-lookup"><span data-stu-id="3c96e-109">This command stops the application gateway stored in the $AppGw variable.</span></span>

## <span data-ttu-id="3c96e-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="3c96e-110">PARAMETERS</span></span>

### <span data-ttu-id="3c96e-111">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="3c96e-111">-ApplicationGateway</span></span>
<span data-ttu-id="3c96e-112">Gibt das Anwendungsgateway an, das mit diesem Cmdlet beendet wird.</span><span class="sxs-lookup"><span data-stu-id="3c96e-112">Specifies the application gateway that this cmdlet stops.</span></span>

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

### <span data-ttu-id="3c96e-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="3c96e-113">-AsJob</span></span>
<span data-ttu-id="3c96e-114">Ausführen eines Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="3c96e-114">Run cmdlet in the background</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3c96e-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3c96e-115">-DefaultProfile</span></span>
<span data-ttu-id="3c96e-116">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="3c96e-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="3c96e-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3c96e-117">CommonParameters</span></span>
<span data-ttu-id="3c96e-118">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3c96e-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3c96e-119">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3c96e-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3c96e-120">Eingaben</span><span class="sxs-lookup"><span data-stu-id="3c96e-120">INPUTS</span></span>

### <span data-ttu-id="3c96e-121">System. String</span><span class="sxs-lookup"><span data-stu-id="3c96e-121">System.String</span></span>

## <span data-ttu-id="3c96e-122">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="3c96e-122">OUTPUTS</span></span>

### <span data-ttu-id="3c96e-123">Microsoft. Azure. Commands. Network. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="3c96e-123">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="3c96e-124">Notizen</span><span class="sxs-lookup"><span data-stu-id="3c96e-124">NOTES</span></span>

## <span data-ttu-id="3c96e-125">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="3c96e-125">RELATED LINKS</span></span>

[<span data-ttu-id="3c96e-126">Get-AzureRmApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="3c96e-126">Get-AzureRmApplicationGateway</span></span>](./Get-AzureRmApplicationGateway.md)

[<span data-ttu-id="3c96e-127">Neu – AzureRmApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="3c96e-127">New-AzureRmApplicationGateway</span></span>](./New-AzureRmApplicationGateway.md)

[<span data-ttu-id="3c96e-128">Remove-AzureRmApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="3c96e-128">Remove-AzureRmApplicationGateway</span></span>](./Remove-AzureRmApplicationGateway.md)

[<span data-ttu-id="3c96e-129">Satz-AzureRmApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="3c96e-129">Set-AzureRmApplicationGateway</span></span>](./Set-AzureRmApplicationGateway.md)

[<span data-ttu-id="3c96e-130">Anfang-AzureRmApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="3c96e-130">Start-AzureRmApplicationGateway</span></span>](./Start-AzureRmApplicationGateway.md)


