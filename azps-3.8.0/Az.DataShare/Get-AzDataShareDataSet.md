---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataShare.dll-Help.xml
Module Name: Az.DataShare
online version: https://docs.microsoft.com/en-us/powershell/module/az.datashare/get-azdatasharedataset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Get-AzDataShareDataSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Get-AzDataShareDataSet.md
ms.openlocfilehash: 73272c2afd0b3d8ef62a522f2e67f04854c2232e
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/21/2020
ms.locfileid: "93995667"
---
# <span data-ttu-id="07f34-101">Get-AzDataShareDataSet</span><span class="sxs-lookup"><span data-stu-id="07f34-101">Get-AzDataShareDataSet</span></span>

## <span data-ttu-id="07f34-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="07f34-102">SYNOPSIS</span></span>
<span data-ttu-id="07f34-103">Ruft Informationen zu Datensätzen in Azure Data Share ab.</span><span class="sxs-lookup"><span data-stu-id="07f34-103">Gets information about Data Sets in Azure data share.</span></span>

## <span data-ttu-id="07f34-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="07f34-104">SYNTAX</span></span>

### <span data-ttu-id="07f34-105">ByFieldsParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="07f34-105">ByFieldsParameterSet (Default)</span></span>
```
Get-AzDataShareDataSet -ResourceGroupName <String> -AccountName <String> -ShareName <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="07f34-106">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="07f34-106">ByResourceIdParameterSet</span></span>
```
Get-AzDataShareDataSet -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="07f34-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="07f34-107">DESCRIPTION</span></span>
<span data-ttu-id="07f34-108">Das Cmdlet " **Get-AzDataShareDataSet** " Ruft Informationen zu Datensätzen ab, die in einer Freigabe in einem Azure Data Share-Konto hinzugefügt wurden.</span><span class="sxs-lookup"><span data-stu-id="07f34-108">The **Get-AzDataShareDataSet** cmdlet gets information about data sets added in a share in an Azure data share account.</span></span> <span data-ttu-id="07f34-109">Wenn Sie den Namen der Datengruppe angeben, ruft dieses Cmdlet Informationen zu der Datengruppe ab.</span><span class="sxs-lookup"><span data-stu-id="07f34-109">If you specify the name of data set, this cmdlet gets information about the data set.</span></span> <span data-ttu-id="07f34-110">Wenn Sie keinen Namen angeben, ruft dieses Cmdlet Informationen zu allen Datensätzen in einer Freigabe ab. Ich</span><span class="sxs-lookup"><span data-stu-id="07f34-110">If you do not specify a name, this cmdlet gets information about all the data sets in a share.I</span></span>

## <span data-ttu-id="07f34-111">Beispiele</span><span class="sxs-lookup"><span data-stu-id="07f34-111">EXAMPLES</span></span>

### <span data-ttu-id="07f34-112">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="07f34-112">Example 1</span></span>
```
PS C:\> Get-AzDataShareDataSet -ResourceGroupName "ADS" -AccountName "WikiAds" -ShareName "AdsShare" -Name "AdsDataSet"
ContainerName  : AdsContainer
DataSetId      : d2411889-5357-4ca8-8d65-9363e46ef2ed
ResourceGroup  : ADS
SubscriptionId : 1834da9b-787a-44f6-ae81-60707ab8c957
StorageAccount : AdsStorage
Id             : /subscriptions/1834da9b-787a-44f6-ae81-60707ab8c957/resourceGroups/ADS/providers/Microsoft.DataShare/accounts/shelltest/shares/share4/dataSets/AdsDataSet
Name           : AdsDataSet
Type           : Microsoft.DataShare/DataSets
```

<span data-ttu-id="07f34-113">Dieser Befehl zeigt Informationen zu Daten Satz AdsDataSet in Freigabe AdsShare in Azure Data Share-Konto WikiAdsAccount und Ressourcengruppen anzeigen an.</span><span class="sxs-lookup"><span data-stu-id="07f34-113">This command displays information about data set AdsDataSet in share AdsShare in Azure data share account WikiAdsAccount and resource group ADS.</span></span>

## <span data-ttu-id="07f34-114">Parameter</span><span class="sxs-lookup"><span data-stu-id="07f34-114">PARAMETERS</span></span>

### <span data-ttu-id="07f34-115">-Kontoname</span><span class="sxs-lookup"><span data-stu-id="07f34-115">-AccountName</span></span>
<span data-ttu-id="07f34-116">Name des Azure Data Share-Kontos</span><span class="sxs-lookup"><span data-stu-id="07f34-116">Azure data share account name.</span></span>

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

### <span data-ttu-id="07f34-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="07f34-117">-DefaultProfile</span></span>
<span data-ttu-id="07f34-118">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="07f34-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="07f34-119">-Name</span><span class="sxs-lookup"><span data-stu-id="07f34-119">-Name</span></span>
<span data-ttu-id="07f34-120">Name des Azure-Datensatzes.</span><span class="sxs-lookup"><span data-stu-id="07f34-120">Azure data set name.</span></span>

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

### <span data-ttu-id="07f34-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="07f34-121">-ResourceGroupName</span></span>
<span data-ttu-id="07f34-122">Der Name der Ressourcengruppe des Azure Data Share-Kontos.</span><span class="sxs-lookup"><span data-stu-id="07f34-122">The resource group name of the azure data share account.</span></span>

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

### <span data-ttu-id="07f34-123">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="07f34-123">-ResourceId</span></span>
<span data-ttu-id="07f34-124">Die Ressourcen-ID der Azure-Datengruppe.</span><span class="sxs-lookup"><span data-stu-id="07f34-124">The resource id of the azure data set.</span></span>

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

### <span data-ttu-id="07f34-125">-Freigabename</span><span class="sxs-lookup"><span data-stu-id="07f34-125">-ShareName</span></span>
<span data-ttu-id="07f34-126">Name der Azure-Datenfreigabe.</span><span class="sxs-lookup"><span data-stu-id="07f34-126">Azure data share name.</span></span>

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

### <span data-ttu-id="07f34-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="07f34-127">CommonParameters</span></span>
<span data-ttu-id="07f34-128">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="07f34-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="07f34-129">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="07f34-129">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="07f34-130">Eingaben</span><span class="sxs-lookup"><span data-stu-id="07f34-130">INPUTS</span></span>

### <span data-ttu-id="07f34-131">System. String</span><span class="sxs-lookup"><span data-stu-id="07f34-131">System.String</span></span>

## <span data-ttu-id="07f34-132">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="07f34-132">OUTPUTS</span></span>

### <span data-ttu-id="07f34-133">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareDataSet</span><span class="sxs-lookup"><span data-stu-id="07f34-133">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareDataSet</span></span>

## <span data-ttu-id="07f34-134">Notizen</span><span class="sxs-lookup"><span data-stu-id="07f34-134">NOTES</span></span>

## <span data-ttu-id="07f34-135">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="07f34-135">RELATED LINKS</span></span>
