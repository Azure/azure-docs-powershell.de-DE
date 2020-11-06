---
external help file: Microsoft.Azure.Commands.DataLakeStore.dll-Help.xml
Module Name: AzureRM.DataLakeStore
ms.assetid: 4E9EA2E9-4BE2-4530-BC2B-D369C016CD8C
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datalakestore/join-azurermdatalakestoreitem
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Join-AzureRmDataLakeStoreItem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Join-AzureRmDataLakeStoreItem.md
ms.openlocfilehash: c321c605977e09f119d19e5c4ced44261c3de0cd
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93481230"
---
# <span data-ttu-id="3a5f3-101">Join-AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="3a5f3-101">Join-AzureRmDataLakeStoreItem</span></span>

## <span data-ttu-id="3a5f3-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="3a5f3-102">SYNOPSIS</span></span>
<span data-ttu-id="3a5f3-103">Verknüpft eine oder mehrere Dateien, um eine Datei im Data Lake Store zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="3a5f3-103">Joins one or more files to create one file in Data Lake Store.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="3a5f3-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="3a5f3-104">SYNTAX</span></span>

```
Join-AzureRmDataLakeStoreItem [-Account] <String> [-Paths] <DataLakeStorePathInstance[]>
 [-Destination] <DataLakeStorePathInstance> [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3a5f3-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="3a5f3-105">DESCRIPTION</span></span>
<span data-ttu-id="3a5f3-106">Das Cmdlet " **Join-AzureRmDataLakeStoreItem** " verknüpft eine oder mehrere Dateien, um eine Datei im Data Lake Store zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="3a5f3-106">The **Join-AzureRmDataLakeStoreItem** cmdlet joins one or more files to create one file in Data Lake Store.</span></span>

## <span data-ttu-id="3a5f3-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="3a5f3-107">EXAMPLES</span></span>

### <span data-ttu-id="3a5f3-108">Beispiel 1: teilnehmen an zwei Elementen</span><span class="sxs-lookup"><span data-stu-id="3a5f3-108">Example 1: Join two items</span></span>
```
PS C:\>Join-AzureRmDataLakeStoreItem -AccountName "ContosoADL" -Paths "/MyFiles/File01.txt","/MyFiles/File02.txt" -Destination "/MyFiles/CombinedFile.txt"
```

<span data-ttu-id="3a5f3-109">Dieser Befehl verknüpft File01.txt und File02.txt, um die Datei CombinedFile.txt zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="3a5f3-109">This command joins File01.txt and File02.txt to create the file CombinedFile.txt.</span></span>

## <span data-ttu-id="3a5f3-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="3a5f3-110">PARAMETERS</span></span>

### <span data-ttu-id="3a5f3-111">-Konto</span><span class="sxs-lookup"><span data-stu-id="3a5f3-111">-Account</span></span>
<span data-ttu-id="3a5f3-112">Gibt den Namen des Data Lake Store-Kontos an.</span><span class="sxs-lookup"><span data-stu-id="3a5f3-112">Specifies the name of the Data Lake Store account.</span></span>

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

### <span data-ttu-id="3a5f3-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3a5f3-113">-DefaultProfile</span></span>
<span data-ttu-id="3a5f3-114">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="3a5f3-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="3a5f3-115">-Ziel</span><span class="sxs-lookup"><span data-stu-id="3a5f3-115">-Destination</span></span>
<span data-ttu-id="3a5f3-116">Gibt den Daten See-Speicherpfad für das verknüpfte Element an, beginnend mit dem Stammverzeichnis (/).</span><span class="sxs-lookup"><span data-stu-id="3a5f3-116">Specifies the Data Lake Store path for the joined item, starting with the root directory (/).</span></span>

```yaml
Type: DataLakeStorePathInstance
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3a5f3-117">-Force</span><span class="sxs-lookup"><span data-stu-id="3a5f3-117">-Force</span></span>
<span data-ttu-id="3a5f3-118">Gibt an, dass dieser Vorgang die Zieldatei überschreiben kann, wenn Sie bereits vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="3a5f3-118">Indicates that this operation can overwrite the destination file if it already exists.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3a5f3-119">-Pfade</span><span class="sxs-lookup"><span data-stu-id="3a5f3-119">-Paths</span></span>
<span data-ttu-id="3a5f3-120">Gibt ein Array von Data Lake Store-Pfaden der zu kombinierenden Dateien an, beginnend mit dem Stammverzeichnis (/).</span><span class="sxs-lookup"><span data-stu-id="3a5f3-120">Specifies an array of Data Lake Store paths of the files to combine, starting with the root directory (/).</span></span>

```yaml
Type: DataLakeStorePathInstance[]
Parameter Sets: (All)
Aliases: Path

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3a5f3-121">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="3a5f3-121">-Confirm</span></span>
<span data-ttu-id="3a5f3-122">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="3a5f3-122">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3a5f3-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3a5f3-123">-WhatIf</span></span>
<span data-ttu-id="3a5f3-124">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="3a5f3-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3a5f3-125">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="3a5f3-125">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3a5f3-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3a5f3-126">CommonParameters</span></span>
<span data-ttu-id="3a5f3-127">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3a5f3-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3a5f3-128">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3a5f3-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3a5f3-129">Eingaben</span><span class="sxs-lookup"><span data-stu-id="3a5f3-129">INPUTS</span></span>

### <span data-ttu-id="3a5f3-130">Keine</span><span class="sxs-lookup"><span data-stu-id="3a5f3-130">None</span></span>
<span data-ttu-id="3a5f3-131">Dieses Cmdlet akzeptiert keine Eingaben.</span><span class="sxs-lookup"><span data-stu-id="3a5f3-131">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="3a5f3-132">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="3a5f3-132">OUTPUTS</span></span>

### <span data-ttu-id="3a5f3-133">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="3a5f3-133">string</span></span>
<span data-ttu-id="3a5f3-134">Der vollständige Pfad zur resultierenden Datei aus den verknüpften Dateien.</span><span class="sxs-lookup"><span data-stu-id="3a5f3-134">The full path to the resulting file from the joined files.</span></span>

## <span data-ttu-id="3a5f3-135">Notizen</span><span class="sxs-lookup"><span data-stu-id="3a5f3-135">NOTES</span></span>

## <span data-ttu-id="3a5f3-136">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="3a5f3-136">RELATED LINKS</span></span>

[<span data-ttu-id="3a5f3-137">Get-AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="3a5f3-137">Get-AzureRmDataLakeStoreItem</span></span>](./Get-AzureRmDataLakeStoreItem.md)

[<span data-ttu-id="3a5f3-138">Export-AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="3a5f3-138">Export-AzureRmDataLakeStoreItem</span></span>](./Export-AzureRmDataLakeStoreItem.md)

[<span data-ttu-id="3a5f3-139">Importieren-AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="3a5f3-139">Import-AzureRmDataLakeStoreItem</span></span>](./Import-AzureRmDataLakeStoreItem.md)

[<span data-ttu-id="3a5f3-140">Neu – AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="3a5f3-140">New-AzureRmDataLakeStoreItem</span></span>](./New-AzureRmDataLakeStoreItem.md)

[<span data-ttu-id="3a5f3-141">Remove-AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="3a5f3-141">Remove-AzureRmDataLakeStoreItem</span></span>](./Remove-AzureRmDataLakeStoreItem.md)

[<span data-ttu-id="3a5f3-142">Test-AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="3a5f3-142">Test-AzureRmDataLakeStoreItem</span></span>](./Test-AzureRmDataLakeStoreItem.md)


