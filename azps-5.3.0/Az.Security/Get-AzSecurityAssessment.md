---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/en-us/powershell/module/az.security/Get-AzSecurityAssessment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzSecurityAssessment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzSecurityAssessment.md
ms.openlocfilehash: 524a10f910b6e0d1b247f74a0b99063cbecba65c
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98472045"
---
# <span data-ttu-id="e9e6e-101">Get-AzSecurityAssessment</span><span class="sxs-lookup"><span data-stu-id="e9e6e-101">Get-AzSecurityAssessment</span></span>

## <span data-ttu-id="e9e6e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e9e6e-102">SYNOPSIS</span></span>
<span data-ttu-id="e9e6e-103">Ruft Sicherheitsbewertungen und deren Ergebnisse in einem Abonnement ab.</span><span class="sxs-lookup"><span data-stu-id="e9e6e-103">Gets security assessments and their results on a subscription</span></span>

## <span data-ttu-id="e9e6e-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="e9e6e-104">SYNTAX</span></span>

### <span data-ttu-id="e9e6e-105">SubscriptionScope (Standard)</span><span class="sxs-lookup"><span data-stu-id="e9e6e-105">SubscriptionScope (Default)</span></span>
```
Get-AzSecurityAssessment [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e9e6e-106">SubscriptionLevelResource</span><span class="sxs-lookup"><span data-stu-id="e9e6e-106">SubscriptionLevelResource</span></span>
```
Get-AzSecurityAssessment -Name <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e9e6e-107">ResourceIdScope</span><span class="sxs-lookup"><span data-stu-id="e9e6e-107">ResourceIdScope</span></span>
```
Get-AzSecurityAssessment -Name <String> -AssessedResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="e9e6e-108">ResourceId</span><span class="sxs-lookup"><span data-stu-id="e9e6e-108">ResourceId</span></span>
```
Get-AzSecurityAssessment -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e9e6e-109">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="e9e6e-109">DESCRIPTION</span></span>
<span data-ttu-id="e9e6e-110">Ruft sicherheitsbeurteilungen und deren Ergebnisse im Abonnement ab.</span><span class="sxs-lookup"><span data-stu-id="e9e6e-110">Gets security assessment and their results on subscription.</span></span> <span data-ttu-id="e9e6e-111">Sicherheitsbewertungen teilen Ihnen mit, welche bewährten Methoden vom Azure Security Center empfohlen werden, um in Ihrem Azure-Abonnement abgemildert zu werden.</span><span class="sxs-lookup"><span data-stu-id="e9e6e-111">Security assessments will let you know which best practices are recommanded by Azure Security Center to be mitigated on your Azure subscription.</span></span>

## <span data-ttu-id="e9e6e-112">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="e9e6e-112">EXAMPLES</span></span>

### <span data-ttu-id="e9e6e-113">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="e9e6e-113">Example 1</span></span>
```powershell
PS C:\> Get-AzSecurityAssessment
```

<span data-ttu-id="e9e6e-114">Ruft alle Sicherheitsbeurteilungen in einem Abonnement ab.</span><span class="sxs-lookup"><span data-stu-id="e9e6e-114">Gets all the security assessment in a subscription</span></span>

## <span data-ttu-id="e9e6e-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="e9e6e-115">PARAMETERS</span></span>

### <span data-ttu-id="e9e6e-116">-AssessedResourceId</span><span class="sxs-lookup"><span data-stu-id="e9e6e-116">-AssessedResourceId</span></span>
<span data-ttu-id="e9e6e-117">Vollständige Ressourcen-ID der Ressource, für die die Bewertung berechnet wird.</span><span class="sxs-lookup"><span data-stu-id="e9e6e-117">Full resource ID of the resource that the assessment is calculated on.</span></span>

```yaml
Type: String
Parameter Sets: ResourceIdScope
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e9e6e-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e9e6e-118">-DefaultProfile</span></span>
<span data-ttu-id="e9e6e-119">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="e9e6e-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e9e6e-120">-Name</span><span class="sxs-lookup"><span data-stu-id="e9e6e-120">-Name</span></span>
<span data-ttu-id="e9e6e-121">Ressourcenname.</span><span class="sxs-lookup"><span data-stu-id="e9e6e-121">Resource name.</span></span>

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

```yaml
Type: String
Parameter Sets: ResourceIdScope
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e9e6e-122">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="e9e6e-122">-ResourceId</span></span>
<span data-ttu-id="e9e6e-123">DIE ID der Sicherheitsressource, für die Sie den Befehl aufrufen möchten.</span><span class="sxs-lookup"><span data-stu-id="e9e6e-123">ID of the security resource that you want to invoke the command on.</span></span>

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

### <span data-ttu-id="e9e6e-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e9e6e-124">CommonParameters</span></span>
<span data-ttu-id="e9e6e-125">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e9e6e-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e9e6e-126">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="e9e6e-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e9e6e-127">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="e9e6e-127">INPUTS</span></span>

### <span data-ttu-id="e9e6e-128">System.String</span><span class="sxs-lookup"><span data-stu-id="e9e6e-128">System.String</span></span>

## <span data-ttu-id="e9e6e-129">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="e9e6e-129">OUTPUTS</span></span>

### <span data-ttu-id="e9e6e-130">Microsoft.Azure.Commands.Security.Models.Assessments.PSSecurityAssessment</span><span class="sxs-lookup"><span data-stu-id="e9e6e-130">Microsoft.Azure.Commands.Security.Models.Assessments.PSSecurityAssessment</span></span>

## <span data-ttu-id="e9e6e-131">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="e9e6e-131">NOTES</span></span>

## <span data-ttu-id="e9e6e-132">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="e9e6e-132">RELATED LINKS</span></span>
