---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeStore.dll-Help.xml
Module Name: Az.DataLakeStore
ms.assetid: 4E9EA2E9-4BE2-4530-BC2B-D369C016CD8C
online version: https://docs.microsoft.com/en-us/powershell/module/az.datalakestore/join-azdatalakestoreitem
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Join-AzDataLakeStoreItem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Join-AzDataLakeStoreItem.md
ms.openlocfilehash: 7ff40890783edbfaf610434f0b25ad04b4b3be21
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93661272"
---
# <span data-ttu-id="77bb9-101">Join-AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="77bb9-101">Join-AzDataLakeStoreItem</span></span>

## <span data-ttu-id="77bb9-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="77bb9-102">SYNOPSIS</span></span>
<span data-ttu-id="77bb9-103">Verknüpft eine oder mehrere Dateien, um eine Datei im Data Lake Store zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="77bb9-103">Joins one or more files to create one file in Data Lake Store.</span></span>

## <span data-ttu-id="77bb9-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="77bb9-104">SYNTAX</span></span>

```
Join-AzDataLakeStoreItem [-Account] <String> [-Paths] <DataLakeStorePathInstance[]>
 [-Destination] <DataLakeStorePathInstance> [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="77bb9-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="77bb9-105">DESCRIPTION</span></span>
<span data-ttu-id="77bb9-106">Das Cmdlet " **Join-AzDataLakeStoreItem** " verknüpft eine oder mehrere Dateien, um eine Datei im Data Lake Store zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="77bb9-106">The **Join-AzDataLakeStoreItem** cmdlet joins one or more files to create one file in Data Lake Store.</span></span>

## <span data-ttu-id="77bb9-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="77bb9-107">EXAMPLES</span></span>

### <span data-ttu-id="77bb9-108">Beispiel 1: teilnehmen an zwei Elementen</span><span class="sxs-lookup"><span data-stu-id="77bb9-108">Example 1: Join two items</span></span>
```
PS C:\>Join-AzDataLakeStoreItem -AccountName "ContosoADL" -Paths "/MyFiles/File01.txt","/MyFiles/File02.txt" -Destination "/MyFiles/CombinedFile.txt"
```

<span data-ttu-id="77bb9-109">Dieser Befehl verknüpft File01.txt und File02.txt, um die Datei CombinedFile.txt zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="77bb9-109">This command joins File01.txt and File02.txt to create the file CombinedFile.txt.</span></span>

## <span data-ttu-id="77bb9-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="77bb9-110">PARAMETERS</span></span>

### <span data-ttu-id="77bb9-111">-Konto</span><span class="sxs-lookup"><span data-stu-id="77bb9-111">-Account</span></span>
<span data-ttu-id="77bb9-112">Gibt den Namen des Data Lake Store-Kontos an.</span><span class="sxs-lookup"><span data-stu-id="77bb9-112">Specifies the name of the Data Lake Store account.</span></span>

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

### <span data-ttu-id="77bb9-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="77bb9-113">-DefaultProfile</span></span>
<span data-ttu-id="77bb9-114">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="77bb9-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="77bb9-115">-Ziel</span><span class="sxs-lookup"><span data-stu-id="77bb9-115">-Destination</span></span>
<span data-ttu-id="77bb9-116">Gibt den Daten See-Speicherpfad für das verknüpfte Element an, beginnend mit dem Stammverzeichnis (/).</span><span class="sxs-lookup"><span data-stu-id="77bb9-116">Specifies the Data Lake Store path for the joined item, starting with the root directory (/).</span></span>

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

### <span data-ttu-id="77bb9-117">-Force</span><span class="sxs-lookup"><span data-stu-id="77bb9-117">-Force</span></span>
<span data-ttu-id="77bb9-118">Gibt an, dass dieser Vorgang die Zieldatei überschreiben kann, wenn Sie bereits vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="77bb9-118">Indicates that this operation can overwrite the destination file if it already exists.</span></span>

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

### <span data-ttu-id="77bb9-119">-Pfade</span><span class="sxs-lookup"><span data-stu-id="77bb9-119">-Paths</span></span>
<span data-ttu-id="77bb9-120">Gibt ein Array von Data Lake Store-Pfaden der zu kombinierenden Dateien an, beginnend mit dem Stammverzeichnis (/).</span><span class="sxs-lookup"><span data-stu-id="77bb9-120">Specifies an array of Data Lake Store paths of the files to combine, starting with the root directory (/).</span></span>

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

### <span data-ttu-id="77bb9-121">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="77bb9-121">-Confirm</span></span>
<span data-ttu-id="77bb9-122">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="77bb9-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="77bb9-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="77bb9-123">-WhatIf</span></span>
<span data-ttu-id="77bb9-124">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="77bb9-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="77bb9-125">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="77bb9-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="77bb9-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="77bb9-126">CommonParameters</span></span>
<span data-ttu-id="77bb9-127">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="77bb9-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="77bb9-128">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="77bb9-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="77bb9-129">Eingaben</span><span class="sxs-lookup"><span data-stu-id="77bb9-129">INPUTS</span></span>

### <span data-ttu-id="77bb9-130">System. String</span><span class="sxs-lookup"><span data-stu-id="77bb9-130">System.String</span></span>

### <span data-ttu-id="77bb9-131">Microsoft. Azure. Commands. DataLakeStore. Models. DataLakeStorePathInstance []</span><span class="sxs-lookup"><span data-stu-id="77bb9-131">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStorePathInstance[]</span></span>

### <span data-ttu-id="77bb9-132">Microsoft. Azure. Commands. DataLakeStore. Models. DataLakeStorePathInstance</span><span class="sxs-lookup"><span data-stu-id="77bb9-132">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStorePathInstance</span></span>

### <span data-ttu-id="77bb9-133">System. Management. Automation. Switchparameter</span><span class="sxs-lookup"><span data-stu-id="77bb9-133">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="77bb9-134">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="77bb9-134">OUTPUTS</span></span>

### <span data-ttu-id="77bb9-135">System. String</span><span class="sxs-lookup"><span data-stu-id="77bb9-135">System.String</span></span>

## <span data-ttu-id="77bb9-136">Notizen</span><span class="sxs-lookup"><span data-stu-id="77bb9-136">NOTES</span></span>

## <span data-ttu-id="77bb9-137">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="77bb9-137">RELATED LINKS</span></span>

[<span data-ttu-id="77bb9-138">Get-AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="77bb9-138">Get-AzDataLakeStoreItem</span></span>](./Get-AzDataLakeStoreItem.md)

[<span data-ttu-id="77bb9-139">Export-AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="77bb9-139">Export-AzDataLakeStoreItem</span></span>](./Export-AzDataLakeStoreItem.md)

[<span data-ttu-id="77bb9-140">Importieren-AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="77bb9-140">Import-AzDataLakeStoreItem</span></span>](./Import-AzDataLakeStoreItem.md)

[<span data-ttu-id="77bb9-141">Neu – AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="77bb9-141">New-AzDataLakeStoreItem</span></span>](./New-AzDataLakeStoreItem.md)

[<span data-ttu-id="77bb9-142">Remove-AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="77bb9-142">Remove-AzDataLakeStoreItem</span></span>](./Remove-AzDataLakeStoreItem.md)

[<span data-ttu-id="77bb9-143">Test-AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="77bb9-143">Test-AzDataLakeStoreItem</span></span>](./Test-AzDataLakeStoreItem.md)


