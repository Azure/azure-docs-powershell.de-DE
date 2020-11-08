---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 556A9F12-DF72-468F-9C3F-A747CC70BD2F
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/test-azdnsavailability
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Test-AzDnsAvailability.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Test-AzDnsAvailability.md
ms.openlocfilehash: 2ee468c47f22e90ce47b003dcae1becfb905134e
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/21/2020
ms.locfileid: "93995805"
---
# <span data-ttu-id="9086a-101">Test-AzDnsAvailability</span><span class="sxs-lookup"><span data-stu-id="9086a-101">Test-AzDnsAvailability</span></span>

## <span data-ttu-id="9086a-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="9086a-102">SYNOPSIS</span></span>
<span data-ttu-id="9086a-103">Überprüft, ob ein Domänenname in der cloudapp.Azure.com-Zone für die Verwendung verfügbar ist.</span><span class="sxs-lookup"><span data-stu-id="9086a-103">Checks whether a domain name in the cloudapp.azure.com zone is available for use.</span></span>

## <span data-ttu-id="9086a-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="9086a-104">SYNTAX</span></span>

```
Test-AzDnsAvailability -DomainNameLabel <String> -Location <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="9086a-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="9086a-105">DESCRIPTION</span></span>
<span data-ttu-id="9086a-106">Überprüft, ob ein Domänenname in der cloudapp.Azure.com-Zone für die Verwendung verfügbar ist.</span><span class="sxs-lookup"><span data-stu-id="9086a-106">Checks whether a domain name in the cloudapp.azure.com zone is available for use.</span></span>

## <span data-ttu-id="9086a-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="9086a-107">EXAMPLES</span></span>

### <span data-ttu-id="9086a-108">Beispiel 1: Überprüfen Sie, ob contoso.westus.cloudapp.Azure.com zur Verwendung verfügbar ist.</span><span class="sxs-lookup"><span data-stu-id="9086a-108">Example 1: Check if contoso.westus.cloudapp.azure.com is available for use.</span></span>
```
Test-AzDnsAvailability -DomainNameLabel contoso -Location westus
```

## <span data-ttu-id="9086a-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="9086a-109">PARAMETERS</span></span>

### <span data-ttu-id="9086a-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9086a-110">-DefaultProfile</span></span>
<span data-ttu-id="9086a-111">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="9086a-111">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="9086a-112">-DomainNameLabel</span><span class="sxs-lookup"><span data-stu-id="9086a-112">-DomainNameLabel</span></span>
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

### <span data-ttu-id="9086a-113">-Standort</span><span class="sxs-lookup"><span data-stu-id="9086a-113">-Location</span></span>
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

### <span data-ttu-id="9086a-114">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9086a-114">CommonParameters</span></span>
<span data-ttu-id="9086a-115">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9086a-115">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9086a-116">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9086a-116">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9086a-117">Eingaben</span><span class="sxs-lookup"><span data-stu-id="9086a-117">INPUTS</span></span>

### <span data-ttu-id="9086a-118">Keine</span><span class="sxs-lookup"><span data-stu-id="9086a-118">None</span></span>

## <span data-ttu-id="9086a-119">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="9086a-119">OUTPUTS</span></span>

### <span data-ttu-id="9086a-120">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="9086a-120">System.Boolean</span></span>

## <span data-ttu-id="9086a-121">Notizen</span><span class="sxs-lookup"><span data-stu-id="9086a-121">NOTES</span></span>

## <span data-ttu-id="9086a-122">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="9086a-122">RELATED LINKS</span></span>
