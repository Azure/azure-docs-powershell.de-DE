---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeStore.dll-Help.xml
Module Name: Az.DataLakeStore
ms.assetid: 0937A390-6AC2-4611-AA6C-99936AC0ABFD
online version: https://docs.microsoft.com/en-us/powershell/module/az.datalakestore/test-azdatalakestoreitem
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Test-AzDataLakeStoreItem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Test-AzDataLakeStoreItem.md
ms.openlocfilehash: 83f44ced24587340f063f24a17036184115cf299
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/21/2020
ms.locfileid: "93847615"
---
# <span data-ttu-id="d53e8-101">Test-AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="d53e8-101">Test-AzDataLakeStoreItem</span></span>

## <span data-ttu-id="d53e8-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="d53e8-102">SYNOPSIS</span></span>
<span data-ttu-id="d53e8-103">Testet das vorhanden sein einer Datei oder eines Ordners im Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="d53e8-103">Tests the existence of a file or folder in Data Lake Store.</span></span>

## <span data-ttu-id="d53e8-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="d53e8-104">SYNTAX</span></span>

```
Test-AzDataLakeStoreItem [-Account] <String> [-Path] <DataLakeStorePathInstance> [[-PathType] <PathType>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d53e8-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="d53e8-105">DESCRIPTION</span></span>
<span data-ttu-id="d53e8-106">Das Cmdlet **Test-AzDataLakeStoreItem** testet das vorhanden sein einer Datei oder eines Ordners im Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="d53e8-106">The **Test-AzDataLakeStoreItem** cmdlet tests the existence of a file or folder in Data Lake Store.</span></span>

## <span data-ttu-id="d53e8-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="d53e8-107">EXAMPLES</span></span>

### <span data-ttu-id="d53e8-108">Beispiel 1: Testen einer Datei</span><span class="sxs-lookup"><span data-stu-id="d53e8-108">Example 1: Test a file</span></span>
```
PS C:\>Test-AzDataLakeStoreItem -AccountName "ContosoADL" -Path "/MyFiles/Test.csv"
```

<span data-ttu-id="d53e8-109">Dieser Befehl testet, ob die Datei Test.csv im ContosoADL-Konto vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="d53e8-109">This command tests whether the file Test.csv exists in the ContosoADL account.</span></span>

## <span data-ttu-id="d53e8-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="d53e8-110">PARAMETERS</span></span>

### <span data-ttu-id="d53e8-111">-Konto</span><span class="sxs-lookup"><span data-stu-id="d53e8-111">-Account</span></span>
<span data-ttu-id="d53e8-112">Gibt den Namen des Data Lake Store-Kontos an.</span><span class="sxs-lookup"><span data-stu-id="d53e8-112">Specifies the name of the Data Lake Store account.</span></span>

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

### <span data-ttu-id="d53e8-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d53e8-113">-DefaultProfile</span></span>
<span data-ttu-id="d53e8-114">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="d53e8-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d53e8-115">-Path</span><span class="sxs-lookup"><span data-stu-id="d53e8-115">-Path</span></span>
<span data-ttu-id="d53e8-116">Gibt den Daten See-Speicherpfad des zu testenden Elements an, beginnend mit dem Stammverzeichnis (/).</span><span class="sxs-lookup"><span data-stu-id="d53e8-116">Specifies the Data Lake Store path of the item to test, starting with the root directory (/).</span></span>

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

### <span data-ttu-id="d53e8-117">-PathType</span><span class="sxs-lookup"><span data-stu-id="d53e8-117">-PathType</span></span>
<span data-ttu-id="d53e8-118">Gibt den Typ des zu testenden Elements an.</span><span class="sxs-lookup"><span data-stu-id="d53e8-118">Specifies the type of item to test.</span></span>
<span data-ttu-id="d53e8-119">Die zulässigen Werte für diesen Parameter lauten wie folgt:</span><span class="sxs-lookup"><span data-stu-id="d53e8-119">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="d53e8-120">Alle</span><span class="sxs-lookup"><span data-stu-id="d53e8-120">Any</span></span> 
- <span data-ttu-id="d53e8-121">Datei</span><span class="sxs-lookup"><span data-stu-id="d53e8-121">File</span></span> 
- <span data-ttu-id="d53e8-122">Ordner</span><span class="sxs-lookup"><span data-stu-id="d53e8-122">Folder</span></span>

```yaml
Type: Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStoreEnums+PathType
Parameter Sets: (All)
Aliases:
Accepted values: Any, File, Folder

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d53e8-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d53e8-123">CommonParameters</span></span>
<span data-ttu-id="d53e8-124">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d53e8-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d53e8-125">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d53e8-125">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d53e8-126">Eingaben</span><span class="sxs-lookup"><span data-stu-id="d53e8-126">INPUTS</span></span>

### <span data-ttu-id="d53e8-127">System. String</span><span class="sxs-lookup"><span data-stu-id="d53e8-127">System.String</span></span>

### <span data-ttu-id="d53e8-128">Microsoft. Azure. Commands. DataLakeStore. Models. DataLakeStorePathInstance</span><span class="sxs-lookup"><span data-stu-id="d53e8-128">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStorePathInstance</span></span>

### <span data-ttu-id="d53e8-129">Microsoft. Azure. Commands. DataLakeStore. Models. DataLakeStoreEnums + PathType</span><span class="sxs-lookup"><span data-stu-id="d53e8-129">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStoreEnums+PathType</span></span>

## <span data-ttu-id="d53e8-130">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="d53e8-130">OUTPUTS</span></span>

### <span data-ttu-id="d53e8-131">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="d53e8-131">System.Boolean</span></span>

## <span data-ttu-id="d53e8-132">Notizen</span><span class="sxs-lookup"><span data-stu-id="d53e8-132">NOTES</span></span>

## <span data-ttu-id="d53e8-133">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="d53e8-133">RELATED LINKS</span></span>

[<span data-ttu-id="d53e8-134">Export-AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="d53e8-134">Export-AzDataLakeStoreItem</span></span>](./Export-AzDataLakeStoreItem.md)

[<span data-ttu-id="d53e8-135">Get-AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="d53e8-135">Get-AzDataLakeStoreItem</span></span>](./Get-AzDataLakeStoreItem.md)

[<span data-ttu-id="d53e8-136">Importieren-AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="d53e8-136">Import-AzDataLakeStoreItem</span></span>](./Import-AzDataLakeStoreItem.md)

[<span data-ttu-id="d53e8-137">Teilnehmen – AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="d53e8-137">Join-AzDataLakeStoreItem</span></span>](./Join-AzDataLakeStoreItem.md)

[<span data-ttu-id="d53e8-138">Verschieben-AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="d53e8-138">Move-AzDataLakeStoreItem</span></span>](./Move-AzDataLakeStoreItem.md)

[<span data-ttu-id="d53e8-139">Remove-AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="d53e8-139">Remove-AzDataLakeStoreItem</span></span>](./Remove-AzDataLakeStoreItem.md)


