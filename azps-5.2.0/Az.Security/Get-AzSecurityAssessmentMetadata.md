---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/en-us/powershell/module/az.security/Get-AzSecurityAssessmentMetadata
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzSecurityAssessmentMetadata.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzSecurityAssessmentMetadata.md
ms.openlocfilehash: 6b2819041b9fd136ee1ecc65b9d8b36132af5317
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98289823"
---
# <span data-ttu-id="dda98-101">Get-AzSecurityAssessmentMetadata</span><span class="sxs-lookup"><span data-stu-id="dda98-101">Get-AzSecurityAssessmentMetadata</span></span>

## <span data-ttu-id="dda98-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="dda98-102">SYNOPSIS</span></span>
<span data-ttu-id="dda98-103">Ruft Sicherheitsbewertungstypen und Metadta in einem Abonnement ab.</span><span class="sxs-lookup"><span data-stu-id="dda98-103">Gets security assessments types and metadta in a subscription.</span></span>

## <span data-ttu-id="dda98-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="dda98-104">SYNTAX</span></span>

### <span data-ttu-id="dda98-105">SubscriptionScope (Standard)</span><span class="sxs-lookup"><span data-stu-id="dda98-105">SubscriptionScope (Default)</span></span>
```
Get-AzSecurityAssessmentMetadata [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="dda98-106">SubscriptionLevelResource</span><span class="sxs-lookup"><span data-stu-id="dda98-106">SubscriptionLevelResource</span></span>
```
Get-AzSecurityAssessmentMetadata -Name <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="dda98-107">ResourceId</span><span class="sxs-lookup"><span data-stu-id="dda98-107">ResourceId</span></span>
```
Get-AzSecurityAssessmentMetadata -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="dda98-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="dda98-108">DESCRIPTION</span></span>
<span data-ttu-id="dda98-109">Ruft Sicherheitsbewertungstypen und Metadta in einem Abonnement ab.</span><span class="sxs-lookup"><span data-stu-id="dda98-109">Gets security assessments types and metadta in a subscription.</span></span> <span data-ttu-id="dda98-110">Die Metadaten zur Sicherheitsbewertung umfassen Built-In Bewertungen und benutzerdefinierte Bewertungstypen, die der Benutzer definieren kann.</span><span class="sxs-lookup"><span data-stu-id="dda98-110">Security Assessment metadata include Built-In assessments and custom assessment types that the user can define.</span></span>

## <span data-ttu-id="dda98-111">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="dda98-111">EXAMPLES</span></span>

### <span data-ttu-id="dda98-112">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="dda98-112">Example 1</span></span>
```powershell
PS C:\> Get-AzSecurityAssessmentMetadata
```

<span data-ttu-id="dda98-113">Ruft alle integrierten Bewertungen und die benutzerdefinierten Bewertungen ab, die im aktuellen Abonnement konfiguriert wurden.</span><span class="sxs-lookup"><span data-stu-id="dda98-113">Gets all the built in assessments and the custom assessments that were configured on the current subscription.</span></span>

## <span data-ttu-id="dda98-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="dda98-114">PARAMETERS</span></span>

### <span data-ttu-id="dda98-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dda98-115">-DefaultProfile</span></span>
<span data-ttu-id="dda98-116">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="dda98-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="dda98-117">-Name</span><span class="sxs-lookup"><span data-stu-id="dda98-117">-Name</span></span>
<span data-ttu-id="dda98-118">Ressourcenname.</span><span class="sxs-lookup"><span data-stu-id="dda98-118">Resource name.</span></span>

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

### <span data-ttu-id="dda98-119">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="dda98-119">-ResourceId</span></span>
<span data-ttu-id="dda98-120">DIE ID der Sicherheitsressource, für die Sie den Befehl aufrufen möchten.</span><span class="sxs-lookup"><span data-stu-id="dda98-120">ID of the security resource that you want to invoke the command on.</span></span>

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

### <span data-ttu-id="dda98-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dda98-121">CommonParameters</span></span>
<span data-ttu-id="dda98-122">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="dda98-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dda98-123">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="dda98-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dda98-124">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="dda98-124">INPUTS</span></span>

### <span data-ttu-id="dda98-125">System.String</span><span class="sxs-lookup"><span data-stu-id="dda98-125">System.String</span></span>

## <span data-ttu-id="dda98-126">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="dda98-126">OUTPUTS</span></span>

### <span data-ttu-id="dda98-127">Microsoft.Azure.Commands.Security.Models.AssessmentMetadata.PSSecurityAssessmentMetadata</span><span class="sxs-lookup"><span data-stu-id="dda98-127">Microsoft.Azure.Commands.Security.Models.AssessmentMetadata.PSSecurityAssessmentMetadata</span></span>

## <span data-ttu-id="dda98-128">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="dda98-128">NOTES</span></span>

## <span data-ttu-id="dda98-129">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="dda98-129">RELATED LINKS</span></span>
