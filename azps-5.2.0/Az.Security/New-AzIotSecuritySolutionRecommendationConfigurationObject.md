---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/en-us/powershell/module/az.security/New-AzIotSecuritySolutionRecommendationConfigurationObject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/New-AzIotSecuritySolutionRecommendationConfigurationObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/New-AzIotSecuritySolutionRecommendationConfigurationObject.md
ms.openlocfilehash: 448b72ce068c29e357db69abb45420157c3c1bf0
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98296410"
---
# <span data-ttu-id="d5a83-101">New-AzIotSecuritySolutionRecommendationConfigurationObject</span><span class="sxs-lookup"><span data-stu-id="d5a83-101">New-AzIotSecuritySolutionRecommendationConfigurationObject</span></span>

## <span data-ttu-id="d5a83-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d5a83-102">SYNOPSIS</span></span>
<span data-ttu-id="d5a83-103">Erstellen einer neuen Empfehlungskonfiguration für die iot-Sicherheitslösung</span><span class="sxs-lookup"><span data-stu-id="d5a83-103">Create new recommendation configuration for iot security solution</span></span>

## <span data-ttu-id="d5a83-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="d5a83-104">SYNTAX</span></span>

```
New-AzIotSecuritySolutionRecommendationConfigurationObject -RecommendationType <String> -Enabled <Boolean>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d5a83-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="d5a83-105">DESCRIPTION</span></span>
<span data-ttu-id="d5a83-106">AzIotSecuritySolutionRecommendationConfigurationObject erstellt ein neues Empfehlungskonfigurationsobjekt für die iot-Sicherheitslösung.</span><span class="sxs-lookup"><span data-stu-id="d5a83-106">The AzIotSecuritySolutionRecommendationConfigurationObject creates a new recommendation configuration object for iot security solution.</span></span>
<span data-ttu-id="d5a83-107">Auf diese Weise wird der Status einer Empfehlung konfiguriert, unabhängig davon, ob sie aktiviert oder deaktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="d5a83-107">This way the status of a recommendation is configured, whether it is enabled or disabled.</span></span>

## <span data-ttu-id="d5a83-108">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="d5a83-108">EXAMPLES</span></span>

### <span data-ttu-id="d5a83-109">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="d5a83-109">Example 1</span></span>
```powershell
PS C:\> New-AzIotSecuritySolutionRecommendationConfigurationObject -RecommendationType "IoT_ACRAuthentication" -Enabled $false

RecommendationType: "IoT_ACRAuthentication"
Name: "Service prinicpal not used with ACR repository"
Status: "Disabled"
```

<span data-ttu-id="d5a83-110">Erstellen einer neuen Empfehlungskonfiguration für den Empfehlungstyp "IoT_ACRAuthentication" mit status set to disable</span><span class="sxs-lookup"><span data-stu-id="d5a83-110">Create new recommendation configuration for recommendation type "IoT_ACRAuthentication" with status set to disable</span></span>

## <span data-ttu-id="d5a83-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="d5a83-111">PARAMETERS</span></span>

### <span data-ttu-id="d5a83-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d5a83-112">-DefaultProfile</span></span>
<span data-ttu-id="d5a83-113">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="d5a83-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d5a83-114">-Enabled</span><span class="sxs-lookup"><span data-stu-id="d5a83-114">-Enabled</span></span>
<span data-ttu-id="d5a83-115">Status .</span><span class="sxs-lookup"><span data-stu-id="d5a83-115">Status .</span></span>

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d5a83-116">-RecommendationType</span><span class="sxs-lookup"><span data-stu-id="d5a83-116">-RecommendationType</span></span>
<span data-ttu-id="d5a83-117">Empfehlungstyp.</span><span class="sxs-lookup"><span data-stu-id="d5a83-117">Recommendation type.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d5a83-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d5a83-118">CommonParameters</span></span>
<span data-ttu-id="d5a83-119">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d5a83-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d5a83-120">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="d5a83-120">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d5a83-121">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="d5a83-121">INPUTS</span></span>

### <span data-ttu-id="d5a83-122">Keine</span><span class="sxs-lookup"><span data-stu-id="d5a83-122">None</span></span>

## <span data-ttu-id="d5a83-123">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="d5a83-123">OUTPUTS</span></span>

### <span data-ttu-id="d5a83-124">Microsoft.Azure.Commands.Security.Models.IotSecuritySolutions.PSRecommendationConfiguration</span><span class="sxs-lookup"><span data-stu-id="d5a83-124">Microsoft.Azure.Commands.Security.Models.IotSecuritySolutions.PSRecommendationConfiguration</span></span>

## <span data-ttu-id="d5a83-125">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="d5a83-125">NOTES</span></span>

## <span data-ttu-id="d5a83-126">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="d5a83-126">RELATED LINKS</span></span>
