---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeStore.dll-Help.xml
Module Name: Az.DataLakeStore
ms.assetid: 613DE097-65E0-4F08-839D-F9B53F772382
online version: https://docs.microsoft.com/en-us/powershell/module/az.datalakestore/test-azdatalakestoreaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Test-AzDataLakeStoreAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Test-AzDataLakeStoreAccount.md
ms.openlocfilehash: 25837486fad8b17a272f5687129ff936f6d50a02
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98372811"
---
# <span data-ttu-id="5db29-101">Test-AzDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="5db29-101">Test-AzDataLakeStoreAccount</span></span>

## <span data-ttu-id="5db29-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5db29-102">SYNOPSIS</span></span>
<span data-ttu-id="5db29-103">Überprüft das Vorhandensein eines Data Lake Store-Kontos.</span><span class="sxs-lookup"><span data-stu-id="5db29-103">Tests the existence of a Data Lake Store account.</span></span>

## <span data-ttu-id="5db29-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="5db29-104">SYNTAX</span></span>

```
Test-AzDataLakeStoreAccount [-Name] <String> [[-ResourceGroupName] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="5db29-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="5db29-105">DESCRIPTION</span></span>
<span data-ttu-id="5db29-106">Das **Cmdlet "Test-AzDataLakeStoreAccount"** überprüft das Vorhandensein eines Data Lake Store-Kontos.</span><span class="sxs-lookup"><span data-stu-id="5db29-106">The **Test-AzDataLakeStoreAccount** cmdlet tests the existence of a Data Lake Store account.</span></span>

## <span data-ttu-id="5db29-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="5db29-107">EXAMPLES</span></span>

### <span data-ttu-id="5db29-108">Beispiel 1: Testen eines Kontos</span><span class="sxs-lookup"><span data-stu-id="5db29-108">Example 1: Test an account</span></span>
```
PS C:\>Test-AzDataLakeStoreAccount -Name "ContosoADL"
```

<span data-ttu-id="5db29-109">Mit diesem Befehl wird überprüft, ob das Konto "ContosoADL" vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="5db29-109">This command tests whether the account named ContosoADL exists.</span></span>

## <span data-ttu-id="5db29-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="5db29-110">PARAMETERS</span></span>

### <span data-ttu-id="5db29-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5db29-111">-DefaultProfile</span></span>
<span data-ttu-id="5db29-112">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden</span><span class="sxs-lookup"><span data-stu-id="5db29-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="5db29-113">-Name</span><span class="sxs-lookup"><span data-stu-id="5db29-113">-Name</span></span>
<span data-ttu-id="5db29-114">Gibt den Namen des zu testden Data Lake Store-Kontos an.</span><span class="sxs-lookup"><span data-stu-id="5db29-114">Specifies the name of the Data Lake Store account to test.</span></span>

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

### <span data-ttu-id="5db29-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5db29-115">-ResourceGroupName</span></span>
<span data-ttu-id="5db29-116">Gibt den Namen der Ressourcengruppe an, die das zu testde Konto enthält.</span><span class="sxs-lookup"><span data-stu-id="5db29-116">Specifies the name of the resource group that contains the account to test.</span></span>

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

### <span data-ttu-id="5db29-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5db29-117">CommonParameters</span></span>
<span data-ttu-id="5db29-118">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5db29-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5db29-119">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5db29-119">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5db29-120">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="5db29-120">INPUTS</span></span>

### <span data-ttu-id="5db29-121">System.String</span><span class="sxs-lookup"><span data-stu-id="5db29-121">System.String</span></span>

## <span data-ttu-id="5db29-122">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="5db29-122">OUTPUTS</span></span>

### <span data-ttu-id="5db29-123">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="5db29-123">System.Boolean</span></span>

## <span data-ttu-id="5db29-124">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="5db29-124">NOTES</span></span>

## <span data-ttu-id="5db29-125">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="5db29-125">RELATED LINKS</span></span>

[<span data-ttu-id="5db29-126">Get-AzDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="5db29-126">Get-AzDataLakeStoreAccount</span></span>](./Get-AzDataLakeStoreAccount.md)

[<span data-ttu-id="5db29-127">New-AzDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="5db29-127">New-AzDataLakeStoreAccount</span></span>](./New-AzDataLakeStoreAccount.md)

[<span data-ttu-id="5db29-128">Remove-AzDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="5db29-128">Remove-AzDataLakeStoreAccount</span></span>](./Remove-AzDataLakeStoreAccount.md)

[<span data-ttu-id="5db29-129">Set-AzDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="5db29-129">Set-AzDataLakeStoreAccount</span></span>](./Set-AzDataLakeStoreAccount.md)


