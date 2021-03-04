---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeStore.dll-Help.xml
Module Name: Az.DataLakeStore
ms.assetid: ECA70C6C-E0B0-445D-BCAD-041625FAC632
online version: https://docs.microsoft.com/powershell/module/az.datalakestore/get-azdatalakestoreitem
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Get-AzDataLakeStoreItem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Get-AzDataLakeStoreItem.md
ms.openlocfilehash: 3a39e2f341404ac3f6dbb75c27408dd9d9ee2d47
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101947192"
---
# <span data-ttu-id="01ca3-101">Get-AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="01ca3-101">Get-AzDataLakeStoreItem</span></span>

## <span data-ttu-id="01ca3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="01ca3-102">SYNOPSIS</span></span>
<span data-ttu-id="01ca3-103">Ruft die Details einer Datei oder eines Ordners im Data Lake Store ab.</span><span class="sxs-lookup"><span data-stu-id="01ca3-103">Gets the details of a file or folder in Data Lake Store.</span></span>

## <span data-ttu-id="01ca3-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="01ca3-104">SYNTAX</span></span>

```
Get-AzDataLakeStoreItem [-Account] <String> [-Path] <DataLakeStorePathInstance>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="01ca3-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="01ca3-105">DESCRIPTION</span></span>
<span data-ttu-id="01ca3-106">Das **Get-AzDataLakeStoreItem-Cmdlet** ruft die Details einer Datei oder eines Ordners im Data Lake Store ab.</span><span class="sxs-lookup"><span data-stu-id="01ca3-106">The **Get-AzDataLakeStoreItem** cmdlet gets the details of a file or folder in Data Lake Store.</span></span>

## <span data-ttu-id="01ca3-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="01ca3-107">EXAMPLES</span></span>

### <span data-ttu-id="01ca3-108">Beispiel 1: Erhalten von Details zu einer Datei aus dem Data Lake Store</span><span class="sxs-lookup"><span data-stu-id="01ca3-108">Example 1: Get details of a file from the Data Lake Store</span></span>
```
PS C:\>Get-AzDataLakeStoreItem -AccountName "ContosoADL" -Path "/MyFiles/Test.csv"
```

<span data-ttu-id="01ca3-109">Mit diesem Befehl werden die Details der Dateidatei Test.csv aus dem Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="01ca3-109">This command gets the details of the file Test.csv from the Data Lake Store.</span></span>

## <span data-ttu-id="01ca3-110">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="01ca3-110">PARAMETERS</span></span>

### <span data-ttu-id="01ca3-111">-Konto</span><span class="sxs-lookup"><span data-stu-id="01ca3-111">-Account</span></span>
<span data-ttu-id="01ca3-112">Gibt den Namen des Data Lake Store-Kontos an.</span><span class="sxs-lookup"><span data-stu-id="01ca3-112">Specifies the name of the Data Lake Store account.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: AccountName

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="01ca3-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="01ca3-113">-DefaultProfile</span></span>
<span data-ttu-id="01ca3-114">Die Anmeldeinformationen, das Konto, der Mandant und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="01ca3-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="01ca3-115">-Path</span><span class="sxs-lookup"><span data-stu-id="01ca3-115">-Path</span></span>
<span data-ttu-id="01ca3-116">Gibt den Data Lake Store-Pfad an, über den Details zu einem Element ab dem Stammverzeichnis (/) angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="01ca3-116">Specifies the Data Lake Store path from which to get details of an item, starting with the root directory (/).</span></span>

```yaml
Type: Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStorePathInstance
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="01ca3-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="01ca3-117">CommonParameters</span></span>
<span data-ttu-id="01ca3-118">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="01ca3-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="01ca3-119">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="01ca3-119">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="01ca3-120">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="01ca3-120">INPUTS</span></span>

### <span data-ttu-id="01ca3-121">System.String</span><span class="sxs-lookup"><span data-stu-id="01ca3-121">System.String</span></span>

### <span data-ttu-id="01ca3-122">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStorePathInstance</span><span class="sxs-lookup"><span data-stu-id="01ca3-122">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStorePathInstance</span></span>

## <span data-ttu-id="01ca3-123">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="01ca3-123">OUTPUTS</span></span>

### <span data-ttu-id="01ca3-124">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="01ca3-124">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStoreItem</span></span>

## <span data-ttu-id="01ca3-125">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="01ca3-125">NOTES</span></span>

## <span data-ttu-id="01ca3-126">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="01ca3-126">RELATED LINKS</span></span>

[<span data-ttu-id="01ca3-127">Export-AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="01ca3-127">Export-AzDataLakeStoreItem</span></span>](./Export-AzDataLakeStoreItem.md)

[<span data-ttu-id="01ca3-128">Get-AzDataLakeStoreChildItem</span><span class="sxs-lookup"><span data-stu-id="01ca3-128">Get-AzDataLakeStoreChildItem</span></span>](./Get-AzDataLakeStoreChildItem.md)

[<span data-ttu-id="01ca3-129">Import-AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="01ca3-129">Import-AzDataLakeStoreItem</span></span>](./Import-AzDataLakeStoreItem.md)

[<span data-ttu-id="01ca3-130">Join-AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="01ca3-130">Join-AzDataLakeStoreItem</span></span>](./Join-AzDataLakeStoreItem.md)

[<span data-ttu-id="01ca3-131">Move-AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="01ca3-131">Move-AzDataLakeStoreItem</span></span>](./Move-AzDataLakeStoreItem.md)

[<span data-ttu-id="01ca3-132">New-AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="01ca3-132">New-AzDataLakeStoreItem</span></span>](./New-AzDataLakeStoreItem.md)

[<span data-ttu-id="01ca3-133">Remove-AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="01ca3-133">Remove-AzDataLakeStoreItem</span></span>](./Remove-AzDataLakeStoreItem.md)

[<span data-ttu-id="01ca3-134">Test-AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="01ca3-134">Test-AzDataLakeStoreItem</span></span>](./Test-AzDataLakeStoreItem.md)


