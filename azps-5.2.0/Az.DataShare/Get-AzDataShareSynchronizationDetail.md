---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataShare.dll-Help.xml
Module Name: Az.DataShare
online version: https://docs.microsoft.com/en-us/powershell/module/az.datashare/get-azdatasharesynchronizationdetail
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Get-AzDataShareSynchronizationDetail.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Get-AzDataShareSynchronizationDetail.md
ms.openlocfilehash: 2ee3714895b751223768ac3f98efbd04405ae69f
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98299152"
---
# <span data-ttu-id="6eb9a-101">Get-AzDataShareSynchronizationDetail</span><span class="sxs-lookup"><span data-stu-id="6eb9a-101">Get-AzDataShareSynchronizationDetail</span></span>

## <span data-ttu-id="6eb9a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6eb9a-102">SYNOPSIS</span></span>
<span data-ttu-id="6eb9a-103">Ruft Informationen zu den Synchronisierungsdetails für eine Freigabe ab.</span><span class="sxs-lookup"><span data-stu-id="6eb9a-103">Gets information about synchronization details for a share.</span></span>

## <span data-ttu-id="6eb9a-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="6eb9a-104">SYNTAX</span></span>

### <span data-ttu-id="6eb9a-105">ByFieldsParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="6eb9a-105">ByFieldsParameterSet (Default)</span></span>
```
Get-AzDataShareSynchronizationDetail -ResourceGroupName <String> -AccountName <String> -ShareName <String>
 -SynchronizationId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="6eb9a-106">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="6eb9a-106">ByResourceIdParameterSet</span></span>
```
Get-AzDataShareSynchronizationDetail -SynchronizationId <String> -ResourceId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="6eb9a-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="6eb9a-107">DESCRIPTION</span></span>
<span data-ttu-id="6eb9a-108">Das **Cmdlet "Get-AzDataShareSynchronizationDetail"** enthält Details zur für eine Freigabe initiierten Synchronisierung.</span><span class="sxs-lookup"><span data-stu-id="6eb9a-108">The **Get-AzDataShareSynchronizationDetail** cmdlet provides details of the synchronization initiated for a share.</span></span>

## <span data-ttu-id="6eb9a-109">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="6eb9a-109">EXAMPLES</span></span>

### <span data-ttu-id="6eb9a-110">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="6eb9a-110">Example 1</span></span>
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

<span data-ttu-id="6eb9a-111">Dieser Befehl enthält Informationen zu den Synchronisierungsdetails aller Datensätze, die der bereitgestellten Synchronisierungs-ID zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="6eb9a-111">This command provides information about the synchronization details of all the data sets corresponding to the provided synchronization id.</span></span>

## <span data-ttu-id="6eb9a-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="6eb9a-112">PARAMETERS</span></span>

### <span data-ttu-id="6eb9a-113">-AccountName</span><span class="sxs-lookup"><span data-stu-id="6eb9a-113">-AccountName</span></span>
<span data-ttu-id="6eb9a-114">Name des Azure-Datenfreigabekontos</span><span class="sxs-lookup"><span data-stu-id="6eb9a-114">Azure data share account name</span></span>

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

### <span data-ttu-id="6eb9a-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6eb9a-115">-DefaultProfile</span></span>
<span data-ttu-id="6eb9a-116">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="6eb9a-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6eb9a-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6eb9a-117">-ResourceGroupName</span></span>
<span data-ttu-id="6eb9a-118">Der Ressourcengruppenname des Azure Data Share-Kontos</span><span class="sxs-lookup"><span data-stu-id="6eb9a-118">The resource group name of the azure data share account</span></span>

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

### <span data-ttu-id="6eb9a-119">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="6eb9a-119">-ResourceId</span></span>
<span data-ttu-id="6eb9a-120">Azure Data Share Resource ID</span><span class="sxs-lookup"><span data-stu-id="6eb9a-120">Azure data share resource id</span></span>

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

### <span data-ttu-id="6eb9a-121">-ShareName</span><span class="sxs-lookup"><span data-stu-id="6eb9a-121">-ShareName</span></span>
<span data-ttu-id="6eb9a-122">Name der Azure-Datenfreigabe</span><span class="sxs-lookup"><span data-stu-id="6eb9a-122">Azure data share name</span></span>

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

### <span data-ttu-id="6eb9a-123">-SynchronizationId</span><span class="sxs-lookup"><span data-stu-id="6eb9a-123">-SynchronizationId</span></span>
<span data-ttu-id="6eb9a-124">Synchronisierungs-ID der Freigabesynchronisierung</span><span class="sxs-lookup"><span data-stu-id="6eb9a-124">Synchronization id of share synchronization</span></span>

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

### <span data-ttu-id="6eb9a-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6eb9a-125">CommonParameters</span></span>
<span data-ttu-id="6eb9a-126">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6eb9a-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6eb9a-127">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="6eb9a-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6eb9a-128">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="6eb9a-128">INPUTS</span></span>

### <span data-ttu-id="6eb9a-129">System.String</span><span class="sxs-lookup"><span data-stu-id="6eb9a-129">System.String</span></span>

## <span data-ttu-id="6eb9a-130">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="6eb9a-130">OUTPUTS</span></span>

### <span data-ttu-id="6eb9a-131">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareSynchronizationDetail</span><span class="sxs-lookup"><span data-stu-id="6eb9a-131">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareSynchronizationDetail</span></span>

## <span data-ttu-id="6eb9a-132">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="6eb9a-132">NOTES</span></span>

## <span data-ttu-id="6eb9a-133">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="6eb9a-133">RELATED LINKS</span></span>
