---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 556A9F12-DF72-468F-9C3F-A747CC70BD2F
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/test-azurermdnsavailability
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Test-AzureRmDnsAvailability.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Test-AzureRmDnsAvailability.md
ms.openlocfilehash: 348fd7e97566520b27163de91d4d52162d4c3978
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93498269"
---
# <span data-ttu-id="82e48-101">Test-AzureRmDnsAvailability</span><span class="sxs-lookup"><span data-stu-id="82e48-101">Test-AzureRmDnsAvailability</span></span>

## <span data-ttu-id="82e48-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="82e48-102">SYNOPSIS</span></span>
<span data-ttu-id="82e48-103">Überprüft, ob ein Domänenname in der cloudapp.Azure.com-Zone für die Verwendung verfügbar ist.</span><span class="sxs-lookup"><span data-stu-id="82e48-103">Checks whether a domain name in the cloudapp.azure.com zone is available for use.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="82e48-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="82e48-104">SYNTAX</span></span>

```
Test-AzureRmDnsAvailability -DomainNameLabel <String> -Location <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="82e48-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="82e48-105">DESCRIPTION</span></span>
<span data-ttu-id="82e48-106">Überprüft, ob ein Domänenname in der cloudapp.Azure.com-Zone für die Verwendung verfügbar ist.</span><span class="sxs-lookup"><span data-stu-id="82e48-106">Checks whether a domain name in the cloudapp.azure.com zone is available for use.</span></span>

## <span data-ttu-id="82e48-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="82e48-107">EXAMPLES</span></span>

### <span data-ttu-id="82e48-108">Beispiel 1: Überprüfen Sie, ob contoso.cloudapp.Azure.com zur Verwendung verfügbar ist.</span><span class="sxs-lookup"><span data-stu-id="82e48-108">Example 1: Check if contoso.cloudapp.azure.com is available for use.</span></span>
```
Test-AzureRmDnsAvailability -DomainNameLabel contoso -Location westus
```

## <span data-ttu-id="82e48-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="82e48-109">PARAMETERS</span></span>

### <span data-ttu-id="82e48-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="82e48-110">-DefaultProfile</span></span>
<span data-ttu-id="82e48-111">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="82e48-111">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="82e48-112">-DomainNameLabel</span><span class="sxs-lookup"><span data-stu-id="82e48-112">-DomainNameLabel</span></span>
```yaml
Type: System.String
Parameter Sets: (All)
Aliases: DomainQualifiedName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="82e48-113">-Standort</span><span class="sxs-lookup"><span data-stu-id="82e48-113">-Location</span></span>
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

### <span data-ttu-id="82e48-114">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="82e48-114">CommonParameters</span></span>
<span data-ttu-id="82e48-115">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="82e48-115">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="82e48-116">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="82e48-116">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="82e48-117">Eingaben</span><span class="sxs-lookup"><span data-stu-id="82e48-117">INPUTS</span></span>

### <span data-ttu-id="82e48-118">Keine</span><span class="sxs-lookup"><span data-stu-id="82e48-118">None</span></span>

## <span data-ttu-id="82e48-119">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="82e48-119">OUTPUTS</span></span>

### <span data-ttu-id="82e48-120">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="82e48-120">System.Boolean</span></span>

## <span data-ttu-id="82e48-121">Notizen</span><span class="sxs-lookup"><span data-stu-id="82e48-121">NOTES</span></span>

## <span data-ttu-id="82e48-122">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="82e48-122">RELATED LINKS</span></span>
