---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/en-us/powershell/module/az.security/Get-AzSecurityAssessmentMetadata
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzSecurityAssessmentMetadata.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzSecurityAssessmentMetadata.md
ms.openlocfilehash: 6b2819041b9fd136ee1ecc65b9d8b36132af5317
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94008963"
---
# <span data-ttu-id="8f6d5-101">Get-AzSecurityAssessmentMetadata</span><span class="sxs-lookup"><span data-stu-id="8f6d5-101">Get-AzSecurityAssessmentMetadata</span></span>

## <span data-ttu-id="8f6d5-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="8f6d5-102">SYNOPSIS</span></span>
<span data-ttu-id="8f6d5-103">Ruft Typen von Sicherheitsbewertungen und metadta in einem Abonnement ab.</span><span class="sxs-lookup"><span data-stu-id="8f6d5-103">Gets security assessments types and metadta in a subscription.</span></span>

## <span data-ttu-id="8f6d5-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="8f6d5-104">SYNTAX</span></span>

### <span data-ttu-id="8f6d5-105">SubscriptionScope (Standard)</span><span class="sxs-lookup"><span data-stu-id="8f6d5-105">SubscriptionScope (Default)</span></span>
```
Get-AzSecurityAssessmentMetadata [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="8f6d5-106">SubscriptionLevelResource</span><span class="sxs-lookup"><span data-stu-id="8f6d5-106">SubscriptionLevelResource</span></span>
```
Get-AzSecurityAssessmentMetadata -Name <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="8f6d5-107">ResourceId</span><span class="sxs-lookup"><span data-stu-id="8f6d5-107">ResourceId</span></span>
```
Get-AzSecurityAssessmentMetadata -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="8f6d5-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="8f6d5-108">DESCRIPTION</span></span>
<span data-ttu-id="8f6d5-109">Ruft Typen von Sicherheitsbewertungen und metadta in einem Abonnement ab.</span><span class="sxs-lookup"><span data-stu-id="8f6d5-109">Gets security assessments types and metadta in a subscription.</span></span> <span data-ttu-id="8f6d5-110">Zu den Metadaten für die Sicherheitsbewertung gehören Built-In Bewertungen und benutzerdefinierte Bewertungstypen, die vom benutzerdefiniert werden können.</span><span class="sxs-lookup"><span data-stu-id="8f6d5-110">Security Assessment metadata include Built-In assessments and custom assessment types that the user can define.</span></span>

## <span data-ttu-id="8f6d5-111">Beispiele</span><span class="sxs-lookup"><span data-stu-id="8f6d5-111">EXAMPLES</span></span>

### <span data-ttu-id="8f6d5-112">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="8f6d5-112">Example 1</span></span>
```powershell
PS C:\> Get-AzSecurityAssessmentMetadata
```

<span data-ttu-id="8f6d5-113">Ruft alle integrierten Bewertungen und die benutzerdefinierten Bewertungen ab, die für das aktuelle Abonnement konfiguriert wurden.</span><span class="sxs-lookup"><span data-stu-id="8f6d5-113">Gets all the built in assessments and the custom assessments that were configured on the current subscription.</span></span>

## <span data-ttu-id="8f6d5-114">Parameter</span><span class="sxs-lookup"><span data-stu-id="8f6d5-114">PARAMETERS</span></span>

### <span data-ttu-id="8f6d5-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8f6d5-115">-DefaultProfile</span></span>
<span data-ttu-id="8f6d5-116">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="8f6d5-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8f6d5-117">-Name</span><span class="sxs-lookup"><span data-stu-id="8f6d5-117">-Name</span></span>
<span data-ttu-id="8f6d5-118">Ressourcenname</span><span class="sxs-lookup"><span data-stu-id="8f6d5-118">Resource name.</span></span>

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

### <span data-ttu-id="8f6d5-119">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="8f6d5-119">-ResourceId</span></span>
<span data-ttu-id="8f6d5-120">Die ID der Sicherheitsressource, auf der Sie den Befehl aufrufen möchten.</span><span class="sxs-lookup"><span data-stu-id="8f6d5-120">ID of the security resource that you want to invoke the command on.</span></span>

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

### <span data-ttu-id="8f6d5-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8f6d5-121">CommonParameters</span></span>
<span data-ttu-id="8f6d5-122">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8f6d5-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8f6d5-123">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="8f6d5-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8f6d5-124">Eingaben</span><span class="sxs-lookup"><span data-stu-id="8f6d5-124">INPUTS</span></span>

### <span data-ttu-id="8f6d5-125">System. String</span><span class="sxs-lookup"><span data-stu-id="8f6d5-125">System.String</span></span>

## <span data-ttu-id="8f6d5-126">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="8f6d5-126">OUTPUTS</span></span>

### <span data-ttu-id="8f6d5-127">Microsoft. Azure. Commands. Security. Models. AssessmentMetadata. PSSecurityAssessmentMetadata</span><span class="sxs-lookup"><span data-stu-id="8f6d5-127">Microsoft.Azure.Commands.Security.Models.AssessmentMetadata.PSSecurityAssessmentMetadata</span></span>

## <span data-ttu-id="8f6d5-128">Notizen</span><span class="sxs-lookup"><span data-stu-id="8f6d5-128">NOTES</span></span>

## <span data-ttu-id="8f6d5-129">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="8f6d5-129">RELATED LINKS</span></span>
