---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataShare.dll-Help.xml
Module Name: Az.DataShare
online version: https://docs.microsoft.com/en-us/powershell/module/az.datashare/get-azdatasharesubscriptionsynchronizationdetail
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Get-AzDataShareSubscriptionSynchronizationDetail.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Get-AzDataShareSubscriptionSynchronizationDetail.md
ms.openlocfilehash: 49917b7d9719e682060c8a3cf24c30bbb9141874
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94173859"
---
# <span data-ttu-id="baae5-101">Get-AzDataShareSubscriptionSynchronizationDetail</span><span class="sxs-lookup"><span data-stu-id="baae5-101">Get-AzDataShareSubscriptionSynchronizationDetail</span></span>

## <span data-ttu-id="baae5-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="baae5-102">SYNOPSIS</span></span>
<span data-ttu-id="baae5-103">Ruft Informationen zu Synchronität-Details für das Freigabe Abonnement ab.</span><span class="sxs-lookup"><span data-stu-id="baae5-103">Gets information about synchonization details for share subscription.</span></span>

## <span data-ttu-id="baae5-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="baae5-104">SYNTAX</span></span>

### <span data-ttu-id="baae5-105">ByFieldsParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="baae5-105">ByFieldsParameterSet (Default)</span></span>
```
Get-AzDataShareSubscriptionSynchronizationDetail -ResourceGroupName <String> -AccountName <String>
 -ShareSubscriptionName <String> -SynchronizationId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="baae5-106">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="baae5-106">ByResourceIdParameterSet</span></span>
```
Get-AzDataShareSubscriptionSynchronizationDetail -SynchronizationId <String> -ResourceId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="baae5-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="baae5-107">DESCRIPTION</span></span>
<span data-ttu-id="baae5-108">Das Cmdlet " **Get-AzDataShareSubscriptionSynchronizationDetail** " enthält Details zu der für ein Freigabe Abonnement initiierten Synchronisierung.</span><span class="sxs-lookup"><span data-stu-id="baae5-108">The **Get-AzDataShareSubscriptionSynchronizationDetail** cmdlet provides details of the synchronization initiated for a share subscription.</span></span>

## <span data-ttu-id="baae5-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="baae5-109">EXAMPLES</span></span>

### <span data-ttu-id="baae5-110">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="baae5-110">Example 1</span></span>
```
PS C:\> Get-AzDataShareSubscriptionSynchronizationDetail -ResourceGroupName "ADS" -AccountName "WikiAds" -ShareSubscriptionName "AdsShareSubscription" -SynchronizationId "a6ee5c8d-0ce0-485e-b2f2-966b187dc6c7"

DataSetId    : d2411889-5357-4ca8-8d65-9363e46ef2ed
DataSetType  : BlobFolder
EndTime      : 7/8/2019 10:24:27 PM
StartTime    : 7/8/2019 10:23:09 PM
Status       : Succeeded
DurationMs   : 78870
FilesRead    : 1
FilesWritten : 1
SizeRead     : 2779935
SizeWritten  : 2779935
Name         : 16d5161b-2b3f-4d90-b074-13ad7121bcc7
Message      :
```

<span data-ttu-id="baae5-111">Dieser Befehl enthält Informationen zur Synchronisierung, die für das Freigeben von Abonnement AdsShareSubscription unter Datenfreigabe Konto WikiAds initiiert wurde.</span><span class="sxs-lookup"><span data-stu-id="baae5-111">This command provides information about synchronization initiated for share subscription AdsShareSubscription under data share account WikiAds.</span></span>

## <span data-ttu-id="baae5-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="baae5-112">PARAMETERS</span></span>

### <span data-ttu-id="baae5-113">-Kontoname</span><span class="sxs-lookup"><span data-stu-id="baae5-113">-AccountName</span></span>
<span data-ttu-id="baae5-114">Name des Azure-Datenfreigabe Kontos</span><span class="sxs-lookup"><span data-stu-id="baae5-114">Azure data share account name</span></span>

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

### <span data-ttu-id="baae5-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="baae5-115">-DefaultProfile</span></span>
<span data-ttu-id="baae5-116">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="baae5-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="baae5-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="baae5-117">-ResourceGroupName</span></span>
<span data-ttu-id="baae5-118">Der Name der Ressourcengruppe des Azure Data Share-Kontos</span><span class="sxs-lookup"><span data-stu-id="baae5-118">The resource group name of the azure data share account</span></span>

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

### <span data-ttu-id="baae5-119">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="baae5-119">-ResourceId</span></span>
<span data-ttu-id="baae5-120">Ressourcen-ID des Azure Data Share-Abonnements</span><span class="sxs-lookup"><span data-stu-id="baae5-120">Azure data share subscription resource id</span></span>

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

### <span data-ttu-id="baae5-121">-ShareSubscriptionName</span><span class="sxs-lookup"><span data-stu-id="baae5-121">-ShareSubscriptionName</span></span>
<span data-ttu-id="baae5-122">Name des Azure Data Share-Abonnements</span><span class="sxs-lookup"><span data-stu-id="baae5-122">Azure data share subscription name</span></span>

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

### <span data-ttu-id="baae5-123">-Synchronisierungs-Nr</span><span class="sxs-lookup"><span data-stu-id="baae5-123">-SynchronizationId</span></span>
<span data-ttu-id="baae5-124">Synchronisierungs-ID der Freigabe Abonnementsynchronisierung</span><span class="sxs-lookup"><span data-stu-id="baae5-124">Synchronization id of share subscription synchronization</span></span>

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

### <span data-ttu-id="baae5-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="baae5-125">CommonParameters</span></span>
<span data-ttu-id="baae5-126">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="baae5-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="baae5-127">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="baae5-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="baae5-128">Eingaben</span><span class="sxs-lookup"><span data-stu-id="baae5-128">INPUTS</span></span>

### <span data-ttu-id="baae5-129">System. String</span><span class="sxs-lookup"><span data-stu-id="baae5-129">System.String</span></span>

## <span data-ttu-id="baae5-130">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="baae5-130">OUTPUTS</span></span>

### <span data-ttu-id="baae5-131">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareSynchronizationDetail</span><span class="sxs-lookup"><span data-stu-id="baae5-131">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareSynchronizationDetail</span></span>

## <span data-ttu-id="baae5-132">Notizen</span><span class="sxs-lookup"><span data-stu-id="baae5-132">NOTES</span></span>

## <span data-ttu-id="baae5-133">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="baae5-133">RELATED LINKS</span></span>
