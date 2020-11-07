---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeStore.dll-Help.xml
Module Name: Az.DataLakeStore
ms.assetid: FFB335D4-AE3E-4788-B6FD-9AFC36F52B61
online version: https://docs.microsoft.com/en-us/powershell/module/az.datalakestore/set-azdatalakestoreitemacl
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Set-AzDataLakeStoreItemAcl.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Set-AzDataLakeStoreItemAcl.md
ms.openlocfilehash: 53cf81c4996a9d77d1452ffd6d5f99c111aecbf1
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93651507"
---
# <span data-ttu-id="03bac-101">Set-AzDataLakeStoreItemAcl</span><span class="sxs-lookup"><span data-stu-id="03bac-101">Set-AzDataLakeStoreItemAcl</span></span>

## <span data-ttu-id="03bac-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="03bac-102">SYNOPSIS</span></span>
<span data-ttu-id="03bac-103">Ändert die ACL einer Datei oder eines Ordners im Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="03bac-103">Modifies the ACL of a file or folder in Data Lake Store.</span></span>

## <span data-ttu-id="03bac-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="03bac-104">SYNTAX</span></span>

```
Set-AzDataLakeStoreItemAcl [-Account] <String> [-Path] <DataLakeStorePathInstance>
 [-Acl] <DataLakeStoreItemAce[]> [-PassThru] [-Recurse] [-Concurrency <Int32>] [-ShowProgress]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="03bac-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="03bac-105">DESCRIPTION</span></span>
<span data-ttu-id="03bac-106">Das Cmdlet " **festlegen-AzDataLakeStoreItemAcl** " ändert die Zugriffssteuerungsliste (ACL) einer Datei oder eines Ordners im Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="03bac-106">The **Set-AzDataLakeStoreItemAcl** cmdlet modifies the access control list (ACL) of a file or folder in Data Lake Store.</span></span>

## <span data-ttu-id="03bac-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="03bac-107">EXAMPLES</span></span>

### <span data-ttu-id="03bac-108">Beispiel 1: Einrichten der ACL für eine Datei und einen Ordner</span><span class="sxs-lookup"><span data-stu-id="03bac-108">Example 1: Set the ACL for a file and a folder</span></span>
```
PS C:\>$ACL = Get-AzDataLakeStoreItemAclEntry -AccountName "ContosoADL" -Path /
PS C:\> Set-AzDataLakeStoreItemAcl -AccountName "ContosoADL" -Path "/MyFiles/Test.txt" -Acl $ACL
```

<span data-ttu-id="03bac-109">Der erste Befehl ruft die ACL für das Stammverzeichnis des ContosoADL-Kontos ab und speichert es dann in der $ACL-Variablen.</span><span class="sxs-lookup"><span data-stu-id="03bac-109">The first command gets the ACL for the root directory of the ContosoADL account, and then stores it in the $ACL variable.</span></span>
<span data-ttu-id="03bac-110">Der zweite Befehl legt die ACL für die Datei Test.txt auf diejenige in $ACL fest.</span><span class="sxs-lookup"><span data-stu-id="03bac-110">The second command sets the ACL for the file Test.txt to the one in $ACL.</span></span>

### <span data-ttu-id="03bac-111">Beispiel 2: rekursives Einrichten der ACL für Ordner</span><span class="sxs-lookup"><span data-stu-id="03bac-111">Example 2: Set the ACL for folder recursively</span></span>
```
PS C:\>$ACL = Get-AzDataLakeStoreItemAclEntry -AccountName "ContosoADL" -Path /Folder1
PS C:\> Set-AzDataLakeStoreItemAcl -AccountName "ContosoADL" -Path "/Folder2" -Acl $ACL -Recurse -Concurrency 128
```

<span data-ttu-id="03bac-112">Der erste Befehl ruft die ACL für das Verzeichnis Folder1 des ContosoADL-Kontos ab und speichert Sie dann in der $ACL-Variablen.</span><span class="sxs-lookup"><span data-stu-id="03bac-112">The first command gets the ACL for the directory Folder1 of the ContosoADL account, and then stores it in the $ACL variable.</span></span>
<span data-ttu-id="03bac-113">Mit dem zweiten Befehl wird die ACL rekursiv auf Ordner2 und deren Unterverzeichnisse und Dateien in $ACL festgelegt.</span><span class="sxs-lookup"><span data-stu-id="03bac-113">The second command sets the ACL recursively to Folder2 and its sub directories and files to the one in $ACL.</span></span>

## <span data-ttu-id="03bac-114">Parameter</span><span class="sxs-lookup"><span data-stu-id="03bac-114">PARAMETERS</span></span>

### <span data-ttu-id="03bac-115">-Konto</span><span class="sxs-lookup"><span data-stu-id="03bac-115">-Account</span></span>
<span data-ttu-id="03bac-116">Gibt den Namen des Data Lake Store-Kontos an.</span><span class="sxs-lookup"><span data-stu-id="03bac-116">Specifies the name of the Data Lake Store account.</span></span>

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

### <span data-ttu-id="03bac-117">-ACL</span><span class="sxs-lookup"><span data-stu-id="03bac-117">-Acl</span></span>
<span data-ttu-id="03bac-118">Gibt eine Zugriffssteuerungsliste für eine Datei oder einen Ordner an.</span><span class="sxs-lookup"><span data-stu-id="03bac-118">Specifies an ACL for a file or a folder.</span></span>

```yaml
Type: Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStoreItemAce[]
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="03bac-119">-Parallelität</span><span class="sxs-lookup"><span data-stu-id="03bac-119">-Concurrency</span></span>
<span data-ttu-id="03bac-120">Die Anzahl von Dateien/Verzeichnissen, die parallel verarbeitet werden.</span><span class="sxs-lookup"><span data-stu-id="03bac-120">Number of files/directories processed in parallel.</span></span> <span data-ttu-id="03bac-121">Optional: Es wird ein angemessener Standardwert ausgewählt.</span><span class="sxs-lookup"><span data-stu-id="03bac-121">Optional: a reasonable default will be selected.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="03bac-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="03bac-122">-DefaultProfile</span></span>
<span data-ttu-id="03bac-123">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="03bac-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="03bac-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="03bac-124">-PassThru</span></span>
<span data-ttu-id="03bac-125">Gibt an, dass die resultierende ACL zurückgegeben werden soll.</span><span class="sxs-lookup"><span data-stu-id="03bac-125">Indicates the resulting ACL should be returned.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="03bac-126">-Path</span><span class="sxs-lookup"><span data-stu-id="03bac-126">-Path</span></span>
<span data-ttu-id="03bac-127">Gibt den Daten See-Speicherpfad der Datei oder des Ordners an, beginnend mit dem Stammverzeichnis (/).</span><span class="sxs-lookup"><span data-stu-id="03bac-127">Specifies the Data Lake Store path of the file or folder, starting with the root directory (/).</span></span>

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

### <span data-ttu-id="03bac-128">-Rekursiv</span><span class="sxs-lookup"><span data-stu-id="03bac-128">-Recurse</span></span>
<span data-ttu-id="03bac-129">Gibt an, dass die ACL rekursiv auf die untergeordneten Unterverzeichnisse und Dateien gesetzt werden soll.</span><span class="sxs-lookup"><span data-stu-id="03bac-129">Indicates the ACL to be set recursively to the child subdirectories and files</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="03bac-130">-Progress</span><span class="sxs-lookup"><span data-stu-id="03bac-130">-ShowProgress</span></span>
<span data-ttu-id="03bac-131">Wenn übergeben, wird der Status Status angezeigt.</span><span class="sxs-lookup"><span data-stu-id="03bac-131">If passed then progress status is showed.</span></span> <span data-ttu-id="03bac-132">Gilt nur, wenn der rekursive ACL-Satz abgeschlossen ist.</span><span class="sxs-lookup"><span data-stu-id="03bac-132">Only applicable when recursive Acl set is done.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="03bac-133">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="03bac-133">-Confirm</span></span>
<span data-ttu-id="03bac-134">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="03bac-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="03bac-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="03bac-135">-WhatIf</span></span>
<span data-ttu-id="03bac-136">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="03bac-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="03bac-137">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="03bac-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="03bac-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="03bac-138">CommonParameters</span></span>
<span data-ttu-id="03bac-139">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="03bac-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="03bac-140">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="03bac-140">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="03bac-141">Eingaben</span><span class="sxs-lookup"><span data-stu-id="03bac-141">INPUTS</span></span>

### <span data-ttu-id="03bac-142">System. String</span><span class="sxs-lookup"><span data-stu-id="03bac-142">System.String</span></span>

### <span data-ttu-id="03bac-143">Microsoft. Azure. Commands. DataLakeStore. Models. DataLakeStorePathInstance</span><span class="sxs-lookup"><span data-stu-id="03bac-143">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStorePathInstance</span></span>

### <span data-ttu-id="03bac-144">Microsoft. Azure. Commands. DataLakeStore. Models. DataLakeStoreItemAce []</span><span class="sxs-lookup"><span data-stu-id="03bac-144">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStoreItemAce[]</span></span>

### <span data-ttu-id="03bac-145">System. Management. Automation. Switchparameter</span><span class="sxs-lookup"><span data-stu-id="03bac-145">System.Management.Automation.SwitchParameter</span></span>

### <span data-ttu-id="03bac-146">System. Int32</span><span class="sxs-lookup"><span data-stu-id="03bac-146">System.Int32</span></span>

## <span data-ttu-id="03bac-147">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="03bac-147">OUTPUTS</span></span>

### <span data-ttu-id="03bac-148">Microsoft. Azure. Commands. DataLakeStore. Models. DataLakeStoreItemAce</span><span class="sxs-lookup"><span data-stu-id="03bac-148">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStoreItemAce</span></span>

## <span data-ttu-id="03bac-149">Notizen</span><span class="sxs-lookup"><span data-stu-id="03bac-149">NOTES</span></span>

## <span data-ttu-id="03bac-150">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="03bac-150">RELATED LINKS</span></span>
