---
external help file: Microsoft.Azure.Commands.DataLakeStore.dll-Help.xml
Module Name: AzureRM.DataLakeStore
ms.assetid: 33E7607E-C2BC-4F46-9038-91AC92041F00
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datalakestore/remove-azurermdatalakestoreitemaclentry
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Remove-AzureRmDataLakeStoreItemAclEntry.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Remove-AzureRmDataLakeStoreItemAclEntry.md
ms.openlocfilehash: 41c1324c3762d0b6e04c0c532976c62c0a16067e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93476797"
---
# <span data-ttu-id="b1660-101">Remove-AzureRmDataLakeStoreItemAclEntry</span><span class="sxs-lookup"><span data-stu-id="b1660-101">Remove-AzureRmDataLakeStoreItemAclEntry</span></span>

## <span data-ttu-id="b1660-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="b1660-102">SYNOPSIS</span></span>
<span data-ttu-id="b1660-103">Entfernt einen Eintrag aus der ACL einer Datei oder eines Ordners im Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="b1660-103">Removes an entry from the ACL of a file or folder in Data Lake Store.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b1660-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="b1660-104">SYNTAX</span></span>

### <span data-ttu-id="b1660-105">RemoveByACLObject (Standard)</span><span class="sxs-lookup"><span data-stu-id="b1660-105">RemoveByACLObject (Default)</span></span>
```
Remove-AzureRmDataLakeStoreItemAclEntry [-Account] <String> [-Path] <DataLakeStorePathInstance>
 [-Acl] <DataLakeStoreItemAce[]> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="b1660-106">RemoveSpecificACE</span><span class="sxs-lookup"><span data-stu-id="b1660-106">RemoveSpecificACE</span></span>
```
Remove-AzureRmDataLakeStoreItemAclEntry [-Account] <String> [-Path] <DataLakeStorePathInstance>
 [-AceType] <AceType> [[-Id] <Guid>] [-Default] [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b1660-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="b1660-107">DESCRIPTION</span></span>
<span data-ttu-id="b1660-108">Das Cmdlet **Remove-AzureRmDataLakeStoreItemAclEntry** entfernt einen Eintrag (ACE) aus der Zugriffssteuerungsliste (ACL) einer Datei oder eines Ordners im Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="b1660-108">The **Remove-AzureRmDataLakeStoreItemAclEntry** cmdlet removes an entry (ACE) from the access control list (ACL) of a file or folder in Data Lake Store.</span></span>

## <span data-ttu-id="b1660-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="b1660-109">EXAMPLES</span></span>

### <span data-ttu-id="b1660-110">Beispiel 1: Entfernen eines Benutzereintrags</span><span class="sxs-lookup"><span data-stu-id="b1660-110">Example 1: Remove a user entry</span></span>
```
PS C:\>Remove-AzureRmDataLakeStoreItemAclEntry -AccountName "ContosoADL" -Path / -AceType User -Id (Get-AzureRmADUser -Mail "PattiFuller@contoso.com").ObjectId
```

<span data-ttu-id="b1660-111">Dieser Befehl entfernt das Benutzer-Ass für Patti Fuller aus dem ContosoADL-Konto.</span><span class="sxs-lookup"><span data-stu-id="b1660-111">This command removes the user ACE for Patti Fuller from the ContosoADL account.</span></span>

## <span data-ttu-id="b1660-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="b1660-112">PARAMETERS</span></span>

### <span data-ttu-id="b1660-113">-Konto</span><span class="sxs-lookup"><span data-stu-id="b1660-113">-Account</span></span>
<span data-ttu-id="b1660-114">Gibt den Namen des Data Lake Store-Kontos an.</span><span class="sxs-lookup"><span data-stu-id="b1660-114">Specifies the name of the Data Lake Store account.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: AccountName

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b1660-115">-AceType</span><span class="sxs-lookup"><span data-stu-id="b1660-115">-AceType</span></span>
<span data-ttu-id="b1660-116">Gibt den Typ des zu entfernenden ACE an.</span><span class="sxs-lookup"><span data-stu-id="b1660-116">Specifies the type of ACE to remove.</span></span>
<span data-ttu-id="b1660-117">Die zulässigen Werte für diesen Parameter lauten wie folgt:</span><span class="sxs-lookup"><span data-stu-id="b1660-117">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="b1660-118">Benutzer</span><span class="sxs-lookup"><span data-stu-id="b1660-118">User</span></span>
- <span data-ttu-id="b1660-119">Gruppe</span><span class="sxs-lookup"><span data-stu-id="b1660-119">Group</span></span>
- <span data-ttu-id="b1660-120">Format</span><span class="sxs-lookup"><span data-stu-id="b1660-120">Mask</span></span>
- <span data-ttu-id="b1660-121">Anderen</span><span class="sxs-lookup"><span data-stu-id="b1660-121">Other</span></span>

```yaml
Type: AceType
Parameter Sets: RemoveSpecificACE
Aliases: 
Accepted values: User, Group, Mask, Other

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b1660-122">-ACL</span><span class="sxs-lookup"><span data-stu-id="b1660-122">-Acl</span></span>
<span data-ttu-id="b1660-123">Gibt das ACL-Objekt an, das die zu entfernende Einträge enthält.</span><span class="sxs-lookup"><span data-stu-id="b1660-123">Specifies the ACL object that contains the entries to be removed.</span></span>

```yaml
Type: DataLakeStoreItemAce[]
Parameter Sets: RemoveByACLObject
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b1660-124">– Standard</span><span class="sxs-lookup"><span data-stu-id="b1660-124">-Default</span></span>
<span data-ttu-id="b1660-125">Gibt an, dass dieser Vorgang das Standard-Ass aus der angegebenen ACL entfernt.</span><span class="sxs-lookup"><span data-stu-id="b1660-125">Indicates that this operation removes the default ACE from the specified ACL.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: RemoveSpecificACE
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b1660-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b1660-126">-DefaultProfile</span></span>
<span data-ttu-id="b1660-127">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="b1660-127">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b1660-128">-ID</span><span class="sxs-lookup"><span data-stu-id="b1660-128">-Id</span></span>
<span data-ttu-id="b1660-129">Gibt die Objekt-ID des AzureActive-Verzeichnis Benutzers, der Gruppe oder des Dienst Prinzipals an, für den ein ACE entfernt werden soll.</span><span class="sxs-lookup"><span data-stu-id="b1660-129">Specifies the object ID of the AzureActive Directory user, group, or service principal for which to remove an ACE.</span></span>

```yaml
Type: Guid
Parameter Sets: RemoveSpecificACE
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b1660-130">-PassThru</span><span class="sxs-lookup"><span data-stu-id="b1660-130">-PassThru</span></span>
<span data-ttu-id="b1660-131">Gibt an, dass eine boolesche Antwort zurückgegeben werden soll, die das Ergebnis des Löschvorgangs angibt.</span><span class="sxs-lookup"><span data-stu-id="b1660-131">Indicates a boolean response should be returned indicating the result of the delete operation.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b1660-132">-Path</span><span class="sxs-lookup"><span data-stu-id="b1660-132">-Path</span></span>
<span data-ttu-id="b1660-133">Gibt den Daten See-Speicherpfad des Elements an, aus dem ein ACE entfernt werden soll, beginnend mit dem Stammverzeichnis (/).</span><span class="sxs-lookup"><span data-stu-id="b1660-133">Specifies the Data Lake Store path of the item from which to remove an ACE, starting with the root directory (/).</span></span>

```yaml
Type: DataLakeStorePathInstance
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b1660-134">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="b1660-134">-Confirm</span></span>
<span data-ttu-id="b1660-135">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="b1660-135">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b1660-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b1660-136">-WhatIf</span></span>
<span data-ttu-id="b1660-137">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="b1660-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b1660-138">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="b1660-138">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b1660-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b1660-139">CommonParameters</span></span>
<span data-ttu-id="b1660-140">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b1660-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b1660-141">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b1660-141">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b1660-142">Eingaben</span><span class="sxs-lookup"><span data-stu-id="b1660-142">INPUTS</span></span>

### <span data-ttu-id="b1660-143">DataLakeStoreItemAce[]</span><span class="sxs-lookup"><span data-stu-id="b1660-143">DataLakeStoreItemAce[]</span></span>
<span data-ttu-id="b1660-144">Der Parameter "ACL" akzeptiert den Wert vom Typ "DataLakeStoreItemAce []" aus der Pipeline.</span><span class="sxs-lookup"><span data-stu-id="b1660-144">Parameter 'Acl' accepts value of type 'DataLakeStoreItemAce[]' from the pipeline</span></span>

## <span data-ttu-id="b1660-145">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="b1660-145">OUTPUTS</span></span>

### <span data-ttu-id="b1660-146">bool</span><span class="sxs-lookup"><span data-stu-id="b1660-146">bool</span></span>
<span data-ttu-id="b1660-147">Wenn passthru angegeben ist, wird nach dem erfolgreichen Abschluss "true" zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="b1660-147">If PassThru is specified, returns true upon successful completion.</span></span>

## <span data-ttu-id="b1660-148">Notizen</span><span class="sxs-lookup"><span data-stu-id="b1660-148">NOTES</span></span>

## <span data-ttu-id="b1660-149">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="b1660-149">RELATED LINKS</span></span>

[<span data-ttu-id="b1660-150">Satz-AzureRmDataLakeStoreItemAclEntry</span><span class="sxs-lookup"><span data-stu-id="b1660-150">Set-AzureRmDataLakeStoreItemAclEntry</span></span>](./Set-AzureRmDataLakeStoreItemAclEntry.md)


