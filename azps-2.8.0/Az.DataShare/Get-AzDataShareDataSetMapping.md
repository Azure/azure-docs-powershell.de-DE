---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataShare.dll-Help.xml
Module Name: Az.DataShare
online version: https://docs.microsoft.com/en-us/powershell/module/az.datashare/get-azdatasharedatasetmapping
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Get-AzDataShareDataSetMapping.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Get-AzDataShareDataSetMapping.md
ms.openlocfilehash: d19825fea43e8fc029e960a513d1c2ad306a8406
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93651444"
---
# <span data-ttu-id="e064f-101">Get-AzDataShareDataSetMapping</span><span class="sxs-lookup"><span data-stu-id="e064f-101">Get-AzDataShareDataSetMapping</span></span>

## <span data-ttu-id="e064f-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="e064f-102">SYNOPSIS</span></span>
<span data-ttu-id="e064f-103">Ruft Informationen zu DataSet-Zuordnungen im Share-Abonnement ab.</span><span class="sxs-lookup"><span data-stu-id="e064f-103">Gets information about dataset mappings in share subscription</span></span>

## <span data-ttu-id="e064f-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="e064f-104">SYNTAX</span></span>

### <span data-ttu-id="e064f-105">ByFieldsParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="e064f-105">ByFieldsParameterSet (Default)</span></span>
```
Get-AzDataShareDataSetMapping -ResourceGroupName <String> -AccountName <String> -ShareSubscriptionName <String>
 [-Name <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e064f-106">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="e064f-106">ByResourceIdParameterSet</span></span>
```
Get-AzDataShareDataSetMapping -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="e064f-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="e064f-107">DESCRIPTION</span></span>
<span data-ttu-id="e064f-108">Das Cmdlet " **Get-AzDataShareDataSetMapping** " Ruft Informationen zu einer bestimmten Dataset-Zuordnung ab, wenn der Name angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="e064f-108">The **Get-AzDataShareDataSetMapping** cmdlet gets information about a particular dataset mapping if the name is specified.</span></span> <span data-ttu-id="e064f-109">Andernfalls werden Informationen zu allen DataSet-Zuordnungen in einem Freigabe Abonnement abgerufen.</span><span class="sxs-lookup"><span data-stu-id="e064f-109">Otherwise, it gets information about all the dataset mappings in a share subscription.</span></span> 

## <span data-ttu-id="e064f-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="e064f-110">EXAMPLES</span></span>

### <span data-ttu-id="e064f-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="e064f-111">Example 1</span></span>
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

 <span data-ttu-id="e064f-112">Dieser Befehl zeigt Informationen zu allen DataSet-Zuordnungen im Freigabe Abonnement an.</span><span class="sxs-lookup"><span data-stu-id="e064f-112">This command displays information about all dataset mappings in the share subscription.</span></span>

## <span data-ttu-id="e064f-113">Parameter</span><span class="sxs-lookup"><span data-stu-id="e064f-113">PARAMETERS</span></span>

### <span data-ttu-id="e064f-114">-Kontoname</span><span class="sxs-lookup"><span data-stu-id="e064f-114">-AccountName</span></span>
<span data-ttu-id="e064f-115">Name des Azure Data Share-Kontos</span><span class="sxs-lookup"><span data-stu-id="e064f-115">Azure data share account name.</span></span>

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

### <span data-ttu-id="e064f-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e064f-116">-DefaultProfile</span></span>
<span data-ttu-id="e064f-117">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="e064f-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e064f-118">-Name</span><span class="sxs-lookup"><span data-stu-id="e064f-118">-Name</span></span>
<span data-ttu-id="e064f-119">Name der Azure-Daten satzzuordnung.</span><span class="sxs-lookup"><span data-stu-id="e064f-119">Azure data set mapping name.</span></span>

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

### <span data-ttu-id="e064f-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e064f-120">-ResourceGroupName</span></span>
<span data-ttu-id="e064f-121">Der Name der Ressourcengruppe des Azure Data Share-Kontos.</span><span class="sxs-lookup"><span data-stu-id="e064f-121">The resource group name of azure data share account.</span></span>

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

### <span data-ttu-id="e064f-122">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="e064f-122">-ResourceId</span></span>
<span data-ttu-id="e064f-123">Die Ressourcen-ID der Azure-Daten satzzuordnung.</span><span class="sxs-lookup"><span data-stu-id="e064f-123">The resource id of the azure data set mapping.</span></span>

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

### <span data-ttu-id="e064f-124">-ShareSubscriptionName</span><span class="sxs-lookup"><span data-stu-id="e064f-124">-ShareSubscriptionName</span></span>
<span data-ttu-id="e064f-125">Name des Azure Data Share-Abonnements</span><span class="sxs-lookup"><span data-stu-id="e064f-125">Azure data share subscription name.</span></span>

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

### <span data-ttu-id="e064f-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e064f-126">CommonParameters</span></span>
<span data-ttu-id="e064f-127">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e064f-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e064f-128">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e064f-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e064f-129">Eingaben</span><span class="sxs-lookup"><span data-stu-id="e064f-129">INPUTS</span></span>

### <span data-ttu-id="e064f-130">System. String</span><span class="sxs-lookup"><span data-stu-id="e064f-130">System.String</span></span>

## <span data-ttu-id="e064f-131">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="e064f-131">OUTPUTS</span></span>

### <span data-ttu-id="e064f-132">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareDataSetMapping</span><span class="sxs-lookup"><span data-stu-id="e064f-132">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareDataSetMapping</span></span>

## <span data-ttu-id="e064f-133">Notizen</span><span class="sxs-lookup"><span data-stu-id="e064f-133">NOTES</span></span>

## <span data-ttu-id="e064f-134">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="e064f-134">RELATED LINKS</span></span>
