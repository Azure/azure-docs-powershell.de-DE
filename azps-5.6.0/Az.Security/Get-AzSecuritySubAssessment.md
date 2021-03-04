---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/powershell/module/az.security/Get-AzSecuritySubAssessment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzSecuritySubAssessment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzSecuritySubAssessment.md
ms.openlocfilehash: c371749643952e8209b3cbec0721331a4d380d94
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101948467"
---
# <span data-ttu-id="0b8eb-101">Get-AzSecuritySubAssessment</span><span class="sxs-lookup"><span data-stu-id="0b8eb-101">Get-AzSecuritySubAssessment</span></span>

## <span data-ttu-id="0b8eb-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0b8eb-102">SYNOPSIS</span></span>
<span data-ttu-id="0b8eb-103">Ruft Unterbewertungsergebnisse in einem Abonnement ab.</span><span class="sxs-lookup"><span data-stu-id="0b8eb-103">Gets sub assessments results in a subscription.</span></span>

## <span data-ttu-id="0b8eb-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="0b8eb-104">SYNTAX</span></span>

### <span data-ttu-id="0b8eb-105">SubscriptionScope (Standard)</span><span class="sxs-lookup"><span data-stu-id="0b8eb-105">SubscriptionScope (Default)</span></span>
```
Get-AzSecuritySubAssessment [-AssessedResourceId <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="0b8eb-106">SubscriptionLevelResource</span><span class="sxs-lookup"><span data-stu-id="0b8eb-106">SubscriptionLevelResource</span></span>
```
Get-AzSecuritySubAssessment -Name <String> [-AssessedResourceId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="0b8eb-107">ResourceIdLevelResource</span><span class="sxs-lookup"><span data-stu-id="0b8eb-107">ResourceIdLevelResource</span></span>
```
Get-AzSecuritySubAssessment -Name <String> -AssessmentName <String> [-AssessedResourceId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="0b8eb-108">ResourceIdScope</span><span class="sxs-lookup"><span data-stu-id="0b8eb-108">ResourceIdScope</span></span>
```
Get-AzSecuritySubAssessment -AssessmentName <String> [-AssessedResourceId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="0b8eb-109">ResourceId</span><span class="sxs-lookup"><span data-stu-id="0b8eb-109">ResourceId</span></span>
```
Get-AzSecuritySubAssessment -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="0b8eb-110">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="0b8eb-110">DESCRIPTION</span></span>
<span data-ttu-id="0b8eb-111">Ruft Unterbewertungsergebnisse in einem Abonnement ab.</span><span class="sxs-lookup"><span data-stu-id="0b8eb-111">Gets sub assessments results in a subscription.</span></span>

## <span data-ttu-id="0b8eb-112">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="0b8eb-112">EXAMPLES</span></span>

### <span data-ttu-id="0b8eb-113">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="0b8eb-113">Example 1</span></span>
```powershell
PS C:\> Get-AzSecuritySubAssessment
```

<span data-ttu-id="0b8eb-114">Ruft alle Ergebnisse der Unterbewertungen in einem Abonnement ab.</span><span class="sxs-lookup"><span data-stu-id="0b8eb-114">Gets all the sub assessments results in a subscription.</span></span>

## <span data-ttu-id="0b8eb-115">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="0b8eb-115">PARAMETERS</span></span>

### <span data-ttu-id="0b8eb-116">-AssessedResourceId</span><span class="sxs-lookup"><span data-stu-id="0b8eb-116">-AssessedResourceId</span></span>
<span data-ttu-id="0b8eb-117">Vollständige Ressourcen-ID der Ressource, für die die Bewertung berechnet wird.</span><span class="sxs-lookup"><span data-stu-id="0b8eb-117">Full resource ID of the resource that the assessment is calculated on.</span></span>

```yaml
Type: String
Parameter Sets: SubscriptionScope, SubscriptionLevelResource
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: ResourceIdLevelResource, ResourceIdScope
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0b8eb-118">-AssessmentName</span><span class="sxs-lookup"><span data-stu-id="0b8eb-118">-AssessmentName</span></span>
<span data-ttu-id="0b8eb-119">Name der Bewertungsressource.</span><span class="sxs-lookup"><span data-stu-id="0b8eb-119">Name of the assessment resource.</span></span>

```yaml
Type: String
Parameter Sets: ResourceIdLevelResource, ResourceIdScope
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0b8eb-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0b8eb-120">-DefaultProfile</span></span>
<span data-ttu-id="0b8eb-121">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="0b8eb-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0b8eb-122">-Name</span><span class="sxs-lookup"><span data-stu-id="0b8eb-122">-Name</span></span>
<span data-ttu-id="0b8eb-123">Ressourcenname.</span><span class="sxs-lookup"><span data-stu-id="0b8eb-123">Resource name.</span></span>

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
Parameter Sets: ResourceIdLevelResource
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0b8eb-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="0b8eb-124">-ResourceId</span></span>
<span data-ttu-id="0b8eb-125">ID der Sicherheitsressource, für die Sie den Befehl aufrufen möchten.</span><span class="sxs-lookup"><span data-stu-id="0b8eb-125">ID of the security resource that you want to invoke the command on.</span></span>

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

### <span data-ttu-id="0b8eb-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0b8eb-126">CommonParameters</span></span>
<span data-ttu-id="0b8eb-127">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0b8eb-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0b8eb-128">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="0b8eb-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0b8eb-129">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="0b8eb-129">INPUTS</span></span>

### <span data-ttu-id="0b8eb-130">System.String</span><span class="sxs-lookup"><span data-stu-id="0b8eb-130">System.String</span></span>

## <span data-ttu-id="0b8eb-131">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="0b8eb-131">OUTPUTS</span></span>

### <span data-ttu-id="0b8eb-132">Microsoft.Azure.Commands.Security.Models.SubAssessments.PSSecuritySubAssessment</span><span class="sxs-lookup"><span data-stu-id="0b8eb-132">Microsoft.Azure.Commands.Security.Models.SubAssessments.PSSecuritySubAssessment</span></span>

## <span data-ttu-id="0b8eb-133">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="0b8eb-133">NOTES</span></span>

## <span data-ttu-id="0b8eb-134">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="0b8eb-134">RELATED LINKS</span></span>
