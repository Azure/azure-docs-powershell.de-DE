---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azapplicationgatewaycustomerror
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayCustomError.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayCustomError.md
ms.openlocfilehash: 162e9a5cd869b6ea50e6d72dc7041ab14dc9a8e6
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100169938"
---
# <span data-ttu-id="61fc2-101">New-AzApplicationGatewayCustomError</span><span class="sxs-lookup"><span data-stu-id="61fc2-101">New-AzApplicationGatewayCustomError</span></span>

## <span data-ttu-id="61fc2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="61fc2-102">SYNOPSIS</span></span>
<span data-ttu-id="61fc2-103">Erstellt einen benutzerdefinierten Fehler mit http-Statuscode und benutzerdefinierter Fehlerseiten-URL.</span><span class="sxs-lookup"><span data-stu-id="61fc2-103">Creates a custom error with http status code and custom error page url</span></span> 

## <span data-ttu-id="61fc2-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="61fc2-104">SYNTAX</span></span>

```
New-AzApplicationGatewayCustomError -StatusCode <String> -CustomErrorPageUrl <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="61fc2-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="61fc2-105">DESCRIPTION</span></span>
<span data-ttu-id="61fc2-106">Das **Cmdlet "New-AzApplicationGatewayCustomError"** erstellt einen benutzerdefinierten Fehler.</span><span class="sxs-lookup"><span data-stu-id="61fc2-106">The **New-AzApplicationGatewayCustomError** cmdlet creates a custom error.</span></span>

## <span data-ttu-id="61fc2-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="61fc2-107">EXAMPLES</span></span>

### <span data-ttu-id="61fc2-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="61fc2-108">Example 1</span></span>
```powershell
PS C:\> $customError403Url = "https://mycustomerrorpages.blob.core.windows.net/errorpages/403-another.htm"
PS C:\> $ce = New-AzApplicationGatewayCustomError -StatusCode HttpStatus403 -CustomErrorPageUrl $customError403Url
```

<span data-ttu-id="61fc2-109">Mit diesem Befehl wird der benutzerdefinierte Fehler des Http-Statuscodes 403 erstellt.</span><span class="sxs-lookup"><span data-stu-id="61fc2-109">This command creates the custom error of http status code 403.</span></span>

## <span data-ttu-id="61fc2-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="61fc2-110">PARAMETERS</span></span>

### <span data-ttu-id="61fc2-111">-CustomErrorPageUrl</span><span class="sxs-lookup"><span data-stu-id="61fc2-111">-CustomErrorPageUrl</span></span>
<span data-ttu-id="61fc2-112">Url der Fehlerseite des Kundenfehlers des Anwendungsgateways.</span><span class="sxs-lookup"><span data-stu-id="61fc2-112">Error page URL of the application gateway customer error.</span></span>

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

### <span data-ttu-id="61fc2-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="61fc2-113">-DefaultProfile</span></span>
<span data-ttu-id="61fc2-114">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="61fc2-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="61fc2-115">-StatusCode</span><span class="sxs-lookup"><span data-stu-id="61fc2-115">-StatusCode</span></span>
<span data-ttu-id="61fc2-116">Statuscode des Kundenfehlers des Anwendungsgateways.</span><span class="sxs-lookup"><span data-stu-id="61fc2-116">Status code of the application gateway customer error.</span></span>

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

### <span data-ttu-id="61fc2-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="61fc2-117">CommonParameters</span></span>
<span data-ttu-id="61fc2-118">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="61fc2-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="61fc2-119">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="61fc2-119">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="61fc2-120">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="61fc2-120">INPUTS</span></span>

### <span data-ttu-id="61fc2-121">Keine</span><span class="sxs-lookup"><span data-stu-id="61fc2-121">None</span></span>

## <span data-ttu-id="61fc2-122">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="61fc2-122">OUTPUTS</span></span>

### <span data-ttu-id="61fc2-123">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayCustomError</span><span class="sxs-lookup"><span data-stu-id="61fc2-123">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayCustomError</span></span>

## <span data-ttu-id="61fc2-124">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="61fc2-124">NOTES</span></span>

## <span data-ttu-id="61fc2-125">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="61fc2-125">RELATED LINKS</span></span>

[<span data-ttu-id="61fc2-126">Add-AzApplicationGatewayCustomError</span><span class="sxs-lookup"><span data-stu-id="61fc2-126">Add-AzApplicationGatewayCustomError</span></span>](./Add-AzApplicationGatewayCustomError.md)

[<span data-ttu-id="61fc2-127">Get-AzApplicationGatewayCustomError</span><span class="sxs-lookup"><span data-stu-id="61fc2-127">Get-AzApplicationGatewayCustomError</span></span>](./Get-AzApplicationGatewayCustomError.md)

[<span data-ttu-id="61fc2-128">Remove-AzApplicationGatewayCustomError</span><span class="sxs-lookup"><span data-stu-id="61fc2-128">Remove-AzApplicationGatewayCustomError</span></span>](./Remove-AzApplicationGatewayCustomError.md)

[<span data-ttu-id="61fc2-129">Set-AzApplicationGatewayCustomError</span><span class="sxs-lookup"><span data-stu-id="61fc2-129">Set-AzApplicationGatewayCustomError</span></span>](./Set-AzApplicationGatewayCustomError.md)
