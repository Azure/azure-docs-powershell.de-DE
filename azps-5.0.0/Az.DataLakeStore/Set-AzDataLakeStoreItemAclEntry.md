---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeStore.dll-Help.xml
Module Name: Az.DataLakeStore
ms.assetid: 0671D833-8B3A-4480-A576-92F1A9E8CE92
online version: https://docs.microsoft.com/en-us/powershell/module/az.datalakestore/set-azdatalakestoreitemaclentry
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Set-AzDataLakeStoreItemAclEntry.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Set-AzDataLakeStoreItemAclEntry.md
ms.openlocfilehash: 4f432596e6165989df07187a9383da04f0929a2d
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94297748"
---
# <span data-ttu-id="a888f-101">Set-AzDataLakeStoreItemAclEntry</span><span class="sxs-lookup"><span data-stu-id="a888f-101">Set-AzDataLakeStoreItemAclEntry</span></span>

## <span data-ttu-id="a888f-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="a888f-102">SYNOPSIS</span></span>
<span data-ttu-id="a888f-103">Ändert einen Eintrag in der ACL einer Datei oder eines Ordners im Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="a888f-103">Modifies an entry in the ACL of a file or folder in Data Lake Store.</span></span>

## <span data-ttu-id="a888f-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="a888f-104">SYNTAX</span></span>

### <span data-ttu-id="a888f-105">SetByACLObject (Standard)</span><span class="sxs-lookup"><span data-stu-id="a888f-105">SetByACLObject (Default)</span></span>
```
Set-AzDataLakeStoreItemAclEntry [-Account] <String> [-Path] <DataLakeStorePathInstance>
 [-Acl] <DataLakeStoreItemAce[]> [-PassThru] [-Recurse] [-Concurrency <Int32>] [-ShowProgress]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a888f-106">SetSpecificACE</span><span class="sxs-lookup"><span data-stu-id="a888f-106">SetSpecificACE</span></span>
```
Set-AzDataLakeStoreItemAclEntry [-Account] <String> [-Path] <DataLakeStorePathInstance> [-AceType] <AceType>
 [[-Id] <Guid>] [-Permissions] <Permission> [-Default] [-PassThru] [-Recurse] [-Concurrency <Int32>]
 [-ShowProgress] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a888f-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="a888f-107">DESCRIPTION</span></span>
<span data-ttu-id="a888f-108">Das Cmdlet " **festlegen-AzDataLakeStoreItemAclEntry** " ändert einen Eintrag (ACE) in der Zugriffssteuerungsliste (ACL) einer Datei oder eines Ordners im Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="a888f-108">The **Set-AzDataLakeStoreItemAclEntry** cmdlet modifies an entry (ACE) in the access control list (ACL) of a file or folder in Data Lake Store.</span></span>

## <span data-ttu-id="a888f-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="a888f-109">EXAMPLES</span></span>

### <span data-ttu-id="a888f-110">Beispiel 1: Ändern von Berechtigungen für einen ACE</span><span class="sxs-lookup"><span data-stu-id="a888f-110">Example 1: Modify permissions for an ACE</span></span>
```
PS C:\>Set-AzDataLakeStoreItemAclEntry -AccountName "ContosoADL" -Path / -AceType User -Id (Get-AzADUser -Mail "PattiFuller@contoso.com").ObjectId -Permissions All
```

<span data-ttu-id="a888f-111">Mit diesem Befehl wird das Ass für Patti Fuller so geändert, dass alle Berechtigungen vorhanden sind.</span><span class="sxs-lookup"><span data-stu-id="a888f-111">This command modifies the ACE for Patti Fuller to have all permissions.</span></span>

### <span data-ttu-id="a888f-112">Beispiel 2: rekursives Ändern der Berechtigungen für ein Ass</span><span class="sxs-lookup"><span data-stu-id="a888f-112">Example 2: Modify permissions for an ACE recursively</span></span>
```
PS C:\>Set-AzDataLakeStoreItemAclEntry -AccountName "ContosoADL" -Path / -AceType User -Id (Get-AzADUser -Mail "PattiFuller@contoso.com").ObjectId -Permissions All -Recurse -Concurrency 128
```

### <span data-ttu-id="a888f-113">Beispiel 3: Ändern der Berechtigungen für ein Ass rekursiv mithilfe des ACL-Objekts</span><span class="sxs-lookup"><span data-stu-id="a888f-113">Example 3: Modify permissions for an ACE recursively using Acl object</span></span>
```
PS C:\>$fullAcl="user:userid1:--x,default:user:userid1:--x"
PS C:\>$newFullAcl = $fullAcl.Split("{,}")
PS C:\>Set-AzDataLakeStoreItemAclEntry -AccountName "ContosoADL" -Path / -Acl $newFullAcl -Recurse -Concurrency 128
```

<span data-ttu-id="a888f-114">Mit diesem Befehl wird der ACE für Patti Fuller rekursiv so geändert, dass alle Berechtigungen für root und alle zugehörigen Unterverzeichnisse und Dateien vorhanden sind.</span><span class="sxs-lookup"><span data-stu-id="a888f-114">This command recursively modifies the ACE for Patti Fuller to have all permissions to root and all its subdirectories and files.</span></span>

## <span data-ttu-id="a888f-115">Parameter</span><span class="sxs-lookup"><span data-stu-id="a888f-115">PARAMETERS</span></span>

### <span data-ttu-id="a888f-116">-Konto</span><span class="sxs-lookup"><span data-stu-id="a888f-116">-Account</span></span>
<span data-ttu-id="a888f-117">Gibt den Namen des Data Lake Store-Kontos an.</span><span class="sxs-lookup"><span data-stu-id="a888f-117">Specifies the name of the Data Lake Store account.</span></span>

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

### <span data-ttu-id="a888f-118">-AceType</span><span class="sxs-lookup"><span data-stu-id="a888f-118">-AceType</span></span>
<span data-ttu-id="a888f-119">Gibt den Typ des zu ändernden ACE an.</span><span class="sxs-lookup"><span data-stu-id="a888f-119">Specifies the type of ACE to modify.</span></span>
<span data-ttu-id="a888f-120">Die zulässigen Werte für diesen Parameter lauten wie folgt:</span><span class="sxs-lookup"><span data-stu-id="a888f-120">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="a888f-121">Benutzer</span><span class="sxs-lookup"><span data-stu-id="a888f-121">User</span></span> 
- <span data-ttu-id="a888f-122">Gruppe</span><span class="sxs-lookup"><span data-stu-id="a888f-122">Group</span></span> 
- <span data-ttu-id="a888f-123">Format</span><span class="sxs-lookup"><span data-stu-id="a888f-123">Mask</span></span> 
- <span data-ttu-id="a888f-124">Anderen</span><span class="sxs-lookup"><span data-stu-id="a888f-124">Other</span></span>

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

### <span data-ttu-id="a888f-125">-ACL</span><span class="sxs-lookup"><span data-stu-id="a888f-125">-Acl</span></span>
<span data-ttu-id="a888f-126">Gibt das ACL-Objekt an, das die zu ändernden Einträge enthält.</span><span class="sxs-lookup"><span data-stu-id="a888f-126">Specifies the ACL object that contains the entries to modify.</span></span>

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

### <span data-ttu-id="a888f-127">-Parallelität</span><span class="sxs-lookup"><span data-stu-id="a888f-127">-Concurrency</span></span>
<span data-ttu-id="a888f-128">Die Anzahl von Dateien/Verzeichnissen, die parallel verarbeitet werden.</span><span class="sxs-lookup"><span data-stu-id="a888f-128">Number of files/directories processed in parallel.</span></span> <span data-ttu-id="a888f-129">Optional: ein angemessener Standardwert wird ausgewählt.</span><span class="sxs-lookup"><span data-stu-id="a888f-129">Optional: a reasonable default will be selected</span></span>

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

### <span data-ttu-id="a888f-130">– Standard</span><span class="sxs-lookup"><span data-stu-id="a888f-130">-Default</span></span>
<span data-ttu-id="a888f-131">Gibt an, dass dieser Vorgang den Standard-ACE aus der angegebenen ACL ändert.</span><span class="sxs-lookup"><span data-stu-id="a888f-131">Indicates that this operation modifies the default ACE from the specified ACL.</span></span>

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

### <span data-ttu-id="a888f-132">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a888f-132">-DefaultProfile</span></span>
<span data-ttu-id="a888f-133">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="a888f-133">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a888f-134">-ID</span><span class="sxs-lookup"><span data-stu-id="a888f-134">-Id</span></span>
<span data-ttu-id="a888f-135">Gibt die Objekt-ID des AzureActive-Verzeichnis Benutzers, der Gruppe oder des Dienst Prinzipals an, für den ein ACE geändert werden soll.</span><span class="sxs-lookup"><span data-stu-id="a888f-135">Specifies the object ID of the AzureActive Directory user, group, or service principal for which to modify an ACE.</span></span>

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

### <span data-ttu-id="a888f-136">-PassThru</span><span class="sxs-lookup"><span data-stu-id="a888f-136">-PassThru</span></span>
<span data-ttu-id="a888f-137">Gibt an, dass die resultierende ACL zurückgegeben werden soll.</span><span class="sxs-lookup"><span data-stu-id="a888f-137">Indicates the resulting ACL should be returned.</span></span>

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

### <span data-ttu-id="a888f-138">-Path</span><span class="sxs-lookup"><span data-stu-id="a888f-138">-Path</span></span>
<span data-ttu-id="a888f-139">Gibt den Daten See-Speicherpfad des Elements an, für das ein ACE geändert werden soll, beginnend mit dem Stammverzeichnis (/).</span><span class="sxs-lookup"><span data-stu-id="a888f-139">Specifies the Data Lake Store path of the item for which to modify an ACE, starting with the root directory (/).</span></span>

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

### <span data-ttu-id="a888f-140">-Berechtigungen</span><span class="sxs-lookup"><span data-stu-id="a888f-140">-Permissions</span></span>
<span data-ttu-id="a888f-141">Gibt die Berechtigungen für das ACE an.</span><span class="sxs-lookup"><span data-stu-id="a888f-141">Specifies the permissions for the ACE.</span></span>
<span data-ttu-id="a888f-142">Die zulässigen Werte für diesen Parameter lauten wie folgt:</span><span class="sxs-lookup"><span data-stu-id="a888f-142">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="a888f-143">Keine</span><span class="sxs-lookup"><span data-stu-id="a888f-143">None</span></span>
- <span data-ttu-id="a888f-144">Ausführen</span><span class="sxs-lookup"><span data-stu-id="a888f-144">Execute</span></span>
- <span data-ttu-id="a888f-145">Schreiben</span><span class="sxs-lookup"><span data-stu-id="a888f-145">Write</span></span>
- <span data-ttu-id="a888f-146">WriteExecute</span><span class="sxs-lookup"><span data-stu-id="a888f-146">WriteExecute</span></span>
- <span data-ttu-id="a888f-147">Lesen</span><span class="sxs-lookup"><span data-stu-id="a888f-147">Read</span></span>
- <span data-ttu-id="a888f-148">ReadExecute</span><span class="sxs-lookup"><span data-stu-id="a888f-148">ReadExecute</span></span>
- <span data-ttu-id="a888f-149">ReadWrite</span><span class="sxs-lookup"><span data-stu-id="a888f-149">ReadWrite</span></span>
- <span data-ttu-id="a888f-150">Alle</span><span class="sxs-lookup"><span data-stu-id="a888f-150">All</span></span>

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

### <span data-ttu-id="a888f-151">-Rekursiv</span><span class="sxs-lookup"><span data-stu-id="a888f-151">-Recurse</span></span>
<span data-ttu-id="a888f-152">Gibt an, dass die ACL rekursiv auf die untergeordneten Unterverzeichnisse und Dateien geändert werden soll.</span><span class="sxs-lookup"><span data-stu-id="a888f-152">Indicates the ACL to be modified recursively to the child subdirectories and files</span></span>

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

### <span data-ttu-id="a888f-153">-Progress</span><span class="sxs-lookup"><span data-stu-id="a888f-153">-ShowProgress</span></span>
<span data-ttu-id="a888f-154">Wenn übergeben, wird der Status Status angezeigt.</span><span class="sxs-lookup"><span data-stu-id="a888f-154">If passed then progress status is showed.</span></span> <span data-ttu-id="a888f-155">Gilt nur, wenn die rekursive ACL-Änderung durchgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="a888f-155">Only applicable when recursive Acl modify is done.</span></span>

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

### <span data-ttu-id="a888f-156">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="a888f-156">-Confirm</span></span>
<span data-ttu-id="a888f-157">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="a888f-157">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a888f-158">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a888f-158">-WhatIf</span></span>
<span data-ttu-id="a888f-159">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="a888f-159">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a888f-160">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="a888f-160">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a888f-161">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a888f-161">CommonParameters</span></span>
<span data-ttu-id="a888f-162">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a888f-162">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a888f-163">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a888f-163">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a888f-164">Eingaben</span><span class="sxs-lookup"><span data-stu-id="a888f-164">INPUTS</span></span>

### <span data-ttu-id="a888f-165">System. String</span><span class="sxs-lookup"><span data-stu-id="a888f-165">System.String</span></span>

### <span data-ttu-id="a888f-166">Microsoft. Azure. Commands. DataLakeStore. Models. DataLakeStorePathInstance</span><span class="sxs-lookup"><span data-stu-id="a888f-166">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStorePathInstance</span></span>

### <span data-ttu-id="a888f-167">Microsoft. Azure. Commands. DataLakeStore. Models. DataLakeStoreItemAce []</span><span class="sxs-lookup"><span data-stu-id="a888f-167">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStoreItemAce[]</span></span>

### <span data-ttu-id="a888f-168">Microsoft. Azure. Commands. DataLakeStore. Models. DataLakeStoreEnums + AceType</span><span class="sxs-lookup"><span data-stu-id="a888f-168">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStoreEnums+AceType</span></span>

### <span data-ttu-id="a888f-169">System. GUID</span><span class="sxs-lookup"><span data-stu-id="a888f-169">System.Guid</span></span>

### <span data-ttu-id="a888f-170">Microsoft. Azure. Commands. DataLakeStore. Models. DataLakeStoreEnums +-Berechtigung</span><span class="sxs-lookup"><span data-stu-id="a888f-170">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStoreEnums+Permission</span></span>

### <span data-ttu-id="a888f-171">System. Management. Automation. Switchparameter</span><span class="sxs-lookup"><span data-stu-id="a888f-171">System.Management.Automation.SwitchParameter</span></span>

### <span data-ttu-id="a888f-172">System. Int32</span><span class="sxs-lookup"><span data-stu-id="a888f-172">System.Int32</span></span>

## <span data-ttu-id="a888f-173">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="a888f-173">OUTPUTS</span></span>

### <span data-ttu-id="a888f-174">Microsoft. Azure. Commands. DataLakeStore. Models. DataLakeStoreItemAce</span><span class="sxs-lookup"><span data-stu-id="a888f-174">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStoreItemAce</span></span>

## <span data-ttu-id="a888f-175">Notizen</span><span class="sxs-lookup"><span data-stu-id="a888f-175">NOTES</span></span>

## <span data-ttu-id="a888f-176">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="a888f-176">RELATED LINKS</span></span>

[<span data-ttu-id="a888f-177">Remove-AzDataLakeStoreItemAclEntry</span><span class="sxs-lookup"><span data-stu-id="a888f-177">Remove-AzDataLakeStoreItemAclEntry</span></span>](./Remove-AzDataLakeStoreItemAclEntry.md)


