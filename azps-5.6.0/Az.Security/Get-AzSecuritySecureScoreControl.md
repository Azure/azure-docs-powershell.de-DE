---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/powershell/module/az.security/Get-AzSecuritySecureScoreControl
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzSecuritySecureScoreControl.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzSecuritySecureScoreControl.md
ms.openlocfilehash: 497865446e943fc34f45f6c98713d559086cca84
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101932267"
---
# <span data-ttu-id="59c43-101">Get-AzSecuritySecureScoreControl</span><span class="sxs-lookup"><span data-stu-id="59c43-101">Get-AzSecuritySecureScoreControl</span></span>

## <span data-ttu-id="59c43-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="59c43-102">SYNOPSIS</span></span>
<span data-ttu-id="59c43-103">Ruft sicherheitssicheren Bewertungssteuerelemente und deren Ergebnisse in einem Abonnement ab.</span><span class="sxs-lookup"><span data-stu-id="59c43-103">Gets security secure score controls and their results on a subscription</span></span>

## <span data-ttu-id="59c43-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="59c43-104">SYNTAX</span></span>

### <span data-ttu-id="59c43-105">SubscriptionScope (Standard)</span><span class="sxs-lookup"><span data-stu-id="59c43-105">SubscriptionScope (Default)</span></span>
```
Get-AzSecuritySecureScoreControl [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="59c43-106">SubscriptionLevelResource</span><span class="sxs-lookup"><span data-stu-id="59c43-106">SubscriptionLevelResource</span></span>
```
Get-AzSecuritySecureScoreControl -Name <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="59c43-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="59c43-107">EXAMPLES</span></span>

### <span data-ttu-id="59c43-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="59c43-108">Example 1</span></span>
```powershell
PS C:\> Get-AzSecuritySecureScoreControl
```

<span data-ttu-id="59c43-109">Ruft alle sicherheitssicheren Punkte in einem Abonnement ab.</span><span class="sxs-lookup"><span data-stu-id="59c43-109">Gets all the security secure scores in a subscription</span></span>

## <span data-ttu-id="59c43-110">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="59c43-110">PARAMETERS</span></span>

### <span data-ttu-id="59c43-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="59c43-111">-DefaultProfile</span></span>
<span data-ttu-id="59c43-112">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="59c43-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="59c43-113">-Name</span><span class="sxs-lookup"><span data-stu-id="59c43-113">-Name</span></span>
<span data-ttu-id="59c43-114">Sicherer Punktzahlname.</span><span class="sxs-lookup"><span data-stu-id="59c43-114">Secure score name.</span></span>

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

### <span data-ttu-id="59c43-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="59c43-115">CommonParameters</span></span>
<span data-ttu-id="59c43-116">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="59c43-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="59c43-117">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="59c43-117">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="59c43-118">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="59c43-118">INPUTS</span></span>

### <span data-ttu-id="59c43-119">System.String</span><span class="sxs-lookup"><span data-stu-id="59c43-119">System.String</span></span>

## <span data-ttu-id="59c43-120">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="59c43-120">OUTPUTS</span></span>

### <span data-ttu-id="59c43-121">Microsoft.Azure.Commands.Security.Models.Assessments.PSSecuritySecureScoreControl</span><span class="sxs-lookup"><span data-stu-id="59c43-121">Microsoft.Azure.Commands.Security.Models.Assessments.PSSecuritySecureScoreControl</span></span>

## <span data-ttu-id="59c43-122">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="59c43-122">NOTES</span></span>

## <span data-ttu-id="59c43-123">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="59c43-123">RELATED LINKS</span></span>
