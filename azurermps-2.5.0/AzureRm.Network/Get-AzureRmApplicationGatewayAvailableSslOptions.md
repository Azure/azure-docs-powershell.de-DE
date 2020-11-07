---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermapplicationgatewayavailablessloptions
schema: 2.0.0
ms.openlocfilehash: 023b2a43114fe47b50956e7f4626a75706e914f5
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/15/2020
ms.locfileid: "93849252"
---
# <span data-ttu-id="6720d-101">Get-AzureRmApplicationGatewayAvailableSslOptions</span><span class="sxs-lookup"><span data-stu-id="6720d-101">Get-AzureRmApplicationGatewayAvailableSslOptions</span></span>

## <span data-ttu-id="6720d-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="6720d-102">SYNOPSIS</span></span>
<span data-ttu-id="6720d-103">Ruft alle verfügbaren SSL-Optionen für die SSL-Richtlinie für Application Gateway ab.</span><span class="sxs-lookup"><span data-stu-id="6720d-103">Gets all available ssl options for ssl policy for Application Gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="6720d-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="6720d-104">SYNTAX</span></span>

```
Get-AzureRmApplicationGatewayAvailableSslOptions [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="6720d-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="6720d-105">DESCRIPTION</span></span>
<span data-ttu-id="6720d-106">Das Cmdlet " **Get-AzureRmApplicationGatewayAvailableSslOptions** " ruft alle verfügbaren SSL-Optionen für die SSL-Richtlinie ab</span><span class="sxs-lookup"><span data-stu-id="6720d-106">The **Get-AzureRmApplicationGatewayAvailableSslOptions** cmdlet gets all available ssl options for ssl policy</span></span>

## <span data-ttu-id="6720d-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="6720d-107">EXAMPLES</span></span>

### <span data-ttu-id="6720d-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="6720d-108">Example 1</span></span>
```
PS C:\>$sslOptions = Get-AzureRmApplicationGatewayAvailableSslOptions
```

<span data-ttu-id="6720d-109">Diese Befehle gibt alle verfügbaren SSL-Optionen für die SSL-Richtlinie zurück.</span><span class="sxs-lookup"><span data-stu-id="6720d-109">This commands returns all available ssl options for ssl policy.</span></span>

## <span data-ttu-id="6720d-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="6720d-110">PARAMETERS</span></span>

### <span data-ttu-id="6720d-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6720d-111">-DefaultProfile</span></span>
<span data-ttu-id="6720d-112">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="6720d-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="6720d-113">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6720d-113">CommonParameters</span></span>
<span data-ttu-id="6720d-114">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6720d-114">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6720d-115">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6720d-115">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6720d-116">Eingaben</span><span class="sxs-lookup"><span data-stu-id="6720d-116">INPUTS</span></span>

### <span data-ttu-id="6720d-117">Keine</span><span class="sxs-lookup"><span data-stu-id="6720d-117">None</span></span>

## <span data-ttu-id="6720d-118">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="6720d-118">OUTPUTS</span></span>

### <span data-ttu-id="6720d-119">Microsoft. Azure. Commands. Network. Models. PSApplicationGatewayAvailableSslOptions</span><span class="sxs-lookup"><span data-stu-id="6720d-119">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayAvailableSslOptions</span></span>

## <span data-ttu-id="6720d-120">Notizen</span><span class="sxs-lookup"><span data-stu-id="6720d-120">NOTES</span></span>

## <span data-ttu-id="6720d-121">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="6720d-121">RELATED LINKS</span></span>

