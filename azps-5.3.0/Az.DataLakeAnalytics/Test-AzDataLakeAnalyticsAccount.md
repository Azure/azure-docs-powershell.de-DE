---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeAnalytics.dll-Help.xml
Module Name: Az.DataLakeAnalytics
ms.assetid: 0B52890D-102F-4C3C-9EF9-017F6ECA3E26
online version: https://docs.microsoft.com/en-us/powershell/module/az.datalakeanalytics/test-azdatalakeanalyticsaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeAnalytics/DataLakeAnalytics/help/Test-AzDataLakeAnalyticsAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeAnalytics/DataLakeAnalytics/help/Test-AzDataLakeAnalyticsAccount.md
ms.openlocfilehash: 0f0cad155cdb274596aba449e26e82b94ca56aae
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98470509"
---
# <span data-ttu-id="850c6-101">Test-AzDataLakeAnalyticsAccount</span><span class="sxs-lookup"><span data-stu-id="850c6-101">Test-AzDataLakeAnalyticsAccount</span></span>

## <span data-ttu-id="850c6-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="850c6-102">SYNOPSIS</span></span>
<span data-ttu-id="850c6-103">Sucht nach dem Vorhandensein eines Data Lake Analytics-Kontos.</span><span class="sxs-lookup"><span data-stu-id="850c6-103">Checks for the existence of a Data Lake Analytics account.</span></span>

## <span data-ttu-id="850c6-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="850c6-104">SYNTAX</span></span>

```
Test-AzDataLakeAnalyticsAccount [-Name] <String> [[-ResourceGroupName] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="850c6-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="850c6-105">DESCRIPTION</span></span>
<span data-ttu-id="850c6-106">Das **Cmdlet "Test-AzDataLakeAnalyticsAccount"** sucht nach dem Vorhandensein eines Data Lake Analytics-Kontos.</span><span class="sxs-lookup"><span data-stu-id="850c6-106">The **Test-AzDataLakeAnalyticsAccount** cmdlet checks for the existence of a Data Lake Analytics account.</span></span>

## <span data-ttu-id="850c6-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="850c6-107">EXAMPLES</span></span>

### <span data-ttu-id="850c6-108">Beispiel 1: Testen, ob ein Konto vorhanden ist</span><span class="sxs-lookup"><span data-stu-id="850c6-108">Example 1: Test whether an account exists</span></span>
```
PS C:\>Test-AzDataLakeAnalyticsAccount -Name "ContosoAdlAccount"
```

<span data-ttu-id="850c6-109">Mit diesem Befehl wird überprüft, ob das Konto "ContosoAdlAccount" vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="850c6-109">This command tests whether the account named ContosoAdlAccount exists.</span></span>

## <span data-ttu-id="850c6-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="850c6-110">PARAMETERS</span></span>

### <span data-ttu-id="850c6-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="850c6-111">-DefaultProfile</span></span>
<span data-ttu-id="850c6-112">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden</span><span class="sxs-lookup"><span data-stu-id="850c6-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="850c6-113">-Name</span><span class="sxs-lookup"><span data-stu-id="850c6-113">-Name</span></span>
<span data-ttu-id="850c6-114">Gibt den Namen des Data Lake Analytics-Kontos an.</span><span class="sxs-lookup"><span data-stu-id="850c6-114">Specifies the Data Lake Analytics account name.</span></span>

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

### <span data-ttu-id="850c6-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="850c6-115">-ResourceGroupName</span></span>
<span data-ttu-id="850c6-116">Gibt den Ressourcengruppennamen des Data Lake Analytics-Kontos an.</span><span class="sxs-lookup"><span data-stu-id="850c6-116">Specifies the resource group name of the Data Lake Analytics account.</span></span>

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

### <span data-ttu-id="850c6-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="850c6-117">CommonParameters</span></span>
<span data-ttu-id="850c6-118">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="850c6-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="850c6-119">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="850c6-119">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="850c6-120">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="850c6-120">INPUTS</span></span>

### <span data-ttu-id="850c6-121">System.String</span><span class="sxs-lookup"><span data-stu-id="850c6-121">System.String</span></span>

## <span data-ttu-id="850c6-122">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="850c6-122">OUTPUTS</span></span>

### <span data-ttu-id="850c6-123">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="850c6-123">System.Boolean</span></span>

## <span data-ttu-id="850c6-124">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="850c6-124">NOTES</span></span>

## <span data-ttu-id="850c6-125">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="850c6-125">RELATED LINKS</span></span>

[<span data-ttu-id="850c6-126">Get-AzDataLakeAnalyticsAccount</span><span class="sxs-lookup"><span data-stu-id="850c6-126">Get-AzDataLakeAnalyticsAccount</span></span>](./Get-AzDataLakeAnalyticsAccount.md)

[<span data-ttu-id="850c6-127">New-AzDataLakeAnalyticsAccount</span><span class="sxs-lookup"><span data-stu-id="850c6-127">New-AzDataLakeAnalyticsAccount</span></span>](./New-AzDataLakeAnalyticsAccount.md)

[<span data-ttu-id="850c6-128">Set-AzDataLakeAnalyticsAccount</span><span class="sxs-lookup"><span data-stu-id="850c6-128">Set-AzDataLakeAnalyticsAccount</span></span>](./Set-AzDataLakeAnalyticsAccount.md)


