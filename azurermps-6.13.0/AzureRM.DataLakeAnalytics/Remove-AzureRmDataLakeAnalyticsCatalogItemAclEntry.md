---
external help file: Microsoft.Azure.Commands.DataLakeAnalytics.dll-Help.xml
Module Name: AzureRM.DataLakeAnalytics
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datalakeanalytics/remove-azurermdatalakeanalyticscatalogitemaclentry
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeAnalytics/Commands.DataLakeAnalytics/help/Remove-AzureRmDataLakeAnalyticsCatalogItemAclEntry.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeAnalytics/Commands.DataLakeAnalytics/help/Remove-AzureRmDataLakeAnalyticsCatalogItemAclEntry.md
ms.openlocfilehash: e97876377e8ea96dc106277991bcc05fec5f3759
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93480370"
---
# <span data-ttu-id="b13b6-101">Remove-AzureRmDataLakeAnalyticsCatalogItemAclEntry</span><span class="sxs-lookup"><span data-stu-id="b13b6-101">Remove-AzureRmDataLakeAnalyticsCatalogItemAclEntry</span></span>

## <span data-ttu-id="b13b6-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="b13b6-102">SYNOPSIS</span></span>
<span data-ttu-id="b13b6-103">Löscht einen Eintrag aus der ACL eines Katalog-oder Katalogelements in Data Lake Analytics.</span><span class="sxs-lookup"><span data-stu-id="b13b6-103">Deletes an entry from the ACL of a catalog or catalog item in Data Lake Analytics.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b13b6-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="b13b6-104">SYNTAX</span></span>

### <span data-ttu-id="b13b6-105">RemoveCatalogAclEntryForUser (Standard)</span><span class="sxs-lookup"><span data-stu-id="b13b6-105">RemoveCatalogAclEntryForUser (Default)</span></span>
```
Remove-AzureRmDataLakeAnalyticsCatalogItemAclEntry [-Account] <String> [-User] -ObjectId <Guid> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b13b6-106">RemoveCatalogItemAclEntryForUser</span><span class="sxs-lookup"><span data-stu-id="b13b6-106">RemoveCatalogItemAclEntryForUser</span></span>
```
Remove-AzureRmDataLakeAnalyticsCatalogItemAclEntry [-Account] <String> [-User] -ObjectId <Guid>
 -ItemType <String> -Path <CatalogPathInstance> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b13b6-107">RemoveCatalogAclEntryForGroup</span><span class="sxs-lookup"><span data-stu-id="b13b6-107">RemoveCatalogAclEntryForGroup</span></span>
```
Remove-AzureRmDataLakeAnalyticsCatalogItemAclEntry [-Account] <String> [-Group] -ObjectId <Guid> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b13b6-108">RemoveCatalogItemAclEntryForGroup</span><span class="sxs-lookup"><span data-stu-id="b13b6-108">RemoveCatalogItemAclEntryForGroup</span></span>
```
Remove-AzureRmDataLakeAnalyticsCatalogItemAclEntry [-Account] <String> [-Group] -ObjectId <Guid>
 -ItemType <String> -Path <CatalogPathInstance> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b13b6-109">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="b13b6-109">DESCRIPTION</span></span>
<span data-ttu-id="b13b6-110">Das Cmdlet **Remove-AzureRmDataLakeAnalyticsCatalogItemAclEntry** entfernt einen Eintrag (ACE) aus der Zugriffssteuerungsliste (ACL) eines Katalog-oder Katalogelements in Data Lake Analytics.</span><span class="sxs-lookup"><span data-stu-id="b13b6-110">The **Remove-AzureRmDataLakeAnalyticsCatalogItemAclEntry** cmdlet removes an entry (ACE) from the access control list (ACL) of a catalog or catalog item in Data Lake Analytics.</span></span>

## <span data-ttu-id="b13b6-111">Beispiele</span><span class="sxs-lookup"><span data-stu-id="b13b6-111">EXAMPLES</span></span>

### <span data-ttu-id="b13b6-112">Beispiel 1: Entfernen der Benutzer-ACL für einen Katalog</span><span class="sxs-lookup"><span data-stu-id="b13b6-112">Example 1: Remove the user ACL for a catalog</span></span>
```powershell
PS C:\> Remove-AzureRmDataLakeAnalyticsCatalogItemAclEntry -Account "contosoadla" -User -ObjectId (Get-AzureRmADUser -Mail "PattiFuller@contoso.com").Id
```

<span data-ttu-id="b13b6-113">Dieser Befehl entfernt die Katalog-ACL für Patti Fuller des contosoadla-Kontos.</span><span class="sxs-lookup"><span data-stu-id="b13b6-113">This command removes the catalog ACL for Patti Fuller of the contosoadla account.</span></span>

### <span data-ttu-id="b13b6-114">Beispiel 2: Entfernen der Benutzer-ACL für eine Datenbank</span><span class="sxs-lookup"><span data-stu-id="b13b6-114">Example 2: Remove the user ACL for a database</span></span>
```powershell
PS C:\> Remove-AzureRmDataLakeAnalyticsCatalogItemAclEntry -Account "contosoadla" -User -ObjectId (Get-AzureRmADUser -Mail "PattiFuller@contoso.com").Id -ItemType Database -Path "databaseName"
```

<span data-ttu-id="b13b6-115">Dieser Befehl entfernt die Datenbank-ACL für Patti Fuller des contosoadla-Kontos.</span><span class="sxs-lookup"><span data-stu-id="b13b6-115">This command removes the database ACL for Patti Fuller of the contosoadla account.</span></span>

## <span data-ttu-id="b13b6-116">Parameter</span><span class="sxs-lookup"><span data-stu-id="b13b6-116">PARAMETERS</span></span>

### <span data-ttu-id="b13b6-117">-Konto</span><span class="sxs-lookup"><span data-stu-id="b13b6-117">-Account</span></span>
<span data-ttu-id="b13b6-118">Gibt den Namen des Daten Lake Analytics-Kontos an.</span><span class="sxs-lookup"><span data-stu-id="b13b6-118">Specifies the Data Lake Analytics account name.</span></span>

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

### <span data-ttu-id="b13b6-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b13b6-119">-DefaultProfile</span></span>
<span data-ttu-id="b13b6-120">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="b13b6-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b13b6-121">-Gruppe</span><span class="sxs-lookup"><span data-stu-id="b13b6-121">-Group</span></span>
<span data-ttu-id="b13b6-122">ACL-Eintrag des Katalogs für Gruppe entfernen.</span><span class="sxs-lookup"><span data-stu-id="b13b6-122">Remove ACL entry of catalog for group.</span></span>

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

### <span data-ttu-id="b13b6-123">-ItemType</span><span class="sxs-lookup"><span data-stu-id="b13b6-123">-ItemType</span></span>
<span data-ttu-id="b13b6-124">Gibt den Typ des Katalogs oder des Katalogelements an.</span><span class="sxs-lookup"><span data-stu-id="b13b6-124">Specifies the type of the catalog or catalog item(s).</span></span> <span data-ttu-id="b13b6-125">Die zulässigen Werte für diesen Parameter lauten wie folgt:</span><span class="sxs-lookup"><span data-stu-id="b13b6-125">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="b13b6-126">Katalog</span><span class="sxs-lookup"><span data-stu-id="b13b6-126">Catalog</span></span>
- <span data-ttu-id="b13b6-127">Datenbank</span><span class="sxs-lookup"><span data-stu-id="b13b6-127">Database</span></span>

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

### <span data-ttu-id="b13b6-128">-ObjectID</span><span class="sxs-lookup"><span data-stu-id="b13b6-128">-ObjectId</span></span>
<span data-ttu-id="b13b6-129">Die Identität des Benutzers, der entfernt werden soll.</span><span class="sxs-lookup"><span data-stu-id="b13b6-129">The identity of the user to remove.</span></span>

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

### <span data-ttu-id="b13b6-130">-PassThru</span><span class="sxs-lookup"><span data-stu-id="b13b6-130">-PassThru</span></span>
<span data-ttu-id="b13b6-131">Gibt an, dass eine boolesche Antwort zurückgegeben werden soll, die das Ergebnis des Löschvorgangs angibt.</span><span class="sxs-lookup"><span data-stu-id="b13b6-131">Indicates a boolean response should be returned indicating the result of the delete operation.</span></span>

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

### <span data-ttu-id="b13b6-132">-Path</span><span class="sxs-lookup"><span data-stu-id="b13b6-132">-Path</span></span>
<span data-ttu-id="b13b6-133">Gibt den Daten See-Analysepfad eines Katalog-oder Katalogelements an.</span><span class="sxs-lookup"><span data-stu-id="b13b6-133">Specifies the Data Lake Analytics path of an catalog or catalog item.</span></span>
<span data-ttu-id="b13b6-134">Die Teile des Pfads sollten durch einen Punkt (.) getrennt werden.</span><span class="sxs-lookup"><span data-stu-id="b13b6-134">The parts of the path should be separated by a period (.).</span></span>

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

### <span data-ttu-id="b13b6-135">-User</span><span class="sxs-lookup"><span data-stu-id="b13b6-135">-User</span></span>
<span data-ttu-id="b13b6-136">ACL-Eintrag des Katalogs für Benutzer entfernen.</span><span class="sxs-lookup"><span data-stu-id="b13b6-136">Remove ACL entry of catalog for user.</span></span>

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

### <span data-ttu-id="b13b6-137">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="b13b6-137">-Confirm</span></span>
<span data-ttu-id="b13b6-138">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="b13b6-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b13b6-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b13b6-139">-WhatIf</span></span>
<span data-ttu-id="b13b6-140">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="b13b6-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b13b6-141">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="b13b6-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b13b6-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b13b6-142">CommonParameters</span></span>
<span data-ttu-id="b13b6-143">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b13b6-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b13b6-144">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b13b6-144">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b13b6-145">Eingaben</span><span class="sxs-lookup"><span data-stu-id="b13b6-145">INPUTS</span></span>

### <span data-ttu-id="b13b6-146">System. String</span><span class="sxs-lookup"><span data-stu-id="b13b6-146">System.String</span></span>

### <span data-ttu-id="b13b6-147">System. GUID</span><span class="sxs-lookup"><span data-stu-id="b13b6-147">System.Guid</span></span>

### <span data-ttu-id="b13b6-148">Microsoft. Azure. Commands. DataLakeAnalytics. Models. CatalogPathInstance</span><span class="sxs-lookup"><span data-stu-id="b13b6-148">Microsoft.Azure.Commands.DataLakeAnalytics.Models.CatalogPathInstance</span></span>

## <span data-ttu-id="b13b6-149">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="b13b6-149">OUTPUTS</span></span>

### <span data-ttu-id="b13b6-150">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="b13b6-150">System.Boolean</span></span>

## <span data-ttu-id="b13b6-151">Notizen</span><span class="sxs-lookup"><span data-stu-id="b13b6-151">NOTES</span></span>

## <span data-ttu-id="b13b6-152">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="b13b6-152">RELATED LINKS</span></span>

[<span data-ttu-id="b13b6-153">U-SQL bietet jetzt Zugriffssteuerung auf Datenbankebene</span><span class="sxs-lookup"><span data-stu-id="b13b6-153">U-SQL now offers database level access control</span></span>](https://github.com/Azure/AzureDataLake/blob/master/docs/Release_Notes/2016/2016_08_01/USQL_Release_Notes_2016_08_01.md#u-sql-now-offers-database-level-access-control)

[<span data-ttu-id="b13b6-154">Get-AzureRmDataLakeAnalyticsCatalogItemAclEntry</span><span class="sxs-lookup"><span data-stu-id="b13b6-154">Get-AzureRmDataLakeAnalyticsCatalogItemAclEntry</span></span>](Get-AzureRmDataLakeAnalyticsCatalogItemAclEntry.md)

[<span data-ttu-id="b13b6-155">Satz-AzureRmDataLakeAnalyticsCatalogItemAclEntry</span><span class="sxs-lookup"><span data-stu-id="b13b6-155">Set-AzureRmDataLakeAnalyticsCatalogItemAclEntry</span></span>](Set-AzureRmDataLakeAnalyticsCatalogItemAclEntry.md)
