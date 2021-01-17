---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeAnalytics.dll-Help.xml
Module Name: Az.DataLakeAnalytics
ms.assetid: 4EA01047-021C-4FA5-82F0-5102BA114BC2
online version: https://docs.microsoft.com/en-us/powershell/module/az.datalakeanalytics/get-azdatalakeanalyticsaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeAnalytics/DataLakeAnalytics/help/Get-AzDataLakeAnalyticsAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeAnalytics/DataLakeAnalytics/help/Get-AzDataLakeAnalyticsAccount.md
ms.openlocfilehash: 1894e5a79660558163d9b95ce49f1736ea002bf9
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98470518"
---
# <span data-ttu-id="6a320-101">Get-AzDataLakeAnalyticsAccount</span><span class="sxs-lookup"><span data-stu-id="6a320-101">Get-AzDataLakeAnalyticsAccount</span></span>

## <span data-ttu-id="6a320-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6a320-102">SYNOPSIS</span></span>
<span data-ttu-id="6a320-103">Ruft Informationen zu einem Data Lake Analytics-Konto ab.</span><span class="sxs-lookup"><span data-stu-id="6a320-103">Gets information about a Data Lake Analytics account.</span></span>

## <span data-ttu-id="6a320-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="6a320-104">SYNTAX</span></span>

### <span data-ttu-id="6a320-105">GetAllInSubscription (Standard)</span><span class="sxs-lookup"><span data-stu-id="6a320-105">GetAllInSubscription (Default)</span></span>
```
Get-AzDataLakeAnalyticsAccount [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="6a320-106">GetByResourceGroup</span><span class="sxs-lookup"><span data-stu-id="6a320-106">GetByResourceGroup</span></span>
```
Get-AzDataLakeAnalyticsAccount [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="6a320-107">GetBySpecificAccount</span><span class="sxs-lookup"><span data-stu-id="6a320-107">GetBySpecificAccount</span></span>
```
Get-AzDataLakeAnalyticsAccount [[-ResourceGroupName] <String>] [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="6a320-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="6a320-108">DESCRIPTION</span></span>
<span data-ttu-id="6a320-109">Das **Cmdlet "Get-AzDataLakeAnalyticsAccount"** ruft Informationen zu einem Azure Data Lake Analytics-Konto ab.</span><span class="sxs-lookup"><span data-stu-id="6a320-109">The **Get-AzDataLakeAnalyticsAccount** cmdlet gets information about an Azure Data Lake Analytics account.</span></span>

## <span data-ttu-id="6a320-110">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="6a320-110">EXAMPLES</span></span>

### <span data-ttu-id="6a320-111">Beispiel 1: Erhalten von Informationen zu einem Data Lake Analytics-Konto</span><span class="sxs-lookup"><span data-stu-id="6a320-111">Example 1: Get information about a Data Lake Analytics account</span></span>
```
PS C:\>Get-AzDataLakeAnalyticsAccount -Name "ContosoAdlAccount"
```

<span data-ttu-id="6a320-112">Dieser Befehl ruft Informationen über das Konto mit dem Namen "ContosoAdlAccount" ab.</span><span class="sxs-lookup"><span data-stu-id="6a320-112">This command gets information about the account named ContosoAdlAccount.</span></span>

## <span data-ttu-id="6a320-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="6a320-113">PARAMETERS</span></span>

### <span data-ttu-id="6a320-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6a320-114">-DefaultProfile</span></span>
<span data-ttu-id="6a320-115">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden</span><span class="sxs-lookup"><span data-stu-id="6a320-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="6a320-116">-Name</span><span class="sxs-lookup"><span data-stu-id="6a320-116">-Name</span></span>
<span data-ttu-id="6a320-117">Gibt den Namen des Data Lake Analytics-Kontos an.</span><span class="sxs-lookup"><span data-stu-id="6a320-117">Specifies the name of the Data Lake Analytics account.</span></span>

```yaml
Type: System.String
Parameter Sets: GetBySpecificAccount
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6a320-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6a320-118">-ResourceGroupName</span></span>
<span data-ttu-id="6a320-119">Gibt den Ressourcengruppennamen des Data Lake Analytics-Kontos an.</span><span class="sxs-lookup"><span data-stu-id="6a320-119">Specifies the resource group name of the Data Lake Analytics account.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByResourceGroup
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: GetBySpecificAccount
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6a320-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6a320-120">CommonParameters</span></span>
<span data-ttu-id="6a320-121">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6a320-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6a320-122">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6a320-122">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6a320-123">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="6a320-123">INPUTS</span></span>

### <span data-ttu-id="6a320-124">System.String</span><span class="sxs-lookup"><span data-stu-id="6a320-124">System.String</span></span>

## <span data-ttu-id="6a320-125">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="6a320-125">OUTPUTS</span></span>

### <span data-ttu-id="6a320-126">Microsoft.Azure.Commands.DataLakeAnalytics.Models.PSDataLakeAnalyticsAccount</span><span class="sxs-lookup"><span data-stu-id="6a320-126">Microsoft.Azure.Commands.DataLakeAnalytics.Models.PSDataLakeAnalyticsAccount</span></span>

### <span data-ttu-id="6a320-127">Microsoft.Azure.Commands.DataLakeAnalytics.Models.PSDataLakeAnalyticsAccountBasic</span><span class="sxs-lookup"><span data-stu-id="6a320-127">Microsoft.Azure.Commands.DataLakeAnalytics.Models.PSDataLakeAnalyticsAccountBasic</span></span>

## <span data-ttu-id="6a320-128">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="6a320-128">NOTES</span></span>

## <span data-ttu-id="6a320-129">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="6a320-129">RELATED LINKS</span></span>

[<span data-ttu-id="6a320-130">New-AzDataLakeAnalyticsAccount</span><span class="sxs-lookup"><span data-stu-id="6a320-130">New-AzDataLakeAnalyticsAccount</span></span>](./New-AzDataLakeAnalyticsAccount.md)

[<span data-ttu-id="6a320-131">Remove-AzDataLakeAnalyticsAccount</span><span class="sxs-lookup"><span data-stu-id="6a320-131">Remove-AzDataLakeAnalyticsAccount</span></span>](./Remove-AzDataLakeAnalyticsAccount.md)

[<span data-ttu-id="6a320-132">Set-AzDataLakeAnalyticsAccount</span><span class="sxs-lookup"><span data-stu-id="6a320-132">Set-AzDataLakeAnalyticsAccount</span></span>](./Set-AzDataLakeAnalyticsAccount.md)

[<span data-ttu-id="6a320-133">Test-AzDataLakeAnalyticsAccount</span><span class="sxs-lookup"><span data-stu-id="6a320-133">Test-AzDataLakeAnalyticsAccount</span></span>](./Test-AzDataLakeAnalyticsAccount.md)


