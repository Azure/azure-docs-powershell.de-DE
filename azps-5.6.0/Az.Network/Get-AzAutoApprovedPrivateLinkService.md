---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/get-azautoapprovedprivatelinkservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzAutoApprovedPrivateLinkService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzAutoApprovedPrivateLinkService.md
ms.openlocfilehash: 42e7b805e772e42ed395f8893b1140faaab715ba
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101940256"
---
# <span data-ttu-id="20446-101">Get-AzAutoApprovedPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="20446-101">Get-AzAutoApprovedPrivateLinkService</span></span>

## <span data-ttu-id="20446-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="20446-102">SYNOPSIS</span></span>
<span data-ttu-id="20446-103">Ruft ein Array privater Linkdienst-ID ab, das mit einem privaten Endpunkt verknüpft werden kann, der automatisch genehmigt wurde.</span><span class="sxs-lookup"><span data-stu-id="20446-103">Gets an array of private link service id that can be linked to a private end point with auto approved.</span></span>

## <span data-ttu-id="20446-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="20446-104">SYNTAX</span></span>

```
Get-AzAutoApprovedPrivateLinkService -Location <String> [-ResourceGroupName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="20446-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="20446-105">DESCRIPTION</span></span>
<span data-ttu-id="20446-106">Der **Get-AzAutoApprovedPrivateLinkService** ruft ein Array privater Linkdienst-ID ab, das mit einem privaten Endpunkt verknüpft werden kann, der automatisch genehmigt wurde.</span><span class="sxs-lookup"><span data-stu-id="20446-106">The **Get-AzAutoApprovedPrivateLinkService** gets an array of private link service id that can be linked to a private end point with auto approved.</span></span>

## <span data-ttu-id="20446-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="20446-107">EXAMPLES</span></span>

### <span data-ttu-id="20446-108">Beispiel</span><span class="sxs-lookup"><span data-stu-id="20446-108">Example</span></span>
```
Get-AzAutoApprovedPrivateLinkService -Location westus -ResourceGroupName TestResourceGroup
```

<span data-ttu-id="20446-109">In diesem Beispiel wird ein Array privater Linkdienst-ID zurückgeben, das mit einem privaten Endpunkt verknüpft werden kann, bei dem die automatische Genehmigung genehmigt wurde.</span><span class="sxs-lookup"><span data-stu-id="20446-109">This example return an array of private link service id that can be linked to a private end point with auto approved.</span></span>

## <span data-ttu-id="20446-110">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="20446-110">PARAMETERS</span></span>

### <span data-ttu-id="20446-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="20446-111">-DefaultProfile</span></span>
<span data-ttu-id="20446-112">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="20446-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="20446-113">-Location</span><span class="sxs-lookup"><span data-stu-id="20446-113">-Location</span></span>
```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="20446-114">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="20446-114">-ResourceGroupName</span></span>
<span data-ttu-id="20446-115">Gibt den Namen der Ressourcengruppe an.</span><span class="sxs-lookup"><span data-stu-id="20446-115">Specifies the name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="20446-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="20446-116">CommonParameters</span></span>
<span data-ttu-id="20446-117">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="20446-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="20446-118">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="20446-118">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="20446-119">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="20446-119">INPUTS</span></span>

### <span data-ttu-id="20446-120">Keine</span><span class="sxs-lookup"><span data-stu-id="20446-120">None</span></span>

## <span data-ttu-id="20446-121">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="20446-121">OUTPUTS</span></span>

### <span data-ttu-id="20446-122">Microsoft.Azure.Commands.Network.Models.PSAutoApprovedPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="20446-122">Microsoft.Azure.Commands.Network.Models.PSAutoApprovedPrivateLinkService</span></span>

## <span data-ttu-id="20446-123">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="20446-123">NOTES</span></span>

## <span data-ttu-id="20446-124">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="20446-124">RELATED LINKS</span></span>
