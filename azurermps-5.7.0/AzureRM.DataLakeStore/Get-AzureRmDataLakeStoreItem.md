---
external help file: Microsoft.Azure.Commands.DataLakeStore.dll-Help.xml
Module Name: AzureRM.DataLakeStore
ms.assetid: ECA70C6C-E0B0-445D-BCAD-041625FAC632
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datalakestore/get-azurermdatalakestoreitem
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Get-AzureRmDataLakeStoreItem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Get-AzureRmDataLakeStoreItem.md
ms.openlocfilehash: b1a570d2821606944d4afde21919dad8832ed380
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93662472"
---
# <span data-ttu-id="98130-101">Get-AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="98130-101">Get-AzureRmDataLakeStoreItem</span></span>

## <span data-ttu-id="98130-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="98130-102">SYNOPSIS</span></span>
<span data-ttu-id="98130-103">Ruft die Details einer Datei oder eines Ordners im Data Lake Store ab.</span><span class="sxs-lookup"><span data-stu-id="98130-103">Gets the details of a file or folder in Data Lake Store.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="98130-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="98130-104">SYNTAX</span></span>

```
Get-AzureRmDataLakeStoreItem [-Account] <String> [-Path] <DataLakeStorePathInstance>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="98130-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="98130-105">DESCRIPTION</span></span>
<span data-ttu-id="98130-106">Das Cmdlet " **Get-AzureRmDataLakeStoreItem** " Ruft die Details einer Datei oder eines Ordners im Data Lake Store ab.</span><span class="sxs-lookup"><span data-stu-id="98130-106">The **Get-AzureRmDataLakeStoreItem** cmdlet gets the details of a file or folder in Data Lake Store.</span></span>

## <span data-ttu-id="98130-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="98130-107">EXAMPLES</span></span>

### <span data-ttu-id="98130-108">Beispiel 1: Abrufen von Details zu einer Datei aus dem Data Lake Store</span><span class="sxs-lookup"><span data-stu-id="98130-108">Example 1: Get details of a file from the Data Lake Store</span></span>
```
PS C:\>Get-AzureRmDataLakeStoreItem -AccountName "ContosoADL" -Path "/MyFiles/Test.csv"
```

<span data-ttu-id="98130-109">Dieser Befehl ruft die Details der Datei Test.csv aus dem Data Lake Store ab.</span><span class="sxs-lookup"><span data-stu-id="98130-109">This command gets the details of the file Test.csv from the Data Lake Store.</span></span>

## <span data-ttu-id="98130-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="98130-110">PARAMETERS</span></span>

### <span data-ttu-id="98130-111">-Konto</span><span class="sxs-lookup"><span data-stu-id="98130-111">-Account</span></span>
<span data-ttu-id="98130-112">Gibt den Namen des Data Lake Store-Kontos an.</span><span class="sxs-lookup"><span data-stu-id="98130-112">Specifies the name of the Data Lake Store account.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: AccountName

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="98130-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="98130-113">-DefaultProfile</span></span>
<span data-ttu-id="98130-114">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="98130-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="98130-115">-Path</span><span class="sxs-lookup"><span data-stu-id="98130-115">-Path</span></span>
<span data-ttu-id="98130-116">Gibt den Daten See-Speicherpfad an, aus dem Details zu einem Element abgerufen werden sollen, beginnend mit dem Stammverzeichnis (/).</span><span class="sxs-lookup"><span data-stu-id="98130-116">Specifies the Data Lake Store path from which to get details of an item, starting with the root directory (/).</span></span>

```yaml
Type: DataLakeStorePathInstance
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="98130-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="98130-117">CommonParameters</span></span>
<span data-ttu-id="98130-118">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="98130-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="98130-119">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="98130-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="98130-120">Eingaben</span><span class="sxs-lookup"><span data-stu-id="98130-120">INPUTS</span></span>

### <span data-ttu-id="98130-121">Keine</span><span class="sxs-lookup"><span data-stu-id="98130-121">None</span></span>
<span data-ttu-id="98130-122">Dieses Cmdlet akzeptiert keine Eingaben.</span><span class="sxs-lookup"><span data-stu-id="98130-122">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="98130-123">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="98130-123">OUTPUTS</span></span>

### <span data-ttu-id="98130-124">DataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="98130-124">DataLakeStoreItem</span></span>
<span data-ttu-id="98130-125">Die Datei oder der Ordner im angegebenen Pfad.</span><span class="sxs-lookup"><span data-stu-id="98130-125">The file or folder at the path specified.</span></span>

## <span data-ttu-id="98130-126">Notizen</span><span class="sxs-lookup"><span data-stu-id="98130-126">NOTES</span></span>

## <span data-ttu-id="98130-127">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="98130-127">RELATED LINKS</span></span>

[<span data-ttu-id="98130-128">Export-AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="98130-128">Export-AzureRmDataLakeStoreItem</span></span>](./Export-AzureRmDataLakeStoreItem.md)

[<span data-ttu-id="98130-129">Get-AzureRmDataLakeStoreChildItem</span><span class="sxs-lookup"><span data-stu-id="98130-129">Get-AzureRmDataLakeStoreChildItem</span></span>](./Get-AzureRmDataLakeStoreChildItem.md)

[<span data-ttu-id="98130-130">Importieren-AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="98130-130">Import-AzureRmDataLakeStoreItem</span></span>](./Import-AzureRmDataLakeStoreItem.md)

[<span data-ttu-id="98130-131">Teilnehmen – AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="98130-131">Join-AzureRmDataLakeStoreItem</span></span>](./Join-AzureRmDataLakeStoreItem.md)

[<span data-ttu-id="98130-132">Verschieben-AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="98130-132">Move-AzureRmDataLakeStoreItem</span></span>](./Move-AzureRmDataLakeStoreItem.md)

[<span data-ttu-id="98130-133">Neu – AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="98130-133">New-AzureRmDataLakeStoreItem</span></span>](./New-AzureRmDataLakeStoreItem.md)

[<span data-ttu-id="98130-134">Remove-AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="98130-134">Remove-AzureRmDataLakeStoreItem</span></span>](./Remove-AzureRmDataLakeStoreItem.md)

[<span data-ttu-id="98130-135">Test-AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="98130-135">Test-AzureRmDataLakeStoreItem</span></span>](./Test-AzureRmDataLakeStoreItem.md)


