---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/new-azurermapplicationgatewaycustomerror
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmApplicationGatewayCustomError.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmApplicationGatewayCustomError.md
ms.openlocfilehash: 9e05684f40223711db7a8a6aaaf1cfb684efced4
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93502010"
---
# <span data-ttu-id="c160c-101">New-AzureRmApplicationGatewayCustomError</span><span class="sxs-lookup"><span data-stu-id="c160c-101">New-AzureRmApplicationGatewayCustomError</span></span>

## <span data-ttu-id="c160c-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="c160c-102">SYNOPSIS</span></span>
<span data-ttu-id="c160c-103">Erstellt einen benutzerdefinierten Fehler mit HTTP-Statuscode und benutzerdefinierter Fehlerseiten-URL.</span><span class="sxs-lookup"><span data-stu-id="c160c-103">Creates a custom error with http status code and custom error page url</span></span> 

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c160c-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="c160c-104">SYNTAX</span></span>

```
New-AzureRmApplicationGatewayCustomError -StatusCode <String> -CustomErrorPageUrl <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c160c-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="c160c-105">DESCRIPTION</span></span>
<span data-ttu-id="c160c-106">Mit dem Cmdlet **New-AzureRmApplicationGatewayCustomError** wird ein benutzerdefinierter Fehler erstellt.</span><span class="sxs-lookup"><span data-stu-id="c160c-106">The **New-AzureRmApplicationGatewayCustomError** cmdlet creates a custom error.</span></span>

## <span data-ttu-id="c160c-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="c160c-107">EXAMPLES</span></span>

### <span data-ttu-id="c160c-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="c160c-108">Example 1</span></span>
```powershell
PS C:\> $customError403Url = "https://mycustomerrorpages.blob.core.windows.net/errorpages/403-another.htm"
PS C:\> $ce = New-AzureRmApplicationGatewayCustomError -StatusCode HttpStatus403 -CustomErrorPageUrl $customError403Url
```

<span data-ttu-id="c160c-109">Mit diesem Befehl wird der benutzerdefinierte Fehler des HTTP-Statuscodes 403 erstellt.</span><span class="sxs-lookup"><span data-stu-id="c160c-109">This command creates the custom error of http status code 403.</span></span>

## <span data-ttu-id="c160c-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="c160c-110">PARAMETERS</span></span>

### <span data-ttu-id="c160c-111">-CustomErrorPageUrl</span><span class="sxs-lookup"><span data-stu-id="c160c-111">-CustomErrorPageUrl</span></span>
<span data-ttu-id="c160c-112">Fehlerseiten-URL des Kunden Fehlers des Application-Gateways.</span><span class="sxs-lookup"><span data-stu-id="c160c-112">Error page URL of the application gateway customer error.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c160c-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c160c-113">-DefaultProfile</span></span>
<span data-ttu-id="c160c-114">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="c160c-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c160c-115">-Statuscode</span><span class="sxs-lookup"><span data-stu-id="c160c-115">-StatusCode</span></span>
<span data-ttu-id="c160c-116">Status Code des Kunden Fehlers des Application Gateway-Kunden.</span><span class="sxs-lookup"><span data-stu-id="c160c-116">Status code of the application gateway customer error.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c160c-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c160c-117">CommonParameters</span></span>
<span data-ttu-id="c160c-118">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c160c-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="c160c-119">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c160c-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c160c-120">Eingaben</span><span class="sxs-lookup"><span data-stu-id="c160c-120">INPUTS</span></span>

### <span data-ttu-id="c160c-121">Keine</span><span class="sxs-lookup"><span data-stu-id="c160c-121">None</span></span>

## <span data-ttu-id="c160c-122">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="c160c-122">OUTPUTS</span></span>

### <span data-ttu-id="c160c-123">Microsoft. Azure. Commands. Network. Models. PSApplicationGatewayCustomError</span><span class="sxs-lookup"><span data-stu-id="c160c-123">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayCustomError</span></span>

## <span data-ttu-id="c160c-124">Notizen</span><span class="sxs-lookup"><span data-stu-id="c160c-124">NOTES</span></span>

## <span data-ttu-id="c160c-125">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="c160c-125">RELATED LINKS</span></span>
