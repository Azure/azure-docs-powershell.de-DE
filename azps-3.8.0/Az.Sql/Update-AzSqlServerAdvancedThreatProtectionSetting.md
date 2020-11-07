---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 2B82F5BA-ABC6-4B37-B641-353CFE814290
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/Update-AzSqlServerAdvancedThreatProtectionSetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Update-AzSqlServerAdvancedThreatProtectionSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Update-AzSqlServerAdvancedThreatProtectionSetting.md
ms.openlocfilehash: 3ec370f0e4865ed5695e4f0890f99b50709e9ad8
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/21/2020
ms.locfileid: "93846444"
---
# <span data-ttu-id="5159a-101">Update-AzSqlServerAdvancedThreatProtectionSetting</span><span class="sxs-lookup"><span data-stu-id="5159a-101">Update-AzSqlServerAdvancedThreatProtectionSetting</span></span>

## <span data-ttu-id="5159a-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="5159a-102">SYNOPSIS</span></span>
<span data-ttu-id="5159a-103">Legt eine erweiterte Bedrohungsschutz Einstellung auf einem Server fest.</span><span class="sxs-lookup"><span data-stu-id="5159a-103">Sets a advanced threat protection settings on a server.</span></span>

## <span data-ttu-id="5159a-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="5159a-104">SYNTAX</span></span>

```
Update-AzSqlServerAdvancedThreatProtectionSetting [-PassThru] [-NotificationRecipientsEmails <String>]
 [-EmailAdmins <Boolean>] [-ExcludedDetectionType <String[]>] [-StorageAccountName <String>]
 [-RetentionInDays <UInt32>] -ServerName <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5159a-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="5159a-105">DESCRIPTION</span></span>
<span data-ttu-id="5159a-106">Das Cmdlet **Update-AzSqlServerAdvancedThreatProtectionSetting** legt eine erweiterte Bedrohungsschutz Einstellung auf einem Azure SQL Server fest.</span><span class="sxs-lookup"><span data-stu-id="5159a-106">The **Update-AzSqlServerAdvancedThreatProtectionSetting** cmdlet sets a advanced threat protection settings on an Azure SQL server.</span></span>
<span data-ttu-id="5159a-107">Um erweiterten Bedrohungsschutz auf einem Server zu aktivieren, müssen auf diesem Server Überwachungseinstellungen aktiviert sein.</span><span class="sxs-lookup"><span data-stu-id="5159a-107">In order to enable advanced threat protection on a server an auditing settings must be enabled on that server.</span></span>
<span data-ttu-id="5159a-108">Um dieses Cmdlet zu verwenden, geben Sie die Parameter *ResourceGroupName* und Servername an, um den Server zu identifizieren.</span><span class="sxs-lookup"><span data-stu-id="5159a-108">To use this cmdlet, specify the *ResourceGroupName* and ServerName parameters to identify the server.</span></span>

## <span data-ttu-id="5159a-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="5159a-109">EXAMPLES</span></span>

### <span data-ttu-id="5159a-110">Beispiel 1: Festlegen der erweiterten Bedrohungsschutz Einstellungen für eine Datenbank</span><span class="sxs-lookup"><span data-stu-id="5159a-110">Example 1: Set the advanced threat protection settings for a database</span></span>
```
PS C:\>Update-AzSqlServerAdvancedThreatProtectionSetting -ResourceGroupName "ResourceGroup11" -ServerName "Server01" -NotificationRecipientsEmails "admin01@contoso.com;secadmin@contoso.com" -EmailAdmins $False -ExcludedDetectionType "Sql_Injection_Vulnerability","SQL_Injection" -StorageAccountName "mystorageAccount"
```

<span data-ttu-id="5159a-111">Mit diesem Befehl werden die erweiterten Bedrohungsschutz Einstellungen für einen Server mit dem Namen "Server01" festgelegt.</span><span class="sxs-lookup"><span data-stu-id="5159a-111">This command sets the advanced threat protection settings for a server named Server01.</span></span>

## <span data-ttu-id="5159a-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="5159a-112">PARAMETERS</span></span>

### <span data-ttu-id="5159a-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5159a-113">-DefaultProfile</span></span>
<span data-ttu-id="5159a-114">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="5159a-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="5159a-115">-Emailadmins</span><span class="sxs-lookup"><span data-stu-id="5159a-115">-EmailAdmins</span></span>
<span data-ttu-id="5159a-116">Gibt an, ob die erweiterten Bedrohungsschutz Einstellungen mithilfe von e-Mail mit Administratoren Kontakt aufnehmen.</span><span class="sxs-lookup"><span data-stu-id="5159a-116">Specifies whether the advanced threat protection settings contacts administrators by using email.</span></span>

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

### <span data-ttu-id="5159a-117">-ExcludedDetectionType</span><span class="sxs-lookup"><span data-stu-id="5159a-117">-ExcludedDetectionType</span></span>
<span data-ttu-id="5159a-118">Gibt ein Array von Erkennungstypen an, die aus den Einstellungen ausgeschlossen werden sollen.</span><span class="sxs-lookup"><span data-stu-id="5159a-118">Specifies an array of detection types to exclude from the settings.</span></span>
<span data-ttu-id="5159a-119">Die zulässigen Werte für diesen Parameter lauten wie folgt:</span><span class="sxs-lookup"><span data-stu-id="5159a-119">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="5159a-120">Sql_Injection</span><span class="sxs-lookup"><span data-stu-id="5159a-120">Sql_Injection</span></span>
- <span data-ttu-id="5159a-121">Sql_Injection_Vulnerability</span><span class="sxs-lookup"><span data-stu-id="5159a-121">Sql_Injection_Vulnerability</span></span>
- <span data-ttu-id="5159a-122">Access_Anomaly</span><span class="sxs-lookup"><span data-stu-id="5159a-122">Access_Anomaly</span></span>
- <span data-ttu-id="5159a-123">Keine</span><span class="sxs-lookup"><span data-stu-id="5159a-123">None</span></span>

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

### <span data-ttu-id="5159a-124">-NotificationRecipientsEmails</span><span class="sxs-lookup"><span data-stu-id="5159a-124">-NotificationRecipientsEmails</span></span>
<span data-ttu-id="5159a-125">Gibt eine durch Semikolons getrennte Liste der e-Mail-Adressen an, an die die Einstellungen Benachrichtigungen senden.</span><span class="sxs-lookup"><span data-stu-id="5159a-125">Specifies a semicolon-separated list of email addresses to which the settings sends alerts.</span></span>

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

### <span data-ttu-id="5159a-126">-PassThru</span><span class="sxs-lookup"><span data-stu-id="5159a-126">-PassThru</span></span>
<span data-ttu-id="5159a-127">Gibt ein Objekt zurück, das das Element darstellt, mit dem Sie arbeiten.</span><span class="sxs-lookup"><span data-stu-id="5159a-127">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="5159a-128">Standardmäßig wird mit diesem Cmdlet keine Ausgabe generiert.</span><span class="sxs-lookup"><span data-stu-id="5159a-128">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="5159a-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5159a-129">-ResourceGroupName</span></span>
<span data-ttu-id="5159a-130">Gibt den Namen der Ressourcengruppe an, zu der der Server gehört.</span><span class="sxs-lookup"><span data-stu-id="5159a-130">Specifies the name of the resource group to which the server belongs.</span></span>

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

### <span data-ttu-id="5159a-131">-RetentionInDays</span><span class="sxs-lookup"><span data-stu-id="5159a-131">-RetentionInDays</span></span>
<span data-ttu-id="5159a-132">Die Anzahl der Aufbewahrungstage für die Überwachungsprotokolle</span><span class="sxs-lookup"><span data-stu-id="5159a-132">The number of retention days for the audit logs</span></span>

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

### <span data-ttu-id="5159a-133">-Servername</span><span class="sxs-lookup"><span data-stu-id="5159a-133">-ServerName</span></span>
<span data-ttu-id="5159a-134">Gibt den Namen des Servers an.</span><span class="sxs-lookup"><span data-stu-id="5159a-134">Specifies the name of the server.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5159a-135">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="5159a-135">-StorageAccountName</span></span>
<span data-ttu-id="5159a-136">Gibt den Namen des zu verwendenden speicherkontos an.</span><span class="sxs-lookup"><span data-stu-id="5159a-136">Specifies the name of the storage account to be used.</span></span> <span data-ttu-id="5159a-137">Platzhalter sind nicht zulässig.</span><span class="sxs-lookup"><span data-stu-id="5159a-137">Wildcards are not permitted.</span></span> <span data-ttu-id="5159a-138">Dieser Parameter ist nicht erforderlich.</span><span class="sxs-lookup"><span data-stu-id="5159a-138">This parameter is not required.</span></span> <span data-ttu-id="5159a-139">Wenn dieser Parameter nicht angegeben wird, verwendet das Cmdlet das Speicherkonto, das zuvor als Teil der erweiterten Bedrohungsschutz Einstellungen der Datenbank definiert wurde.</span><span class="sxs-lookup"><span data-stu-id="5159a-139">When this parameter is not provided, the cmdlet will use the storage account that was defined previously as part of the advanced threat protection settings of the database.</span></span> <span data-ttu-id="5159a-140">Wenn dies das erste Mal ist, dass eine Datenbank-Bedrohungs Erkennungseinstellungen definiert ist und dieser Parameter nicht angegeben wird, schlägt das Cmdlet fehl.</span><span class="sxs-lookup"><span data-stu-id="5159a-140">If this is the first time a database threat detection settings is defined and this parameter is not provided, the cmdlet will fail.</span></span>

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

### <span data-ttu-id="5159a-141">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="5159a-141">-Confirm</span></span>
<span data-ttu-id="5159a-142">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="5159a-142">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5159a-143">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5159a-143">-WhatIf</span></span>
<span data-ttu-id="5159a-144">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="5159a-144">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5159a-145">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="5159a-145">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5159a-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5159a-146">CommonParameters</span></span>
<span data-ttu-id="5159a-147">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5159a-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5159a-148">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="5159a-148">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5159a-149">Eingaben</span><span class="sxs-lookup"><span data-stu-id="5159a-149">INPUTS</span></span>

### <span data-ttu-id="5159a-150">System. String</span><span class="sxs-lookup"><span data-stu-id="5159a-150">System.String</span></span>

### <span data-ttu-id="5159a-151">System. Nullable ' 1 [[System. Boolean, System. private. CoreLib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="5159a-151">System.Nullable\`1[[System.Boolean, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="5159a-152">Microsoft. Azure. Commands. SQL. ThreatDetection. Model. detectiontype []</span><span class="sxs-lookup"><span data-stu-id="5159a-152">Microsoft.Azure.Commands.Sql.ThreatDetection.Model.DetectionType[]</span></span>

### <span data-ttu-id="5159a-153">System. Nullable ' 1 [[System. UInt32, System. private. CoreLib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="5159a-153">System.Nullable\`1[[System.UInt32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="5159a-154">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="5159a-154">OUTPUTS</span></span>

### <span data-ttu-id="5159a-155">Microsoft. Azure. Commands. SQL. ThreatDetection. Model. ServerThreatDetectionsettingsModel</span><span class="sxs-lookup"><span data-stu-id="5159a-155">Microsoft.Azure.Commands.Sql.ThreatDetection.Model.ServerThreatDetectionsettingsModel</span></span>

## <span data-ttu-id="5159a-156">Notizen</span><span class="sxs-lookup"><span data-stu-id="5159a-156">NOTES</span></span>

## <span data-ttu-id="5159a-157">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="5159a-157">RELATED LINKS</span></span>

[<span data-ttu-id="5159a-158">Get-AzSqlServerThreatDetectionsettings</span><span class="sxs-lookup"><span data-stu-id="5159a-158">Get-AzSqlServerThreatDetectionsettings</span></span>](./Get-AzSqlServerThreatDetectionsettings.md)

[<span data-ttu-id="5159a-159">Remove-AzSqlServerThreatDetectionsettings</span><span class="sxs-lookup"><span data-stu-id="5159a-159">Remove-AzSqlServerThreatDetectionsettings</span></span>](03e90cd1-6ae2-4134-bc5e-28cc080614c9)

[<span data-ttu-id="5159a-160">SQL-Datenbank-Dokumentation</span><span class="sxs-lookup"><span data-stu-id="5159a-160">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
