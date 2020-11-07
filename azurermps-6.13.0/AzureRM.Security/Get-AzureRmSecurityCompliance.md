---
external help file: Microsoft.Azure.Commands.SecurityCenter.dll-Help.xml
Module Name: AzureRM.Security
online version: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Security/Commands.Security/help/Get-AzureRmSecurityCompliance.md
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Security/Commands.Security/help/Get-AzureRmSecurityCompliance.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Security/Commands.Security/help/Get-AzureRmSecurityCompliance.md
ms.openlocfilehash: 1a1aa0675637bd5bbe8a8b0d4007ab426aba6592
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93662656"
---
# <span data-ttu-id="59bf2-101">Get-AzureRmSecurityCompliance</span><span class="sxs-lookup"><span data-stu-id="59bf2-101">Get-AzureRmSecurityCompliance</span></span>

## <span data-ttu-id="59bf2-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="59bf2-102">SYNOPSIS</span></span>
<span data-ttu-id="59bf2-103">Abrufen der Sicherheitskonformität eines Abonnements über einen Zeitraum</span><span class="sxs-lookup"><span data-stu-id="59bf2-103">Get the security compliance of a subscription over time</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="59bf2-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="59bf2-104">SYNTAX</span></span>

### <span data-ttu-id="59bf2-105">SubscriptionScope (Standard)</span><span class="sxs-lookup"><span data-stu-id="59bf2-105">SubscriptionScope (Default)</span></span>
```
Get-AzureRmSecurityCompliance [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="59bf2-106">SubscriptionLevelResource</span><span class="sxs-lookup"><span data-stu-id="59bf2-106">SubscriptionLevelResource</span></span>
```
Get-AzureRmSecurityCompliance -Name <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="59bf2-107">ResourceId</span><span class="sxs-lookup"><span data-stu-id="59bf2-107">ResourceId</span></span>
```
Get-AzureRmSecurityCompliance -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="59bf2-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="59bf2-108">DESCRIPTION</span></span>
<span data-ttu-id="59bf2-109">Ruft die Sicherheitskonformität eines Abonnements auf der Grundlage des aktuellen, gesunden und nicht gesicherten Ressourcen Verhältnisses für dieses Abonnement ab.</span><span class="sxs-lookup"><span data-stu-id="59bf2-109">Gets the security compliance of a subscription based on the current healthy and non secured resources ratio on this subscription.</span></span>
<span data-ttu-id="59bf2-110">Die Sicherheitskonformität wird täglich berechnet, und der Verlauf wird gespeichert.</span><span class="sxs-lookup"><span data-stu-id="59bf2-110">The security compliance is calculated every day and the history is saved.</span></span>

## <span data-ttu-id="59bf2-111">Beispiele</span><span class="sxs-lookup"><span data-stu-id="59bf2-111">EXAMPLES</span></span>

### <span data-ttu-id="59bf2-112">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="59bf2-112">Example 1</span></span>
```powershell
PS C:\> Get-AzureRmSecurityCompliance


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

<span data-ttu-id="59bf2-113">Ruft die Sicherheitskonformität eines Abonnements für die letzten 14 Tage ab</span><span class="sxs-lookup"><span data-stu-id="59bf2-113">Gets the security compliance of a subscription for the last 14 days</span></span>

### <span data-ttu-id="59bf2-114">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="59bf2-114">Example 2</span></span>
```powershell
PS C:\> Get-AzureRmSecurityCompliance -Name "2018-08-20Z"


Id                         : /subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/providers/Microsoft.Security/compliances/2018-08-20Z
Name                       : 2018-08-20Z
ResourceCount              : 18
AssessmentTimestampUtcDate : 20/08/2018 00:00:00
AssessmentResult           : {Microsoft.Azure.Commands.Security.Models.Compliances.PSSecurityComplianceSegment}
```

<span data-ttu-id="59bf2-115">Ruft die Sicherheitskonformität eines Abonnements an einem bestimmten Datum ab.</span><span class="sxs-lookup"><span data-stu-id="59bf2-115">Gets the security compliance of a subscription on a specific date</span></span>

## <span data-ttu-id="59bf2-116">Parameter</span><span class="sxs-lookup"><span data-stu-id="59bf2-116">PARAMETERS</span></span>

### <span data-ttu-id="59bf2-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="59bf2-117">-DefaultProfile</span></span>
<span data-ttu-id="59bf2-118">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="59bf2-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="59bf2-119">-Name</span><span class="sxs-lookup"><span data-stu-id="59bf2-119">-Name</span></span>
<span data-ttu-id="59bf2-120">Ressourcenname</span><span class="sxs-lookup"><span data-stu-id="59bf2-120">Resource name.</span></span>

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

### <span data-ttu-id="59bf2-121">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="59bf2-121">-ResourceId</span></span>
<span data-ttu-id="59bf2-122">Ressourcen-ID.</span><span class="sxs-lookup"><span data-stu-id="59bf2-122">Resource ID.</span></span>

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

### <span data-ttu-id="59bf2-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="59bf2-123">CommonParameters</span></span>
<span data-ttu-id="59bf2-124">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="59bf2-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="59bf2-125">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="59bf2-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="59bf2-126">Eingaben</span><span class="sxs-lookup"><span data-stu-id="59bf2-126">INPUTS</span></span>

### <span data-ttu-id="59bf2-127">System. String</span><span class="sxs-lookup"><span data-stu-id="59bf2-127">System.String</span></span>

## <span data-ttu-id="59bf2-128">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="59bf2-128">OUTPUTS</span></span>

### <span data-ttu-id="59bf2-129">Microsoft. Azure. Commands. Security. Models. Compliances. PSSecurityCompliance</span><span class="sxs-lookup"><span data-stu-id="59bf2-129">Microsoft.Azure.Commands.Security.Models.Compliances.PSSecurityCompliance</span></span>

## <span data-ttu-id="59bf2-130">Notizen</span><span class="sxs-lookup"><span data-stu-id="59bf2-130">NOTES</span></span>

## <span data-ttu-id="59bf2-131">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="59bf2-131">RELATED LINKS</span></span>
