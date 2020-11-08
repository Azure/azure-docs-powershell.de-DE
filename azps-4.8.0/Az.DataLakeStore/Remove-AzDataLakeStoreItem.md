---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeStore.dll-Help.xml
Module Name: Az.DataLakeStore
ms.assetid: 164DC871-0F0C-4E71-A37A-2B85CE65C2C4
online version: https://docs.microsoft.com/en-us/powershell/module/az.datalakestore/remove-azdatalakestoreitem
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Remove-AzDataLakeStoreItem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Remove-AzDataLakeStoreItem.md
ms.openlocfilehash: 5f927bd9ef64cc22eda7669e9b0d60127cf503ac
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94174783"
---
# <span data-ttu-id="934e5-101">Remove-AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="934e5-101">Remove-AzDataLakeStoreItem</span></span>

## <span data-ttu-id="934e5-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="934e5-102">SYNOPSIS</span></span>
<span data-ttu-id="934e5-103">Löscht eine Datei oder einen Ordner im Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="934e5-103">Deletes a file or folder in Data Lake Store.</span></span>

## <span data-ttu-id="934e5-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="934e5-104">SYNTAX</span></span>

```
Remove-AzDataLakeStoreItem [-Account] <String> [-Paths] <DataLakeStorePathInstance[]> [-Recurse] [-Force]
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="934e5-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="934e5-105">DESCRIPTION</span></span>
<span data-ttu-id="934e5-106">Das Cmdlet **Remove-AzDataLakeStoreItem** löscht eine Datei oder einen Ordner im Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="934e5-106">The **Remove-AzDataLakeStoreItem** cmdlet deletes a file or folder in Data Lake Store.</span></span>

## <span data-ttu-id="934e5-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="934e5-107">EXAMPLES</span></span>

### <span data-ttu-id="934e5-108">Beispiel 1: Entfernen mehrerer Elemente</span><span class="sxs-lookup"><span data-stu-id="934e5-108">Example 1: Remove multiple items</span></span>
```
PS C:\>Remove-AzDataLakeStoreItem -AccountName "ContosoADL" -Paths "/File01.txt","/MyFiles/File.csv"
```

<span data-ttu-id="934e5-109">Mit diesem Befehl werden die Dateien File01.txt und File.csv aus dem Data Lake Store entfernt.</span><span class="sxs-lookup"><span data-stu-id="934e5-109">This command removes the files File01.txt and File.csv from the Data Lake Store.</span></span>

## <span data-ttu-id="934e5-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="934e5-110">PARAMETERS</span></span>

### <span data-ttu-id="934e5-111">-Konto</span><span class="sxs-lookup"><span data-stu-id="934e5-111">-Account</span></span>
<span data-ttu-id="934e5-112">Gibt den Namen des Data Lake Store-Kontos an.</span><span class="sxs-lookup"><span data-stu-id="934e5-112">Specifies the name of the Data Lake Store account.</span></span>

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

### <span data-ttu-id="934e5-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="934e5-113">-DefaultProfile</span></span>
<span data-ttu-id="934e5-114">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="934e5-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="934e5-115">-Force</span><span class="sxs-lookup"><span data-stu-id="934e5-115">-Force</span></span>
<span data-ttu-id="934e5-116">Erzwingt, dass der Befehl ausgeführt wird, ohne die Bestätigung des Benutzers zu fordern.</span><span class="sxs-lookup"><span data-stu-id="934e5-116">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="934e5-117">-PassThru</span><span class="sxs-lookup"><span data-stu-id="934e5-117">-PassThru</span></span>
<span data-ttu-id="934e5-118">Gibt ein Objekt zurück, das das Element darstellt, mit dem Sie arbeiten.</span><span class="sxs-lookup"><span data-stu-id="934e5-118">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="934e5-119">Standardmäßig wird mit diesem Cmdlet keine Ausgabe generiert.</span><span class="sxs-lookup"><span data-stu-id="934e5-119">By default, this cmdlet does not generate any output.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="934e5-120">-Pfade</span><span class="sxs-lookup"><span data-stu-id="934e5-120">-Paths</span></span>
<span data-ttu-id="934e5-121">Gibt ein Array von Data Lake Store-Pfaden der zu entfernenden Dateien an, beginnend mit dem Stammverzeichnis (/).</span><span class="sxs-lookup"><span data-stu-id="934e5-121">Specifies an array of Data Lake Store paths of the files to remove, starting with the root directory (/).</span></span>

```yaml
Type: Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStorePathInstance[]
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="934e5-122">-Rekursiv</span><span class="sxs-lookup"><span data-stu-id="934e5-122">-Recurse</span></span>
<span data-ttu-id="934e5-123">Gibt an, dass dieser Vorgang alle Elemente im Zielordner, einschließlich Unterordnern, löscht.</span><span class="sxs-lookup"><span data-stu-id="934e5-123">Indicates that this operation deletes all items in the target folder, including subfolders.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="934e5-124">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="934e5-124">-Confirm</span></span>
<span data-ttu-id="934e5-125">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="934e5-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="934e5-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="934e5-126">-WhatIf</span></span>
<span data-ttu-id="934e5-127">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="934e5-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="934e5-128">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="934e5-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="934e5-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="934e5-129">CommonParameters</span></span>
<span data-ttu-id="934e5-130">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="934e5-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="934e5-131">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="934e5-131">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="934e5-132">Eingaben</span><span class="sxs-lookup"><span data-stu-id="934e5-132">INPUTS</span></span>

### <span data-ttu-id="934e5-133">System. String</span><span class="sxs-lookup"><span data-stu-id="934e5-133">System.String</span></span>

### <span data-ttu-id="934e5-134">Microsoft. Azure. Commands. DataLakeStore. Models. DataLakeStorePathInstance []</span><span class="sxs-lookup"><span data-stu-id="934e5-134">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStorePathInstance[]</span></span>

### <span data-ttu-id="934e5-135">System. Management. Automation. Switchparameter</span><span class="sxs-lookup"><span data-stu-id="934e5-135">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="934e5-136">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="934e5-136">OUTPUTS</span></span>

### <span data-ttu-id="934e5-137">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="934e5-137">System.Boolean</span></span>

## <span data-ttu-id="934e5-138">Notizen</span><span class="sxs-lookup"><span data-stu-id="934e5-138">NOTES</span></span>

## <span data-ttu-id="934e5-139">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="934e5-139">RELATED LINKS</span></span>

[<span data-ttu-id="934e5-140">Get-AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="934e5-140">Get-AzDataLakeStoreItem</span></span>](./Get-AzDataLakeStoreItem.md)

[<span data-ttu-id="934e5-141">Export-AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="934e5-141">Export-AzDataLakeStoreItem</span></span>](./Export-AzDataLakeStoreItem.md)

[<span data-ttu-id="934e5-142">Importieren-AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="934e5-142">Import-AzDataLakeStoreItem</span></span>](./Import-AzDataLakeStoreItem.md)

[<span data-ttu-id="934e5-143">Teilnehmen – AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="934e5-143">Join-AzDataLakeStoreItem</span></span>](./Join-AzDataLakeStoreItem.md)

[<span data-ttu-id="934e5-144">Neu – AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="934e5-144">New-AzDataLakeStoreItem</span></span>](./New-AzDataLakeStoreItem.md)

[<span data-ttu-id="934e5-145">Test-AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="934e5-145">Test-AzDataLakeStoreItem</span></span>](./Test-AzDataLakeStoreItem.md)


