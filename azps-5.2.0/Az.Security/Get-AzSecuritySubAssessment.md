---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/en-us/powershell/module/az.security/Get-AzSecuritySubAssessment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzSecuritySubAssessment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzSecuritySubAssessment.md
ms.openlocfilehash: 10808d7e4f6e270801ef56e48b605f4c23cd6246
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98296470"
---
# <span data-ttu-id="3f903-101">Get-AzSecuritySubAssessment</span><span class="sxs-lookup"><span data-stu-id="3f903-101">Get-AzSecuritySubAssessment</span></span>

## <span data-ttu-id="3f903-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3f903-102">SYNOPSIS</span></span>
<span data-ttu-id="3f903-103">Ruft untere Bewertungen ergebnisse in einem Abonnement ab.</span><span class="sxs-lookup"><span data-stu-id="3f903-103">Gets sub assessments results in a subscription.</span></span>

## <span data-ttu-id="3f903-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="3f903-104">SYNTAX</span></span>

### <span data-ttu-id="3f903-105">SubscriptionScope (Standard)</span><span class="sxs-lookup"><span data-stu-id="3f903-105">SubscriptionScope (Default)</span></span>
```
Get-AzSecuritySubAssessment [-AssessedResourceId <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="3f903-106">SubscriptionLevelResource</span><span class="sxs-lookup"><span data-stu-id="3f903-106">SubscriptionLevelResource</span></span>
```
Get-AzSecuritySubAssessment -Name <String> [-AssessedResourceId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="3f903-107">ResourceIdLevelResource</span><span class="sxs-lookup"><span data-stu-id="3f903-107">ResourceIdLevelResource</span></span>
```
Get-AzSecuritySubAssessment -Name <String> -AssessmentName <String> [-AssessedResourceId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="3f903-108">ResourceIdScope</span><span class="sxs-lookup"><span data-stu-id="3f903-108">ResourceIdScope</span></span>
```
Get-AzSecuritySubAssessment -AssessmentName <String> [-AssessedResourceId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="3f903-109">ResourceId</span><span class="sxs-lookup"><span data-stu-id="3f903-109">ResourceId</span></span>
```
Get-AzSecuritySubAssessment -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="3f903-110">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="3f903-110">DESCRIPTION</span></span>
<span data-ttu-id="3f903-111">Ruft untere Bewertungen ergebnisse in einem Abonnement ab.</span><span class="sxs-lookup"><span data-stu-id="3f903-111">Gets sub assessments results in a subscription.</span></span>

## <span data-ttu-id="3f903-112">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="3f903-112">EXAMPLES</span></span>

### <span data-ttu-id="3f903-113">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="3f903-113">Example 1</span></span>
```powershell
PS C:\> Get-AzSecuritySubAssessment
```

<span data-ttu-id="3f903-114">Ruft alle Ergebnisse der untergeordneten Bewertungen in einem Abonnement ab.</span><span class="sxs-lookup"><span data-stu-id="3f903-114">Gets all the sub assessments results in a subscription.</span></span>

## <span data-ttu-id="3f903-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="3f903-115">PARAMETERS</span></span>

### <span data-ttu-id="3f903-116">-AssessedResourceId</span><span class="sxs-lookup"><span data-stu-id="3f903-116">-AssessedResourceId</span></span>
<span data-ttu-id="3f903-117">Vollständige Ressourcen-ID der Ressource, für die die Bewertung berechnet wird.</span><span class="sxs-lookup"><span data-stu-id="3f903-117">Full resource ID of the resource that the assessment is calculated on.</span></span>

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

### <span data-ttu-id="3f903-118">-AssessmentName</span><span class="sxs-lookup"><span data-stu-id="3f903-118">-AssessmentName</span></span>
<span data-ttu-id="3f903-119">Name der Bewertungsressource.</span><span class="sxs-lookup"><span data-stu-id="3f903-119">Name of the assessment resource.</span></span>

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

### <span data-ttu-id="3f903-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3f903-120">-DefaultProfile</span></span>
<span data-ttu-id="3f903-121">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="3f903-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3f903-122">-Name</span><span class="sxs-lookup"><span data-stu-id="3f903-122">-Name</span></span>
<span data-ttu-id="3f903-123">Ressourcenname.</span><span class="sxs-lookup"><span data-stu-id="3f903-123">Resource name.</span></span>

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

### <span data-ttu-id="3f903-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="3f903-124">-ResourceId</span></span>
<span data-ttu-id="3f903-125">DIE ID der Sicherheitsressource, für die Sie den Befehl aufrufen möchten.</span><span class="sxs-lookup"><span data-stu-id="3f903-125">ID of the security resource that you want to invoke the command on.</span></span>

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

### <span data-ttu-id="3f903-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3f903-126">CommonParameters</span></span>
<span data-ttu-id="3f903-127">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3f903-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3f903-128">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="3f903-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3f903-129">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="3f903-129">INPUTS</span></span>

### <span data-ttu-id="3f903-130">System.String</span><span class="sxs-lookup"><span data-stu-id="3f903-130">System.String</span></span>

## <span data-ttu-id="3f903-131">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="3f903-131">OUTPUTS</span></span>

### <span data-ttu-id="3f903-132">Microsoft.Azure.Commands.Security.Models.SubAssessments.PSSecuritySubAssessment</span><span class="sxs-lookup"><span data-stu-id="3f903-132">Microsoft.Azure.Commands.Security.Models.SubAssessments.PSSecuritySubAssessment</span></span>

## <span data-ttu-id="3f903-133">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="3f903-133">NOTES</span></span>

## <span data-ttu-id="3f903-134">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="3f903-134">RELATED LINKS</span></span>
