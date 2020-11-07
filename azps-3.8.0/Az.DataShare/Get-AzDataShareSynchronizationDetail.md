---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataShare.dll-Help.xml
Module Name: Az.DataShare
online version: https://docs.microsoft.com/en-us/powershell/module/az.datashare/get-azdatasharesynchronizationdetail
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Get-AzDataShareSynchronizationDetail.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Get-AzDataShareSynchronizationDetail.md
ms.openlocfilehash: 8e0f62f4b3d29d0aff9a2bdfcd7916805544af14
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/21/2020
ms.locfileid: "93846288"
---
# <span data-ttu-id="b79a8-101">Get-AzDataShareSynchronizationDetail</span><span class="sxs-lookup"><span data-stu-id="b79a8-101">Get-AzDataShareSynchronizationDetail</span></span>

## <span data-ttu-id="b79a8-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="b79a8-102">SYNOPSIS</span></span>
<span data-ttu-id="b79a8-103">Ruft Informationen zu Synchronisierungs Details für eine Freigabe ab.</span><span class="sxs-lookup"><span data-stu-id="b79a8-103">Gets information about synchronization details for a share.</span></span>

## <span data-ttu-id="b79a8-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="b79a8-104">SYNTAX</span></span>

### <span data-ttu-id="b79a8-105">ByFieldsParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="b79a8-105">ByFieldsParameterSet (Default)</span></span>
```
Get-AzDataShareSynchronizationDetail -ResourceGroupName <String> -AccountName <String> -ShareName <String>
 -SynchronizationId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b79a8-106">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="b79a8-106">ByResourceIdParameterSet</span></span>
```
Get-AzDataShareSynchronizationDetail -SynchronizationId <String> -ResourceId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b79a8-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="b79a8-107">DESCRIPTION</span></span>
<span data-ttu-id="b79a8-108">Das Cmdlet " **Get-AzDataShareSynchronizationDetail** " enthält Details zu der für eine Freigabe initiierten Synchronisierung.</span><span class="sxs-lookup"><span data-stu-id="b79a8-108">The **Get-AzDataShareSynchronizationDetail** cmdlet provides details of the synchronization initiated for a share.</span></span>

## <span data-ttu-id="b79a8-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="b79a8-109">EXAMPLES</span></span>

### <span data-ttu-id="b79a8-110">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="b79a8-110">Example 1</span></span>
```
PS C:\> Get-AzDataShareSynchronizationDetail -ResourceGroupName "ADS" -AccountName "WikiAds" -ShareName "AdsShare" -SynchronizationId "02a17faa-4498-45ee-a884-162180af9251"

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

<span data-ttu-id="b79a8-111">Dieser Befehl bietet Informationen zu den Synchronisierungs Details aller Datensätze, die der bereitgestellten Synchronisierungs-ID entsprechen.</span><span class="sxs-lookup"><span data-stu-id="b79a8-111">This command provides information about the synchronization details of all the data sets corresponding to the provided synchronization id.</span></span>

## <span data-ttu-id="b79a8-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="b79a8-112">PARAMETERS</span></span>

### <span data-ttu-id="b79a8-113">-Kontoname</span><span class="sxs-lookup"><span data-stu-id="b79a8-113">-AccountName</span></span>
<span data-ttu-id="b79a8-114">Name des Azure-Datenfreigabe Kontos</span><span class="sxs-lookup"><span data-stu-id="b79a8-114">Azure data share account name</span></span>

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

### <span data-ttu-id="b79a8-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b79a8-115">-DefaultProfile</span></span>
<span data-ttu-id="b79a8-116">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="b79a8-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b79a8-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b79a8-117">-ResourceGroupName</span></span>
<span data-ttu-id="b79a8-118">Der Name der Ressourcengruppe des Azure Data Share-Kontos</span><span class="sxs-lookup"><span data-stu-id="b79a8-118">The resource group name of the azure data share account</span></span>

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

### <span data-ttu-id="b79a8-119">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="b79a8-119">-ResourceId</span></span>
<span data-ttu-id="b79a8-120">Azure Data Share-Ressourcen-ID</span><span class="sxs-lookup"><span data-stu-id="b79a8-120">Azure data share resource id</span></span>

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

### <span data-ttu-id="b79a8-121">-Freigabename</span><span class="sxs-lookup"><span data-stu-id="b79a8-121">-ShareName</span></span>
<span data-ttu-id="b79a8-122">Name der Azure-Datenfreigabe</span><span class="sxs-lookup"><span data-stu-id="b79a8-122">Azure data share name</span></span>

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

### <span data-ttu-id="b79a8-123">-Synchronisierungs-Nr</span><span class="sxs-lookup"><span data-stu-id="b79a8-123">-SynchronizationId</span></span>
<span data-ttu-id="b79a8-124">Synchronisierungs-ID der Freigabe Synchronisierung</span><span class="sxs-lookup"><span data-stu-id="b79a8-124">Synchronization id of share synchronization</span></span>

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

### <span data-ttu-id="b79a8-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b79a8-125">CommonParameters</span></span>
<span data-ttu-id="b79a8-126">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b79a8-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b79a8-127">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b79a8-127">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b79a8-128">Eingaben</span><span class="sxs-lookup"><span data-stu-id="b79a8-128">INPUTS</span></span>

### <span data-ttu-id="b79a8-129">System. String</span><span class="sxs-lookup"><span data-stu-id="b79a8-129">System.String</span></span>

## <span data-ttu-id="b79a8-130">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="b79a8-130">OUTPUTS</span></span>

### <span data-ttu-id="b79a8-131">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareSynchronizationDetail</span><span class="sxs-lookup"><span data-stu-id="b79a8-131">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareSynchronizationDetail</span></span>

## <span data-ttu-id="b79a8-132">Notizen</span><span class="sxs-lookup"><span data-stu-id="b79a8-132">NOTES</span></span>

## <span data-ttu-id="b79a8-133">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="b79a8-133">RELATED LINKS</span></span>
