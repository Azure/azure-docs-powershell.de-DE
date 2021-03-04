---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataShare.dll-Help.xml
Module Name: Az.DataShare
online version: https://docs.microsoft.com/powershell/module/az.datashare/get-azdatasharetrigger
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Get-AzDataShareTrigger.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Get-AzDataShareTrigger.md
ms.openlocfilehash: 430f31a0e44f226584d06a341971ed206a2bf5d2
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101946127"
---
# <span data-ttu-id="d16b3-101">Get-AzDataShareTrigger</span><span class="sxs-lookup"><span data-stu-id="d16b3-101">Get-AzDataShareTrigger</span></span>

## <span data-ttu-id="d16b3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d16b3-102">SYNOPSIS</span></span>
<span data-ttu-id="d16b3-103">Ruft Informationen zu einem Trigger im Freigabeabonnement ab.</span><span class="sxs-lookup"><span data-stu-id="d16b3-103">Gets information about a trigger in share subscription.</span></span>

## <span data-ttu-id="d16b3-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="d16b3-104">SYNTAX</span></span>

### <span data-ttu-id="d16b3-105">ByFieldsParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="d16b3-105">ByFieldsParameterSet (Default)</span></span>
```
Get-AzDataShareTrigger -ResourceGroupName <String> -AccountName <String> -ShareSubscriptionName <String>
 [-Name <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d16b3-106">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="d16b3-106">ByResourceIdParameterSet</span></span>
```
Get-AzDataShareTrigger -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d16b3-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="d16b3-107">DESCRIPTION</span></span>
<span data-ttu-id="d16b3-108">Das **Get-AzDataShareTrigger-Cmdlet** ruft Informationen zum Trigger für ein Freigabeabonnement unter dem Datenfreigabekonto ab.</span><span class="sxs-lookup"><span data-stu-id="d16b3-108">The **Get-AzDataShareTrigger** cmdlet gets information about trigger for share subscription under data share account.</span></span>

## <span data-ttu-id="d16b3-109">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="d16b3-109">EXAMPLES</span></span>

### <span data-ttu-id="d16b3-110">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="d16b3-110">Example 1</span></span>
```
PS C:\> Get-AzDataShareTrigger -ResourceGroupName "ADS" -AccountName "WikiAds" -ShareSubscriptionName "AdsShareSubscription" -Name "AdsTrigger"

CreatedAt           : 7/10/2019 12:16:34 AM
CreatedBy           : Ads test
ProvisioningState   : Succeeded
RecurrenceInterval  : Day
SynchronizationMode : Incremental
SynchronizationTime : 7/9/2019 9:00:00 AM
TriggerStatus       : Active
Id                  : /subscriptions/1834da9b-787a-44f6-ae81-60707ab8c957/resourceGroups/ADS/providers/Microsoft.DataShare/accounts/WikiAds/shareSubscriptions/AdsShareSubscription/triggers/AdsTrigger
Name                : AdsTrigger
Type                : Microsoft.DataShare/Triggers
```

<span data-ttu-id="d16b3-111">Dieser Befehl ruft Informationen zum Trigger AdsTrigger für Das Freigabeabonnement AdsShareSubscription unter WikiAds des Datenfreigabekontos ab.</span><span class="sxs-lookup"><span data-stu-id="d16b3-111">This command gets information about trigger AdsTrigger for share subscription AdsShareSubscription under data share account WikiAds.</span></span>

## <span data-ttu-id="d16b3-112">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="d16b3-112">PARAMETERS</span></span>

### <span data-ttu-id="d16b3-113">-AccountName</span><span class="sxs-lookup"><span data-stu-id="d16b3-113">-AccountName</span></span>
<span data-ttu-id="d16b3-114">Name des Azure-Datenfreigabekontos</span><span class="sxs-lookup"><span data-stu-id="d16b3-114">Azure data share account name</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d16b3-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d16b3-115">-DefaultProfile</span></span>
<span data-ttu-id="d16b3-116">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="d16b3-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d16b3-117">-Name</span><span class="sxs-lookup"><span data-stu-id="d16b3-117">-Name</span></span>
<span data-ttu-id="d16b3-118">Name des Azure-Datenfreigabetriggers</span><span class="sxs-lookup"><span data-stu-id="d16b3-118">Azure data share trigger name</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d16b3-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d16b3-119">-ResourceGroupName</span></span>
<span data-ttu-id="d16b3-120">Der Ressourcengruppenname des Azure Data Share-Kontos</span><span class="sxs-lookup"><span data-stu-id="d16b3-120">The resource group name of the azure data share account</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d16b3-121">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="d16b3-121">-ResourceId</span></span>
<span data-ttu-id="d16b3-122">Die Ressourcen-ID des Triggers</span><span class="sxs-lookup"><span data-stu-id="d16b3-122">The resource id of the trigger</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d16b3-123">-ShareSubscriptionName</span><span class="sxs-lookup"><span data-stu-id="d16b3-123">-ShareSubscriptionName</span></span>
<span data-ttu-id="d16b3-124">Azure Data Share Subscription Name</span><span class="sxs-lookup"><span data-stu-id="d16b3-124">Azure data share subscription name</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d16b3-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d16b3-125">CommonParameters</span></span>
<span data-ttu-id="d16b3-126">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d16b3-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d16b3-127">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="d16b3-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d16b3-128">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="d16b3-128">INPUTS</span></span>

### <span data-ttu-id="d16b3-129">System.String</span><span class="sxs-lookup"><span data-stu-id="d16b3-129">System.String</span></span>

## <span data-ttu-id="d16b3-130">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="d16b3-130">OUTPUTS</span></span>

### <span data-ttu-id="d16b3-131">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareTrigger</span><span class="sxs-lookup"><span data-stu-id="d16b3-131">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareTrigger</span></span>

## <span data-ttu-id="d16b3-132">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="d16b3-132">NOTES</span></span>

## <span data-ttu-id="d16b3-133">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="d16b3-133">RELATED LINKS</span></span>
