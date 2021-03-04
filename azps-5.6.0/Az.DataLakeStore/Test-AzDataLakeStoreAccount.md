---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeStore.dll-Help.xml
Module Name: Az.DataLakeStore
ms.assetid: 613DE097-65E0-4F08-839D-F9B53F772382
online version: https://docs.microsoft.com/powershell/module/az.datalakestore/test-azdatalakestoreaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Test-AzDataLakeStoreAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Test-AzDataLakeStoreAccount.md
ms.openlocfilehash: 8bc8a09add012cb0f190922777e2e9e7fcc46feb
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101941203"
---
# <span data-ttu-id="bbcb0-101">Test-AzDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="bbcb0-101">Test-AzDataLakeStoreAccount</span></span>

## <span data-ttu-id="bbcb0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="bbcb0-102">SYNOPSIS</span></span>
<span data-ttu-id="bbcb0-103">Testet das Vorhandensein eines Data Lake Store-Kontos.</span><span class="sxs-lookup"><span data-stu-id="bbcb0-103">Tests the existence of a Data Lake Store account.</span></span>

## <span data-ttu-id="bbcb0-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="bbcb0-104">SYNTAX</span></span>

```
Test-AzDataLakeStoreAccount [-Name] <String> [[-ResourceGroupName] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="bbcb0-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="bbcb0-105">DESCRIPTION</span></span>
<span data-ttu-id="bbcb0-106">Das **Test-AzDataLakeStoreAccount-Cmdlet** testet das Vorhandensein eines Data Lake Store-Kontos.</span><span class="sxs-lookup"><span data-stu-id="bbcb0-106">The **Test-AzDataLakeStoreAccount** cmdlet tests the existence of a Data Lake Store account.</span></span>

## <span data-ttu-id="bbcb0-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="bbcb0-107">EXAMPLES</span></span>

### <span data-ttu-id="bbcb0-108">Beispiel 1: Testen eines Kontos</span><span class="sxs-lookup"><span data-stu-id="bbcb0-108">Example 1: Test an account</span></span>
```
PS C:\>Test-AzDataLakeStoreAccount -Name "ContosoADL"
```

<span data-ttu-id="bbcb0-109">Mit diesem Befehl wird überprüft, ob das Konto mit dem Namen ContosoADL vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="bbcb0-109">This command tests whether the account named ContosoADL exists.</span></span>

## <span data-ttu-id="bbcb0-110">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="bbcb0-110">PARAMETERS</span></span>

### <span data-ttu-id="bbcb0-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bbcb0-111">-DefaultProfile</span></span>
<span data-ttu-id="bbcb0-112">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden</span><span class="sxs-lookup"><span data-stu-id="bbcb0-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="bbcb0-113">-Name</span><span class="sxs-lookup"><span data-stu-id="bbcb0-113">-Name</span></span>
<span data-ttu-id="bbcb0-114">Gibt den Namen des zu testenden Data Lake Store-Kontos an.</span><span class="sxs-lookup"><span data-stu-id="bbcb0-114">Specifies the name of the Data Lake Store account to test.</span></span>

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

### <span data-ttu-id="bbcb0-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bbcb0-115">-ResourceGroupName</span></span>
<span data-ttu-id="bbcb0-116">Gibt den Namen der Ressourcengruppe an, die das zu testende Konto enthält.</span><span class="sxs-lookup"><span data-stu-id="bbcb0-116">Specifies the name of the resource group that contains the account to test.</span></span>

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

### <span data-ttu-id="bbcb0-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bbcb0-117">CommonParameters</span></span>
<span data-ttu-id="bbcb0-118">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bbcb0-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bbcb0-119">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bbcb0-119">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bbcb0-120">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="bbcb0-120">INPUTS</span></span>

### <span data-ttu-id="bbcb0-121">System.String</span><span class="sxs-lookup"><span data-stu-id="bbcb0-121">System.String</span></span>

## <span data-ttu-id="bbcb0-122">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="bbcb0-122">OUTPUTS</span></span>

### <span data-ttu-id="bbcb0-123">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="bbcb0-123">System.Boolean</span></span>

## <span data-ttu-id="bbcb0-124">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="bbcb0-124">NOTES</span></span>

## <span data-ttu-id="bbcb0-125">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="bbcb0-125">RELATED LINKS</span></span>

[<span data-ttu-id="bbcb0-126">Get-AzDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="bbcb0-126">Get-AzDataLakeStoreAccount</span></span>](./Get-AzDataLakeStoreAccount.md)

[<span data-ttu-id="bbcb0-127">New-AzDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="bbcb0-127">New-AzDataLakeStoreAccount</span></span>](./New-AzDataLakeStoreAccount.md)

[<span data-ttu-id="bbcb0-128">Remove-AzDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="bbcb0-128">Remove-AzDataLakeStoreAccount</span></span>](./Remove-AzDataLakeStoreAccount.md)

[<span data-ttu-id="bbcb0-129">Set-AzDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="bbcb0-129">Set-AzDataLakeStoreAccount</span></span>](./Set-AzDataLakeStoreAccount.md)


