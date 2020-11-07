---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataShare.dll-Help.xml
Module Name: Az.DataShare
online version: https://docs.microsoft.com/en-us/powershell/module/az.datashare/get-azdatasharesubscriptionsynchronization
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Get-AzDataShareSubscriptionSynchronization.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Get-AzDataShareSubscriptionSynchronization.md
ms.openlocfilehash: 4ca33a2bf665923d81257c63f123913af0b8029a
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/21/2020
ms.locfileid: "93846296"
---
# <span data-ttu-id="905e1-101">Get-AzDataShareSubscriptionSynchronization</span><span class="sxs-lookup"><span data-stu-id="905e1-101">Get-AzDataShareSubscriptionSynchronization</span></span>

## <span data-ttu-id="905e1-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="905e1-102">SYNOPSIS</span></span>
<span data-ttu-id="905e1-103">Ruft Informationen zu Synchronisierungs Läufen im Share-Abonnement ab.</span><span class="sxs-lookup"><span data-stu-id="905e1-103">Gets information about synchronization runs in share subscription.</span></span>

## <span data-ttu-id="905e1-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="905e1-104">SYNTAX</span></span>

### <span data-ttu-id="905e1-105">ByFieldsParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="905e1-105">ByFieldsParameterSet (Default)</span></span>
```
Get-AzDataShareSubscriptionSynchronization -ResourceGroupName <String> -AccountName <String>
 -ShareSubscriptionName <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="905e1-106">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="905e1-106">ByResourceIdParameterSet</span></span>
```
Get-AzDataShareSubscriptionSynchronization -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="905e1-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="905e1-107">DESCRIPTION</span></span>
<span data-ttu-id="905e1-108">Das Cmdlet " **Get-AzDataShareSubscriptionSynchronization** " bietet Informaiton Informationen zu allen Synchronisierungs Läufen in einem Freigabe Abonnement unter einem Datenfreigabe Konto des Consumers.</span><span class="sxs-lookup"><span data-stu-id="905e1-108">The **Get-AzDataShareSubscriptionSynchronization** cmdlet provides informaiton about all synchronization runs in a share subscription under a data share account on the consumer.</span></span>

## <span data-ttu-id="905e1-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="905e1-109">EXAMPLES</span></span>

### <span data-ttu-id="905e1-110">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="905e1-110">Example 1</span></span>
```
PS C:\> Get-AzDataShareSubscriptionSynchronization -ResourceGroupName "ADS" -AccountName "WikiAds"  -ShareSubscriptionName "AdsShareSubscription"

durationMs        : 83660
endTime           : 7/10/2019 9:01:23 AM
message           :
startTime         : 7/10/2019 9:00:04 AM
status            : Succeeded
synchronizationId : b087e1a5-9144-4e1d-86d1-2a4adcf551d4
```

<span data-ttu-id="905e1-111">Dieser Befehl bietet Informationen zu allen Synchronisierungs Läufen für ein Freigabe Abonnement AdsShareSubscription unter Datenfreigabe Konto WikiAds.</span><span class="sxs-lookup"><span data-stu-id="905e1-111">This command provides information about all the synchronization runs for a share subscription AdsShareSubscription under data share account WikiAds.</span></span>

## <span data-ttu-id="905e1-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="905e1-112">PARAMETERS</span></span>

### <span data-ttu-id="905e1-113">-Kontoname</span><span class="sxs-lookup"><span data-stu-id="905e1-113">-AccountName</span></span>
<span data-ttu-id="905e1-114">Name des Azure-Datenfreigabe Kontos</span><span class="sxs-lookup"><span data-stu-id="905e1-114">Azure data share account name</span></span>

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

### <span data-ttu-id="905e1-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="905e1-115">-DefaultProfile</span></span>
<span data-ttu-id="905e1-116">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="905e1-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="905e1-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="905e1-117">-ResourceGroupName</span></span>
<span data-ttu-id="905e1-118">Der Name der Ressourcengruppe des Azure Data Share-Kontos</span><span class="sxs-lookup"><span data-stu-id="905e1-118">The resource group name of the azure data share account</span></span>

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

### <span data-ttu-id="905e1-119">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="905e1-119">-ResourceId</span></span>
<span data-ttu-id="905e1-120">Ressourcen-ID des Azure Data Share-Abonnements</span><span class="sxs-lookup"><span data-stu-id="905e1-120">Azure data share subscription resource id</span></span>

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

### <span data-ttu-id="905e1-121">-ShareSubscriptionName</span><span class="sxs-lookup"><span data-stu-id="905e1-121">-ShareSubscriptionName</span></span>
<span data-ttu-id="905e1-122">Name des Azure Data Share-Abonnements</span><span class="sxs-lookup"><span data-stu-id="905e1-122">Azure data share subscription name</span></span>

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

### <span data-ttu-id="905e1-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="905e1-123">CommonParameters</span></span>
<span data-ttu-id="905e1-124">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="905e1-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="905e1-125">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="905e1-125">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="905e1-126">Eingaben</span><span class="sxs-lookup"><span data-stu-id="905e1-126">INPUTS</span></span>

### <span data-ttu-id="905e1-127">System. String</span><span class="sxs-lookup"><span data-stu-id="905e1-127">System.String</span></span>

## <span data-ttu-id="905e1-128">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="905e1-128">OUTPUTS</span></span>

### <span data-ttu-id="905e1-129">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareSubscriptionSynchronization</span><span class="sxs-lookup"><span data-stu-id="905e1-129">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareSubscriptionSynchronization</span></span>

## <span data-ttu-id="905e1-130">Notizen</span><span class="sxs-lookup"><span data-stu-id="905e1-130">NOTES</span></span>

## <span data-ttu-id="905e1-131">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="905e1-131">RELATED LINKS</span></span>
