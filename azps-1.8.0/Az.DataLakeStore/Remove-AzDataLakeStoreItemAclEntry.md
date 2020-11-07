---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeStore.dll-Help.xml
Module Name: Az.DataLakeStore
ms.assetid: 33E7607E-C2BC-4F46-9038-91AC92041F00
online version: https://docs.microsoft.com/en-us/powershell/module/az.datalakestore/remove-azdatalakestoreitemaclentry
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Remove-AzDataLakeStoreItemAclEntry.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Remove-AzDataLakeStoreItemAclEntry.md
ms.openlocfilehash: 7cc09813f03e5424b7d44b7a56810167ca5affba
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93661262"
---
# <span data-ttu-id="f6571-101">Remove-AzDataLakeStoreItemAclEntry</span><span class="sxs-lookup"><span data-stu-id="f6571-101">Remove-AzDataLakeStoreItemAclEntry</span></span>

## <span data-ttu-id="f6571-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="f6571-102">SYNOPSIS</span></span>
<span data-ttu-id="f6571-103">Entfernt einen Eintrag aus der ACL einer Datei oder eines Ordners im Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="f6571-103">Removes an entry from the ACL of a file or folder in Data Lake Store.</span></span>

## <span data-ttu-id="f6571-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="f6571-104">SYNTAX</span></span>

### <span data-ttu-id="f6571-105">RemoveByACLObject (Standard)</span><span class="sxs-lookup"><span data-stu-id="f6571-105">RemoveByACLObject (Default)</span></span>
```
Remove-AzDataLakeStoreItemAclEntry [-Account] <String> [-Path] <DataLakeStorePathInstance>
 [-Acl] <DataLakeStoreItemAce[]> [-PassThru] [-Recurse] [-Concurrency <Int32>] [-ShowProgress]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f6571-106">RemoveSpecificACE</span><span class="sxs-lookup"><span data-stu-id="f6571-106">RemoveSpecificACE</span></span>
```
Remove-AzDataLakeStoreItemAclEntry [-Account] <String> [-Path] <DataLakeStorePathInstance> [-AceType] <AceType>
 [[-Id] <Guid>] [-Default] [-PassThru] [-Recurse] [-Concurrency <Int32>] [-ShowProgress]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f6571-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="f6571-107">DESCRIPTION</span></span>
<span data-ttu-id="f6571-108">Das Cmdlet **Remove-AzDataLakeStoreItemAclEntry** entfernt einen Eintrag (ACE) aus der Zugriffssteuerungsliste (ACL) einer Datei oder eines Ordners im Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="f6571-108">The **Remove-AzDataLakeStoreItemAclEntry** cmdlet removes an entry (ACE) from the access control list (ACL) of a file or folder in Data Lake Store.</span></span>

## <span data-ttu-id="f6571-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="f6571-109">EXAMPLES</span></span>

### <span data-ttu-id="f6571-110">Beispiel 1: Entfernen eines Benutzereintrags</span><span class="sxs-lookup"><span data-stu-id="f6571-110">Example 1: Remove a user entry</span></span>
```
PS C:\>Remove-AzDataLakeStoreItemAclEntry -AccountName "ContosoADL" -Path / -AceType User -Id (Get-AzADUser -Mail "PattiFuller@contoso.com").ObjectId
```

<span data-ttu-id="f6571-111">Dieser Befehl entfernt das Benutzer-Ass für Patti Fuller aus dem ContosoADL-Konto.</span><span class="sxs-lookup"><span data-stu-id="f6571-111">This command removes the user ACE for Patti Fuller from the ContosoADL account.</span></span>

### <span data-ttu-id="f6571-112">Beispiel 2: rekursives Entfernen eines Benutzereintrags</span><span class="sxs-lookup"><span data-stu-id="f6571-112">Example 2: Remove a user entry recursively</span></span>
```
PS C:\>Remove-AzDataLakeStoreItemAclEntry -AccountName "ContosoADL" -Path / -AceType User -Id (Get-AzADUser -Mail "PattiFuller@contoso.com").ObjectId -Recurse -Concurrency 128
```

### <span data-ttu-id="f6571-113">Beispiel 3: Entfernen von Berechtigungen für ein Ass rekursiv mithilfe des ACL-Objekts</span><span class="sxs-lookup"><span data-stu-id="f6571-113">Example 3: Remove permissions for an ACE recursively using Acl object</span></span>
```
PS C:\>$fullAcl="user:userid1,default:user:userid1
PS C:\>$newFullAcl = $fullAcl.Split("{,}")
PS C:\>Remove-AzDataLakeStoreItemAclEntry -AccountName "ContosoADL" -Path / -Acl $newFullAcl -Recurse -Concurrency 128
```

<span data-ttu-id="f6571-114">Dieser Befehl entfernt das Benutzer-Ass für Patti Fuller aus dem Stammverzeichnis und rekursiv aus allen Unterverzeichnissen und Dateien für das Konto ContosoADL.</span><span class="sxs-lookup"><span data-stu-id="f6571-114">This command removes the user ACE for Patti Fuller from the root and recursively from all it's subdirectories and files for account ContosoADL.</span></span>

## <span data-ttu-id="f6571-115">Parameter</span><span class="sxs-lookup"><span data-stu-id="f6571-115">PARAMETERS</span></span>

### <span data-ttu-id="f6571-116">-Konto</span><span class="sxs-lookup"><span data-stu-id="f6571-116">-Account</span></span>
<span data-ttu-id="f6571-117">Gibt den Namen des Data Lake Store-Kontos an.</span><span class="sxs-lookup"><span data-stu-id="f6571-117">Specifies the name of the Data Lake Store account.</span></span>

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

### <span data-ttu-id="f6571-118">-AceType</span><span class="sxs-lookup"><span data-stu-id="f6571-118">-AceType</span></span>
<span data-ttu-id="f6571-119">Gibt den Typ des zu entfernenden ACE an.</span><span class="sxs-lookup"><span data-stu-id="f6571-119">Specifies the type of ACE to remove.</span></span>
<span data-ttu-id="f6571-120">Die zulässigen Werte für diesen Parameter lauten wie folgt:</span><span class="sxs-lookup"><span data-stu-id="f6571-120">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="f6571-121">Benutzer</span><span class="sxs-lookup"><span data-stu-id="f6571-121">User</span></span>
- <span data-ttu-id="f6571-122">Gruppe</span><span class="sxs-lookup"><span data-stu-id="f6571-122">Group</span></span>
- <span data-ttu-id="f6571-123">Format</span><span class="sxs-lookup"><span data-stu-id="f6571-123">Mask</span></span>
- <span data-ttu-id="f6571-124">Anderen</span><span class="sxs-lookup"><span data-stu-id="f6571-124">Other</span></span>

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

### <span data-ttu-id="f6571-125">-ACL</span><span class="sxs-lookup"><span data-stu-id="f6571-125">-Acl</span></span>
<span data-ttu-id="f6571-126">Gibt das ACL-Objekt an, das die zu entfernende Einträge enthält.</span><span class="sxs-lookup"><span data-stu-id="f6571-126">Specifies the ACL object that contains the entries to be removed.</span></span>

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

### <span data-ttu-id="f6571-127">-Parallelität</span><span class="sxs-lookup"><span data-stu-id="f6571-127">-Concurrency</span></span>
<span data-ttu-id="f6571-128">Die Anzahl von Dateien/Verzeichnissen, die parallel verarbeitet werden.</span><span class="sxs-lookup"><span data-stu-id="f6571-128">Number of files/directories processed in parallel.</span></span> <span data-ttu-id="f6571-129">Optional: ein angemessener Standardwert wird ausgewählt.</span><span class="sxs-lookup"><span data-stu-id="f6571-129">Optional: a reasonable default will be selected</span></span>

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

### <span data-ttu-id="f6571-130">– Standard</span><span class="sxs-lookup"><span data-stu-id="f6571-130">-Default</span></span>
<span data-ttu-id="f6571-131">Gibt an, dass dieser Vorgang das Standard-Ass aus der angegebenen ACL entfernt.</span><span class="sxs-lookup"><span data-stu-id="f6571-131">Indicates that this operation removes the default ACE from the specified ACL.</span></span>

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

### <span data-ttu-id="f6571-132">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f6571-132">-DefaultProfile</span></span>
<span data-ttu-id="f6571-133">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="f6571-133">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f6571-134">-ID</span><span class="sxs-lookup"><span data-stu-id="f6571-134">-Id</span></span>
<span data-ttu-id="f6571-135">Gibt die Objekt-ID des AzureActive-Verzeichnis Benutzers, der Gruppe oder des Dienst Prinzipals an, für den ein ACE entfernt werden soll.</span><span class="sxs-lookup"><span data-stu-id="f6571-135">Specifies the object ID of the AzureActive Directory user, group, or service principal for which to remove an ACE.</span></span>

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

### <span data-ttu-id="f6571-136">-PassThru</span><span class="sxs-lookup"><span data-stu-id="f6571-136">-PassThru</span></span>
<span data-ttu-id="f6571-137">Gibt an, dass eine boolesche Antwort zurückgegeben werden soll, die das Ergebnis des Löschvorgangs angibt.</span><span class="sxs-lookup"><span data-stu-id="f6571-137">Indicates a boolean response should be returned indicating the result of the delete operation.</span></span>

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

### <span data-ttu-id="f6571-138">-Path</span><span class="sxs-lookup"><span data-stu-id="f6571-138">-Path</span></span>
<span data-ttu-id="f6571-139">Gibt den Daten See-Speicherpfad des Elements an, aus dem ein ACE entfernt werden soll, beginnend mit dem Stammverzeichnis (/).</span><span class="sxs-lookup"><span data-stu-id="f6571-139">Specifies the Data Lake Store path of the item from which to remove an ACE, starting with the root directory (/).</span></span>

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

### <span data-ttu-id="f6571-140">-Rekursiv</span><span class="sxs-lookup"><span data-stu-id="f6571-140">-Recurse</span></span>
<span data-ttu-id="f6571-141">Gibt an, dass die ACL rekursiv in die untergeordneten Unterverzeichnisse und Dateien entfernt werden soll.</span><span class="sxs-lookup"><span data-stu-id="f6571-141">Indicates the ACL to be removed recursively to the child subdirectories and files</span></span>

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

### <span data-ttu-id="f6571-142">-Progress</span><span class="sxs-lookup"><span data-stu-id="f6571-142">-ShowProgress</span></span>
<span data-ttu-id="f6571-143">Wenn übergeben, wird der Status Status angezeigt.</span><span class="sxs-lookup"><span data-stu-id="f6571-143">If passed then progress status is showed.</span></span> <span data-ttu-id="f6571-144">Gilt nur, wenn die rekursive ACL-Entfernung abgeschlossen ist.</span><span class="sxs-lookup"><span data-stu-id="f6571-144">Only applicable when recursive Acl remove is done.</span></span>

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

### <span data-ttu-id="f6571-145">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="f6571-145">-Confirm</span></span>
<span data-ttu-id="f6571-146">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="f6571-146">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f6571-147">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f6571-147">-WhatIf</span></span>
<span data-ttu-id="f6571-148">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="f6571-148">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f6571-149">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="f6571-149">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f6571-150">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f6571-150">CommonParameters</span></span>
<span data-ttu-id="f6571-151">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f6571-151">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f6571-152">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f6571-152">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f6571-153">Eingaben</span><span class="sxs-lookup"><span data-stu-id="f6571-153">INPUTS</span></span>

### <span data-ttu-id="f6571-154">System. String</span><span class="sxs-lookup"><span data-stu-id="f6571-154">System.String</span></span>

### <span data-ttu-id="f6571-155">Microsoft. Azure. Commands. DataLakeStore. Models. DataLakeStorePathInstance</span><span class="sxs-lookup"><span data-stu-id="f6571-155">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStorePathInstance</span></span>

### <span data-ttu-id="f6571-156">Microsoft. Azure. Commands. DataLakeStore. Models. DataLakeStoreItemAce []</span><span class="sxs-lookup"><span data-stu-id="f6571-156">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStoreItemAce[]</span></span>

### <span data-ttu-id="f6571-157">Microsoft. Azure. Commands. DataLakeStore. Models. DataLakeStoreEnums + AceType</span><span class="sxs-lookup"><span data-stu-id="f6571-157">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStoreEnums+AceType</span></span>

### <span data-ttu-id="f6571-158">System. GUID</span><span class="sxs-lookup"><span data-stu-id="f6571-158">System.Guid</span></span>

### <span data-ttu-id="f6571-159">System. Management. Automation. Switchparameter</span><span class="sxs-lookup"><span data-stu-id="f6571-159">System.Management.Automation.SwitchParameter</span></span>

### <span data-ttu-id="f6571-160">System. Int32</span><span class="sxs-lookup"><span data-stu-id="f6571-160">System.Int32</span></span>

## <span data-ttu-id="f6571-161">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="f6571-161">OUTPUTS</span></span>

### <span data-ttu-id="f6571-162">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="f6571-162">System.Boolean</span></span>

## <span data-ttu-id="f6571-163">Notizen</span><span class="sxs-lookup"><span data-stu-id="f6571-163">NOTES</span></span>

## <span data-ttu-id="f6571-164">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="f6571-164">RELATED LINKS</span></span>

[<span data-ttu-id="f6571-165">Satz-AzDataLakeStoreItemAclEntry</span><span class="sxs-lookup"><span data-stu-id="f6571-165">Set-AzDataLakeStoreItemAclEntry</span></span>](./Set-AzDataLakeStoreItemAclEntry.md)


