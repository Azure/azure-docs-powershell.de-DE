---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/en-us/powershell/module/az.security/New-AzIotSecuritySolutionRecommendationConfigurationObject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/New-AzIotSecuritySolutionRecommendationConfigurationObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/New-AzIotSecuritySolutionRecommendationConfigurationObject.md
ms.openlocfilehash: 448b72ce068c29e357db69abb45420157c3c1bf0
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94176400"
---
# <span data-ttu-id="2606a-101">New-AzIotSecuritySolutionRecommendationConfigurationObject</span><span class="sxs-lookup"><span data-stu-id="2606a-101">New-AzIotSecuritySolutionRecommendationConfigurationObject</span></span>

## <span data-ttu-id="2606a-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="2606a-102">SYNOPSIS</span></span>
<span data-ttu-id="2606a-103">Erstellen einer neuen Empfehlungs Konfiguration für viel Sicherheitslösung</span><span class="sxs-lookup"><span data-stu-id="2606a-103">Create new recommendation configuration for iot security solution</span></span>

## <span data-ttu-id="2606a-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="2606a-104">SYNTAX</span></span>

```
New-AzIotSecuritySolutionRecommendationConfigurationObject -RecommendationType <String> -Enabled <Boolean>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="2606a-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="2606a-105">DESCRIPTION</span></span>
<span data-ttu-id="2606a-106">Das AzIotSecuritySolutionRecommendationConfigurationObject erstellt ein neues Empfehlungs Konfigurationsobjekt für eine viel Sicherheitslösung.</span><span class="sxs-lookup"><span data-stu-id="2606a-106">The AzIotSecuritySolutionRecommendationConfigurationObject creates a new recommendation configuration object for iot security solution.</span></span>
<span data-ttu-id="2606a-107">Auf diese Weise wird der Status einer Empfehlung konfiguriert, unabhängig davon, ob Sie aktiviert oder deaktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="2606a-107">This way the status of a recommendation is configured, whether it is enabled or disabled.</span></span>

## <span data-ttu-id="2606a-108">Beispiele</span><span class="sxs-lookup"><span data-stu-id="2606a-108">EXAMPLES</span></span>

### <span data-ttu-id="2606a-109">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="2606a-109">Example 1</span></span>
```powershell
PS C:\> New-AzIotSecuritySolutionRecommendationConfigurationObject -RecommendationType "IoT_ACRAuthentication" -Enabled $false

RecommendationType: "IoT_ACRAuthentication"
Name: "Service prinicpal not used with ACR repository"
Status: "Disabled"
```

<span data-ttu-id="2606a-110">Neue Empfehlungs Konfiguration für den empfehlungstyp "IoT_ACRAuthentication" erstellen, wobei der Status auf "deaktivieren" gesetzt ist</span><span class="sxs-lookup"><span data-stu-id="2606a-110">Create new recommendation configuration for recommendation type "IoT_ACRAuthentication" with status set to disable</span></span>

## <span data-ttu-id="2606a-111">Parameter</span><span class="sxs-lookup"><span data-stu-id="2606a-111">PARAMETERS</span></span>

### <span data-ttu-id="2606a-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2606a-112">-DefaultProfile</span></span>
<span data-ttu-id="2606a-113">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="2606a-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2606a-114">-Aktiviert</span><span class="sxs-lookup"><span data-stu-id="2606a-114">-Enabled</span></span>
<span data-ttu-id="2606a-115">Status.</span><span class="sxs-lookup"><span data-stu-id="2606a-115">Status .</span></span>

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

### <span data-ttu-id="2606a-116">-Recommendation</span><span class="sxs-lookup"><span data-stu-id="2606a-116">-RecommendationType</span></span>
<span data-ttu-id="2606a-117">Recommendation-Typ.</span><span class="sxs-lookup"><span data-stu-id="2606a-117">Recommendation type.</span></span>

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

### <span data-ttu-id="2606a-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2606a-118">CommonParameters</span></span>
<span data-ttu-id="2606a-119">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2606a-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2606a-120">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="2606a-120">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2606a-121">Eingaben</span><span class="sxs-lookup"><span data-stu-id="2606a-121">INPUTS</span></span>

### <span data-ttu-id="2606a-122">Keine</span><span class="sxs-lookup"><span data-stu-id="2606a-122">None</span></span>

## <span data-ttu-id="2606a-123">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="2606a-123">OUTPUTS</span></span>

### <span data-ttu-id="2606a-124">Microsoft. Azure. Commands. Security. Models. IotSecuritySolutions. PSRecommendationConfiguration</span><span class="sxs-lookup"><span data-stu-id="2606a-124">Microsoft.Azure.Commands.Security.Models.IotSecuritySolutions.PSRecommendationConfiguration</span></span>

## <span data-ttu-id="2606a-125">Notizen</span><span class="sxs-lookup"><span data-stu-id="2606a-125">NOTES</span></span>

## <span data-ttu-id="2606a-126">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="2606a-126">RELATED LINKS</span></span>
