---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeStore.dll-Help.xml
Module Name: Az.DataLakeStore
online version: https://docs.microsoft.com/powershell/module/az.datalakestore/export-azdatalakestorechilditemproperty
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Export-AzDataLakeStoreChildItemProperty.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Export-AzDataLakeStoreChildItemProperty.md
ms.openlocfilehash: 0f43c372901dbfd571343584f0ca8479d5b7081e
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101949448"
---
# <span data-ttu-id="8b0fd-101">Export-AzDataLakeStoreChildItemProperty</span><span class="sxs-lookup"><span data-stu-id="8b0fd-101">Export-AzDataLakeStoreChildItemProperty</span></span>

## <span data-ttu-id="8b0fd-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8b0fd-102">SYNOPSIS</span></span>
<span data-ttu-id="8b0fd-103">Exportiert die Eigenschaften (Datenträgernutzung und Acl) für die gesamte Struktur aus dem angegebenen Pfad in einen Ausgabepfad.</span><span class="sxs-lookup"><span data-stu-id="8b0fd-103">Exports the properties (Disk usage and Acl) for the entire tree from the specified path to a output path</span></span>

## <span data-ttu-id="8b0fd-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="8b0fd-104">SYNTAX</span></span>

### <span data-ttu-id="8b0fd-105">GetDiskUsage</span><span class="sxs-lookup"><span data-stu-id="8b0fd-105">GetDiskUsage</span></span>
```
Export-AzDataLakeStoreChildItemProperty [-Account] <String> [-Path] <DataLakeStorePathInstance>
 [-OutputPath] <String> [-SaveToAdl] [-IncludeFile] [-MaximumDepth <Int32>] [-Concurrency <Int32>]
 [-GetDiskUsage] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="8b0fd-106">GetAllProperties</span><span class="sxs-lookup"><span data-stu-id="8b0fd-106">GetAllProperties</span></span>
```
Export-AzDataLakeStoreChildItemProperty [-Account] <String> [-Path] <DataLakeStorePathInstance>
 [-OutputPath] <String> [-SaveToAdl] [-IncludeFile] [-MaximumDepth <Int32>] [-Concurrency <Int32>]
 [-GetDiskUsage] [-GetAcl] [-HideConsistentAcl] [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8b0fd-107">GetAclDump</span><span class="sxs-lookup"><span data-stu-id="8b0fd-107">GetAclDump</span></span>
```
Export-AzDataLakeStoreChildItemProperty [-Account] <String> [-Path] <DataLakeStorePathInstance>
 [-OutputPath] <String> [-SaveToAdl] [-IncludeFile] [-MaximumDepth <Int32>] [-Concurrency <Int32>] [-GetAcl]
 [-HideConsistentAcl] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="8b0fd-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="8b0fd-108">DESCRIPTION</span></span>
<span data-ttu-id="8b0fd-109">Die **Export-AzDataLakeStoreChildItemProperty** wird verwendet, um die ADLS-Speicherplatznutzung oder/und ACL-Nutzung für das angegebene Verzeichnis und seine Unterverzeichnisse und Dateien zu melden.</span><span class="sxs-lookup"><span data-stu-id="8b0fd-109">The **Export-AzDataLakeStoreChildItemProperty** is used to report the ADLS space usage or/and ACL usage for the given directory and it's sub directories and files.</span></span>

## <span data-ttu-id="8b0fd-110">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="8b0fd-110">EXAMPLES</span></span>

### <span data-ttu-id="8b0fd-111">Beispiel 1: Herunterladen der Datenträgernutzung und der ACL-Nutzung für alle Unterverzeichnisse und Dateien</span><span class="sxs-lookup"><span data-stu-id="8b0fd-111">Example 1: Get the disk usage and ACL usage for all subdirectories and files</span></span>
```
PS C:\> Export-AzDataLakeStoreChildItemProperty -Account ContosoADL -Path /a -OutputPath "C:\Users\contoso\Desktop\DumpFile.txt" -GetAcl -GetDiskUsage -IncludeFile
```

<span data-ttu-id="8b0fd-112">Holen Sie sich die Datenträgernutzung und die ACL-Nutzung für alle Unterverzeichnisse und Dateien unter /a.</span><span class="sxs-lookup"><span data-stu-id="8b0fd-112">Get the disk usage and ACL usage for all subdirectories and files under /a.</span></span> <span data-ttu-id="8b0fd-113">IncludeFile stellt sicher, dass die Verwendung auch für Dateien gemeldet wird</span><span class="sxs-lookup"><span data-stu-id="8b0fd-113">IncludeFile ensures the usage is reported for files also</span></span>

### <span data-ttu-id="8b0fd-114">Beispiel 2: Verwenden der ACL für alle Unterverzeichnisse und Dateien mit ausgeblendeter konsistenter ACL</span><span class="sxs-lookup"><span data-stu-id="8b0fd-114">Example 2: Get the ACL usage for all subdirectories and files with the consistent ACL hidden</span></span>
```
PS C:\> $fullAcl="user:contoso-userid:--x|user::rwx|other::---|group::rwx"
PS C:\> $newFullAcl = $fullAcl.Split("{|}");
PS C:\> Set-AzDataLakeStoreItemAcl -Account ContosoADL -Path /a -Acl $newFullAcl -Recurse -Debug

PS C:\> Export-AzDataLakeStoreChildItemProperty -Account ContosoADL -Path /a -OutputPath "C:\Users\contoso\Desktop\DumpFile.txt" -GetAcl -HideConsistentAcl -IncludeFile
```

<span data-ttu-id="8b0fd-115">Holen Sie sich die ACL-Verwendung für alle Unterverzeichnisse und Dateien unter /a.</span><span class="sxs-lookup"><span data-stu-id="8b0fd-115">Get the ACL usage for all subdirectories and files under /a.</span></span> <span data-ttu-id="8b0fd-116">IncludeFile stellt sicher, dass die Verwendung auch für Dateien gemeldet wird.</span><span class="sxs-lookup"><span data-stu-id="8b0fd-116">IncludeFile ensures the usage is reported for files also.</span></span> <span data-ttu-id="8b0fd-117">HideconsistentAcl zeigt in diesem Fall die Acl von /a an, nicht die "children", da alle Kinder die gleiche acl wie /a haben.</span><span class="sxs-lookup"><span data-stu-id="8b0fd-117">HideconsistentAcl in this case will show the Acl of /a, not it's children since all of the children has same acl as /a.</span></span> <span data-ttu-id="8b0fd-118">Mit diesem Flag wird die acl-Ausgabe der Unterstruktur übersprungen, wenn alle acls mit dem Stamm identisch sind.</span><span class="sxs-lookup"><span data-stu-id="8b0fd-118">This flag skips the acl output of subtree if all it's acls are same as the root.</span></span>

## <span data-ttu-id="8b0fd-119">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="8b0fd-119">PARAMETERS</span></span>

### <span data-ttu-id="8b0fd-120">-Konto</span><span class="sxs-lookup"><span data-stu-id="8b0fd-120">-Account</span></span>
<span data-ttu-id="8b0fd-121">Das Data Lake Store-Konto zum Ausführen des Dateisystemvorgangs in</span><span class="sxs-lookup"><span data-stu-id="8b0fd-121">The Data Lake Store account to execute the filesystem operation in</span></span>

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

### <span data-ttu-id="8b0fd-122">-Parallelität</span><span class="sxs-lookup"><span data-stu-id="8b0fd-122">-Concurrency</span></span>
<span data-ttu-id="8b0fd-123">Gibt die Anzahl der parallel verarbeiteten Dateien/Verzeichnisse an.</span><span class="sxs-lookup"><span data-stu-id="8b0fd-123">Indicates the number of files/directories processed in parallel.</span></span>
<span data-ttu-id="8b0fd-124">Der Standardwert wird als optimaler Aufwand basierend auf der Systemspezifikation berechnet.</span><span class="sxs-lookup"><span data-stu-id="8b0fd-124">Default will be computed as a best effort based on system specification.</span></span>

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

### <span data-ttu-id="8b0fd-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8b0fd-125">-DefaultProfile</span></span>
<span data-ttu-id="8b0fd-126">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="8b0fd-126">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8b0fd-127">-GetAcl</span><span class="sxs-lookup"><span data-stu-id="8b0fd-127">-GetAcl</span></span>
<span data-ttu-id="8b0fd-128">Ruft die Acl ab dem Stammpfad ab.</span><span class="sxs-lookup"><span data-stu-id="8b0fd-128">Retrieves the acl starting from the root path</span></span>

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

### <span data-ttu-id="8b0fd-129">-GetDiskUsage</span><span class="sxs-lookup"><span data-stu-id="8b0fd-129">-GetDiskUsage</span></span>
<span data-ttu-id="8b0fd-130">Ruft die Datenträgernutzung ab dem Stammpfad ab.</span><span class="sxs-lookup"><span data-stu-id="8b0fd-130">Retrieves the disk usage starting from the root path</span></span>

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

### <span data-ttu-id="8b0fd-131">-HideConsistentAcl</span><span class="sxs-lookup"><span data-stu-id="8b0fd-131">-HideConsistentAcl</span></span>
<span data-ttu-id="8b0fd-132">Zeigen Sie keine Verzeichnisunterstruktur an, wenn die ACLs in der gesamten Unterstruktur identisch sind.</span><span class="sxs-lookup"><span data-stu-id="8b0fd-132">Do not show directory subtree if the ACLs are the same throughout the entire subtree.</span></span> <span data-ttu-id="8b0fd-133">Dadurch können nur die Pfade leichter zu sehen sein, bis zu denen sich die ACLs unterscheiden. Wenn z. B. alle Dateien und Ordner unter /a/b identisch sind, zeigen Sie nicht die Unterstruktur unter /a/b an, und geben Sie einfach /a/b mit "True" in der Spalte Konsistente ACL aus. Kann nicht festgelegt werden, wenn IncludeFiles nicht festgelegt ist, da konsistente Acl nicht ohne Abrufen von Acls für die Dateien bestimmt werden kann.</span><span class="sxs-lookup"><span data-stu-id="8b0fd-133">This makes it easier to see only the paths up to which the ACLs differ.For example if all files and folders under /a/b are the same, do not show the subtreeunder /a/b, and just output /a/b with 'True' in the Consistent ACL columnCannot be set if IncludeFiles is not set, because consistent Acl cannot be determined without retrieving acls for the files.</span></span>

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

### <span data-ttu-id="8b0fd-134">-IncludeFile</span><span class="sxs-lookup"><span data-stu-id="8b0fd-134">-IncludeFile</span></span>
<span data-ttu-id="8b0fd-135">Anzeigen von Statistiken auf Dateiebene (standardmäßig werden nur Informationen auf Verzeichnisebene angezeigt)</span><span class="sxs-lookup"><span data-stu-id="8b0fd-135">Show stats at file level (default is to show directory-level info only)</span></span>

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

### <span data-ttu-id="8b0fd-136">-MaximumDepth</span><span class="sxs-lookup"><span data-stu-id="8b0fd-136">-MaximumDepth</span></span>
<span data-ttu-id="8b0fd-137">Maximale Tiefe vom Stammverzeichnis bis zur Anzeige der Datenträgernutzung oder -acl</span><span class="sxs-lookup"><span data-stu-id="8b0fd-137">Maximum depth from the root directory till which disk usage or acl is displayed</span></span>

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

### <span data-ttu-id="8b0fd-138">-OutputPath</span><span class="sxs-lookup"><span data-stu-id="8b0fd-138">-OutputPath</span></span>
<span data-ttu-id="8b0fd-139">Pfad zur Ausgabedatei.</span><span class="sxs-lookup"><span data-stu-id="8b0fd-139">Path to output file.</span></span> <span data-ttu-id="8b0fd-140">Kann ein lokaler Pfad oder ein Adlpfad sein.</span><span class="sxs-lookup"><span data-stu-id="8b0fd-140">Can be a Local path or Adl Path.</span></span> <span data-ttu-id="8b0fd-141">Standardmäßig ist es lokal.</span><span class="sxs-lookup"><span data-stu-id="8b0fd-141">By default it is local.</span></span> <span data-ttu-id="8b0fd-142">Wenn SaveToAdl angegeben ist, handelt es sich um einen ADL-Pfad in demselben Konto.</span><span class="sxs-lookup"><span data-stu-id="8b0fd-142">If SaveToAdl is specified then it is an ADL path in the same account</span></span>

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

### <span data-ttu-id="8b0fd-143">-PassThru</span><span class="sxs-lookup"><span data-stu-id="8b0fd-143">-PassThru</span></span>
<span data-ttu-id="8b0fd-144">Gibt an, dass eine boolesche Antwort zurückgegeben werden soll, die das Ergebnis des Löschvorgangs angibt.</span><span class="sxs-lookup"><span data-stu-id="8b0fd-144">Indicates a boolean response should be returned indicating the result of the delete operation.</span></span>

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

### <span data-ttu-id="8b0fd-145">-Path</span><span class="sxs-lookup"><span data-stu-id="8b0fd-145">-Path</span></span>
<span data-ttu-id="8b0fd-146">Der Pfad im angegebenen Data Lake-Konto, der abgerufen werden soll.</span><span class="sxs-lookup"><span data-stu-id="8b0fd-146">The path in the specified Data Lake account that should be retrieve.</span></span>
<span data-ttu-id="8b0fd-147">Kann eine Datei oder ein Ordner im Format "/folder/file.txt" sein, wobei das erste "/" nach dem DNS den Stamm des Dateisystems angibt.</span><span class="sxs-lookup"><span data-stu-id="8b0fd-147">Can be a file or folder In the format '/folder/file.txt', where the first '/' after the DNS indicates the root of the file system.</span></span>

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

### <span data-ttu-id="8b0fd-148">-SaveToAdl</span><span class="sxs-lookup"><span data-stu-id="8b0fd-148">-SaveToAdl</span></span>
<span data-ttu-id="8b0fd-149">Wenn übergeben, wird die Dumpdatei in ADL gespeichert.</span><span class="sxs-lookup"><span data-stu-id="8b0fd-149">If passed then saves the dump file to ADL.</span></span>
<span data-ttu-id="8b0fd-150">Die DumpFile ist in diesem Fall ein ADL-Pfad.</span><span class="sxs-lookup"><span data-stu-id="8b0fd-150">The DumpFile wil be a ADL path in that case</span></span>

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

### <span data-ttu-id="8b0fd-151">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="8b0fd-151">-Confirm</span></span>
<span data-ttu-id="8b0fd-152">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="8b0fd-152">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8b0fd-153">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8b0fd-153">-WhatIf</span></span>
<span data-ttu-id="8b0fd-154">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="8b0fd-154">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8b0fd-155">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="8b0fd-155">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8b0fd-156">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8b0fd-156">CommonParameters</span></span>
<span data-ttu-id="8b0fd-157">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8b0fd-157">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8b0fd-158">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8b0fd-158">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8b0fd-159">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="8b0fd-159">INPUTS</span></span>

### <span data-ttu-id="8b0fd-160">System.String</span><span class="sxs-lookup"><span data-stu-id="8b0fd-160">System.String</span></span>

### <span data-ttu-id="8b0fd-161">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStorePathInstance</span><span class="sxs-lookup"><span data-stu-id="8b0fd-161">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStorePathInstance</span></span>

### <span data-ttu-id="8b0fd-162">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="8b0fd-162">System.Management.Automation.SwitchParameter</span></span>

### <span data-ttu-id="8b0fd-163">System.Int32</span><span class="sxs-lookup"><span data-stu-id="8b0fd-163">System.Int32</span></span>

## <span data-ttu-id="8b0fd-164">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="8b0fd-164">OUTPUTS</span></span>

### <span data-ttu-id="8b0fd-165">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="8b0fd-165">System.Boolean</span></span>

## <span data-ttu-id="8b0fd-166">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="8b0fd-166">NOTES</span></span>

## <span data-ttu-id="8b0fd-167">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="8b0fd-167">RELATED LINKS</span></span>
