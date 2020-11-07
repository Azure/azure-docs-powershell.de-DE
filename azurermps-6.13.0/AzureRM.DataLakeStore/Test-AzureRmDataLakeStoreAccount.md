---
external help file: Microsoft.Azure.Commands.DataLakeStore.dll-Help.xml
Module Name: AzureRM.DataLakeStore
ms.assetid: 613DE097-65E0-4F08-839D-F9B53F772382
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datalakestore/test-azurermdatalakestoreaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Test-AzureRmDataLakeStoreAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Test-AzureRmDataLakeStoreAccount.md
ms.openlocfilehash: b1b3a05b6f2d19ba350567c8793822d4129c5445
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93662178"
---
# <span data-ttu-id="a3099-101">Test-AzureRmDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="a3099-101">Test-AzureRmDataLakeStoreAccount</span></span>

## <span data-ttu-id="a3099-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="a3099-102">SYNOPSIS</span></span>
<span data-ttu-id="a3099-103">Testet das vorhanden sein eines Data Lake Store-Kontos.</span><span class="sxs-lookup"><span data-stu-id="a3099-103">Tests the existence of a Data Lake Store account.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a3099-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="a3099-104">SYNTAX</span></span>

```
Test-AzureRmDataLakeStoreAccount [-Name] <String> [[-ResourceGroupName] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a3099-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="a3099-105">DESCRIPTION</span></span>
<span data-ttu-id="a3099-106">Das Cmdlet **Test-AzureRmDataLakeStoreAccount** testet das vorhanden sein eines Data Lake Store-Kontos.</span><span class="sxs-lookup"><span data-stu-id="a3099-106">The **Test-AzureRmDataLakeStoreAccount** cmdlet tests the existence of a Data Lake Store account.</span></span>

## <span data-ttu-id="a3099-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="a3099-107">EXAMPLES</span></span>

### <span data-ttu-id="a3099-108">Beispiel 1: Testen eines Kontos</span><span class="sxs-lookup"><span data-stu-id="a3099-108">Example 1: Test an account</span></span>
```
PS C:\>Test-AzureRmDataLakeStoreAccount -Name "ContosoADL"
```

<span data-ttu-id="a3099-109">Dieser Befehl testet, ob das Konto mit dem Namen ContosoADL vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="a3099-109">This command tests whether the account named ContosoADL exists.</span></span>

## <span data-ttu-id="a3099-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="a3099-110">PARAMETERS</span></span>

### <span data-ttu-id="a3099-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a3099-111">-DefaultProfile</span></span>
<span data-ttu-id="a3099-112">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="a3099-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="a3099-113">-Name</span><span class="sxs-lookup"><span data-stu-id="a3099-113">-Name</span></span>
<span data-ttu-id="a3099-114">Gibt den Namen des Daten Lake Store-Kontos an, das getestet werden soll.</span><span class="sxs-lookup"><span data-stu-id="a3099-114">Specifies the name of the Data Lake Store account to test.</span></span>

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

### <span data-ttu-id="a3099-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a3099-115">-ResourceGroupName</span></span>
<span data-ttu-id="a3099-116">Gibt den Namen der Ressourcengruppe an, die das zu testende Konto enthält.</span><span class="sxs-lookup"><span data-stu-id="a3099-116">Specifies the name of the resource group that contains the account to test.</span></span>

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

### <span data-ttu-id="a3099-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a3099-117">CommonParameters</span></span>
<span data-ttu-id="a3099-118">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a3099-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a3099-119">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a3099-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a3099-120">Eingaben</span><span class="sxs-lookup"><span data-stu-id="a3099-120">INPUTS</span></span>

### <span data-ttu-id="a3099-121">System. String</span><span class="sxs-lookup"><span data-stu-id="a3099-121">System.String</span></span>

## <span data-ttu-id="a3099-122">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="a3099-122">OUTPUTS</span></span>

### <span data-ttu-id="a3099-123">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="a3099-123">System.Boolean</span></span>

## <span data-ttu-id="a3099-124">Notizen</span><span class="sxs-lookup"><span data-stu-id="a3099-124">NOTES</span></span>

## <span data-ttu-id="a3099-125">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="a3099-125">RELATED LINKS</span></span>

[<span data-ttu-id="a3099-126">Get-AzureRmDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="a3099-126">Get-AzureRmDataLakeStoreAccount</span></span>](./Get-AzureRmDataLakeStoreAccount.md)

[<span data-ttu-id="a3099-127">Neu – AzureRmDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="a3099-127">New-AzureRmDataLakeStoreAccount</span></span>](./New-AzureRmDataLakeStoreAccount.md)

[<span data-ttu-id="a3099-128">Remove-AzureRmDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="a3099-128">Remove-AzureRmDataLakeStoreAccount</span></span>](./Remove-AzureRmDataLakeStoreAccount.md)

[<span data-ttu-id="a3099-129">Satz-AzureRmDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="a3099-129">Set-AzureRmDataLakeStoreAccount</span></span>](./Set-AzureRmDataLakeStoreAccount.md)


