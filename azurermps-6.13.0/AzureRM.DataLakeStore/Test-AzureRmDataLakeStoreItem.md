---
external help file: Microsoft.Azure.Commands.DataLakeStore.dll-Help.xml
Module Name: AzureRM.DataLakeStore
ms.assetid: 0937A390-6AC2-4611-AA6C-99936AC0ABFD
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datalakestore/test-azurermdatalakestoreitem
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Test-AzureRmDataLakeStoreItem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Test-AzureRmDataLakeStoreItem.md
ms.openlocfilehash: e9410c8bd63a123f275f6e644971870b998deea0
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93502117"
---
# <span data-ttu-id="8bd8a-101">Test-AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="8bd8a-101">Test-AzureRmDataLakeStoreItem</span></span>

## <span data-ttu-id="8bd8a-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="8bd8a-102">SYNOPSIS</span></span>
<span data-ttu-id="8bd8a-103">Testet das vorhanden sein einer Datei oder eines Ordners im Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="8bd8a-103">Tests the existence of a file or folder in Data Lake Store.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="8bd8a-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="8bd8a-104">SYNTAX</span></span>

```
Test-AzureRmDataLakeStoreItem [-Account] <String> [-Path] <DataLakeStorePathInstance> [[-PathType] <PathType>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="8bd8a-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="8bd8a-105">DESCRIPTION</span></span>
<span data-ttu-id="8bd8a-106">Das Cmdlet **Test-AzureRmDataLakeStoreItem** testet das vorhanden sein einer Datei oder eines Ordners im Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="8bd8a-106">The **Test-AzureRmDataLakeStoreItem** cmdlet tests the existence of a file or folder in Data Lake Store.</span></span>

## <span data-ttu-id="8bd8a-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="8bd8a-107">EXAMPLES</span></span>

### <span data-ttu-id="8bd8a-108">Beispiel 1: Testen einer Datei</span><span class="sxs-lookup"><span data-stu-id="8bd8a-108">Example 1: Test a file</span></span>
```
PS C:\>Test-AzureRmDataLakeStoreItem -AccountName "ContosoADL" -Path "/MyFiles/Test.csv"
```

<span data-ttu-id="8bd8a-109">Dieser Befehl testet, ob die Datei Test.csv im ContosoADL-Konto vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="8bd8a-109">This command tests whether the file Test.csv exists in the ContosoADL account.</span></span>

## <span data-ttu-id="8bd8a-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="8bd8a-110">PARAMETERS</span></span>

### <span data-ttu-id="8bd8a-111">-Konto</span><span class="sxs-lookup"><span data-stu-id="8bd8a-111">-Account</span></span>
<span data-ttu-id="8bd8a-112">Gibt den Namen des Data Lake Store-Kontos an.</span><span class="sxs-lookup"><span data-stu-id="8bd8a-112">Specifies the name of the Data Lake Store account.</span></span>

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

### <span data-ttu-id="8bd8a-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8bd8a-113">-DefaultProfile</span></span>
<span data-ttu-id="8bd8a-114">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="8bd8a-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="8bd8a-115">-Path</span><span class="sxs-lookup"><span data-stu-id="8bd8a-115">-Path</span></span>
<span data-ttu-id="8bd8a-116">Gibt den Daten See-Speicherpfad des zu testenden Elements an, beginnend mit dem Stammverzeichnis (/).</span><span class="sxs-lookup"><span data-stu-id="8bd8a-116">Specifies the Data Lake Store path of the item to test, starting with the root directory (/).</span></span>

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

### <span data-ttu-id="8bd8a-117">-PathType</span><span class="sxs-lookup"><span data-stu-id="8bd8a-117">-PathType</span></span>
<span data-ttu-id="8bd8a-118">Gibt den Typ des zu testenden Elements an.</span><span class="sxs-lookup"><span data-stu-id="8bd8a-118">Specifies the type of item to test.</span></span>
<span data-ttu-id="8bd8a-119">Die zulässigen Werte für diesen Parameter lauten wie folgt:</span><span class="sxs-lookup"><span data-stu-id="8bd8a-119">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="8bd8a-120">Alle</span><span class="sxs-lookup"><span data-stu-id="8bd8a-120">Any</span></span> 
- <span data-ttu-id="8bd8a-121">Datei</span><span class="sxs-lookup"><span data-stu-id="8bd8a-121">File</span></span> 
- <span data-ttu-id="8bd8a-122">Ordner</span><span class="sxs-lookup"><span data-stu-id="8bd8a-122">Folder</span></span>

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

### <span data-ttu-id="8bd8a-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8bd8a-123">CommonParameters</span></span>
<span data-ttu-id="8bd8a-124">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8bd8a-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8bd8a-125">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8bd8a-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8bd8a-126">Eingaben</span><span class="sxs-lookup"><span data-stu-id="8bd8a-126">INPUTS</span></span>

### <span data-ttu-id="8bd8a-127">System. String</span><span class="sxs-lookup"><span data-stu-id="8bd8a-127">System.String</span></span>

### <span data-ttu-id="8bd8a-128">Microsoft. Azure. Commands. DataLakeStore. Models. DataLakeStorePathInstance</span><span class="sxs-lookup"><span data-stu-id="8bd8a-128">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStorePathInstance</span></span>

### <span data-ttu-id="8bd8a-129">Microsoft. Azure. Commands. DataLakeStore. Models. DataLakeStoreEnums + PathType</span><span class="sxs-lookup"><span data-stu-id="8bd8a-129">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStoreEnums+PathType</span></span>

## <span data-ttu-id="8bd8a-130">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="8bd8a-130">OUTPUTS</span></span>

### <span data-ttu-id="8bd8a-131">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="8bd8a-131">System.Boolean</span></span>

## <span data-ttu-id="8bd8a-132">Notizen</span><span class="sxs-lookup"><span data-stu-id="8bd8a-132">NOTES</span></span>

## <span data-ttu-id="8bd8a-133">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="8bd8a-133">RELATED LINKS</span></span>

[<span data-ttu-id="8bd8a-134">Export-AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="8bd8a-134">Export-AzureRmDataLakeStoreItem</span></span>](./Export-AzureRmDataLakeStoreItem.md)

[<span data-ttu-id="8bd8a-135">Get-AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="8bd8a-135">Get-AzureRmDataLakeStoreItem</span></span>](./Get-AzureRmDataLakeStoreItem.md)

[<span data-ttu-id="8bd8a-136">Importieren-AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="8bd8a-136">Import-AzureRmDataLakeStoreItem</span></span>](./Import-AzureRmDataLakeStoreItem.md)

[<span data-ttu-id="8bd8a-137">Teilnehmen – AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="8bd8a-137">Join-AzureRmDataLakeStoreItem</span></span>](./Join-AzureRmDataLakeStoreItem.md)

[<span data-ttu-id="8bd8a-138">Verschieben-AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="8bd8a-138">Move-AzureRmDataLakeStoreItem</span></span>](./Move-AzureRmDataLakeStoreItem.md)

[<span data-ttu-id="8bd8a-139">Remove-AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="8bd8a-139">Remove-AzureRmDataLakeStoreItem</span></span>](./Remove-AzureRmDataLakeStoreItem.md)


