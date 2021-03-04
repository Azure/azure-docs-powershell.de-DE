---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/powershell/module/az.security/Get-AzSecuritySecureScore
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzSecuritySecureScore.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzSecuritySecureScore.md
ms.openlocfilehash: 0cce3e4e1aa0f5de93e9c54c00cfa1902a4c24b2
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101941416"
---
# <span data-ttu-id="22e48-101">Get-AzSecuritySecureScore</span><span class="sxs-lookup"><span data-stu-id="22e48-101">Get-AzSecuritySecureScore</span></span>

## <span data-ttu-id="22e48-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="22e48-102">SYNOPSIS</span></span>
<span data-ttu-id="22e48-103">Ruft sichere Bewertungen und deren Ergebnisse in einem Abonnement ab</span><span class="sxs-lookup"><span data-stu-id="22e48-103">Gets security secure scores and their results on a subscription</span></span>

## <span data-ttu-id="22e48-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="22e48-104">SYNTAX</span></span>

### <span data-ttu-id="22e48-105">SubscriptionScope (Standard)</span><span class="sxs-lookup"><span data-stu-id="22e48-105">SubscriptionScope (Default)</span></span>
```
Get-AzSecuritySecureScore [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="22e48-106">SubscriptionLevelResource</span><span class="sxs-lookup"><span data-stu-id="22e48-106">SubscriptionLevelResource</span></span>
```
Get-AzSecuritySecureScore -Name <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="22e48-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="22e48-107">EXAMPLES</span></span>

### <span data-ttu-id="22e48-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="22e48-108">Example 1</span></span>
```powershell
PS C:\> Get-AzSecuritySecureScore
```

<span data-ttu-id="22e48-109">Ruft alle sicherheitssicheren Punkte in einem Abonnement ab.</span><span class="sxs-lookup"><span data-stu-id="22e48-109">Gets all the security secure scores in a subscription</span></span>

## <span data-ttu-id="22e48-110">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="22e48-110">PARAMETERS</span></span>

### <span data-ttu-id="22e48-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="22e48-111">-DefaultProfile</span></span>
<span data-ttu-id="22e48-112">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="22e48-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="22e48-113">-Name</span><span class="sxs-lookup"><span data-stu-id="22e48-113">-Name</span></span>
<span data-ttu-id="22e48-114">Ressourcenname.</span><span class="sxs-lookup"><span data-stu-id="22e48-114">Resource name.</span></span>

```yaml
Type: String
Parameter Sets: SubscriptionLevelResource
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="22e48-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="22e48-115">CommonParameters</span></span>
<span data-ttu-id="22e48-116">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="22e48-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="22e48-117">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="22e48-117">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="22e48-118">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="22e48-118">INPUTS</span></span>

### <span data-ttu-id="22e48-119">System.String</span><span class="sxs-lookup"><span data-stu-id="22e48-119">System.String</span></span>

## <span data-ttu-id="22e48-120">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="22e48-120">OUTPUTS</span></span>

### <span data-ttu-id="22e48-121">Microsoft.Azure.Commands.Security.Models.Assessments.PSSecuritySecureScore</span><span class="sxs-lookup"><span data-stu-id="22e48-121">Microsoft.Azure.Commands.Security.Models.Assessments.PSSecuritySecureScore</span></span>

## <span data-ttu-id="22e48-122">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="22e48-122">NOTES</span></span>

## <span data-ttu-id="22e48-123">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="22e48-123">RELATED LINKS</span></span>
