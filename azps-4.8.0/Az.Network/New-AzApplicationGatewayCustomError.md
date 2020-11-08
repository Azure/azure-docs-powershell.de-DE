---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azapplicationgatewaycustomerror
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayCustomError.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayCustomError.md
ms.openlocfilehash: 162e9a5cd869b6ea50e6d72dc7041ab14dc9a8e6
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94174603"
---
# <span data-ttu-id="4b4bf-101">New-AzApplicationGatewayCustomError</span><span class="sxs-lookup"><span data-stu-id="4b4bf-101">New-AzApplicationGatewayCustomError</span></span>

## <span data-ttu-id="4b4bf-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="4b4bf-102">SYNOPSIS</span></span>
<span data-ttu-id="4b4bf-103">Erstellt einen benutzerdefinierten Fehler mit HTTP-Statuscode und benutzerdefinierter Fehlerseiten-URL.</span><span class="sxs-lookup"><span data-stu-id="4b4bf-103">Creates a custom error with http status code and custom error page url</span></span> 

## <span data-ttu-id="4b4bf-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="4b4bf-104">SYNTAX</span></span>

```
New-AzApplicationGatewayCustomError -StatusCode <String> -CustomErrorPageUrl <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="4b4bf-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="4b4bf-105">DESCRIPTION</span></span>
<span data-ttu-id="4b4bf-106">Mit dem Cmdlet **New-AzApplicationGatewayCustomError** wird ein benutzerdefinierter Fehler erstellt.</span><span class="sxs-lookup"><span data-stu-id="4b4bf-106">The **New-AzApplicationGatewayCustomError** cmdlet creates a custom error.</span></span>

## <span data-ttu-id="4b4bf-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="4b4bf-107">EXAMPLES</span></span>

### <span data-ttu-id="4b4bf-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="4b4bf-108">Example 1</span></span>
```powershell
PS C:\> $customError403Url = "https://mycustomerrorpages.blob.core.windows.net/errorpages/403-another.htm"
PS C:\> $ce = New-AzApplicationGatewayCustomError -StatusCode HttpStatus403 -CustomErrorPageUrl $customError403Url
```

<span data-ttu-id="4b4bf-109">Mit diesem Befehl wird der benutzerdefinierte Fehler des HTTP-Statuscodes 403 erstellt.</span><span class="sxs-lookup"><span data-stu-id="4b4bf-109">This command creates the custom error of http status code 403.</span></span>

## <span data-ttu-id="4b4bf-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="4b4bf-110">PARAMETERS</span></span>

### <span data-ttu-id="4b4bf-111">-CustomErrorPageUrl</span><span class="sxs-lookup"><span data-stu-id="4b4bf-111">-CustomErrorPageUrl</span></span>
<span data-ttu-id="4b4bf-112">Fehlerseiten-URL des Kunden Fehlers des Application-Gateways.</span><span class="sxs-lookup"><span data-stu-id="4b4bf-112">Error page URL of the application gateway customer error.</span></span>

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

### <span data-ttu-id="4b4bf-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4b4bf-113">-DefaultProfile</span></span>
<span data-ttu-id="4b4bf-114">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="4b4bf-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4b4bf-115">-Statuscode</span><span class="sxs-lookup"><span data-stu-id="4b4bf-115">-StatusCode</span></span>
<span data-ttu-id="4b4bf-116">Status Code des Kunden Fehlers des Application Gateway-Kunden.</span><span class="sxs-lookup"><span data-stu-id="4b4bf-116">Status code of the application gateway customer error.</span></span>

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

### <span data-ttu-id="4b4bf-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4b4bf-117">CommonParameters</span></span>
<span data-ttu-id="4b4bf-118">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4b4bf-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4b4bf-119">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4b4bf-119">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4b4bf-120">Eingaben</span><span class="sxs-lookup"><span data-stu-id="4b4bf-120">INPUTS</span></span>

### <span data-ttu-id="4b4bf-121">Keine</span><span class="sxs-lookup"><span data-stu-id="4b4bf-121">None</span></span>

## <span data-ttu-id="4b4bf-122">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="4b4bf-122">OUTPUTS</span></span>

### <span data-ttu-id="4b4bf-123">Microsoft. Azure. Commands. Network. Models. PSApplicationGatewayCustomError</span><span class="sxs-lookup"><span data-stu-id="4b4bf-123">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayCustomError</span></span>

## <span data-ttu-id="4b4bf-124">Notizen</span><span class="sxs-lookup"><span data-stu-id="4b4bf-124">NOTES</span></span>

## <span data-ttu-id="4b4bf-125">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="4b4bf-125">RELATED LINKS</span></span>

[<span data-ttu-id="4b4bf-126">Add-AzApplicationGatewayCustomError</span><span class="sxs-lookup"><span data-stu-id="4b4bf-126">Add-AzApplicationGatewayCustomError</span></span>](./Add-AzApplicationGatewayCustomError.md)

[<span data-ttu-id="4b4bf-127">Get-AzApplicationGatewayCustomError</span><span class="sxs-lookup"><span data-stu-id="4b4bf-127">Get-AzApplicationGatewayCustomError</span></span>](./Get-AzApplicationGatewayCustomError.md)

[<span data-ttu-id="4b4bf-128">Remove-AzApplicationGatewayCustomError</span><span class="sxs-lookup"><span data-stu-id="4b4bf-128">Remove-AzApplicationGatewayCustomError</span></span>](./Remove-AzApplicationGatewayCustomError.md)

[<span data-ttu-id="4b4bf-129">Satz-AzApplicationGatewayCustomError</span><span class="sxs-lookup"><span data-stu-id="4b4bf-129">Set-AzApplicationGatewayCustomError</span></span>](./Set-AzApplicationGatewayCustomError.md)
