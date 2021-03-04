---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/powershell/module/az.security/Get-AzSecurityCompliance
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzSecurityCompliance.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzSecurityCompliance.md
ms.openlocfilehash: 785cc5d27d84175621e21f56ffa263ea46b9474f
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101950619"
---
# <span data-ttu-id="dc00c-101">Get-AzSecurityCompliance</span><span class="sxs-lookup"><span data-stu-id="dc00c-101">Get-AzSecurityCompliance</span></span>

## <span data-ttu-id="dc00c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="dc00c-102">SYNOPSIS</span></span>
<span data-ttu-id="dc00c-103">Erhalten der Sicherheitskonformität eines Abonnements im Laufe der Zeit</span><span class="sxs-lookup"><span data-stu-id="dc00c-103">Get the security compliance of a subscription over time</span></span>

## <span data-ttu-id="dc00c-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="dc00c-104">SYNTAX</span></span>

### <span data-ttu-id="dc00c-105">SubscriptionScope (Standard)</span><span class="sxs-lookup"><span data-stu-id="dc00c-105">SubscriptionScope (Default)</span></span>
```
Get-AzSecurityCompliance [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="dc00c-106">SubscriptionLevelResource</span><span class="sxs-lookup"><span data-stu-id="dc00c-106">SubscriptionLevelResource</span></span>
```
Get-AzSecurityCompliance -Name <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="dc00c-107">ResourceId</span><span class="sxs-lookup"><span data-stu-id="dc00c-107">ResourceId</span></span>
```
Get-AzSecurityCompliance -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="dc00c-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="dc00c-108">DESCRIPTION</span></span>
<span data-ttu-id="dc00c-109">Ruft die Sicherheitskonformität eines Abonnements ab, die auf dem aktuellen Verhältnis gesunder und nicht gesicherter Ressourcen für dieses Abonnement basiert.</span><span class="sxs-lookup"><span data-stu-id="dc00c-109">Gets the security compliance of a subscription based on the current healthy and non secured resources ratio on this subscription.</span></span>
<span data-ttu-id="dc00c-110">Die Sicherheitskonformität wird täglich berechnet und der Verlauf gespeichert.</span><span class="sxs-lookup"><span data-stu-id="dc00c-110">The security compliance is calculated every day and the history is saved.</span></span>

## <span data-ttu-id="dc00c-111">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="dc00c-111">EXAMPLES</span></span>

### <span data-ttu-id="dc00c-112">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="dc00c-112">Example 1</span></span>
```powershell
PS C:\> Get-AzSecurityCompliance


Id                         : /subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/providers/Microsoft.Security/compliances/2018-08-20Z
Name                       : 2018-08-20Z
ResourceCount              : 18
AssessmentTimestampUtcDate : 20/08/2018 00:00:00
AssessmentResult           : {Microsoft.Azure.Commands.Security.Models.Compliances.PSSecurityComplianceSegment}

Id                         : /subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/providers/Microsoft.Security/compliances/2018-08-19Z
Name                       : 2018-08-19Z
ResourceCount              : 18
AssessmentTimestampUtcDate : 19/08/2018 00:00:00
AssessmentResult           : {Microsoft.Azure.Commands.Security.Models.Compliances.PSSecurityComplianceSegment}

Id                         : /subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/providers/Microsoft.Security/compliances/2018-08-18Z
Name                       : 2018-08-18Z
ResourceCount              : 18
AssessmentTimestampUtcDate : 18/08/2018 00:00:00
AssessmentResult           : {Microsoft.Azure.Commands.Security.Models.Compliances.PSSecurityComplianceSegment}

Id                         : /subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/providers/Microsoft.Security/compliances/2018-08-17Z
Name                       : 2018-08-17Z
ResourceCount              : 18
AssessmentTimestampUtcDate : 17/08/2018 00:00:00
AssessmentResult           : {Microsoft.Azure.Commands.Security.Models.Compliances.PSSecurityComplianceSegment}

Id                         : /subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/providers/Microsoft.Security/compliances/2018-08-16Z
Name                       : 2018-08-16Z
ResourceCount              : 18
AssessmentTimestampUtcDate : 16/08/2018 00:00:00
AssessmentResult           : {Microsoft.Azure.Commands.Security.Models.Compliances.PSSecurityComplianceSegment}

Id                         : /subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/providers/Microsoft.Security/compliances/2018-08-15Z
Name                       : 2018-08-15Z
ResourceCount              : 18
AssessmentTimestampUtcDate : 15/08/2018 00:00:00
AssessmentResult           : {Microsoft.Azure.Commands.Security.Models.Compliances.PSSecurityComplianceSegment}

Id                         : /subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/providers/Microsoft.Security/compliances/2018-08-14Z
Name                       : 2018-08-14Z
ResourceCount              : 18
AssessmentTimestampUtcDate : 14/08/2018 00:00:00
AssessmentResult           : {Microsoft.Azure.Commands.Security.Models.Compliances.PSSecurityComplianceSegment}

Id                         : /subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/providers/Microsoft.Security/compliances/2018-08-13Z
Name                       : 2018-08-13Z
ResourceCount              : 18
AssessmentTimestampUtcDate : 13/08/2018 00:00:00
AssessmentResult           : {Microsoft.Azure.Commands.Security.Models.Compliances.PSSecurityComplianceSegment}

Id                         : /subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/providers/Microsoft.Security/compliances/2018-08-12Z
Name                       : 2018-08-12Z
ResourceCount              : 18
AssessmentTimestampUtcDate : 12/08/2018 00:00:00
AssessmentResult           : {Microsoft.Azure.Commands.Security.Models.Compliances.PSSecurityComplianceSegment}

Id                         : /subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/providers/Microsoft.Security/compliances/2018-08-11Z
Name                       : 2018-08-11Z
ResourceCount              : 18
AssessmentTimestampUtcDate : 11/08/2018 00:00:00
AssessmentResult           : {Microsoft.Azure.Commands.Security.Models.Compliances.PSSecurityComplianceSegment}

Id                         : /subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/providers/Microsoft.Security/compliances/2018-08-10Z
Name                       : 2018-08-10Z
ResourceCount              : 18
AssessmentTimestampUtcDate : 10/08/2018 00:00:00
AssessmentResult           : {Microsoft.Azure.Commands.Security.Models.Compliances.PSSecurityComplianceSegment}

Id                         : /subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/providers/Microsoft.Security/compliances/2018-08-09Z
Name                       : 2018-08-09Z
ResourceCount              : 18
AssessmentTimestampUtcDate : 09/08/2018 00:00:00
AssessmentResult           : {Microsoft.Azure.Commands.Security.Models.Compliances.PSSecurityComplianceSegment}

Id                         : /subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/providers/Microsoft.Security/compliances/2018-08-08Z
Name                       : 2018-08-08Z
ResourceCount              : 18
AssessmentTimestampUtcDate : 08/08/2018 00:00:00
AssessmentResult           : {Microsoft.Azure.Commands.Security.Models.Compliances.PSSecurityComplianceSegment}

Id                         : /subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/providers/Microsoft.Security/compliances/2018-08-07Z
Name                       : 2018-08-07Z
ResourceCount              : 18
AssessmentTimestampUtcDate : 07/08/2018 00:00:00
AssessmentResult           : {Microsoft.Azure.Commands.Security.Models.Compliances.PSSecurityComplianceSegment}
```

<span data-ttu-id="dc00c-113">Ruft die Sicherheitskonformität eines Abonnements für die letzten 14 Tage ab.</span><span class="sxs-lookup"><span data-stu-id="dc00c-113">Gets the security compliance of a subscription for the last 14 days</span></span>

### <span data-ttu-id="dc00c-114">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="dc00c-114">Example 2</span></span>
```powershell
PS C:\> Get-AzSecurityCompliance -Name "2018-08-20Z"


Id                         : /subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/providers/Microsoft.Security/compliances/2018-08-20Z
Name                       : 2018-08-20Z
ResourceCount              : 18
AssessmentTimestampUtcDate : 20/08/2018 00:00:00
AssessmentResult           : {Microsoft.Azure.Commands.Security.Models.Compliances.PSSecurityComplianceSegment}
```

<span data-ttu-id="dc00c-115">Ruft die Sicherheitskonformität eines Abonnements an einem bestimmten Datum ab.</span><span class="sxs-lookup"><span data-stu-id="dc00c-115">Gets the security compliance of a subscription on a specific date</span></span>

## <span data-ttu-id="dc00c-116">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="dc00c-116">PARAMETERS</span></span>

### <span data-ttu-id="dc00c-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dc00c-117">-DefaultProfile</span></span>
<span data-ttu-id="dc00c-118">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="dc00c-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="dc00c-119">-Name</span><span class="sxs-lookup"><span data-stu-id="dc00c-119">-Name</span></span>
<span data-ttu-id="dc00c-120">Ressourcenname.</span><span class="sxs-lookup"><span data-stu-id="dc00c-120">Resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: SubscriptionLevelResource
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dc00c-121">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="dc00c-121">-ResourceId</span></span>
<span data-ttu-id="dc00c-122">Ressourcen-ID.</span><span class="sxs-lookup"><span data-stu-id="dc00c-122">Resource ID.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="dc00c-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dc00c-123">CommonParameters</span></span>
<span data-ttu-id="dc00c-124">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="dc00c-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dc00c-125">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="dc00c-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dc00c-126">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="dc00c-126">INPUTS</span></span>

### <span data-ttu-id="dc00c-127">System.String</span><span class="sxs-lookup"><span data-stu-id="dc00c-127">System.String</span></span>

## <span data-ttu-id="dc00c-128">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="dc00c-128">OUTPUTS</span></span>

### <span data-ttu-id="dc00c-129">Microsoft.Azure.Commands.Security.Models.Compliances.PSSecurityCompliance</span><span class="sxs-lookup"><span data-stu-id="dc00c-129">Microsoft.Azure.Commands.Security.Models.Compliances.PSSecurityCompliance</span></span>

## <span data-ttu-id="dc00c-130">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="dc00c-130">NOTES</span></span>

## <span data-ttu-id="dc00c-131">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="dc00c-131">RELATED LINKS</span></span>
