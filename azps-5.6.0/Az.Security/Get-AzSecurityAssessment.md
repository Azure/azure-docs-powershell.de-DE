---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/powershell/module/az.security/Get-AzSecurityAssessment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzSecurityAssessment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzSecurityAssessment.md
ms.openlocfilehash: 5a8a09955158c21ff6d52e2327370c48448c12d9
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101946888"
---
# <span data-ttu-id="3e84d-101">Get-AzSecurityAssessment</span><span class="sxs-lookup"><span data-stu-id="3e84d-101">Get-AzSecurityAssessment</span></span>

## <span data-ttu-id="3e84d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3e84d-102">SYNOPSIS</span></span>
<span data-ttu-id="3e84d-103">Ruft Sicherheitsbewertungen und deren Ergebnisse in einem Abonnement ab</span><span class="sxs-lookup"><span data-stu-id="3e84d-103">Gets security assessments and their results on a subscription</span></span>

## <span data-ttu-id="3e84d-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="3e84d-104">SYNTAX</span></span>

### <span data-ttu-id="3e84d-105">SubscriptionScope (Standard)</span><span class="sxs-lookup"><span data-stu-id="3e84d-105">SubscriptionScope (Default)</span></span>
```
Get-AzSecurityAssessment [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="3e84d-106">SubscriptionLevelResource</span><span class="sxs-lookup"><span data-stu-id="3e84d-106">SubscriptionLevelResource</span></span>
```
Get-AzSecurityAssessment -Name <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="3e84d-107">ResourceIdScope</span><span class="sxs-lookup"><span data-stu-id="3e84d-107">ResourceIdScope</span></span>
```
Get-AzSecurityAssessment -Name <String> -AssessedResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="3e84d-108">ResourceId</span><span class="sxs-lookup"><span data-stu-id="3e84d-108">ResourceId</span></span>
```
Get-AzSecurityAssessment -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="3e84d-109">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="3e84d-109">DESCRIPTION</span></span>
<span data-ttu-id="3e84d-110">Ruft die Sicherheitsbewertung und deren Ergebnisse im Abonnement ab.</span><span class="sxs-lookup"><span data-stu-id="3e84d-110">Gets security assessment and their results on subscription.</span></span> <span data-ttu-id="3e84d-111">Sicherheitsbewertungen lassen Sie wissen, welche bewährten Methoden vom Azure Security Center erneut empfohlen werden, um in Ihrem Azure-Abonnement abgemildert zu werden.</span><span class="sxs-lookup"><span data-stu-id="3e84d-111">Security assessments will let you know which best practices are recommanded by Azure Security Center to be mitigated on your Azure subscription.</span></span>

## <span data-ttu-id="3e84d-112">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="3e84d-112">EXAMPLES</span></span>

### <span data-ttu-id="3e84d-113">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="3e84d-113">Example 1</span></span>
```powershell
PS C:\> Get-AzSecurityAssessment
```

<span data-ttu-id="3e84d-114">Ruft alle Sicherheitsbeurteilungen in einem Abonnement ab.</span><span class="sxs-lookup"><span data-stu-id="3e84d-114">Gets all the security assessment in a subscription</span></span>

## <span data-ttu-id="3e84d-115">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="3e84d-115">PARAMETERS</span></span>

### <span data-ttu-id="3e84d-116">-AssessedResourceId</span><span class="sxs-lookup"><span data-stu-id="3e84d-116">-AssessedResourceId</span></span>
<span data-ttu-id="3e84d-117">Vollständige Ressourcen-ID der Ressource, für die die Bewertung berechnet wird.</span><span class="sxs-lookup"><span data-stu-id="3e84d-117">Full resource ID of the resource that the assessment is calculated on.</span></span>

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

### <span data-ttu-id="3e84d-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3e84d-118">-DefaultProfile</span></span>
<span data-ttu-id="3e84d-119">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="3e84d-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3e84d-120">-Name</span><span class="sxs-lookup"><span data-stu-id="3e84d-120">-Name</span></span>
<span data-ttu-id="3e84d-121">Ressourcenname.</span><span class="sxs-lookup"><span data-stu-id="3e84d-121">Resource name.</span></span>

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

### <span data-ttu-id="3e84d-122">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="3e84d-122">-ResourceId</span></span>
<span data-ttu-id="3e84d-123">ID der Sicherheitsressource, für die Sie den Befehl aufrufen möchten.</span><span class="sxs-lookup"><span data-stu-id="3e84d-123">ID of the security resource that you want to invoke the command on.</span></span>

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

### <span data-ttu-id="3e84d-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3e84d-124">CommonParameters</span></span>
<span data-ttu-id="3e84d-125">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3e84d-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3e84d-126">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="3e84d-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3e84d-127">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="3e84d-127">INPUTS</span></span>

### <span data-ttu-id="3e84d-128">System.String</span><span class="sxs-lookup"><span data-stu-id="3e84d-128">System.String</span></span>

## <span data-ttu-id="3e84d-129">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="3e84d-129">OUTPUTS</span></span>

### <span data-ttu-id="3e84d-130">Microsoft.Azure.Commands.Security.Models.Assessments.PSSecurityAssessment</span><span class="sxs-lookup"><span data-stu-id="3e84d-130">Microsoft.Azure.Commands.Security.Models.Assessments.PSSecurityAssessment</span></span>

## <span data-ttu-id="3e84d-131">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="3e84d-131">NOTES</span></span>

## <span data-ttu-id="3e84d-132">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="3e84d-132">RELATED LINKS</span></span>
