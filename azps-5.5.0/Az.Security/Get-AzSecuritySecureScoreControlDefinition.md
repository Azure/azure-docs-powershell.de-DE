---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/en-us/powershell/module/az.security/Get-AzSecuritySecureScoreControlDefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzSecuritySecureScoreControlDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzSecuritySecureScoreControlDefinition.md
ms.openlocfilehash: 557e048dcce528b4c84f6d1b74915d81d6c6f0c8
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100156372"
---
# <span data-ttu-id="8e679-101">Get-AzSecuritySecureScoreControlDefinition</span><span class="sxs-lookup"><span data-stu-id="8e679-101">Get-AzSecuritySecureScoreControlDefinition</span></span>

## <span data-ttu-id="8e679-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8e679-102">SYNOPSIS</span></span>
<span data-ttu-id="8e679-103">Ruft Definitionen von Secure Score Control für Sicherheit in einem Abonnement ab</span><span class="sxs-lookup"><span data-stu-id="8e679-103">Gets security secure score control definitions on a subscription</span></span>

## <span data-ttu-id="8e679-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="8e679-104">SYNTAX</span></span>

### <span data-ttu-id="8e679-105">SubscriptionScope (Standard)</span><span class="sxs-lookup"><span data-stu-id="8e679-105">SubscriptionScope (Default)</span></span>
```
Get-AzSecuritySecureScoreControlDefinition [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="8e679-106">SubscriptionLevelResource</span><span class="sxs-lookup"><span data-stu-id="8e679-106">SubscriptionLevelResource</span></span>
```
Get-AzSecuritySecureScoreControlDefinition -Name <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="8e679-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="8e679-107">EXAMPLES</span></span>

### <span data-ttu-id="8e679-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="8e679-108">Example 1</span></span>
```powershell
PS C:\> Get-AzSecuritySecureScoreControlDefinition
```

<span data-ttu-id="8e679-109">Ruft alle Definitionen der Secure Score -Sicherheit in einem Abonnement ab.</span><span class="sxs-lookup"><span data-stu-id="8e679-109">Gets all the security secure score control definitions in a subscription</span></span>

## <span data-ttu-id="8e679-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="8e679-110">PARAMETERS</span></span>

### <span data-ttu-id="8e679-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8e679-111">-DefaultProfile</span></span>
<span data-ttu-id="8e679-112">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="8e679-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8e679-113">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8e679-113">CommonParameters</span></span>
<span data-ttu-id="8e679-114">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8e679-114">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8e679-115">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="8e679-115">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8e679-116">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="8e679-116">INPUTS</span></span>

### <span data-ttu-id="8e679-117">System.String</span><span class="sxs-lookup"><span data-stu-id="8e679-117">System.String</span></span>

## <span data-ttu-id="8e679-118">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="8e679-118">OUTPUTS</span></span>

### <span data-ttu-id="8e679-119">Microsoft.Azure.Commands.Security.Models.Assessments.PSSecuritySecureScoreControlDefinition</span><span class="sxs-lookup"><span data-stu-id="8e679-119">Microsoft.Azure.Commands.Security.Models.Assessments.PSSecuritySecureScoreControlDefinition</span></span>

## <span data-ttu-id="8e679-120">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="8e679-120">NOTES</span></span>

## <span data-ttu-id="8e679-121">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="8e679-121">RELATED LINKS</span></span>
