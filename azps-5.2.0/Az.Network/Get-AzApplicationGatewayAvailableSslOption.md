---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azapplicationgatewayavailablessloption
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayAvailableSslOption.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayAvailableSslOption.md
ms.openlocfilehash: f2175583aaaf3af04120e22e32db79d7b20f1e30
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98307203"
---
# <span data-ttu-id="f7848-101">Get-AzApplicationGatewayAvailableSslOption</span><span class="sxs-lookup"><span data-stu-id="f7848-101">Get-AzApplicationGatewayAvailableSslOption</span></span>

## <span data-ttu-id="f7848-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f7848-102">SYNOPSIS</span></span>
<span data-ttu-id="f7848-103">Ruft alle verfügbaren Ssl-Optionen für die Ssl-Richtlinie für das Anwendungsgateway ab.</span><span class="sxs-lookup"><span data-stu-id="f7848-103">Gets all available ssl options for ssl policy for Application Gateway.</span></span>

## <span data-ttu-id="f7848-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="f7848-104">SYNTAX</span></span>

```
Get-AzApplicationGatewayAvailableSslOption [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f7848-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="f7848-105">DESCRIPTION</span></span>
<span data-ttu-id="f7848-106">Das **Cmdlet "Get-AzApplicationGatewayAvailableSslOption"** ruft alle verfügbaren Optionen für SSL ab</span><span class="sxs-lookup"><span data-stu-id="f7848-106">The **Get-AzApplicationGatewayAvailableSslOption** cmdlet gets all available ssl options for ssl policy</span></span>

## <span data-ttu-id="f7848-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="f7848-107">EXAMPLES</span></span>

### <span data-ttu-id="f7848-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="f7848-108">Example 1</span></span>
```
PS C:\>$sslOptions = Get-AzApplicationGatewayAvailableSslOption
```

<span data-ttu-id="f7848-109">Diese Befehle geben alle verfügbaren Ssl-Optionen für die Ssl-Richtlinie zurück.</span><span class="sxs-lookup"><span data-stu-id="f7848-109">This commands returns all available ssl options for ssl policy.</span></span>

## <span data-ttu-id="f7848-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="f7848-110">PARAMETERS</span></span>

### <span data-ttu-id="f7848-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f7848-111">-DefaultProfile</span></span>
<span data-ttu-id="f7848-112">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="f7848-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f7848-113">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f7848-113">CommonParameters</span></span>
<span data-ttu-id="f7848-114">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f7848-114">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f7848-115">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="f7848-115">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f7848-116">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="f7848-116">INPUTS</span></span>

### <span data-ttu-id="f7848-117">Keine</span><span class="sxs-lookup"><span data-stu-id="f7848-117">None</span></span>

## <span data-ttu-id="f7848-118">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="f7848-118">OUTPUTS</span></span>

### <span data-ttu-id="f7848-119">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayAvailableSslOptions</span><span class="sxs-lookup"><span data-stu-id="f7848-119">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayAvailableSslOptions</span></span>

## <span data-ttu-id="f7848-120">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="f7848-120">NOTES</span></span>

## <span data-ttu-id="f7848-121">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="f7848-121">RELATED LINKS</span></span>
