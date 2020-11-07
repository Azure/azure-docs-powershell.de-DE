---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeAnalytics.dll-Help.xml
Module Name: Az.DataLakeAnalytics
ms.assetid: 0B52890D-102F-4C3C-9EF9-017F6ECA3E26
online version: https://docs.microsoft.com/en-us/powershell/module/az.datalakeanalytics/test-azdatalakeanalyticsaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeAnalytics/DataLakeAnalytics/help/Test-AzDataLakeAnalyticsAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeAnalytics/DataLakeAnalytics/help/Test-AzDataLakeAnalyticsAccount.md
ms.openlocfilehash: 77247853fe6412b0d01fb01c71e592efca12063d
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93820231"
---
# <span data-ttu-id="31c76-101">Test-AzDataLakeAnalyticsAccount</span><span class="sxs-lookup"><span data-stu-id="31c76-101">Test-AzDataLakeAnalyticsAccount</span></span>

## <span data-ttu-id="31c76-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="31c76-102">SYNOPSIS</span></span>
<span data-ttu-id="31c76-103">Überprüft, ob ein Data Lake Analytics-Konto vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="31c76-103">Checks for the existence of a Data Lake Analytics account.</span></span>

## <span data-ttu-id="31c76-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="31c76-104">SYNTAX</span></span>

```
Test-AzDataLakeAnalyticsAccount [-Name] <String> [[-ResourceGroupName] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="31c76-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="31c76-105">DESCRIPTION</span></span>
<span data-ttu-id="31c76-106">Das Cmdlet **Test-AzDataLakeAnalyticsAccount** überprüft, ob ein Data Lake Analytics-Konto vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="31c76-106">The **Test-AzDataLakeAnalyticsAccount** cmdlet checks for the existence of a Data Lake Analytics account.</span></span>

## <span data-ttu-id="31c76-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="31c76-107">EXAMPLES</span></span>

### <span data-ttu-id="31c76-108">Beispiel 1: testen, ob ein Konto vorhanden ist</span><span class="sxs-lookup"><span data-stu-id="31c76-108">Example 1: Test whether an account exists</span></span>
```
PS C:\>Test-AzDataLakeAnalyticsAccount -Name "ContosoAdlAccount"
```

<span data-ttu-id="31c76-109">Dieser Befehl testet, ob das Konto mit dem Namen ContosoAdlAccount vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="31c76-109">This command tests whether the account named ContosoAdlAccount exists.</span></span>

## <span data-ttu-id="31c76-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="31c76-110">PARAMETERS</span></span>

### <span data-ttu-id="31c76-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="31c76-111">-DefaultProfile</span></span>
<span data-ttu-id="31c76-112">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="31c76-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="31c76-113">-Name</span><span class="sxs-lookup"><span data-stu-id="31c76-113">-Name</span></span>
<span data-ttu-id="31c76-114">Gibt den Namen des Daten Lake Analytics-Kontos an.</span><span class="sxs-lookup"><span data-stu-id="31c76-114">Specifies the Data Lake Analytics account name.</span></span>

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

### <span data-ttu-id="31c76-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="31c76-115">-ResourceGroupName</span></span>
<span data-ttu-id="31c76-116">Gibt den Ressourcengruppennamen des Data Lake Analytics-Kontos an.</span><span class="sxs-lookup"><span data-stu-id="31c76-116">Specifies the resource group name of the Data Lake Analytics account.</span></span>

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

### <span data-ttu-id="31c76-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="31c76-117">CommonParameters</span></span>
<span data-ttu-id="31c76-118">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="31c76-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="31c76-119">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="31c76-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="31c76-120">Eingaben</span><span class="sxs-lookup"><span data-stu-id="31c76-120">INPUTS</span></span>

### <span data-ttu-id="31c76-121">System. String</span><span class="sxs-lookup"><span data-stu-id="31c76-121">System.String</span></span>

## <span data-ttu-id="31c76-122">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="31c76-122">OUTPUTS</span></span>

### <span data-ttu-id="31c76-123">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="31c76-123">System.Boolean</span></span>

## <span data-ttu-id="31c76-124">Notizen</span><span class="sxs-lookup"><span data-stu-id="31c76-124">NOTES</span></span>

## <span data-ttu-id="31c76-125">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="31c76-125">RELATED LINKS</span></span>

[<span data-ttu-id="31c76-126">Get-AzDataLakeAnalyticsAccount</span><span class="sxs-lookup"><span data-stu-id="31c76-126">Get-AzDataLakeAnalyticsAccount</span></span>](./Get-AzDataLakeAnalyticsAccount.md)

[<span data-ttu-id="31c76-127">Neu – AzDataLakeAnalyticsAccount</span><span class="sxs-lookup"><span data-stu-id="31c76-127">New-AzDataLakeAnalyticsAccount</span></span>](./New-AzDataLakeAnalyticsAccount.md)

[<span data-ttu-id="31c76-128">Satz-AzDataLakeAnalyticsAccount</span><span class="sxs-lookup"><span data-stu-id="31c76-128">Set-AzDataLakeAnalyticsAccount</span></span>](./Set-AzDataLakeAnalyticsAccount.md)


