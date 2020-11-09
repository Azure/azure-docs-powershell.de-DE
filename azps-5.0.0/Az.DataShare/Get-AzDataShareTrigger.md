---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataShare.dll-Help.xml
Module Name: Az.DataShare
online version: https://docs.microsoft.com/en-us/powershell/module/az.datashare/get-azdatasharetrigger
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Get-AzDataShareTrigger.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Get-AzDataShareTrigger.md
ms.openlocfilehash: 23554c4de23062fa44a690843232dbc6337e3c9e
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94297477"
---
# <span data-ttu-id="331a4-101">Get-AzDataShareTrigger</span><span class="sxs-lookup"><span data-stu-id="331a4-101">Get-AzDataShareTrigger</span></span>

## <span data-ttu-id="331a4-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="331a4-102">SYNOPSIS</span></span>
<span data-ttu-id="331a4-103">Ruft Informationen zu einem Trigger im Share-Abonnement ab.</span><span class="sxs-lookup"><span data-stu-id="331a4-103">Gets information about a trigger in share subscription.</span></span>

## <span data-ttu-id="331a4-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="331a4-104">SYNTAX</span></span>

### <span data-ttu-id="331a4-105">ByFieldsParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="331a4-105">ByFieldsParameterSet (Default)</span></span>
```
Get-AzDataShareTrigger -ResourceGroupName <String> -AccountName <String> -ShareSubscriptionName <String>
 [-Name <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="331a4-106">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="331a4-106">ByResourceIdParameterSet</span></span>
```
Get-AzDataShareTrigger -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="331a4-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="331a4-107">DESCRIPTION</span></span>
<span data-ttu-id="331a4-108">Das Cmdlet " **Get-AzDataShareTrigger** " Ruft Informationen zu Trigger für das Freigabe Abonnement unter Datenfreigabe Konto ab.</span><span class="sxs-lookup"><span data-stu-id="331a4-108">The **Get-AzDataShareTrigger** cmdlet gets information about trigger for share subscription under data share account.</span></span>

## <span data-ttu-id="331a4-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="331a4-109">EXAMPLES</span></span>

### <span data-ttu-id="331a4-110">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="331a4-110">Example 1</span></span>
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

<span data-ttu-id="331a4-111">Dieser Befehl ruft Informationen zu Trigger-AdsTrigger für Freigabe Abonnement-AdsShareSubscription unter Datenfreigabe Konto WikiAds.</span><span class="sxs-lookup"><span data-stu-id="331a4-111">This command gets information about trigger AdsTrigger for share subscription AdsShareSubscription under data share account WikiAds.</span></span>

## <span data-ttu-id="331a4-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="331a4-112">PARAMETERS</span></span>

### <span data-ttu-id="331a4-113">-Kontoname</span><span class="sxs-lookup"><span data-stu-id="331a4-113">-AccountName</span></span>
<span data-ttu-id="331a4-114">Name des Azure-Datenfreigabe Kontos</span><span class="sxs-lookup"><span data-stu-id="331a4-114">Azure data share account name</span></span>

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

### <span data-ttu-id="331a4-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="331a4-115">-DefaultProfile</span></span>
<span data-ttu-id="331a4-116">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="331a4-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="331a4-117">-Name</span><span class="sxs-lookup"><span data-stu-id="331a4-117">-Name</span></span>
<span data-ttu-id="331a4-118">Name des Azure Data Freigabe-Triggers</span><span class="sxs-lookup"><span data-stu-id="331a4-118">Azure data share trigger name</span></span>

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

### <span data-ttu-id="331a4-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="331a4-119">-ResourceGroupName</span></span>
<span data-ttu-id="331a4-120">Der Name der Ressourcengruppe des Azure Data Share-Kontos</span><span class="sxs-lookup"><span data-stu-id="331a4-120">The resource group name of the azure data share account</span></span>

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

### <span data-ttu-id="331a4-121">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="331a4-121">-ResourceId</span></span>
<span data-ttu-id="331a4-122">Die Ressourcen-ID des Triggers</span><span class="sxs-lookup"><span data-stu-id="331a4-122">The resource id of the trigger</span></span>

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

### <span data-ttu-id="331a4-123">-ShareSubscriptionName</span><span class="sxs-lookup"><span data-stu-id="331a4-123">-ShareSubscriptionName</span></span>
<span data-ttu-id="331a4-124">Name des Azure Data Share-Abonnements</span><span class="sxs-lookup"><span data-stu-id="331a4-124">Azure data share subscription name</span></span>

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

### <span data-ttu-id="331a4-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="331a4-125">CommonParameters</span></span>
<span data-ttu-id="331a4-126">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="331a4-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="331a4-127">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="331a4-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="331a4-128">Eingaben</span><span class="sxs-lookup"><span data-stu-id="331a4-128">INPUTS</span></span>

### <span data-ttu-id="331a4-129">System. String</span><span class="sxs-lookup"><span data-stu-id="331a4-129">System.String</span></span>

## <span data-ttu-id="331a4-130">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="331a4-130">OUTPUTS</span></span>

### <span data-ttu-id="331a4-131">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareTrigger</span><span class="sxs-lookup"><span data-stu-id="331a4-131">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareTrigger</span></span>

## <span data-ttu-id="331a4-132">Notizen</span><span class="sxs-lookup"><span data-stu-id="331a4-132">NOTES</span></span>

## <span data-ttu-id="331a4-133">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="331a4-133">RELATED LINKS</span></span>
