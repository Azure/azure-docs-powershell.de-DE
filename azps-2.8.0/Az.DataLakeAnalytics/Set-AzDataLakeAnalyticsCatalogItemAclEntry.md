---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeAnalytics.dll-Help.xml
Module Name: Az.DataLakeAnalytics
online version: https://docs.microsoft.com/en-us/powershell/module/az.datalakeanalytics/set-azdatalakeanalyticscatalogitemaclentry
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeAnalytics/DataLakeAnalytics/help/Set-AzDataLakeAnalyticsCatalogItemAclEntry.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeAnalytics/DataLakeAnalytics/help/Set-AzDataLakeAnalyticsCatalogItemAclEntry.md
ms.openlocfilehash: 4187addb4a256e3304ea5fc8a7bdfb19ed71ac46
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93651593"
---
# <span data-ttu-id="0ee24-101">Set-AzDataLakeAnalyticsCatalogItemAclEntry</span><span class="sxs-lookup"><span data-stu-id="0ee24-101">Set-AzDataLakeAnalyticsCatalogItemAclEntry</span></span>

## <span data-ttu-id="0ee24-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="0ee24-102">SYNOPSIS</span></span>
<span data-ttu-id="0ee24-103">Ändert einen Eintrag in der ACL eines Katalog-oder Katalogelements in Data Lake Analytics.</span><span class="sxs-lookup"><span data-stu-id="0ee24-103">Modifies an entry in the ACL of a catalog or catalog item in Data Lake Analytics.</span></span>

## <span data-ttu-id="0ee24-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="0ee24-104">SYNTAX</span></span>

### <span data-ttu-id="0ee24-105">SetCatalogAclEntryForUser (Standard)</span><span class="sxs-lookup"><span data-stu-id="0ee24-105">SetCatalogAclEntryForUser (Default)</span></span>
```
Set-AzDataLakeAnalyticsCatalogItemAclEntry [-Account] <String> [-User] -ObjectId <Guid>
 -Permissions <PermissionType> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="0ee24-106">SetCatalogItemAclEntryForUser</span><span class="sxs-lookup"><span data-stu-id="0ee24-106">SetCatalogItemAclEntryForUser</span></span>
```
Set-AzDataLakeAnalyticsCatalogItemAclEntry [-Account] <String> [-User] -ObjectId <Guid> -ItemType <String>
 -Path <CatalogPathInstance> -Permissions <PermissionType> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0ee24-107">SetCatalogAclEntryForGroup</span><span class="sxs-lookup"><span data-stu-id="0ee24-107">SetCatalogAclEntryForGroup</span></span>
```
Set-AzDataLakeAnalyticsCatalogItemAclEntry [-Account] <String> [-Group] -ObjectId <Guid>
 -Permissions <PermissionType> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="0ee24-108">SetCatalogItemAclEntryForGroup</span><span class="sxs-lookup"><span data-stu-id="0ee24-108">SetCatalogItemAclEntryForGroup</span></span>
```
Set-AzDataLakeAnalyticsCatalogItemAclEntry [-Account] <String> [-Group] -ObjectId <Guid> -ItemType <String>
 -Path <CatalogPathInstance> -Permissions <PermissionType> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0ee24-109">SetCatalogAclEntryForOther</span><span class="sxs-lookup"><span data-stu-id="0ee24-109">SetCatalogAclEntryForOther</span></span>
```
Set-AzDataLakeAnalyticsCatalogItemAclEntry [-Account] <String> [-Other] -Permissions <PermissionType>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0ee24-110">SetCatalogItemAclEntryForOther</span><span class="sxs-lookup"><span data-stu-id="0ee24-110">SetCatalogItemAclEntryForOther</span></span>
```
Set-AzDataLakeAnalyticsCatalogItemAclEntry [-Account] <String> [-Other] -ItemType <String>
 -Path <CatalogPathInstance> -Permissions <PermissionType> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0ee24-111">SetCatalogAclEntryForUserOwner</span><span class="sxs-lookup"><span data-stu-id="0ee24-111">SetCatalogAclEntryForUserOwner</span></span>
```
Set-AzDataLakeAnalyticsCatalogItemAclEntry [-Account] <String> [-UserOwner] -Permissions <PermissionType>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0ee24-112">SetCatalogItemAclEntryForUserOwner</span><span class="sxs-lookup"><span data-stu-id="0ee24-112">SetCatalogItemAclEntryForUserOwner</span></span>
```
Set-AzDataLakeAnalyticsCatalogItemAclEntry [-Account] <String> [-UserOwner] -ItemType <String>
 -Path <CatalogPathInstance> -Permissions <PermissionType> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0ee24-113">SetCatalogAclEntryForGroupOwner</span><span class="sxs-lookup"><span data-stu-id="0ee24-113">SetCatalogAclEntryForGroupOwner</span></span>
```
Set-AzDataLakeAnalyticsCatalogItemAclEntry [-Account] <String> [-GroupOwner] -Permissions <PermissionType>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0ee24-114">SetCatalogItemAclEntryForGroupOwner</span><span class="sxs-lookup"><span data-stu-id="0ee24-114">SetCatalogItemAclEntryForGroupOwner</span></span>
```
Set-AzDataLakeAnalyticsCatalogItemAclEntry [-Account] <String> [-GroupOwner] -ItemType <String>
 -Path <CatalogPathInstance> -Permissions <PermissionType> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0ee24-115">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="0ee24-115">DESCRIPTION</span></span>
<span data-ttu-id="0ee24-116">Das Cmdlet " **festlegen-AzDataLakeAnalyticsCatalogItemAclEntry** " fügt einen Eintrag (ACE) in der Zugriffssteuerungsliste (ACL) eines Katalog-oder Katalogelements in Data Lake Analytics hinzu oder ändert ihn.</span><span class="sxs-lookup"><span data-stu-id="0ee24-116">The **Set-AzDataLakeAnalyticsCatalogItemAclEntry** cmdlet adds or modifies an entry (ACE) in the access control list (ACL) of a catalog or catalog item in Data Lake Analytics.</span></span>

## <span data-ttu-id="0ee24-117">Beispiele</span><span class="sxs-lookup"><span data-stu-id="0ee24-117">EXAMPLES</span></span>

### <span data-ttu-id="0ee24-118">Beispiel 1: Ändern von Benutzerberechtigungen für einen Katalog</span><span class="sxs-lookup"><span data-stu-id="0ee24-118">Example 1: Modify user permissions for a catalog</span></span>
```powershell
PS C:\> Set-AzDataLakeAnalyticsCatalogItemAclEntry -Account "contosoadla" -User -ObjectId (Get-AzADUser -Mail "PattiFuller@contoso.com").Id -Permissions Read

Type  Id                                   Permissions
----  --                                   -----------
User  90a6f74b-fd73-490e-900a-c4f0f9694d02        Read
Group 902b155a-5601-4ca8-8178-ad3289211f88   ReadWrite
Other 00000000-0000-0000-0000-000000000000        None
User  bd0b55bb-3a57-442a-b2f6-78c95c10ef86        Read
```

<span data-ttu-id="0ee24-119">Mit diesem Befehl wird der Katalog-ACE für Patti Fuller so geändert, dass Sie über Leseberechtigungen verfügt.</span><span class="sxs-lookup"><span data-stu-id="0ee24-119">This command modifies the catalog ACE for Patti Fuller to have read permissions.</span></span>

### <span data-ttu-id="0ee24-120">Beispiel 2: Ändern von Benutzerberechtigungen für eine Datenbank</span><span class="sxs-lookup"><span data-stu-id="0ee24-120">Example 2: Modify user Permissions for a database</span></span>
```powershell
PS C:\> Set-AzDataLakeAnalyticsCatalogItemAclEntry -Account "contosoadla" -User -ObjectId (Get-AzADUser -Mail "PattiFuller@contoso.com").Id -ItemType Database -Path "databaseName" -Permissions Read

Type  Id                                   Permissions
----  --                                   -----------
User  90a6f74b-fd73-490e-900a-c4f0f9694d02        Read
Group 902b155a-5601-4ca8-8178-ad3289211f88   ReadWrite
Other 00000000-0000-0000-0000-000000000000        None
User  bd0b55bb-3a57-442a-b2f6-78c95c10ef86        Read
```

<span data-ttu-id="0ee24-121">Mit diesem Befehl wird der Datenbank-ACE für Patti Fuller so geändert, dass Sie über Leseberechtigungen verfügt.</span><span class="sxs-lookup"><span data-stu-id="0ee24-121">This command modifies the database ACE for Patti Fuller to have read permissions.</span></span>

### <span data-ttu-id="0ee24-122">Beispiel 3: Ändern anderer Berechtigungen für einen Katalog</span><span class="sxs-lookup"><span data-stu-id="0ee24-122">Example 3: Modify other permissions for a catalog</span></span>
```powershell
PS C:\> Set-AzDataLakeAnalyticsCatalogItemAclEntry -Account "contosoadla" -Other -Permissions Read

Type  Id                                   Permissions
----  --                                   -----------
User  90a6f74b-fd73-490e-900a-c4f0f9694d02        Read
Group 902b155a-5601-4ca8-8178-ad3289211f88   ReadWrite
Other 00000000-0000-0000-0000-000000000000        Read
User  bd0b55bb-3a57-442a-b2f6-78c95c10ef86        Read
```

<span data-ttu-id="0ee24-123">Mit diesem Befehl wird der Katalog-ACE für other geändert, um über Leseberechtigungen zu verfügen.</span><span class="sxs-lookup"><span data-stu-id="0ee24-123">This command modifies the catalog ACE for other to have read permissions.</span></span>

### <span data-ttu-id="0ee24-124">Beispiel 4: Ändern anderer Berechtigungen für eine Datenbank</span><span class="sxs-lookup"><span data-stu-id="0ee24-124">Example 4: Modify other Permissions for a database</span></span>
```powershell
PS C:\> Set-AzDataLakeAnalyticsCatalogItemAclEntry -Account "contosoadla" -Other -ItemType Database -Path "databaseName" -Permissions Read

Type  Id                                   Permissions
----  --                                   -----------
User  90a6f74b-fd73-490e-900a-c4f0f9694d02        Read
Group 902b155a-5601-4ca8-8178-ad3289211f88   ReadWrite
Other 00000000-0000-0000-0000-000000000000        Read
User  bd0b55bb-3a57-442a-b2f6-78c95c10ef86        Read
```

### <span data-ttu-id="0ee24-125">Beispiel 5: Ändern der Benutzer Besitzer Berechtigungen für einen Katalog</span><span class="sxs-lookup"><span data-stu-id="0ee24-125">Example 5: Modify user owner permissions for a catalog</span></span>
```powershell
PS C:\> Set-AzDataLakeAnalyticsCatalogItemAclEntry -Account "contosoadla" -UserOwner -Permissions Read

Type      Id                                   Permissions
----      --                                   -----------
UserOwner 0316ac75-6703-4ace-984f-a4dd79aeeafc        Read
```

<span data-ttu-id="0ee24-126">Dieser Befehl legt die Berechtigung "Besitzer" für das zu lesende Konto fest.</span><span class="sxs-lookup"><span data-stu-id="0ee24-126">This command sets the owner permission for the account to Read.</span></span>

### <span data-ttu-id="0ee24-127">Beispiel 6: Ändern der Benutzer Besitzer Berechtigungen für eine Datenbank</span><span class="sxs-lookup"><span data-stu-id="0ee24-127">Example 6: Modify user owner Permissions for a database</span></span>
```powershell
PS C:\> Set-AzDataLakeAnalyticsCatalogItemAclEntry -Account "contosoadla" -UserOwner -ItemType Database -Path "databaseName" -Permissions Read

Type       Id                                   Permissions
----       --                                   -----------
GroupOwner 0316ac75-6703-4ace-984f-a4dd79aeeafc        Read
```

<span data-ttu-id="0ee24-128">Dieser Befehl legt die Berechtigung "Besitzer" für die zu lesende Datenbank fest.</span><span class="sxs-lookup"><span data-stu-id="0ee24-128">This command sets the owner permission for the database to Read.</span></span>

## <span data-ttu-id="0ee24-129">Parameter</span><span class="sxs-lookup"><span data-stu-id="0ee24-129">PARAMETERS</span></span>

### <span data-ttu-id="0ee24-130">-Konto</span><span class="sxs-lookup"><span data-stu-id="0ee24-130">-Account</span></span>
<span data-ttu-id="0ee24-131">Gibt den Namen des Daten Lake Analytics-Kontos an.</span><span class="sxs-lookup"><span data-stu-id="0ee24-131">Specifies the Data Lake Analytics account name.</span></span>

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

### <span data-ttu-id="0ee24-132">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0ee24-132">-DefaultProfile</span></span>
<span data-ttu-id="0ee24-133">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="0ee24-133">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0ee24-134">-Gruppe</span><span class="sxs-lookup"><span data-stu-id="0ee24-134">-Group</span></span>
<span data-ttu-id="0ee24-135">Festlegen des ACL-Eintrags für den Katalog für Gruppe.</span><span class="sxs-lookup"><span data-stu-id="0ee24-135">Set ACL entry of catalog for group.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: SetCatalogAclEntryForGroup, SetCatalogItemAclEntryForGroup
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0ee24-136">-GroupOwner</span><span class="sxs-lookup"><span data-stu-id="0ee24-136">-GroupOwner</span></span>
<span data-ttu-id="0ee24-137">Festlegen des ACL-Eintrags für den Katalog für den Gruppenbesitzer</span><span class="sxs-lookup"><span data-stu-id="0ee24-137">Set ACL entry of catalog for group owner.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: SetCatalogAclEntryForGroupOwner, SetCatalogItemAclEntryForGroupOwner
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0ee24-138">-ItemType</span><span class="sxs-lookup"><span data-stu-id="0ee24-138">-ItemType</span></span>
<span data-ttu-id="0ee24-139">Gibt den Typ des Katalogs oder des Katalogelements an.</span><span class="sxs-lookup"><span data-stu-id="0ee24-139">Specifies the type of the catalog or catalog item(s).</span></span> <span data-ttu-id="0ee24-140">Die zulässigen Werte für diesen Parameter lauten wie folgt:</span><span class="sxs-lookup"><span data-stu-id="0ee24-140">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="0ee24-141">Katalog</span><span class="sxs-lookup"><span data-stu-id="0ee24-141">Catalog</span></span>
- <span data-ttu-id="0ee24-142">Datenbank</span><span class="sxs-lookup"><span data-stu-id="0ee24-142">Database</span></span>

```yaml
Type: System.String
Parameter Sets: SetCatalogItemAclEntryForUser, SetCatalogItemAclEntryForGroup, SetCatalogItemAclEntryForOther, SetCatalogItemAclEntryForUserOwner, SetCatalogItemAclEntryForGroupOwner
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0ee24-143">-ObjectID</span><span class="sxs-lookup"><span data-stu-id="0ee24-143">-ObjectId</span></span>
<span data-ttu-id="0ee24-144">Die Identität des Benutzers, der gesetzt werden soll.</span><span class="sxs-lookup"><span data-stu-id="0ee24-144">The identity of the user to set.</span></span>

```yaml
Type: System.Guid
Parameter Sets: SetCatalogAclEntryForUser, SetCatalogItemAclEntryForUser, SetCatalogAclEntryForGroup, SetCatalogItemAclEntryForGroup
Aliases: Id, UserId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0ee24-145">-Sonstige</span><span class="sxs-lookup"><span data-stu-id="0ee24-145">-Other</span></span>
<span data-ttu-id="0ee24-146">Festlegen des ACL-Eintrags für Catalog für andere.</span><span class="sxs-lookup"><span data-stu-id="0ee24-146">Set ACL entry of catalog for other.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: SetCatalogAclEntryForOther, SetCatalogItemAclEntryForOther
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0ee24-147">-Path</span><span class="sxs-lookup"><span data-stu-id="0ee24-147">-Path</span></span>
<span data-ttu-id="0ee24-148">Gibt den Daten See-Analysepfad eines Katalog-oder Katalogelements an.</span><span class="sxs-lookup"><span data-stu-id="0ee24-148">Specifies the Data Lake Analytics path of an catalog or catalog item.</span></span>
<span data-ttu-id="0ee24-149">Die Teile des Pfads sollten durch einen Punkt (.) getrennt werden.</span><span class="sxs-lookup"><span data-stu-id="0ee24-149">The parts of the path should be separated by a period (.).</span></span>

```yaml
Type: Microsoft.Azure.Commands.DataLakeAnalytics.Models.CatalogPathInstance
Parameter Sets: SetCatalogItemAclEntryForUser, SetCatalogItemAclEntryForGroup, SetCatalogItemAclEntryForOther, SetCatalogItemAclEntryForUserOwner, SetCatalogItemAclEntryForGroupOwner
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0ee24-150">-Berechtigungen</span><span class="sxs-lookup"><span data-stu-id="0ee24-150">-Permissions</span></span>
<span data-ttu-id="0ee24-151">Gibt die Berechtigungen für das ACE an.</span><span class="sxs-lookup"><span data-stu-id="0ee24-151">Specifies the permissions for the ACE.</span></span>
<span data-ttu-id="0ee24-152">Die zulässigen Werte für diesen Parameter lauten wie folgt:</span><span class="sxs-lookup"><span data-stu-id="0ee24-152">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="0ee24-153">Keine</span><span class="sxs-lookup"><span data-stu-id="0ee24-153">None</span></span>
- <span data-ttu-id="0ee24-154">Lesen</span><span class="sxs-lookup"><span data-stu-id="0ee24-154">Read</span></span>
- <span data-ttu-id="0ee24-155">ReadWrite</span><span class="sxs-lookup"><span data-stu-id="0ee24-155">ReadWrite</span></span>

```yaml
Type: Microsoft.Azure.Commands.DataLakeAnalytics.Models.DataLakeAnalyticsEnums+PermissionType
Parameter Sets: (All)
Aliases:
Accepted values: None, Read, ReadWrite

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0ee24-156">-User</span><span class="sxs-lookup"><span data-stu-id="0ee24-156">-User</span></span>
<span data-ttu-id="0ee24-157">ACL-Eintrag für Catalog für Benutzer festlegen</span><span class="sxs-lookup"><span data-stu-id="0ee24-157">Set ACL entry of catalog for user.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: SetCatalogAclEntryForUser, SetCatalogItemAclEntryForUser
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0ee24-158">-UserOwner</span><span class="sxs-lookup"><span data-stu-id="0ee24-158">-UserOwner</span></span>
<span data-ttu-id="0ee24-159">Festlegen des ACL-Eintrags für Catalog für Benutzer Besitzer</span><span class="sxs-lookup"><span data-stu-id="0ee24-159">Set ACL entry of catalog for user owner.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: SetCatalogAclEntryForUserOwner, SetCatalogItemAclEntryForUserOwner
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0ee24-160">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="0ee24-160">-Confirm</span></span>
<span data-ttu-id="0ee24-161">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="0ee24-161">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0ee24-162">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0ee24-162">-WhatIf</span></span>
<span data-ttu-id="0ee24-163">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="0ee24-163">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0ee24-164">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="0ee24-164">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0ee24-165">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0ee24-165">CommonParameters</span></span>
<span data-ttu-id="0ee24-166">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0ee24-166">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0ee24-167">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0ee24-167">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0ee24-168">Eingaben</span><span class="sxs-lookup"><span data-stu-id="0ee24-168">INPUTS</span></span>

### <span data-ttu-id="0ee24-169">System. String</span><span class="sxs-lookup"><span data-stu-id="0ee24-169">System.String</span></span>

### <span data-ttu-id="0ee24-170">System. GUID</span><span class="sxs-lookup"><span data-stu-id="0ee24-170">System.Guid</span></span>

### <span data-ttu-id="0ee24-171">Microsoft. Azure. Commands. DataLakeAnalytics. Models. CatalogPathInstance</span><span class="sxs-lookup"><span data-stu-id="0ee24-171">Microsoft.Azure.Commands.DataLakeAnalytics.Models.CatalogPathInstance</span></span>

### <span data-ttu-id="0ee24-172">Microsoft. Azure. Commands. DataLakeAnalytics. Models. DataLakeAnalyticsEnums + PermissionType</span><span class="sxs-lookup"><span data-stu-id="0ee24-172">Microsoft.Azure.Commands.DataLakeAnalytics.Models.DataLakeAnalyticsEnums+PermissionType</span></span>

## <span data-ttu-id="0ee24-173">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="0ee24-173">OUTPUTS</span></span>

### <span data-ttu-id="0ee24-174">Microsoft.Azure.Commands.DataLakeAnalytics.Models.PSDataLakeAnalyticsAcl</span><span class="sxs-lookup"><span data-stu-id="0ee24-174">Microsoft.Azure.Commands.DataLakeAnalytics.Models.PSDataLakeAnalyticsAcl</span></span>

## <span data-ttu-id="0ee24-175">Notizen</span><span class="sxs-lookup"><span data-stu-id="0ee24-175">NOTES</span></span>

## <span data-ttu-id="0ee24-176">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="0ee24-176">RELATED LINKS</span></span>

[<span data-ttu-id="0ee24-177">Get-AzDataLakeAnalyticsCatalogItemAclEntry</span><span class="sxs-lookup"><span data-stu-id="0ee24-177">Get-AzDataLakeAnalyticsCatalogItemAclEntry</span></span>](Get-AzDataLakeAnalyticsCatalogItemAclEntry.md)

[<span data-ttu-id="0ee24-178">Remove-AzDataLakeAnalyticsCatalogItemAclEntry</span><span class="sxs-lookup"><span data-stu-id="0ee24-178">Remove-AzDataLakeAnalyticsCatalogItemAclEntry</span></span>](Remove-AzDataLakeAnalyticsCatalogItemAclEntry.md)

[<span data-ttu-id="0ee24-179">U-SQL bietet jetzt Zugriffssteuerung auf Datenbankebene</span><span class="sxs-lookup"><span data-stu-id="0ee24-179">U-SQL now offers database level access control</span></span>](https://github.com/Azure/AzureDataLake/blob/master/docs/Release_Notes/2016/2016_08_01/USQL_Release_Notes_2016_08_01.md#u-sql-now-offers-database-level-access-control)
