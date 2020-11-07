---
external help file: Microsoft.Azure.Commands.DataLakeAnalytics.dll-Help.xml
Module Name: AzureRM.DataLakeAnalytics
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datalakeanalytics/get-azurermdatalakeanalyticscatalogitemaclentry
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeAnalytics/Commands.DataLakeAnalytics/help/Get-AzureRmDataLakeAnalyticsCatalogItemAclEntry.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeAnalytics/Commands.DataLakeAnalytics/help/Get-AzureRmDataLakeAnalyticsCatalogItemAclEntry.md
ms.openlocfilehash: 349fe79bf3ff3bea0097542ee0189b5a1999bd35
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93664076"
---
# <span data-ttu-id="a85e2-101">Get-AzureRmDataLakeAnalyticsCatalogItemAclEntry</span><span class="sxs-lookup"><span data-stu-id="a85e2-101">Get-AzureRmDataLakeAnalyticsCatalogItemAclEntry</span></span>

## <span data-ttu-id="a85e2-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="a85e2-102">SYNOPSIS</span></span>
<span data-ttu-id="a85e2-103">Ruft einen Eintrag in der ACL eines Katalog-oder Katalogelements in Data Lake Analytics ab.</span><span class="sxs-lookup"><span data-stu-id="a85e2-103">Gets an entry in the ACL of a catalog or catalog item in Data Lake Analytics.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a85e2-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="a85e2-104">SYNTAX</span></span>

### <span data-ttu-id="a85e2-105">GetCatalogAclEntry (Standard)</span><span class="sxs-lookup"><span data-stu-id="a85e2-105">GetCatalogAclEntry (Default)</span></span>
```
Get-AzureRmDataLakeAnalyticsCatalogItemAclEntry [-Account] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="a85e2-106">GetCatalogAclEntryForUserOwner</span><span class="sxs-lookup"><span data-stu-id="a85e2-106">GetCatalogAclEntryForUserOwner</span></span>
```
Get-AzureRmDataLakeAnalyticsCatalogItemAclEntry [-Account] <String> [-UserOwner]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a85e2-107">GetCatalogAclEntryForGroupOwner</span><span class="sxs-lookup"><span data-stu-id="a85e2-107">GetCatalogAclEntryForGroupOwner</span></span>
```
Get-AzureRmDataLakeAnalyticsCatalogItemAclEntry [-Account] <String> [-GroupOwner]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a85e2-108">GetCatalogItemAclEntry</span><span class="sxs-lookup"><span data-stu-id="a85e2-108">GetCatalogItemAclEntry</span></span>
```
Get-AzureRmDataLakeAnalyticsCatalogItemAclEntry [-Account] <String> -ItemType <String>
 -Path <CatalogPathInstance> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a85e2-109">GetCatalogItemAclEntryForUserOwner</span><span class="sxs-lookup"><span data-stu-id="a85e2-109">GetCatalogItemAclEntryForUserOwner</span></span>
```
Get-AzureRmDataLakeAnalyticsCatalogItemAclEntry [-Account] <String> [-UserOwner] -ItemType <String>
 -Path <CatalogPathInstance> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a85e2-110">GetCatalogItemAclEntryForGroupOwner</span><span class="sxs-lookup"><span data-stu-id="a85e2-110">GetCatalogItemAclEntryForGroupOwner</span></span>
```
Get-AzureRmDataLakeAnalyticsCatalogItemAclEntry [-Account] <String> [-GroupOwner] -ItemType <String>
 -Path <CatalogPathInstance> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a85e2-111">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="a85e2-111">DESCRIPTION</span></span>
<span data-ttu-id="a85e2-112">Das Cmdlet " **Get-AzureRmDataLakeAnalyticsCatalogItemAclEntry** " Ruft eine Liste von Einträgen (ACEs) in der Zugriffssteuerungsliste (ACL) eines Katalog-oder Katalogelements in Data Lake Analytics ab.</span><span class="sxs-lookup"><span data-stu-id="a85e2-112">The **Get-AzureRmDataLakeAnalyticsCatalogItemAclEntry** cmdlet gets a list of entries (ACEs) in the access control list (ACL) of a catalog or catalog item in Data Lake Analytics.</span></span>

## <span data-ttu-id="a85e2-113">Beispiele</span><span class="sxs-lookup"><span data-stu-id="a85e2-113">EXAMPLES</span></span>

### <span data-ttu-id="a85e2-114">Beispiel 1: Abrufen der ACL für einen Katalog</span><span class="sxs-lookup"><span data-stu-id="a85e2-114">Example 1: Get the ACL for a catalog</span></span>
```powershell
PS C:\> Get-AzureRmDataLakeAnalyticsCatalogItemAclEntry -Account "contosoadla"

Type  Id                                   Permissions
----  --                                   -----------
User  90a6f74b-fd73-490e-900a-c4f0f9694d02        Read
Group 902b155a-5601-4ca8-8178-ad3289211f88   ReadWrite
Other 00000000-0000-0000-0000-000000000000        None
```

<span data-ttu-id="a85e2-115">Mit diesem Befehl wird die ACL für den Katalog des angegebenen Data Lake Analytics-Kontos abgerufen.</span><span class="sxs-lookup"><span data-stu-id="a85e2-115">This command gets the ACL for the catalog of the specified Data Lake Analytics account</span></span>

### <span data-ttu-id="a85e2-116">Beispiel 2: Abrufen des ACL-Eintrags des Benutzer Besitzers für einen Katalog</span><span class="sxs-lookup"><span data-stu-id="a85e2-116">Example 2: Get the ACL entry of user owner for a catalog</span></span>
```powershell
PS C:\> Get-AzureRmDataLakeAnalyticsCatalogItemAclEntry -Account "contosoadla" -UserOwner

Type      Id                                   Permissions
----      --                                   -----------
UserOwner 0316ac75-6703-4ace-984f-a4dd79aeeafc   ReadWrite
```

<span data-ttu-id="a85e2-117">Dieser Befehl ruft die ACL-Eingabe des Benutzer Besitzers für den Katalog des angegebenen Data Lake Analytics-Kontos ab.</span><span class="sxs-lookup"><span data-stu-id="a85e2-117">This command gets ACL entry of the user owner for the catalog of the specified Data Lake Analytics account</span></span>

### <span data-ttu-id="a85e2-118">Beispiel 3: Abrufen des ACL-Eintrags des Gruppen Besitzers für einen Katalog</span><span class="sxs-lookup"><span data-stu-id="a85e2-118">Example 3: Get the ACL entry of group owner for a catalog</span></span>
```powershell
PS C:\> Get-AzureRmDataLakeAnalyticsCatalogItemAclEntry -Account "contosoadla" -GroupOwner

Type       Id                                   Permissions
----       --                                   -----------
GroupOwner 0316ac75-6703-4ace-984f-a4dd79aeeafc   ReadWrite
```

<span data-ttu-id="a85e2-119">Dieser Befehl ruft die ACL-Eingabe des Gruppen Besitzers für den Katalog des angegebenen Data Lake Analytics-Kontos ab.</span><span class="sxs-lookup"><span data-stu-id="a85e2-119">This command gets ACL entry of the group owner for the catalog of the specified Data Lake Analytics account</span></span>

### <span data-ttu-id="a85e2-120">Beispiel 4: Abrufen der ACL für eine Datenbank</span><span class="sxs-lookup"><span data-stu-id="a85e2-120">Example 4: Get the ACL for a database</span></span>
```powershell
PS C:\> Get-AzureRmDataLakeAnalyticsCatalogItemAclEntry -Account "contosoadla" -ItemType Database -Path "databaseName"

Type  Id                                   Permissions
----  --                                   -----------
User  90a6f74b-fd73-490e-900a-c4f0f9694d02        Read
Group 902b155a-5601-4ca8-8178-ad3289211f88   ReadWrite
Other 00000000-0000-0000-0000-000000000000        None
```

<span data-ttu-id="a85e2-121">Mit diesem Befehl wird die ACL für die Datenbank des angegebenen Data Lake Analytics-Kontos abgerufen.</span><span class="sxs-lookup"><span data-stu-id="a85e2-121">This command gets the ACL for the database of the specified Data Lake Analytics account</span></span>

### <span data-ttu-id="a85e2-122">Beispiel 5: Abrufen des ACL-Eintrags des Benutzer Besitzers für eine Datenbank</span><span class="sxs-lookup"><span data-stu-id="a85e2-122">Example 5: Get the ACL entry of user owner for a database</span></span>
```powershell
PS C:\> Get-AzureRmDataLakeAnalyticsCatalogItemAclEntry -Account "contosoadla" -UserOwner -ItemType Database -Path "databaseName"

Type      Id                                   Permissions
----      --                                   -----------
UserOwner 0316ac75-6703-4ace-984f-a4dd79aeeafc   ReadWrite
```

<span data-ttu-id="a85e2-123">Mit diesem Befehl wird der ACL-Eintrag des Benutzer Besitzers für die Datenbank des angegebenen Data Lake Analytics-Kontos abgerufen.</span><span class="sxs-lookup"><span data-stu-id="a85e2-123">This command gets the ACL entry of the user owner for the database of the specified Data Lake Analytics account</span></span>

### <span data-ttu-id="a85e2-124">Beispiel 6: Abrufen des ACL-Eintrags des Gruppen Besitzers für eine Datenbank</span><span class="sxs-lookup"><span data-stu-id="a85e2-124">Example 6: Get the ACL entry of group owner for a database</span></span>
```powershell
PS C:\> Get-AzureRmDataLakeAnalyticsCatalogItemAclEntry -Account "contosoadla" -GroupOwner -ItemType Database -Path "databaseName"

Type       Id                                   Permissions
----       --                                   -----------
GroupOwner 0316ac75-6703-4ace-984f-a4dd79aeeafc   ReadWrite
```

<span data-ttu-id="a85e2-125">Mit diesem Befehl wird der ACL-Eintrag des Gruppen Besitzers für die Datenbank des angegebenen Data Lake Analytics-Kontos abgerufen.</span><span class="sxs-lookup"><span data-stu-id="a85e2-125">This command gets the ACL entry of the group owner for the database of the specified Data Lake Analytics account</span></span>

## <span data-ttu-id="a85e2-126">Parameter</span><span class="sxs-lookup"><span data-stu-id="a85e2-126">PARAMETERS</span></span>

### <span data-ttu-id="a85e2-127">-Konto</span><span class="sxs-lookup"><span data-stu-id="a85e2-127">-Account</span></span>
<span data-ttu-id="a85e2-128">Gibt den Namen des Daten Lake Analytics-Kontos an.</span><span class="sxs-lookup"><span data-stu-id="a85e2-128">Specifies the Data Lake Analytics account name.</span></span>

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

### <span data-ttu-id="a85e2-129">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a85e2-129">-DefaultProfile</span></span>
<span data-ttu-id="a85e2-130">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="a85e2-130">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a85e2-131">-GroupOwner</span><span class="sxs-lookup"><span data-stu-id="a85e2-131">-GroupOwner</span></span>
<span data-ttu-id="a85e2-132">Abrufen des ACL-Eintrags des Katalogs für den Gruppenbesitzer</span><span class="sxs-lookup"><span data-stu-id="a85e2-132">Get ACL entry of catalog for group owner</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: GetCatalogAclEntryForGroupOwner, GetCatalogItemAclEntryForGroupOwner
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a85e2-133">-ItemType</span><span class="sxs-lookup"><span data-stu-id="a85e2-133">-ItemType</span></span>
<span data-ttu-id="a85e2-134">Gibt den Typ des Katalogs oder des Katalogelements an.</span><span class="sxs-lookup"><span data-stu-id="a85e2-134">Specifies the type of the catalog or catalog item(s).</span></span> <span data-ttu-id="a85e2-135">Die zulässigen Werte für diesen Parameter lauten wie folgt:</span><span class="sxs-lookup"><span data-stu-id="a85e2-135">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="a85e2-136">Katalog</span><span class="sxs-lookup"><span data-stu-id="a85e2-136">Catalog</span></span>
- <span data-ttu-id="a85e2-137">Datenbank</span><span class="sxs-lookup"><span data-stu-id="a85e2-137">Database</span></span>

```yaml
Type: System.String
Parameter Sets: GetCatalogItemAclEntry, GetCatalogItemAclEntryForUserOwner, GetCatalogItemAclEntryForGroupOwner
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a85e2-138">-Path</span><span class="sxs-lookup"><span data-stu-id="a85e2-138">-Path</span></span>
<span data-ttu-id="a85e2-139">Gibt den Daten See-Analysepfad eines Katalog-oder Katalogelements an.</span><span class="sxs-lookup"><span data-stu-id="a85e2-139">Specifies the Data Lake Analytics path of an catalog or catalog item.</span></span>
<span data-ttu-id="a85e2-140">Die Teile des Pfads sollten durch einen Punkt (.) getrennt werden.</span><span class="sxs-lookup"><span data-stu-id="a85e2-140">The parts of the path should be separated by a period (.).</span></span>

```yaml
Type: Microsoft.Azure.Commands.DataLakeAnalytics.Models.CatalogPathInstance
Parameter Sets: GetCatalogItemAclEntry, GetCatalogItemAclEntryForUserOwner, GetCatalogItemAclEntryForGroupOwner
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a85e2-141">-UserOwner</span><span class="sxs-lookup"><span data-stu-id="a85e2-141">-UserOwner</span></span>
<span data-ttu-id="a85e2-142">Abrufen des ACL-Eintrags des Katalogs für den Benutzer Besitzer</span><span class="sxs-lookup"><span data-stu-id="a85e2-142">Get ACL entry of catalog for user owner.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: GetCatalogAclEntryForUserOwner, GetCatalogItemAclEntryForUserOwner
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a85e2-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a85e2-143">CommonParameters</span></span>
<span data-ttu-id="a85e2-144">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a85e2-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a85e2-145">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a85e2-145">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a85e2-146">Eingaben</span><span class="sxs-lookup"><span data-stu-id="a85e2-146">INPUTS</span></span>

### <span data-ttu-id="a85e2-147">System. String</span><span class="sxs-lookup"><span data-stu-id="a85e2-147">System.String</span></span>

### <span data-ttu-id="a85e2-148">Microsoft. Azure. Commands. DataLakeAnalytics. Models. CatalogPathInstance</span><span class="sxs-lookup"><span data-stu-id="a85e2-148">Microsoft.Azure.Commands.DataLakeAnalytics.Models.CatalogPathInstance</span></span>

## <span data-ttu-id="a85e2-149">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="a85e2-149">OUTPUTS</span></span>

### <span data-ttu-id="a85e2-150">Microsoft.Azure.Commands.DataLakeAnalytics.Models.PSDataLakeAnalyticsAcl</span><span class="sxs-lookup"><span data-stu-id="a85e2-150">Microsoft.Azure.Commands.DataLakeAnalytics.Models.PSDataLakeAnalyticsAcl</span></span>

## <span data-ttu-id="a85e2-151">Notizen</span><span class="sxs-lookup"><span data-stu-id="a85e2-151">NOTES</span></span>

## <span data-ttu-id="a85e2-152">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="a85e2-152">RELATED LINKS</span></span>

[<span data-ttu-id="a85e2-153">U-SQL bietet jetzt Zugriffssteuerung auf Datenbankebene</span><span class="sxs-lookup"><span data-stu-id="a85e2-153">U-SQL now offers database level access control</span></span>](https://github.com/Azure/AzureDataLake/blob/master/docs/Release_Notes/2016/2016_08_01/USQL_Release_Notes_2016_08_01.md#u-sql-now-offers-database-level-access-control)

[<span data-ttu-id="a85e2-154">Remove-AzureRmDataLakeAnalyticsCatalogItemAclEntry</span><span class="sxs-lookup"><span data-stu-id="a85e2-154">Remove-AzureRmDataLakeAnalyticsCatalogItemAclEntry</span></span>](Remove-AzureRmDataLakeAnalyticsCatalogItemAclEntry.md)

[<span data-ttu-id="a85e2-155">Satz-AzureRmDataLakeAnalyticsCatalogItemAclEntry</span><span class="sxs-lookup"><span data-stu-id="a85e2-155">Set-AzureRmDataLakeAnalyticsCatalogItemAclEntry</span></span>](Set-AzureRmDataLakeAnalyticsCatalogItemAclEntry.md)
