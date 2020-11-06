---
external help file: Microsoft.Azure.Commands.DataLakeStore.dll-Help.xml
Module Name: AzureRM.DataLakeStore
ms.assetid: 0937A390-6AC2-4611-AA6C-99936AC0ABFD
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Test-AzureRmDataLakeStoreItem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Test-AzureRmDataLakeStoreItem.md
ms.openlocfilehash: a5087c3c2d2354eb33ab9777687d43f56f3eb42c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93500061"
---
# <span data-ttu-id="150fd-101">Test-AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="150fd-101">Test-AzureRmDataLakeStoreItem</span></span>

## <span data-ttu-id="150fd-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="150fd-102">SYNOPSIS</span></span>
<span data-ttu-id="150fd-103">Testet das vorhanden sein einer Datei oder eines Ordners im Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="150fd-103">Tests the existence of a file or folder in Data Lake Store.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="150fd-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="150fd-104">SYNTAX</span></span>

```
Test-AzureRmDataLakeStoreItem [-Account] <String> [-Path] <DataLakeStorePathInstance> [[-PathType] <PathType>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="150fd-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="150fd-105">DESCRIPTION</span></span>
<span data-ttu-id="150fd-106">Das Cmdlet **Test-AzureRmDataLakeStoreItem** testet das vorhanden sein einer Datei oder eines Ordners im Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="150fd-106">The **Test-AzureRmDataLakeStoreItem** cmdlet tests the existence of a file or folder in Data Lake Store.</span></span>

## <span data-ttu-id="150fd-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="150fd-107">EXAMPLES</span></span>

### <span data-ttu-id="150fd-108">Beispiel 1: Testen einer Datei</span><span class="sxs-lookup"><span data-stu-id="150fd-108">Example 1: Test a file</span></span>
```
PS C:\>Test-AzureRmDataLakeStoreItem -AccountName "ContosoADL" -Path "/MyFiles/Test.csv"
```

<span data-ttu-id="150fd-109">Dieser Befehl testet, ob die Datei Test.csv im ContosoADL-Konto vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="150fd-109">This command tests whether the file Test.csv exists in the ContosoADL account.</span></span>

## <span data-ttu-id="150fd-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="150fd-110">PARAMETERS</span></span>

### <span data-ttu-id="150fd-111">-Konto</span><span class="sxs-lookup"><span data-stu-id="150fd-111">-Account</span></span>
<span data-ttu-id="150fd-112">Gibt den Namen des Data Lake Store-Kontos an.</span><span class="sxs-lookup"><span data-stu-id="150fd-112">Specifies the name of the Data Lake Store account.</span></span>

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

### <span data-ttu-id="150fd-113">-Path</span><span class="sxs-lookup"><span data-stu-id="150fd-113">-Path</span></span>
<span data-ttu-id="150fd-114">Gibt den Daten See-Speicherpfad des zu testenden Elements an, beginnend mit dem Stammverzeichnis (/).</span><span class="sxs-lookup"><span data-stu-id="150fd-114">Specifies the Data Lake Store path of the item to test, starting with the root directory (/).</span></span>

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

### <span data-ttu-id="150fd-115">-PathType</span><span class="sxs-lookup"><span data-stu-id="150fd-115">-PathType</span></span>
<span data-ttu-id="150fd-116">Gibt den Typ des zu testenden Elements an.</span><span class="sxs-lookup"><span data-stu-id="150fd-116">Specifies the type of item to test.</span></span>
<span data-ttu-id="150fd-117">Die zulässigen Werte für diesen Parameter lauten wie folgt:</span><span class="sxs-lookup"><span data-stu-id="150fd-117">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="150fd-118">Alle</span><span class="sxs-lookup"><span data-stu-id="150fd-118">Any</span></span> 
- <span data-ttu-id="150fd-119">Datei</span><span class="sxs-lookup"><span data-stu-id="150fd-119">File</span></span> 
- <span data-ttu-id="150fd-120">Ordner</span><span class="sxs-lookup"><span data-stu-id="150fd-120">Folder</span></span>

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

### <span data-ttu-id="150fd-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="150fd-121">-DefaultProfile</span></span>
<span data-ttu-id="150fd-122">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="150fd-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="150fd-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="150fd-123">CommonParameters</span></span>
<span data-ttu-id="150fd-124">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="150fd-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="150fd-125">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="150fd-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="150fd-126">Eingaben</span><span class="sxs-lookup"><span data-stu-id="150fd-126">INPUTS</span></span>

## <span data-ttu-id="150fd-127">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="150fd-127">OUTPUTS</span></span>

### <span data-ttu-id="150fd-128">bool</span><span class="sxs-lookup"><span data-stu-id="150fd-128">bool</span></span>
<span data-ttu-id="150fd-129">"Wahr" oder "falsch" gibt an, dass die angegebene Datei oder der angegebene Ordner vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="150fd-129">True or false indicating the existence of the specified file or folder.</span></span>

## <span data-ttu-id="150fd-130">Notizen</span><span class="sxs-lookup"><span data-stu-id="150fd-130">NOTES</span></span>

## <span data-ttu-id="150fd-131">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="150fd-131">RELATED LINKS</span></span>

[<span data-ttu-id="150fd-132">Export-AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="150fd-132">Export-AzureRmDataLakeStoreItem</span></span>](./Export-AzureRmDataLakeStoreItem.md)

[<span data-ttu-id="150fd-133">Get-AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="150fd-133">Get-AzureRmDataLakeStoreItem</span></span>](./Get-AzureRmDataLakeStoreItem.md)

[<span data-ttu-id="150fd-134">Importieren-AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="150fd-134">Import-AzureRmDataLakeStoreItem</span></span>](./Import-AzureRmDataLakeStoreItem.md)

[<span data-ttu-id="150fd-135">Teilnehmen – AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="150fd-135">Join-AzureRmDataLakeStoreItem</span></span>](./Join-AzureRmDataLakeStoreItem.md)

[<span data-ttu-id="150fd-136">Verschieben-AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="150fd-136">Move-AzureRmDataLakeStoreItem</span></span>](./Move-AzureRmDataLakeStoreItem.md)

[<span data-ttu-id="150fd-137">Remove-AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="150fd-137">Remove-AzureRmDataLakeStoreItem</span></span>](./Remove-AzureRmDataLakeStoreItem.md)


