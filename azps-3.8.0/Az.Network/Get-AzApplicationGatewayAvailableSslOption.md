---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azapplicationgatewayavailablessloption
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayAvailableSslOption.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayAvailableSslOption.md
ms.openlocfilehash: f2175583aaaf3af04120e22e32db79d7b20f1e30
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/21/2020
ms.locfileid: "94003789"
---
# <span data-ttu-id="7e5dd-101">Get-AzApplicationGatewayAvailableSslOption</span><span class="sxs-lookup"><span data-stu-id="7e5dd-101">Get-AzApplicationGatewayAvailableSslOption</span></span>

## <span data-ttu-id="7e5dd-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="7e5dd-102">SYNOPSIS</span></span>
<span data-ttu-id="7e5dd-103">Ruft alle verfügbaren SSL-Optionen für die SSL-Richtlinie für Application Gateway ab.</span><span class="sxs-lookup"><span data-stu-id="7e5dd-103">Gets all available ssl options for ssl policy for Application Gateway.</span></span>

## <span data-ttu-id="7e5dd-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="7e5dd-104">SYNTAX</span></span>

```
Get-AzApplicationGatewayAvailableSslOption [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="7e5dd-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="7e5dd-105">DESCRIPTION</span></span>
<span data-ttu-id="7e5dd-106">Das Cmdlet " **Get-AzApplicationGatewayAvailableSslOption** " ruft alle verfügbaren SSL-Optionen für die SSL-Richtlinie ab</span><span class="sxs-lookup"><span data-stu-id="7e5dd-106">The **Get-AzApplicationGatewayAvailableSslOption** cmdlet gets all available ssl options for ssl policy</span></span>

## <span data-ttu-id="7e5dd-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="7e5dd-107">EXAMPLES</span></span>

### <span data-ttu-id="7e5dd-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="7e5dd-108">Example 1</span></span>
```
PS C:\>$sslOptions = Get-AzApplicationGatewayAvailableSslOption
```

<span data-ttu-id="7e5dd-109">Diese Befehle gibt alle verfügbaren SSL-Optionen für die SSL-Richtlinie zurück.</span><span class="sxs-lookup"><span data-stu-id="7e5dd-109">This commands returns all available ssl options for ssl policy.</span></span>

## <span data-ttu-id="7e5dd-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="7e5dd-110">PARAMETERS</span></span>

### <span data-ttu-id="7e5dd-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7e5dd-111">-DefaultProfile</span></span>
<span data-ttu-id="7e5dd-112">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="7e5dd-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="7e5dd-113">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7e5dd-113">CommonParameters</span></span>
<span data-ttu-id="7e5dd-114">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7e5dd-114">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7e5dd-115">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="7e5dd-115">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7e5dd-116">Eingaben</span><span class="sxs-lookup"><span data-stu-id="7e5dd-116">INPUTS</span></span>

### <span data-ttu-id="7e5dd-117">Keine</span><span class="sxs-lookup"><span data-stu-id="7e5dd-117">None</span></span>

## <span data-ttu-id="7e5dd-118">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="7e5dd-118">OUTPUTS</span></span>

### <span data-ttu-id="7e5dd-119">Microsoft. Azure. Commands. Network. Models. PSApplicationGatewayAvailableSslOptions</span><span class="sxs-lookup"><span data-stu-id="7e5dd-119">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayAvailableSslOptions</span></span>

## <span data-ttu-id="7e5dd-120">Notizen</span><span class="sxs-lookup"><span data-stu-id="7e5dd-120">NOTES</span></span>

## <span data-ttu-id="7e5dd-121">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="7e5dd-121">RELATED LINKS</span></span>
