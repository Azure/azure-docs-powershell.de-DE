---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/get-azdatalakegen2childitem
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzDataLakeGen2ChildItem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzDataLakeGen2ChildItem.md
ms.openlocfilehash: 9160eabf2492969ad7fa3916791854abd4ef6c44
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94010394"
---
# <span data-ttu-id="12637-101">Get-AzDataLakeGen2ChildItem</span><span class="sxs-lookup"><span data-stu-id="12637-101">Get-AzDataLakeGen2ChildItem</span></span>

## <span data-ttu-id="12637-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="12637-102">SYNOPSIS</span></span>
<span data-ttu-id="12637-103">Listet Unterverzeichnisse und Dateien aus einem Verzeichnis oder Dateisystem Stamm auf.</span><span class="sxs-lookup"><span data-stu-id="12637-103">Lists sub directorys and files from a directory or filesystem root.</span></span>

## <span data-ttu-id="12637-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="12637-104">SYNTAX</span></span>

```
Get-AzDataLakeGen2ChildItem [-FileSystem] <String> [[-Path] <String>] [-FetchProperty] [-Recurse]
 [-MaxCount <Int32>] [-ContinuationToken <String>] [-AsJob] [-OutputUserPrincipalName]
 [-Context <IStorageContext>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="12637-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="12637-105">DESCRIPTION</span></span>
<span data-ttu-id="12637-106">Das Cmdlet " **Get-AzDataLakeGen2ChildItem** " listet Unterverzeichnisse und Dateien in einem Verzeichnis oder Dateisystem in einem Azure Storage-Konto auf.</span><span class="sxs-lookup"><span data-stu-id="12637-106">The **Get-AzDataLakeGen2ChildItem** cmdlet lists sub directorys and files in a directory or Filesystem in an Azure storage account.</span></span>
<span data-ttu-id="12637-107">Dieses Cmdlet funktioniert nur, wenn der Hierarchical-Namespace für das Speicherkonto aktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="12637-107">This cmdlet only works if Hierarchical Namespace is enabled for the Storage account.</span></span> <span data-ttu-id="12637-108">Diese Art von Konto kann erstellt werden, indem Sie das Cmdlet "New-AzStorageAccount" mit "-EnableHierarchicalNamespace $true" ausführen.</span><span class="sxs-lookup"><span data-stu-id="12637-108">This kind of account can be created by run "New-AzStorageAccount" cmdlet with "-EnableHierarchicalNamespace $true".</span></span>

## <span data-ttu-id="12637-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="12637-109">EXAMPLES</span></span>

### <span data-ttu-id="12637-110">Beispiel 1: Auflisten der direkten untergeordneten Elemente aus einem Dateisystem</span><span class="sxs-lookup"><span data-stu-id="12637-110">Example 1: List the direct sub items from a Filesystem</span></span>
```
PS C:\>Get-AzDataLakeGen2ChildItem -FileSystem "filesystem1" 

   FileSystem Name: filesystem1

Path                 IsDirectory  Length          LastModified         Permissions  Owner                Group               
----                 -----------  ------          ------------         -----------  -----                -----               
dir1                 True                         2020-03-13 13:07:34Z rwxr-x---    $superuser           $superuser          
dir2                 True                         2020-03-23 09:28:36Z rwxr-x---    $superuser           $superuser
```

<span data-ttu-id="12637-111">Dieser Befehl listet die direkten untergeordneten Elemente eines Dateisystems auf.</span><span class="sxs-lookup"><span data-stu-id="12637-111">This command lists the direct sub items from a Filesystem</span></span>

### <span data-ttu-id="12637-112">Beispiel 2: Auflisten rekursiv aus einem Verzeichnis und Abrufen von Eigenschaften/ACL</span><span class="sxs-lookup"><span data-stu-id="12637-112">Example 2: List recursively from a directory, and fetch Properties/ACL</span></span>
```
PS C:\>Get-AzDataLakeGen2ChildItem -FileSystem "filesystem1" -Path "dir1/" -Recurse -FetchProperty

   FileSystem Name: filesystem1

Path                 IsDirectory  Length          LastModified         Permissions  Owner                Group               
----                 -----------  ------          ------------         -----------  -----                -----               
dir1/dir3            True                         2020-03-23 09:34:31Z rwx---rwx    $superuser           $superuser          
dir1/file1           False        1024            2020-03-23 09:29:18Z rwx---rwx    $superuser           $superuser           
dir1/testfile_1K_0   False        1024            2020-03-23 09:29:21Z rw-r-----    $superuser           $superuser
```

<span data-ttu-id="12637-113">Dieser Befehl listet die direkten untergeordneten Elemente eines Dateisystems auf.</span><span class="sxs-lookup"><span data-stu-id="12637-113">This command lists the direct sub items from a Filesystem</span></span>

### <span data-ttu-id="12637-114">Beispiel 3: Auflisten von Elementen rekursiv aus einem Dateisystem in mehreren Batches</span><span class="sxs-lookup"><span data-stu-id="12637-114">Example 3: List items recursively from a Filesystem in multiple batches</span></span>
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

<span data-ttu-id="12637-115">In diesem Beispiel werden die *MaxCount* -und *ContinuationToken* -Parameter verwendet, um Elemente rekursiv aus einem Dateisystem in mehreren Batches aufzulisten.</span><span class="sxs-lookup"><span data-stu-id="12637-115">This example uses the *MaxCount* and *ContinuationToken* parameters to list items recursively from a Filesystem in multiple batches.</span></span>
<span data-ttu-id="12637-116">Die ersten vier Befehle weisen Variablenwerte zu, die im Beispiel verwendet werden sollen.</span><span class="sxs-lookup"><span data-stu-id="12637-116">The first four commands assign values to variables to use in the example.</span></span>
<span data-ttu-id="12637-117">Der fünfte Befehl gibt eine **do-while-** Anweisung an, die das Cmdlet " **Get-AzDataLakeGen2ChildItem** " zum Auflisten von Elementen verwendet.</span><span class="sxs-lookup"><span data-stu-id="12637-117">The fifth command specifies a **Do-While** statement that uses the **Get-AzDataLakeGen2ChildItem** cmdlet to list items.</span></span>
<span data-ttu-id="12637-118">Die Anweisung enthält das Fortsetzungstoken, das in der $Token Variablen gespeichert ist.</span><span class="sxs-lookup"><span data-stu-id="12637-118">The statement includes the continuation token stored in the $Token variable.</span></span>
<span data-ttu-id="12637-119">$Token ändert den Wert während der Ausführung der Schleife.</span><span class="sxs-lookup"><span data-stu-id="12637-119">$Token changes value as the loop runs.</span></span>
<span data-ttu-id="12637-120">Der endgültige Befehl verwendet den Befehl **Echo** , um die Summe anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="12637-120">The final command uses the **Echo** command to display the total.</span></span>

## <span data-ttu-id="12637-121">Parameter</span><span class="sxs-lookup"><span data-stu-id="12637-121">PARAMETERS</span></span>

### <span data-ttu-id="12637-122">-AsJob</span><span class="sxs-lookup"><span data-stu-id="12637-122">-AsJob</span></span>
<span data-ttu-id="12637-123">Ausführen eines Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="12637-123">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="12637-124">-Context</span><span class="sxs-lookup"><span data-stu-id="12637-124">-Context</span></span>
<span data-ttu-id="12637-125">Azure-Speicherkontext Objekt</span><span class="sxs-lookup"><span data-stu-id="12637-125">Azure Storage Context Object</span></span>

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

### <span data-ttu-id="12637-126">-ContinuationToken</span><span class="sxs-lookup"><span data-stu-id="12637-126">-ContinuationToken</span></span>
<span data-ttu-id="12637-127">Fortsetzungs Token.</span><span class="sxs-lookup"><span data-stu-id="12637-127">Continuation Token.</span></span>

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

### <span data-ttu-id="12637-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="12637-128">-DefaultProfile</span></span>
<span data-ttu-id="12637-129">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="12637-129">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="12637-130">-Fetchproperty</span><span class="sxs-lookup"><span data-stu-id="12637-130">-FetchProperty</span></span>
<span data-ttu-id="12637-131">Abrufen der Eigenschaften und ACL des datalake-Elements.</span><span class="sxs-lookup"><span data-stu-id="12637-131">Fetch the datalake item properties and ACL.</span></span>

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

### <span data-ttu-id="12637-132">-Dateisystem</span><span class="sxs-lookup"><span data-stu-id="12637-132">-FileSystem</span></span>
<span data-ttu-id="12637-133">Dateisystemname</span><span class="sxs-lookup"><span data-stu-id="12637-133">FileSystem name</span></span>

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

### <span data-ttu-id="12637-134">-MaxCount</span><span class="sxs-lookup"><span data-stu-id="12637-134">-MaxCount</span></span>
<span data-ttu-id="12637-135">Die maximale Anzahl der BLOBs, die zurückgegeben werden können.</span><span class="sxs-lookup"><span data-stu-id="12637-135">The max count of the blobs that can return.</span></span>

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

### <span data-ttu-id="12637-136">-OutputUserPrincipalName</span><span class="sxs-lookup"><span data-stu-id="12637-136">-OutputUserPrincipalName</span></span>
<span data-ttu-id="12637-137">Wenn speicify diesen Parameter verwendet, werden die in den Feldern "Besitzer" und "Gruppe" der einzelnen Listeneinträge zurückgegebenen Benutzer Identitätswerte aus Azure Active Directory-Objekt-IDs in Benutzerprinzipalnamen umgewandelt.</span><span class="sxs-lookup"><span data-stu-id="12637-137">If speicify this parameter, the user identity values returned in the owner and group fields of each list entry will be transformed from Azure Active Directory Object IDs to User Principal Names.</span></span> <span data-ttu-id="12637-138">Wenn dieser Parameter nicht speicify wird, werden die Werte als Azure Active Directory-Objekt-IDs zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="12637-138">If not speicify this parameter, the values will be returned as Azure Active Directory Object IDs.</span></span> <span data-ttu-id="12637-139">Beachten Sie, dass Gruppen-und Anwendungsobjekt-IDs nicht übersetzt werden, da Sie keine eindeutigen Anzeigenamen aufweisen.</span><span class="sxs-lookup"><span data-stu-id="12637-139">Note that group and application Object IDs are not translated because they do not have unique friendly names.</span></span>

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

### <span data-ttu-id="12637-140">-Path</span><span class="sxs-lookup"><span data-stu-id="12637-140">-Path</span></span>
<span data-ttu-id="12637-141">Der Pfad im angegebenen Dateisystem, der abgerufen werden soll.</span><span class="sxs-lookup"><span data-stu-id="12637-141">The path in the specified Filesystem that should be retrieved.</span></span>
<span data-ttu-id="12637-142">Sollte ein Verzeichnis im Format "Verzeichnis1/directory2/" sein.</span><span class="sxs-lookup"><span data-stu-id="12637-142">Should be a directory, in the format 'directory1/directory2/'.</span></span>

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

### <span data-ttu-id="12637-143">-Rekursiv</span><span class="sxs-lookup"><span data-stu-id="12637-143">-Recurse</span></span>
<span data-ttu-id="12637-144">Gibt an, ob das untergeordnete Element rekursiv abgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="12637-144">Indicates if will recursively get the Child Item.</span></span>
<span data-ttu-id="12637-145">Der Standardwert ist "false".</span><span class="sxs-lookup"><span data-stu-id="12637-145">The default is false.</span></span>

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

### <span data-ttu-id="12637-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="12637-146">CommonParameters</span></span>
<span data-ttu-id="12637-147">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="12637-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="12637-148">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="12637-148">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="12637-149">Eingaben</span><span class="sxs-lookup"><span data-stu-id="12637-149">INPUTS</span></span>

### <span data-ttu-id="12637-150">System. String</span><span class="sxs-lookup"><span data-stu-id="12637-150">System.String</span></span>

### <span data-ttu-id="12637-151">Microsoft. Azure. Commands. Common. Authentication. Abstractions. IStorageContext</span><span class="sxs-lookup"><span data-stu-id="12637-151">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="12637-152">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="12637-152">OUTPUTS</span></span>

### <span data-ttu-id="12637-153">Microsoft. WindowsAzure. Commands. Common. Storage. ResourceModel. AzureDataLakeGen2Item</span><span class="sxs-lookup"><span data-stu-id="12637-153">Microsoft.WindowsAzure.Commands.Common.Storage.ResourceModel.AzureDataLakeGen2Item</span></span>

## <span data-ttu-id="12637-154">Notizen</span><span class="sxs-lookup"><span data-stu-id="12637-154">NOTES</span></span>

## <span data-ttu-id="12637-155">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="12637-155">RELATED LINKS</span></span>
