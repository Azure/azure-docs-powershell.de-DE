---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeAnalytics.dll-Help.xml
Module Name: Az.DataLakeAnalytics
ms.assetid: 0B52890D-102F-4C3C-9EF9-017F6ECA3E26
online version: https://docs.microsoft.com/powershell/module/az.datalakeanalytics/test-azdatalakeanalyticsaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeAnalytics/DataLakeAnalytics/help/Test-AzDataLakeAnalyticsAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeAnalytics/DataLakeAnalytics/help/Test-AzDataLakeAnalyticsAccount.md
ms.openlocfilehash: b5c1303625676006929a3c2eee80f5d5961bc438
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101947195"
---
# <span data-ttu-id="18aa8-101">Test-AzDataLakeAnalyticsAccount</span><span class="sxs-lookup"><span data-stu-id="18aa8-101">Test-AzDataLakeAnalyticsAccount</span></span>

## <span data-ttu-id="18aa8-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="18aa8-102">SYNOPSIS</span></span>
<span data-ttu-id="18aa8-103">Überprüft das Vorhandensein eines Data Lake Analytics-Kontos.</span><span class="sxs-lookup"><span data-stu-id="18aa8-103">Checks for the existence of a Data Lake Analytics account.</span></span>

## <span data-ttu-id="18aa8-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="18aa8-104">SYNTAX</span></span>

```
Test-AzDataLakeAnalyticsAccount [-Name] <String> [[-ResourceGroupName] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="18aa8-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="18aa8-105">DESCRIPTION</span></span>
<span data-ttu-id="18aa8-106">Das **Cmdlet Test-AzDataLakeAnalyticsAccount** überprüft das Vorhandensein eines Data Lake Analytics-Kontos.</span><span class="sxs-lookup"><span data-stu-id="18aa8-106">The **Test-AzDataLakeAnalyticsAccount** cmdlet checks for the existence of a Data Lake Analytics account.</span></span>

## <span data-ttu-id="18aa8-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="18aa8-107">EXAMPLES</span></span>

### <span data-ttu-id="18aa8-108">Beispiel 1: Testen, ob ein Konto vorhanden ist</span><span class="sxs-lookup"><span data-stu-id="18aa8-108">Example 1: Test whether an account exists</span></span>
```
PS C:\>Test-AzDataLakeAnalyticsAccount -Name "ContosoAdlAccount"
```

<span data-ttu-id="18aa8-109">Mit diesem Befehl wird überprüft, ob das Konto "ContosoAdlAccount" vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="18aa8-109">This command tests whether the account named ContosoAdlAccount exists.</span></span>

## <span data-ttu-id="18aa8-110">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="18aa8-110">PARAMETERS</span></span>

### <span data-ttu-id="18aa8-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="18aa8-111">-DefaultProfile</span></span>
<span data-ttu-id="18aa8-112">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden</span><span class="sxs-lookup"><span data-stu-id="18aa8-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="18aa8-113">-Name</span><span class="sxs-lookup"><span data-stu-id="18aa8-113">-Name</span></span>
<span data-ttu-id="18aa8-114">Gibt den Namen des Data Lake Analytics-Kontos an.</span><span class="sxs-lookup"><span data-stu-id="18aa8-114">Specifies the Data Lake Analytics account name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="18aa8-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="18aa8-115">-ResourceGroupName</span></span>
<span data-ttu-id="18aa8-116">Gibt den Ressourcengruppennamen des Data Lake Analytics-Kontos an.</span><span class="sxs-lookup"><span data-stu-id="18aa8-116">Specifies the resource group name of the Data Lake Analytics account.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="18aa8-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="18aa8-117">CommonParameters</span></span>
<span data-ttu-id="18aa8-118">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="18aa8-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="18aa8-119">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="18aa8-119">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="18aa8-120">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="18aa8-120">INPUTS</span></span>

### <span data-ttu-id="18aa8-121">System.String</span><span class="sxs-lookup"><span data-stu-id="18aa8-121">System.String</span></span>

## <span data-ttu-id="18aa8-122">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="18aa8-122">OUTPUTS</span></span>

### <span data-ttu-id="18aa8-123">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="18aa8-123">System.Boolean</span></span>

## <span data-ttu-id="18aa8-124">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="18aa8-124">NOTES</span></span>

## <span data-ttu-id="18aa8-125">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="18aa8-125">RELATED LINKS</span></span>

[<span data-ttu-id="18aa8-126">Get-AzDataLakeAnalyticsAccount</span><span class="sxs-lookup"><span data-stu-id="18aa8-126">Get-AzDataLakeAnalyticsAccount</span></span>](./Get-AzDataLakeAnalyticsAccount.md)

[<span data-ttu-id="18aa8-127">New-AzDataLakeAnalyticsAccount</span><span class="sxs-lookup"><span data-stu-id="18aa8-127">New-AzDataLakeAnalyticsAccount</span></span>](./New-AzDataLakeAnalyticsAccount.md)

[<span data-ttu-id="18aa8-128">Set-AzDataLakeAnalyticsAccount</span><span class="sxs-lookup"><span data-stu-id="18aa8-128">Set-AzDataLakeAnalyticsAccount</span></span>](./Set-AzDataLakeAnalyticsAccount.md)


