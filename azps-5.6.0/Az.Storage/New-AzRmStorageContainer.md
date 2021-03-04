---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/powershell/module/az.storage/new-azrmstoragecontainer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzRmStorageContainer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzRmStorageContainer.md
ms.openlocfilehash: c85b482ff077263d20ae770e6ec6d91b497153e7
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101940736"
---
# <span data-ttu-id="1ba63-101">New-AzRmStorageContainer</span><span class="sxs-lookup"><span data-stu-id="1ba63-101">New-AzRmStorageContainer</span></span>

## <span data-ttu-id="1ba63-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1ba63-102">SYNOPSIS</span></span>
<span data-ttu-id="1ba63-103">Erstellt einen Speicherblobcontainer</span><span class="sxs-lookup"><span data-stu-id="1ba63-103">Creates a Storage blob container</span></span>

## <span data-ttu-id="1ba63-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="1ba63-104">SYNTAX</span></span>

### <span data-ttu-id="1ba63-105">AccountName (Standard)</span><span class="sxs-lookup"><span data-stu-id="1ba63-105">AccountName (Default)</span></span>
```
New-AzRmStorageContainer [-ResourceGroupName] <String> [-StorageAccountName] <String> -Name <String>
 [-PublicAccess <PSPublicAccess>] [-Metadata <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1ba63-106">AccountNameEncryptionScope</span><span class="sxs-lookup"><span data-stu-id="1ba63-106">AccountNameEncryptionScope</span></span>
```
New-AzRmStorageContainer [-ResourceGroupName] <String> [-StorageAccountName] <String> -Name <String>
 -DefaultEncryptionScope <String> -PreventEncryptionScopeOverride <Boolean> [-PublicAccess <PSPublicAccess>]
 [-Metadata <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1ba63-107">AccountObject</span><span class="sxs-lookup"><span data-stu-id="1ba63-107">AccountObject</span></span>
```
New-AzRmStorageContainer -StorageAccount <PSStorageAccount> -Name <String> [-PublicAccess <PSPublicAccess>]
 [-Metadata <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1ba63-108">AccountObjectEncryptionScope</span><span class="sxs-lookup"><span data-stu-id="1ba63-108">AccountObjectEncryptionScope</span></span>
```
New-AzRmStorageContainer -StorageAccount <PSStorageAccount> -Name <String> -DefaultEncryptionScope <String>
 -PreventEncryptionScopeOverride <Boolean> [-PublicAccess <PSPublicAccess>] [-Metadata <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1ba63-109">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="1ba63-109">DESCRIPTION</span></span>
<span data-ttu-id="1ba63-110">Das **Cmdlet New-AzRmStorageContainer** erstellt einen Speicherblobcontainer.</span><span class="sxs-lookup"><span data-stu-id="1ba63-110">The **New-AzRmStorageContainer** cmdlet creates a Storage blob container</span></span>

## <span data-ttu-id="1ba63-111">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="1ba63-111">EXAMPLES</span></span>

### <span data-ttu-id="1ba63-112">Beispiel 1: Erstellen eines Speicherblobscontainers mit dem Namen des Speicherkontos und dem Containernamen mit Metadaten</span><span class="sxs-lookup"><span data-stu-id="1ba63-112">Example 1: Create a Storage blob container with Storage account name and container name, with metadata</span></span>
```
PS C:\>New-AzRmStorageContainer -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount" -ContainerName "myContainer" -Metadata @{tag0="value0";tag1="value1";tag2="value2"}
```

<span data-ttu-id="1ba63-113">Mit diesem Befehl wird ein Speicherblobcontainer mit dem Namen des Speicherkontos und dem Containernamen mit Metadaten erstellt.</span><span class="sxs-lookup"><span data-stu-id="1ba63-113">This command creates a Storage blob container with Storage account name and container name, with metadata.</span></span>

### <span data-ttu-id="1ba63-114">Beispiel 2: Erstellen eines Speicherblobscontainers mit Speicherkontoobjekt und Containername mit öffentlichem Zugriff als Blob</span><span class="sxs-lookup"><span data-stu-id="1ba63-114">Example 2: Create a Storage blob container with Storage account object and container name, with public access as Blob</span></span>
```
PS C:\>$accountObject = Get-AzStorageAccount -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount"
PS C:\>New-AzRmStorageContainer -StorageAccount $accountObject -ContainerName "myContainer" -PublicAccess Blob
```

<span data-ttu-id="1ba63-115">Mit diesem Befehl wird ein Speicherblobcontainer mit Speicherkontoobjekt und Containername mit öffentlichem Zugriff als Blob erstellt.</span><span class="sxs-lookup"><span data-stu-id="1ba63-115">This command creates a Storage blob container with Storage account object and container name, with public access as Blob.</span></span>

### <span data-ttu-id="1ba63-116">Beispiel 3: Erstellen eines Speichercontainers mit EncryptionScope-Einstellung</span><span class="sxs-lookup"><span data-stu-id="1ba63-116">Example 3: Create a storage container with EncryptionScope setting</span></span>
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

<span data-ttu-id="1ba63-117">Dieser Befehl erstellt einen Speichercontainer mit einer EntschlüsselungsverschlüsselungScope und blockiert die Außerkraftsetzung des Verschlüsselungsbereichs von der Containereinstellung.</span><span class="sxs-lookup"><span data-stu-id="1ba63-117">This command creates a storage container with a defalt encryptionScope, and blocks override of encryption scope from the container default.</span></span>
<span data-ttu-id="1ba63-118">Zeigen Sie dann die zugehörigen Containereigenschaften an.</span><span class="sxs-lookup"><span data-stu-id="1ba63-118">Then show the related container properties.</span></span>

## <span data-ttu-id="1ba63-119">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="1ba63-119">PARAMETERS</span></span>

### <span data-ttu-id="1ba63-120">-DefaultEncryptionScope</span><span class="sxs-lookup"><span data-stu-id="1ba63-120">-DefaultEncryptionScope</span></span>
<span data-ttu-id="1ba63-121">Standardmäßig wird der Container für die Verwendung des angegebenen Verschlüsselungsbereichs für alle Schreibvorgänge verwendet.</span><span class="sxs-lookup"><span data-stu-id="1ba63-121">Default the container to use specified encryption scope for all writes.</span></span>

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

### <span data-ttu-id="1ba63-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1ba63-122">-DefaultProfile</span></span>
<span data-ttu-id="1ba63-123">Die Anmeldeinformationen, das Konto, der Mandant und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="1ba63-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="1ba63-124">-Metadaten</span><span class="sxs-lookup"><span data-stu-id="1ba63-124">-Metadata</span></span>
<span data-ttu-id="1ba63-125">Containermetadaten</span><span class="sxs-lookup"><span data-stu-id="1ba63-125">Container Metadata</span></span>

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

### <span data-ttu-id="1ba63-126">-Name</span><span class="sxs-lookup"><span data-stu-id="1ba63-126">-Name</span></span>
<span data-ttu-id="1ba63-127">Containername</span><span class="sxs-lookup"><span data-stu-id="1ba63-127">Container Name</span></span>

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

### <span data-ttu-id="1ba63-128">-PreventEncryptionScopeOverride</span><span class="sxs-lookup"><span data-stu-id="1ba63-128">-PreventEncryptionScopeOverride</span></span>
<span data-ttu-id="1ba63-129">Block override of encryption scope from the container default.</span><span class="sxs-lookup"><span data-stu-id="1ba63-129">Block override of encryption scope from the container default.</span></span>

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

### <span data-ttu-id="1ba63-130">-PublicAccess</span><span class="sxs-lookup"><span data-stu-id="1ba63-130">-PublicAccess</span></span>
<span data-ttu-id="1ba63-131">Container PublicAccess</span><span class="sxs-lookup"><span data-stu-id="1ba63-131">Container PublicAccess</span></span>

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

### <span data-ttu-id="1ba63-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1ba63-132">-ResourceGroupName</span></span>
<span data-ttu-id="1ba63-133">Ressourcengruppenname.</span><span class="sxs-lookup"><span data-stu-id="1ba63-133">Resource Group Name.</span></span>

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

### <span data-ttu-id="1ba63-134">-StorageAccount</span><span class="sxs-lookup"><span data-stu-id="1ba63-134">-StorageAccount</span></span>
<span data-ttu-id="1ba63-135">Speicherkontoobjekt</span><span class="sxs-lookup"><span data-stu-id="1ba63-135">Storage account object</span></span>

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

### <span data-ttu-id="1ba63-136">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="1ba63-136">-StorageAccountName</span></span>
<span data-ttu-id="1ba63-137">Speicherkontoname.</span><span class="sxs-lookup"><span data-stu-id="1ba63-137">Storage Account Name.</span></span>

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

### <span data-ttu-id="1ba63-138">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="1ba63-138">-Confirm</span></span>
<span data-ttu-id="1ba63-139">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="1ba63-139">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1ba63-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1ba63-140">-WhatIf</span></span>
<span data-ttu-id="1ba63-141">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="1ba63-141">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="1ba63-142">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="1ba63-142">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1ba63-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1ba63-143">CommonParameters</span></span>
<span data-ttu-id="1ba63-144">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1ba63-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1ba63-145">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1ba63-145">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1ba63-146">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="1ba63-146">INPUTS</span></span>

### <span data-ttu-id="1ba63-147">System.String</span><span class="sxs-lookup"><span data-stu-id="1ba63-147">System.String</span></span>

### <span data-ttu-id="1ba63-148">Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount</span><span class="sxs-lookup"><span data-stu-id="1ba63-148">Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount</span></span>

## <span data-ttu-id="1ba63-149">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="1ba63-149">OUTPUTS</span></span>

### <span data-ttu-id="1ba63-150">Microsoft.Azure.Commands.Management.Storage.Models.PSContainer</span><span class="sxs-lookup"><span data-stu-id="1ba63-150">Microsoft.Azure.Commands.Management.Storage.Models.PSContainer</span></span>

## <span data-ttu-id="1ba63-151">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="1ba63-151">NOTES</span></span>

## <span data-ttu-id="1ba63-152">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="1ba63-152">RELATED LINKS</span></span>
