---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeStore.dll-Help.xml
Module Name: Az.DataLakeStore
ms.assetid: 33E7607E-C2BC-4F46-9038-91AC92041F00
online version: https://docs.microsoft.com/powershell/module/az.datalakestore/remove-azdatalakestoreitemaclentry
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Remove-AzDataLakeStoreItemAclEntry.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Remove-AzDataLakeStoreItemAclEntry.md
ms.openlocfilehash: e41b1c01976cdc631d146721a4ee63d61d52afef
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101923784"
---
# <span data-ttu-id="4a46b-101">Remove-AzDataLakeStoreItemAclEntry</span><span class="sxs-lookup"><span data-stu-id="4a46b-101">Remove-AzDataLakeStoreItemAclEntry</span></span>

## <span data-ttu-id="4a46b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4a46b-102">SYNOPSIS</span></span>
<span data-ttu-id="4a46b-103">Entfernt einen Eintrag aus der ACL einer Datei oder eines Ordners im Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="4a46b-103">Removes an entry from the ACL of a file or folder in Data Lake Store.</span></span>

## <span data-ttu-id="4a46b-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="4a46b-104">SYNTAX</span></span>

### <span data-ttu-id="4a46b-105">RemoveByACLObject (Standard)</span><span class="sxs-lookup"><span data-stu-id="4a46b-105">RemoveByACLObject (Default)</span></span>
```
Remove-AzDataLakeStoreItemAclEntry [-Account] <String> [-Path] <DataLakeStorePathInstance>
 [-Acl] <DataLakeStoreItemAce[]> [-PassThru] [-Recurse] [-Concurrency <Int32>] [-ShowProgress]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4a46b-106">RemoveSpecificACE</span><span class="sxs-lookup"><span data-stu-id="4a46b-106">RemoveSpecificACE</span></span>
```
Remove-AzDataLakeStoreItemAclEntry [-Account] <String> [-Path] <DataLakeStorePathInstance> [-AceType] <AceType>
 [[-Id] <Guid>] [-Default] [-PassThru] [-Recurse] [-Concurrency <Int32>] [-ShowProgress]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4a46b-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="4a46b-107">DESCRIPTION</span></span>
<span data-ttu-id="4a46b-108">Das **Cmdlet Remove-AzDataLakeStoreItemAclEntry** entfernt einen Eintrag (ACE) aus der Zugriffssteuerungsliste (Access Control List, ACL) einer Datei oder eines Ordners im Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="4a46b-108">The **Remove-AzDataLakeStoreItemAclEntry** cmdlet removes an entry (ACE) from the access control list (ACL) of a file or folder in Data Lake Store.</span></span>

## <span data-ttu-id="4a46b-109">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="4a46b-109">EXAMPLES</span></span>

### <span data-ttu-id="4a46b-110">Beispiel 1: Entfernen eines Benutzereintrags</span><span class="sxs-lookup"><span data-stu-id="4a46b-110">Example 1: Remove a user entry</span></span>
```
PS C:\>Remove-AzDataLakeStoreItemAclEntry -AccountName "ContosoADL" -Path / -AceType User -Id (Get-AzADUser -Mail "PattiFuller@contoso.com").ObjectId
```

<span data-ttu-id="4a46b-111">Mit diesem Befehl wird der Benutzer-ACE für Patti Fuller aus dem ContosoADL-Konto entfernt.</span><span class="sxs-lookup"><span data-stu-id="4a46b-111">This command removes the user ACE for Patti Fuller from the ContosoADL account.</span></span>

### <span data-ttu-id="4a46b-112">Beispiel 2: Rekursiv entfernen eines Benutzereintrags</span><span class="sxs-lookup"><span data-stu-id="4a46b-112">Example 2: Remove a user entry recursively</span></span>
```
PS C:\>Remove-AzDataLakeStoreItemAclEntry -AccountName "ContosoADL" -Path / -AceType User -Id (Get-AzADUser -Mail "PattiFuller@contoso.com").ObjectId -Recurse -Concurrency 128
```

### <span data-ttu-id="4a46b-113">Beispiel 3: Entfernen von Berechtigungen für ein ACE rekursiv mit dem Acl-Objekt</span><span class="sxs-lookup"><span data-stu-id="4a46b-113">Example 3: Remove permissions for an ACE recursively using Acl object</span></span>
```
PS C:\>$fullAcl="user:userid1,default:user:userid1
PS C:\>$newFullAcl = $fullAcl.Split("{,}")
PS C:\>Remove-AzDataLakeStoreItemAclEntry -AccountName "ContosoADL" -Path / -Acl $newFullAcl -Recurse -Concurrency 128
```

<span data-ttu-id="4a46b-114">Mit diesem Befehl wird das Benutzer-ACE für Patti Fuller aus dem Stammverzeichnis entfernt und rekursiv aus allen Unterverzeichnissen und Dateien für das Konto ContosoADL entfernt.</span><span class="sxs-lookup"><span data-stu-id="4a46b-114">This command removes the user ACE for Patti Fuller from the root and recursively from all it's subdirectories and files for account ContosoADL.</span></span>

## <span data-ttu-id="4a46b-115">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="4a46b-115">PARAMETERS</span></span>

### <span data-ttu-id="4a46b-116">-Konto</span><span class="sxs-lookup"><span data-stu-id="4a46b-116">-Account</span></span>
<span data-ttu-id="4a46b-117">Gibt den Namen des Data Lake Store-Kontos an.</span><span class="sxs-lookup"><span data-stu-id="4a46b-117">Specifies the name of the Data Lake Store account.</span></span>

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

### <span data-ttu-id="4a46b-118">-AceType</span><span class="sxs-lookup"><span data-stu-id="4a46b-118">-AceType</span></span>
<span data-ttu-id="4a46b-119">Gibt den Typ des zu entfernenden ACE an.</span><span class="sxs-lookup"><span data-stu-id="4a46b-119">Specifies the type of ACE to remove.</span></span>
<span data-ttu-id="4a46b-120">Die zulässigen Werte für diesen Parameter sind:</span><span class="sxs-lookup"><span data-stu-id="4a46b-120">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="4a46b-121">Benutzer</span><span class="sxs-lookup"><span data-stu-id="4a46b-121">User</span></span>
- <span data-ttu-id="4a46b-122">Gruppe</span><span class="sxs-lookup"><span data-stu-id="4a46b-122">Group</span></span>
- <span data-ttu-id="4a46b-123">Maske</span><span class="sxs-lookup"><span data-stu-id="4a46b-123">Mask</span></span>
- <span data-ttu-id="4a46b-124">Sonstige</span><span class="sxs-lookup"><span data-stu-id="4a46b-124">Other</span></span>

```yaml
Type: Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStoreEnums+AceType
Parameter Sets: RemoveSpecificACE
Aliases:
Accepted values: User, Group, Mask, Other

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4a46b-125">-Acl</span><span class="sxs-lookup"><span data-stu-id="4a46b-125">-Acl</span></span>
<span data-ttu-id="4a46b-126">Gibt das ACL-Objekt an, das die zu entfernenden Einträge enthält.</span><span class="sxs-lookup"><span data-stu-id="4a46b-126">Specifies the ACL object that contains the entries to be removed.</span></span>

```yaml
Type: Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStoreItemAce[]
Parameter Sets: RemoveByACLObject
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="4a46b-127">-Parallelität</span><span class="sxs-lookup"><span data-stu-id="4a46b-127">-Concurrency</span></span>
<span data-ttu-id="4a46b-128">Anzahl der parallel verarbeiteten Dateien/Verzeichnisse.</span><span class="sxs-lookup"><span data-stu-id="4a46b-128">Number of files/directories processed in parallel.</span></span> <span data-ttu-id="4a46b-129">Optional: Eine angemessene Standardeinstellung wird ausgewählt.</span><span class="sxs-lookup"><span data-stu-id="4a46b-129">Optional: a reasonable default will be selected</span></span>

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

### <span data-ttu-id="4a46b-130">-Standard</span><span class="sxs-lookup"><span data-stu-id="4a46b-130">-Default</span></span>
<span data-ttu-id="4a46b-131">Gibt an, dass mit diesem Vorgang das Standard-ACE aus der angegebenen ACL entfernt wird.</span><span class="sxs-lookup"><span data-stu-id="4a46b-131">Indicates that this operation removes the default ACE from the specified ACL.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: RemoveSpecificACE
Aliases:

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4a46b-132">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4a46b-132">-DefaultProfile</span></span>
<span data-ttu-id="4a46b-133">Die Anmeldeinformationen, das Konto, der Mandant und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="4a46b-133">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="4a46b-134">-ID</span><span class="sxs-lookup"><span data-stu-id="4a46b-134">-Id</span></span>
<span data-ttu-id="4a46b-135">Gibt die Objekt-ID des AzureActive Directory-Benutzers, der Gruppe oder des Dienstprinzipal an, für den ein ACE entfernt werden soll.</span><span class="sxs-lookup"><span data-stu-id="4a46b-135">Specifies the object ID of the AzureActive Directory user, group, or service principal for which to remove an ACE.</span></span>

```yaml
Type: System.Guid
Parameter Sets: RemoveSpecificACE
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4a46b-136">-PassThru</span><span class="sxs-lookup"><span data-stu-id="4a46b-136">-PassThru</span></span>
<span data-ttu-id="4a46b-137">Gibt an, dass eine boolesche Antwort zurückgegeben werden soll, die das Ergebnis des Löschvorgangs angibt.</span><span class="sxs-lookup"><span data-stu-id="4a46b-137">Indicates a boolean response should be returned indicating the result of the delete operation.</span></span>

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

### <span data-ttu-id="4a46b-138">-Path</span><span class="sxs-lookup"><span data-stu-id="4a46b-138">-Path</span></span>
<span data-ttu-id="4a46b-139">Gibt den Data Lake Store-Pfad des Elements an, aus dem ein ACE entfernt werden soll, beginnend mit dem Stammverzeichnis (/).</span><span class="sxs-lookup"><span data-stu-id="4a46b-139">Specifies the Data Lake Store path of the item from which to remove an ACE, starting with the root directory (/).</span></span>

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

### <span data-ttu-id="4a46b-140">-Rekursieren</span><span class="sxs-lookup"><span data-stu-id="4a46b-140">-Recurse</span></span>
<span data-ttu-id="4a46b-141">Gibt an, dass die ACL rekursiv in die untergeordneten Unterverzeichnisse und Dateien entfernt werden soll</span><span class="sxs-lookup"><span data-stu-id="4a46b-141">Indicates the ACL to be removed recursively to the child subdirectories and files</span></span>

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

### <span data-ttu-id="4a46b-142">-ShowProgress</span><span class="sxs-lookup"><span data-stu-id="4a46b-142">-ShowProgress</span></span>
<span data-ttu-id="4a46b-143">Wenn der Status übergeben ist, wird der Status angezeigt.</span><span class="sxs-lookup"><span data-stu-id="4a46b-143">If passed then progress status is showed.</span></span> <span data-ttu-id="4a46b-144">Gilt nur, wenn die rekursive Acl-Entfernung erfolgt.</span><span class="sxs-lookup"><span data-stu-id="4a46b-144">Only applicable when recursive Acl remove is done.</span></span>

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

### <span data-ttu-id="4a46b-145">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="4a46b-145">-Confirm</span></span>
<span data-ttu-id="4a46b-146">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="4a46b-146">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4a46b-147">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4a46b-147">-WhatIf</span></span>
<span data-ttu-id="4a46b-148">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="4a46b-148">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4a46b-149">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="4a46b-149">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4a46b-150">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4a46b-150">CommonParameters</span></span>
<span data-ttu-id="4a46b-151">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4a46b-151">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4a46b-152">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4a46b-152">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4a46b-153">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="4a46b-153">INPUTS</span></span>

### <span data-ttu-id="4a46b-154">System.String</span><span class="sxs-lookup"><span data-stu-id="4a46b-154">System.String</span></span>

### <span data-ttu-id="4a46b-155">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStorePathInstance</span><span class="sxs-lookup"><span data-stu-id="4a46b-155">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStorePathInstance</span></span>

### <span data-ttu-id="4a46b-156">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStoreItemAce[]</span><span class="sxs-lookup"><span data-stu-id="4a46b-156">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStoreItemAce[]</span></span>

### <span data-ttu-id="4a46b-157">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStoreEnums+AceType</span><span class="sxs-lookup"><span data-stu-id="4a46b-157">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStoreEnums+AceType</span></span>

### <span data-ttu-id="4a46b-158">System.Guid</span><span class="sxs-lookup"><span data-stu-id="4a46b-158">System.Guid</span></span>

### <span data-ttu-id="4a46b-159">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="4a46b-159">System.Management.Automation.SwitchParameter</span></span>

### <span data-ttu-id="4a46b-160">System.Int32</span><span class="sxs-lookup"><span data-stu-id="4a46b-160">System.Int32</span></span>

## <span data-ttu-id="4a46b-161">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="4a46b-161">OUTPUTS</span></span>

### <span data-ttu-id="4a46b-162">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="4a46b-162">System.Boolean</span></span>

## <span data-ttu-id="4a46b-163">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="4a46b-163">NOTES</span></span>

## <span data-ttu-id="4a46b-164">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="4a46b-164">RELATED LINKS</span></span>

[<span data-ttu-id="4a46b-165">Set-AzDataLakeStoreItemAclEntry</span><span class="sxs-lookup"><span data-stu-id="4a46b-165">Set-AzDataLakeStoreItemAclEntry</span></span>](./Set-AzDataLakeStoreItemAclEntry.md)


