---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeStore.dll-Help.xml
Module Name: Az.DataLakeStore
ms.assetid: FFB335D4-AE3E-4788-B6FD-9AFC36F52B61
online version: https://docs.microsoft.com/powershell/module/az.datalakestore/set-azdatalakestoreitemacl
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Set-AzDataLakeStoreItemAcl.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Set-AzDataLakeStoreItemAcl.md
ms.openlocfilehash: 16663994a245a7429560ccf2ab855a84acc6ae57
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101920707"
---
# <span data-ttu-id="1ff62-101">Set-AzDataLakeStoreItemAcl</span><span class="sxs-lookup"><span data-stu-id="1ff62-101">Set-AzDataLakeStoreItemAcl</span></span>

## <span data-ttu-id="1ff62-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1ff62-102">SYNOPSIS</span></span>
<span data-ttu-id="1ff62-103">Ändert die ACL einer Datei oder eines Ordners im Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="1ff62-103">Modifies the ACL of a file or folder in Data Lake Store.</span></span>

## <span data-ttu-id="1ff62-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="1ff62-104">SYNTAX</span></span>

```
Set-AzDataLakeStoreItemAcl [-Account] <String> [-Path] <DataLakeStorePathInstance>
 [-Acl] <DataLakeStoreItemAce[]> [-PassThru] [-Recurse] [-Concurrency <Int32>] [-ShowProgress]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1ff62-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="1ff62-105">DESCRIPTION</span></span>
<span data-ttu-id="1ff62-106">Das **Cmdlet Set-AzDataLakeStoreItemAcl** ändert die Zugriffssteuerungsliste (Access Control List, ACL) einer Datei oder eines Ordners im Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="1ff62-106">The **Set-AzDataLakeStoreItemAcl** cmdlet modifies the access control list (ACL) of a file or folder in Data Lake Store.</span></span>

## <span data-ttu-id="1ff62-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="1ff62-107">EXAMPLES</span></span>

### <span data-ttu-id="1ff62-108">Beispiel 1: Festlegen der ACL für eine Datei und einen Ordner</span><span class="sxs-lookup"><span data-stu-id="1ff62-108">Example 1: Set the ACL for a file and a folder</span></span>
```
PS C:\>$ACL = Get-AzDataLakeStoreItemAclEntry -AccountName "ContosoADL" -Path /
PS C:\> Set-AzDataLakeStoreItemAcl -AccountName "ContosoADL" -Path "/MyFiles/Test.txt" -Acl $ACL
```

<span data-ttu-id="1ff62-109">Der erste Befehl ruft die ACL für das Stammverzeichnis des ContosoADL-Kontos ab und speichert sie dann in der $ACL.</span><span class="sxs-lookup"><span data-stu-id="1ff62-109">The first command gets the ACL for the root directory of the ContosoADL account, and then stores it in the $ACL variable.</span></span>
<span data-ttu-id="1ff62-110">Mit dem zweiten Befehl wird die ACL für die Dateidatei Test.txt auf die in $ACL.</span><span class="sxs-lookup"><span data-stu-id="1ff62-110">The second command sets the ACL for the file Test.txt to the one in $ACL.</span></span>

### <span data-ttu-id="1ff62-111">Beispiel 2: Festlegen der ACL für den Ordner rekursiv</span><span class="sxs-lookup"><span data-stu-id="1ff62-111">Example 2: Set the ACL for folder recursively</span></span>
```
PS C:\>$ACL = Get-AzDataLakeStoreItemAclEntry -AccountName "ContosoADL" -Path /Folder1
PS C:\> Set-AzDataLakeStoreItemAcl -AccountName "ContosoADL" -Path "/Folder2" -Acl $ACL -Recurse -Concurrency 128
```

<span data-ttu-id="1ff62-112">Der erste Befehl ruft die ACL für den Verzeichnisordner1 des ContosoADL-Kontos ab und speichert sie dann in der $ACL Variablen.</span><span class="sxs-lookup"><span data-stu-id="1ff62-112">The first command gets the ACL for the directory Folder1 of the ContosoADL account, and then stores it in the $ACL variable.</span></span>
<span data-ttu-id="1ff62-113">Mit dem zweiten Befehl wird die ACL rekursiv auf Ordner2 und deren Unterverzeichnissen und Dateien auf das Verzeichnis in $ACL.</span><span class="sxs-lookup"><span data-stu-id="1ff62-113">The second command sets the ACL recursively to Folder2 and its sub directories and files to the one in $ACL.</span></span>

## <span data-ttu-id="1ff62-114">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="1ff62-114">PARAMETERS</span></span>

### <span data-ttu-id="1ff62-115">-Konto</span><span class="sxs-lookup"><span data-stu-id="1ff62-115">-Account</span></span>
<span data-ttu-id="1ff62-116">Gibt den Namen des Data Lake Store-Kontos an.</span><span class="sxs-lookup"><span data-stu-id="1ff62-116">Specifies the name of the Data Lake Store account.</span></span>

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

### <span data-ttu-id="1ff62-117">-Acl</span><span class="sxs-lookup"><span data-stu-id="1ff62-117">-Acl</span></span>
<span data-ttu-id="1ff62-118">Gibt eine ACL für eine Datei oder einen Ordner an.</span><span class="sxs-lookup"><span data-stu-id="1ff62-118">Specifies an ACL for a file or a folder.</span></span>

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

### <span data-ttu-id="1ff62-119">-Parallelität</span><span class="sxs-lookup"><span data-stu-id="1ff62-119">-Concurrency</span></span>
<span data-ttu-id="1ff62-120">Anzahl der parallel verarbeiteten Dateien/Verzeichnisse.</span><span class="sxs-lookup"><span data-stu-id="1ff62-120">Number of files/directories processed in parallel.</span></span> <span data-ttu-id="1ff62-121">Optional: Eine angemessene Standardeinstellung wird ausgewählt.</span><span class="sxs-lookup"><span data-stu-id="1ff62-121">Optional: a reasonable default will be selected.</span></span>

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

### <span data-ttu-id="1ff62-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1ff62-122">-DefaultProfile</span></span>
<span data-ttu-id="1ff62-123">Die Anmeldeinformationen, das Konto, der Mandant und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="1ff62-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="1ff62-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="1ff62-124">-PassThru</span></span>
<span data-ttu-id="1ff62-125">Gibt an, dass die resultierende ACL zurückgegeben werden soll.</span><span class="sxs-lookup"><span data-stu-id="1ff62-125">Indicates the resulting ACL should be returned.</span></span>

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

### <span data-ttu-id="1ff62-126">-Path</span><span class="sxs-lookup"><span data-stu-id="1ff62-126">-Path</span></span>
<span data-ttu-id="1ff62-127">Gibt den Data Lake Store-Pfad der Datei oder des Ordners an, beginnend mit dem Stammverzeichnis (/).</span><span class="sxs-lookup"><span data-stu-id="1ff62-127">Specifies the Data Lake Store path of the file or folder, starting with the root directory (/).</span></span>

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

### <span data-ttu-id="1ff62-128">-Rekursieren</span><span class="sxs-lookup"><span data-stu-id="1ff62-128">-Recurse</span></span>
<span data-ttu-id="1ff62-129">Gibt die ACL an, die rekursiv auf die untergeordneten Unterverzeichnisse und Dateien festgelegt werden soll</span><span class="sxs-lookup"><span data-stu-id="1ff62-129">Indicates the ACL to be set recursively to the child subdirectories and files</span></span>

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

### <span data-ttu-id="1ff62-130">-ShowProgress</span><span class="sxs-lookup"><span data-stu-id="1ff62-130">-ShowProgress</span></span>
<span data-ttu-id="1ff62-131">Wenn der Status übergeben ist, wird der Status angezeigt.</span><span class="sxs-lookup"><span data-stu-id="1ff62-131">If passed then progress status is showed.</span></span> <span data-ttu-id="1ff62-132">Gilt nur, wenn der rekursive Acl-Satz erledigt ist.</span><span class="sxs-lookup"><span data-stu-id="1ff62-132">Only applicable when recursive Acl set is done.</span></span>

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

### <span data-ttu-id="1ff62-133">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="1ff62-133">-Confirm</span></span>
<span data-ttu-id="1ff62-134">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="1ff62-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1ff62-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1ff62-135">-WhatIf</span></span>
<span data-ttu-id="1ff62-136">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="1ff62-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1ff62-137">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="1ff62-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1ff62-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1ff62-138">CommonParameters</span></span>
<span data-ttu-id="1ff62-139">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1ff62-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1ff62-140">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1ff62-140">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1ff62-141">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="1ff62-141">INPUTS</span></span>

### <span data-ttu-id="1ff62-142">System.String</span><span class="sxs-lookup"><span data-stu-id="1ff62-142">System.String</span></span>

### <span data-ttu-id="1ff62-143">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStorePathInstance</span><span class="sxs-lookup"><span data-stu-id="1ff62-143">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStorePathInstance</span></span>

### <span data-ttu-id="1ff62-144">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStoreItemAce[]</span><span class="sxs-lookup"><span data-stu-id="1ff62-144">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStoreItemAce[]</span></span>

### <span data-ttu-id="1ff62-145">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="1ff62-145">System.Management.Automation.SwitchParameter</span></span>

### <span data-ttu-id="1ff62-146">System.Int32</span><span class="sxs-lookup"><span data-stu-id="1ff62-146">System.Int32</span></span>

## <span data-ttu-id="1ff62-147">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="1ff62-147">OUTPUTS</span></span>

### <span data-ttu-id="1ff62-148">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStoreItemAce</span><span class="sxs-lookup"><span data-stu-id="1ff62-148">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStoreItemAce</span></span>

## <span data-ttu-id="1ff62-149">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="1ff62-149">NOTES</span></span>

## <span data-ttu-id="1ff62-150">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="1ff62-150">RELATED LINKS</span></span>
