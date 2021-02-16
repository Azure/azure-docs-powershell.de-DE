---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeStore.dll-Help.xml
Module Name: Az.DataLakeStore
ms.assetid: ECA70C6C-E0B0-445D-BCAD-041625FAC632
online version: https://docs.microsoft.com/en-us/powershell/module/az.datalakestore/get-azdatalakestoreitem
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Get-AzDataLakeStoreItem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Get-AzDataLakeStoreItem.md
ms.openlocfilehash: ad741d955399b355534074737741b153d8d48690
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100161900"
---
# <span data-ttu-id="1a3cb-101">Get-AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="1a3cb-101">Get-AzDataLakeStoreItem</span></span>

## <span data-ttu-id="1a3cb-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1a3cb-102">SYNOPSIS</span></span>
<span data-ttu-id="1a3cb-103">Ruft die Details einer Datei oder eines Ordners im Data Lake Store ab.</span><span class="sxs-lookup"><span data-stu-id="1a3cb-103">Gets the details of a file or folder in Data Lake Store.</span></span>

## <span data-ttu-id="1a3cb-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="1a3cb-104">SYNTAX</span></span>

```
Get-AzDataLakeStoreItem [-Account] <String> [-Path] <DataLakeStorePathInstance>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="1a3cb-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="1a3cb-105">DESCRIPTION</span></span>
<span data-ttu-id="1a3cb-106">Das **Cmdlet "Get-AzDataLakeStoreItem"** ruft die Details einer Datei oder eines Ordners im Data Lake Store ab.</span><span class="sxs-lookup"><span data-stu-id="1a3cb-106">The **Get-AzDataLakeStoreItem** cmdlet gets the details of a file or folder in Data Lake Store.</span></span>

## <span data-ttu-id="1a3cb-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="1a3cb-107">EXAMPLES</span></span>

### <span data-ttu-id="1a3cb-108">Beispiel 1: Erhalten von Details zu einer Datei aus dem Data Lake Store</span><span class="sxs-lookup"><span data-stu-id="1a3cb-108">Example 1: Get details of a file from the Data Lake Store</span></span>
```
PS C:\>Get-AzDataLakeStoreItem -AccountName "ContosoADL" -Path "/MyFiles/Test.csv"
```

<span data-ttu-id="1a3cb-109">Dieser Befehl ruft die Details des Dateityps Test.csv aus dem Data Lake Store ab.</span><span class="sxs-lookup"><span data-stu-id="1a3cb-109">This command gets the details of the file Test.csv from the Data Lake Store.</span></span>

## <span data-ttu-id="1a3cb-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="1a3cb-110">PARAMETERS</span></span>

### <span data-ttu-id="1a3cb-111">-Konto</span><span class="sxs-lookup"><span data-stu-id="1a3cb-111">-Account</span></span>
<span data-ttu-id="1a3cb-112">Gibt den Namen des Data Lake Store-Kontos an.</span><span class="sxs-lookup"><span data-stu-id="1a3cb-112">Specifies the name of the Data Lake Store account.</span></span>

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

### <span data-ttu-id="1a3cb-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1a3cb-113">-DefaultProfile</span></span>
<span data-ttu-id="1a3cb-114">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="1a3cb-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="1a3cb-115">-Path</span><span class="sxs-lookup"><span data-stu-id="1a3cb-115">-Path</span></span>
<span data-ttu-id="1a3cb-116">Gibt den Data Lake Store-Pfad an, über den Details zu einem Element angezeigt werden, beginnend mit dem Stammverzeichnis (/).</span><span class="sxs-lookup"><span data-stu-id="1a3cb-116">Specifies the Data Lake Store path from which to get details of an item, starting with the root directory (/).</span></span>

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

### <span data-ttu-id="1a3cb-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1a3cb-117">CommonParameters</span></span>
<span data-ttu-id="1a3cb-118">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1a3cb-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1a3cb-119">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1a3cb-119">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1a3cb-120">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="1a3cb-120">INPUTS</span></span>

### <span data-ttu-id="1a3cb-121">System.String</span><span class="sxs-lookup"><span data-stu-id="1a3cb-121">System.String</span></span>

### <span data-ttu-id="1a3cb-122">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStorePathInstance</span><span class="sxs-lookup"><span data-stu-id="1a3cb-122">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStorePathInstance</span></span>

## <span data-ttu-id="1a3cb-123">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="1a3cb-123">OUTPUTS</span></span>

### <span data-ttu-id="1a3cb-124">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="1a3cb-124">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStoreItem</span></span>

## <span data-ttu-id="1a3cb-125">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="1a3cb-125">NOTES</span></span>

## <span data-ttu-id="1a3cb-126">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="1a3cb-126">RELATED LINKS</span></span>

[<span data-ttu-id="1a3cb-127">Export-AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="1a3cb-127">Export-AzDataLakeStoreItem</span></span>](./Export-AzDataLakeStoreItem.md)

[<span data-ttu-id="1a3cb-128">Get-AzDataLakeStoreChildItem</span><span class="sxs-lookup"><span data-stu-id="1a3cb-128">Get-AzDataLakeStoreChildItem</span></span>](./Get-AzDataLakeStoreChildItem.md)

[<span data-ttu-id="1a3cb-129">Import-AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="1a3cb-129">Import-AzDataLakeStoreItem</span></span>](./Import-AzDataLakeStoreItem.md)

[<span data-ttu-id="1a3cb-130">Join-AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="1a3cb-130">Join-AzDataLakeStoreItem</span></span>](./Join-AzDataLakeStoreItem.md)

[<span data-ttu-id="1a3cb-131">Move-AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="1a3cb-131">Move-AzDataLakeStoreItem</span></span>](./Move-AzDataLakeStoreItem.md)

[<span data-ttu-id="1a3cb-132">New-AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="1a3cb-132">New-AzDataLakeStoreItem</span></span>](./New-AzDataLakeStoreItem.md)

[<span data-ttu-id="1a3cb-133">Remove-AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="1a3cb-133">Remove-AzDataLakeStoreItem</span></span>](./Remove-AzDataLakeStoreItem.md)

[<span data-ttu-id="1a3cb-134">Test-AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="1a3cb-134">Test-AzDataLakeStoreItem</span></span>](./Test-AzDataLakeStoreItem.md)


