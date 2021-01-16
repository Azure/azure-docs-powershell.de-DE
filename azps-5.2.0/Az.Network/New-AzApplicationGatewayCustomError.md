---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azapplicationgatewaycustomerror
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayCustomError.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayCustomError.md
ms.openlocfilehash: 162e9a5cd869b6ea50e6d72dc7041ab14dc9a8e6
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98298011"
---
# <span data-ttu-id="2155c-101">New-AzApplicationGatewayCustomError</span><span class="sxs-lookup"><span data-stu-id="2155c-101">New-AzApplicationGatewayCustomError</span></span>

## <span data-ttu-id="2155c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2155c-102">SYNOPSIS</span></span>
<span data-ttu-id="2155c-103">Erstellt einen benutzerdefinierten Fehler mit http-Statuscode und der URL der benutzerdefinierten Fehlerseite.</span><span class="sxs-lookup"><span data-stu-id="2155c-103">Creates a custom error with http status code and custom error page url</span></span> 

## <span data-ttu-id="2155c-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="2155c-104">SYNTAX</span></span>

```
New-AzApplicationGatewayCustomError -StatusCode <String> -CustomErrorPageUrl <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="2155c-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="2155c-105">DESCRIPTION</span></span>
<span data-ttu-id="2155c-106">Das **Cmdlet "New-AzApplicationGatewayCustomError"** erstellt einen benutzerdefinierten Fehler.</span><span class="sxs-lookup"><span data-stu-id="2155c-106">The **New-AzApplicationGatewayCustomError** cmdlet creates a custom error.</span></span>

## <span data-ttu-id="2155c-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="2155c-107">EXAMPLES</span></span>

### <span data-ttu-id="2155c-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="2155c-108">Example 1</span></span>
```powershell
PS C:\> $customError403Url = "https://mycustomerrorpages.blob.core.windows.net/errorpages/403-another.htm"
PS C:\> $ce = New-AzApplicationGatewayCustomError -StatusCode HttpStatus403 -CustomErrorPageUrl $customError403Url
```

<span data-ttu-id="2155c-109">Mit diesem Befehl wird der benutzerdefinierte Fehler des Http-Statuscodes 403 erstellt.</span><span class="sxs-lookup"><span data-stu-id="2155c-109">This command creates the custom error of http status code 403.</span></span>

## <span data-ttu-id="2155c-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="2155c-110">PARAMETERS</span></span>

### <span data-ttu-id="2155c-111">-CustomErrorPageUrl</span><span class="sxs-lookup"><span data-stu-id="2155c-111">-CustomErrorPageUrl</span></span>
<span data-ttu-id="2155c-112">Fehlerseiten-URL des Kundenfehlers des Anwendungsgateways.</span><span class="sxs-lookup"><span data-stu-id="2155c-112">Error page URL of the application gateway customer error.</span></span>

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

### <span data-ttu-id="2155c-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2155c-113">-DefaultProfile</span></span>
<span data-ttu-id="2155c-114">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="2155c-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2155c-115">-StatusCode</span><span class="sxs-lookup"><span data-stu-id="2155c-115">-StatusCode</span></span>
<span data-ttu-id="2155c-116">Statuscode des Kundenfehlers des Anwendungsgateways.</span><span class="sxs-lookup"><span data-stu-id="2155c-116">Status code of the application gateway customer error.</span></span>

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

### <span data-ttu-id="2155c-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2155c-117">CommonParameters</span></span>
<span data-ttu-id="2155c-118">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2155c-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2155c-119">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2155c-119">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2155c-120">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="2155c-120">INPUTS</span></span>

### <span data-ttu-id="2155c-121">Keine</span><span class="sxs-lookup"><span data-stu-id="2155c-121">None</span></span>

## <span data-ttu-id="2155c-122">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="2155c-122">OUTPUTS</span></span>

### <span data-ttu-id="2155c-123">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayCustomError</span><span class="sxs-lookup"><span data-stu-id="2155c-123">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayCustomError</span></span>

## <span data-ttu-id="2155c-124">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="2155c-124">NOTES</span></span>

## <span data-ttu-id="2155c-125">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="2155c-125">RELATED LINKS</span></span>

[<span data-ttu-id="2155c-126">Add-AzApplicationGatewayCustomError</span><span class="sxs-lookup"><span data-stu-id="2155c-126">Add-AzApplicationGatewayCustomError</span></span>](./Add-AzApplicationGatewayCustomError.md)

[<span data-ttu-id="2155c-127">Get-AzApplicationGatewayCustomError</span><span class="sxs-lookup"><span data-stu-id="2155c-127">Get-AzApplicationGatewayCustomError</span></span>](./Get-AzApplicationGatewayCustomError.md)

[<span data-ttu-id="2155c-128">Remove-AzApplicationGatewayCustomError</span><span class="sxs-lookup"><span data-stu-id="2155c-128">Remove-AzApplicationGatewayCustomError</span></span>](./Remove-AzApplicationGatewayCustomError.md)

[<span data-ttu-id="2155c-129">Set-AzApplicationGatewayCustomError</span><span class="sxs-lookup"><span data-stu-id="2155c-129">Set-AzApplicationGatewayCustomError</span></span>](./Set-AzApplicationGatewayCustomError.md)
