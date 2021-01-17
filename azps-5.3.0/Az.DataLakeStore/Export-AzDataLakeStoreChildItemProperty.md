---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeStore.dll-Help.xml
Module Name: Az.DataLakeStore
online version: https://docs.microsoft.com/en-us/powershell/module/az.datalakestore/export-azdatalakestorechilditemproperty
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Export-AzDataLakeStoreChildItemProperty.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Export-AzDataLakeStoreChildItemProperty.md
ms.openlocfilehash: 25615684db8b78a461b39b1a8cfc159d42a56883
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98458100"
---
# <span data-ttu-id="aba89-101">Export-AzDataLakeStoreChildItemProperty</span><span class="sxs-lookup"><span data-stu-id="aba89-101">Export-AzDataLakeStoreChildItemProperty</span></span>

## <span data-ttu-id="aba89-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="aba89-102">SYNOPSIS</span></span>
<span data-ttu-id="aba89-103">Exportiert die Eigenschaften (Datenträgernutzung und Acl) für die gesamte Struktur aus dem angegebenen Pfad in einen Ausgabepfad.</span><span class="sxs-lookup"><span data-stu-id="aba89-103">Exports the properties (Disk usage and Acl) for the entire tree from the specified path to a output path</span></span>

## <span data-ttu-id="aba89-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="aba89-104">SYNTAX</span></span>

### <span data-ttu-id="aba89-105">GetDiskUsage</span><span class="sxs-lookup"><span data-stu-id="aba89-105">GetDiskUsage</span></span>
```
Export-AzDataLakeStoreChildItemProperty [-Account] <String> [-Path] <DataLakeStorePathInstance>
 [-OutputPath] <String> [-SaveToAdl] [-IncludeFile] [-MaximumDepth <Int32>] [-Concurrency <Int32>]
 [-GetDiskUsage] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="aba89-106">GetAllProperties</span><span class="sxs-lookup"><span data-stu-id="aba89-106">GetAllProperties</span></span>
```
Export-AzDataLakeStoreChildItemProperty [-Account] <String> [-Path] <DataLakeStorePathInstance>
 [-OutputPath] <String> [-SaveToAdl] [-IncludeFile] [-MaximumDepth <Int32>] [-Concurrency <Int32>]
 [-GetDiskUsage] [-GetAcl] [-HideConsistentAcl] [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="aba89-107">GetAclDump</span><span class="sxs-lookup"><span data-stu-id="aba89-107">GetAclDump</span></span>
```
Export-AzDataLakeStoreChildItemProperty [-Account] <String> [-Path] <DataLakeStorePathInstance>
 [-OutputPath] <String> [-SaveToAdl] [-IncludeFile] [-MaximumDepth <Int32>] [-Concurrency <Int32>] [-GetAcl]
 [-HideConsistentAcl] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="aba89-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="aba89-108">DESCRIPTION</span></span>
<span data-ttu-id="aba89-109">Die **Export-AzDataLakeStoreChildItemProperty** wird verwendet, um die ADLS-Speicherplatznutzung bzw./und die Verwendung von ACL für das angegebene Verzeichnis und die Unterverzeichnisse und Dateien zu melden.</span><span class="sxs-lookup"><span data-stu-id="aba89-109">The **Export-AzDataLakeStoreChildItemProperty** is used to report the ADLS space usage or/and ACL usage for the given directory and it's sub directories and files.</span></span>

## <span data-ttu-id="aba89-110">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="aba89-110">EXAMPLES</span></span>

### <span data-ttu-id="aba89-111">Beispiel 1: Herunterladen der Datenträgernutzung und der Verwendung von ACL für alle Unterverzeichnisse und Dateien</span><span class="sxs-lookup"><span data-stu-id="aba89-111">Example 1: Get the disk usage and ACL usage for all subdirectories and files</span></span>
```
PS C:\> Export-AzDataLakeStoreChildItemProperty -Account ContosoADL -Path /a -OutputPath "C:\Users\contoso\Desktop\DumpFile.txt" -GetAcl -GetDiskUsage -IncludeFile
```

<span data-ttu-id="aba89-112">Sie können die Datenträgernutzung und die Verwendung des ACL für alle Unterverzeichnisse und Dateien unter "/a" erhalten.</span><span class="sxs-lookup"><span data-stu-id="aba89-112">Get the disk usage and ACL usage for all subdirectories and files under /a.</span></span> <span data-ttu-id="aba89-113">IncludeFile stellt sicher, dass die Verwendung auch für Dateien gemeldet wird</span><span class="sxs-lookup"><span data-stu-id="aba89-113">IncludeFile ensures the usage is reported for files also</span></span>

### <span data-ttu-id="aba89-114">Beispiel 2: Erhalten der Verwendung von ACL für alle Unterverzeichnisse und Dateien mit ausgeblendeter einheitlicher ACL</span><span class="sxs-lookup"><span data-stu-id="aba89-114">Example 2: Get the ACL usage for all subdirectories and files with the consistent ACL hidden</span></span>
```
PS C:\> $fullAcl="user:contoso-userid:--x|user::rwx|other::---|group::rwx"
PS C:\> $newFullAcl = $fullAcl.Split("{|}");
PS C:\> Set-AzDataLakeStoreItemAcl -Account ContosoADL -Path /a -Acl $newFullAcl -Recurse -Debug

PS C:\> Export-AzDataLakeStoreChildItemProperty -Account ContosoADL -Path /a -OutputPath "C:\Users\contoso\Desktop\DumpFile.txt" -GetAcl -HideConsistentAcl -IncludeFile
```

<span data-ttu-id="aba89-115">Verwenden Sie die Verwendung von ACL für alle Unterverzeichnisse und Dateien unter "/a".</span><span class="sxs-lookup"><span data-stu-id="aba89-115">Get the ACL usage for all subdirectories and files under /a.</span></span> <span data-ttu-id="aba89-116">IncludeFile stellt sicher, dass die Verwendung auch für Dateien gemeldet wird.</span><span class="sxs-lookup"><span data-stu-id="aba89-116">IncludeFile ensures the usage is reported for files also.</span></span> <span data-ttu-id="aba89-117">In diesem Fall wird "HideconsistentAcl" die "Acl" von "/a" und nicht "Children" (Kinder) anzeigen, da alle unterg.</span><span class="sxs-lookup"><span data-stu-id="aba89-117">HideconsistentAcl in this case will show the Acl of /a, not it's children since all of the children has same acl as /a.</span></span> <span data-ttu-id="aba89-118">Mit diesem Flag wird die acl-Ausgabe der Unterstruktur übersprungen, wenn alle acls identisch mit dem Stamm sind.</span><span class="sxs-lookup"><span data-stu-id="aba89-118">This flag skips the acl output of subtree if all it's acls are same as the root.</span></span>

## <span data-ttu-id="aba89-119">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="aba89-119">PARAMETERS</span></span>

### <span data-ttu-id="aba89-120">-Konto</span><span class="sxs-lookup"><span data-stu-id="aba89-120">-Account</span></span>
<span data-ttu-id="aba89-121">Das Data Lake Store-Konto zum Ausführen des Dateisystemvorgangs in</span><span class="sxs-lookup"><span data-stu-id="aba89-121">The Data Lake Store account to execute the filesystem operation in</span></span>

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

### <span data-ttu-id="aba89-122">-Parallelität</span><span class="sxs-lookup"><span data-stu-id="aba89-122">-Concurrency</span></span>
<span data-ttu-id="aba89-123">Gibt die Anzahl der parallel verarbeiteten Dateien/Verzeichnisse an.</span><span class="sxs-lookup"><span data-stu-id="aba89-123">Indicates the number of files/directories processed in parallel.</span></span>
<span data-ttu-id="aba89-124">Der Standardwert wird als beste Leistung basierend auf der Systemspezifikation berechnet.</span><span class="sxs-lookup"><span data-stu-id="aba89-124">Default will be computed as a best effort based on system specification.</span></span>

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

### <span data-ttu-id="aba89-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="aba89-125">-DefaultProfile</span></span>
<span data-ttu-id="aba89-126">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="aba89-126">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="aba89-127">-GetAcl</span><span class="sxs-lookup"><span data-stu-id="aba89-127">-GetAcl</span></span>
<span data-ttu-id="aba89-128">Ruft die Acl ab dem Stammpfad ab.</span><span class="sxs-lookup"><span data-stu-id="aba89-128">Retrieves the acl starting from the root path</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: GetAllProperties, GetAclDump
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="aba89-129">-GetDiskUsage</span><span class="sxs-lookup"><span data-stu-id="aba89-129">-GetDiskUsage</span></span>
<span data-ttu-id="aba89-130">Ruft die Datenträgernutzung ab dem Stammpfad ab.</span><span class="sxs-lookup"><span data-stu-id="aba89-130">Retrieves the disk usage starting from the root path</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: GetDiskUsage, GetAllProperties
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="aba89-131">-HideConsistentAcl</span><span class="sxs-lookup"><span data-stu-id="aba89-131">-HideConsistentAcl</span></span>
<span data-ttu-id="aba89-132">Zeigen Sie keine Verzeichnisunterstruktur an, wenn die ACLs in der gesamten Unterstruktur gleich sind.</span><span class="sxs-lookup"><span data-stu-id="aba89-132">Do not show directory subtree if the ACLs are the same throughout the entire subtree.</span></span> <span data-ttu-id="aba89-133">Dadurch sind nur die Pfade leichter zu erkennen, bis zu denen sich die ACLs unterscheiden. Wenn beispielsweise alle Dateien und Ordner unter "/a/b" identisch sind, zeigen Sie nicht die Unterstruktur "/a/b" an, und geben Sie einfach "/a/b" mit "True" in der Spalte "Consistent ACL" ein, wenn "IncludeFiles" nicht festgelegt ist, da eine konsistente Acl nicht ermittelt werden kann, ohne dass Acl für die Dateien abgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="aba89-133">This makes it easier to see only the paths up to which the ACLs differ.For example if all files and folders under /a/b are the same, do not show the subtreeunder /a/b, and just output /a/b with 'True' in the Consistent ACL columnCannot be set if IncludeFiles is not set, because consistent Acl cannot be determined without retrieving acls for the files.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: GetAllProperties, GetAclDump
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="aba89-134">-IncludeFile</span><span class="sxs-lookup"><span data-stu-id="aba89-134">-IncludeFile</span></span>
<span data-ttu-id="aba89-135">Anzeigen von Statistiken auf Dateiebene (standardmäßig werden nur Informationen auf Verzeichnisebene angezeigt)</span><span class="sxs-lookup"><span data-stu-id="aba89-135">Show stats at file level (default is to show directory-level info only)</span></span>

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

### <span data-ttu-id="aba89-136">-MaximumDepth</span><span class="sxs-lookup"><span data-stu-id="aba89-136">-MaximumDepth</span></span>
<span data-ttu-id="aba89-137">Maximale Tiefe aus dem Stammverzeichnis bis zur Anzeige der Datenträgernutzung oder des Acl</span><span class="sxs-lookup"><span data-stu-id="aba89-137">Maximum depth from the root directory till which disk usage or acl is displayed</span></span>

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

### <span data-ttu-id="aba89-138">-OutputPath</span><span class="sxs-lookup"><span data-stu-id="aba89-138">-OutputPath</span></span>
<span data-ttu-id="aba89-139">Pfad zur Ausgabedatei.</span><span class="sxs-lookup"><span data-stu-id="aba89-139">Path to output file.</span></span> <span data-ttu-id="aba89-140">Kann ein lokaler Pfad oder ein "Adl-Pfad" sein.</span><span class="sxs-lookup"><span data-stu-id="aba89-140">Can be a Local path or Adl Path.</span></span> <span data-ttu-id="aba89-141">Standardmäßig ist sie lokal.</span><span class="sxs-lookup"><span data-stu-id="aba89-141">By default it is local.</span></span> <span data-ttu-id="aba89-142">Wenn "SaveToAdl" angegeben ist, handelt es sich um einen ADL-Pfad im selben Konto.</span><span class="sxs-lookup"><span data-stu-id="aba89-142">If SaveToAdl is specified then it is an ADL path in the same account</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="aba89-143">-PassThru</span><span class="sxs-lookup"><span data-stu-id="aba89-143">-PassThru</span></span>
<span data-ttu-id="aba89-144">Gibt an, dass eine boolesche Antwort zurückgegeben werden sollte, die das Ergebnis des Löschvorgangs angibt.</span><span class="sxs-lookup"><span data-stu-id="aba89-144">Indicates a boolean response should be returned indicating the result of the delete operation.</span></span>

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

### <span data-ttu-id="aba89-145">-Path</span><span class="sxs-lookup"><span data-stu-id="aba89-145">-Path</span></span>
<span data-ttu-id="aba89-146">Der Pfad im angegebenen Data Lake-Konto, das abgerufen werden soll.</span><span class="sxs-lookup"><span data-stu-id="aba89-146">The path in the specified Data Lake account that should be retrieve.</span></span>
<span data-ttu-id="aba89-147">Kann eine Datei oder ein Ordner im Format '/folder/file.txt' sein, wobei das erste "/" nach dem DNS den Stamm des Dateisystems angibt.</span><span class="sxs-lookup"><span data-stu-id="aba89-147">Can be a file or folder In the format '/folder/file.txt', where the first '/' after the DNS indicates the root of the file system.</span></span>

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

### <span data-ttu-id="aba89-148">-SaveToAdl</span><span class="sxs-lookup"><span data-stu-id="aba89-148">-SaveToAdl</span></span>
<span data-ttu-id="aba89-149">Wenn sie übergeben wird, wird die Dumpdatei in ADL gespeichert.</span><span class="sxs-lookup"><span data-stu-id="aba89-149">If passed then saves the dump file to ADL.</span></span>
<span data-ttu-id="aba89-150">In diesem Fall ist "DumpFile" ein ADL-Pfad.</span><span class="sxs-lookup"><span data-stu-id="aba89-150">The DumpFile wil be a ADL path in that case</span></span>

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

### <span data-ttu-id="aba89-151">-Confirm</span><span class="sxs-lookup"><span data-stu-id="aba89-151">-Confirm</span></span>
<span data-ttu-id="aba89-152">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="aba89-152">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="aba89-153">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="aba89-153">-WhatIf</span></span>
<span data-ttu-id="aba89-154">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="aba89-154">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="aba89-155">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="aba89-155">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="aba89-156">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="aba89-156">CommonParameters</span></span>
<span data-ttu-id="aba89-157">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="aba89-157">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="aba89-158">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="aba89-158">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="aba89-159">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="aba89-159">INPUTS</span></span>

### <span data-ttu-id="aba89-160">System.String</span><span class="sxs-lookup"><span data-stu-id="aba89-160">System.String</span></span>

### <span data-ttu-id="aba89-161">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStorePathInstance</span><span class="sxs-lookup"><span data-stu-id="aba89-161">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStorePathInstance</span></span>

### <span data-ttu-id="aba89-162">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="aba89-162">System.Management.Automation.SwitchParameter</span></span>

### <span data-ttu-id="aba89-163">System.Int32</span><span class="sxs-lookup"><span data-stu-id="aba89-163">System.Int32</span></span>

## <span data-ttu-id="aba89-164">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="aba89-164">OUTPUTS</span></span>

### <span data-ttu-id="aba89-165">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="aba89-165">System.Boolean</span></span>

## <span data-ttu-id="aba89-166">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="aba89-166">NOTES</span></span>

## <span data-ttu-id="aba89-167">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="aba89-167">RELATED LINKS</span></span>
