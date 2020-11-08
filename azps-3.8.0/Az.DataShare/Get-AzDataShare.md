---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataShare.dll-Help.xml
Module Name: Az.DataShare
online version: https://docs.microsoft.com/en-us/powershell/module/az.datashare/get-azdatashare
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Get-AzDataShare.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Get-AzDataShare.md
ms.openlocfilehash: a01d67a5ebf98e07a9410903e4c00b4ed4ee70a2
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/21/2020
ms.locfileid: "93995666"
---
# <span data-ttu-id="8a291-101">Get-AzDataShare</span><span class="sxs-lookup"><span data-stu-id="8a291-101">Get-AzDataShare</span></span>

## <span data-ttu-id="8a291-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="8a291-102">SYNOPSIS</span></span>
<span data-ttu-id="8a291-103">Abrufen von Informationen zu Datenfreigaben</span><span class="sxs-lookup"><span data-stu-id="8a291-103">Get information about Data Shares.</span></span>

## <span data-ttu-id="8a291-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="8a291-104">SYNTAX</span></span>

### <span data-ttu-id="8a291-105">ByFieldsParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="8a291-105">ByFieldsParameterSet (Default)</span></span>
```
Get-AzDataShare -ResourceGroupName <String> -AccountName <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="8a291-106">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="8a291-106">ByResourceIdParameterSet</span></span>
```
Get-AzDataShare -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="8a291-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="8a291-107">DESCRIPTION</span></span>
<span data-ttu-id="8a291-108">Das Cmdlet " **Get-AzDataShare** " Ruft Informationen zu Datenfreigaben in einem Azure-Datenfreigabe-Depot.</span><span class="sxs-lookup"><span data-stu-id="8a291-108">The **Get-AzDataShare** cmdlet gets information about data shares in an Azure data share accoount.</span></span>
<span data-ttu-id="8a291-109">Wenn Sie den Namen einer Datenfreigabe angeben, erhält dieses Cmdlet Informationen zu dieser Datenfreigabe.</span><span class="sxs-lookup"><span data-stu-id="8a291-109">If you specify the name of a data share, this cmdlet gets information about that data share.</span></span>
<span data-ttu-id="8a291-110">Wenn Sie keinen Namen angeben, ruft dieses Cmdlet Informationen zu allen Datenfreigaben in einem Azure-Datenfreigabe Konto ab.</span><span class="sxs-lookup"><span data-stu-id="8a291-110">If you do not specify a name, this cmdlet gets information about all of the data shares in an Azure data share account.</span></span>

## <span data-ttu-id="8a291-111">Beispiele</span><span class="sxs-lookup"><span data-stu-id="8a291-111">EXAMPLES</span></span>

### <span data-ttu-id="8a291-112">Beispiel 1: Abrufen einer bestimmten Datenfreigabe</span><span class="sxs-lookup"><span data-stu-id="8a291-112">Example 1 : Get a specific data share</span></span>
```
PS C:\>Get-AzDataShare -ResourceGroupName "ADS" -AccountName "WikiAdsAccount" -Name "AdsShare"
Name                : AdsShare
Id                  : /subscriptions/f3ead1ff-d0ab-4cf4-9a5a-86f1661d4685/resourceGroups/ADS/providers/Microsoft.DataShare/accounts/WikiAdsAccount/shares/AdsShare
Type                : Microsoft.DataShare/shares
CreatedAt           : 6/11/2019 12:00:00 AM
CreatedBy           : Contoso ADS
ShareKind           : CopyBased
Description         : Example of description  
ProvisioningState   : Succeeded
Terms               : This should not be shared
```

<span data-ttu-id="8a291-113">Dieser Befehl zeigt Informationen zu Datenfreigabe-AdsShare im Azure Data Share-Konto WikiAdsAccount und Anzeigen der Ressourcengruppe an.</span><span class="sxs-lookup"><span data-stu-id="8a291-113">This command displays information about data share AdsShare in the Azure data share account WikiAdsAccount and resource group ADS.</span></span>

## <span data-ttu-id="8a291-114">Parameter</span><span class="sxs-lookup"><span data-stu-id="8a291-114">PARAMETERS</span></span>

### <span data-ttu-id="8a291-115">-Kontoname</span><span class="sxs-lookup"><span data-stu-id="8a291-115">-AccountName</span></span>
<span data-ttu-id="8a291-116">Name des Azure-Datenfreigabe Kontos</span><span class="sxs-lookup"><span data-stu-id="8a291-116">Azure data share account name</span></span>

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

### <span data-ttu-id="8a291-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8a291-117">-DefaultProfile</span></span>
<span data-ttu-id="8a291-118">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="8a291-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8a291-119">-Name</span><span class="sxs-lookup"><span data-stu-id="8a291-119">-Name</span></span>
<span data-ttu-id="8a291-120">Name der Azure-Datenfreigabe</span><span class="sxs-lookup"><span data-stu-id="8a291-120">Azure data share name</span></span>

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

### <span data-ttu-id="8a291-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8a291-121">-ResourceGroupName</span></span>
<span data-ttu-id="8a291-122">Der Name der Ressourcengruppe des Azure Data Share-Kontos</span><span class="sxs-lookup"><span data-stu-id="8a291-122">The resource group name of the azure data share account</span></span>

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

### <span data-ttu-id="8a291-123">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="8a291-123">-ResourceId</span></span>
<span data-ttu-id="8a291-124">Die Ressourcen-ID der Azure-Datenfreigabe</span><span class="sxs-lookup"><span data-stu-id="8a291-124">The resource id of the azure data share</span></span>

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

### <span data-ttu-id="8a291-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8a291-125">CommonParameters</span></span>
<span data-ttu-id="8a291-126">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8a291-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8a291-127">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8a291-127">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8a291-128">Eingaben</span><span class="sxs-lookup"><span data-stu-id="8a291-128">INPUTS</span></span>

### <span data-ttu-id="8a291-129">System. String</span><span class="sxs-lookup"><span data-stu-id="8a291-129">System.String</span></span>

## <span data-ttu-id="8a291-130">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="8a291-130">OUTPUTS</span></span>

### <span data-ttu-id="8a291-131">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShare</span><span class="sxs-lookup"><span data-stu-id="8a291-131">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShare</span></span>

## <span data-ttu-id="8a291-132">Notizen</span><span class="sxs-lookup"><span data-stu-id="8a291-132">NOTES</span></span>

## <span data-ttu-id="8a291-133">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="8a291-133">RELATED LINKS</span></span>
