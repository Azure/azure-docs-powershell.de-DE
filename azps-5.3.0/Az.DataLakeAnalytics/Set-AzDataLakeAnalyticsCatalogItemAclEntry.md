---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeAnalytics.dll-Help.xml
Module Name: Az.DataLakeAnalytics
online version: https://docs.microsoft.com/en-us/powershell/module/az.datalakeanalytics/set-azdatalakeanalyticscatalogitemaclentry
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeAnalytics/DataLakeAnalytics/help/Set-AzDataLakeAnalyticsCatalogItemAclEntry.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeAnalytics/DataLakeAnalytics/help/Set-AzDataLakeAnalyticsCatalogItemAclEntry.md
ms.openlocfilehash: ab02a118eab993174261fc1a70c2dedbd6403d5a
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98472545"
---
# <span data-ttu-id="d3f38-101">Set-AzDataLakeAnalyticsCatalogItemAclEntry</span><span class="sxs-lookup"><span data-stu-id="d3f38-101">Set-AzDataLakeAnalyticsCatalogItemAclEntry</span></span>

## <span data-ttu-id="d3f38-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d3f38-102">SYNOPSIS</span></span>
<span data-ttu-id="d3f38-103">Ändert einen Eintrag in der ACL eines Katalogs oder Katalogelements in Data Lake Analytics.</span><span class="sxs-lookup"><span data-stu-id="d3f38-103">Modifies an entry in the ACL of a catalog or catalog item in Data Lake Analytics.</span></span>

## <span data-ttu-id="d3f38-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="d3f38-104">SYNTAX</span></span>

### <span data-ttu-id="d3f38-105">SetCatalogAclEntryForUser (Standard)</span><span class="sxs-lookup"><span data-stu-id="d3f38-105">SetCatalogAclEntryForUser (Default)</span></span>
```
Set-AzDataLakeAnalyticsCatalogItemAclEntry [-Account] <String> [-User] -ObjectId <Guid>
 -Permissions <PermissionType> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="d3f38-106">SetCatalogItemAclEntryForUser</span><span class="sxs-lookup"><span data-stu-id="d3f38-106">SetCatalogItemAclEntryForUser</span></span>
```
Set-AzDataLakeAnalyticsCatalogItemAclEntry [-Account] <String> [-User] -ObjectId <Guid> -ItemType <String>
 -Path <CatalogPathInstance> -Permissions <PermissionType> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d3f38-107">SetCatalogAclEntryForGroup</span><span class="sxs-lookup"><span data-stu-id="d3f38-107">SetCatalogAclEntryForGroup</span></span>
```
Set-AzDataLakeAnalyticsCatalogItemAclEntry [-Account] <String> [-Group] -ObjectId <Guid>
 -Permissions <PermissionType> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="d3f38-108">SetCatalogItemAclEntryForGroup</span><span class="sxs-lookup"><span data-stu-id="d3f38-108">SetCatalogItemAclEntryForGroup</span></span>
```
Set-AzDataLakeAnalyticsCatalogItemAclEntry [-Account] <String> [-Group] -ObjectId <Guid> -ItemType <String>
 -Path <CatalogPathInstance> -Permissions <PermissionType> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d3f38-109">SetCatalogAclEntryForOther</span><span class="sxs-lookup"><span data-stu-id="d3f38-109">SetCatalogAclEntryForOther</span></span>
```
Set-AzDataLakeAnalyticsCatalogItemAclEntry [-Account] <String> [-Other] -Permissions <PermissionType>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d3f38-110">SetCatalogItemAclEntryForOther</span><span class="sxs-lookup"><span data-stu-id="d3f38-110">SetCatalogItemAclEntryForOther</span></span>
```
Set-AzDataLakeAnalyticsCatalogItemAclEntry [-Account] <String> [-Other] -ItemType <String>
 -Path <CatalogPathInstance> -Permissions <PermissionType> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d3f38-111">SetCatalogAclEntryForUserOwner</span><span class="sxs-lookup"><span data-stu-id="d3f38-111">SetCatalogAclEntryForUserOwner</span></span>
```
Set-AzDataLakeAnalyticsCatalogItemAclEntry [-Account] <String> [-UserOwner] -Permissions <PermissionType>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d3f38-112">SetCatalogItemAclEntryForUserOwner</span><span class="sxs-lookup"><span data-stu-id="d3f38-112">SetCatalogItemAclEntryForUserOwner</span></span>
```
Set-AzDataLakeAnalyticsCatalogItemAclEntry [-Account] <String> [-UserOwner] -ItemType <String>
 -Path <CatalogPathInstance> -Permissions <PermissionType> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d3f38-113">SetCatalogAclEntryForGroupOwner</span><span class="sxs-lookup"><span data-stu-id="d3f38-113">SetCatalogAclEntryForGroupOwner</span></span>
```
Set-AzDataLakeAnalyticsCatalogItemAclEntry [-Account] <String> [-GroupOwner] -Permissions <PermissionType>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d3f38-114">SetCatalogItemAclEntryForGroupOwner</span><span class="sxs-lookup"><span data-stu-id="d3f38-114">SetCatalogItemAclEntryForGroupOwner</span></span>
```
Set-AzDataLakeAnalyticsCatalogItemAclEntry [-Account] <String> [-GroupOwner] -ItemType <String>
 -Path <CatalogPathInstance> -Permissions <PermissionType> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d3f38-115">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="d3f38-115">DESCRIPTION</span></span>
<span data-ttu-id="d3f38-116">Das **Cmdlet "Set-AzDataLakeAnalyticsCatalogItemAclEntry"** fügt in der Zugriffssteuerungsliste (Access Control List, ACL) eines Katalogs oder Katalogelements in Data Lake Analytics einen Eintrag hinzu oder ändert diesen.</span><span class="sxs-lookup"><span data-stu-id="d3f38-116">The **Set-AzDataLakeAnalyticsCatalogItemAclEntry** cmdlet adds or modifies an entry (ACE) in the access control list (ACL) of a catalog or catalog item in Data Lake Analytics.</span></span>

## <span data-ttu-id="d3f38-117">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="d3f38-117">EXAMPLES</span></span>

### <span data-ttu-id="d3f38-118">Beispiel 1: Ändern von Benutzerberechtigungen für einen Katalog</span><span class="sxs-lookup"><span data-stu-id="d3f38-118">Example 1: Modify user permissions for a catalog</span></span>
```powershell
PS C:\> Set-AzDataLakeAnalyticsCatalogItemAclEntry -Account "contosoadla" -User -ObjectId (Get-AzADUser -Mail "PattiFuller@contoso.com").Id -Permissions Read

Type  Id                                   Permissions
----  --                                   -----------
User  90a6f74b-fd73-490e-900a-c4f0f9694d02        Read
Group 902b155a-5601-4ca8-8178-ad3289211f88   ReadWrite
Other 00000000-0000-0000-0000-000000000000        None
User  bd0b55bb-3a57-442a-b2f6-78c95c10ef86        Read
```

<span data-ttu-id="d3f38-119">Dieser Befehl ändert den Katalog-ACE für Deni Fuller, um Leseberechtigungen zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="d3f38-119">This command modifies the catalog ACE for Patti Fuller to have read permissions.</span></span>

### <span data-ttu-id="d3f38-120">Beispiel 2: Ändern von Benutzerberechtigungen für eine Datenbank</span><span class="sxs-lookup"><span data-stu-id="d3f38-120">Example 2: Modify user Permissions for a database</span></span>
```powershell
PS C:\> Set-AzDataLakeAnalyticsCatalogItemAclEntry -Account "contosoadla" -User -ObjectId (Get-AzADUser -Mail "PattiFuller@contoso.com").Id -ItemType Database -Path "databaseName" -Permissions Read

Type  Id                                   Permissions
----  --                                   -----------
User  90a6f74b-fd73-490e-900a-c4f0f9694d02        Read
Group 902b155a-5601-4ca8-8178-ad3289211f88   ReadWrite
Other 00000000-0000-0000-0000-000000000000        None
User  bd0b55bb-3a57-442a-b2f6-78c95c10ef86        Read
```

<span data-ttu-id="d3f38-121">Mit diesem Befehl wird die Datenbank-ACE für Deni Fuller so geändert, dass leseberechtigungen vorhanden sind.</span><span class="sxs-lookup"><span data-stu-id="d3f38-121">This command modifies the database ACE for Patti Fuller to have read permissions.</span></span>

### <span data-ttu-id="d3f38-122">Beispiel 3: Ändern anderer Berechtigungen für einen Katalog</span><span class="sxs-lookup"><span data-stu-id="d3f38-122">Example 3: Modify other permissions for a catalog</span></span>
```powershell
PS C:\> Set-AzDataLakeAnalyticsCatalogItemAclEntry -Account "contosoadla" -Other -Permissions Read

Type  Id                                   Permissions
----  --                                   -----------
User  90a6f74b-fd73-490e-900a-c4f0f9694d02        Read
Group 902b155a-5601-4ca8-8178-ad3289211f88   ReadWrite
Other 00000000-0000-0000-0000-000000000000        Read
User  bd0b55bb-3a57-442a-b2f6-78c95c10ef86        Read
```

<span data-ttu-id="d3f38-123">Dieser Befehl ändert den Katalog-ACE für andere, damit er Leseberechtigungen hat.</span><span class="sxs-lookup"><span data-stu-id="d3f38-123">This command modifies the catalog ACE for other to have read permissions.</span></span>

### <span data-ttu-id="d3f38-124">Beispiel 4: Ändern anderer Berechtigungen für eine Datenbank</span><span class="sxs-lookup"><span data-stu-id="d3f38-124">Example 4: Modify other Permissions for a database</span></span>
```powershell
PS C:\> Set-AzDataLakeAnalyticsCatalogItemAclEntry -Account "contosoadla" -Other -ItemType Database -Path "databaseName" -Permissions Read

Type  Id                                   Permissions
----  --                                   -----------
User  90a6f74b-fd73-490e-900a-c4f0f9694d02        Read
Group 902b155a-5601-4ca8-8178-ad3289211f88   ReadWrite
Other 00000000-0000-0000-0000-000000000000        Read
User  bd0b55bb-3a57-442a-b2f6-78c95c10ef86        Read
```

### <span data-ttu-id="d3f38-125">Beispiel 5: Ändern der Benutzerbesitzerberechtigungen für einen Katalog</span><span class="sxs-lookup"><span data-stu-id="d3f38-125">Example 5: Modify user owner permissions for a catalog</span></span>
```powershell
PS C:\> Set-AzDataLakeAnalyticsCatalogItemAclEntry -Account "contosoadla" -UserOwner -Permissions Read

Type      Id                                   Permissions
----      --                                   -----------
UserOwner 0316ac75-6703-4ace-984f-a4dd79aeeafc        Read
```

<span data-ttu-id="d3f38-126">Dieser Befehl legt die Berechtigung "Besitzer" für das Konto auf "Lesen" fest.</span><span class="sxs-lookup"><span data-stu-id="d3f38-126">This command sets the owner permission for the account to Read.</span></span>

### <span data-ttu-id="d3f38-127">Beispiel 6: Ändern der Benutzerbesitzerberechtigungen für eine Datenbank</span><span class="sxs-lookup"><span data-stu-id="d3f38-127">Example 6: Modify user owner Permissions for a database</span></span>
```powershell
PS C:\> Set-AzDataLakeAnalyticsCatalogItemAclEntry -Account "contosoadla" -UserOwner -ItemType Database -Path "databaseName" -Permissions Read

Type       Id                                   Permissions
----       --                                   -----------
GroupOwner 0316ac75-6703-4ace-984f-a4dd79aeeafc        Read
```

<span data-ttu-id="d3f38-128">Dieser Befehl legt die Berechtigung "Besitzer" für die Datenbank auf "Lesen" fest.</span><span class="sxs-lookup"><span data-stu-id="d3f38-128">This command sets the owner permission for the database to Read.</span></span>

## <span data-ttu-id="d3f38-129">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="d3f38-129">PARAMETERS</span></span>

### <span data-ttu-id="d3f38-130">-Konto</span><span class="sxs-lookup"><span data-stu-id="d3f38-130">-Account</span></span>
<span data-ttu-id="d3f38-131">Gibt den Namen des Data Lake Analytics-Kontos an.</span><span class="sxs-lookup"><span data-stu-id="d3f38-131">Specifies the Data Lake Analytics account name.</span></span>

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

### <span data-ttu-id="d3f38-132">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d3f38-132">-DefaultProfile</span></span>
<span data-ttu-id="d3f38-133">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="d3f38-133">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d3f38-134">-Group</span><span class="sxs-lookup"><span data-stu-id="d3f38-134">-Group</span></span>
<span data-ttu-id="d3f38-135">Festlegen des Eintrags "ACL" des Katalogs für die Gruppe</span><span class="sxs-lookup"><span data-stu-id="d3f38-135">Set ACL entry of catalog for group.</span></span>

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

### <span data-ttu-id="d3f38-136">-GroupOwner</span><span class="sxs-lookup"><span data-stu-id="d3f38-136">-GroupOwner</span></span>
<span data-ttu-id="d3f38-137">Festlegen des Eintrags "ACL" des Katalogs für den Gruppenbesitzer.</span><span class="sxs-lookup"><span data-stu-id="d3f38-137">Set ACL entry of catalog for group owner.</span></span>

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

### <span data-ttu-id="d3f38-138">-ItemType</span><span class="sxs-lookup"><span data-stu-id="d3f38-138">-ItemType</span></span>
<span data-ttu-id="d3f38-139">Gibt den Typ des Katalogs oder Katalogelements an.</span><span class="sxs-lookup"><span data-stu-id="d3f38-139">Specifies the type of the catalog or catalog item(s).</span></span> <span data-ttu-id="d3f38-140">Die zulässigen Werte für diesen Parameter sind:</span><span class="sxs-lookup"><span data-stu-id="d3f38-140">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="d3f38-141">Katalog</span><span class="sxs-lookup"><span data-stu-id="d3f38-141">Catalog</span></span>
- <span data-ttu-id="d3f38-142">Datenbank</span><span class="sxs-lookup"><span data-stu-id="d3f38-142">Database</span></span>

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

### <span data-ttu-id="d3f38-143">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="d3f38-143">-ObjectId</span></span>
<span data-ttu-id="d3f38-144">Die Identität des benutzers, der festgelegt werden soll.</span><span class="sxs-lookup"><span data-stu-id="d3f38-144">The identity of the user to set.</span></span>

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

### <span data-ttu-id="d3f38-145">-Sonstiges</span><span class="sxs-lookup"><span data-stu-id="d3f38-145">-Other</span></span>
<span data-ttu-id="d3f38-146">Festlegen des Eintrags "ACL" des Katalogs für andere</span><span class="sxs-lookup"><span data-stu-id="d3f38-146">Set ACL entry of catalog for other.</span></span>

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

### <span data-ttu-id="d3f38-147">-Path</span><span class="sxs-lookup"><span data-stu-id="d3f38-147">-Path</span></span>
<span data-ttu-id="d3f38-148">Gibt den Data Lake Analytics-Pfad eines Katalogs oder Katalogelements an.</span><span class="sxs-lookup"><span data-stu-id="d3f38-148">Specifies the Data Lake Analytics path of an catalog or catalog item.</span></span>
<span data-ttu-id="d3f38-149">Die Teile des Pfads sollten durch einen Bestimmten (.) getrennt sein.</span><span class="sxs-lookup"><span data-stu-id="d3f38-149">The parts of the path should be separated by a period (.).</span></span>

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

### <span data-ttu-id="d3f38-150">-Permissions</span><span class="sxs-lookup"><span data-stu-id="d3f38-150">-Permissions</span></span>
<span data-ttu-id="d3f38-151">Gibt die Berechtigungen für das ACE an.</span><span class="sxs-lookup"><span data-stu-id="d3f38-151">Specifies the permissions for the ACE.</span></span>
<span data-ttu-id="d3f38-152">Die zulässigen Werte für diesen Parameter sind:</span><span class="sxs-lookup"><span data-stu-id="d3f38-152">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="d3f38-153">Keine</span><span class="sxs-lookup"><span data-stu-id="d3f38-153">None</span></span>
- <span data-ttu-id="d3f38-154">Lesen</span><span class="sxs-lookup"><span data-stu-id="d3f38-154">Read</span></span>
- <span data-ttu-id="d3f38-155">ReadWrite</span><span class="sxs-lookup"><span data-stu-id="d3f38-155">ReadWrite</span></span>

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

### <span data-ttu-id="d3f38-156">-User</span><span class="sxs-lookup"><span data-stu-id="d3f38-156">-User</span></span>
<span data-ttu-id="d3f38-157">Festlegen des Eintrags "ACL" des Katalogs für den Benutzer</span><span class="sxs-lookup"><span data-stu-id="d3f38-157">Set ACL entry of catalog for user.</span></span>

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

### <span data-ttu-id="d3f38-158">-UserOwner</span><span class="sxs-lookup"><span data-stu-id="d3f38-158">-UserOwner</span></span>
<span data-ttu-id="d3f38-159">Legen Sie den Eintrag "ACL" des Katalogs für den Benutzerbesitzer ein.</span><span class="sxs-lookup"><span data-stu-id="d3f38-159">Set ACL entry of catalog for user owner.</span></span>

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

### <span data-ttu-id="d3f38-160">-Confirm</span><span class="sxs-lookup"><span data-stu-id="d3f38-160">-Confirm</span></span>
<span data-ttu-id="d3f38-161">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="d3f38-161">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d3f38-162">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="d3f38-162">-WhatIf</span></span>
<span data-ttu-id="d3f38-163">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="d3f38-163">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d3f38-164">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="d3f38-164">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d3f38-165">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d3f38-165">CommonParameters</span></span>
<span data-ttu-id="d3f38-166">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d3f38-166">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d3f38-167">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d3f38-167">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d3f38-168">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="d3f38-168">INPUTS</span></span>

### <span data-ttu-id="d3f38-169">System.String</span><span class="sxs-lookup"><span data-stu-id="d3f38-169">System.String</span></span>

### <span data-ttu-id="d3f38-170">System.Guid</span><span class="sxs-lookup"><span data-stu-id="d3f38-170">System.Guid</span></span>

### <span data-ttu-id="d3f38-171">Microsoft.Azure.Commands.DataLakeAnalytics.Models.CatalogPathInstance</span><span class="sxs-lookup"><span data-stu-id="d3f38-171">Microsoft.Azure.Commands.DataLakeAnalytics.Models.CatalogPathInstance</span></span>

### <span data-ttu-id="d3f38-172">Microsoft.Azure.Commands.DataLakeAnalytics.Models.DataLakeAnalyticsEnums+PermissionType</span><span class="sxs-lookup"><span data-stu-id="d3f38-172">Microsoft.Azure.Commands.DataLakeAnalytics.Models.DataLakeAnalyticsEnums+PermissionType</span></span>

## <span data-ttu-id="d3f38-173">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="d3f38-173">OUTPUTS</span></span>

### <span data-ttu-id="d3f38-174">Microsoft.Azure.Commands.DataLakeAnalytics.Models.PSDataLakeAnalyticsAcl</span><span class="sxs-lookup"><span data-stu-id="d3f38-174">Microsoft.Azure.Commands.DataLakeAnalytics.Models.PSDataLakeAnalyticsAcl</span></span>

## <span data-ttu-id="d3f38-175">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="d3f38-175">NOTES</span></span>

## <span data-ttu-id="d3f38-176">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="d3f38-176">RELATED LINKS</span></span>

[<span data-ttu-id="d3f38-177">Get-AzDataLakeAnalyticsCatalogItemAclEntry</span><span class="sxs-lookup"><span data-stu-id="d3f38-177">Get-AzDataLakeAnalyticsCatalogItemAclEntry</span></span>](Get-AzDataLakeAnalyticsCatalogItemAclEntry.md)

[<span data-ttu-id="d3f38-178">Remove-AzDataLakeAnalyticsCatalogItemAclEntry</span><span class="sxs-lookup"><span data-stu-id="d3f38-178">Remove-AzDataLakeAnalyticsCatalogItemAclEntry</span></span>](Remove-AzDataLakeAnalyticsCatalogItemAclEntry.md)

[<span data-ttu-id="d3f38-179">U-SQL bietet jetzt Zugriffssteuerung auf Datenbankebene</span><span class="sxs-lookup"><span data-stu-id="d3f38-179">U-SQL now offers database level access control</span></span>](https://github.com/Azure/AzureDataLake/blob/master/docs/Release_Notes/2016/2016_08_01/USQL_Release_Notes_2016_08_01.md#u-sql-now-offers-database-level-access-control)
