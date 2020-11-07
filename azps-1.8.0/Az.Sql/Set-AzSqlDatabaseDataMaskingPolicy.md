---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 1B138185-E836-414F-93CD-7BAE7F474E73
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/set-azsqldatabasedatamaskingpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlDatabaseDataMaskingPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlDatabaseDataMaskingPolicy.md
ms.openlocfilehash: e0af0c6d741e45c2e00e958342fad940acc2c3e0
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93659004"
---
# <span data-ttu-id="a78ac-101">Set-AzSqlDatabaseDataMaskingPolicy</span><span class="sxs-lookup"><span data-stu-id="a78ac-101">Set-AzSqlDatabaseDataMaskingPolicy</span></span>

## <span data-ttu-id="a78ac-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="a78ac-102">SYNOPSIS</span></span>
<span data-ttu-id="a78ac-103">Legt die Daten Maskierung für eine Datenbank fest.</span><span class="sxs-lookup"><span data-stu-id="a78ac-103">Sets data masking for a database.</span></span>

## <span data-ttu-id="a78ac-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="a78ac-104">SYNTAX</span></span>

```
Set-AzSqlDatabaseDataMaskingPolicy [-PassThru] [-PrivilegedUsers <String>] [-DataMaskingState <String>]
 [-ServerName] <String> [-DatabaseName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a78ac-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="a78ac-105">DESCRIPTION</span></span>
<span data-ttu-id="a78ac-106">Das Cmdlet " **Set-AzSqlDatabaseDataMaskingPolicy** " legt die Daten Maskierungs Richtlinie für eine Azure SQL-Datenbank fest.</span><span class="sxs-lookup"><span data-stu-id="a78ac-106">The **Set-AzSqlDatabaseDataMaskingPolicy** cmdlet sets the data masking policy for an Azure SQL database.</span></span>
<span data-ttu-id="a78ac-107">Um dieses Cmdlet zu verwenden, verwenden Sie die Parameter *ResourceGroupName* , *Servername* und *DatabaseName* , um die Datenbank zu identifizieren.</span><span class="sxs-lookup"><span data-stu-id="a78ac-107">To use this cmdlet, use the *ResourceGroupName* , *ServerName* , and *DatabaseName* parameters to identify the database.</span></span>
<span data-ttu-id="a78ac-108">Sie können den *DataMaskingState* -Parameter festlegen, um anzugeben, ob Daten Maskierungs Vorgänge aktiviert oder deaktiviert werden sollen.</span><span class="sxs-lookup"><span data-stu-id="a78ac-108">You can set the *DataMaskingState* parameter to specify whether data masking operations are enabled or disabled.</span></span>
<span data-ttu-id="a78ac-109">Wenn das Cmdlet erfolgreich ausgeführt wird und der *passthru* -Parameter verwendet wird, gibt es zusätzlich zu den Datenbankbezeichnern ein Objekt zurück, das die aktuelle Daten Maskierungs Richtlinie beschreibt.</span><span class="sxs-lookup"><span data-stu-id="a78ac-109">If the cmdlet succeeds and the *PassThru* parameter is used, it returns an object describing the current data masking policy in addition to the database identifiers.</span></span>
<span data-ttu-id="a78ac-110">Zu den Datenbankbezeichnern gehören **ResourceGroupName** , **Servername** und **DatabaseName** , sind aber nicht darauf limitiert.</span><span class="sxs-lookup"><span data-stu-id="a78ac-110">Database identifiers include, but are not limited to, **ResourceGroupName** , **ServerName** , and **DatabaseName**.</span></span>
<span data-ttu-id="a78ac-111">Dieses Cmdlet wird auch vom SQL Server Stretch-Datenbankdienst auf Azure unterstützt.</span><span class="sxs-lookup"><span data-stu-id="a78ac-111">This cmdlet is also supported by the SQL Server Stretch Database service on Azure.</span></span>

## <span data-ttu-id="a78ac-112">Beispiele</span><span class="sxs-lookup"><span data-stu-id="a78ac-112">EXAMPLES</span></span>

### <span data-ttu-id="a78ac-113">Beispiel 1: Festlegen der Daten Maskierungs Richtlinie für eine Datenbank</span><span class="sxs-lookup"><span data-stu-id="a78ac-113">Example 1: Set the data masking policy for a database</span></span>
```
PS C:\>Set-AzSqlDatabaseDataMaskingPolicy -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01 -PrivilegedUsers "public" -DataMaskingState "Enabled"
```

<span data-ttu-id="a78ac-114">Mit diesem Befehl wird die Daten Maskierungs Richtlinie für eine Datenbank mit dem Namen "database01" auf dem Server mit dem Namen "Server01" festgelegt.</span><span class="sxs-lookup"><span data-stu-id="a78ac-114">This command sets the data masking policy for a database named database01 on the server named server01.</span></span>

## <span data-ttu-id="a78ac-115">Parameter</span><span class="sxs-lookup"><span data-stu-id="a78ac-115">PARAMETERS</span></span>

### <span data-ttu-id="a78ac-116">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="a78ac-116">-DatabaseName</span></span>
<span data-ttu-id="a78ac-117">Gibt den Namen der Datenbank an, in der die Richtlinie festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="a78ac-117">Specifies the name of the database where the policy is set.</span></span>

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

### <span data-ttu-id="a78ac-118">-DataMaskingState</span><span class="sxs-lookup"><span data-stu-id="a78ac-118">-DataMaskingState</span></span>
<span data-ttu-id="a78ac-119">Gibt an, ob der Daten Maskierungs Vorgang aktiviert oder deaktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="a78ac-119">Specifies whether data masking operation is enabled or disabled.</span></span>
<span data-ttu-id="a78ac-120">Die zulässigen Werte für diesen Parameter lauten wie folgt:</span><span class="sxs-lookup"><span data-stu-id="a78ac-120">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="a78ac-121">Aktiviert</span><span class="sxs-lookup"><span data-stu-id="a78ac-121">Enabled</span></span>
- <span data-ttu-id="a78ac-122">Deaktiviert der Standardwert ist aktiviert.</span><span class="sxs-lookup"><span data-stu-id="a78ac-122">Disabled The default value is Enabled.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Enabled, Disabled

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a78ac-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a78ac-123">-DefaultProfile</span></span>
<span data-ttu-id="a78ac-124">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="a78ac-124">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="a78ac-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="a78ac-125">-PassThru</span></span>
<span data-ttu-id="a78ac-126">Gibt ein Objekt zurück, das das Element darstellt, mit dem Sie arbeiten.</span><span class="sxs-lookup"><span data-stu-id="a78ac-126">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="a78ac-127">Standardmäßig wird mit diesem Cmdlet keine Ausgabe generiert.</span><span class="sxs-lookup"><span data-stu-id="a78ac-127">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="a78ac-128">-PrivilegedUsers</span><span class="sxs-lookup"><span data-stu-id="a78ac-128">-PrivilegedUsers</span></span>
<span data-ttu-id="a78ac-129">Gibt eine durch Semikolons getrennte Liste mit privilegierten Benutzer-IDs an.</span><span class="sxs-lookup"><span data-stu-id="a78ac-129">Specifies a semicolon-separated list of privileged user IDs.</span></span>
<span data-ttu-id="a78ac-130">Diesen Benutzern ist es gestattet, die Maskierungs Daten anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="a78ac-130">These users are allowed to view the masking data.</span></span>

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

### <span data-ttu-id="a78ac-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a78ac-131">-ResourceGroupName</span></span>
<span data-ttu-id="a78ac-132">Gibt den Namen der Ressourcengruppe an, der die Datenbank zugewiesen ist.</span><span class="sxs-lookup"><span data-stu-id="a78ac-132">Specifies the name of the resource group to which the database is assigned.</span></span>

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

### <span data-ttu-id="a78ac-133">-Servername</span><span class="sxs-lookup"><span data-stu-id="a78ac-133">-ServerName</span></span>
<span data-ttu-id="a78ac-134">Gibt den Namen des Servers an, der die Datenbank hostet.</span><span class="sxs-lookup"><span data-stu-id="a78ac-134">Specifies the name of the server hosting the database.</span></span>

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

### <span data-ttu-id="a78ac-135">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="a78ac-135">-Confirm</span></span>
<span data-ttu-id="a78ac-136">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="a78ac-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a78ac-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a78ac-137">-WhatIf</span></span>
<span data-ttu-id="a78ac-138">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="a78ac-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a78ac-139">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="a78ac-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a78ac-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a78ac-140">CommonParameters</span></span>
<span data-ttu-id="a78ac-141">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a78ac-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a78ac-142">Weitere Informationen finden Sie unter [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="a78ac-142">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a78ac-143">Eingaben</span><span class="sxs-lookup"><span data-stu-id="a78ac-143">INPUTS</span></span>

### <span data-ttu-id="a78ac-144">System. String</span><span class="sxs-lookup"><span data-stu-id="a78ac-144">System.String</span></span>

## <span data-ttu-id="a78ac-145">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="a78ac-145">OUTPUTS</span></span>

### <span data-ttu-id="a78ac-146">Microsoft. Azure. Commands. SQL. datamasking. Model. DatabaseDataMaskingPolicyModel</span><span class="sxs-lookup"><span data-stu-id="a78ac-146">Microsoft.Azure.Commands.Sql.DataMasking.Model.DatabaseDataMaskingPolicyModel</span></span>

## <span data-ttu-id="a78ac-147">Notizen</span><span class="sxs-lookup"><span data-stu-id="a78ac-147">NOTES</span></span>

## <span data-ttu-id="a78ac-148">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="a78ac-148">RELATED LINKS</span></span>

[<span data-ttu-id="a78ac-149">Get-AzSqlDatabaseDataMaskingPolicy</span><span class="sxs-lookup"><span data-stu-id="a78ac-149">Get-AzSqlDatabaseDataMaskingPolicy</span></span>](./Get-AzSqlDatabaseDataMaskingPolicy.md)

[<span data-ttu-id="a78ac-150">Get-AzSqlDatabaseDataMaskingRule</span><span class="sxs-lookup"><span data-stu-id="a78ac-150">Get-AzSqlDatabaseDataMaskingRule</span></span>](./Get-AzSqlDatabaseDataMaskingRule.md)

[<span data-ttu-id="a78ac-151">Neu – AzSqlDatabaseDataMaskingRule</span><span class="sxs-lookup"><span data-stu-id="a78ac-151">New-AzSqlDatabaseDataMaskingRule</span></span>](./New-AzSqlDatabaseDataMaskingRule.md)

[<span data-ttu-id="a78ac-152">Remove-AzSqlDatabaseDataMaskingRule</span><span class="sxs-lookup"><span data-stu-id="a78ac-152">Remove-AzSqlDatabaseDataMaskingRule</span></span>](./Remove-AzSqlDatabaseDataMaskingRule.md)

[<span data-ttu-id="a78ac-153">Satz-AzSqlDatabaseDataMaskingRule</span><span class="sxs-lookup"><span data-stu-id="a78ac-153">Set-AzSqlDatabaseDataMaskingRule</span></span>](./Set-AzSqlDatabaseDataMaskingRule.md)

[<span data-ttu-id="a78ac-154">SQL-Datenbank-Dokumentation</span><span class="sxs-lookup"><span data-stu-id="a78ac-154">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)


