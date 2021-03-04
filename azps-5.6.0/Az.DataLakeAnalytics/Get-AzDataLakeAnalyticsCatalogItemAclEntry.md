---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeAnalytics.dll-Help.xml
Module Name: Az.DataLakeAnalytics
online version: https://docs.microsoft.com/powershell/module/az.datalakeanalytics/get-azdatalakeanalyticscatalogitemaclentry
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeAnalytics/DataLakeAnalytics/help/Get-AzDataLakeAnalyticsCatalogItemAclEntry.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeAnalytics/DataLakeAnalytics/help/Get-AzDataLakeAnalyticsCatalogItemAclEntry.md
ms.openlocfilehash: 63e0f3622ea7ae83f805688e4634b30c38cb601d
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101925000"
---
# <span data-ttu-id="a69aa-101">Get-AzDataLakeAnalyticsCatalogItemAclEntry</span><span class="sxs-lookup"><span data-stu-id="a69aa-101">Get-AzDataLakeAnalyticsCatalogItemAclEntry</span></span>

## <span data-ttu-id="a69aa-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a69aa-102">SYNOPSIS</span></span>
<span data-ttu-id="a69aa-103">Ruft einen Eintrag in der ACL eines Katalogs oder Katalogelements in Data Lake Analytics ab.</span><span class="sxs-lookup"><span data-stu-id="a69aa-103">Gets an entry in the ACL of a catalog or catalog item in Data Lake Analytics.</span></span>

## <span data-ttu-id="a69aa-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="a69aa-104">SYNTAX</span></span>

### <span data-ttu-id="a69aa-105">GetCatalogAclEntry (Standard)</span><span class="sxs-lookup"><span data-stu-id="a69aa-105">GetCatalogAclEntry (Default)</span></span>
```
Get-AzDataLakeAnalyticsCatalogItemAclEntry [-Account] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="a69aa-106">GetCatalogAclEntryForUserOwner</span><span class="sxs-lookup"><span data-stu-id="a69aa-106">GetCatalogAclEntryForUserOwner</span></span>
```
Get-AzDataLakeAnalyticsCatalogItemAclEntry [-Account] <String> [-UserOwner]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a69aa-107">GetCatalogAclEntryForGroupOwner</span><span class="sxs-lookup"><span data-stu-id="a69aa-107">GetCatalogAclEntryForGroupOwner</span></span>
```
Get-AzDataLakeAnalyticsCatalogItemAclEntry [-Account] <String> [-GroupOwner]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a69aa-108">GetCatalogItemAclEntry</span><span class="sxs-lookup"><span data-stu-id="a69aa-108">GetCatalogItemAclEntry</span></span>
```
Get-AzDataLakeAnalyticsCatalogItemAclEntry [-Account] <String> -ItemType <String> -Path <CatalogPathInstance>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a69aa-109">GetCatalogItemAclEntryForUserOwner</span><span class="sxs-lookup"><span data-stu-id="a69aa-109">GetCatalogItemAclEntryForUserOwner</span></span>
```
Get-AzDataLakeAnalyticsCatalogItemAclEntry [-Account] <String> [-UserOwner] -ItemType <String>
 -Path <CatalogPathInstance> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a69aa-110">GetCatalogItemAclEntryForGroupOwner</span><span class="sxs-lookup"><span data-stu-id="a69aa-110">GetCatalogItemAclEntryForGroupOwner</span></span>
```
Get-AzDataLakeAnalyticsCatalogItemAclEntry [-Account] <String> [-GroupOwner] -ItemType <String>
 -Path <CatalogPathInstance> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a69aa-111">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="a69aa-111">DESCRIPTION</span></span>
<span data-ttu-id="a69aa-112">Das **Cmdlet Get-AzDataLakeAnalyticsCatalogItemAclEntry** ruft eine Liste der Einträge (ACEs) in der Zugriffssteuerungsliste (Access Control List, ACL) eines Katalogs oder Katalogelements in Data Lake Analytics ab.</span><span class="sxs-lookup"><span data-stu-id="a69aa-112">The **Get-AzDataLakeAnalyticsCatalogItemAclEntry** cmdlet gets a list of entries (ACEs) in the access control list (ACL) of a catalog or catalog item in Data Lake Analytics.</span></span>

## <span data-ttu-id="a69aa-113">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="a69aa-113">EXAMPLES</span></span>

### <span data-ttu-id="a69aa-114">Beispiel 1: Herunterladen der ACL für einen Katalog</span><span class="sxs-lookup"><span data-stu-id="a69aa-114">Example 1: Get the ACL for a catalog</span></span>
```powershell
PS C:\> Get-AzDataLakeAnalyticsCatalogItemAclEntry -Account "contosoadla"

Type  Id                                   Permissions
----  --                                   -----------
User  90a6f74b-fd73-490e-900a-c4f0f9694d02        Read
Group 902b155a-5601-4ca8-8178-ad3289211f88   ReadWrite
Other 00000000-0000-0000-0000-000000000000        None
```

<span data-ttu-id="a69aa-115">Dieser Befehl ruft die ACL für den Katalog des angegebenen Data Lake Analytics-Kontos ab.</span><span class="sxs-lookup"><span data-stu-id="a69aa-115">This command gets the ACL for the catalog of the specified Data Lake Analytics account</span></span>

### <span data-ttu-id="a69aa-116">Beispiel 2: Herunterladen des ACL-Eintrags des Benutzerbesitzers für einen Katalog</span><span class="sxs-lookup"><span data-stu-id="a69aa-116">Example 2: Get the ACL entry of user owner for a catalog</span></span>
```powershell
PS C:\> Get-AzDataLakeAnalyticsCatalogItemAclEntry -Account "contosoadla" -UserOwner

Type      Id                                   Permissions
----      --                                   -----------
UserOwner 0316ac75-6703-4ace-984f-a4dd79aeeafc   ReadWrite
```

<span data-ttu-id="a69aa-117">Dieser Befehl ruft den ACL-Eintrag des Benutzerbesitzers für den Katalog des angegebenen Data Lake Analytics-Kontos ab.</span><span class="sxs-lookup"><span data-stu-id="a69aa-117">This command gets ACL entry of the user owner for the catalog of the specified Data Lake Analytics account</span></span>

### <span data-ttu-id="a69aa-118">Beispiel 3: Herunterladen des ACL-Eintrags des Gruppenbesitzers für einen Katalog</span><span class="sxs-lookup"><span data-stu-id="a69aa-118">Example 3: Get the ACL entry of group owner for a catalog</span></span>
```powershell
PS C:\> Get-AzDataLakeAnalyticsCatalogItemAclEntry -Account "contosoadla" -GroupOwner

Type       Id                                   Permissions
----       --                                   -----------
GroupOwner 0316ac75-6703-4ace-984f-a4dd79aeeafc   ReadWrite
```

<span data-ttu-id="a69aa-119">Dieser Befehl ruft den ACL-Eintrag des Gruppenbesitzers für den Katalog des angegebenen Data Lake Analytics-Kontos ab.</span><span class="sxs-lookup"><span data-stu-id="a69aa-119">This command gets ACL entry of the group owner for the catalog of the specified Data Lake Analytics account</span></span>

### <span data-ttu-id="a69aa-120">Beispiel 4: Erhalten der ACL für eine Datenbank</span><span class="sxs-lookup"><span data-stu-id="a69aa-120">Example 4: Get the ACL for a database</span></span>
```powershell
PS C:\> Get-AzDataLakeAnalyticsCatalogItemAclEntry -Account "contosoadla" -ItemType Database -Path "databaseName"

Type  Id                                   Permissions
----  --                                   -----------
User  90a6f74b-fd73-490e-900a-c4f0f9694d02        Read
Group 902b155a-5601-4ca8-8178-ad3289211f88   ReadWrite
Other 00000000-0000-0000-0000-000000000000        None
```

<span data-ttu-id="a69aa-121">Dieser Befehl ruft die ACL für die Datenbank des angegebenen Data Lake Analytics-Kontos ab.</span><span class="sxs-lookup"><span data-stu-id="a69aa-121">This command gets the ACL for the database of the specified Data Lake Analytics account</span></span>

### <span data-ttu-id="a69aa-122">Beispiel 5: Erhalten des ACL-Eintrags des Benutzerbesitzers für eine Datenbank</span><span class="sxs-lookup"><span data-stu-id="a69aa-122">Example 5: Get the ACL entry of user owner for a database</span></span>
```powershell
PS C:\> Get-AzDataLakeAnalyticsCatalogItemAclEntry -Account "contosoadla" -UserOwner -ItemType Database -Path "databaseName"

Type      Id                                   Permissions
----      --                                   -----------
UserOwner 0316ac75-6703-4ace-984f-a4dd79aeeafc   ReadWrite
```

<span data-ttu-id="a69aa-123">Dieser Befehl ruft den ACL-Eintrag des Benutzerbesitzers für die Datenbank des angegebenen Data Lake Analytics-Kontos ab.</span><span class="sxs-lookup"><span data-stu-id="a69aa-123">This command gets the ACL entry of the user owner for the database of the specified Data Lake Analytics account</span></span>

### <span data-ttu-id="a69aa-124">Beispiel 6: Erhalten des ACL-Eintrags des Gruppenbesitzers für eine Datenbank</span><span class="sxs-lookup"><span data-stu-id="a69aa-124">Example 6: Get the ACL entry of group owner for a database</span></span>
```powershell
PS C:\> Get-AzDataLakeAnalyticsCatalogItemAclEntry -Account "contosoadla" -GroupOwner -ItemType Database -Path "databaseName"

Type       Id                                   Permissions
----       --                                   -----------
GroupOwner 0316ac75-6703-4ace-984f-a4dd79aeeafc   ReadWrite
```

<span data-ttu-id="a69aa-125">Dieser Befehl ruft den ACL-Eintrag des Gruppenbesitzers für die Datenbank des angegebenen Data Lake Analytics-Kontos ab.</span><span class="sxs-lookup"><span data-stu-id="a69aa-125">This command gets the ACL entry of the group owner for the database of the specified Data Lake Analytics account</span></span>

## <span data-ttu-id="a69aa-126">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="a69aa-126">PARAMETERS</span></span>

### <span data-ttu-id="a69aa-127">-Konto</span><span class="sxs-lookup"><span data-stu-id="a69aa-127">-Account</span></span>
<span data-ttu-id="a69aa-128">Gibt den Namen des Data Lake Analytics-Kontos an.</span><span class="sxs-lookup"><span data-stu-id="a69aa-128">Specifies the Data Lake Analytics account name.</span></span>

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

### <span data-ttu-id="a69aa-129">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a69aa-129">-DefaultProfile</span></span>
<span data-ttu-id="a69aa-130">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="a69aa-130">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a69aa-131">-GroupOwner</span><span class="sxs-lookup"><span data-stu-id="a69aa-131">-GroupOwner</span></span>
<span data-ttu-id="a69aa-132">ACL-Eintrag des Katalogs für gruppenbesitzer</span><span class="sxs-lookup"><span data-stu-id="a69aa-132">Get ACL entry of catalog for group owner</span></span>

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

### <span data-ttu-id="a69aa-133">-ItemType</span><span class="sxs-lookup"><span data-stu-id="a69aa-133">-ItemType</span></span>
<span data-ttu-id="a69aa-134">Gibt den Typ des Katalogs oder Katalogelements an.</span><span class="sxs-lookup"><span data-stu-id="a69aa-134">Specifies the type of the catalog or catalog item(s).</span></span> <span data-ttu-id="a69aa-135">Die zulässigen Werte für diesen Parameter sind:</span><span class="sxs-lookup"><span data-stu-id="a69aa-135">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="a69aa-136">Katalog</span><span class="sxs-lookup"><span data-stu-id="a69aa-136">Catalog</span></span>
- <span data-ttu-id="a69aa-137">Datenbank</span><span class="sxs-lookup"><span data-stu-id="a69aa-137">Database</span></span>

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

### <span data-ttu-id="a69aa-138">-Path</span><span class="sxs-lookup"><span data-stu-id="a69aa-138">-Path</span></span>
<span data-ttu-id="a69aa-139">Gibt den Data Lake Analytics-Pfad eines Katalogs oder Katalogelements an.</span><span class="sxs-lookup"><span data-stu-id="a69aa-139">Specifies the Data Lake Analytics path of an catalog or catalog item.</span></span>
<span data-ttu-id="a69aa-140">Die Teile des Pfads sollten durch einen Zeitraum (.) getrennt sein.</span><span class="sxs-lookup"><span data-stu-id="a69aa-140">The parts of the path should be separated by a period (.).</span></span>

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

### <span data-ttu-id="a69aa-141">-UserOwner</span><span class="sxs-lookup"><span data-stu-id="a69aa-141">-UserOwner</span></span>
<span data-ttu-id="a69aa-142">Holen Sie sich den ACL-Eintrag des Katalogs für den Benutzerbesitzer.</span><span class="sxs-lookup"><span data-stu-id="a69aa-142">Get ACL entry of catalog for user owner.</span></span>

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

### <span data-ttu-id="a69aa-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a69aa-143">CommonParameters</span></span>
<span data-ttu-id="a69aa-144">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a69aa-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a69aa-145">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a69aa-145">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a69aa-146">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="a69aa-146">INPUTS</span></span>

### <span data-ttu-id="a69aa-147">System.String</span><span class="sxs-lookup"><span data-stu-id="a69aa-147">System.String</span></span>

### <span data-ttu-id="a69aa-148">Microsoft.Azure.Commands.DataLakeAnalytics.Models.CatalogPathInstance</span><span class="sxs-lookup"><span data-stu-id="a69aa-148">Microsoft.Azure.Commands.DataLakeAnalytics.Models.CatalogPathInstance</span></span>

## <span data-ttu-id="a69aa-149">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="a69aa-149">OUTPUTS</span></span>

### <span data-ttu-id="a69aa-150">Microsoft.Azure.Commands.DataLakeAnalytics.Models.PSDataLakeAnalyticsAcl</span><span class="sxs-lookup"><span data-stu-id="a69aa-150">Microsoft.Azure.Commands.DataLakeAnalytics.Models.PSDataLakeAnalyticsAcl</span></span>

## <span data-ttu-id="a69aa-151">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="a69aa-151">NOTES</span></span>

## <span data-ttu-id="a69aa-152">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="a69aa-152">RELATED LINKS</span></span>

[<span data-ttu-id="a69aa-153">U-SQL bietet jetzt Zugriffssteuerung auf Datenbankebene</span><span class="sxs-lookup"><span data-stu-id="a69aa-153">U-SQL now offers database level access control</span></span>](https://github.com/Azure/AzureDataLake/blob/master/docs/Release_Notes/2016/2016_08_01/USQL_Release_Notes_2016_08_01.md#u-sql-now-offers-database-level-access-control)

[<span data-ttu-id="a69aa-154">Remove-AzDataLakeAnalyticsCatalogItemAclEntry</span><span class="sxs-lookup"><span data-stu-id="a69aa-154">Remove-AzDataLakeAnalyticsCatalogItemAclEntry</span></span>](Remove-AzDataLakeAnalyticsCatalogItemAclEntry.md)

[<span data-ttu-id="a69aa-155">Set-AzDataLakeAnalyticsCatalogItemAclEntry</span><span class="sxs-lookup"><span data-stu-id="a69aa-155">Set-AzDataLakeAnalyticsCatalogItemAclEntry</span></span>](Set-AzDataLakeAnalyticsCatalogItemAclEntry.md)
