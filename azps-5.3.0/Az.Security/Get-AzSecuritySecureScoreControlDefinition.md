---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/en-us/powershell/module/az.security/Get-AzSecuritySecureScoreControlDefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzSecuritySecureScoreControlDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzSecuritySecureScoreControlDefinition.md
ms.openlocfilehash: 557e048dcce528b4c84f6d1b74915d81d6c6f0c8
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98472028"
---
# <span data-ttu-id="aeff1-101">Get-AzSecuritySecureScoreControlDefinition</span><span class="sxs-lookup"><span data-stu-id="aeff1-101">Get-AzSecuritySecureScoreControlDefinition</span></span>

## <span data-ttu-id="aeff1-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="aeff1-102">SYNOPSIS</span></span>
<span data-ttu-id="aeff1-103">Ruft Definitionen von Secure Score Control für Sicherheit in einem Abonnement ab</span><span class="sxs-lookup"><span data-stu-id="aeff1-103">Gets security secure score control definitions on a subscription</span></span>

## <span data-ttu-id="aeff1-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="aeff1-104">SYNTAX</span></span>

### <span data-ttu-id="aeff1-105">SubscriptionScope (Standard)</span><span class="sxs-lookup"><span data-stu-id="aeff1-105">SubscriptionScope (Default)</span></span>
```
Get-AzSecuritySecureScoreControlDefinition [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="aeff1-106">SubscriptionLevelResource</span><span class="sxs-lookup"><span data-stu-id="aeff1-106">SubscriptionLevelResource</span></span>
```
Get-AzSecuritySecureScoreControlDefinition -Name <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="aeff1-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="aeff1-107">EXAMPLES</span></span>

### <span data-ttu-id="aeff1-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="aeff1-108">Example 1</span></span>
```powershell
PS C:\> Get-AzSecuritySecureScoreControlDefinition
```

<span data-ttu-id="aeff1-109">Ruft alle Definitionen der Secure Score -Sicherheit in einem Abonnement ab.</span><span class="sxs-lookup"><span data-stu-id="aeff1-109">Gets all the security secure score control definitions in a subscription</span></span>

## <span data-ttu-id="aeff1-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="aeff1-110">PARAMETERS</span></span>

### <span data-ttu-id="aeff1-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="aeff1-111">-DefaultProfile</span></span>
<span data-ttu-id="aeff1-112">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="aeff1-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="aeff1-113">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="aeff1-113">CommonParameters</span></span>
<span data-ttu-id="aeff1-114">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="aeff1-114">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="aeff1-115">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="aeff1-115">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="aeff1-116">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="aeff1-116">INPUTS</span></span>

### <span data-ttu-id="aeff1-117">System.String</span><span class="sxs-lookup"><span data-stu-id="aeff1-117">System.String</span></span>

## <span data-ttu-id="aeff1-118">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="aeff1-118">OUTPUTS</span></span>

### <span data-ttu-id="aeff1-119">Microsoft.Azure.Commands.Security.Models.Assessments.PSSecuritySecureScoreControlDefinition</span><span class="sxs-lookup"><span data-stu-id="aeff1-119">Microsoft.Azure.Commands.Security.Models.Assessments.PSSecuritySecureScoreControlDefinition</span></span>

## <span data-ttu-id="aeff1-120">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="aeff1-120">NOTES</span></span>

## <span data-ttu-id="aeff1-121">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="aeff1-121">RELATED LINKS</span></span>
