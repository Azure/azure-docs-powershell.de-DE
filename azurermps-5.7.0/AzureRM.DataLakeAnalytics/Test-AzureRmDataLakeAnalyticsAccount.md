---
external help file: Microsoft.Azure.Commands.DataLakeAnalytics.dll-Help.xml
Module Name: AzureRM.DataLakeAnalytics
ms.assetid: 0B52890D-102F-4C3C-9EF9-017F6ECA3E26
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datalakeanalytics/test-azurermdatalakeanalyticsaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeAnalytics/Commands.DataLakeAnalytics/help/Test-AzureRmDataLakeAnalyticsAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeAnalytics/Commands.DataLakeAnalytics/help/Test-AzureRmDataLakeAnalyticsAccount.md
ms.openlocfilehash: a6e147d64a1dea77febc833b5c46e78d070f3ba5
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93478505"
---
# <span data-ttu-id="4a23f-101">Test-AzureRmDataLakeAnalyticsAccount</span><span class="sxs-lookup"><span data-stu-id="4a23f-101">Test-AzureRmDataLakeAnalyticsAccount</span></span>

## <span data-ttu-id="4a23f-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="4a23f-102">SYNOPSIS</span></span>
<span data-ttu-id="4a23f-103">Überprüft, ob ein Data Lake Analytics-Konto vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="4a23f-103">Checks for the existence of a Data Lake Analytics account.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="4a23f-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="4a23f-104">SYNTAX</span></span>

```
Test-AzureRmDataLakeAnalyticsAccount [-Name] <String> [[-ResourceGroupName] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="4a23f-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="4a23f-105">DESCRIPTION</span></span>
<span data-ttu-id="4a23f-106">Das Cmdlet **Test-AzureRmDataLakeAnalyticsAccount** überprüft, ob ein Data Lake Analytics-Konto vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="4a23f-106">The **Test-AzureRmDataLakeAnalyticsAccount** cmdlet checks for the existence of a Data Lake Analytics account.</span></span>

## <span data-ttu-id="4a23f-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="4a23f-107">EXAMPLES</span></span>

### <span data-ttu-id="4a23f-108">Beispiel 1: testen, ob ein Konto vorhanden ist</span><span class="sxs-lookup"><span data-stu-id="4a23f-108">Example 1: Test whether an account exists</span></span>
```
PS C:\>Test-AzureRmDataLakeAnalyticsAccount -Name "ContosoAdlAccount"
```

<span data-ttu-id="4a23f-109">Dieser Befehl testet, ob das Konto mit dem Namen ContosoAdlAccount vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="4a23f-109">This command tests whether the account named ContosoAdlAccount exists.</span></span>

## <span data-ttu-id="4a23f-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="4a23f-110">PARAMETERS</span></span>

### <span data-ttu-id="4a23f-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4a23f-111">-DefaultProfile</span></span>
<span data-ttu-id="4a23f-112">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="4a23f-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="4a23f-113">-Name</span><span class="sxs-lookup"><span data-stu-id="4a23f-113">-Name</span></span>
<span data-ttu-id="4a23f-114">Gibt den Namen des Daten Lake Analytics-Kontos an.</span><span class="sxs-lookup"><span data-stu-id="4a23f-114">Specifies the Data Lake Analytics account name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4a23f-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4a23f-115">-ResourceGroupName</span></span>
<span data-ttu-id="4a23f-116">Gibt den Ressourcengruppennamen des Data Lake Analytics-Kontos an.</span><span class="sxs-lookup"><span data-stu-id="4a23f-116">Specifies the resource group name of the Data Lake Analytics account.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4a23f-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4a23f-117">CommonParameters</span></span>
<span data-ttu-id="4a23f-118">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4a23f-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4a23f-119">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4a23f-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4a23f-120">Eingaben</span><span class="sxs-lookup"><span data-stu-id="4a23f-120">INPUTS</span></span>

### <span data-ttu-id="4a23f-121">Keine</span><span class="sxs-lookup"><span data-stu-id="4a23f-121">None</span></span>
<span data-ttu-id="4a23f-122">Dieses Cmdlet akzeptiert keine Eingaben.</span><span class="sxs-lookup"><span data-stu-id="4a23f-122">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="4a23f-123">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="4a23f-123">OUTPUTS</span></span>

### <span data-ttu-id="4a23f-124">bool</span><span class="sxs-lookup"><span data-stu-id="4a23f-124">bool</span></span>
<span data-ttu-id="4a23f-125">"Wahr" oder "falsch" gibt an, ob das Konto vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="4a23f-125">True or false indicating whether the account exists or not.</span></span>

## <span data-ttu-id="4a23f-126">Notizen</span><span class="sxs-lookup"><span data-stu-id="4a23f-126">NOTES</span></span>

## <span data-ttu-id="4a23f-127">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="4a23f-127">RELATED LINKS</span></span>

[<span data-ttu-id="4a23f-128">Get-AzureRmDataLakeAnalyticsAccount</span><span class="sxs-lookup"><span data-stu-id="4a23f-128">Get-AzureRmDataLakeAnalyticsAccount</span></span>](./Get-AzureRmDataLakeAnalyticsAccount.md)

[<span data-ttu-id="4a23f-129">Neu – AzureRmDataLakeAnalyticsAccount</span><span class="sxs-lookup"><span data-stu-id="4a23f-129">New-AzureRmDataLakeAnalyticsAccount</span></span>](./New-AzureRmDataLakeAnalyticsAccount.md)

[<span data-ttu-id="4a23f-130">Satz-AzureRmDataLakeAnalyticsAccount</span><span class="sxs-lookup"><span data-stu-id="4a23f-130">Set-AzureRmDataLakeAnalyticsAccount</span></span>](./Set-AzureRmDataLakeAnalyticsAccount.md)


