---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/en-us/powershell/module/az.security/Get-AzSecuritySecureScoreControl
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzSecuritySecureScoreControl.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzSecuritySecureScoreControl.md
ms.openlocfilehash: 6f3b932ae4d8aad746eb1586525326ba9453af9a
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100156388"
---
# <span data-ttu-id="7b30e-101">Get-AzSecuritySecureScoreControl</span><span class="sxs-lookup"><span data-stu-id="7b30e-101">Get-AzSecuritySecureScoreControl</span></span>

## <span data-ttu-id="7b30e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7b30e-102">SYNOPSIS</span></span>
<span data-ttu-id="7b30e-103">Ruft Sicherheitskontrollen und deren Ergebnisse in einem Abonnement ab</span><span class="sxs-lookup"><span data-stu-id="7b30e-103">Gets security secure score controls and their results on a subscription</span></span>

## <span data-ttu-id="7b30e-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="7b30e-104">SYNTAX</span></span>

### <span data-ttu-id="7b30e-105">SubscriptionScope (Standard)</span><span class="sxs-lookup"><span data-stu-id="7b30e-105">SubscriptionScope (Default)</span></span>
```
Get-AzSecuritySecureScoreControl [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="7b30e-106">SubscriptionLevelResource</span><span class="sxs-lookup"><span data-stu-id="7b30e-106">SubscriptionLevelResource</span></span>
```
Get-AzSecuritySecureScoreControl -Name <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="7b30e-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="7b30e-107">EXAMPLES</span></span>

### <span data-ttu-id="7b30e-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="7b30e-108">Example 1</span></span>
```powershell
PS C:\> Get-AzSecuritySecureScoreControl
```

<span data-ttu-id="7b30e-109">Ruft alle sicheren Punkte in einem Abonnement ab</span><span class="sxs-lookup"><span data-stu-id="7b30e-109">Gets all the security secure scores in a subscription</span></span>

## <span data-ttu-id="7b30e-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="7b30e-110">PARAMETERS</span></span>

### <span data-ttu-id="7b30e-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7b30e-111">-DefaultProfile</span></span>
<span data-ttu-id="7b30e-112">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="7b30e-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7b30e-113">-Name</span><span class="sxs-lookup"><span data-stu-id="7b30e-113">-Name</span></span>
<span data-ttu-id="7b30e-114">Name der sicheren Punktzahl.</span><span class="sxs-lookup"><span data-stu-id="7b30e-114">Secure score name.</span></span>

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

### <span data-ttu-id="7b30e-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7b30e-115">CommonParameters</span></span>
<span data-ttu-id="7b30e-116">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7b30e-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7b30e-117">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="7b30e-117">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7b30e-118">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="7b30e-118">INPUTS</span></span>

### <span data-ttu-id="7b30e-119">System.String</span><span class="sxs-lookup"><span data-stu-id="7b30e-119">System.String</span></span>

## <span data-ttu-id="7b30e-120">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="7b30e-120">OUTPUTS</span></span>

### <span data-ttu-id="7b30e-121">Microsoft.Azure.Commands.Security.Models.Assessments.PSSecuritySecureScoreControl</span><span class="sxs-lookup"><span data-stu-id="7b30e-121">Microsoft.Azure.Commands.Security.Models.Assessments.PSSecuritySecureScoreControl</span></span>

## <span data-ttu-id="7b30e-122">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="7b30e-122">NOTES</span></span>

## <span data-ttu-id="7b30e-123">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="7b30e-123">RELATED LINKS</span></span>
