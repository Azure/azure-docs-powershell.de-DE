---
external help file: Microsoft.Azure.Commands.DataLakeStore.dll-Help.xml
Module Name: AzureRM.DataLakeStore
ms.assetid: FFB335D4-AE3E-4788-B6FD-9AFC36F52B61
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datalakestore/set-azurermdatalakestoreitemacl
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Set-AzureRmDataLakeStoreItemAcl.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Set-AzureRmDataLakeStoreItemAcl.md
ms.openlocfilehash: 45bf9fe3fb57eb6e627f1b2c7bc3e9146ccfd444
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93496225"
---
# <span data-ttu-id="4543e-101">Set-AzureRmDataLakeStoreItemAcl</span><span class="sxs-lookup"><span data-stu-id="4543e-101">Set-AzureRmDataLakeStoreItemAcl</span></span>

## <span data-ttu-id="4543e-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="4543e-102">SYNOPSIS</span></span>
<span data-ttu-id="4543e-103">Ändert die ACL einer Datei oder eines Ordners im Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="4543e-103">Modifies the ACL of a file or folder in Data Lake Store.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="4543e-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="4543e-104">SYNTAX</span></span>

```
Set-AzureRmDataLakeStoreItemAcl [-Account] <String> [-Path] <DataLakeStorePathInstance>
 [-Acl] <DataLakeStoreItemAce[]> [-PassThru] [-Recurse] [-Concurrency <Int32>] [-ShowProgress]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4543e-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="4543e-105">DESCRIPTION</span></span>
<span data-ttu-id="4543e-106">Das Cmdlet " **festlegen-AzureRmDataLakeStoreItemAcl** " ändert die Zugriffssteuerungsliste (ACL) einer Datei oder eines Ordners im Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="4543e-106">The **Set-AzureRmDataLakeStoreItemAcl** cmdlet modifies the access control list (ACL) of a file or folder in Data Lake Store.</span></span>

## <span data-ttu-id="4543e-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="4543e-107">EXAMPLES</span></span>

### <span data-ttu-id="4543e-108">Beispiel 1: Einrichten der ACL für eine Datei und einen Ordner</span><span class="sxs-lookup"><span data-stu-id="4543e-108">Example 1: Set the ACL for a file and a folder</span></span>
```
PS C:\>$ACL = Get-AzureRmDataLakeStoreItemAclEntry -AccountName "ContosoADL" -Path /
PS C:\> Set-AzureRmDataLakeStoreItemAcl -AccountName "ContosoADL" -Path "/MyFiles/Test.txt" -Acl $ACL
```

<span data-ttu-id="4543e-109">Der erste Befehl ruft die ACL für das Stammverzeichnis des ContosoADL-Kontos ab und speichert es dann in der $ACL-Variablen.</span><span class="sxs-lookup"><span data-stu-id="4543e-109">The first command gets the ACL for the root directory of the ContosoADL account, and then stores it in the $ACL variable.</span></span>
<span data-ttu-id="4543e-110">Der zweite Befehl legt die ACL für die Datei Test.txt auf diejenige in $ACL fest.</span><span class="sxs-lookup"><span data-stu-id="4543e-110">The second command sets the ACL for the file Test.txt to the one in $ACL.</span></span>

### <span data-ttu-id="4543e-111">Beispiel 2: rekursives Einrichten der ACL für Ordner</span><span class="sxs-lookup"><span data-stu-id="4543e-111">Example 2: Set the ACL for folder recursively</span></span>
```
PS C:\>$ACL = Get-AzureRmDataLakeStoreItemAclEntry -AccountName "ContosoADL" -Path /Folder1
PS C:\> Set-AzureRmDataLakeStoreItemAcl -AccountName "ContosoADL" -Path "/Folder2" -Acl $ACL -Recurse -Concurrency 128
```

<span data-ttu-id="4543e-112">Der erste Befehl ruft die ACL für das Verzeichnis Folder1 des ContosoADL-Kontos ab und speichert Sie dann in der $ACL-Variablen.</span><span class="sxs-lookup"><span data-stu-id="4543e-112">The first command gets the ACL for the directory Folder1 of the ContosoADL account, and then stores it in the $ACL variable.</span></span>
<span data-ttu-id="4543e-113">Mit dem zweiten Befehl wird die ACL rekursiv auf Ordner2 und deren Unterverzeichnisse und Dateien in $ACL festgelegt.</span><span class="sxs-lookup"><span data-stu-id="4543e-113">The second command sets the ACL recursively to Folder2 and its sub directories and files to the one in $ACL.</span></span>

## <span data-ttu-id="4543e-114">Parameter</span><span class="sxs-lookup"><span data-stu-id="4543e-114">PARAMETERS</span></span>

### <span data-ttu-id="4543e-115">-Konto</span><span class="sxs-lookup"><span data-stu-id="4543e-115">-Account</span></span>
<span data-ttu-id="4543e-116">Gibt den Namen des Data Lake Store-Kontos an.</span><span class="sxs-lookup"><span data-stu-id="4543e-116">Specifies the name of the Data Lake Store account.</span></span>

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

### <span data-ttu-id="4543e-117">-ACL</span><span class="sxs-lookup"><span data-stu-id="4543e-117">-Acl</span></span>
<span data-ttu-id="4543e-118">Gibt eine Zugriffssteuerungsliste für eine Datei oder einen Ordner an.</span><span class="sxs-lookup"><span data-stu-id="4543e-118">Specifies an ACL for a file or a folder.</span></span>

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

### <span data-ttu-id="4543e-119">-Parallelität</span><span class="sxs-lookup"><span data-stu-id="4543e-119">-Concurrency</span></span>
<span data-ttu-id="4543e-120">Die Anzahl von Dateien/Verzeichnissen, die parallel verarbeitet werden.</span><span class="sxs-lookup"><span data-stu-id="4543e-120">Number of files/directories processed in parallel.</span></span> <span data-ttu-id="4543e-121">Optional: Es wird ein angemessener Standardwert ausgewählt.</span><span class="sxs-lookup"><span data-stu-id="4543e-121">Optional: a reasonable default will be selected.</span></span>

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

### <span data-ttu-id="4543e-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4543e-122">-DefaultProfile</span></span>
<span data-ttu-id="4543e-123">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="4543e-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="4543e-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="4543e-124">-PassThru</span></span>
<span data-ttu-id="4543e-125">Gibt an, dass die resultierende ACL zurückgegeben werden soll.</span><span class="sxs-lookup"><span data-stu-id="4543e-125">Indicates the resulting ACL should be returned.</span></span>

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

### <span data-ttu-id="4543e-126">-Path</span><span class="sxs-lookup"><span data-stu-id="4543e-126">-Path</span></span>
<span data-ttu-id="4543e-127">Gibt den Daten See-Speicherpfad der Datei oder des Ordners an, beginnend mit dem Stammverzeichnis (/).</span><span class="sxs-lookup"><span data-stu-id="4543e-127">Specifies the Data Lake Store path of the file or folder, starting with the root directory (/).</span></span>

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

### <span data-ttu-id="4543e-128">-Rekursiv</span><span class="sxs-lookup"><span data-stu-id="4543e-128">-Recurse</span></span>
<span data-ttu-id="4543e-129">Gibt an, dass die ACL rekursiv auf die untergeordneten Unterverzeichnisse und Dateien gesetzt werden soll.</span><span class="sxs-lookup"><span data-stu-id="4543e-129">Indicates the ACL to be set recursively to the child subdirectories and files</span></span>

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

### <span data-ttu-id="4543e-130">-Progress</span><span class="sxs-lookup"><span data-stu-id="4543e-130">-ShowProgress</span></span>
<span data-ttu-id="4543e-131">Wenn übergeben, wird der Status Status angezeigt.</span><span class="sxs-lookup"><span data-stu-id="4543e-131">If passed then progress status is showed.</span></span> <span data-ttu-id="4543e-132">Gilt nur, wenn der rekursive ACL-Satz abgeschlossen ist.</span><span class="sxs-lookup"><span data-stu-id="4543e-132">Only applicable when recursive Acl set is done.</span></span>

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

### <span data-ttu-id="4543e-133">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="4543e-133">-Confirm</span></span>
<span data-ttu-id="4543e-134">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="4543e-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4543e-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4543e-135">-WhatIf</span></span>
<span data-ttu-id="4543e-136">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="4543e-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4543e-137">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="4543e-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4543e-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4543e-138">CommonParameters</span></span>
<span data-ttu-id="4543e-139">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4543e-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4543e-140">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4543e-140">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4543e-141">Eingaben</span><span class="sxs-lookup"><span data-stu-id="4543e-141">INPUTS</span></span>

### <span data-ttu-id="4543e-142">System. String</span><span class="sxs-lookup"><span data-stu-id="4543e-142">System.String</span></span>

### <span data-ttu-id="4543e-143">Microsoft. Azure. Commands. DataLakeStore. Models. DataLakeStorePathInstance</span><span class="sxs-lookup"><span data-stu-id="4543e-143">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStorePathInstance</span></span>

### <span data-ttu-id="4543e-144">Microsoft. Azure. Commands. DataLakeStore. Models. DataLakeStoreItemAce []</span><span class="sxs-lookup"><span data-stu-id="4543e-144">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStoreItemAce[]</span></span>

### <span data-ttu-id="4543e-145">System. Management. Automation. Switchparameter</span><span class="sxs-lookup"><span data-stu-id="4543e-145">System.Management.Automation.SwitchParameter</span></span>

### <span data-ttu-id="4543e-146">System. Int32</span><span class="sxs-lookup"><span data-stu-id="4543e-146">System.Int32</span></span>

## <span data-ttu-id="4543e-147">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="4543e-147">OUTPUTS</span></span>

### <span data-ttu-id="4543e-148">Microsoft. Azure. Commands. DataLakeStore. Models. DataLakeStoreItemAce</span><span class="sxs-lookup"><span data-stu-id="4543e-148">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStoreItemAce</span></span>
<span data-ttu-id="4543e-149">Wenn passthru angegeben wird, gibt die resultierende Liste der ACL-Einträge zurück.</span><span class="sxs-lookup"><span data-stu-id="4543e-149">If PassThru is specified, will return the resulting list of ACL entries.</span></span>

## <span data-ttu-id="4543e-150">Notizen</span><span class="sxs-lookup"><span data-stu-id="4543e-150">NOTES</span></span>

## <span data-ttu-id="4543e-151">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="4543e-151">RELATED LINKS</span></span>
