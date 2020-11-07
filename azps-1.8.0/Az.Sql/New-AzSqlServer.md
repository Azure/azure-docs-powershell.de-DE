---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 7039528F-42AE-45DB-BF81-FE5003F8AEE2
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/new-azsqlserver
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlServer.md
ms.openlocfilehash: 0d5eb08c938fe17e4270cd66038a738341937cb9
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93659091"
---
# <span data-ttu-id="708bb-101">New-AzSqlServer</span><span class="sxs-lookup"><span data-stu-id="708bb-101">New-AzSqlServer</span></span>

## <span data-ttu-id="708bb-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="708bb-102">SYNOPSIS</span></span>
<span data-ttu-id="708bb-103">Erstellt einen SQL-Datenbankserver.</span><span class="sxs-lookup"><span data-stu-id="708bb-103">Creates a SQL Database server.</span></span>

## <span data-ttu-id="708bb-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="708bb-104">SYNTAX</span></span>

```
New-AzSqlServer -ServerName <String> -SqlAdministratorCredentials <PSCredential> -Location <String>
 [-Tags <Hashtable>] [-ServerVersion <String>] [-AssignIdentity] [-AsJob] [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="708bb-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="708bb-105">DESCRIPTION</span></span>
<span data-ttu-id="708bb-106">Das Cmdlet **New-AzSqlServer** erstellt einen Azure SQL-Datenbankserver.</span><span class="sxs-lookup"><span data-stu-id="708bb-106">The **New-AzSqlServer** cmdlet creates an Azure SQL Database server.</span></span>

## <span data-ttu-id="708bb-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="708bb-107">EXAMPLES</span></span>

### <span data-ttu-id="708bb-108">Beispiel 1: Erstellen eines neuen Azure SQL-Datenbankservers</span><span class="sxs-lookup"><span data-stu-id="708bb-108">Example 1: Create a new Azure SQL Database server</span></span>
```
PS C:\>New-AzSqlServer -ResourceGroupName "ResourceGroup01" -Location "Central US" -ServerName "server01" -ServerVersion "12.0" -SqlAdministratorCredentials (Get-Credential)
ResourceGroupName        : resourcegroup01
ServerName               : server01
Location                 : Central US
SqlAdministratorLogin    : adminLogin
SqlAdministratorPassword :
ServerVersion            : 12.0
Tags                     :
```

<span data-ttu-id="708bb-109">Dieser Befehl erstellt einen Azure SQL-Datenbankserver der Version 12.</span><span class="sxs-lookup"><span data-stu-id="708bb-109">This command creates a version 12 Azure SQL Database server.</span></span>

## <span data-ttu-id="708bb-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="708bb-110">PARAMETERS</span></span>

### <span data-ttu-id="708bb-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="708bb-111">-AsJob</span></span>
<span data-ttu-id="708bb-112">Ausführen eines Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="708bb-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="708bb-113">-AssignIdentity</span><span class="sxs-lookup"><span data-stu-id="708bb-113">-AssignIdentity</span></span>
<span data-ttu-id="708bb-114">Sie können eine Azure Active Directory-Identität für diesen Server für die Verwendung mit Schlüssel Verwaltungsdiensten wie Azure keyvault generieren und zuweisen.</span><span class="sxs-lookup"><span data-stu-id="708bb-114">Generate and assign an Azure Active Directory Identity for this server for use with key management services like Azure KeyVault.</span></span>

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

### <span data-ttu-id="708bb-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="708bb-115">-DefaultProfile</span></span>
<span data-ttu-id="708bb-116">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="708bb-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="708bb-117">-Standort</span><span class="sxs-lookup"><span data-stu-id="708bb-117">-Location</span></span>
<span data-ttu-id="708bb-118">Gibt den Speicherort des Rechenzentrums an, in dem dieses Cmdlet den Server erstellt.</span><span class="sxs-lookup"><span data-stu-id="708bb-118">Specifies the location of the data center where this cmdlet creates the server.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="708bb-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="708bb-119">-ResourceGroupName</span></span>
<span data-ttu-id="708bb-120">Gibt den Namen der Ressourcengruppe an, der das Cmdlet den Server zuweist.</span><span class="sxs-lookup"><span data-stu-id="708bb-120">Specifies the name of the resource group to which this cmdlet assigns the server.</span></span>

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

### <span data-ttu-id="708bb-121">-Servername</span><span class="sxs-lookup"><span data-stu-id="708bb-121">-ServerName</span></span>
<span data-ttu-id="708bb-122">Gibt den Namen des neuen Servers an.</span><span class="sxs-lookup"><span data-stu-id="708bb-122">Specifies the name of the new server.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="708bb-123">-Server Version vom</span><span class="sxs-lookup"><span data-stu-id="708bb-123">-ServerVersion</span></span>
<span data-ttu-id="708bb-124">Gibt die Version des neuen Servers an.</span><span class="sxs-lookup"><span data-stu-id="708bb-124">Specifies the version of the new server.</span></span> <span data-ttu-id="708bb-125">Die zulässigen Werte für diesen Parameter lauten: 2,0 und 12,0.</span><span class="sxs-lookup"><span data-stu-id="708bb-125">The acceptable values for this parameter are: 2.0 and 12.0.</span></span>
<span data-ttu-id="708bb-126">Geben Sie 2,0 an, um einen Server der Version 11 zu erstellen, oder 12,0, um einen Server der Version 12 zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="708bb-126">Specify 2.0 to create a version 11 server, or 12.0 to create a version 12 server.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="708bb-127">-SqlAdministratorCredentials</span><span class="sxs-lookup"><span data-stu-id="708bb-127">-SqlAdministratorCredentials</span></span>
<span data-ttu-id="708bb-128">Gibt die SQL-Datenbankserver-Administratoranmeldeinformationen für den neuen Server an.</span><span class="sxs-lookup"><span data-stu-id="708bb-128">Specifies the SQL Database server administrator credentials for the new server.</span></span> <span data-ttu-id="708bb-129">Verwenden Sie das Get-Credential-Cmdlet, um ein **PSCredential** -Objekt zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="708bb-129">To obtain a **PSCredential** object, use the Get-Credential cmdlet.</span></span> <span data-ttu-id="708bb-130">Wenn Sie weitere Informationen wünschen, geben Sie `Get-Help
Get-Credential` .</span><span class="sxs-lookup"><span data-stu-id="708bb-130">For more information, type `Get-Help
Get-Credential`.</span></span>

```yaml
Type: System.Management.Automation.PSCredential
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="708bb-131">-Tags</span><span class="sxs-lookup"><span data-stu-id="708bb-131">-Tags</span></span>
<span data-ttu-id="708bb-132">Schlüssel-Wert-Paare in Form einer Hashtabelle</span><span class="sxs-lookup"><span data-stu-id="708bb-132">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="708bb-133">Beispiel: @ {Key0 = "value0"; key1 = $NULL; key2 = "Value2"}</span><span class="sxs-lookup"><span data-stu-id="708bb-133">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases: Tag

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="708bb-134">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="708bb-134">-Confirm</span></span>
<span data-ttu-id="708bb-135">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="708bb-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="708bb-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="708bb-136">-WhatIf</span></span>
<span data-ttu-id="708bb-137">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="708bb-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="708bb-138">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="708bb-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="708bb-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="708bb-139">CommonParameters</span></span>
<span data-ttu-id="708bb-140">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="708bb-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="708bb-141">Weitere Informationen finden Sie unter [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="708bb-141">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="708bb-142">Eingaben</span><span class="sxs-lookup"><span data-stu-id="708bb-142">INPUTS</span></span>

### <span data-ttu-id="708bb-143">System. String</span><span class="sxs-lookup"><span data-stu-id="708bb-143">System.String</span></span>

## <span data-ttu-id="708bb-144">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="708bb-144">OUTPUTS</span></span>

### <span data-ttu-id="708bb-145">Microsoft. Azure. Commands. SQL. Server. Model. AzureSqlServerModel</span><span class="sxs-lookup"><span data-stu-id="708bb-145">Microsoft.Azure.Commands.Sql.Server.Model.AzureSqlServerModel</span></span>

## <span data-ttu-id="708bb-146">Notizen</span><span class="sxs-lookup"><span data-stu-id="708bb-146">NOTES</span></span>

## <span data-ttu-id="708bb-147">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="708bb-147">RELATED LINKS</span></span>

[<span data-ttu-id="708bb-148">Get-AzSqlServer</span><span class="sxs-lookup"><span data-stu-id="708bb-148">Get-AzSqlServer</span></span>](./Get-AzSqlServer.md)

[<span data-ttu-id="708bb-149">Remove-AzSqlServer</span><span class="sxs-lookup"><span data-stu-id="708bb-149">Remove-AzSqlServer</span></span>](./Remove-AzSqlServer.md)

[<span data-ttu-id="708bb-150">Satz-AzSqlServer</span><span class="sxs-lookup"><span data-stu-id="708bb-150">Set-AzSqlServer</span></span>](./Set-AzSqlServer.md)

[<span data-ttu-id="708bb-151">Neu – AzSqlServerFirewallRule</span><span class="sxs-lookup"><span data-stu-id="708bb-151">New-AzSqlServerFirewallRule</span></span>](./New-AzSqlServerFirewallRule.md)

[<span data-ttu-id="708bb-152">SQL-Datenbank-Dokumentation</span><span class="sxs-lookup"><span data-stu-id="708bb-152">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
