---
external help file: Microsoft.Azure.Commands.DataLakeStore.dll-Help.xml
Module Name: AzureRM.DataLakeStore
ms.assetid: 0671D833-8B3A-4480-A576-92F1A9E8CE92
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Set-AzureRmDataLakeStoreItemAclEntry.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Set-AzureRmDataLakeStoreItemAclEntry.md
ms.openlocfilehash: 9646ef98499e56e24ce81c78f6b94dce75ff0078
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93504178"
---
# <span data-ttu-id="b62eb-101">Set-AzureRmDataLakeStoreItemAclEntry</span><span class="sxs-lookup"><span data-stu-id="b62eb-101">Set-AzureRmDataLakeStoreItemAclEntry</span></span>

## <span data-ttu-id="b62eb-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="b62eb-102">SYNOPSIS</span></span>
<span data-ttu-id="b62eb-103">Ändert einen Eintrag in der ACL einer Datei oder eines Ordners im Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="b62eb-103">Modifies an entry in the ACL of a file or folder in Data Lake Store.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b62eb-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="b62eb-104">SYNTAX</span></span>

### <span data-ttu-id="b62eb-105">Festlegen von ACL-Einträgen mit ACL-Objekt (Standard)</span><span class="sxs-lookup"><span data-stu-id="b62eb-105">Set ACL Entries using ACL object (Default)</span></span>
```
Set-AzureRmDataLakeStoreItemAclEntry [-Account] <String> [-Path] <DataLakeStorePathInstance>
 [-Acl] <DataLakeStoreItemAce[]> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="b62eb-106">Spezifisches Ass einstellen</span><span class="sxs-lookup"><span data-stu-id="b62eb-106">Set specific ACE</span></span>
```
Set-AzureRmDataLakeStoreItemAclEntry [-Account] <String> [-Path] <DataLakeStorePathInstance>
 [-AceType] <AceType> [[-Id] <Guid>] [-Permissions] <Permission> [-Default] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b62eb-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="b62eb-107">DESCRIPTION</span></span>
<span data-ttu-id="b62eb-108">Das Cmdlet " **festlegen-AzureRmDataLakeStoreItemAclEntry** " ändert einen Eintrag (ACE) in der Zugriffssteuerungsliste (ACL) einer Datei oder eines Ordners im Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="b62eb-108">The **Set-AzureRmDataLakeStoreItemAclEntry** cmdlet modifies an entry (ACE) in the access control list (ACL) of a file or folder in Data Lake Store.</span></span>

## <span data-ttu-id="b62eb-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="b62eb-109">EXAMPLES</span></span>

### <span data-ttu-id="b62eb-110">Beispiel 1: Ändern von Berechtigungen für einen ACE</span><span class="sxs-lookup"><span data-stu-id="b62eb-110">Example 1: Modify permissions for an ACE</span></span>
```
PS C:\>Set-AzureRmDataLakeStoreItemAclEntry -AccountName "ContosoADL" -Path / -AceType User -Id (Get-AzureRmADUser -Mail "PattiFuller@contoso.com").ObjectId -Permissions All
```

<span data-ttu-id="b62eb-111">Mit diesem Befehl wird das Ass für Patti Fuller so geändert, dass alle Berechtigungen vorhanden sind.</span><span class="sxs-lookup"><span data-stu-id="b62eb-111">This command modifies the ACE for Patti Fuller to have all permissions.</span></span>

## <span data-ttu-id="b62eb-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="b62eb-112">PARAMETERS</span></span>

### <span data-ttu-id="b62eb-113">-Konto</span><span class="sxs-lookup"><span data-stu-id="b62eb-113">-Account</span></span>
<span data-ttu-id="b62eb-114">Gibt den Namen des Data Lake Store-Kontos an.</span><span class="sxs-lookup"><span data-stu-id="b62eb-114">Specifies the name of the Data Lake Store account.</span></span>

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

### <span data-ttu-id="b62eb-115">-AceType</span><span class="sxs-lookup"><span data-stu-id="b62eb-115">-AceType</span></span>
<span data-ttu-id="b62eb-116">Gibt den Typ des zu ändernden ACE an.</span><span class="sxs-lookup"><span data-stu-id="b62eb-116">Specifies the type of ACE to modify.</span></span>
<span data-ttu-id="b62eb-117">Die zulässigen Werte für diesen Parameter lauten wie folgt:</span><span class="sxs-lookup"><span data-stu-id="b62eb-117">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="b62eb-118">Benutzer</span><span class="sxs-lookup"><span data-stu-id="b62eb-118">User</span></span> 
- <span data-ttu-id="b62eb-119">Gruppe</span><span class="sxs-lookup"><span data-stu-id="b62eb-119">Group</span></span> 
- <span data-ttu-id="b62eb-120">Format</span><span class="sxs-lookup"><span data-stu-id="b62eb-120">Mask</span></span> 
- <span data-ttu-id="b62eb-121">Anderen</span><span class="sxs-lookup"><span data-stu-id="b62eb-121">Other</span></span>

```yaml
Type: Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStoreEnums+AceType
Parameter Sets: Set specific ACE
Aliases: 
Accepted values: User, Group, Mask, Other

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b62eb-122">-ACL</span><span class="sxs-lookup"><span data-stu-id="b62eb-122">-Acl</span></span>
<span data-ttu-id="b62eb-123">Gibt das ACL-Objekt an, das die zu ändernden Einträge enthält.</span><span class="sxs-lookup"><span data-stu-id="b62eb-123">Specifies the ACL object that contains the entries to modify.</span></span>

```yaml
Type: Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStoreItemAce[]
Parameter Sets: Set ACL Entries using ACL object
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b62eb-124">– Standard</span><span class="sxs-lookup"><span data-stu-id="b62eb-124">-Default</span></span>
<span data-ttu-id="b62eb-125">Gibt an, dass dieser Vorgang den Standard-ACE aus der angegebenen ACL ändert.</span><span class="sxs-lookup"><span data-stu-id="b62eb-125">Indicates that this operation modifies the default ACE from the specified ACL.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: Set specific ACE
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b62eb-126">-ID</span><span class="sxs-lookup"><span data-stu-id="b62eb-126">-Id</span></span>
<span data-ttu-id="b62eb-127">Gibt die Objekt-ID des AzureActive-Verzeichnis Benutzers, der Gruppe oder des Dienst Prinzipals an, für den ein ACE geändert werden soll.</span><span class="sxs-lookup"><span data-stu-id="b62eb-127">Specifies the object ID of the AzureActive Directory user, group, or service principal for which to modify an ACE.</span></span>

```yaml
Type: System.Guid
Parameter Sets: Set specific ACE
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b62eb-128">-PassThru</span><span class="sxs-lookup"><span data-stu-id="b62eb-128">-PassThru</span></span>
<span data-ttu-id="b62eb-129">Gibt an, dass die resultierende ACL zurückgegeben werden soll.</span><span class="sxs-lookup"><span data-stu-id="b62eb-129">Indicates the resulting ACL should be returned.</span></span>

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

### <span data-ttu-id="b62eb-130">-Path</span><span class="sxs-lookup"><span data-stu-id="b62eb-130">-Path</span></span>
<span data-ttu-id="b62eb-131">Gibt den Daten See-Speicherpfad des Elements an, für das ein ACE geändert werden soll, beginnend mit dem Stammverzeichnis (/).</span><span class="sxs-lookup"><span data-stu-id="b62eb-131">Specifies the Data Lake Store path of the item for which to modify an ACE, starting with the root directory (/).</span></span>

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

### <span data-ttu-id="b62eb-132">-Berechtigungen</span><span class="sxs-lookup"><span data-stu-id="b62eb-132">-Permissions</span></span>
<span data-ttu-id="b62eb-133">Gibt die Berechtigungen für das ACE an.</span><span class="sxs-lookup"><span data-stu-id="b62eb-133">Specifies the permissions for the ACE.</span></span>
<span data-ttu-id="b62eb-134">Die zulässigen Werte für diesen Parameter lauten wie folgt:</span><span class="sxs-lookup"><span data-stu-id="b62eb-134">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="b62eb-135">Keine</span><span class="sxs-lookup"><span data-stu-id="b62eb-135">None</span></span>
- <span data-ttu-id="b62eb-136">Ausführen</span><span class="sxs-lookup"><span data-stu-id="b62eb-136">Execute</span></span>
- <span data-ttu-id="b62eb-137">Schreiben</span><span class="sxs-lookup"><span data-stu-id="b62eb-137">Write</span></span>
- <span data-ttu-id="b62eb-138">WriteExecute</span><span class="sxs-lookup"><span data-stu-id="b62eb-138">WriteExecute</span></span>
- <span data-ttu-id="b62eb-139">Lesen</span><span class="sxs-lookup"><span data-stu-id="b62eb-139">Read</span></span>
- <span data-ttu-id="b62eb-140">ReadExecute</span><span class="sxs-lookup"><span data-stu-id="b62eb-140">ReadExecute</span></span>
- <span data-ttu-id="b62eb-141">ReadWrite</span><span class="sxs-lookup"><span data-stu-id="b62eb-141">ReadWrite</span></span>
- <span data-ttu-id="b62eb-142">Alle</span><span class="sxs-lookup"><span data-stu-id="b62eb-142">All</span></span>

```yaml
Type: Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStoreEnums+Permission
Parameter Sets: Set specific ACE
Aliases: 

Required: True
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b62eb-143">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="b62eb-143">-Confirm</span></span>
<span data-ttu-id="b62eb-144">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="b62eb-144">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b62eb-145">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b62eb-145">-WhatIf</span></span>
<span data-ttu-id="b62eb-146">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="b62eb-146">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b62eb-147">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="b62eb-147">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b62eb-148">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b62eb-148">-DefaultProfile</span></span>
<span data-ttu-id="b62eb-149">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="b62eb-149">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b62eb-150">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b62eb-150">CommonParameters</span></span>
<span data-ttu-id="b62eb-151">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b62eb-151">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b62eb-152">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b62eb-152">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b62eb-153">Eingaben</span><span class="sxs-lookup"><span data-stu-id="b62eb-153">INPUTS</span></span>

### <span data-ttu-id="b62eb-154">DataLakeStoreItemAce[]</span><span class="sxs-lookup"><span data-stu-id="b62eb-154">DataLakeStoreItemAce[]</span></span>
<span data-ttu-id="b62eb-155">Der Parameter "ACL" akzeptiert den Wert vom Typ "DataLakeStoreItemAce []" aus der Pipeline.</span><span class="sxs-lookup"><span data-stu-id="b62eb-155">Parameter 'Acl' accepts value of type 'DataLakeStoreItemAce[]' from the pipeline</span></span>

## <span data-ttu-id="b62eb-156">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="b62eb-156">OUTPUTS</span></span>

### <span data-ttu-id="b62eb-157">IEnumerable<DataLakeStoreItemAce></span><span class="sxs-lookup"><span data-stu-id="b62eb-157">IEnumerable<DataLakeStoreItemAce></span></span>
<span data-ttu-id="b62eb-158">Wenn passthru angegeben wird, gibt die resultierende Liste der ACL-Einträge zurück.</span><span class="sxs-lookup"><span data-stu-id="b62eb-158">If PassThru is specified, will return the resulting list of ACL entries.</span></span>

## <span data-ttu-id="b62eb-159">Notizen</span><span class="sxs-lookup"><span data-stu-id="b62eb-159">NOTES</span></span>

## <span data-ttu-id="b62eb-160">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="b62eb-160">RELATED LINKS</span></span>

[<span data-ttu-id="b62eb-161">Remove-AzureRmDataLakeStoreItemAclEntry</span><span class="sxs-lookup"><span data-stu-id="b62eb-161">Remove-AzureRmDataLakeStoreItemAclEntry</span></span>](./Remove-AzureRmDataLakeStoreItemAclEntry.md)


