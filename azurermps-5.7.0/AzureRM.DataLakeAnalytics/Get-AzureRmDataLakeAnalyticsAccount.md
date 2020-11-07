---
external help file: Microsoft.Azure.Commands.DataLakeAnalytics.dll-Help.xml
Module Name: AzureRM.DataLakeAnalytics
ms.assetid: 4EA01047-021C-4FA5-82F0-5102BA114BC2
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datalakeanalytics/get-azurermdatalakeanalyticsaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeAnalytics/Commands.DataLakeAnalytics/help/Get-AzureRmDataLakeAnalyticsAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeAnalytics/Commands.DataLakeAnalytics/help/Get-AzureRmDataLakeAnalyticsAccount.md
ms.openlocfilehash: 71d524aeea441c80b90642a01f1a2f34996904ba
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93662586"
---
# <span data-ttu-id="9e1af-101">Get-AzureRmDataLakeAnalyticsAccount</span><span class="sxs-lookup"><span data-stu-id="9e1af-101">Get-AzureRmDataLakeAnalyticsAccount</span></span>

## <span data-ttu-id="9e1af-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="9e1af-102">SYNOPSIS</span></span>
<span data-ttu-id="9e1af-103">Ruft Informationen zu einem Data Lake Analytics-Konto ab.</span><span class="sxs-lookup"><span data-stu-id="9e1af-103">Gets information about a Data Lake Analytics account.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="9e1af-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="9e1af-104">SYNTAX</span></span>

### <span data-ttu-id="9e1af-105">GetAllInSubscription (Standard)</span><span class="sxs-lookup"><span data-stu-id="9e1af-105">GetAllInSubscription (Default)</span></span>
```
Get-AzureRmDataLakeAnalyticsAccount [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="9e1af-106">GetByResourceGroup</span><span class="sxs-lookup"><span data-stu-id="9e1af-106">GetByResourceGroup</span></span>
```
Get-AzureRmDataLakeAnalyticsAccount [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="9e1af-107">GetBySpecificAccount</span><span class="sxs-lookup"><span data-stu-id="9e1af-107">GetBySpecificAccount</span></span>
```
Get-AzureRmDataLakeAnalyticsAccount [[-ResourceGroupName] <String>] [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="9e1af-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="9e1af-108">DESCRIPTION</span></span>
<span data-ttu-id="9e1af-109">Das Cmdlet " **Get-AzureRmDataLakeAnalyticsAccount** " Ruft Informationen zu einem Azure Data Lake Analytics-Konto ab.</span><span class="sxs-lookup"><span data-stu-id="9e1af-109">The **Get-AzureRmDataLakeAnalyticsAccount** cmdlet gets information about an Azure Data Lake Analytics account.</span></span>

## <span data-ttu-id="9e1af-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="9e1af-110">EXAMPLES</span></span>

### <span data-ttu-id="9e1af-111">Beispiel 1: Abrufen von Informationen zu einem Data Lake Analytics-Konto</span><span class="sxs-lookup"><span data-stu-id="9e1af-111">Example 1: Get information about a Data Lake Analytics account</span></span>
```
PS C:\>Get-AzureRmDataLakeAnalyticsAccount -Name "ContosoAdlAccount"
```

<span data-ttu-id="9e1af-112">Dieser Befehl ruft Informationen über das Konto mit dem Namen ContosoAdlAccount ab.</span><span class="sxs-lookup"><span data-stu-id="9e1af-112">This command gets information about the account named ContosoAdlAccount.</span></span>

## <span data-ttu-id="9e1af-113">Parameter</span><span class="sxs-lookup"><span data-stu-id="9e1af-113">PARAMETERS</span></span>

### <span data-ttu-id="9e1af-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9e1af-114">-DefaultProfile</span></span>
<span data-ttu-id="9e1af-115">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="9e1af-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9e1af-116">-Name</span><span class="sxs-lookup"><span data-stu-id="9e1af-116">-Name</span></span>
<span data-ttu-id="9e1af-117">Gibt den Namen des Data Lake Analytics-Kontos an.</span><span class="sxs-lookup"><span data-stu-id="9e1af-117">Specifies the name of the Data Lake Analytics account.</span></span>

```yaml
Type: String
Parameter Sets: GetBySpecificAccount
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9e1af-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9e1af-118">-ResourceGroupName</span></span>
<span data-ttu-id="9e1af-119">Gibt den Ressourcengruppennamen des Data Lake Analytics-Kontos an.</span><span class="sxs-lookup"><span data-stu-id="9e1af-119">Specifies the resource group name of the Data Lake Analytics account.</span></span>

```yaml
Type: String
Parameter Sets: GetByResourceGroup
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: GetBySpecificAccount
Aliases: 

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9e1af-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9e1af-120">CommonParameters</span></span>
<span data-ttu-id="9e1af-121">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9e1af-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9e1af-122">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9e1af-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9e1af-123">Eingaben</span><span class="sxs-lookup"><span data-stu-id="9e1af-123">INPUTS</span></span>

### <span data-ttu-id="9e1af-124">Keine</span><span class="sxs-lookup"><span data-stu-id="9e1af-124">None</span></span>
<span data-ttu-id="9e1af-125">Dieses Cmdlet akzeptiert keine Eingaben.</span><span class="sxs-lookup"><span data-stu-id="9e1af-125">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="9e1af-126">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="9e1af-126">OUTPUTS</span></span>

### <span data-ttu-id="9e1af-127">PSDataLakeAnalyticsAccount</span><span class="sxs-lookup"><span data-stu-id="9e1af-127">PSDataLakeAnalyticsAccount</span></span>
<span data-ttu-id="9e1af-128">Die angegebenen Kontodetails.</span><span class="sxs-lookup"><span data-stu-id="9e1af-128">The specified account details.</span></span>

### <span data-ttu-id="9e1af-129">Liste<PSDataLakeAnalyticsAccountBasic></span><span class="sxs-lookup"><span data-stu-id="9e1af-129">List<PSDataLakeAnalyticsAccountBasic></span></span>
<span data-ttu-id="9e1af-130">Die Liste der Konten in der angegebenen Ressourcengruppe oder dem angegebenen Abonnement.</span><span class="sxs-lookup"><span data-stu-id="9e1af-130">The list of accounts in the specified resource group or subscription.</span></span>

## <span data-ttu-id="9e1af-131">Notizen</span><span class="sxs-lookup"><span data-stu-id="9e1af-131">NOTES</span></span>

## <span data-ttu-id="9e1af-132">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="9e1af-132">RELATED LINKS</span></span>

[<span data-ttu-id="9e1af-133">Neu – AzureRmDataLakeAnalyticsAccount</span><span class="sxs-lookup"><span data-stu-id="9e1af-133">New-AzureRmDataLakeAnalyticsAccount</span></span>](./New-AzureRmDataLakeAnalyticsAccount.md)

[<span data-ttu-id="9e1af-134">Remove-AzureRmDataLakeAnalyticsAccount</span><span class="sxs-lookup"><span data-stu-id="9e1af-134">Remove-AzureRmDataLakeAnalyticsAccount</span></span>](./Remove-AzureRmDataLakeAnalyticsAccount.md)

[<span data-ttu-id="9e1af-135">Satz-AzureRmDataLakeAnalyticsAccount</span><span class="sxs-lookup"><span data-stu-id="9e1af-135">Set-AzureRmDataLakeAnalyticsAccount</span></span>](./Set-AzureRmDataLakeAnalyticsAccount.md)

[<span data-ttu-id="9e1af-136">Test-AzureRmDataLakeAnalyticsAccount</span><span class="sxs-lookup"><span data-stu-id="9e1af-136">Test-AzureRmDataLakeAnalyticsAccount</span></span>](./Test-AzureRmDataLakeAnalyticsAccount.md)


