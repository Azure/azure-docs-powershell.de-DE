---
external help file: Microsoft.Azure.Commands.DataLakeAnalytics.dll-Help.xml
Module Name: AzureRM.DataLakeAnalytics
ms.assetid: 4EA01047-021C-4FA5-82F0-5102BA114BC2
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeAnalytics/Commands.DataLakeAnalytics/help/Get-AzureRmDataLakeAnalyticsAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeAnalytics/Commands.DataLakeAnalytics/help/Get-AzureRmDataLakeAnalyticsAccount.md
ms.openlocfilehash: 1ab8cbd8ead120ecc531e3e252fe2c31a58f10c7
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93662430"
---
# <span data-ttu-id="506f1-101">Get-AzureRmDataLakeAnalyticsAccount</span><span class="sxs-lookup"><span data-stu-id="506f1-101">Get-AzureRmDataLakeAnalyticsAccount</span></span>

## <span data-ttu-id="506f1-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="506f1-102">SYNOPSIS</span></span>
<span data-ttu-id="506f1-103">Ruft Informationen zu einem Data Lake Analytics-Konto ab.</span><span class="sxs-lookup"><span data-stu-id="506f1-103">Gets information about a Data Lake Analytics account.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="506f1-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="506f1-104">SYNTAX</span></span>

### <span data-ttu-id="506f1-105">Alle im Abonnement (Standard)</span><span class="sxs-lookup"><span data-stu-id="506f1-105">All In Subscription (Default)</span></span>
```
Get-AzureRmDataLakeAnalyticsAccount [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="506f1-106">Alle in der Ressourcengruppe</span><span class="sxs-lookup"><span data-stu-id="506f1-106">All In Resource Group</span></span>
```
Get-AzureRmDataLakeAnalyticsAccount [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="506f1-107">Bestimmtes Konto</span><span class="sxs-lookup"><span data-stu-id="506f1-107">Specific Account</span></span>
```
Get-AzureRmDataLakeAnalyticsAccount [[-ResourceGroupName] <String>] [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="506f1-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="506f1-108">DESCRIPTION</span></span>
<span data-ttu-id="506f1-109">Das Cmdlet " **Get-AzureRmDataLakeAnalyticsAccount** " Ruft Informationen zu einem Azure Data Lake Analytics-Konto ab.</span><span class="sxs-lookup"><span data-stu-id="506f1-109">The **Get-AzureRmDataLakeAnalyticsAccount** cmdlet gets information about an Azure Data Lake Analytics account.</span></span>

## <span data-ttu-id="506f1-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="506f1-110">EXAMPLES</span></span>

### <span data-ttu-id="506f1-111">Beispiel 1: Abrufen von Informationen zu einem Data Lake Analytics-Konto</span><span class="sxs-lookup"><span data-stu-id="506f1-111">Example 1: Get information about a Data Lake Analytics account</span></span>
```
PS C:\>Get-AzureRmDataLakeAnalyticsAccount -Name "ContosoAdlAccount"
```

<span data-ttu-id="506f1-112">Dieser Befehl ruft Informationen über das Konto mit dem Namen ContosoAdlAccount ab.</span><span class="sxs-lookup"><span data-stu-id="506f1-112">This command gets information about the account named ContosoAdlAccount.</span></span>

## <span data-ttu-id="506f1-113">Parameter</span><span class="sxs-lookup"><span data-stu-id="506f1-113">PARAMETERS</span></span>

### <span data-ttu-id="506f1-114">-Name</span><span class="sxs-lookup"><span data-stu-id="506f1-114">-Name</span></span>
<span data-ttu-id="506f1-115">Gibt den Namen des Data Lake Analytics-Kontos an.</span><span class="sxs-lookup"><span data-stu-id="506f1-115">Specifies the name of the Data Lake Analytics account.</span></span>

```yaml
Type: System.String
Parameter Sets: Specific Account
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="506f1-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="506f1-116">-ResourceGroupName</span></span>
<span data-ttu-id="506f1-117">Gibt den Ressourcengruppennamen des Data Lake Analytics-Kontos an.</span><span class="sxs-lookup"><span data-stu-id="506f1-117">Specifies the resource group name of the Data Lake Analytics account.</span></span>

```yaml
Type: System.String
Parameter Sets: All In Resource Group
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: Specific Account
Aliases: 

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="506f1-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="506f1-118">-DefaultProfile</span></span>
<span data-ttu-id="506f1-119">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="506f1-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="506f1-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="506f1-120">CommonParameters</span></span>
<span data-ttu-id="506f1-121">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="506f1-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="506f1-122">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="506f1-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="506f1-123">Eingaben</span><span class="sxs-lookup"><span data-stu-id="506f1-123">INPUTS</span></span>

## <span data-ttu-id="506f1-124">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="506f1-124">OUTPUTS</span></span>

### <span data-ttu-id="506f1-125">PSDataLakeAnalyticsAccount</span><span class="sxs-lookup"><span data-stu-id="506f1-125">PSDataLakeAnalyticsAccount</span></span>
<span data-ttu-id="506f1-126">Die angegebenen Kontodetails.</span><span class="sxs-lookup"><span data-stu-id="506f1-126">The specified account details.</span></span>

### <span data-ttu-id="506f1-127">Liste<PSDataLakeAnalyticsAccount></span><span class="sxs-lookup"><span data-stu-id="506f1-127">List<PSDataLakeAnalyticsAccount></span></span>
<span data-ttu-id="506f1-128">Die Liste der Konten in der angegebenen Ressourcengruppe oder dem angegebenen Abonnement.</span><span class="sxs-lookup"><span data-stu-id="506f1-128">The list of accounts in the specified resource group or subscription.</span></span>

## <span data-ttu-id="506f1-129">Notizen</span><span class="sxs-lookup"><span data-stu-id="506f1-129">NOTES</span></span>

## <span data-ttu-id="506f1-130">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="506f1-130">RELATED LINKS</span></span>

[<span data-ttu-id="506f1-131">Neu – AzureRmDataLakeAnalyticsAccount</span><span class="sxs-lookup"><span data-stu-id="506f1-131">New-AzureRmDataLakeAnalyticsAccount</span></span>](./New-AzureRmDataLakeAnalyticsAccount.md)

[<span data-ttu-id="506f1-132">Remove-AzureRmDataLakeAnalyticsAccount</span><span class="sxs-lookup"><span data-stu-id="506f1-132">Remove-AzureRmDataLakeAnalyticsAccount</span></span>](./Remove-AzureRmDataLakeAnalyticsAccount.md)

[<span data-ttu-id="506f1-133">Satz-AzureRmDataLakeAnalyticsAccount</span><span class="sxs-lookup"><span data-stu-id="506f1-133">Set-AzureRmDataLakeAnalyticsAccount</span></span>](./Set-AzureRmDataLakeAnalyticsAccount.md)

[<span data-ttu-id="506f1-134">Test-AzureRmDataLakeAnalyticsAccount</span><span class="sxs-lookup"><span data-stu-id="506f1-134">Test-AzureRmDataLakeAnalyticsAccount</span></span>](./Test-AzureRmDataLakeAnalyticsAccount.md)


