---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataShare.dll-Help.xml
Module Name: Az.DataShare
online version: https://docs.microsoft.com/en-us/powershell/module/az.datashare/get-azdatasharesubscriptionsynchronization
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Get-AzDataShareSubscriptionSynchronization.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Get-AzDataShareSubscriptionSynchronization.md
ms.openlocfilehash: 62b0a959e632c3e54b07e9238ae4ea9034a7408b
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93651428"
---
# <span data-ttu-id="53b6c-101">Get-AzDataShareSubscriptionSynchronization</span><span class="sxs-lookup"><span data-stu-id="53b6c-101">Get-AzDataShareSubscriptionSynchronization</span></span>

## <span data-ttu-id="53b6c-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="53b6c-102">SYNOPSIS</span></span>
<span data-ttu-id="53b6c-103">Ruft Informationen zu Synchronisierungs Läufen im Share-Abonnement ab.</span><span class="sxs-lookup"><span data-stu-id="53b6c-103">Gets information about synchronization runs in share subscription.</span></span>

## <span data-ttu-id="53b6c-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="53b6c-104">SYNTAX</span></span>

### <span data-ttu-id="53b6c-105">ByFieldsParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="53b6c-105">ByFieldsParameterSet (Default)</span></span>
```
Get-AzDataShareSubscriptionSynchronization -ResourceGroupName <String> -AccountName <String>
 -ShareSubscriptionName <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="53b6c-106">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="53b6c-106">ByResourceIdParameterSet</span></span>
```
Get-AzDataShareSubscriptionSynchronization -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="53b6c-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="53b6c-107">DESCRIPTION</span></span>
<span data-ttu-id="53b6c-108">Das Cmdlet " **Get-AzDataShareSubscriptionSynchronization** " bietet Informaiton Informationen zu allen Synchronisierungs Läufen in einem Freigabe Abonnement unter einem Datenfreigabe Konto des Consumers.</span><span class="sxs-lookup"><span data-stu-id="53b6c-108">The **Get-AzDataShareSubscriptionSynchronization** cmdlet provides informaiton about all synchronization runs in a share subscription under a data share account on the consumer.</span></span>

## <span data-ttu-id="53b6c-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="53b6c-109">EXAMPLES</span></span>

### <span data-ttu-id="53b6c-110">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="53b6c-110">Example 1</span></span>
```
PS C:\> Get-AzDataShareSubscriptionSynchronization -ResourceGroupName "ADS" -AccountName "WikiAds"  -ShareSubscriptionName "AdsShareSubscription"

durationMs        : 83660
endTime           : 7/10/2019 9:01:23 AM
message           :
startTime         : 7/10/2019 9:00:04 AM
status            : Succeeded
synchronizationId : b087e1a5-9144-4e1d-86d1-2a4adcf551d4
```

<span data-ttu-id="53b6c-111">Dieser Befehl bietet Informationen zu allen Synchronisierungs Läufen für ein Freigabe Abonnement AdsShareSubscription unter Datenfreigabe Konto WikiAds.</span><span class="sxs-lookup"><span data-stu-id="53b6c-111">This command provides information about all the synchronization runs for a share subscription AdsShareSubscription under data share account WikiAds.</span></span>

## <span data-ttu-id="53b6c-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="53b6c-112">PARAMETERS</span></span>

### <span data-ttu-id="53b6c-113">-Kontoname</span><span class="sxs-lookup"><span data-stu-id="53b6c-113">-AccountName</span></span>
<span data-ttu-id="53b6c-114">Name des Azure-Datenfreigabe Kontos</span><span class="sxs-lookup"><span data-stu-id="53b6c-114">Azure data share account name</span></span>

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

### <span data-ttu-id="53b6c-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="53b6c-115">-DefaultProfile</span></span>
<span data-ttu-id="53b6c-116">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="53b6c-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="53b6c-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="53b6c-117">-ResourceGroupName</span></span>
<span data-ttu-id="53b6c-118">Der Name der Ressourcengruppe des Azure Data Share-Kontos</span><span class="sxs-lookup"><span data-stu-id="53b6c-118">The resource group name of the azure data share account</span></span>

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

### <span data-ttu-id="53b6c-119">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="53b6c-119">-ResourceId</span></span>
<span data-ttu-id="53b6c-120">Ressourcen-ID des Azure Data Share-Abonnements</span><span class="sxs-lookup"><span data-stu-id="53b6c-120">Azure data share subscription resource id</span></span>

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

### <span data-ttu-id="53b6c-121">-ShareSubscriptionName</span><span class="sxs-lookup"><span data-stu-id="53b6c-121">-ShareSubscriptionName</span></span>
<span data-ttu-id="53b6c-122">Name des Azure Data Share-Abonnements</span><span class="sxs-lookup"><span data-stu-id="53b6c-122">Azure data share subscription name</span></span>

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

### <span data-ttu-id="53b6c-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="53b6c-123">CommonParameters</span></span>
<span data-ttu-id="53b6c-124">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="53b6c-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="53b6c-125">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="53b6c-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="53b6c-126">Eingaben</span><span class="sxs-lookup"><span data-stu-id="53b6c-126">INPUTS</span></span>

### <span data-ttu-id="53b6c-127">System. String</span><span class="sxs-lookup"><span data-stu-id="53b6c-127">System.String</span></span>

## <span data-ttu-id="53b6c-128">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="53b6c-128">OUTPUTS</span></span>

### <span data-ttu-id="53b6c-129">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareSubscriptionSynchronization</span><span class="sxs-lookup"><span data-stu-id="53b6c-129">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareSubscriptionSynchronization</span></span>

## <span data-ttu-id="53b6c-130">Notizen</span><span class="sxs-lookup"><span data-stu-id="53b6c-130">NOTES</span></span>

## <span data-ttu-id="53b6c-131">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="53b6c-131">RELATED LINKS</span></span>
