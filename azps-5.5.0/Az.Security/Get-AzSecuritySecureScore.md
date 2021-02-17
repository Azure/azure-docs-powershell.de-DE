---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/en-us/powershell/module/az.security/Get-AzSecuritySecureScore
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzSecuritySecureScore.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzSecuritySecureScore.md
ms.openlocfilehash: 5b14298f48c5723b4d84b0f22d799ac0a21699e0
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100156404"
---
# <span data-ttu-id="7a8aa-101">Get-AzSecuritySecureScore</span><span class="sxs-lookup"><span data-stu-id="7a8aa-101">Get-AzSecuritySecureScore</span></span>

## <span data-ttu-id="7a8aa-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7a8aa-102">SYNOPSIS</span></span>
<span data-ttu-id="7a8aa-103">Erhalten sicherer Punkte und deren Ergebnisse in einem Abonnement</span><span class="sxs-lookup"><span data-stu-id="7a8aa-103">Gets security secure scores and their results on a subscription</span></span>

## <span data-ttu-id="7a8aa-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="7a8aa-104">SYNTAX</span></span>

### <span data-ttu-id="7a8aa-105">SubscriptionScope (Standard)</span><span class="sxs-lookup"><span data-stu-id="7a8aa-105">SubscriptionScope (Default)</span></span>
```
Get-AzSecuritySecureScore [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="7a8aa-106">SubscriptionLevelResource</span><span class="sxs-lookup"><span data-stu-id="7a8aa-106">SubscriptionLevelResource</span></span>
```
Get-AzSecuritySecureScore -Name <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="7a8aa-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="7a8aa-107">EXAMPLES</span></span>

### <span data-ttu-id="7a8aa-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="7a8aa-108">Example 1</span></span>
```powershell
PS C:\> Get-AzSecuritySecureScore
```

<span data-ttu-id="7a8aa-109">Ruft alle sicheren Punkte in einem Abonnement ab</span><span class="sxs-lookup"><span data-stu-id="7a8aa-109">Gets all the security secure scores in a subscription</span></span>

## <span data-ttu-id="7a8aa-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="7a8aa-110">PARAMETERS</span></span>

### <span data-ttu-id="7a8aa-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7a8aa-111">-DefaultProfile</span></span>
<span data-ttu-id="7a8aa-112">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="7a8aa-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7a8aa-113">-Name</span><span class="sxs-lookup"><span data-stu-id="7a8aa-113">-Name</span></span>
<span data-ttu-id="7a8aa-114">Ressourcenname.</span><span class="sxs-lookup"><span data-stu-id="7a8aa-114">Resource name.</span></span>

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

### <span data-ttu-id="7a8aa-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7a8aa-115">CommonParameters</span></span>
<span data-ttu-id="7a8aa-116">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7a8aa-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7a8aa-117">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="7a8aa-117">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7a8aa-118">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="7a8aa-118">INPUTS</span></span>

### <span data-ttu-id="7a8aa-119">System.String</span><span class="sxs-lookup"><span data-stu-id="7a8aa-119">System.String</span></span>

## <span data-ttu-id="7a8aa-120">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="7a8aa-120">OUTPUTS</span></span>

### <span data-ttu-id="7a8aa-121">Microsoft.Azure.Commands.Security.Models.Assessments.PSSecuritySecureScore</span><span class="sxs-lookup"><span data-stu-id="7a8aa-121">Microsoft.Azure.Commands.Security.Models.Assessments.PSSecuritySecureScore</span></span>

## <span data-ttu-id="7a8aa-122">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="7a8aa-122">NOTES</span></span>

## <span data-ttu-id="7a8aa-123">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="7a8aa-123">RELATED LINKS</span></span>
