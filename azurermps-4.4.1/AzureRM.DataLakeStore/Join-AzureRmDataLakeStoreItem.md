---
external help file: Microsoft.Azure.Commands.DataLakeStore.dll-Help.xml
Module Name: AzureRM.DataLakeStore
ms.assetid: 4E9EA2E9-4BE2-4530-BC2B-D369C016CD8C
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Join-AzureRmDataLakeStoreItem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Join-AzureRmDataLakeStoreItem.md
ms.openlocfilehash: 1f09d1da5ab4ad88ff16be56affaa582ad1e24d2
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93500861"
---
# <span data-ttu-id="d6341-101">Join-AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="d6341-101">Join-AzureRmDataLakeStoreItem</span></span>

## <span data-ttu-id="d6341-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="d6341-102">SYNOPSIS</span></span>
<span data-ttu-id="d6341-103">Verknüpft eine oder mehrere Dateien, um eine Datei im Data Lake Store zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="d6341-103">Joins one or more files to create one file in Data Lake Store.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d6341-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="d6341-104">SYNTAX</span></span>

```
Join-AzureRmDataLakeStoreItem [-Account] <String> [-Paths] <DataLakeStorePathInstance[]>
 [-Destination] <DataLakeStorePathInstance> [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d6341-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="d6341-105">DESCRIPTION</span></span>
<span data-ttu-id="d6341-106">Das Cmdlet " **Join-AzureRmDataLakeStoreItem** " verknüpft eine oder mehrere Dateien, um eine Datei im Data Lake Store zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="d6341-106">The **Join-AzureRmDataLakeStoreItem** cmdlet joins one or more files to create one file in Data Lake Store.</span></span>

## <span data-ttu-id="d6341-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="d6341-107">EXAMPLES</span></span>

### <span data-ttu-id="d6341-108">Beispiel 1: teilnehmen an zwei Elementen</span><span class="sxs-lookup"><span data-stu-id="d6341-108">Example 1: Join two items</span></span>
```
PS C:\>Join-AzureRmDataLakeStoreItem -AccountName "ContosoADL" -Paths "/MyFiles/File01.txt","/MyFiles/File02.txt" -Destination "/MyFiles/CombinedFile.txt"
```

<span data-ttu-id="d6341-109">Dieser Befehl verknüpft File01.txt und File02.txt, um die Datei CombinedFile.txt zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="d6341-109">This command joins File01.txt and File02.txt to create the file CombinedFile.txt.</span></span>

## <span data-ttu-id="d6341-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="d6341-110">PARAMETERS</span></span>

### <span data-ttu-id="d6341-111">-Konto</span><span class="sxs-lookup"><span data-stu-id="d6341-111">-Account</span></span>
<span data-ttu-id="d6341-112">Gibt den Namen des Data Lake Store-Kontos an.</span><span class="sxs-lookup"><span data-stu-id="d6341-112">Specifies the name of the Data Lake Store account.</span></span>

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

### <span data-ttu-id="d6341-113">-Ziel</span><span class="sxs-lookup"><span data-stu-id="d6341-113">-Destination</span></span>
<span data-ttu-id="d6341-114">Gibt den Daten See-Speicherpfad für das verknüpfte Element an, beginnend mit dem Stammverzeichnis (/).</span><span class="sxs-lookup"><span data-stu-id="d6341-114">Specifies the Data Lake Store path for the joined item, starting with the root directory (/).</span></span>

```yaml
Type: Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStorePathInstance
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d6341-115">-Force</span><span class="sxs-lookup"><span data-stu-id="d6341-115">-Force</span></span>
<span data-ttu-id="d6341-116">Gibt an, dass dieser Vorgang die Zieldatei überschreiben kann, wenn Sie bereits vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="d6341-116">Indicates that this operation can overwrite the destination file if it already exists.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d6341-117">-Pfade</span><span class="sxs-lookup"><span data-stu-id="d6341-117">-Paths</span></span>
<span data-ttu-id="d6341-118">Gibt ein Array von Data Lake Store-Pfaden der zu kombinierenden Dateien an, beginnend mit dem Stammverzeichnis (/).</span><span class="sxs-lookup"><span data-stu-id="d6341-118">Specifies an array of Data Lake Store paths of the files to combine, starting with the root directory (/).</span></span>

```yaml
Type: Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStorePathInstance[]
Parameter Sets: (All)
Aliases: Path

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d6341-119">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="d6341-119">-Confirm</span></span>
<span data-ttu-id="d6341-120">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="d6341-120">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d6341-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d6341-121">-WhatIf</span></span>
<span data-ttu-id="d6341-122">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="d6341-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d6341-123">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="d6341-123">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d6341-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d6341-124">-DefaultProfile</span></span>
<span data-ttu-id="d6341-125">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="d6341-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d6341-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d6341-126">CommonParameters</span></span>
<span data-ttu-id="d6341-127">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d6341-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d6341-128">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d6341-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d6341-129">Eingaben</span><span class="sxs-lookup"><span data-stu-id="d6341-129">INPUTS</span></span>

## <span data-ttu-id="d6341-130">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="d6341-130">OUTPUTS</span></span>

### <span data-ttu-id="d6341-131">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="d6341-131">string</span></span>
<span data-ttu-id="d6341-132">Der vollständige Pfad zur resultierenden Datei aus den verknüpften Dateien.</span><span class="sxs-lookup"><span data-stu-id="d6341-132">The full path to the resulting file from the joined files.</span></span>

## <span data-ttu-id="d6341-133">Notizen</span><span class="sxs-lookup"><span data-stu-id="d6341-133">NOTES</span></span>

## <span data-ttu-id="d6341-134">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="d6341-134">RELATED LINKS</span></span>

[<span data-ttu-id="d6341-135">Get-AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="d6341-135">Get-AzureRmDataLakeStoreItem</span></span>](./Get-AzureRmDataLakeStoreItem.md)

[<span data-ttu-id="d6341-136">Export-AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="d6341-136">Export-AzureRmDataLakeStoreItem</span></span>](./Export-AzureRmDataLakeStoreItem.md)

[<span data-ttu-id="d6341-137">Importieren-AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="d6341-137">Import-AzureRmDataLakeStoreItem</span></span>](./Import-AzureRmDataLakeStoreItem.md)

[<span data-ttu-id="d6341-138">Neu – AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="d6341-138">New-AzureRmDataLakeStoreItem</span></span>](./New-AzureRmDataLakeStoreItem.md)

[<span data-ttu-id="d6341-139">Remove-AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="d6341-139">Remove-AzureRmDataLakeStoreItem</span></span>](./Remove-AzureRmDataLakeStoreItem.md)

[<span data-ttu-id="d6341-140">Test-AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="d6341-140">Test-AzureRmDataLakeStoreItem</span></span>](./Test-AzureRmDataLakeStoreItem.md)


