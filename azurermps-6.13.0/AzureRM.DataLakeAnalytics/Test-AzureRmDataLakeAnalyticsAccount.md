---
external help file: Microsoft.Azure.Commands.DataLakeAnalytics.dll-Help.xml
Module Name: AzureRM.DataLakeAnalytics
ms.assetid: 0B52890D-102F-4C3C-9EF9-017F6ECA3E26
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datalakeanalytics/test-azurermdatalakeanalyticsaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeAnalytics/Commands.DataLakeAnalytics/help/Test-AzureRmDataLakeAnalyticsAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeAnalytics/Commands.DataLakeAnalytics/help/Test-AzureRmDataLakeAnalyticsAccount.md
ms.openlocfilehash: e527501424edfbbc12693b47b5858c3c46592402
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93663167"
---
# <span data-ttu-id="272ee-101">Test-AzureRmDataLakeAnalyticsAccount</span><span class="sxs-lookup"><span data-stu-id="272ee-101">Test-AzureRmDataLakeAnalyticsAccount</span></span>

## <span data-ttu-id="272ee-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="272ee-102">SYNOPSIS</span></span>
<span data-ttu-id="272ee-103">Überprüft, ob ein Data Lake Analytics-Konto vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="272ee-103">Checks for the existence of a Data Lake Analytics account.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="272ee-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="272ee-104">SYNTAX</span></span>

```
Test-AzureRmDataLakeAnalyticsAccount [-Name] <String> [[-ResourceGroupName] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="272ee-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="272ee-105">DESCRIPTION</span></span>
<span data-ttu-id="272ee-106">Das Cmdlet **Test-AzureRmDataLakeAnalyticsAccount** überprüft, ob ein Data Lake Analytics-Konto vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="272ee-106">The **Test-AzureRmDataLakeAnalyticsAccount** cmdlet checks for the existence of a Data Lake Analytics account.</span></span>

## <span data-ttu-id="272ee-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="272ee-107">EXAMPLES</span></span>

### <span data-ttu-id="272ee-108">Beispiel 1: testen, ob ein Konto vorhanden ist</span><span class="sxs-lookup"><span data-stu-id="272ee-108">Example 1: Test whether an account exists</span></span>
```
PS C:\>Test-AzureRmDataLakeAnalyticsAccount -Name "ContosoAdlAccount"
```

<span data-ttu-id="272ee-109">Dieser Befehl testet, ob das Konto mit dem Namen ContosoAdlAccount vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="272ee-109">This command tests whether the account named ContosoAdlAccount exists.</span></span>

## <span data-ttu-id="272ee-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="272ee-110">PARAMETERS</span></span>

### <span data-ttu-id="272ee-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="272ee-111">-DefaultProfile</span></span>
<span data-ttu-id="272ee-112">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="272ee-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="272ee-113">-Name</span><span class="sxs-lookup"><span data-stu-id="272ee-113">-Name</span></span>
<span data-ttu-id="272ee-114">Gibt den Namen des Daten Lake Analytics-Kontos an.</span><span class="sxs-lookup"><span data-stu-id="272ee-114">Specifies the Data Lake Analytics account name.</span></span>

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

### <span data-ttu-id="272ee-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="272ee-115">-ResourceGroupName</span></span>
<span data-ttu-id="272ee-116">Gibt den Ressourcengruppennamen des Data Lake Analytics-Kontos an.</span><span class="sxs-lookup"><span data-stu-id="272ee-116">Specifies the resource group name of the Data Lake Analytics account.</span></span>

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

### <span data-ttu-id="272ee-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="272ee-117">CommonParameters</span></span>
<span data-ttu-id="272ee-118">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="272ee-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="272ee-119">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="272ee-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="272ee-120">Eingaben</span><span class="sxs-lookup"><span data-stu-id="272ee-120">INPUTS</span></span>

### <span data-ttu-id="272ee-121">System. String</span><span class="sxs-lookup"><span data-stu-id="272ee-121">System.String</span></span>

## <span data-ttu-id="272ee-122">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="272ee-122">OUTPUTS</span></span>

### <span data-ttu-id="272ee-123">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="272ee-123">System.Boolean</span></span>

## <span data-ttu-id="272ee-124">Notizen</span><span class="sxs-lookup"><span data-stu-id="272ee-124">NOTES</span></span>

## <span data-ttu-id="272ee-125">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="272ee-125">RELATED LINKS</span></span>

[<span data-ttu-id="272ee-126">Get-AzureRmDataLakeAnalyticsAccount</span><span class="sxs-lookup"><span data-stu-id="272ee-126">Get-AzureRmDataLakeAnalyticsAccount</span></span>](./Get-AzureRmDataLakeAnalyticsAccount.md)

[<span data-ttu-id="272ee-127">Neu – AzureRmDataLakeAnalyticsAccount</span><span class="sxs-lookup"><span data-stu-id="272ee-127">New-AzureRmDataLakeAnalyticsAccount</span></span>](./New-AzureRmDataLakeAnalyticsAccount.md)

[<span data-ttu-id="272ee-128">Satz-AzureRmDataLakeAnalyticsAccount</span><span class="sxs-lookup"><span data-stu-id="272ee-128">Set-AzureRmDataLakeAnalyticsAccount</span></span>](./Set-AzureRmDataLakeAnalyticsAccount.md)


