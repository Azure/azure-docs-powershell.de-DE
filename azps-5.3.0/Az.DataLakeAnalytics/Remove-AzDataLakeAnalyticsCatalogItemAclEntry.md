---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeAnalytics.dll-Help.xml
Module Name: Az.DataLakeAnalytics
online version: https://docs.microsoft.com/en-us/powershell/module/az.datalakeanalytics/remove-azdatalakeanalyticscatalogitemaclentry
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeAnalytics/DataLakeAnalytics/help/Remove-AzDataLakeAnalyticsCatalogItemAclEntry.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeAnalytics/DataLakeAnalytics/help/Remove-AzDataLakeAnalyticsCatalogItemAclEntry.md
ms.openlocfilehash: 8b227d16a55d1e5f92c6021099a01b9df5550bd2
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98458124"
---
# <span data-ttu-id="89589-101">Remove-AzDataLakeAnalyticsCatalogItemAclEntry</span><span class="sxs-lookup"><span data-stu-id="89589-101">Remove-AzDataLakeAnalyticsCatalogItemAclEntry</span></span>

## <span data-ttu-id="89589-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="89589-102">SYNOPSIS</span></span>
<span data-ttu-id="89589-103">Löscht einen Eintrag aus der ACL eines Katalogs oder Katalogelements in Data Lake Analytics.</span><span class="sxs-lookup"><span data-stu-id="89589-103">Deletes an entry from the ACL of a catalog or catalog item in Data Lake Analytics.</span></span>

## <span data-ttu-id="89589-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="89589-104">SYNTAX</span></span>

### <span data-ttu-id="89589-105">RemoveCatalogAclEntryForUser (Standard)</span><span class="sxs-lookup"><span data-stu-id="89589-105">RemoveCatalogAclEntryForUser (Default)</span></span>
```
Remove-AzDataLakeAnalyticsCatalogItemAclEntry [-Account] <String> [-User] -ObjectId <Guid> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="89589-106">RemoveCatalogItemAclEntryForUser</span><span class="sxs-lookup"><span data-stu-id="89589-106">RemoveCatalogItemAclEntryForUser</span></span>
```
Remove-AzDataLakeAnalyticsCatalogItemAclEntry [-Account] <String> [-User] -ObjectId <Guid> -ItemType <String>
 -Path <CatalogPathInstance> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="89589-107">RemoveCatalogAclEntryForGroup</span><span class="sxs-lookup"><span data-stu-id="89589-107">RemoveCatalogAclEntryForGroup</span></span>
```
Remove-AzDataLakeAnalyticsCatalogItemAclEntry [-Account] <String> [-Group] -ObjectId <Guid> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="89589-108">RemoveCatalogItemAclEntryForGroup</span><span class="sxs-lookup"><span data-stu-id="89589-108">RemoveCatalogItemAclEntryForGroup</span></span>
```
Remove-AzDataLakeAnalyticsCatalogItemAclEntry [-Account] <String> [-Group] -ObjectId <Guid> -ItemType <String>
 -Path <CatalogPathInstance> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="89589-109">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="89589-109">DESCRIPTION</span></span>
<span data-ttu-id="89589-110">Das Cmdlet **"Remove-AzDataLakeAnalyticsCatalogItemAclEntry"** entfernt einen Eintrag (ACE) aus der Zugriffssteuerungsliste (Access Control List, ACL) eines Katalogs oder Katalogelements in Data Lake Analytics.</span><span class="sxs-lookup"><span data-stu-id="89589-110">The **Remove-AzDataLakeAnalyticsCatalogItemAclEntry** cmdlet removes an entry (ACE) from the access control list (ACL) of a catalog or catalog item in Data Lake Analytics.</span></span>

## <span data-ttu-id="89589-111">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="89589-111">EXAMPLES</span></span>

### <span data-ttu-id="89589-112">Beispiel 1: Entfernen der Benutzer-ACL für einen Katalog</span><span class="sxs-lookup"><span data-stu-id="89589-112">Example 1: Remove the user ACL for a catalog</span></span>
```powershell
PS C:\> Remove-AzDataLakeAnalyticsCatalogItemAclEntry -Account "contosoadla" -User -ObjectId (Get-AzADUser -Mail "PattiFuller@contoso.com").Id
```

<span data-ttu-id="89589-113">Mit diesem Befehl wird die Katalog-ACL für Denverdinger des contosoadla-Kontos entfernt.</span><span class="sxs-lookup"><span data-stu-id="89589-113">This command removes the catalog ACL for Patti Fuller of the contosoadla account.</span></span>

### <span data-ttu-id="89589-114">Beispiel 2: Entfernen der Benutzer-ACL für eine Datenbank</span><span class="sxs-lookup"><span data-stu-id="89589-114">Example 2: Remove the user ACL for a database</span></span>
```powershell
PS C:\> Remove-AzDataLakeAnalyticsCatalogItemAclEntry -Account "contosoadla" -User -ObjectId (Get-AzADUser -Mail "PattiFuller@contoso.com").Id -ItemType Database -Path "databaseName"
```

<span data-ttu-id="89589-115">Mit diesem Befehl wird die Datenbank-ACL für Hangi Fuller des contosoadla-Kontos entfernt.</span><span class="sxs-lookup"><span data-stu-id="89589-115">This command removes the database ACL for Patti Fuller of the contosoadla account.</span></span>

## <span data-ttu-id="89589-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="89589-116">PARAMETERS</span></span>

### <span data-ttu-id="89589-117">-Konto</span><span class="sxs-lookup"><span data-stu-id="89589-117">-Account</span></span>
<span data-ttu-id="89589-118">Gibt den Namen des Data Lake Analytics-Kontos an.</span><span class="sxs-lookup"><span data-stu-id="89589-118">Specifies the Data Lake Analytics account name.</span></span>

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

### <span data-ttu-id="89589-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="89589-119">-DefaultProfile</span></span>
<span data-ttu-id="89589-120">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="89589-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="89589-121">-Group</span><span class="sxs-lookup"><span data-stu-id="89589-121">-Group</span></span>
<span data-ttu-id="89589-122">Entfernen sie den Eintrag "ACL" des Katalogs für die Gruppe.</span><span class="sxs-lookup"><span data-stu-id="89589-122">Remove ACL entry of catalog for group.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: RemoveCatalogAclEntryForGroup, RemoveCatalogItemAclEntryForGroup
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="89589-123">-ItemType</span><span class="sxs-lookup"><span data-stu-id="89589-123">-ItemType</span></span>
<span data-ttu-id="89589-124">Gibt den Typ des/der Katalog- oder Katalogelement(en) an.</span><span class="sxs-lookup"><span data-stu-id="89589-124">Specifies the type of the catalog or catalog item(s).</span></span> <span data-ttu-id="89589-125">Die zulässigen Werte für diesen Parameter sind:</span><span class="sxs-lookup"><span data-stu-id="89589-125">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="89589-126">Katalog</span><span class="sxs-lookup"><span data-stu-id="89589-126">Catalog</span></span>
- <span data-ttu-id="89589-127">Datenbank</span><span class="sxs-lookup"><span data-stu-id="89589-127">Database</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveCatalogItemAclEntryForUser, RemoveCatalogItemAclEntryForGroup
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="89589-128">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="89589-128">-ObjectId</span></span>
<span data-ttu-id="89589-129">Die Identität des zu entfernende Benutzers.</span><span class="sxs-lookup"><span data-stu-id="89589-129">The identity of the user to remove.</span></span>

```yaml
Type: System.Guid
Parameter Sets: (All)
Aliases: Id, UserId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="89589-130">-PassThru</span><span class="sxs-lookup"><span data-stu-id="89589-130">-PassThru</span></span>
<span data-ttu-id="89589-131">Gibt an, dass eine boolesche Antwort zurückgegeben werden sollte, die das Ergebnis des Löschvorgangs angibt.</span><span class="sxs-lookup"><span data-stu-id="89589-131">Indicates a boolean response should be returned indicating the result of the delete operation.</span></span>

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

### <span data-ttu-id="89589-132">-Path</span><span class="sxs-lookup"><span data-stu-id="89589-132">-Path</span></span>
<span data-ttu-id="89589-133">Gibt den Data Lake Analytics-Pfad eines Katalogs oder Katalogelements an.</span><span class="sxs-lookup"><span data-stu-id="89589-133">Specifies the Data Lake Analytics path of an catalog or catalog item.</span></span>
<span data-ttu-id="89589-134">Die Teile des Pfads sollten durch einen Bestimmten (.) getrennt sein.</span><span class="sxs-lookup"><span data-stu-id="89589-134">The parts of the path should be separated by a period (.).</span></span>

```yaml
Type: Microsoft.Azure.Commands.DataLakeAnalytics.Models.CatalogPathInstance
Parameter Sets: RemoveCatalogItemAclEntryForUser, RemoveCatalogItemAclEntryForGroup
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="89589-135">-User</span><span class="sxs-lookup"><span data-stu-id="89589-135">-User</span></span>
<span data-ttu-id="89589-136">Entfernen sie den Eintrag "ACL" des Katalogs für den Benutzer.</span><span class="sxs-lookup"><span data-stu-id="89589-136">Remove ACL entry of catalog for user.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: RemoveCatalogAclEntryForUser, RemoveCatalogItemAclEntryForUser
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="89589-137">-Confirm</span><span class="sxs-lookup"><span data-stu-id="89589-137">-Confirm</span></span>
<span data-ttu-id="89589-138">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="89589-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="89589-139">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="89589-139">-WhatIf</span></span>
<span data-ttu-id="89589-140">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="89589-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="89589-141">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="89589-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="89589-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="89589-142">CommonParameters</span></span>
<span data-ttu-id="89589-143">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="89589-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="89589-144">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="89589-144">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="89589-145">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="89589-145">INPUTS</span></span>

### <span data-ttu-id="89589-146">System.String</span><span class="sxs-lookup"><span data-stu-id="89589-146">System.String</span></span>

### <span data-ttu-id="89589-147">System.Guid</span><span class="sxs-lookup"><span data-stu-id="89589-147">System.Guid</span></span>

### <span data-ttu-id="89589-148">Microsoft.Azure.Commands.DataLakeAnalytics.Models.CatalogPathInstance</span><span class="sxs-lookup"><span data-stu-id="89589-148">Microsoft.Azure.Commands.DataLakeAnalytics.Models.CatalogPathInstance</span></span>

## <span data-ttu-id="89589-149">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="89589-149">OUTPUTS</span></span>

### <span data-ttu-id="89589-150">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="89589-150">System.Boolean</span></span>

## <span data-ttu-id="89589-151">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="89589-151">NOTES</span></span>

## <span data-ttu-id="89589-152">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="89589-152">RELATED LINKS</span></span>

[<span data-ttu-id="89589-153">U-SQL bietet jetzt Zugriffssteuerung auf Datenbankebene</span><span class="sxs-lookup"><span data-stu-id="89589-153">U-SQL now offers database level access control</span></span>](https://github.com/Azure/AzureDataLake/blob/master/docs/Release_Notes/2016/2016_08_01/USQL_Release_Notes_2016_08_01.md#u-sql-now-offers-database-level-access-control)

[<span data-ttu-id="89589-154">Get-AzDataLakeAnalyticsCatalogItemAclEntry</span><span class="sxs-lookup"><span data-stu-id="89589-154">Get-AzDataLakeAnalyticsCatalogItemAclEntry</span></span>](Get-AzDataLakeAnalyticsCatalogItemAclEntry.md)

[<span data-ttu-id="89589-155">Set-AzDataLakeAnalyticsCatalogItemAclEntry</span><span class="sxs-lookup"><span data-stu-id="89589-155">Set-AzDataLakeAnalyticsCatalogItemAclEntry</span></span>](Set-AzDataLakeAnalyticsCatalogItemAclEntry.md)
