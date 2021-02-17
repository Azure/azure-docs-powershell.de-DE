---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 2B82F5BA-ABC6-4B37-B641-353CFE814290
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/set-azsqlserverthreatdetectionpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlServerThreatDetectionPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlServerThreatDetectionPolicy.md
ms.openlocfilehash: 49b484c17b595a8f676a089f8627b70a1f34c471
ms.sourcegitcommit: 0c61b7f42dec507e576c92e0a516c6655e9f50fc
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/14/2021
ms.locfileid: "100399497"
---
# <span data-ttu-id="6a8e4-101">Set-AzSqlServerThreatDetectionPolicy</span><span class="sxs-lookup"><span data-stu-id="6a8e4-101">Set-AzSqlServerThreatDetectionPolicy</span></span>

## <span data-ttu-id="6a8e4-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6a8e4-102">SYNOPSIS</span></span>
<span data-ttu-id="6a8e4-103">Legt eine Bedrohungserkennungsrichtlinie auf einem Server fest.</span><span class="sxs-lookup"><span data-stu-id="6a8e4-103">Sets a threat detection policy on a server.</span></span>

## <span data-ttu-id="6a8e4-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="6a8e4-104">SYNTAX</span></span>

```
Set-AzSqlServerThreatDetectionPolicy [-PassThru] [-NotificationRecipientsEmails <String>]
 [-EmailAdmins <Boolean>] [-ExcludedDetectionType <String[]>] [-StorageAccountName <String>]
 [-RetentionInDays <UInt32>] -ServerName <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6a8e4-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="6a8e4-105">DESCRIPTION</span></span>
<span data-ttu-id="6a8e4-106">Das **Cmdlet Set-AzSqlServerThreatDetectionPolicy** legt eine Bedrohungserkennungsrichtlinie für einen Azure SQL fest.</span><span class="sxs-lookup"><span data-stu-id="6a8e4-106">The **Set-AzSqlServerThreatDetectionPolicy** cmdlet sets a threat detection policy on an Azure SQL server.</span></span>
<span data-ttu-id="6a8e4-107">Um die Bedrohungserkennung auf einem Server zu aktivieren, muss eine Überwachungsrichtlinie auf diesem Server aktiviert sein.</span><span class="sxs-lookup"><span data-stu-id="6a8e4-107">In order to enable threat detection on a server an auditing policy must be enabled on that server.</span></span>
<span data-ttu-id="6a8e4-108">Um dieses Cmdlet zu verwenden, geben Sie die *Parameter "ResourceGroupName"* und "ServerName" an, um den Server zu identifizieren.</span><span class="sxs-lookup"><span data-stu-id="6a8e4-108">To use this cmdlet, specify the *ResourceGroupName* and ServerName parameters to identify the server.</span></span>

## <span data-ttu-id="6a8e4-109">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="6a8e4-109">EXAMPLES</span></span>

### <span data-ttu-id="6a8e4-110">Beispiel 1: Festlegen der Bedrohungserkennungsrichtlinie für eine Datenbank</span><span class="sxs-lookup"><span data-stu-id="6a8e4-110">Example 1: Set the threat detection policy for a database</span></span>
```
PS C:\>Set-AzSqlServerThreatDetectionPolicy -ResourceGroupName "ResourceGroup11" -ServerName "Server01" -NotificationRecipientsEmails "admin01@contoso.com;secadmin@contoso.com" -EmailAdmins $False -ExcludedDetectionType "Sql_Injection_Vulnerability","SQL_Injection" -StorageAccountName "mystorageAccount"
```

<span data-ttu-id="6a8e4-111">Dieser Befehl legt die Bedrohungserkennungsrichtlinie für einen Server mit dem Namen Server01 fest.</span><span class="sxs-lookup"><span data-stu-id="6a8e4-111">This command sets the threat detection policy for a server named Server01.</span></span>

## <span data-ttu-id="6a8e4-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="6a8e4-112">PARAMETERS</span></span>

### <span data-ttu-id="6a8e4-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6a8e4-113">-DefaultProfile</span></span>
<span data-ttu-id="6a8e4-114">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden</span><span class="sxs-lookup"><span data-stu-id="6a8e4-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="6a8e4-115">-EmailAdmins</span><span class="sxs-lookup"><span data-stu-id="6a8e4-115">-EmailAdmins</span></span>
<span data-ttu-id="6a8e4-116">Gibt an, ob die Bedrohungserkennungsrichtlinie mithilfe von E-Mail Kontakt zu Administratoren hat.</span><span class="sxs-lookup"><span data-stu-id="6a8e4-116">Specifies whether the threat detection policy contacts administrators by using email.</span></span>

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

### <span data-ttu-id="6a8e4-117">-ExcludedDetectionType</span><span class="sxs-lookup"><span data-stu-id="6a8e4-117">-ExcludedDetectionType</span></span>
<span data-ttu-id="6a8e4-118">Gibt ein Array von Erkennungstypen an, die aus der Richtlinie ausgeschlossen werden.</span><span class="sxs-lookup"><span data-stu-id="6a8e4-118">Specifies an array of detection types to exclude from the policy.</span></span>
<span data-ttu-id="6a8e4-119">Die zulässigen Werte für diesen Parameter sind:</span><span class="sxs-lookup"><span data-stu-id="6a8e4-119">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="6a8e4-120">Sql_Injection</span><span class="sxs-lookup"><span data-stu-id="6a8e4-120">Sql_Injection</span></span>
- <span data-ttu-id="6a8e4-121">Sql_Injection_Vulnerability</span><span class="sxs-lookup"><span data-stu-id="6a8e4-121">Sql_Injection_Vulnerability</span></span>
- <span data-ttu-id="6a8e4-122">Access_Anomaly</span><span class="sxs-lookup"><span data-stu-id="6a8e4-122">Access_Anomaly</span></span>
- <span data-ttu-id="6a8e4-123">Keine</span><span class="sxs-lookup"><span data-stu-id="6a8e4-123">None</span></span>

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

### <span data-ttu-id="6a8e4-124">-NotificationRecipientsEmails</span><span class="sxs-lookup"><span data-stu-id="6a8e4-124">-NotificationRecipientsEmails</span></span>
<span data-ttu-id="6a8e4-125">Gibt eine durch Semikolons getrennte Liste der E-Mail-Adressen an, an die die Richtlinie Benachrichtigungen sendet.</span><span class="sxs-lookup"><span data-stu-id="6a8e4-125">Specifies a semicolon-separated list of email addresses to which the policy sends alerts.</span></span>

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

### <span data-ttu-id="6a8e4-126">-PassThru</span><span class="sxs-lookup"><span data-stu-id="6a8e4-126">-PassThru</span></span>
<span data-ttu-id="6a8e4-127">Gibt ein Objekt zurück, das das Element darstellt, mit dem Sie arbeiten.</span><span class="sxs-lookup"><span data-stu-id="6a8e4-127">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="6a8e4-128">Standardmäßig generiert dieses Cmdlet keine Ausgabe.</span><span class="sxs-lookup"><span data-stu-id="6a8e4-128">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="6a8e4-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6a8e4-129">-ResourceGroupName</span></span>
<span data-ttu-id="6a8e4-130">Gibt den Namen der Ressourcengruppe an, zu der der Server gehört.</span><span class="sxs-lookup"><span data-stu-id="6a8e4-130">Specifies the name of the resource group to which the server belongs.</span></span>

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

### <span data-ttu-id="6a8e4-131">-RetentionInDays</span><span class="sxs-lookup"><span data-stu-id="6a8e4-131">-RetentionInDays</span></span>
<span data-ttu-id="6a8e4-132">Die Anzahl der Aufbewahrungstage für die Überwachungsprotokolle</span><span class="sxs-lookup"><span data-stu-id="6a8e4-132">The number of retention days for the audit logs</span></span>

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

### <span data-ttu-id="6a8e4-133">-ServerName</span><span class="sxs-lookup"><span data-stu-id="6a8e4-133">-ServerName</span></span>
<span data-ttu-id="6a8e4-134">Gibt den Namen des Servers an.</span><span class="sxs-lookup"><span data-stu-id="6a8e4-134">Specifies the name of the server.</span></span>

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

### <span data-ttu-id="6a8e4-135">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="6a8e4-135">-StorageAccountName</span></span>
<span data-ttu-id="6a8e4-136">Gibt den Namen des zu verwendenden Speicherkontos an.</span><span class="sxs-lookup"><span data-stu-id="6a8e4-136">Specifies the name of the storage account to be used.</span></span> <span data-ttu-id="6a8e4-137">Platzhalter sind nicht zulässig.</span><span class="sxs-lookup"><span data-stu-id="6a8e4-137">Wildcards are not permitted.</span></span> <span data-ttu-id="6a8e4-138">Dieser Parameter ist nicht erforderlich.</span><span class="sxs-lookup"><span data-stu-id="6a8e4-138">This parameter is not required.</span></span> <span data-ttu-id="6a8e4-139">Wenn dieser Parameter nicht bereitgestellt wird, verwendet das Cmdlet das Speicherkonto, das zuvor als Teil der Bedrohungserkennungsrichtlinie der Datenbank definiert wurde.</span><span class="sxs-lookup"><span data-stu-id="6a8e4-139">When this parameter is not provided, the cmdlet will use the storage account that was defined previously as part of the threat detection policy of the database.</span></span> <span data-ttu-id="6a8e4-140">Wenn dies das erste Mal ist, dass eine Datenbank theat-Erkennungsrichtlinie definiert wird und dieser Parameter nicht bereitgestellt wird, kann das Cmdlet nicht verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="6a8e4-140">If this is the first time a database theat detection policy is defined and this parameter is not provided, the cmdlet will fail.</span></span>

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

### <span data-ttu-id="6a8e4-141">-Confirm</span><span class="sxs-lookup"><span data-stu-id="6a8e4-141">-Confirm</span></span>
<span data-ttu-id="6a8e4-142">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="6a8e4-142">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6a8e4-143">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="6a8e4-143">-WhatIf</span></span>
<span data-ttu-id="6a8e4-144">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="6a8e4-144">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6a8e4-145">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="6a8e4-145">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6a8e4-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6a8e4-146">CommonParameters</span></span>
<span data-ttu-id="6a8e4-147">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6a8e4-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6a8e4-148">Weitere Informationen finden Sie unter [about_CommonParameters.](https://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="6a8e4-148">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6a8e4-149">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="6a8e4-149">INPUTS</span></span>

### <span data-ttu-id="6a8e4-150">System.String</span><span class="sxs-lookup"><span data-stu-id="6a8e4-150">System.String</span></span>

### <span data-ttu-id="6a8e4-151">System.Nullable'1[[System.Boolean, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="6a8e4-151">System.Nullable\`1[[System.Boolean, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="6a8e4-152">Microsoft.Azure.Commands.Sql.ThreatDetection.Model.DetectionType[]</span><span class="sxs-lookup"><span data-stu-id="6a8e4-152">Microsoft.Azure.Commands.Sql.ThreatDetection.Model.DetectionType[]</span></span>

### <span data-ttu-id="6a8e4-153">System.Nullable'1[[System.UInt32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="6a8e4-153">System.Nullable\`1[[System.UInt32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="6a8e4-154">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="6a8e4-154">OUTPUTS</span></span>

### <span data-ttu-id="6a8e4-155">Microsoft.Azure.Commands.Sql.ThreatDetection.Model.ServerThreatDetectionPolicyModel</span><span class="sxs-lookup"><span data-stu-id="6a8e4-155">Microsoft.Azure.Commands.Sql.ThreatDetection.Model.ServerThreatDetectionPolicyModel</span></span>

## <span data-ttu-id="6a8e4-156">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="6a8e4-156">NOTES</span></span>

## <span data-ttu-id="6a8e4-157">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="6a8e4-157">RELATED LINKS</span></span>

[<span data-ttu-id="6a8e4-158">Get-AzSqlServerThreatDetectionPolicy</span><span class="sxs-lookup"><span data-stu-id="6a8e4-158">Get-AzSqlServerThreatDetectionPolicy</span></span>](./Get-AzSqlServerThreatDetectionPolicy.md)

[<span data-ttu-id="6a8e4-159">SQL Datenbankdokumentation</span><span class="sxs-lookup"><span data-stu-id="6a8e4-159">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
