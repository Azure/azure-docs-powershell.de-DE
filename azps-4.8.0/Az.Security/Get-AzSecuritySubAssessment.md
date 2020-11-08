---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/en-us/powershell/module/az.security/Get-AzSecuritySubAssessment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzSecuritySubAssessment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzSecuritySubAssessment.md
ms.openlocfilehash: 10808d7e4f6e270801ef56e48b605f4c23cd6246
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94166098"
---
# <span data-ttu-id="442b8-101">Get-AzSecuritySubAssessment</span><span class="sxs-lookup"><span data-stu-id="442b8-101">Get-AzSecuritySubAssessment</span></span>

## <span data-ttu-id="442b8-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="442b8-102">SYNOPSIS</span></span>
<span data-ttu-id="442b8-103">Erhält unter Bewertungen Ergebnisse in einem Abonnement.</span><span class="sxs-lookup"><span data-stu-id="442b8-103">Gets sub assessments results in a subscription.</span></span>

## <span data-ttu-id="442b8-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="442b8-104">SYNTAX</span></span>

### <span data-ttu-id="442b8-105">SubscriptionScope (Standard)</span><span class="sxs-lookup"><span data-stu-id="442b8-105">SubscriptionScope (Default)</span></span>
```
Get-AzSecuritySubAssessment [-AssessedResourceId <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="442b8-106">SubscriptionLevelResource</span><span class="sxs-lookup"><span data-stu-id="442b8-106">SubscriptionLevelResource</span></span>
```
Get-AzSecuritySubAssessment -Name <String> [-AssessedResourceId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="442b8-107">ResourceIdLevelResource</span><span class="sxs-lookup"><span data-stu-id="442b8-107">ResourceIdLevelResource</span></span>
```
Get-AzSecuritySubAssessment -Name <String> -AssessmentName <String> [-AssessedResourceId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="442b8-108">ResourceIdScope</span><span class="sxs-lookup"><span data-stu-id="442b8-108">ResourceIdScope</span></span>
```
Get-AzSecuritySubAssessment -AssessmentName <String> [-AssessedResourceId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="442b8-109">ResourceId</span><span class="sxs-lookup"><span data-stu-id="442b8-109">ResourceId</span></span>
```
Get-AzSecuritySubAssessment -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="442b8-110">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="442b8-110">DESCRIPTION</span></span>
<span data-ttu-id="442b8-111">Erhält unter Bewertungen Ergebnisse in einem Abonnement.</span><span class="sxs-lookup"><span data-stu-id="442b8-111">Gets sub assessments results in a subscription.</span></span>

## <span data-ttu-id="442b8-112">Beispiele</span><span class="sxs-lookup"><span data-stu-id="442b8-112">EXAMPLES</span></span>

### <span data-ttu-id="442b8-113">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="442b8-113">Example 1</span></span>
```powershell
PS C:\> Get-AzSecuritySubAssessment
```

<span data-ttu-id="442b8-114">Ruft alle unter Bewertungen Ergebnisse in einem Abonnement ab.</span><span class="sxs-lookup"><span data-stu-id="442b8-114">Gets all the sub assessments results in a subscription.</span></span>

## <span data-ttu-id="442b8-115">Parameter</span><span class="sxs-lookup"><span data-stu-id="442b8-115">PARAMETERS</span></span>

### <span data-ttu-id="442b8-116">-AssessedResourceId</span><span class="sxs-lookup"><span data-stu-id="442b8-116">-AssessedResourceId</span></span>
<span data-ttu-id="442b8-117">Die vollständige Ressourcen-ID der Ressource, auf der die Bewertung berechnet wird.</span><span class="sxs-lookup"><span data-stu-id="442b8-117">Full resource ID of the resource that the assessment is calculated on.</span></span>

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

### <span data-ttu-id="442b8-118">-Assessmentname</span><span class="sxs-lookup"><span data-stu-id="442b8-118">-AssessmentName</span></span>
<span data-ttu-id="442b8-119">Der Name der Beurteilungs Ressource.</span><span class="sxs-lookup"><span data-stu-id="442b8-119">Name of the assessment resource.</span></span>

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

### <span data-ttu-id="442b8-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="442b8-120">-DefaultProfile</span></span>
<span data-ttu-id="442b8-121">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="442b8-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="442b8-122">-Name</span><span class="sxs-lookup"><span data-stu-id="442b8-122">-Name</span></span>
<span data-ttu-id="442b8-123">Ressourcenname</span><span class="sxs-lookup"><span data-stu-id="442b8-123">Resource name.</span></span>

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

### <span data-ttu-id="442b8-124">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="442b8-124">-ResourceId</span></span>
<span data-ttu-id="442b8-125">Die ID der Sicherheitsressource, auf der Sie den Befehl aufrufen möchten.</span><span class="sxs-lookup"><span data-stu-id="442b8-125">ID of the security resource that you want to invoke the command on.</span></span>

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

### <span data-ttu-id="442b8-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="442b8-126">CommonParameters</span></span>
<span data-ttu-id="442b8-127">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="442b8-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="442b8-128">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="442b8-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="442b8-129">Eingaben</span><span class="sxs-lookup"><span data-stu-id="442b8-129">INPUTS</span></span>

### <span data-ttu-id="442b8-130">System. String</span><span class="sxs-lookup"><span data-stu-id="442b8-130">System.String</span></span>

## <span data-ttu-id="442b8-131">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="442b8-131">OUTPUTS</span></span>

### <span data-ttu-id="442b8-132">Microsoft. Azure. Commands. Security. Models. subassessments. PSSecuritySubAssessment</span><span class="sxs-lookup"><span data-stu-id="442b8-132">Microsoft.Azure.Commands.Security.Models.SubAssessments.PSSecuritySubAssessment</span></span>

## <span data-ttu-id="442b8-133">Notizen</span><span class="sxs-lookup"><span data-stu-id="442b8-133">NOTES</span></span>

## <span data-ttu-id="442b8-134">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="442b8-134">RELATED LINKS</span></span>
