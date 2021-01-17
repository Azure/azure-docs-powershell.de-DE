---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/new-azrmstoragecontainer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzRmStorageContainer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzRmStorageContainer.md
ms.openlocfilehash: 901061390c68853832bad14965620abad21817e8
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98467955"
---
# <span data-ttu-id="51564-101">New-AzRmStorageContainer</span><span class="sxs-lookup"><span data-stu-id="51564-101">New-AzRmStorageContainer</span></span>

## <span data-ttu-id="51564-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="51564-102">SYNOPSIS</span></span>
<span data-ttu-id="51564-103">Erstellt einen Speicher-BLOB-Container.</span><span class="sxs-lookup"><span data-stu-id="51564-103">Creates a Storage blob container</span></span>

## <span data-ttu-id="51564-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="51564-104">SYNTAX</span></span>

### <span data-ttu-id="51564-105">AccountName (Standard)</span><span class="sxs-lookup"><span data-stu-id="51564-105">AccountName (Default)</span></span>
```
New-AzRmStorageContainer [-ResourceGroupName] <String> [-StorageAccountName] <String> -Name <String>
 [-PublicAccess <PSPublicAccess>] [-Metadata <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="51564-106">AccountNameEncryptionScope</span><span class="sxs-lookup"><span data-stu-id="51564-106">AccountNameEncryptionScope</span></span>
```
New-AzRmStorageContainer [-ResourceGroupName] <String> [-StorageAccountName] <String> -Name <String>
 -DefaultEncryptionScope <String> -PreventEncryptionScopeOverride <Boolean> [-PublicAccess <PSPublicAccess>]
 [-Metadata <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="51564-107">AccountObject</span><span class="sxs-lookup"><span data-stu-id="51564-107">AccountObject</span></span>
```
New-AzRmStorageContainer -StorageAccount <PSStorageAccount> -Name <String> [-PublicAccess <PSPublicAccess>]
 [-Metadata <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="51564-108">AccountObjectEncryptionScope</span><span class="sxs-lookup"><span data-stu-id="51564-108">AccountObjectEncryptionScope</span></span>
```
New-AzRmStorageContainer -StorageAccount <PSStorageAccount> -Name <String> -DefaultEncryptionScope <String>
 -PreventEncryptionScopeOverride <Boolean> [-PublicAccess <PSPublicAccess>] [-Metadata <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="51564-109">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="51564-109">DESCRIPTION</span></span>
<span data-ttu-id="51564-110">Das **Cmdlet "New-AzRmStorageContainer"** erstellt einen Speicher-BLOB-Container.</span><span class="sxs-lookup"><span data-stu-id="51564-110">The **New-AzRmStorageContainer** cmdlet creates a Storage blob container</span></span>

## <span data-ttu-id="51564-111">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="51564-111">EXAMPLES</span></span>

### <span data-ttu-id="51564-112">Beispiel 1: Erstellen eines Speicher-BLOB-Containers mit dem Namen des Speicherkontos und dem Containernamen mit Metadaten</span><span class="sxs-lookup"><span data-stu-id="51564-112">Example 1: Create a Storage blob container with Storage account name and container name, with metadata</span></span>
```
PS C:\>New-AzRmStorageContainer -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount" -ContainerName "myContainer" -Metadata @{tag0="value0";tag1="value1";tag2="value2"}
```

<span data-ttu-id="51564-113">Mit diesem Befehl wird ein Speicher-BLOB-Container mit dem Namen des Speicherkontos und dem Containernamen mit Metadaten erstellt.</span><span class="sxs-lookup"><span data-stu-id="51564-113">This command creates a Storage blob container with Storage account name and container name, with metadata.</span></span>

### <span data-ttu-id="51564-114">Beispiel 2: Erstellen eines Speicher-BLOB-Containers mit Speicherkontoobjekt und Containername, mit öffentlichem Zugriff als BLOB</span><span class="sxs-lookup"><span data-stu-id="51564-114">Example 2: Create a Storage blob container with Storage account object and container name, with public access as Blob</span></span>
```
PS C:\>$accountObject = Get-AzStorageAccount -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount"
PS C:\>New-AzRmStorageContainer -StorageAccount $accountObject -ContainerName "myContainer" -PublicAccess Blob
```

<span data-ttu-id="51564-115">Mit diesem Befehl wird ein Speicher-BLOB-Container mit Speicherkontoobjekt und Containername mit öffentlichem Zugriff als BLOB erstellt.</span><span class="sxs-lookup"><span data-stu-id="51564-115">This command creates a Storage blob container with Storage account object and container name, with public access as Blob.</span></span>

### <span data-ttu-id="51564-116">Beispiel 3: Erstellen eines Speichercontainers mit Einstellung "EncryptionScope"</span><span class="sxs-lookup"><span data-stu-id="51564-116">Example 3: Create a storage container with EncryptionScope setting</span></span>
```
PS C:\> $c = New-AzRmStorageContainer -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount" -Name testcontainer -DefaultEncryptionScope "testscope" -PreventEncryptionScopeOverride $true

PS C:\> $c

   ResourceGroupName: myResourceGroup, StorageAccountName: myStorageAccount

Name          PublicAccess LastModified HasLegalHold HasImmutabilityPolicy
----          ------------ ------------ ------------ ---------------------
testcontainer                           False        False                

PS C:\> $c.DefaultEncryptionScope
testscope

PS C:\> $c.DenyEncryptionScopeOverride
True
```

<span data-ttu-id="51564-117">Mit diesem Befehl wird ein Speichercontainer mit einem defalt encryptionScope erstellt und die Außerkraftsetzung des Verschlüsselungsbereichs vom Container standardmäßig blockiert.</span><span class="sxs-lookup"><span data-stu-id="51564-117">This command creates a storage container with a defalt encryptionScope, and blocks override of encryption scope from the container default.</span></span>
<span data-ttu-id="51564-118">Zeigen Sie dann die zugehörigen Containereigenschaften an.</span><span class="sxs-lookup"><span data-stu-id="51564-118">Then show the related container properties.</span></span>

## <span data-ttu-id="51564-119">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="51564-119">PARAMETERS</span></span>

### <span data-ttu-id="51564-120">-DefaultEncryptionScope</span><span class="sxs-lookup"><span data-stu-id="51564-120">-DefaultEncryptionScope</span></span>
<span data-ttu-id="51564-121">Standardmäßig verwendet der Container den angegebenen Verschlüsselungsbereich für alle Schreibvorgänge.</span><span class="sxs-lookup"><span data-stu-id="51564-121">Default the container to use specified encryption scope for all writes.</span></span>

```yaml
Type: System.String
Parameter Sets: AccountNameEncryptionScope, AccountObjectEncryptionScope
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="51564-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="51564-122">-DefaultProfile</span></span>
<span data-ttu-id="51564-123">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="51564-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="51564-124">-Metadata</span><span class="sxs-lookup"><span data-stu-id="51564-124">-Metadata</span></span>
<span data-ttu-id="51564-125">Containermetadaten</span><span class="sxs-lookup"><span data-stu-id="51564-125">Container Metadata</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="51564-126">-Name</span><span class="sxs-lookup"><span data-stu-id="51564-126">-Name</span></span>
<span data-ttu-id="51564-127">Containername</span><span class="sxs-lookup"><span data-stu-id="51564-127">Container Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: N, ContainerName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="51564-128">-PreventEncryptionScopeOverride</span><span class="sxs-lookup"><span data-stu-id="51564-128">-PreventEncryptionScopeOverride</span></span>
<span data-ttu-id="51564-129">Blocküberschreibung des Verschlüsselungsbereichs vom Container standardmäßig.</span><span class="sxs-lookup"><span data-stu-id="51564-129">Block override of encryption scope from the container default.</span></span>

```yaml
Type: System.Boolean
Parameter Sets: AccountNameEncryptionScope, AccountObjectEncryptionScope
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="51564-130">-PublicAccess</span><span class="sxs-lookup"><span data-stu-id="51564-130">-PublicAccess</span></span>
<span data-ttu-id="51564-131">Container PublicAccess</span><span class="sxs-lookup"><span data-stu-id="51564-131">Container PublicAccess</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.Storage.Models.PSPublicAccess
Parameter Sets: (All)
Aliases:
Accepted values: Container, Blob, None

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="51564-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="51564-132">-ResourceGroupName</span></span>
<span data-ttu-id="51564-133">Ressourcengruppenname.</span><span class="sxs-lookup"><span data-stu-id="51564-133">Resource Group Name.</span></span>

```yaml
Type: System.String
Parameter Sets: AccountName, AccountNameEncryptionScope
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="51564-134">-StorageAccount</span><span class="sxs-lookup"><span data-stu-id="51564-134">-StorageAccount</span></span>
<span data-ttu-id="51564-135">Speicherkontoobjekt</span><span class="sxs-lookup"><span data-stu-id="51564-135">Storage account object</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount
Parameter Sets: AccountObject, AccountObjectEncryptionScope
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="51564-136">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="51564-136">-StorageAccountName</span></span>
<span data-ttu-id="51564-137">Speicherkontoname.</span><span class="sxs-lookup"><span data-stu-id="51564-137">Storage Account Name.</span></span>

```yaml
Type: System.String
Parameter Sets: AccountName, AccountNameEncryptionScope
Aliases: AccountName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="51564-138">-Confirm</span><span class="sxs-lookup"><span data-stu-id="51564-138">-Confirm</span></span>
<span data-ttu-id="51564-139">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="51564-139">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="51564-140">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="51564-140">-WhatIf</span></span>
<span data-ttu-id="51564-141">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="51564-141">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="51564-142">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="51564-142">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="51564-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="51564-143">CommonParameters</span></span>
<span data-ttu-id="51564-144">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="51564-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="51564-145">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="51564-145">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="51564-146">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="51564-146">INPUTS</span></span>

### <span data-ttu-id="51564-147">System.String</span><span class="sxs-lookup"><span data-stu-id="51564-147">System.String</span></span>

### <span data-ttu-id="51564-148">Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount</span><span class="sxs-lookup"><span data-stu-id="51564-148">Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount</span></span>

## <span data-ttu-id="51564-149">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="51564-149">OUTPUTS</span></span>

### <span data-ttu-id="51564-150">Microsoft.Azure.Commands.Management.Storage.Models.PSContainer</span><span class="sxs-lookup"><span data-stu-id="51564-150">Microsoft.Azure.Commands.Management.Storage.Models.PSContainer</span></span>

## <span data-ttu-id="51564-151">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="51564-151">NOTES</span></span>

## <span data-ttu-id="51564-152">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="51564-152">RELATED LINKS</span></span>
