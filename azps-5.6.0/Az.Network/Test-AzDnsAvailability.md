---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 556A9F12-DF72-468F-9C3F-A747CC70BD2F
online version: https://docs.microsoft.com/powershell/module/az.network/test-azdnsavailability
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Test-AzDnsAvailability.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Test-AzDnsAvailability.md
ms.openlocfilehash: dbc21a337263bb0e509188d472e4ff984e22322b
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101918488"
---
# <span data-ttu-id="d84ba-101">Test-AzDnsAvailability</span><span class="sxs-lookup"><span data-stu-id="d84ba-101">Test-AzDnsAvailability</span></span>

## <span data-ttu-id="d84ba-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d84ba-102">SYNOPSIS</span></span>
<span data-ttu-id="d84ba-103">Überprüft, ob ein Domänenname in der cloudapp.azure.com zur Verwendung verfügbar ist.</span><span class="sxs-lookup"><span data-stu-id="d84ba-103">Checks whether a domain name in the cloudapp.azure.com zone is available for use.</span></span>

## <span data-ttu-id="d84ba-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="d84ba-104">SYNTAX</span></span>

```
Test-AzDnsAvailability -DomainNameLabel <String> -Location <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="d84ba-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="d84ba-105">DESCRIPTION</span></span>
<span data-ttu-id="d84ba-106">Überprüft, ob ein Domänenname in der cloudapp.azure.com zur Verwendung verfügbar ist.</span><span class="sxs-lookup"><span data-stu-id="d84ba-106">Checks whether a domain name in the cloudapp.azure.com zone is available for use.</span></span>

## <span data-ttu-id="d84ba-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="d84ba-107">EXAMPLES</span></span>

### <span data-ttu-id="d84ba-108">Beispiel 1: Überprüfen Sie, ob contoso.westus.cloudapp.azure.com zur Verwendung verfügbar ist.</span><span class="sxs-lookup"><span data-stu-id="d84ba-108">Example 1: Check if contoso.westus.cloudapp.azure.com is available for use.</span></span>
```
Test-AzDnsAvailability -DomainNameLabel contoso -Location westus
```

## <span data-ttu-id="d84ba-109">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="d84ba-109">PARAMETERS</span></span>

### <span data-ttu-id="d84ba-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d84ba-110">-DefaultProfile</span></span>
<span data-ttu-id="d84ba-111">Die Anmeldeinformationen, das Konto, der Mandant und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="d84ba-111">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d84ba-112">-DomainNameLabel</span><span class="sxs-lookup"><span data-stu-id="d84ba-112">-DomainNameLabel</span></span>
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

### <span data-ttu-id="d84ba-113">-Location</span><span class="sxs-lookup"><span data-stu-id="d84ba-113">-Location</span></span>
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

### <span data-ttu-id="d84ba-114">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d84ba-114">CommonParameters</span></span>
<span data-ttu-id="d84ba-115">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d84ba-115">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d84ba-116">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d84ba-116">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d84ba-117">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="d84ba-117">INPUTS</span></span>

### <span data-ttu-id="d84ba-118">Keine</span><span class="sxs-lookup"><span data-stu-id="d84ba-118">None</span></span>

## <span data-ttu-id="d84ba-119">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="d84ba-119">OUTPUTS</span></span>

### <span data-ttu-id="d84ba-120">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="d84ba-120">System.Boolean</span></span>

## <span data-ttu-id="d84ba-121">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="d84ba-121">NOTES</span></span>

## <span data-ttu-id="d84ba-122">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="d84ba-122">RELATED LINKS</span></span>
