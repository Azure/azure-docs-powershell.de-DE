---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeStore.dll-Help.xml
Module Name: Az.DataLakeStore
ms.assetid: ECA70C6C-E0B0-445D-BCAD-041625FAC632
online version: https://docs.microsoft.com/en-us/powershell/module/az.datalakestore/get-azdatalakestoreitem
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Get-AzDataLakeStoreItem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Get-AzDataLakeStoreItem.md
ms.openlocfilehash: ad741d955399b355534074737741b153d8d48690
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94008058"
---
# <span data-ttu-id="4d7cc-101">Get-AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="4d7cc-101">Get-AzDataLakeStoreItem</span></span>

## <span data-ttu-id="4d7cc-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="4d7cc-102">SYNOPSIS</span></span>
<span data-ttu-id="4d7cc-103">Ruft die Details einer Datei oder eines Ordners im Data Lake Store ab.</span><span class="sxs-lookup"><span data-stu-id="4d7cc-103">Gets the details of a file or folder in Data Lake Store.</span></span>

## <span data-ttu-id="4d7cc-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="4d7cc-104">SYNTAX</span></span>

```
Get-AzDataLakeStoreItem [-Account] <String> [-Path] <DataLakeStorePathInstance>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="4d7cc-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="4d7cc-105">DESCRIPTION</span></span>
<span data-ttu-id="4d7cc-106">Das Cmdlet " **Get-AzDataLakeStoreItem** " Ruft die Details einer Datei oder eines Ordners im Data Lake Store ab.</span><span class="sxs-lookup"><span data-stu-id="4d7cc-106">The **Get-AzDataLakeStoreItem** cmdlet gets the details of a file or folder in Data Lake Store.</span></span>

## <span data-ttu-id="4d7cc-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="4d7cc-107">EXAMPLES</span></span>

### <span data-ttu-id="4d7cc-108">Beispiel 1: Abrufen von Details zu einer Datei aus dem Data Lake Store</span><span class="sxs-lookup"><span data-stu-id="4d7cc-108">Example 1: Get details of a file from the Data Lake Store</span></span>
```
PS C:\>Get-AzDataLakeStoreItem -AccountName "ContosoADL" -Path "/MyFiles/Test.csv"
```

<span data-ttu-id="4d7cc-109">Dieser Befehl ruft die Details der Datei Test.csv aus dem Data Lake Store ab.</span><span class="sxs-lookup"><span data-stu-id="4d7cc-109">This command gets the details of the file Test.csv from the Data Lake Store.</span></span>

## <span data-ttu-id="4d7cc-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="4d7cc-110">PARAMETERS</span></span>

### <span data-ttu-id="4d7cc-111">-Konto</span><span class="sxs-lookup"><span data-stu-id="4d7cc-111">-Account</span></span>
<span data-ttu-id="4d7cc-112">Gibt den Namen des Data Lake Store-Kontos an.</span><span class="sxs-lookup"><span data-stu-id="4d7cc-112">Specifies the name of the Data Lake Store account.</span></span>

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

### <span data-ttu-id="4d7cc-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4d7cc-113">-DefaultProfile</span></span>
<span data-ttu-id="4d7cc-114">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="4d7cc-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="4d7cc-115">-Path</span><span class="sxs-lookup"><span data-stu-id="4d7cc-115">-Path</span></span>
<span data-ttu-id="4d7cc-116">Gibt den Daten See-Speicherpfad an, aus dem Details zu einem Element abgerufen werden sollen, beginnend mit dem Stammverzeichnis (/).</span><span class="sxs-lookup"><span data-stu-id="4d7cc-116">Specifies the Data Lake Store path from which to get details of an item, starting with the root directory (/).</span></span>

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

### <span data-ttu-id="4d7cc-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4d7cc-117">CommonParameters</span></span>
<span data-ttu-id="4d7cc-118">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4d7cc-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4d7cc-119">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4d7cc-119">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4d7cc-120">Eingaben</span><span class="sxs-lookup"><span data-stu-id="4d7cc-120">INPUTS</span></span>

### <span data-ttu-id="4d7cc-121">System. String</span><span class="sxs-lookup"><span data-stu-id="4d7cc-121">System.String</span></span>

### <span data-ttu-id="4d7cc-122">Microsoft. Azure. Commands. DataLakeStore. Models. DataLakeStorePathInstance</span><span class="sxs-lookup"><span data-stu-id="4d7cc-122">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStorePathInstance</span></span>

## <span data-ttu-id="4d7cc-123">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="4d7cc-123">OUTPUTS</span></span>

### <span data-ttu-id="4d7cc-124">Microsoft. Azure. Commands. DataLakeStore. Models. DataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="4d7cc-124">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStoreItem</span></span>

## <span data-ttu-id="4d7cc-125">Notizen</span><span class="sxs-lookup"><span data-stu-id="4d7cc-125">NOTES</span></span>

## <span data-ttu-id="4d7cc-126">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="4d7cc-126">RELATED LINKS</span></span>

[<span data-ttu-id="4d7cc-127">Export-AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="4d7cc-127">Export-AzDataLakeStoreItem</span></span>](./Export-AzDataLakeStoreItem.md)

[<span data-ttu-id="4d7cc-128">Get-AzDataLakeStoreChildItem</span><span class="sxs-lookup"><span data-stu-id="4d7cc-128">Get-AzDataLakeStoreChildItem</span></span>](./Get-AzDataLakeStoreChildItem.md)

[<span data-ttu-id="4d7cc-129">Importieren-AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="4d7cc-129">Import-AzDataLakeStoreItem</span></span>](./Import-AzDataLakeStoreItem.md)

[<span data-ttu-id="4d7cc-130">Teilnehmen – AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="4d7cc-130">Join-AzDataLakeStoreItem</span></span>](./Join-AzDataLakeStoreItem.md)

[<span data-ttu-id="4d7cc-131">Verschieben-AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="4d7cc-131">Move-AzDataLakeStoreItem</span></span>](./Move-AzDataLakeStoreItem.md)

[<span data-ttu-id="4d7cc-132">Neu – AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="4d7cc-132">New-AzDataLakeStoreItem</span></span>](./New-AzDataLakeStoreItem.md)

[<span data-ttu-id="4d7cc-133">Remove-AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="4d7cc-133">Remove-AzDataLakeStoreItem</span></span>](./Remove-AzDataLakeStoreItem.md)

[<span data-ttu-id="4d7cc-134">Test-AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="4d7cc-134">Test-AzDataLakeStoreItem</span></span>](./Test-AzDataLakeStoreItem.md)


