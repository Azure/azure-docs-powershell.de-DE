---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 457FD595-D5E1-45C4-9DB8-C3C6C30A0E94
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/Update-AzSqlDatabaseAdvancedThreatProtectionSetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Update-AzSqlDatabaseAdvancedThreatProtectionSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Update-AzSqlDatabaseAdvancedThreatProtectionSetting.md
ms.openlocfilehash: baa3e3d4b272bccab5fe33b9af05edc9ed254236
ms.sourcegitcommit: 0c61b7f42dec507e576c92e0a516c6655e9f50fc
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/14/2021
ms.locfileid: "100406705"
---
# <span data-ttu-id="3ad53-101">Update-AzSqlDatabaseAdvancedThreatProtectionSetting</span><span class="sxs-lookup"><span data-stu-id="3ad53-101">Update-AzSqlDatabaseAdvancedThreatProtectionSetting</span></span>

## <span data-ttu-id="3ad53-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3ad53-102">SYNOPSIS</span></span>
<span data-ttu-id="3ad53-103">Legt eine erweiterte Threat Protection-Einstellung für eine Datenbank fest.</span><span class="sxs-lookup"><span data-stu-id="3ad53-103">Sets a advanced threat protection settings on a database.</span></span>

## <span data-ttu-id="3ad53-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="3ad53-104">SYNTAX</span></span>

```
Update-AzSqlDatabaseAdvancedThreatProtectionSetting [-PassThru] [-NotificationRecipientsEmails <String>]
 [-EmailAdmins <Boolean>] [-ExcludedDetectionType <String[]>] [-StorageAccountName <String>]
 [-RetentionInDays <UInt32>] [-ServerName] <String> [-DatabaseName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3ad53-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="3ad53-105">DESCRIPTION</span></span>
<span data-ttu-id="3ad53-106">Das **Cmdlet "Update-AzSqlDatabaseAdvancedThreatProtectionSetting"** legt eine erweiterte Threat Protection-Einstellung für eine Azure SQL fest.</span><span class="sxs-lookup"><span data-stu-id="3ad53-106">The **Update-AzSqlDatabaseAdvancedThreatProtectionSetting** cmdlet sets a advanced threat protection settings on an Azure SQL database.</span></span>
<span data-ttu-id="3ad53-107">Um erweiterten Bedrohungsschutz für eine Datenbank zu aktivieren, müssen für diese Datenbank Überwachungseinstellungen aktiviert sein.</span><span class="sxs-lookup"><span data-stu-id="3ad53-107">In order to enable advanced threat protection on a database an auditing settings must be enabled on that database.</span></span>
<span data-ttu-id="3ad53-108">Um dieses Cmdlet zu verwenden, geben Sie die Parameter *"ResourceGroupName",* *"ServerName"* und *"DatabaseName"* an, um die Datenbank zu identifizieren.</span><span class="sxs-lookup"><span data-stu-id="3ad53-108">To use this cmdlet, specify the *ResourceGroupName*, *ServerName* and *DatabaseName* parameters to identify the database.</span></span>
<span data-ttu-id="3ad53-109">Dieses Cmdlet wird auch vom Dienst SQL Server Stretch Database in Azure unterstützt.</span><span class="sxs-lookup"><span data-stu-id="3ad53-109">This cmdlet is also supported by the SQL Server Stretch Database service on Azure.</span></span>

## <span data-ttu-id="3ad53-110">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="3ad53-110">EXAMPLES</span></span>

### <span data-ttu-id="3ad53-111">Beispiel 1: Festlegen der erweiterten Threat Protection-Einstellungen für eine Datenbank</span><span class="sxs-lookup"><span data-stu-id="3ad53-111">Example 1: Set the advanced threat protection settings for a database</span></span>
```
PS C:\>Update-AzSqlDatabaseAdvancedThreatProtectionSetting -ResourceGroupName "ResourceGroup11" -ServerName "Server01" -DatabaseName "Database01" -NotificationRecipientsEmails "admin01@contoso.com;secadmin@contoso.com" -EmailAdmins $False -ExcludedDetectionType "Sql_Injection_Vulnerability", "SQL_Injection" -StorageAccountName "mystorageAccount"
```

<span data-ttu-id="3ad53-112">Mit diesem Befehl werden die erweiterten Threat Protection-Einstellungen für eine Datenbank mit dem Namen "Database01" auf dem Server "Server01" festgelegt.</span><span class="sxs-lookup"><span data-stu-id="3ad53-112">This command sets the advanced threat protection settings for a database named Database01 on the server named Server01.</span></span>

## <span data-ttu-id="3ad53-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="3ad53-113">PARAMETERS</span></span>

### <span data-ttu-id="3ad53-114">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="3ad53-114">-DatabaseName</span></span>
<span data-ttu-id="3ad53-115">Gibt den Namen der Datenbank an, in der die Einstellungen festgelegt sind.</span><span class="sxs-lookup"><span data-stu-id="3ad53-115">Specifies the name of the database where the settings is set.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3ad53-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3ad53-116">-DefaultProfile</span></span>
<span data-ttu-id="3ad53-117">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden</span><span class="sxs-lookup"><span data-stu-id="3ad53-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="3ad53-118">-EmailAdmins</span><span class="sxs-lookup"><span data-stu-id="3ad53-118">-EmailAdmins</span></span>
<span data-ttu-id="3ad53-119">Gibt an, ob die erweiterten Threat Protection-Einstellungen mithilfe von E-Mail Kontakt zu Administratoren haben.</span><span class="sxs-lookup"><span data-stu-id="3ad53-119">Specifies whether the advanced threat protection settings contacts administrators by using email.</span></span>

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3ad53-120">-ExcludedDetectionType</span><span class="sxs-lookup"><span data-stu-id="3ad53-120">-ExcludedDetectionType</span></span>
<span data-ttu-id="3ad53-121">Gibt ein Array von Erkennungstypen an, die aus den Einstellungen ausgeschlossen werden.</span><span class="sxs-lookup"><span data-stu-id="3ad53-121">Specifies an array of detection types to exclude from the settings.</span></span>
<span data-ttu-id="3ad53-122">Die zulässigen Werte für diesen Parameter sind:</span><span class="sxs-lookup"><span data-stu-id="3ad53-122">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="3ad53-123">Sql_Injection</span><span class="sxs-lookup"><span data-stu-id="3ad53-123">Sql_Injection</span></span>
- <span data-ttu-id="3ad53-124">Sql_Injection_Vulnerability</span><span class="sxs-lookup"><span data-stu-id="3ad53-124">Sql_Injection_Vulnerability</span></span>
- <span data-ttu-id="3ad53-125">Access_Anomaly</span><span class="sxs-lookup"><span data-stu-id="3ad53-125">Access_Anomaly</span></span>
- <span data-ttu-id="3ad53-126">Keine</span><span class="sxs-lookup"><span data-stu-id="3ad53-126">None</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3ad53-127">-NotificationRecipientsEmails</span><span class="sxs-lookup"><span data-stu-id="3ad53-127">-NotificationRecipientsEmails</span></span>
<span data-ttu-id="3ad53-128">Gibt eine durch Semikolons getrennte Liste von E-Mail-Adressen an, an die die Einstellungen Benachrichtigungen senden.</span><span class="sxs-lookup"><span data-stu-id="3ad53-128">Specifies a semicolon-separated list of email addresses to which the settings sends alerts.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3ad53-129">-PassThru</span><span class="sxs-lookup"><span data-stu-id="3ad53-129">-PassThru</span></span>
<span data-ttu-id="3ad53-130">Gibt ein Objekt zurück, das das Element darstellt, mit dem Sie arbeiten.</span><span class="sxs-lookup"><span data-stu-id="3ad53-130">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="3ad53-131">Standardmäßig generiert dieses Cmdlet keine Ausgabe.</span><span class="sxs-lookup"><span data-stu-id="3ad53-131">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="3ad53-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3ad53-132">-ResourceGroupName</span></span>
<span data-ttu-id="3ad53-133">Gibt den Namen der Ressourcengruppe an, der der Server zugewiesen ist.</span><span class="sxs-lookup"><span data-stu-id="3ad53-133">Specifies the name of the resource group to which the server is assigned.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3ad53-134">-RetentionInDays</span><span class="sxs-lookup"><span data-stu-id="3ad53-134">-RetentionInDays</span></span>
<span data-ttu-id="3ad53-135">Die Anzahl der Aufbewahrungstage für die Überwachungsprotokolle</span><span class="sxs-lookup"><span data-stu-id="3ad53-135">The number of retention days for the audit logs</span></span>

```yaml
Type: System.Nullable`1[System.UInt32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3ad53-136">-ServerName</span><span class="sxs-lookup"><span data-stu-id="3ad53-136">-ServerName</span></span>
<span data-ttu-id="3ad53-137">Gibt den Namen des Servers an.</span><span class="sxs-lookup"><span data-stu-id="3ad53-137">Specifies the name of the server.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3ad53-138">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="3ad53-138">-StorageAccountName</span></span>
<span data-ttu-id="3ad53-139">Gibt den Namen des zu verwendenden Speicherkontos an.</span><span class="sxs-lookup"><span data-stu-id="3ad53-139">Specifies the name of the storage account to be used.</span></span> <span data-ttu-id="3ad53-140">Platzhalter sind nicht zulässig.</span><span class="sxs-lookup"><span data-stu-id="3ad53-140">Wildcards are not permitted.</span></span> <span data-ttu-id="3ad53-141">Dieser Parameter ist nicht erforderlich.</span><span class="sxs-lookup"><span data-stu-id="3ad53-141">This parameter is not required.</span></span> <span data-ttu-id="3ad53-142">Wenn dieser Parameter nicht bereitgestellt wird, verwendet das Cmdlet das Speicherkonto, das zuvor als Teil der erweiterten Threat Protection-Einstellungen der Datenbank definiert wurde.</span><span class="sxs-lookup"><span data-stu-id="3ad53-142">When this parameter is not provided, the cmdlet will use the storage account that was defined previously as part of the advanced threat protection settings of the database.</span></span> <span data-ttu-id="3ad53-143">Wenn dies das erste Mal ist, dass erweiterte Threat Protection-Einstellungen für eine Datenbank definiert werden und dieser Parameter nicht bereitgestellt wird, kann das Cmdlet nicht verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="3ad53-143">If this is the first time a database advanced threat protection settings is defined and this parameter is not provided, the cmdlet will fail.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3ad53-144">-Confirm</span><span class="sxs-lookup"><span data-stu-id="3ad53-144">-Confirm</span></span>
<span data-ttu-id="3ad53-145">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="3ad53-145">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3ad53-146">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="3ad53-146">-WhatIf</span></span>
<span data-ttu-id="3ad53-147">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="3ad53-147">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3ad53-148">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="3ad53-148">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3ad53-149">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3ad53-149">CommonParameters</span></span>
<span data-ttu-id="3ad53-150">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3ad53-150">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3ad53-151">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="3ad53-151">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3ad53-152">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="3ad53-152">INPUTS</span></span>

### <span data-ttu-id="3ad53-153">System.String</span><span class="sxs-lookup"><span data-stu-id="3ad53-153">System.String</span></span>

### <span data-ttu-id="3ad53-154">System.Nullable'1[[System.Boolean, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="3ad53-154">System.Nullable\`1[[System.Boolean, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="3ad53-155">Microsoft.Azure.Commands.Sql.ThreatDetection.Model.DetectionType[]</span><span class="sxs-lookup"><span data-stu-id="3ad53-155">Microsoft.Azure.Commands.Sql.ThreatDetection.Model.DetectionType[]</span></span>

### <span data-ttu-id="3ad53-156">System.Nullable'1[[System.UInt32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="3ad53-156">System.Nullable\`1[[System.UInt32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="3ad53-157">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="3ad53-157">OUTPUTS</span></span>

### <span data-ttu-id="3ad53-158">Microsoft.Azure.Commands.Sql.ThreatDetection.Model.DatabaseThreatDetectionsettingsModel</span><span class="sxs-lookup"><span data-stu-id="3ad53-158">Microsoft.Azure.Commands.Sql.ThreatDetection.Model.DatabaseThreatDetectionsettingsModel</span></span>

## <span data-ttu-id="3ad53-159">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="3ad53-159">NOTES</span></span>

## <span data-ttu-id="3ad53-160">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="3ad53-160">RELATED LINKS</span></span>

[<span data-ttu-id="3ad53-161">SQL Datenbankdokumentation</span><span class="sxs-lookup"><span data-stu-id="3ad53-161">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
