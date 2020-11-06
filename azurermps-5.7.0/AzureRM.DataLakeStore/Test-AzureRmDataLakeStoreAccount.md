---
external help file: Microsoft.Azure.Commands.DataLakeStore.dll-Help.xml
Module Name: AzureRM.DataLakeStore
ms.assetid: 613DE097-65E0-4F08-839D-F9B53F772382
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datalakestore/test-azurermdatalakestoreaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Test-AzureRmDataLakeStoreAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Test-AzureRmDataLakeStoreAccount.md
ms.openlocfilehash: 15c0614094ed28a9888e2e39a6cfb81547fbb6e9
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93502617"
---
# <span data-ttu-id="7ffbe-101">Test-AzureRmDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="7ffbe-101">Test-AzureRmDataLakeStoreAccount</span></span>

## <span data-ttu-id="7ffbe-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="7ffbe-102">SYNOPSIS</span></span>
<span data-ttu-id="7ffbe-103">Testet das vorhanden sein eines Data Lake Store-Kontos.</span><span class="sxs-lookup"><span data-stu-id="7ffbe-103">Tests the existence of a Data Lake Store account.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="7ffbe-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="7ffbe-104">SYNTAX</span></span>

```
Test-AzureRmDataLakeStoreAccount [-Name] <String> [[-ResourceGroupName] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="7ffbe-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="7ffbe-105">DESCRIPTION</span></span>
<span data-ttu-id="7ffbe-106">Das Cmdlet **Test-AzureRmDataLakeStoreAccount** testet das vorhanden sein eines Data Lake Store-Kontos.</span><span class="sxs-lookup"><span data-stu-id="7ffbe-106">The **Test-AzureRmDataLakeStoreAccount** cmdlet tests the existence of a Data Lake Store account.</span></span>

## <span data-ttu-id="7ffbe-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="7ffbe-107">EXAMPLES</span></span>

### <span data-ttu-id="7ffbe-108">Beispiel 1: Testen eines Kontos</span><span class="sxs-lookup"><span data-stu-id="7ffbe-108">Example 1: Test an account</span></span>
```
PS C:\>Test-AzureRmDataLakeStoreAccount -Name "ContosoADL"
```

<span data-ttu-id="7ffbe-109">Dieser Befehl testet, ob das Konto mit dem Namen ContosoADL vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="7ffbe-109">This command tests whether the account named ContosoADL exists.</span></span>

## <span data-ttu-id="7ffbe-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="7ffbe-110">PARAMETERS</span></span>

### <span data-ttu-id="7ffbe-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7ffbe-111">-DefaultProfile</span></span>
<span data-ttu-id="7ffbe-112">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="7ffbe-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="7ffbe-113">-Name</span><span class="sxs-lookup"><span data-stu-id="7ffbe-113">-Name</span></span>
<span data-ttu-id="7ffbe-114">Gibt den Namen des Daten Lake Store-Kontos an, das getestet werden soll.</span><span class="sxs-lookup"><span data-stu-id="7ffbe-114">Specifies the name of the Data Lake Store account to test.</span></span>

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

### <span data-ttu-id="7ffbe-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7ffbe-115">-ResourceGroupName</span></span>
<span data-ttu-id="7ffbe-116">Gibt den Namen der Ressourcengruppe an, die das zu testende Konto enthält.</span><span class="sxs-lookup"><span data-stu-id="7ffbe-116">Specifies the name of the resource group that contains the account to test.</span></span>

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

### <span data-ttu-id="7ffbe-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7ffbe-117">CommonParameters</span></span>
<span data-ttu-id="7ffbe-118">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7ffbe-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7ffbe-119">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7ffbe-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7ffbe-120">Eingaben</span><span class="sxs-lookup"><span data-stu-id="7ffbe-120">INPUTS</span></span>

### <span data-ttu-id="7ffbe-121">Keine</span><span class="sxs-lookup"><span data-stu-id="7ffbe-121">None</span></span>
<span data-ttu-id="7ffbe-122">Dieses Cmdlet akzeptiert keine Eingaben.</span><span class="sxs-lookup"><span data-stu-id="7ffbe-122">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="7ffbe-123">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="7ffbe-123">OUTPUTS</span></span>

### <span data-ttu-id="7ffbe-124">bool</span><span class="sxs-lookup"><span data-stu-id="7ffbe-124">bool</span></span>
<span data-ttu-id="7ffbe-125">"Wahr" oder "falsch" gibt an, dass das angegebene Konto vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="7ffbe-125">True or false indicating the existence of the specified account.</span></span>

## <span data-ttu-id="7ffbe-126">Notizen</span><span class="sxs-lookup"><span data-stu-id="7ffbe-126">NOTES</span></span>

## <span data-ttu-id="7ffbe-127">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="7ffbe-127">RELATED LINKS</span></span>

[<span data-ttu-id="7ffbe-128">Get-AzureRmDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="7ffbe-128">Get-AzureRmDataLakeStoreAccount</span></span>](./Get-AzureRmDataLakeStoreAccount.md)

[<span data-ttu-id="7ffbe-129">Neu – AzureRmDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="7ffbe-129">New-AzureRmDataLakeStoreAccount</span></span>](./New-AzureRmDataLakeStoreAccount.md)

[<span data-ttu-id="7ffbe-130">Remove-AzureRmDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="7ffbe-130">Remove-AzureRmDataLakeStoreAccount</span></span>](./Remove-AzureRmDataLakeStoreAccount.md)

[<span data-ttu-id="7ffbe-131">Satz-AzureRmDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="7ffbe-131">Set-AzureRmDataLakeStoreAccount</span></span>](./Set-AzureRmDataLakeStoreAccount.md)


