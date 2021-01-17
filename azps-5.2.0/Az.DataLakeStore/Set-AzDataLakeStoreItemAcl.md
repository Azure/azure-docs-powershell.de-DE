---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeStore.dll-Help.xml
Module Name: Az.DataLakeStore
ms.assetid: FFB335D4-AE3E-4788-B6FD-9AFC36F52B61
online version: https://docs.microsoft.com/en-us/powershell/module/az.datalakestore/set-azdatalakestoreitemacl
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Set-AzDataLakeStoreItemAcl.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Set-AzDataLakeStoreItemAcl.md
ms.openlocfilehash: 8b3412acd7513718c8c34e3fc8bb10c5e33f11a8
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98362772"
---
# <span data-ttu-id="b41b0-101">Set-AzDataLakeStoreItemAcl</span><span class="sxs-lookup"><span data-stu-id="b41b0-101">Set-AzDataLakeStoreItemAcl</span></span>

## <span data-ttu-id="b41b0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b41b0-102">SYNOPSIS</span></span>
<span data-ttu-id="b41b0-103">Ändert die ACL einer Datei oder eines Ordners im Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="b41b0-103">Modifies the ACL of a file or folder in Data Lake Store.</span></span>

## <span data-ttu-id="b41b0-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="b41b0-104">SYNTAX</span></span>

```
Set-AzDataLakeStoreItemAcl [-Account] <String> [-Path] <DataLakeStorePathInstance>
 [-Acl] <DataLakeStoreItemAce[]> [-PassThru] [-Recurse] [-Concurrency <Int32>] [-ShowProgress]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b41b0-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="b41b0-105">DESCRIPTION</span></span>
<span data-ttu-id="b41b0-106">Das **Cmdlet "Set-AzDataLakeStoreItemAcl"** ändert die Zugriffssteuerungsliste (Access Control List, ACL) einer Datei oder eines Ordners im Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="b41b0-106">The **Set-AzDataLakeStoreItemAcl** cmdlet modifies the access control list (ACL) of a file or folder in Data Lake Store.</span></span>

## <span data-ttu-id="b41b0-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="b41b0-107">EXAMPLES</span></span>

### <span data-ttu-id="b41b0-108">Beispiel 1: Festlegen der ACL für eine Datei und einen Ordner</span><span class="sxs-lookup"><span data-stu-id="b41b0-108">Example 1: Set the ACL for a file and a folder</span></span>
```
PS C:\>$ACL = Get-AzDataLakeStoreItemAclEntry -AccountName "ContosoADL" -Path /
PS C:\> Set-AzDataLakeStoreItemAcl -AccountName "ContosoADL" -Path "/MyFiles/Test.txt" -Acl $ACL
```

<span data-ttu-id="b41b0-109">Der erste Befehl ruft die ACL für das Stammverzeichnis des ContosoADL-Kontos ab und speichert sie dann in der $ACL Variable.</span><span class="sxs-lookup"><span data-stu-id="b41b0-109">The first command gets the ACL for the root directory of the ContosoADL account, and then stores it in the $ACL variable.</span></span>
<span data-ttu-id="b41b0-110">Mit dem zweiten Befehl wird die ACL für die Dateidatei Test.txt auf die in der Datei gespeicherte $ACL.</span><span class="sxs-lookup"><span data-stu-id="b41b0-110">The second command sets the ACL for the file Test.txt to the one in $ACL.</span></span>

### <span data-ttu-id="b41b0-111">Beispiel 2: Rekursiv festlegen der ACL für den Ordner</span><span class="sxs-lookup"><span data-stu-id="b41b0-111">Example 2: Set the ACL for folder recursively</span></span>
```
PS C:\>$ACL = Get-AzDataLakeStoreItemAclEntry -AccountName "ContosoADL" -Path /Folder1
PS C:\> Set-AzDataLakeStoreItemAcl -AccountName "ContosoADL" -Path "/Folder2" -Acl $ACL -Recurse -Concurrency 128
```

<span data-ttu-id="b41b0-112">Der erste Befehl ruft die ACL für den Verzeichnisordner1 des ContosoADL-Kontos ab und speichert sie dann in der $ACL Variable.</span><span class="sxs-lookup"><span data-stu-id="b41b0-112">The first command gets the ACL for the directory Folder1 of the ContosoADL account, and then stores it in the $ACL variable.</span></span>
<span data-ttu-id="b41b0-113">Mit dem zweiten Befehl wird die ACL rekursiv auf "Folder2" und die untergeordneten Verzeichnisse und Dateien auf das Verzeichnis in $ACL.</span><span class="sxs-lookup"><span data-stu-id="b41b0-113">The second command sets the ACL recursively to Folder2 and its sub directories and files to the one in $ACL.</span></span>

## <span data-ttu-id="b41b0-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="b41b0-114">PARAMETERS</span></span>

### <span data-ttu-id="b41b0-115">-Konto</span><span class="sxs-lookup"><span data-stu-id="b41b0-115">-Account</span></span>
<span data-ttu-id="b41b0-116">Gibt den Namen des Data Lake Store-Kontos an.</span><span class="sxs-lookup"><span data-stu-id="b41b0-116">Specifies the name of the Data Lake Store account.</span></span>

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

### <span data-ttu-id="b41b0-117">-Acl</span><span class="sxs-lookup"><span data-stu-id="b41b0-117">-Acl</span></span>
<span data-ttu-id="b41b0-118">Gibt eine ACL für eine Datei oder einen Ordner an.</span><span class="sxs-lookup"><span data-stu-id="b41b0-118">Specifies an ACL for a file or a folder.</span></span>

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

### <span data-ttu-id="b41b0-119">-Parallelität</span><span class="sxs-lookup"><span data-stu-id="b41b0-119">-Concurrency</span></span>
<span data-ttu-id="b41b0-120">Die Anzahl der parallel verarbeiteten Dateien/Verzeichnisse.</span><span class="sxs-lookup"><span data-stu-id="b41b0-120">Number of files/directories processed in parallel.</span></span> <span data-ttu-id="b41b0-121">Optional: Es wird ein angemessener Standardwert ausgewählt.</span><span class="sxs-lookup"><span data-stu-id="b41b0-121">Optional: a reasonable default will be selected.</span></span>

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

### <span data-ttu-id="b41b0-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b41b0-122">-DefaultProfile</span></span>
<span data-ttu-id="b41b0-123">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="b41b0-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b41b0-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="b41b0-124">-PassThru</span></span>
<span data-ttu-id="b41b0-125">Gibt an, dass die resultierende ACL zurückgegeben werden soll.</span><span class="sxs-lookup"><span data-stu-id="b41b0-125">Indicates the resulting ACL should be returned.</span></span>

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

### <span data-ttu-id="b41b0-126">-Path</span><span class="sxs-lookup"><span data-stu-id="b41b0-126">-Path</span></span>
<span data-ttu-id="b41b0-127">Gibt den Data Lake Store-Pfad der Datei oder des Ordners an, beginnend mit dem Stammverzeichnis (/).</span><span class="sxs-lookup"><span data-stu-id="b41b0-127">Specifies the Data Lake Store path of the file or folder, starting with the root directory (/).</span></span>

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

### <span data-ttu-id="b41b0-128">-Recurse</span><span class="sxs-lookup"><span data-stu-id="b41b0-128">-Recurse</span></span>
<span data-ttu-id="b41b0-129">Gibt an, dass die ACL rekursiv für die untergeordneten Unterverzeichnisse und Dateien festgelegt werden soll</span><span class="sxs-lookup"><span data-stu-id="b41b0-129">Indicates the ACL to be set recursively to the child subdirectories and files</span></span>

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

### <span data-ttu-id="b41b0-130">-ShowProgress</span><span class="sxs-lookup"><span data-stu-id="b41b0-130">-ShowProgress</span></span>
<span data-ttu-id="b41b0-131">Wenn der Status erfolgreich ist, wird der Status angezeigt.</span><span class="sxs-lookup"><span data-stu-id="b41b0-131">If passed then progress status is showed.</span></span> <span data-ttu-id="b41b0-132">Gilt nur, wenn der rekursive Acl-Satz erfolgt.</span><span class="sxs-lookup"><span data-stu-id="b41b0-132">Only applicable when recursive Acl set is done.</span></span>

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

### <span data-ttu-id="b41b0-133">-Confirm</span><span class="sxs-lookup"><span data-stu-id="b41b0-133">-Confirm</span></span>
<span data-ttu-id="b41b0-134">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="b41b0-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b41b0-135">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="b41b0-135">-WhatIf</span></span>
<span data-ttu-id="b41b0-136">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="b41b0-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b41b0-137">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="b41b0-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b41b0-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b41b0-138">CommonParameters</span></span>
<span data-ttu-id="b41b0-139">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b41b0-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b41b0-140">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b41b0-140">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b41b0-141">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="b41b0-141">INPUTS</span></span>

### <span data-ttu-id="b41b0-142">System.String</span><span class="sxs-lookup"><span data-stu-id="b41b0-142">System.String</span></span>

### <span data-ttu-id="b41b0-143">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStorePathInstance</span><span class="sxs-lookup"><span data-stu-id="b41b0-143">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStorePathInstance</span></span>

### <span data-ttu-id="b41b0-144">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStoreItemAce[]</span><span class="sxs-lookup"><span data-stu-id="b41b0-144">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStoreItemAce[]</span></span>

### <span data-ttu-id="b41b0-145">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="b41b0-145">System.Management.Automation.SwitchParameter</span></span>

### <span data-ttu-id="b41b0-146">System.Int32</span><span class="sxs-lookup"><span data-stu-id="b41b0-146">System.Int32</span></span>

## <span data-ttu-id="b41b0-147">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="b41b0-147">OUTPUTS</span></span>

### <span data-ttu-id="b41b0-148">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStoreItemAce</span><span class="sxs-lookup"><span data-stu-id="b41b0-148">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStoreItemAce</span></span>

## <span data-ttu-id="b41b0-149">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="b41b0-149">NOTES</span></span>

## <span data-ttu-id="b41b0-150">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="b41b0-150">RELATED LINKS</span></span>
