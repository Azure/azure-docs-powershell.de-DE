---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 2B82F5BA-ABC6-4B37-B641-353CFE814290
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/Update-AzSqlServerAdvancedThreatProtectionSettings
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Update-AzSqlServerAdvancedThreatProtectionSettings.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Update-AzSqlServerAdvancedThreatProtectionSettings.md
ms.openlocfilehash: 0567454db7421e47faa6690a5c4ad698287ada6a
ms.sourcegitcommit: 0c61b7f42dec507e576c92e0a516c6655e9f50fc
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/14/2021
ms.locfileid: "100413318"
---
# <span data-ttu-id="065f9-101">Update-AzSqlServerAdvancedThreatProtectionSettings</span><span class="sxs-lookup"><span data-stu-id="065f9-101">Update-AzSqlServerAdvancedThreatProtectionSettings</span></span>

## <span data-ttu-id="065f9-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="065f9-102">SYNOPSIS</span></span>
<span data-ttu-id="065f9-103">Legt eine erweiterte Threat Protection-Einstellung auf einem Server fest.</span><span class="sxs-lookup"><span data-stu-id="065f9-103">Sets a advanced threat protection settings on a server.</span></span>

## <span data-ttu-id="065f9-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="065f9-104">SYNTAX</span></span>

```
Update-AzSqlServerAdvancedThreatProtectionSettings [-PassThru] [-NotificationRecipientsEmails <String>]
 [-EmailAdmins <Boolean>] [-ExcludedDetectionType <String[]>] [-StorageAccountName <String>]
 [-RetentionInDays <UInt32>] -ServerName <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="065f9-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="065f9-105">DESCRIPTION</span></span>
<span data-ttu-id="065f9-106">Das **Cmdlet "Update-AzSqlServerAdvancedThreatProtectionSettings"** legt eine erweiterte Threat Protection-Einstellung auf einem Azure SQL fest.</span><span class="sxs-lookup"><span data-stu-id="065f9-106">The **Update-AzSqlServerAdvancedThreatProtectionSettings** cmdlet sets a advanced threat protection settings on an Azure SQL server.</span></span>
<span data-ttu-id="065f9-107">Um advanced Threat Protection auf einem Server zu aktivieren, müssen auf diesem Server Überwachungseinstellungen aktiviert sein.</span><span class="sxs-lookup"><span data-stu-id="065f9-107">In order to enable advanced threat protection on a server an auditing settings must be enabled on that server.</span></span>
<span data-ttu-id="065f9-108">Um dieses Cmdlet zu verwenden, geben Sie die *Parameter "ResourceGroupName"* und "ServerName" an, um den Server zu identifizieren.</span><span class="sxs-lookup"><span data-stu-id="065f9-108">To use this cmdlet, specify the *ResourceGroupName* and ServerName parameters to identify the server.</span></span>

## <span data-ttu-id="065f9-109">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="065f9-109">EXAMPLES</span></span>

### <span data-ttu-id="065f9-110">Beispiel 1: Festlegen der erweiterten Threat Protection-Einstellungen für eine Datenbank</span><span class="sxs-lookup"><span data-stu-id="065f9-110">Example 1: Set the advanced threat protection settings for a database</span></span>
```
PS C:\>Update-AzSqlServerAdvancedThreatProtectionSettings -ResourceGroupName "ResourceGroup11" -ServerName "Server01" -NotificationRecipientsEmails "admin01@contoso.com;secadmin@contoso.com" -EmailAdmins $False -ExcludedDetectionType "Sql_Injection_Vulnerability","SQL_Injection" -StorageAccountName "mystorageAccount"
```

<span data-ttu-id="065f9-111">Mit diesem Befehl werden die erweiterten Threat Protection-Einstellungen für einen Server namens Server01 festgelegt.</span><span class="sxs-lookup"><span data-stu-id="065f9-111">This command sets the advanced threat protection settings for a server named Server01.</span></span>

## <span data-ttu-id="065f9-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="065f9-112">PARAMETERS</span></span>

### <span data-ttu-id="065f9-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="065f9-113">-DefaultProfile</span></span>
<span data-ttu-id="065f9-114">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden</span><span class="sxs-lookup"><span data-stu-id="065f9-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="065f9-115">-EmailAdmins</span><span class="sxs-lookup"><span data-stu-id="065f9-115">-EmailAdmins</span></span>
<span data-ttu-id="065f9-116">Gibt an, ob die erweiterten Threat Protection-Einstellungen mithilfe von E-Mail Kontakt zu Administratoren haben.</span><span class="sxs-lookup"><span data-stu-id="065f9-116">Specifies whether the advanced threat protection settings contacts administrators by using email.</span></span>

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

### <span data-ttu-id="065f9-117">-ExcludedDetectionType</span><span class="sxs-lookup"><span data-stu-id="065f9-117">-ExcludedDetectionType</span></span>
<span data-ttu-id="065f9-118">Gibt ein Array von Erkennungstypen an, die aus den Einstellungen ausgeschlossen werden.</span><span class="sxs-lookup"><span data-stu-id="065f9-118">Specifies an array of detection types to exclude from the settings.</span></span>
<span data-ttu-id="065f9-119">Die zulässigen Werte für diesen Parameter sind:</span><span class="sxs-lookup"><span data-stu-id="065f9-119">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="065f9-120">Sql_Injection</span><span class="sxs-lookup"><span data-stu-id="065f9-120">Sql_Injection</span></span>
- <span data-ttu-id="065f9-121">Sql_Injection_Vulnerability</span><span class="sxs-lookup"><span data-stu-id="065f9-121">Sql_Injection_Vulnerability</span></span>
- <span data-ttu-id="065f9-122">Access_Anomaly</span><span class="sxs-lookup"><span data-stu-id="065f9-122">Access_Anomaly</span></span>
- <span data-ttu-id="065f9-123">Keine</span><span class="sxs-lookup"><span data-stu-id="065f9-123">None</span></span>

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

### <span data-ttu-id="065f9-124">-NotificationRecipientsEmails</span><span class="sxs-lookup"><span data-stu-id="065f9-124">-NotificationRecipientsEmails</span></span>
<span data-ttu-id="065f9-125">Gibt eine durch Semikolons getrennte Liste von E-Mail-Adressen an, an die die Einstellungen Benachrichtigungen senden.</span><span class="sxs-lookup"><span data-stu-id="065f9-125">Specifies a semicolon-separated list of email addresses to which the settings sends alerts.</span></span>

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

### <span data-ttu-id="065f9-126">-PassThru</span><span class="sxs-lookup"><span data-stu-id="065f9-126">-PassThru</span></span>
<span data-ttu-id="065f9-127">Gibt ein Objekt zurück, das das Element darstellt, mit dem Sie arbeiten.</span><span class="sxs-lookup"><span data-stu-id="065f9-127">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="065f9-128">Standardmäßig generiert dieses Cmdlet keine Ausgabe.</span><span class="sxs-lookup"><span data-stu-id="065f9-128">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="065f9-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="065f9-129">-ResourceGroupName</span></span>
<span data-ttu-id="065f9-130">Gibt den Namen der Ressourcengruppe an, zu der der Server gehört.</span><span class="sxs-lookup"><span data-stu-id="065f9-130">Specifies the name of the resource group to which the server belongs.</span></span>

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

### <span data-ttu-id="065f9-131">-RetentionInDays</span><span class="sxs-lookup"><span data-stu-id="065f9-131">-RetentionInDays</span></span>
<span data-ttu-id="065f9-132">Die Anzahl der Aufbewahrungstage für die Überwachungsprotokolle</span><span class="sxs-lookup"><span data-stu-id="065f9-132">The number of retention days for the audit logs</span></span>

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

### <span data-ttu-id="065f9-133">-ServerName</span><span class="sxs-lookup"><span data-stu-id="065f9-133">-ServerName</span></span>
<span data-ttu-id="065f9-134">Gibt den Namen des Servers an.</span><span class="sxs-lookup"><span data-stu-id="065f9-134">Specifies the name of the server.</span></span>

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

### <span data-ttu-id="065f9-135">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="065f9-135">-StorageAccountName</span></span>
<span data-ttu-id="065f9-136">Gibt den Namen des zu verwendenden Speicherkontos an.</span><span class="sxs-lookup"><span data-stu-id="065f9-136">Specifies the name of the storage account to be used.</span></span> <span data-ttu-id="065f9-137">Platzhalter sind nicht zulässig.</span><span class="sxs-lookup"><span data-stu-id="065f9-137">Wildcards are not permitted.</span></span> <span data-ttu-id="065f9-138">Dieser Parameter ist nicht erforderlich.</span><span class="sxs-lookup"><span data-stu-id="065f9-138">This parameter is not required.</span></span> <span data-ttu-id="065f9-139">Wenn dieser Parameter nicht bereitgestellt wird, verwendet das Cmdlet das Speicherkonto, das zuvor als Teil der erweiterten Threat Protection-Einstellungen der Datenbank definiert wurde.</span><span class="sxs-lookup"><span data-stu-id="065f9-139">When this parameter is not provided, the cmdlet will use the storage account that was defined previously as part of the advanced threat protection settings of the database.</span></span> <span data-ttu-id="065f9-140">Wenn dies das erste Mal ist, dass einstellungen für die Erkennung von Datenbankbedrohungen definiert werden und dieser Parameter nicht bereitgestellt wird, kann das Cmdlet nicht verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="065f9-140">If this is the first time a database threat detection settings is defined and this parameter is not provided, the cmdlet will fail.</span></span>

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

### <span data-ttu-id="065f9-141">-Confirm</span><span class="sxs-lookup"><span data-stu-id="065f9-141">-Confirm</span></span>
<span data-ttu-id="065f9-142">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="065f9-142">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="065f9-143">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="065f9-143">-WhatIf</span></span>
<span data-ttu-id="065f9-144">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="065f9-144">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="065f9-145">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="065f9-145">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="065f9-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="065f9-146">CommonParameters</span></span>
<span data-ttu-id="065f9-147">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="065f9-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="065f9-148">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="065f9-148">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="065f9-149">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="065f9-149">INPUTS</span></span>

### <span data-ttu-id="065f9-150">System.String</span><span class="sxs-lookup"><span data-stu-id="065f9-150">System.String</span></span>

### <span data-ttu-id="065f9-151">System.Nullable'1[[System.Boolean, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="065f9-151">System.Nullable\`1[[System.Boolean, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="065f9-152">Microsoft.Azure.Commands.Sql.ThreatDetection.Model.DetectionType[]</span><span class="sxs-lookup"><span data-stu-id="065f9-152">Microsoft.Azure.Commands.Sql.ThreatDetection.Model.DetectionType[]</span></span>

### <span data-ttu-id="065f9-153">System.Nullable'1[[System.UInt32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="065f9-153">System.Nullable\`1[[System.UInt32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="065f9-154">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="065f9-154">OUTPUTS</span></span>

### <span data-ttu-id="065f9-155">Microsoft.Azure.Commands.Sql.ThreatDetection.Model.ServerThreatDetectionsettingsModel</span><span class="sxs-lookup"><span data-stu-id="065f9-155">Microsoft.Azure.Commands.Sql.ThreatDetection.Model.ServerThreatDetectionsettingsModel</span></span>

## <span data-ttu-id="065f9-156">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="065f9-156">NOTES</span></span>

## <span data-ttu-id="065f9-157">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="065f9-157">RELATED LINKS</span></span>

[<span data-ttu-id="065f9-158">SQL Datenbankdokumentation</span><span class="sxs-lookup"><span data-stu-id="065f9-158">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
