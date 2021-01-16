---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataShare.dll-Help.xml
Module Name: Az.DataShare
online version: https://docs.microsoft.com/en-us/powershell/module/az.datashare/get-azdatasharetrigger
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Get-AzDataShareTrigger.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Get-AzDataShareTrigger.md
ms.openlocfilehash: 23554c4de23062fa44a690843232dbc6337e3c9e
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98290344"
---
# <span data-ttu-id="b806f-101">Get-AzDataShareTrigger</span><span class="sxs-lookup"><span data-stu-id="b806f-101">Get-AzDataShareTrigger</span></span>

## <span data-ttu-id="b806f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b806f-102">SYNOPSIS</span></span>
<span data-ttu-id="b806f-103">Ruft Informationen zu einem Trigger in einem Freigabeabonnement ab.</span><span class="sxs-lookup"><span data-stu-id="b806f-103">Gets information about a trigger in share subscription.</span></span>

## <span data-ttu-id="b806f-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="b806f-104">SYNTAX</span></span>

### <span data-ttu-id="b806f-105">ByFieldsParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="b806f-105">ByFieldsParameterSet (Default)</span></span>
```
Get-AzDataShareTrigger -ResourceGroupName <String> -AccountName <String> -ShareSubscriptionName <String>
 [-Name <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b806f-106">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="b806f-106">ByResourceIdParameterSet</span></span>
```
Get-AzDataShareTrigger -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b806f-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="b806f-107">DESCRIPTION</span></span>
<span data-ttu-id="b806f-108">Das **Cmdlet "Get-AzDataShareTrigger"** ruft Informationen zum Trigger für das Freigabeabonnement unter dem Datenfreigabekonto ab.</span><span class="sxs-lookup"><span data-stu-id="b806f-108">The **Get-AzDataShareTrigger** cmdlet gets information about trigger for share subscription under data share account.</span></span>

## <span data-ttu-id="b806f-109">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="b806f-109">EXAMPLES</span></span>

### <span data-ttu-id="b806f-110">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="b806f-110">Example 1</span></span>
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

<span data-ttu-id="b806f-111">Dieser Befehl ruft Informationen zum Auslöser von AdsTrigger für das Freigabeabonnement AdsShareSubscription unter "WikiAds" des Datenfreigabekontos ab.</span><span class="sxs-lookup"><span data-stu-id="b806f-111">This command gets information about trigger AdsTrigger for share subscription AdsShareSubscription under data share account WikiAds.</span></span>

## <span data-ttu-id="b806f-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="b806f-112">PARAMETERS</span></span>

### <span data-ttu-id="b806f-113">-AccountName</span><span class="sxs-lookup"><span data-stu-id="b806f-113">-AccountName</span></span>
<span data-ttu-id="b806f-114">Name des Azure-Datenfreigabekontos</span><span class="sxs-lookup"><span data-stu-id="b806f-114">Azure data share account name</span></span>

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

### <span data-ttu-id="b806f-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b806f-115">-DefaultProfile</span></span>
<span data-ttu-id="b806f-116">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="b806f-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b806f-117">-Name</span><span class="sxs-lookup"><span data-stu-id="b806f-117">-Name</span></span>
<span data-ttu-id="b806f-118">Name des Azure-Datenfreigabe-Triggers</span><span class="sxs-lookup"><span data-stu-id="b806f-118">Azure data share trigger name</span></span>

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

### <span data-ttu-id="b806f-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b806f-119">-ResourceGroupName</span></span>
<span data-ttu-id="b806f-120">Der Ressourcengruppenname des Azure Data Share-Kontos</span><span class="sxs-lookup"><span data-stu-id="b806f-120">The resource group name of the azure data share account</span></span>

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

### <span data-ttu-id="b806f-121">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="b806f-121">-ResourceId</span></span>
<span data-ttu-id="b806f-122">Die Ressourcen-ID des Triggers</span><span class="sxs-lookup"><span data-stu-id="b806f-122">The resource id of the trigger</span></span>

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

### <span data-ttu-id="b806f-123">-ShareSubscriptionName</span><span class="sxs-lookup"><span data-stu-id="b806f-123">-ShareSubscriptionName</span></span>
<span data-ttu-id="b806f-124">Name des Azure Data Share-Abonnements</span><span class="sxs-lookup"><span data-stu-id="b806f-124">Azure data share subscription name</span></span>

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

### <span data-ttu-id="b806f-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b806f-125">CommonParameters</span></span>
<span data-ttu-id="b806f-126">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b806f-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b806f-127">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="b806f-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b806f-128">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="b806f-128">INPUTS</span></span>

### <span data-ttu-id="b806f-129">System.String</span><span class="sxs-lookup"><span data-stu-id="b806f-129">System.String</span></span>

## <span data-ttu-id="b806f-130">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="b806f-130">OUTPUTS</span></span>

### <span data-ttu-id="b806f-131">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareTrigger</span><span class="sxs-lookup"><span data-stu-id="b806f-131">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareTrigger</span></span>

## <span data-ttu-id="b806f-132">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="b806f-132">NOTES</span></span>

## <span data-ttu-id="b806f-133">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="b806f-133">RELATED LINKS</span></span>
