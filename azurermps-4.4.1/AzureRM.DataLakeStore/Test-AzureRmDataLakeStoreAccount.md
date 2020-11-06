---
external help file: Microsoft.Azure.Commands.DataLakeStore.dll-Help.xml
Module Name: AzureRM.DataLakeStore
ms.assetid: 613DE097-65E0-4F08-839D-F9B53F772382
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Test-AzureRmDataLakeStoreAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Test-AzureRmDataLakeStoreAccount.md
ms.openlocfilehash: 8aeb682b270de821a6944c619d7933148b2855e1
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93505070"
---
# <span data-ttu-id="09656-101">Test-AzureRmDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="09656-101">Test-AzureRmDataLakeStoreAccount</span></span>

## <span data-ttu-id="09656-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="09656-102">SYNOPSIS</span></span>
<span data-ttu-id="09656-103">Testet das vorhanden sein eines Data Lake Store-Kontos.</span><span class="sxs-lookup"><span data-stu-id="09656-103">Tests the existence of a Data Lake Store account.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="09656-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="09656-104">SYNTAX</span></span>

```
Test-AzureRmDataLakeStoreAccount [-Name] <String> [[-ResourceGroupName] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="09656-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="09656-105">DESCRIPTION</span></span>
<span data-ttu-id="09656-106">Das Cmdlet **Test-AzureRmDataLakeStoreAccount** testet das vorhanden sein eines Data Lake Store-Kontos.</span><span class="sxs-lookup"><span data-stu-id="09656-106">The **Test-AzureRmDataLakeStoreAccount** cmdlet tests the existence of a Data Lake Store account.</span></span>

## <span data-ttu-id="09656-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="09656-107">EXAMPLES</span></span>

### <span data-ttu-id="09656-108">Beispiel 1: Testen eines Kontos</span><span class="sxs-lookup"><span data-stu-id="09656-108">Example 1: Test an account</span></span>
```
PS C:\>Test-AzureRmDataLakeStoreAccount -Name "ContosoADL"
```

<span data-ttu-id="09656-109">Dieser Befehl testet, ob das Konto mit dem Namen ContosoADL vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="09656-109">This command tests whether the account named ContosoADL exists.</span></span>

## <span data-ttu-id="09656-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="09656-110">PARAMETERS</span></span>

### <span data-ttu-id="09656-111">-Name</span><span class="sxs-lookup"><span data-stu-id="09656-111">-Name</span></span>
<span data-ttu-id="09656-112">Gibt den Namen des Daten Lake Store-Kontos an, das getestet werden soll.</span><span class="sxs-lookup"><span data-stu-id="09656-112">Specifies the name of the Data Lake Store account to test.</span></span>

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

### <span data-ttu-id="09656-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="09656-113">-ResourceGroupName</span></span>
<span data-ttu-id="09656-114">Gibt den Namen der Ressourcengruppe an, die das zu testende Konto enthält.</span><span class="sxs-lookup"><span data-stu-id="09656-114">Specifies the name of the resource group that contains the account to test.</span></span>

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

### <span data-ttu-id="09656-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="09656-115">-DefaultProfile</span></span>
<span data-ttu-id="09656-116">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="09656-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="09656-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="09656-117">CommonParameters</span></span>
<span data-ttu-id="09656-118">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="09656-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="09656-119">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="09656-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="09656-120">Eingaben</span><span class="sxs-lookup"><span data-stu-id="09656-120">INPUTS</span></span>

## <span data-ttu-id="09656-121">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="09656-121">OUTPUTS</span></span>

### <span data-ttu-id="09656-122">bool</span><span class="sxs-lookup"><span data-stu-id="09656-122">bool</span></span>
<span data-ttu-id="09656-123">"Wahr" oder "falsch" gibt an, dass das angegebene Konto vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="09656-123">True or false indicating the existence of the specified account.</span></span>

## <span data-ttu-id="09656-124">Notizen</span><span class="sxs-lookup"><span data-stu-id="09656-124">NOTES</span></span>

## <span data-ttu-id="09656-125">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="09656-125">RELATED LINKS</span></span>

[<span data-ttu-id="09656-126">Get-AzureRmDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="09656-126">Get-AzureRmDataLakeStoreAccount</span></span>](./Get-AzureRmDataLakeStoreAccount.md)

[<span data-ttu-id="09656-127">Neu – AzureRmDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="09656-127">New-AzureRmDataLakeStoreAccount</span></span>](./New-AzureRmDataLakeStoreAccount.md)

[<span data-ttu-id="09656-128">Remove-AzureRmDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="09656-128">Remove-AzureRmDataLakeStoreAccount</span></span>](./Remove-AzureRmDataLakeStoreAccount.md)

[<span data-ttu-id="09656-129">Satz-AzureRmDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="09656-129">Set-AzureRmDataLakeStoreAccount</span></span>](./Set-AzureRmDataLakeStoreAccount.md)


