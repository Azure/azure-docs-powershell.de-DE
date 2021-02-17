---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 556A9F12-DF72-468F-9C3F-A747CC70BD2F
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/test-azdnsavailability
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Test-AzDnsAvailability.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Test-AzDnsAvailability.md
ms.openlocfilehash: 2ee468c47f22e90ce47b003dcae1becfb905134e
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100169589"
---
# <span data-ttu-id="a6eee-101">Test-AzDnsAvailability</span><span class="sxs-lookup"><span data-stu-id="a6eee-101">Test-AzDnsAvailability</span></span>

## <span data-ttu-id="a6eee-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a6eee-102">SYNOPSIS</span></span>
<span data-ttu-id="a6eee-103">Überprüft, ob ein Domänenname in der cloudapp.azure.com für die Verwendung verfügbar ist.</span><span class="sxs-lookup"><span data-stu-id="a6eee-103">Checks whether a domain name in the cloudapp.azure.com zone is available for use.</span></span>

## <span data-ttu-id="a6eee-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="a6eee-104">SYNTAX</span></span>

```
Test-AzDnsAvailability -DomainNameLabel <String> -Location <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="a6eee-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="a6eee-105">DESCRIPTION</span></span>
<span data-ttu-id="a6eee-106">Überprüft, ob ein Domänenname in der cloudapp.azure.com für die Verwendung verfügbar ist.</span><span class="sxs-lookup"><span data-stu-id="a6eee-106">Checks whether a domain name in the cloudapp.azure.com zone is available for use.</span></span>

## <span data-ttu-id="a6eee-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="a6eee-107">EXAMPLES</span></span>

### <span data-ttu-id="a6eee-108">Beispiel 1: Überprüfen Sie, contoso.westus.cloudapp.azure.com für die Verwendung zur Verfügung steht.</span><span class="sxs-lookup"><span data-stu-id="a6eee-108">Example 1: Check if contoso.westus.cloudapp.azure.com is available for use.</span></span>
```
Test-AzDnsAvailability -DomainNameLabel contoso -Location westus
```

## <span data-ttu-id="a6eee-109">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="a6eee-109">PARAMETERS</span></span>

### <span data-ttu-id="a6eee-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a6eee-110">-DefaultProfile</span></span>
<span data-ttu-id="a6eee-111">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="a6eee-111">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a6eee-112">-DomainNameLabel</span><span class="sxs-lookup"><span data-stu-id="a6eee-112">-DomainNameLabel</span></span>
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

### <span data-ttu-id="a6eee-113">-Location</span><span class="sxs-lookup"><span data-stu-id="a6eee-113">-Location</span></span>
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

### <span data-ttu-id="a6eee-114">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a6eee-114">CommonParameters</span></span>
<span data-ttu-id="a6eee-115">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a6eee-115">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a6eee-116">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a6eee-116">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a6eee-117">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="a6eee-117">INPUTS</span></span>

### <span data-ttu-id="a6eee-118">Keine</span><span class="sxs-lookup"><span data-stu-id="a6eee-118">None</span></span>

## <span data-ttu-id="a6eee-119">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="a6eee-119">OUTPUTS</span></span>

### <span data-ttu-id="a6eee-120">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="a6eee-120">System.Boolean</span></span>

## <span data-ttu-id="a6eee-121">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="a6eee-121">NOTES</span></span>

## <span data-ttu-id="a6eee-122">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="a6eee-122">RELATED LINKS</span></span>
