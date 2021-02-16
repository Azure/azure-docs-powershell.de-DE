---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeStore.dll-Help.xml
Module Name: Az.DataLakeStore
ms.assetid: 0671D833-8B3A-4480-A576-92F1A9E8CE92
online version: https://docs.microsoft.com/en-us/powershell/module/az.datalakestore/set-azdatalakestoreitemaclentry
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Set-AzDataLakeStoreItemAclEntry.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Set-AzDataLakeStoreItemAclEntry.md
ms.openlocfilehash: 4f432596e6165989df07187a9383da04f0929a2d
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100161865"
---
# <span data-ttu-id="ed0b1-101">Set-AzDataLakeStoreItemAclEntry</span><span class="sxs-lookup"><span data-stu-id="ed0b1-101">Set-AzDataLakeStoreItemAclEntry</span></span>

## <span data-ttu-id="ed0b1-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ed0b1-102">SYNOPSIS</span></span>
<span data-ttu-id="ed0b1-103">Ändert einen Eintrag in der ACL einer Datei oder eines Ordners im Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="ed0b1-103">Modifies an entry in the ACL of a file or folder in Data Lake Store.</span></span>

## <span data-ttu-id="ed0b1-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="ed0b1-104">SYNTAX</span></span>

### <span data-ttu-id="ed0b1-105">SetByACLObject (Standard)</span><span class="sxs-lookup"><span data-stu-id="ed0b1-105">SetByACLObject (Default)</span></span>
```
Set-AzDataLakeStoreItemAclEntry [-Account] <String> [-Path] <DataLakeStorePathInstance>
 [-Acl] <DataLakeStoreItemAce[]> [-PassThru] [-Recurse] [-Concurrency <Int32>] [-ShowProgress]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ed0b1-106">SetSpecificACE</span><span class="sxs-lookup"><span data-stu-id="ed0b1-106">SetSpecificACE</span></span>
```
Set-AzDataLakeStoreItemAclEntry [-Account] <String> [-Path] <DataLakeStorePathInstance> [-AceType] <AceType>
 [[-Id] <Guid>] [-Permissions] <Permission> [-Default] [-PassThru] [-Recurse] [-Concurrency <Int32>]
 [-ShowProgress] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ed0b1-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="ed0b1-107">DESCRIPTION</span></span>
<span data-ttu-id="ed0b1-108">Das **Cmdlet "Set-AzDataLakeStoreItemAclEntry"** ändert einen Eintrag (ACE) in der Zugriffssteuerungsliste (Access Control List, ACL) einer Datei oder eines Ordners im Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="ed0b1-108">The **Set-AzDataLakeStoreItemAclEntry** cmdlet modifies an entry (ACE) in the access control list (ACL) of a file or folder in Data Lake Store.</span></span>

## <span data-ttu-id="ed0b1-109">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="ed0b1-109">EXAMPLES</span></span>

### <span data-ttu-id="ed0b1-110">Beispiel 1: Ändern von Berechtigungen für ein ACE</span><span class="sxs-lookup"><span data-stu-id="ed0b1-110">Example 1: Modify permissions for an ACE</span></span>
```
PS C:\>Set-AzDataLakeStoreItemAclEntry -AccountName "ContosoADL" -Path / -AceType User -Id (Get-AzADUser -Mail "PattiFuller@contoso.com").ObjectId -Permissions All
```

<span data-ttu-id="ed0b1-111">Mit diesem Befehl wird der ACE für Dentingen Fuller so geändert, dass alle Berechtigungen erteilt sind.</span><span class="sxs-lookup"><span data-stu-id="ed0b1-111">This command modifies the ACE for Patti Fuller to have all permissions.</span></span>

### <span data-ttu-id="ed0b1-112">Beispiel 2: Rekursives Ändern von Berechtigungen für ein ACE</span><span class="sxs-lookup"><span data-stu-id="ed0b1-112">Example 2: Modify permissions for an ACE recursively</span></span>
```
PS C:\>Set-AzDataLakeStoreItemAclEntry -AccountName "ContosoADL" -Path / -AceType User -Id (Get-AzADUser -Mail "PattiFuller@contoso.com").ObjectId -Permissions All -Recurse -Concurrency 128
```

### <span data-ttu-id="ed0b1-113">Beispiel 3: Ändern von Berechtigungen für ein ACE rekursiv mithilfe des Objekts "Acl"</span><span class="sxs-lookup"><span data-stu-id="ed0b1-113">Example 3: Modify permissions for an ACE recursively using Acl object</span></span>
```
PS C:\>$fullAcl="user:userid1:--x,default:user:userid1:--x"
PS C:\>$newFullAcl = $fullAcl.Split("{,}")
PS C:\>Set-AzDataLakeStoreItemAclEntry -AccountName "ContosoADL" -Path / -Acl $newFullAcl -Recurse -Concurrency 128
```

<span data-ttu-id="ed0b1-114">Mit diesem Befehl wird der ACE für Diei Fuller rekursiv so geändert, dass alle Berechtigungen für Stammverzeichnisse und alle Unterverzeichnisse und Dateien erteilt werden.</span><span class="sxs-lookup"><span data-stu-id="ed0b1-114">This command recursively modifies the ACE for Patti Fuller to have all permissions to root and all its subdirectories and files.</span></span>

## <span data-ttu-id="ed0b1-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="ed0b1-115">PARAMETERS</span></span>

### <span data-ttu-id="ed0b1-116">-Konto</span><span class="sxs-lookup"><span data-stu-id="ed0b1-116">-Account</span></span>
<span data-ttu-id="ed0b1-117">Gibt den Namen des Data Lake Store-Kontos an.</span><span class="sxs-lookup"><span data-stu-id="ed0b1-117">Specifies the name of the Data Lake Store account.</span></span>

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

### <span data-ttu-id="ed0b1-118">-AceType</span><span class="sxs-lookup"><span data-stu-id="ed0b1-118">-AceType</span></span>
<span data-ttu-id="ed0b1-119">Gibt den Typ des zu ändernden ACE an.</span><span class="sxs-lookup"><span data-stu-id="ed0b1-119">Specifies the type of ACE to modify.</span></span>
<span data-ttu-id="ed0b1-120">Die zulässigen Werte für diesen Parameter sind:</span><span class="sxs-lookup"><span data-stu-id="ed0b1-120">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="ed0b1-121">Benutzer</span><span class="sxs-lookup"><span data-stu-id="ed0b1-121">User</span></span> 
- <span data-ttu-id="ed0b1-122">Gruppe</span><span class="sxs-lookup"><span data-stu-id="ed0b1-122">Group</span></span> 
- <span data-ttu-id="ed0b1-123">Mask</span><span class="sxs-lookup"><span data-stu-id="ed0b1-123">Mask</span></span> 
- <span data-ttu-id="ed0b1-124">Sonstiges</span><span class="sxs-lookup"><span data-stu-id="ed0b1-124">Other</span></span>

```yaml
Type: Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStoreEnums+AceType
Parameter Sets: SetSpecificACE
Aliases:
Accepted values: User, Group, Mask, Other

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ed0b1-125">-Acl</span><span class="sxs-lookup"><span data-stu-id="ed0b1-125">-Acl</span></span>
<span data-ttu-id="ed0b1-126">Gibt das ACL-Objekt an, das die zu ändernden Einträge enthält.</span><span class="sxs-lookup"><span data-stu-id="ed0b1-126">Specifies the ACL object that contains the entries to modify.</span></span>

```yaml
Type: Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStoreItemAce[]
Parameter Sets: SetByACLObject
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ed0b1-127">-Parallelität</span><span class="sxs-lookup"><span data-stu-id="ed0b1-127">-Concurrency</span></span>
<span data-ttu-id="ed0b1-128">Die Anzahl der parallel verarbeiteten Dateien/Verzeichnisse.</span><span class="sxs-lookup"><span data-stu-id="ed0b1-128">Number of files/directories processed in parallel.</span></span> <span data-ttu-id="ed0b1-129">Optional: Es wird ein angemessener Standardwert ausgewählt.</span><span class="sxs-lookup"><span data-stu-id="ed0b1-129">Optional: a reasonable default will be selected</span></span>

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

### <span data-ttu-id="ed0b1-130">-Default</span><span class="sxs-lookup"><span data-stu-id="ed0b1-130">-Default</span></span>
<span data-ttu-id="ed0b1-131">Gibt an, dass durch diesen Vorgang der Standard-ACE von der angegebenen ACL geändert wird.</span><span class="sxs-lookup"><span data-stu-id="ed0b1-131">Indicates that this operation modifies the default ACE from the specified ACL.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: SetSpecificACE
Aliases:

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ed0b1-132">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ed0b1-132">-DefaultProfile</span></span>
<span data-ttu-id="ed0b1-133">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="ed0b1-133">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ed0b1-134">-ID</span><span class="sxs-lookup"><span data-stu-id="ed0b1-134">-Id</span></span>
<span data-ttu-id="ed0b1-135">Gibt die Objekt-ID des AzureActive Directory-Benutzers, der Gruppe oder des Dienstprinzipal an, für den bzw. die ein ACE geändert werden soll.</span><span class="sxs-lookup"><span data-stu-id="ed0b1-135">Specifies the object ID of the AzureActive Directory user, group, or service principal for which to modify an ACE.</span></span>

```yaml
Type: System.Guid
Parameter Sets: SetSpecificACE
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ed0b1-136">-PassThru</span><span class="sxs-lookup"><span data-stu-id="ed0b1-136">-PassThru</span></span>
<span data-ttu-id="ed0b1-137">Gibt an, dass die resultierende ACL zurückgegeben werden soll.</span><span class="sxs-lookup"><span data-stu-id="ed0b1-137">Indicates the resulting ACL should be returned.</span></span>

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

### <span data-ttu-id="ed0b1-138">-Path</span><span class="sxs-lookup"><span data-stu-id="ed0b1-138">-Path</span></span>
<span data-ttu-id="ed0b1-139">Gibt den Data Lake Store-Pfad des Elements an, für das ein ACE geändert werden soll, beginnend mit dem Stammverzeichnis (/).</span><span class="sxs-lookup"><span data-stu-id="ed0b1-139">Specifies the Data Lake Store path of the item for which to modify an ACE, starting with the root directory (/).</span></span>

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

### <span data-ttu-id="ed0b1-140">-Permissions</span><span class="sxs-lookup"><span data-stu-id="ed0b1-140">-Permissions</span></span>
<span data-ttu-id="ed0b1-141">Gibt die Berechtigungen für das ACE an.</span><span class="sxs-lookup"><span data-stu-id="ed0b1-141">Specifies the permissions for the ACE.</span></span>
<span data-ttu-id="ed0b1-142">Die zulässigen Werte für diesen Parameter sind:</span><span class="sxs-lookup"><span data-stu-id="ed0b1-142">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="ed0b1-143">Keine</span><span class="sxs-lookup"><span data-stu-id="ed0b1-143">None</span></span>
- <span data-ttu-id="ed0b1-144">Ausführen</span><span class="sxs-lookup"><span data-stu-id="ed0b1-144">Execute</span></span>
- <span data-ttu-id="ed0b1-145">Schreiben</span><span class="sxs-lookup"><span data-stu-id="ed0b1-145">Write</span></span>
- <span data-ttu-id="ed0b1-146">WriteExecute</span><span class="sxs-lookup"><span data-stu-id="ed0b1-146">WriteExecute</span></span>
- <span data-ttu-id="ed0b1-147">Lesen</span><span class="sxs-lookup"><span data-stu-id="ed0b1-147">Read</span></span>
- <span data-ttu-id="ed0b1-148">ReadExecute</span><span class="sxs-lookup"><span data-stu-id="ed0b1-148">ReadExecute</span></span>
- <span data-ttu-id="ed0b1-149">ReadWrite</span><span class="sxs-lookup"><span data-stu-id="ed0b1-149">ReadWrite</span></span>
- <span data-ttu-id="ed0b1-150">Alle</span><span class="sxs-lookup"><span data-stu-id="ed0b1-150">All</span></span>

```yaml
Type: Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStoreEnums+Permission
Parameter Sets: SetSpecificACE
Aliases:

Required: True
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ed0b1-151">-Recurse</span><span class="sxs-lookup"><span data-stu-id="ed0b1-151">-Recurse</span></span>
<span data-ttu-id="ed0b1-152">Gibt an, dass die ACL rekursiv in die untergeordneten Unterverzeichnisse und Dateien geändert werden soll.</span><span class="sxs-lookup"><span data-stu-id="ed0b1-152">Indicates the ACL to be modified recursively to the child subdirectories and files</span></span>

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

### <span data-ttu-id="ed0b1-153">-ShowProgress</span><span class="sxs-lookup"><span data-stu-id="ed0b1-153">-ShowProgress</span></span>
<span data-ttu-id="ed0b1-154">Wenn der Status erfolgreich ist, wird der Status angezeigt.</span><span class="sxs-lookup"><span data-stu-id="ed0b1-154">If passed then progress status is showed.</span></span> <span data-ttu-id="ed0b1-155">Gilt nur, wenn eine rekursive Änderung des Acl erfolgt.</span><span class="sxs-lookup"><span data-stu-id="ed0b1-155">Only applicable when recursive Acl modify is done.</span></span>

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

### <span data-ttu-id="ed0b1-156">-Confirm</span><span class="sxs-lookup"><span data-stu-id="ed0b1-156">-Confirm</span></span>
<span data-ttu-id="ed0b1-157">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="ed0b1-157">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ed0b1-158">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="ed0b1-158">-WhatIf</span></span>
<span data-ttu-id="ed0b1-159">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="ed0b1-159">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ed0b1-160">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="ed0b1-160">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ed0b1-161">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ed0b1-161">CommonParameters</span></span>
<span data-ttu-id="ed0b1-162">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ed0b1-162">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ed0b1-163">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ed0b1-163">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ed0b1-164">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="ed0b1-164">INPUTS</span></span>

### <span data-ttu-id="ed0b1-165">System.String</span><span class="sxs-lookup"><span data-stu-id="ed0b1-165">System.String</span></span>

### <span data-ttu-id="ed0b1-166">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStorePathInstance</span><span class="sxs-lookup"><span data-stu-id="ed0b1-166">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStorePathInstance</span></span>

### <span data-ttu-id="ed0b1-167">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStoreItemAce[]</span><span class="sxs-lookup"><span data-stu-id="ed0b1-167">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStoreItemAce[]</span></span>

### <span data-ttu-id="ed0b1-168">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStoreEnums+AceType</span><span class="sxs-lookup"><span data-stu-id="ed0b1-168">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStoreEnums+AceType</span></span>

### <span data-ttu-id="ed0b1-169">System.Guid</span><span class="sxs-lookup"><span data-stu-id="ed0b1-169">System.Guid</span></span>

### <span data-ttu-id="ed0b1-170">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStoreEnums+Permission</span><span class="sxs-lookup"><span data-stu-id="ed0b1-170">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStoreEnums+Permission</span></span>

### <span data-ttu-id="ed0b1-171">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="ed0b1-171">System.Management.Automation.SwitchParameter</span></span>

### <span data-ttu-id="ed0b1-172">System.Int32</span><span class="sxs-lookup"><span data-stu-id="ed0b1-172">System.Int32</span></span>

## <span data-ttu-id="ed0b1-173">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="ed0b1-173">OUTPUTS</span></span>

### <span data-ttu-id="ed0b1-174">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStoreItemAce</span><span class="sxs-lookup"><span data-stu-id="ed0b1-174">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStoreItemAce</span></span>

## <span data-ttu-id="ed0b1-175">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="ed0b1-175">NOTES</span></span>

## <span data-ttu-id="ed0b1-176">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="ed0b1-176">RELATED LINKS</span></span>

[<span data-ttu-id="ed0b1-177">Remove-AzDataLakeStoreItemAclEntry</span><span class="sxs-lookup"><span data-stu-id="ed0b1-177">Remove-AzDataLakeStoreItemAclEntry</span></span>](./Remove-AzDataLakeStoreItemAclEntry.md)


