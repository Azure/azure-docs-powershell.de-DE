---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataShare.dll-Help.xml
Module Name: Az.DataShare
online version: https://docs.microsoft.com/en-us/powershell/module/az.datashare/get-azdatasharedatasetmapping
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Get-AzDataShareDataSetMapping.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Get-AzDataShareDataSetMapping.md
ms.openlocfilehash: 99f80aa920a402867b6385a3b4ef7ac118838f80
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100166028"
---
# <span data-ttu-id="fe4ca-101">Get-AzDataShareDataSetMapping</span><span class="sxs-lookup"><span data-stu-id="fe4ca-101">Get-AzDataShareDataSetMapping</span></span>

## <span data-ttu-id="fe4ca-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="fe4ca-102">SYNOPSIS</span></span>
<span data-ttu-id="fe4ca-103">Ruft Informationen zu Datasetzuordnungen im Freigabeabonnement ab.</span><span class="sxs-lookup"><span data-stu-id="fe4ca-103">Gets information about dataset mappings in share subscription</span></span>

## <span data-ttu-id="fe4ca-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="fe4ca-104">SYNTAX</span></span>

### <span data-ttu-id="fe4ca-105">ByFieldsParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="fe4ca-105">ByFieldsParameterSet (Default)</span></span>
```
Get-AzDataShareDataSetMapping -ResourceGroupName <String> -AccountName <String> -ShareSubscriptionName <String>
 [-Name <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="fe4ca-106">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="fe4ca-106">ByResourceIdParameterSet</span></span>
```
Get-AzDataShareDataSetMapping -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="fe4ca-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="fe4ca-107">DESCRIPTION</span></span>
<span data-ttu-id="fe4ca-108">Das **Cmdlet "Get-AzDataShareDataSetMapping"** ruft Informationen zu einer bestimmten Datasetzuordnung ab, wenn der Name angegeben ist.</span><span class="sxs-lookup"><span data-stu-id="fe4ca-108">The **Get-AzDataShareDataSetMapping** cmdlet gets information about a particular dataset mapping if the name is specified.</span></span> <span data-ttu-id="fe4ca-109">Andernfalls werden Informationen zu allen Datasetzuordnungen in einem Freigabeabonnement angezeigt.</span><span class="sxs-lookup"><span data-stu-id="fe4ca-109">Otherwise, it gets information about all the dataset mappings in a share subscription.</span></span> 

## <span data-ttu-id="fe4ca-110">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="fe4ca-110">EXAMPLES</span></span>

### <span data-ttu-id="fe4ca-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="fe4ca-111">Example 1</span></span>
```
PS C:\> Get-AzDataShareDataSetMapping -ResourceGroupName "ADS" -AccountName "WikiAdsAccount" -ShareSubscriptionName "WikiADS"

ContainerName        : testing
Prefix               : providercontainer
DataSetId            : 372899d4-5e67-4c85-bc60-21168b484424
ResourceGroup        : ADS
SubscriptionId       : 4834da9b-787a-44f6-ae81-60707ab8c957
StorageAccount       : storageaccount
DataSetMappingStatus : Ok
Id                   : /subscriptions/4834da9b-787a-44f6-ae81-60707ab8c957/resourceGroups/ADS/providers/Microsoft.DataShare/accounts/WikiAdsAccount/shareSubscriptions/WikiADS/dataSetMappings/dsm
Name                 : dsm
Type                 : Microsoft.DataShare/DataSetMappings
```

 <span data-ttu-id="fe4ca-112">Dieser Befehl zeigt Informationen zu allen Datasetzuordnungen im Freigabeabonnement an.</span><span class="sxs-lookup"><span data-stu-id="fe4ca-112">This command displays information about all dataset mappings in the share subscription.</span></span>

## <span data-ttu-id="fe4ca-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="fe4ca-113">PARAMETERS</span></span>

### <span data-ttu-id="fe4ca-114">-AccountName</span><span class="sxs-lookup"><span data-stu-id="fe4ca-114">-AccountName</span></span>
<span data-ttu-id="fe4ca-115">Name des Azure-Datenfreigabekontos.</span><span class="sxs-lookup"><span data-stu-id="fe4ca-115">Azure data share account name.</span></span>

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

### <span data-ttu-id="fe4ca-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fe4ca-116">-DefaultProfile</span></span>
<span data-ttu-id="fe4ca-117">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="fe4ca-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="fe4ca-118">-Name</span><span class="sxs-lookup"><span data-stu-id="fe4ca-118">-Name</span></span>
<span data-ttu-id="fe4ca-119">Name der Azure-Datensatzzuordnung.</span><span class="sxs-lookup"><span data-stu-id="fe4ca-119">Azure data set mapping name.</span></span>

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

### <span data-ttu-id="fe4ca-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fe4ca-120">-ResourceGroupName</span></span>
<span data-ttu-id="fe4ca-121">Der Ressourcengruppenname des Azure Data Share-Kontos.</span><span class="sxs-lookup"><span data-stu-id="fe4ca-121">The resource group name of azure data share account.</span></span>

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

### <span data-ttu-id="fe4ca-122">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="fe4ca-122">-ResourceId</span></span>
<span data-ttu-id="fe4ca-123">Die Ressourcen-ID der Azure-Datensetzuordnung.</span><span class="sxs-lookup"><span data-stu-id="fe4ca-123">The resource id of the azure data set mapping.</span></span>

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

### <span data-ttu-id="fe4ca-124">-ShareSubscriptionName</span><span class="sxs-lookup"><span data-stu-id="fe4ca-124">-ShareSubscriptionName</span></span>
<span data-ttu-id="fe4ca-125">Name des Azure Data Share-Abonnements.</span><span class="sxs-lookup"><span data-stu-id="fe4ca-125">Azure data share subscription name.</span></span>

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

### <span data-ttu-id="fe4ca-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fe4ca-126">CommonParameters</span></span>
<span data-ttu-id="fe4ca-127">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fe4ca-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fe4ca-128">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="fe4ca-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fe4ca-129">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="fe4ca-129">INPUTS</span></span>

### <span data-ttu-id="fe4ca-130">System.String</span><span class="sxs-lookup"><span data-stu-id="fe4ca-130">System.String</span></span>

## <span data-ttu-id="fe4ca-131">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="fe4ca-131">OUTPUTS</span></span>

### <span data-ttu-id="fe4ca-132">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareDataSetMapping</span><span class="sxs-lookup"><span data-stu-id="fe4ca-132">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareDataSetMapping</span></span>

## <span data-ttu-id="fe4ca-133">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="fe4ca-133">NOTES</span></span>

## <span data-ttu-id="fe4ca-134">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="fe4ca-134">RELATED LINKS</span></span>
