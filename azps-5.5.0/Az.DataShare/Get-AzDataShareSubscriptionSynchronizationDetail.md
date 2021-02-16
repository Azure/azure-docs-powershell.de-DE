---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataShare.dll-Help.xml
Module Name: Az.DataShare
online version: https://docs.microsoft.com/en-us/powershell/module/az.datashare/get-azdatasharesubscriptionsynchronizationdetail
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Get-AzDataShareSubscriptionSynchronizationDetail.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Get-AzDataShareSubscriptionSynchronizationDetail.md
ms.openlocfilehash: 49917b7d9719e682060c8a3cf24c30bbb9141874
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100161833"
---
# <span data-ttu-id="9254e-101">Get-AzDataShareSubscriptionSynchronizationDetail</span><span class="sxs-lookup"><span data-stu-id="9254e-101">Get-AzDataShareSubscriptionSynchronizationDetail</span></span>

## <span data-ttu-id="9254e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9254e-102">SYNOPSIS</span></span>
<span data-ttu-id="9254e-103">Ruft Informationen zu Synchronisierungsdetails für ein Freigabeabonnement ab.</span><span class="sxs-lookup"><span data-stu-id="9254e-103">Gets information about synchonization details for share subscription.</span></span>

## <span data-ttu-id="9254e-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="9254e-104">SYNTAX</span></span>

### <span data-ttu-id="9254e-105">ByFieldsParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="9254e-105">ByFieldsParameterSet (Default)</span></span>
```
Get-AzDataShareSubscriptionSynchronizationDetail -ResourceGroupName <String> -AccountName <String>
 -ShareSubscriptionName <String> -SynchronizationId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="9254e-106">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="9254e-106">ByResourceIdParameterSet</span></span>
```
Get-AzDataShareSubscriptionSynchronizationDetail -SynchronizationId <String> -ResourceId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="9254e-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="9254e-107">DESCRIPTION</span></span>
<span data-ttu-id="9254e-108">Das **Cmdlet "Get-AzDataShareSubscriptionSynchronizationDetail"** enthält Details zur Synchronisierung, die für ein Freigabeabonnement initiiert wurde.</span><span class="sxs-lookup"><span data-stu-id="9254e-108">The **Get-AzDataShareSubscriptionSynchronizationDetail** cmdlet provides details of the synchronization initiated for a share subscription.</span></span>

## <span data-ttu-id="9254e-109">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="9254e-109">EXAMPLES</span></span>

### <span data-ttu-id="9254e-110">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="9254e-110">Example 1</span></span>
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

<span data-ttu-id="9254e-111">Dieser Befehl enthält Informationen über die für ein Freigabeabonnement initiierte AdsShareSubscription unter "WikiAds" des Datenfreigabekontos.</span><span class="sxs-lookup"><span data-stu-id="9254e-111">This command provides information about synchronization initiated for share subscription AdsShareSubscription under data share account WikiAds.</span></span>

## <span data-ttu-id="9254e-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="9254e-112">PARAMETERS</span></span>

### <span data-ttu-id="9254e-113">-AccountName</span><span class="sxs-lookup"><span data-stu-id="9254e-113">-AccountName</span></span>
<span data-ttu-id="9254e-114">Name des Azure-Datenfreigabekontos</span><span class="sxs-lookup"><span data-stu-id="9254e-114">Azure data share account name</span></span>

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

### <span data-ttu-id="9254e-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9254e-115">-DefaultProfile</span></span>
<span data-ttu-id="9254e-116">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="9254e-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9254e-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9254e-117">-ResourceGroupName</span></span>
<span data-ttu-id="9254e-118">Der Ressourcengruppenname des Azure Data Share-Kontos</span><span class="sxs-lookup"><span data-stu-id="9254e-118">The resource group name of the azure data share account</span></span>

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

### <span data-ttu-id="9254e-119">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="9254e-119">-ResourceId</span></span>
<span data-ttu-id="9254e-120">Ressourcen-ID des Azure-Datenfreigabeabonnements</span><span class="sxs-lookup"><span data-stu-id="9254e-120">Azure data share subscription resource id</span></span>

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

### <span data-ttu-id="9254e-121">-ShareSubscriptionName</span><span class="sxs-lookup"><span data-stu-id="9254e-121">-ShareSubscriptionName</span></span>
<span data-ttu-id="9254e-122">Name des Azure Data Share-Abonnements</span><span class="sxs-lookup"><span data-stu-id="9254e-122">Azure data share subscription name</span></span>

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

### <span data-ttu-id="9254e-123">-SynchronizationId</span><span class="sxs-lookup"><span data-stu-id="9254e-123">-SynchronizationId</span></span>
<span data-ttu-id="9254e-124">Synchronisierungs-ID der Synchronisierung des Freigabeabonnements</span><span class="sxs-lookup"><span data-stu-id="9254e-124">Synchronization id of share subscription synchronization</span></span>

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

### <span data-ttu-id="9254e-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9254e-125">CommonParameters</span></span>
<span data-ttu-id="9254e-126">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9254e-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9254e-127">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="9254e-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9254e-128">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="9254e-128">INPUTS</span></span>

### <span data-ttu-id="9254e-129">System.String</span><span class="sxs-lookup"><span data-stu-id="9254e-129">System.String</span></span>

## <span data-ttu-id="9254e-130">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="9254e-130">OUTPUTS</span></span>

### <span data-ttu-id="9254e-131">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareSynchronizationDetail</span><span class="sxs-lookup"><span data-stu-id="9254e-131">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareSynchronizationDetail</span></span>

## <span data-ttu-id="9254e-132">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="9254e-132">NOTES</span></span>

## <span data-ttu-id="9254e-133">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="9254e-133">RELATED LINKS</span></span>
