---
external help file: Microsoft.Azure.Commands.DataLakeStore.dll-Help.xml
Module Name: AzureRM.DataLakeStore
ms.assetid: 33E7607E-C2BC-4F46-9038-91AC92041F00
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datalakestore/remove-azurermdatalakestoreitemaclentry
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Remove-AzureRmDataLakeStoreItemAclEntry.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Remove-AzureRmDataLakeStoreItemAclEntry.md
ms.openlocfilehash: 154c57c6a403fce574a785aaf60d95a7936907b9
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93476097"
---
# <span data-ttu-id="72ff6-101">Remove-AzureRmDataLakeStoreItemAclEntry</span><span class="sxs-lookup"><span data-stu-id="72ff6-101">Remove-AzureRmDataLakeStoreItemAclEntry</span></span>

## <span data-ttu-id="72ff6-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="72ff6-102">SYNOPSIS</span></span>
<span data-ttu-id="72ff6-103">Entfernt einen Eintrag aus der ACL einer Datei oder eines Ordners im Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="72ff6-103">Removes an entry from the ACL of a file or folder in Data Lake Store.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="72ff6-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="72ff6-104">SYNTAX</span></span>

### <span data-ttu-id="72ff6-105">RemoveByACLObject (Standard)</span><span class="sxs-lookup"><span data-stu-id="72ff6-105">RemoveByACLObject (Default)</span></span>
```
Remove-AzureRmDataLakeStoreItemAclEntry [-Account] <String> [-Path] <DataLakeStorePathInstance>
 [-Acl] <DataLakeStoreItemAce[]> [-PassThru] [-Recurse] [-Concurrency <Int32>] [-ShowProgress]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="72ff6-106">RemoveSpecificACE</span><span class="sxs-lookup"><span data-stu-id="72ff6-106">RemoveSpecificACE</span></span>
```
Remove-AzureRmDataLakeStoreItemAclEntry [-Account] <String> [-Path] <DataLakeStorePathInstance>
 [-AceType] <AceType> [[-Id] <Guid>] [-Default] [-PassThru] [-Recurse] [-Concurrency <Int32>] [-ShowProgress]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="72ff6-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="72ff6-107">DESCRIPTION</span></span>
<span data-ttu-id="72ff6-108">Das Cmdlet **Remove-AzureRmDataLakeStoreItemAclEntry** entfernt einen Eintrag (ACE) aus der Zugriffssteuerungsliste (ACL) einer Datei oder eines Ordners im Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="72ff6-108">The **Remove-AzureRmDataLakeStoreItemAclEntry** cmdlet removes an entry (ACE) from the access control list (ACL) of a file or folder in Data Lake Store.</span></span>

## <span data-ttu-id="72ff6-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="72ff6-109">EXAMPLES</span></span>

### <span data-ttu-id="72ff6-110">Beispiel 1: Entfernen eines Benutzereintrags</span><span class="sxs-lookup"><span data-stu-id="72ff6-110">Example 1: Remove a user entry</span></span>
```
PS C:\>Remove-AzureRmDataLakeStoreItemAclEntry -AccountName "ContosoADL" -Path / -AceType User -Id (Get-AzureRmADUser -Mail "PattiFuller@contoso.com").ObjectId
```

<span data-ttu-id="72ff6-111">Dieser Befehl entfernt das Benutzer-Ass für Patti Fuller aus dem ContosoADL-Konto.</span><span class="sxs-lookup"><span data-stu-id="72ff6-111">This command removes the user ACE for Patti Fuller from the ContosoADL account.</span></span>

### <span data-ttu-id="72ff6-112">Beispiel 2: rekursives Entfernen eines Benutzereintrags</span><span class="sxs-lookup"><span data-stu-id="72ff6-112">Example 2: Remove a user entry recursively</span></span>
```
PS C:\>Remove-AzureRmDataLakeStoreItemAclEntry -AccountName "ContosoADL" -Path / -AceType User -Id (Get-AzureRmADUser -Mail "PattiFuller@contoso.com").ObjectId -Recurse -Concurrency 128
```

### <span data-ttu-id="72ff6-113">Beispiel 3: Entfernen von Berechtigungen für ein Ass rekursiv mithilfe des ACL-Objekts</span><span class="sxs-lookup"><span data-stu-id="72ff6-113">Example 3: Remove permissions for an ACE recursively using Acl object</span></span>
```
PS C:\>$fullAcl="user:userid1,default:user:userid1
PS C:\>$newFullAcl = $fullAcl.Split("{,}")
PS C:\>Remove-AzureRmDataLakeStoreItemAclEntry -AccountName "ContosoADL" -Path / -Acl $newFullAcl -Recurse -Concurrency 128
```

<span data-ttu-id="72ff6-114">Dieser Befehl entfernt das Benutzer-Ass für Patti Fuller aus dem Stammverzeichnis und rekursiv aus allen Unterverzeichnissen und Dateien für das Konto ContosoADL.</span><span class="sxs-lookup"><span data-stu-id="72ff6-114">This command removes the user ACE for Patti Fuller from the root and recursively from all it's subdirectories and files for account ContosoADL.</span></span>

## <span data-ttu-id="72ff6-115">Parameter</span><span class="sxs-lookup"><span data-stu-id="72ff6-115">PARAMETERS</span></span>

### <span data-ttu-id="72ff6-116">-Konto</span><span class="sxs-lookup"><span data-stu-id="72ff6-116">-Account</span></span>
<span data-ttu-id="72ff6-117">Gibt den Namen des Data Lake Store-Kontos an.</span><span class="sxs-lookup"><span data-stu-id="72ff6-117">Specifies the name of the Data Lake Store account.</span></span>

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

### <span data-ttu-id="72ff6-118">-AceType</span><span class="sxs-lookup"><span data-stu-id="72ff6-118">-AceType</span></span>
<span data-ttu-id="72ff6-119">Gibt den Typ des zu entfernenden ACE an.</span><span class="sxs-lookup"><span data-stu-id="72ff6-119">Specifies the type of ACE to remove.</span></span>
<span data-ttu-id="72ff6-120">Die zulässigen Werte für diesen Parameter lauten wie folgt:</span><span class="sxs-lookup"><span data-stu-id="72ff6-120">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="72ff6-121">Benutzer</span><span class="sxs-lookup"><span data-stu-id="72ff6-121">User</span></span>
- <span data-ttu-id="72ff6-122">Gruppe</span><span class="sxs-lookup"><span data-stu-id="72ff6-122">Group</span></span>
- <span data-ttu-id="72ff6-123">Format</span><span class="sxs-lookup"><span data-stu-id="72ff6-123">Mask</span></span>
- <span data-ttu-id="72ff6-124">Anderen</span><span class="sxs-lookup"><span data-stu-id="72ff6-124">Other</span></span>

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

### <span data-ttu-id="72ff6-125">-ACL</span><span class="sxs-lookup"><span data-stu-id="72ff6-125">-Acl</span></span>
<span data-ttu-id="72ff6-126">Gibt das ACL-Objekt an, das die zu entfernende Einträge enthält.</span><span class="sxs-lookup"><span data-stu-id="72ff6-126">Specifies the ACL object that contains the entries to be removed.</span></span>

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

### <span data-ttu-id="72ff6-127">-Parallelität</span><span class="sxs-lookup"><span data-stu-id="72ff6-127">-Concurrency</span></span>
<span data-ttu-id="72ff6-128">Die Anzahl von Dateien/Verzeichnissen, die parallel verarbeitet werden.</span><span class="sxs-lookup"><span data-stu-id="72ff6-128">Number of files/directories processed in parallel.</span></span> <span data-ttu-id="72ff6-129">Optional: ein angemessener Standardwert wird ausgewählt.</span><span class="sxs-lookup"><span data-stu-id="72ff6-129">Optional: a reasonable default will be selected</span></span>

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

### <span data-ttu-id="72ff6-130">– Standard</span><span class="sxs-lookup"><span data-stu-id="72ff6-130">-Default</span></span>
<span data-ttu-id="72ff6-131">Gibt an, dass dieser Vorgang das Standard-Ass aus der angegebenen ACL entfernt.</span><span class="sxs-lookup"><span data-stu-id="72ff6-131">Indicates that this operation removes the default ACE from the specified ACL.</span></span>

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

### <span data-ttu-id="72ff6-132">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="72ff6-132">-DefaultProfile</span></span>
<span data-ttu-id="72ff6-133">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="72ff6-133">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="72ff6-134">-ID</span><span class="sxs-lookup"><span data-stu-id="72ff6-134">-Id</span></span>
<span data-ttu-id="72ff6-135">Gibt die Objekt-ID des AzureActive-Verzeichnis Benutzers, der Gruppe oder des Dienst Prinzipals an, für den ein ACE entfernt werden soll.</span><span class="sxs-lookup"><span data-stu-id="72ff6-135">Specifies the object ID of the AzureActive Directory user, group, or service principal for which to remove an ACE.</span></span>

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

### <span data-ttu-id="72ff6-136">-PassThru</span><span class="sxs-lookup"><span data-stu-id="72ff6-136">-PassThru</span></span>
<span data-ttu-id="72ff6-137">Gibt an, dass eine boolesche Antwort zurückgegeben werden soll, die das Ergebnis des Löschvorgangs angibt.</span><span class="sxs-lookup"><span data-stu-id="72ff6-137">Indicates a boolean response should be returned indicating the result of the delete operation.</span></span>

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

### <span data-ttu-id="72ff6-138">-Path</span><span class="sxs-lookup"><span data-stu-id="72ff6-138">-Path</span></span>
<span data-ttu-id="72ff6-139">Gibt den Daten See-Speicherpfad des Elements an, aus dem ein ACE entfernt werden soll, beginnend mit dem Stammverzeichnis (/).</span><span class="sxs-lookup"><span data-stu-id="72ff6-139">Specifies the Data Lake Store path of the item from which to remove an ACE, starting with the root directory (/).</span></span>

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

### <span data-ttu-id="72ff6-140">-Rekursiv</span><span class="sxs-lookup"><span data-stu-id="72ff6-140">-Recurse</span></span>
<span data-ttu-id="72ff6-141">Gibt an, dass die ACL rekursiv in die untergeordneten Unterverzeichnisse und Dateien entfernt werden soll.</span><span class="sxs-lookup"><span data-stu-id="72ff6-141">Indicates the ACL to be removed recursively to the child subdirectories and files</span></span>

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

### <span data-ttu-id="72ff6-142">-Progress</span><span class="sxs-lookup"><span data-stu-id="72ff6-142">-ShowProgress</span></span>
<span data-ttu-id="72ff6-143">Wenn übergeben, wird der Status Status angezeigt.</span><span class="sxs-lookup"><span data-stu-id="72ff6-143">If passed then progress status is showed.</span></span> <span data-ttu-id="72ff6-144">Gilt nur, wenn die rekursive ACL-Entfernung abgeschlossen ist.</span><span class="sxs-lookup"><span data-stu-id="72ff6-144">Only applicable when recursive Acl remove is done.</span></span>

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

### <span data-ttu-id="72ff6-145">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="72ff6-145">-Confirm</span></span>
<span data-ttu-id="72ff6-146">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="72ff6-146">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="72ff6-147">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="72ff6-147">-WhatIf</span></span>
<span data-ttu-id="72ff6-148">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="72ff6-148">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="72ff6-149">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="72ff6-149">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="72ff6-150">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="72ff6-150">CommonParameters</span></span>
<span data-ttu-id="72ff6-151">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="72ff6-151">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="72ff6-152">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="72ff6-152">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="72ff6-153">Eingaben</span><span class="sxs-lookup"><span data-stu-id="72ff6-153">INPUTS</span></span>

### <span data-ttu-id="72ff6-154">System. String</span><span class="sxs-lookup"><span data-stu-id="72ff6-154">System.String</span></span>

### <span data-ttu-id="72ff6-155">Microsoft. Azure. Commands. DataLakeStore. Models. DataLakeStorePathInstance</span><span class="sxs-lookup"><span data-stu-id="72ff6-155">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStorePathInstance</span></span>

### <span data-ttu-id="72ff6-156">Microsoft. Azure. Commands. DataLakeStore. Models. DataLakeStoreItemAce []</span><span class="sxs-lookup"><span data-stu-id="72ff6-156">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStoreItemAce[]</span></span>

### <span data-ttu-id="72ff6-157">Microsoft. Azure. Commands. DataLakeStore. Models. DataLakeStoreEnums + AceType</span><span class="sxs-lookup"><span data-stu-id="72ff6-157">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStoreEnums+AceType</span></span>

### <span data-ttu-id="72ff6-158">System. GUID</span><span class="sxs-lookup"><span data-stu-id="72ff6-158">System.Guid</span></span>

### <span data-ttu-id="72ff6-159">System. Management. Automation. Switchparameter</span><span class="sxs-lookup"><span data-stu-id="72ff6-159">System.Management.Automation.SwitchParameter</span></span>

### <span data-ttu-id="72ff6-160">System. Int32</span><span class="sxs-lookup"><span data-stu-id="72ff6-160">System.Int32</span></span>

## <span data-ttu-id="72ff6-161">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="72ff6-161">OUTPUTS</span></span>

### <span data-ttu-id="72ff6-162">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="72ff6-162">System.Boolean</span></span>

## <span data-ttu-id="72ff6-163">Notizen</span><span class="sxs-lookup"><span data-stu-id="72ff6-163">NOTES</span></span>

## <span data-ttu-id="72ff6-164">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="72ff6-164">RELATED LINKS</span></span>

[<span data-ttu-id="72ff6-165">Satz-AzureRmDataLakeStoreItemAclEntry</span><span class="sxs-lookup"><span data-stu-id="72ff6-165">Set-AzureRmDataLakeStoreItemAclEntry</span></span>](./Set-AzureRmDataLakeStoreItemAclEntry.md)


