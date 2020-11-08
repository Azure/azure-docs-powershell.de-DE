---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/en-us/powershell/module/az.security/Get-AzSecurityAssessment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzSecurityAssessment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzSecurityAssessment.md
ms.openlocfilehash: 524a10f910b6e0d1b247f74a0b99063cbecba65c
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94179670"
---
# <span data-ttu-id="e0cf1-101">Get-AzSecurityAssessment</span><span class="sxs-lookup"><span data-stu-id="e0cf1-101">Get-AzSecurityAssessment</span></span>

## <span data-ttu-id="e0cf1-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="e0cf1-102">SYNOPSIS</span></span>
<span data-ttu-id="e0cf1-103">Ruft Sicherheitsbewertungen und deren Ergebnisse für ein Abonnement ab.</span><span class="sxs-lookup"><span data-stu-id="e0cf1-103">Gets security assessments and their results on a subscription</span></span>

## <span data-ttu-id="e0cf1-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="e0cf1-104">SYNTAX</span></span>

### <span data-ttu-id="e0cf1-105">SubscriptionScope (Standard)</span><span class="sxs-lookup"><span data-stu-id="e0cf1-105">SubscriptionScope (Default)</span></span>
```
Get-AzSecurityAssessment [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e0cf1-106">SubscriptionLevelResource</span><span class="sxs-lookup"><span data-stu-id="e0cf1-106">SubscriptionLevelResource</span></span>
```
Get-AzSecurityAssessment -Name <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e0cf1-107">ResourceIdScope</span><span class="sxs-lookup"><span data-stu-id="e0cf1-107">ResourceIdScope</span></span>
```
Get-AzSecurityAssessment -Name <String> -AssessedResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="e0cf1-108">ResourceId</span><span class="sxs-lookup"><span data-stu-id="e0cf1-108">ResourceId</span></span>
```
Get-AzSecurityAssessment -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e0cf1-109">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="e0cf1-109">DESCRIPTION</span></span>
<span data-ttu-id="e0cf1-110">Ruft die Sicherheitsbewertung und die Ergebnisse des Abonnements ab.</span><span class="sxs-lookup"><span data-stu-id="e0cf1-110">Gets security assessment and their results on subscription.</span></span> <span data-ttu-id="e0cf1-111">Mithilfe von Sicherheitsbewertungen können Sie wissen, welche bewährten Methoden vom Azure Security Center für Ihr Azure-Abonnement verringert werden.</span><span class="sxs-lookup"><span data-stu-id="e0cf1-111">Security assessments will let you know which best practices are recommanded by Azure Security Center to be mitigated on your Azure subscription.</span></span>

## <span data-ttu-id="e0cf1-112">Beispiele</span><span class="sxs-lookup"><span data-stu-id="e0cf1-112">EXAMPLES</span></span>

### <span data-ttu-id="e0cf1-113">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="e0cf1-113">Example 1</span></span>
```powershell
PS C:\> Get-AzSecurityAssessment
```

<span data-ttu-id="e0cf1-114">Ruft alle Sicherheitsbewertungen in einem Abonnement ab.</span><span class="sxs-lookup"><span data-stu-id="e0cf1-114">Gets all the security assessment in a subscription</span></span>

## <span data-ttu-id="e0cf1-115">Parameter</span><span class="sxs-lookup"><span data-stu-id="e0cf1-115">PARAMETERS</span></span>

### <span data-ttu-id="e0cf1-116">-AssessedResourceId</span><span class="sxs-lookup"><span data-stu-id="e0cf1-116">-AssessedResourceId</span></span>
<span data-ttu-id="e0cf1-117">Die vollständige Ressourcen-ID der Ressource, auf der die Bewertung berechnet wird.</span><span class="sxs-lookup"><span data-stu-id="e0cf1-117">Full resource ID of the resource that the assessment is calculated on.</span></span>

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

### <span data-ttu-id="e0cf1-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e0cf1-118">-DefaultProfile</span></span>
<span data-ttu-id="e0cf1-119">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="e0cf1-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e0cf1-120">-Name</span><span class="sxs-lookup"><span data-stu-id="e0cf1-120">-Name</span></span>
<span data-ttu-id="e0cf1-121">Ressourcenname</span><span class="sxs-lookup"><span data-stu-id="e0cf1-121">Resource name.</span></span>

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

### <span data-ttu-id="e0cf1-122">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="e0cf1-122">-ResourceId</span></span>
<span data-ttu-id="e0cf1-123">Die ID der Sicherheitsressource, auf der Sie den Befehl aufrufen möchten.</span><span class="sxs-lookup"><span data-stu-id="e0cf1-123">ID of the security resource that you want to invoke the command on.</span></span>

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

### <span data-ttu-id="e0cf1-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e0cf1-124">CommonParameters</span></span>
<span data-ttu-id="e0cf1-125">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e0cf1-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e0cf1-126">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="e0cf1-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e0cf1-127">Eingaben</span><span class="sxs-lookup"><span data-stu-id="e0cf1-127">INPUTS</span></span>

### <span data-ttu-id="e0cf1-128">System. String</span><span class="sxs-lookup"><span data-stu-id="e0cf1-128">System.String</span></span>

## <span data-ttu-id="e0cf1-129">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="e0cf1-129">OUTPUTS</span></span>

### <span data-ttu-id="e0cf1-130">Microsoft. Azure. Commands. Security. Models. Assessments. PSSecurityAssessment</span><span class="sxs-lookup"><span data-stu-id="e0cf1-130">Microsoft.Azure.Commands.Security.Models.Assessments.PSSecurityAssessment</span></span>

## <span data-ttu-id="e0cf1-131">Notizen</span><span class="sxs-lookup"><span data-stu-id="e0cf1-131">NOTES</span></span>

## <span data-ttu-id="e0cf1-132">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="e0cf1-132">RELATED LINKS</span></span>
