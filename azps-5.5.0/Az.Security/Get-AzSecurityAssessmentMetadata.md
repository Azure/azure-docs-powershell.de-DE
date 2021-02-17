---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/en-us/powershell/module/az.security/Get-AzSecurityAssessmentMetadata
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzSecurityAssessmentMetadata.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzSecurityAssessmentMetadata.md
ms.openlocfilehash: 6b2819041b9fd136ee1ecc65b9d8b36132af5317
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100165169"
---
# <span data-ttu-id="b94cf-101">Get-AzSecurityAssessmentMetadata</span><span class="sxs-lookup"><span data-stu-id="b94cf-101">Get-AzSecurityAssessmentMetadata</span></span>

## <span data-ttu-id="b94cf-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b94cf-102">SYNOPSIS</span></span>
<span data-ttu-id="b94cf-103">Ruft Sicherheitsbewertungstypen und Metadta in einem Abonnement ab.</span><span class="sxs-lookup"><span data-stu-id="b94cf-103">Gets security assessments types and metadta in a subscription.</span></span>

## <span data-ttu-id="b94cf-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="b94cf-104">SYNTAX</span></span>

### <span data-ttu-id="b94cf-105">SubscriptionScope (Standard)</span><span class="sxs-lookup"><span data-stu-id="b94cf-105">SubscriptionScope (Default)</span></span>
```
Get-AzSecurityAssessmentMetadata [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b94cf-106">SubscriptionLevelResource</span><span class="sxs-lookup"><span data-stu-id="b94cf-106">SubscriptionLevelResource</span></span>
```
Get-AzSecurityAssessmentMetadata -Name <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b94cf-107">ResourceId</span><span class="sxs-lookup"><span data-stu-id="b94cf-107">ResourceId</span></span>
```
Get-AzSecurityAssessmentMetadata -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="b94cf-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="b94cf-108">DESCRIPTION</span></span>
<span data-ttu-id="b94cf-109">Ruft Sicherheitsbewertungstypen und Metadta in einem Abonnement ab.</span><span class="sxs-lookup"><span data-stu-id="b94cf-109">Gets security assessments types and metadta in a subscription.</span></span> <span data-ttu-id="b94cf-110">Metadaten zur Sicherheitsbewertung umfassen Built-In Bewertungen und benutzerdefinierte Bewertungstypen, die der Benutzer definieren kann.</span><span class="sxs-lookup"><span data-stu-id="b94cf-110">Security Assessment metadata include Built-In assessments and custom assessment types that the user can define.</span></span>

## <span data-ttu-id="b94cf-111">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="b94cf-111">EXAMPLES</span></span>

### <span data-ttu-id="b94cf-112">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="b94cf-112">Example 1</span></span>
```powershell
PS C:\> Get-AzSecurityAssessmentMetadata
```

<span data-ttu-id="b94cf-113">Ruft alle integrierten Bewertungen und die benutzerdefinierten Bewertungen ab, die im aktuellen Abonnement konfiguriert wurden.</span><span class="sxs-lookup"><span data-stu-id="b94cf-113">Gets all the built in assessments and the custom assessments that were configured on the current subscription.</span></span>

## <span data-ttu-id="b94cf-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="b94cf-114">PARAMETERS</span></span>

### <span data-ttu-id="b94cf-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b94cf-115">-DefaultProfile</span></span>
<span data-ttu-id="b94cf-116">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="b94cf-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b94cf-117">-Name</span><span class="sxs-lookup"><span data-stu-id="b94cf-117">-Name</span></span>
<span data-ttu-id="b94cf-118">Ressourcenname.</span><span class="sxs-lookup"><span data-stu-id="b94cf-118">Resource name.</span></span>

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

### <span data-ttu-id="b94cf-119">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="b94cf-119">-ResourceId</span></span>
<span data-ttu-id="b94cf-120">DIE ID der Sicherheitsressource, für die Sie den Befehl aufrufen möchten.</span><span class="sxs-lookup"><span data-stu-id="b94cf-120">ID of the security resource that you want to invoke the command on.</span></span>

```yaml
Type: String
Parameter Sets: ResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b94cf-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b94cf-121">CommonParameters</span></span>
<span data-ttu-id="b94cf-122">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b94cf-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b94cf-123">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="b94cf-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b94cf-124">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="b94cf-124">INPUTS</span></span>

### <span data-ttu-id="b94cf-125">System.String</span><span class="sxs-lookup"><span data-stu-id="b94cf-125">System.String</span></span>

## <span data-ttu-id="b94cf-126">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="b94cf-126">OUTPUTS</span></span>

### <span data-ttu-id="b94cf-127">Microsoft.Azure.Commands.Security.Models.AssessmentMetadata.PSSecurityAssessmentMetadata</span><span class="sxs-lookup"><span data-stu-id="b94cf-127">Microsoft.Azure.Commands.Security.Models.AssessmentMetadata.PSSecurityAssessmentMetadata</span></span>

## <span data-ttu-id="b94cf-128">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="b94cf-128">NOTES</span></span>

## <span data-ttu-id="b94cf-129">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="b94cf-129">RELATED LINKS</span></span>
