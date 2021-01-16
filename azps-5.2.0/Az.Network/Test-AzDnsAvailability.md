---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 556A9F12-DF72-468F-9C3F-A747CC70BD2F
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/test-azdnsavailability
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Test-AzDnsAvailability.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Test-AzDnsAvailability.md
ms.openlocfilehash: 2ee468c47f22e90ce47b003dcae1becfb905134e
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98363388"
---
# <span data-ttu-id="f2af4-101">Test-AzDnsAvailability</span><span class="sxs-lookup"><span data-stu-id="f2af4-101">Test-AzDnsAvailability</span></span>

## <span data-ttu-id="f2af4-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f2af4-102">SYNOPSIS</span></span>
<span data-ttu-id="f2af4-103">Überprüft, ob ein Domänenname in der cloudapp.azure.com für die Verwendung verfügbar ist.</span><span class="sxs-lookup"><span data-stu-id="f2af4-103">Checks whether a domain name in the cloudapp.azure.com zone is available for use.</span></span>

## <span data-ttu-id="f2af4-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="f2af4-104">SYNTAX</span></span>

```
Test-AzDnsAvailability -DomainNameLabel <String> -Location <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="f2af4-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="f2af4-105">DESCRIPTION</span></span>
<span data-ttu-id="f2af4-106">Überprüft, ob ein Domänenname in der cloudapp.azure.com für die Verwendung verfügbar ist.</span><span class="sxs-lookup"><span data-stu-id="f2af4-106">Checks whether a domain name in the cloudapp.azure.com zone is available for use.</span></span>

## <span data-ttu-id="f2af4-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="f2af4-107">EXAMPLES</span></span>

### <span data-ttu-id="f2af4-108">Beispiel 1: Überprüfen Sie, contoso.westus.cloudapp.azure.com für die Verwendung zur Verfügung steht.</span><span class="sxs-lookup"><span data-stu-id="f2af4-108">Example 1: Check if contoso.westus.cloudapp.azure.com is available for use.</span></span>
```
Test-AzDnsAvailability -DomainNameLabel contoso -Location westus
```

## <span data-ttu-id="f2af4-109">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="f2af4-109">PARAMETERS</span></span>

### <span data-ttu-id="f2af4-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f2af4-110">-DefaultProfile</span></span>
<span data-ttu-id="f2af4-111">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="f2af4-111">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f2af4-112">-DomainNameLabel</span><span class="sxs-lookup"><span data-stu-id="f2af4-112">-DomainNameLabel</span></span>
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

### <span data-ttu-id="f2af4-113">-Location</span><span class="sxs-lookup"><span data-stu-id="f2af4-113">-Location</span></span>
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

### <span data-ttu-id="f2af4-114">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f2af4-114">CommonParameters</span></span>
<span data-ttu-id="f2af4-115">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f2af4-115">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f2af4-116">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f2af4-116">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f2af4-117">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="f2af4-117">INPUTS</span></span>

### <span data-ttu-id="f2af4-118">Keine</span><span class="sxs-lookup"><span data-stu-id="f2af4-118">None</span></span>

## <span data-ttu-id="f2af4-119">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="f2af4-119">OUTPUTS</span></span>

### <span data-ttu-id="f2af4-120">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="f2af4-120">System.Boolean</span></span>

## <span data-ttu-id="f2af4-121">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="f2af4-121">NOTES</span></span>

## <span data-ttu-id="f2af4-122">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="f2af4-122">RELATED LINKS</span></span>
