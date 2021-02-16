---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/get-azdatalakegen2childitem
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzDataLakeGen2ChildItem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzDataLakeGen2ChildItem.md
ms.openlocfilehash: 9160eabf2492969ad7fa3916791854abd4ef6c44
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100155068"
---
# <span data-ttu-id="2dcb0-101">Get-AzDataLakeGen2ChildItem</span><span class="sxs-lookup"><span data-stu-id="2dcb0-101">Get-AzDataLakeGen2ChildItem</span></span>

## <span data-ttu-id="2dcb0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2dcb0-102">SYNOPSIS</span></span>
<span data-ttu-id="2dcb0-103">Listet Unterverzeichnisse und Dateien aus einem Verzeichnis- oder Dateisystemstamm auf.</span><span class="sxs-lookup"><span data-stu-id="2dcb0-103">Lists sub directorys and files from a directory or filesystem root.</span></span>

## <span data-ttu-id="2dcb0-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="2dcb0-104">SYNTAX</span></span>

```
Get-AzDataLakeGen2ChildItem [-FileSystem] <String> [[-Path] <String>] [-FetchProperty] [-Recurse]
 [-MaxCount <Int32>] [-ContinuationToken <String>] [-AsJob] [-OutputUserPrincipalName]
 [-Context <IStorageContext>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="2dcb0-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="2dcb0-105">DESCRIPTION</span></span>
<span data-ttu-id="2dcb0-106">Das **Cmdlet "Get-AzDataLakeGen2ChildItem"** listet Unterverzeichnisse und Dateien in einem Verzeichnis oder Filesystem in einem Azure-Speicherkonto auf.</span><span class="sxs-lookup"><span data-stu-id="2dcb0-106">The **Get-AzDataLakeGen2ChildItem** cmdlet lists sub directorys and files in a directory or Filesystem in an Azure storage account.</span></span>
<span data-ttu-id="2dcb0-107">Dieses Cmdlet funktioniert nur, wenn der hierarchische Namespace für das Konto "Storage" aktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="2dcb0-107">This cmdlet only works if Hierarchical Namespace is enabled for the Storage account.</span></span> <span data-ttu-id="2dcb0-108">Diese Art von Konto kann durch Ausführen des Cmdlets "New-AzStorageAccount" mit "-EnableHierarchicalNamespace $true" erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="2dcb0-108">This kind of account can be created by run "New-AzStorageAccount" cmdlet with "-EnableHierarchicalNamespace $true".</span></span>

## <span data-ttu-id="2dcb0-109">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="2dcb0-109">EXAMPLES</span></span>

### <span data-ttu-id="2dcb0-110">Beispiel 1: Auflisten der direkten untergeordneten Elemente aus einem Filesystem</span><span class="sxs-lookup"><span data-stu-id="2dcb0-110">Example 1: List the direct sub items from a Filesystem</span></span>
```
PS C:\>Get-AzDataLakeGen2ChildItem -FileSystem "filesystem1" 

   FileSystem Name: filesystem1

Path                 IsDirectory  Length          LastModified         Permissions  Owner                Group               
----                 -----------  ------          ------------         -----------  -----                -----               
dir1                 True                         2020-03-13 13:07:34Z rwxr-x---    $superuser           $superuser          
dir2                 True                         2020-03-23 09:28:36Z rwxr-x---    $superuser           $superuser
```

<span data-ttu-id="2dcb0-111">Dieser Befehl listet die direkten untergeordneten Elemente aus einem Filesystem auf.</span><span class="sxs-lookup"><span data-stu-id="2dcb0-111">This command lists the direct sub items from a Filesystem</span></span>

### <span data-ttu-id="2dcb0-112">Beispiel 2: Rekursiv aus einem Verzeichnis auflisten und Eigenschaften/ACL abrufen</span><span class="sxs-lookup"><span data-stu-id="2dcb0-112">Example 2: List recursively from a directory, and fetch Properties/ACL</span></span>
```
PS C:\>Get-AzDataLakeGen2ChildItem -FileSystem "filesystem1" -Path "dir1/" -Recurse -FetchProperty

   FileSystem Name: filesystem1

Path                 IsDirectory  Length          LastModified         Permissions  Owner                Group               
----                 -----------  ------          ------------         -----------  -----                -----               
dir1/dir3            True                         2020-03-23 09:34:31Z rwx---rwx    $superuser           $superuser          
dir1/file1           False        1024            2020-03-23 09:29:18Z rwx---rwx    $superuser           $superuser           
dir1/testfile_1K_0   False        1024            2020-03-23 09:29:21Z rw-r-----    $superuser           $superuser
```

<span data-ttu-id="2dcb0-113">Dieser Befehl listet die direkten untergeordneten Elemente aus einem Filesystem auf.</span><span class="sxs-lookup"><span data-stu-id="2dcb0-113">This command lists the direct sub items from a Filesystem</span></span>

### <span data-ttu-id="2dcb0-114">Beispiel 3: Rekursives Auflisten von Elementen aus einem Filesystem in mehreren Batches</span><span class="sxs-lookup"><span data-stu-id="2dcb0-114">Example 3: List items recursively from a Filesystem in multiple batches</span></span>
```
PS C:\> $MaxReturn = 10000
PS C:\> $FileSystemName = "filesystem1"
PS C:\> $Total = 0
PS C:\> $Token = $Null
PS C:\> do
 {
     $items = Get-AzDataLakeGen2ChildItem -FileSystem $FileSystemName -Recurse -MaxCount $MaxReturn  -ContinuationToken $Token
     $Total += $items.Count
     if($items.Length -le 0) { Break;}
     $Token = $items[$items.Count -1].ContinuationToken;
 }
 While ($Token -ne $Null)
PS C:\> Echo "Total $Total items in Filesystem $FileSystemName"
```

<span data-ttu-id="2dcb0-115">In diesem Beispiel werden die *Parameter "MaxCount"* und *"ContinuationToken"* verwendet, um Elemente rekursiv aus einem Dateisystem in mehreren Batches auflisten.</span><span class="sxs-lookup"><span data-stu-id="2dcb0-115">This example uses the *MaxCount* and *ContinuationToken* parameters to list items recursively from a Filesystem in multiple batches.</span></span>
<span data-ttu-id="2dcb0-116">Die ersten vier Befehle weisen Variablen Werte zu, die im Beispiel verwendet werden sollen.</span><span class="sxs-lookup"><span data-stu-id="2dcb0-116">The first four commands assign values to variables to use in the example.</span></span>
<span data-ttu-id="2dcb0-117">Der fünfte Befehl gibt eine **Do-While-Anweisung** an, die das **Cmdlet "Get-AzDataLakeGen2ChildItem"** zum Auflisten von Elementen verwendet.</span><span class="sxs-lookup"><span data-stu-id="2dcb0-117">The fifth command specifies a **Do-While** statement that uses the **Get-AzDataLakeGen2ChildItem** cmdlet to list items.</span></span>
<span data-ttu-id="2dcb0-118">Die Anweisung enthält das fortsetzungstoken, das in der Variablen $Token ist.</span><span class="sxs-lookup"><span data-stu-id="2dcb0-118">The statement includes the continuation token stored in the $Token variable.</span></span>
<span data-ttu-id="2dcb0-119">$Token ändert den Wert, während die Schleife ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="2dcb0-119">$Token changes value as the loop runs.</span></span>
<span data-ttu-id="2dcb0-120">Im letzten Befehl wird der Befehl **"Echo"** zum Anzeigen der Summe verwendet.</span><span class="sxs-lookup"><span data-stu-id="2dcb0-120">The final command uses the **Echo** command to display the total.</span></span>

## <span data-ttu-id="2dcb0-121">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="2dcb0-121">PARAMETERS</span></span>

### <span data-ttu-id="2dcb0-122">-AsJob</span><span class="sxs-lookup"><span data-stu-id="2dcb0-122">-AsJob</span></span>
<span data-ttu-id="2dcb0-123">Ausführen des Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="2dcb0-123">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="2dcb0-124">-Context</span><span class="sxs-lookup"><span data-stu-id="2dcb0-124">-Context</span></span>
<span data-ttu-id="2dcb0-125">Azure Storage Context Object</span><span class="sxs-lookup"><span data-stu-id="2dcb0-125">Azure Storage Context Object</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="2dcb0-126">-ContinuationToken</span><span class="sxs-lookup"><span data-stu-id="2dcb0-126">-ContinuationToken</span></span>
<span data-ttu-id="2dcb0-127">Fortsetzungstoken.</span><span class="sxs-lookup"><span data-stu-id="2dcb0-127">Continuation Token.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2dcb0-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2dcb0-128">-DefaultProfile</span></span>
<span data-ttu-id="2dcb0-129">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="2dcb0-129">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2dcb0-130">-FetchProperty</span><span class="sxs-lookup"><span data-stu-id="2dcb0-130">-FetchProperty</span></span>
<span data-ttu-id="2dcb0-131">Rufen Sie die "datalake"-Elementeigenschaften und den ACL ab.</span><span class="sxs-lookup"><span data-stu-id="2dcb0-131">Fetch the datalake item properties and ACL.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: FetchPermission

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2dcb0-132">-FileSystem</span><span class="sxs-lookup"><span data-stu-id="2dcb0-132">-FileSystem</span></span>
<span data-ttu-id="2dcb0-133">FileSystem name</span><span class="sxs-lookup"><span data-stu-id="2dcb0-133">FileSystem name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="2dcb0-134">-MaxCount</span><span class="sxs-lookup"><span data-stu-id="2dcb0-134">-MaxCount</span></span>
<span data-ttu-id="2dcb0-135">Die maximale Anzahl der BLOB-BloBs, die zurückgeben können.</span><span class="sxs-lookup"><span data-stu-id="2dcb0-135">The max count of the blobs that can return.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2dcb0-136">-OutputUserPrincipalName</span><span class="sxs-lookup"><span data-stu-id="2dcb0-136">-OutputUserPrincipalName</span></span>
<span data-ttu-id="2dcb0-137">Wenn Sie diesen Parameter vereinheitlichen, werden die in den Besitzer- und Gruppenfeldern jedes Listeneintrags zurückgegebenen Benutzeridentitätswerte aus Azure Active Directory-Objekt-IDs in Benutzerprinzipalnamen transformiert.</span><span class="sxs-lookup"><span data-stu-id="2dcb0-137">If speicify this parameter, the user identity values returned in the owner and group fields of each list entry will be transformed from Azure Active Directory Object IDs to User Principal Names.</span></span> <span data-ttu-id="2dcb0-138">Wenn dieser Parameter nicht angegeben wird, werden die Werte als Azure Active Directory-Objekt-IDs zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="2dcb0-138">If not speicify this parameter, the values will be returned as Azure Active Directory Object IDs.</span></span> <span data-ttu-id="2dcb0-139">Beachten Sie, dass Gruppen- und Anwendungsobjekt-IDs nicht übersetzt werden, da sie keine eindeutigen Anzeigenamen haben.</span><span class="sxs-lookup"><span data-stu-id="2dcb0-139">Note that group and application Object IDs are not translated because they do not have unique friendly names.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: UserPrincipalName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2dcb0-140">-Path</span><span class="sxs-lookup"><span data-stu-id="2dcb0-140">-Path</span></span>
<span data-ttu-id="2dcb0-141">Der Pfad im angegebenen Dateisystem, der abgerufen werden soll.</span><span class="sxs-lookup"><span data-stu-id="2dcb0-141">The path in the specified Filesystem that should be retrieved.</span></span>
<span data-ttu-id="2dcb0-142">Sollte ein Verzeichnis im Format 'directory1/directory2/' sein.</span><span class="sxs-lookup"><span data-stu-id="2dcb0-142">Should be a directory, in the format 'directory1/directory2/'.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="2dcb0-143">-Recurse</span><span class="sxs-lookup"><span data-stu-id="2dcb0-143">-Recurse</span></span>
<span data-ttu-id="2dcb0-144">Gibt an, ob das untergeordnete Element rekursiv erhalten wird.</span><span class="sxs-lookup"><span data-stu-id="2dcb0-144">Indicates if will recursively get the Child Item.</span></span>
<span data-ttu-id="2dcb0-145">Der Standardwert ist "false".</span><span class="sxs-lookup"><span data-stu-id="2dcb0-145">The default is false.</span></span>

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

### <span data-ttu-id="2dcb0-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2dcb0-146">CommonParameters</span></span>
<span data-ttu-id="2dcb0-147">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2dcb0-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2dcb0-148">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2dcb0-148">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2dcb0-149">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="2dcb0-149">INPUTS</span></span>

### <span data-ttu-id="2dcb0-150">System.String</span><span class="sxs-lookup"><span data-stu-id="2dcb0-150">System.String</span></span>

### <span data-ttu-id="2dcb0-151">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span><span class="sxs-lookup"><span data-stu-id="2dcb0-151">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="2dcb0-152">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="2dcb0-152">OUTPUTS</span></span>

### <span data-ttu-id="2dcb0-153">Microsoft.WindowsAzure.Commands.Common.Storage.ResourceModel.AzureDataLakeGen2Item</span><span class="sxs-lookup"><span data-stu-id="2dcb0-153">Microsoft.WindowsAzure.Commands.Common.Storage.ResourceModel.AzureDataLakeGen2Item</span></span>

## <span data-ttu-id="2dcb0-154">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="2dcb0-154">NOTES</span></span>

## <span data-ttu-id="2dcb0-155">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="2dcb0-155">RELATED LINKS</span></span>
