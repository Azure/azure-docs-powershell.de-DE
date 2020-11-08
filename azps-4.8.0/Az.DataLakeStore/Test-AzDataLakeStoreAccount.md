---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeStore.dll-Help.xml
Module Name: Az.DataLakeStore
ms.assetid: 613DE097-65E0-4F08-839D-F9B53F772382
online version: https://docs.microsoft.com/en-us/powershell/module/az.datalakestore/test-azdatalakestoreaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Test-AzDataLakeStoreAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Test-AzDataLakeStoreAccount.md
ms.openlocfilehash: 25837486fad8b17a272f5687129ff936f6d50a02
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94167003"
---
# <span data-ttu-id="9f1a2-101">Test-AzDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="9f1a2-101">Test-AzDataLakeStoreAccount</span></span>

## <span data-ttu-id="9f1a2-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="9f1a2-102">SYNOPSIS</span></span>
<span data-ttu-id="9f1a2-103">Testet das vorhanden sein eines Data Lake Store-Kontos.</span><span class="sxs-lookup"><span data-stu-id="9f1a2-103">Tests the existence of a Data Lake Store account.</span></span>

## <span data-ttu-id="9f1a2-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="9f1a2-104">SYNTAX</span></span>

```
Test-AzDataLakeStoreAccount [-Name] <String> [[-ResourceGroupName] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="9f1a2-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="9f1a2-105">DESCRIPTION</span></span>
<span data-ttu-id="9f1a2-106">Das Cmdlet **Test-AzDataLakeStoreAccount** testet das vorhanden sein eines Data Lake Store-Kontos.</span><span class="sxs-lookup"><span data-stu-id="9f1a2-106">The **Test-AzDataLakeStoreAccount** cmdlet tests the existence of a Data Lake Store account.</span></span>

## <span data-ttu-id="9f1a2-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="9f1a2-107">EXAMPLES</span></span>

### <span data-ttu-id="9f1a2-108">Beispiel 1: Testen eines Kontos</span><span class="sxs-lookup"><span data-stu-id="9f1a2-108">Example 1: Test an account</span></span>
```
PS C:\>Test-AzDataLakeStoreAccount -Name "ContosoADL"
```

<span data-ttu-id="9f1a2-109">Dieser Befehl testet, ob das Konto mit dem Namen ContosoADL vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="9f1a2-109">This command tests whether the account named ContosoADL exists.</span></span>

## <span data-ttu-id="9f1a2-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="9f1a2-110">PARAMETERS</span></span>

### <span data-ttu-id="9f1a2-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9f1a2-111">-DefaultProfile</span></span>
<span data-ttu-id="9f1a2-112">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="9f1a2-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="9f1a2-113">-Name</span><span class="sxs-lookup"><span data-stu-id="9f1a2-113">-Name</span></span>
<span data-ttu-id="9f1a2-114">Gibt den Namen des Daten Lake Store-Kontos an, das getestet werden soll.</span><span class="sxs-lookup"><span data-stu-id="9f1a2-114">Specifies the name of the Data Lake Store account to test.</span></span>

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

### <span data-ttu-id="9f1a2-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9f1a2-115">-ResourceGroupName</span></span>
<span data-ttu-id="9f1a2-116">Gibt den Namen der Ressourcengruppe an, die das zu testende Konto enthält.</span><span class="sxs-lookup"><span data-stu-id="9f1a2-116">Specifies the name of the resource group that contains the account to test.</span></span>

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

### <span data-ttu-id="9f1a2-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9f1a2-117">CommonParameters</span></span>
<span data-ttu-id="9f1a2-118">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9f1a2-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9f1a2-119">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9f1a2-119">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9f1a2-120">Eingaben</span><span class="sxs-lookup"><span data-stu-id="9f1a2-120">INPUTS</span></span>

### <span data-ttu-id="9f1a2-121">System. String</span><span class="sxs-lookup"><span data-stu-id="9f1a2-121">System.String</span></span>

## <span data-ttu-id="9f1a2-122">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="9f1a2-122">OUTPUTS</span></span>

### <span data-ttu-id="9f1a2-123">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="9f1a2-123">System.Boolean</span></span>

## <span data-ttu-id="9f1a2-124">Notizen</span><span class="sxs-lookup"><span data-stu-id="9f1a2-124">NOTES</span></span>

## <span data-ttu-id="9f1a2-125">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="9f1a2-125">RELATED LINKS</span></span>

[<span data-ttu-id="9f1a2-126">Get-AzDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="9f1a2-126">Get-AzDataLakeStoreAccount</span></span>](./Get-AzDataLakeStoreAccount.md)

[<span data-ttu-id="9f1a2-127">Neu – AzDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="9f1a2-127">New-AzDataLakeStoreAccount</span></span>](./New-AzDataLakeStoreAccount.md)

[<span data-ttu-id="9f1a2-128">Remove-AzDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="9f1a2-128">Remove-AzDataLakeStoreAccount</span></span>](./Remove-AzDataLakeStoreAccount.md)

[<span data-ttu-id="9f1a2-129">Satz-AzDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="9f1a2-129">Set-AzDataLakeStoreAccount</span></span>](./Set-AzDataLakeStoreAccount.md)


