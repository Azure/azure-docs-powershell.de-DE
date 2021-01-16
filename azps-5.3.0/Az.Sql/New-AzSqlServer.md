---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 7039528F-42AE-45DB-BF81-FE5003F8AEE2
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/new-azsqlserver
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlServer.md
ms.openlocfilehash: ec2e71e6556824ad92e1a5839f0b10c91960fec0
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98460684"
---
# <span data-ttu-id="ec8ae-101">New-AzSqlServer</span><span class="sxs-lookup"><span data-stu-id="ec8ae-101">New-AzSqlServer</span></span>

## <span data-ttu-id="ec8ae-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ec8ae-102">SYNOPSIS</span></span>
<span data-ttu-id="ec8ae-103">Erstellt einen SQL Datenbankserver.</span><span class="sxs-lookup"><span data-stu-id="ec8ae-103">Creates a SQL Database server.</span></span>

## <span data-ttu-id="ec8ae-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="ec8ae-104">SYNTAX</span></span>

```
New-AzSqlServer -ServerName <String> -SqlAdministratorCredentials <PSCredential> -Location <String>
 [-Tags <Hashtable>] [-ServerVersion <String>] [-AssignIdentity] [-PublicNetworkAccess <String>]
 [-MinimalTlsVersion <String>] [-AsJob] [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ec8ae-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="ec8ae-105">DESCRIPTION</span></span>
<span data-ttu-id="ec8ae-106">Das **Cmdlet "New-AzSqlServer"** erstellt einen Azure SQL-Datenbankserver.</span><span class="sxs-lookup"><span data-stu-id="ec8ae-106">The **New-AzSqlServer** cmdlet creates an Azure SQL Database server.</span></span>

## <span data-ttu-id="ec8ae-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="ec8ae-107">EXAMPLES</span></span>

### <span data-ttu-id="ec8ae-108">Beispiel 1: Erstellen eines neuen Azure SQL Datenbankservers</span><span class="sxs-lookup"><span data-stu-id="ec8ae-108">Example 1: Create a new Azure SQL Database server</span></span>
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

<span data-ttu-id="ec8ae-109">Mit diesem Befehl wird eine Version 12 von Azure SQL Datenbankserver erstellt.</span><span class="sxs-lookup"><span data-stu-id="ec8ae-109">This command creates a version 12 Azure SQL Database server.</span></span>

## <span data-ttu-id="ec8ae-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="ec8ae-110">PARAMETERS</span></span>

### <span data-ttu-id="ec8ae-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="ec8ae-111">-AsJob</span></span>
<span data-ttu-id="ec8ae-112">Ausführen des Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="ec8ae-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="ec8ae-113">-AssignIdentity</span><span class="sxs-lookup"><span data-stu-id="ec8ae-113">-AssignIdentity</span></span>
<span data-ttu-id="ec8ae-114">Generieren und zuweisen Sie eine Azure Active Directory-Identität für diesen Server zur Verwendung mit Schlüsselverwaltungsdiensten wie Azure KeyVault.</span><span class="sxs-lookup"><span data-stu-id="ec8ae-114">Generate and assign an Azure Active Directory Identity for this server for use with key management services like Azure KeyVault.</span></span>

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

### <span data-ttu-id="ec8ae-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ec8ae-115">-DefaultProfile</span></span>
<span data-ttu-id="ec8ae-116">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden</span><span class="sxs-lookup"><span data-stu-id="ec8ae-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="ec8ae-117">-Location</span><span class="sxs-lookup"><span data-stu-id="ec8ae-117">-Location</span></span>
<span data-ttu-id="ec8ae-118">Gibt den Speicherort des Rechenzentrums an, in dem dieses Cmdlet den Server erstellt.</span><span class="sxs-lookup"><span data-stu-id="ec8ae-118">Specifies the location of the data center where this cmdlet creates the server.</span></span>

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

### <span data-ttu-id="ec8ae-119">-MinimalTlsVersion</span><span class="sxs-lookup"><span data-stu-id="ec8ae-119">-MinimalTlsVersion</span></span>
<span data-ttu-id="ec8ae-120">Die minimale TLS-Version, die für Sql Server erzwungen werden muss</span><span class="sxs-lookup"><span data-stu-id="ec8ae-120">The minimal TLS version to enforce for Sql Server</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: 1.0, 1.1, 1.2

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ec8ae-121">-PublicNetworkAccess</span><span class="sxs-lookup"><span data-stu-id="ec8ae-121">-PublicNetworkAccess</span></span>
<span data-ttu-id="ec8ae-122">Verwendet eine Kennzeichnung(en), die aktiviert/deaktiviert ist, um anzugeben, ob der Zugriff auf den Server im öffentlichen Netzwerk zulässig ist.</span><span class="sxs-lookup"><span data-stu-id="ec8ae-122">Takes a flag, enabled/disabled, to specify whether public network access to server is allowed or not.</span></span>
<span data-ttu-id="ec8ae-123">Wenn dies deaktiviert ist, können nur Verbindungen, die über private Links hergestellt werden, diesen Server erreichen.</span><span class="sxs-lookup"><span data-stu-id="ec8ae-123">When disabled, only connections made through Private Links can reach this server.</span></span>

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

### <span data-ttu-id="ec8ae-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ec8ae-124">-ResourceGroupName</span></span>
<span data-ttu-id="ec8ae-125">Gibt den Namen der Ressourcengruppe an, der dieses Cmdlet den Server zu weist.</span><span class="sxs-lookup"><span data-stu-id="ec8ae-125">Specifies the name of the resource group to which this cmdlet assigns the server.</span></span>

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

### <span data-ttu-id="ec8ae-126">-ServerName</span><span class="sxs-lookup"><span data-stu-id="ec8ae-126">-ServerName</span></span>
<span data-ttu-id="ec8ae-127">Gibt den Namen des neuen Servers an.</span><span class="sxs-lookup"><span data-stu-id="ec8ae-127">Specifies the name of the new server.</span></span>

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

### <span data-ttu-id="ec8ae-128">-ServerVersion</span><span class="sxs-lookup"><span data-stu-id="ec8ae-128">-ServerVersion</span></span>
<span data-ttu-id="ec8ae-129">Gibt die Version des neuen Servers an.</span><span class="sxs-lookup"><span data-stu-id="ec8ae-129">Specifies the version of the new server.</span></span> <span data-ttu-id="ec8ae-130">Die zulässigen Werte für diesen Parameter sind: 2.0 und 12.0.</span><span class="sxs-lookup"><span data-stu-id="ec8ae-130">The acceptable values for this parameter are: 2.0 and 12.0.</span></span>
<span data-ttu-id="ec8ae-131">Geben Sie 2.0 zum Erstellen eines Servers der Version 11 oder 12.0 zum Erstellen eines Servers der Version 12 an.</span><span class="sxs-lookup"><span data-stu-id="ec8ae-131">Specify 2.0 to create a version 11 server, or 12.0 to create a version 12 server.</span></span>

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

### <span data-ttu-id="ec8ae-132">-SqlAdministratorCredentials</span><span class="sxs-lookup"><span data-stu-id="ec8ae-132">-SqlAdministratorCredentials</span></span>
<span data-ttu-id="ec8ae-133">Gibt die Anmeldeinformationen SQL Datenbankserveradministrator für den neuen Server an.</span><span class="sxs-lookup"><span data-stu-id="ec8ae-133">Specifies the SQL Database server administrator credentials for the new server.</span></span> <span data-ttu-id="ec8ae-134">Zum Abrufen eines **"PSCredential"-Objekts** verwenden Sie das Get-Credential-Cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ec8ae-134">To obtain a **PSCredential** object, use the Get-Credential cmdlet.</span></span> <span data-ttu-id="ec8ae-135">Weitere Informationen erhalten Sie, wenn Sie " `Get-Help
Get-Credential` eingeben" aus.</span><span class="sxs-lookup"><span data-stu-id="ec8ae-135">For more information, type `Get-Help
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

### <span data-ttu-id="ec8ae-136">-Tags</span><span class="sxs-lookup"><span data-stu-id="ec8ae-136">-Tags</span></span>
<span data-ttu-id="ec8ae-137">Schlüssel-Wert-Paare in Form einer Hashtabelle.</span><span class="sxs-lookup"><span data-stu-id="ec8ae-137">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="ec8ae-138">Beispiel: @{key0="value0";key1=$null;key2="value2"}</span><span class="sxs-lookup"><span data-stu-id="ec8ae-138">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="ec8ae-139">-Confirm</span><span class="sxs-lookup"><span data-stu-id="ec8ae-139">-Confirm</span></span>
<span data-ttu-id="ec8ae-140">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="ec8ae-140">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ec8ae-141">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="ec8ae-141">-WhatIf</span></span>
<span data-ttu-id="ec8ae-142">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="ec8ae-142">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ec8ae-143">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="ec8ae-143">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ec8ae-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ec8ae-144">CommonParameters</span></span>
<span data-ttu-id="ec8ae-145">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ec8ae-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ec8ae-146">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="ec8ae-146">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ec8ae-147">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="ec8ae-147">INPUTS</span></span>

### <span data-ttu-id="ec8ae-148">System.String</span><span class="sxs-lookup"><span data-stu-id="ec8ae-148">System.String</span></span>

## <span data-ttu-id="ec8ae-149">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="ec8ae-149">OUTPUTS</span></span>

### <span data-ttu-id="ec8ae-150">Microsoft.Azure.Commands.Sql.Server.Model.AzureSqlServerModel</span><span class="sxs-lookup"><span data-stu-id="ec8ae-150">Microsoft.Azure.Commands.Sql.Server.Model.AzureSqlServerModel</span></span>

## <span data-ttu-id="ec8ae-151">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="ec8ae-151">NOTES</span></span>

## <span data-ttu-id="ec8ae-152">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="ec8ae-152">RELATED LINKS</span></span>

[<span data-ttu-id="ec8ae-153">Get-AzSqlServer</span><span class="sxs-lookup"><span data-stu-id="ec8ae-153">Get-AzSqlServer</span></span>](./Get-AzSqlServer.md)

[<span data-ttu-id="ec8ae-154">Remove-AzSqlServer</span><span class="sxs-lookup"><span data-stu-id="ec8ae-154">Remove-AzSqlServer</span></span>](./Remove-AzSqlServer.md)

[<span data-ttu-id="ec8ae-155">Set-AzSqlServer</span><span class="sxs-lookup"><span data-stu-id="ec8ae-155">Set-AzSqlServer</span></span>](./Set-AzSqlServer.md)

[<span data-ttu-id="ec8ae-156">New-AzSqlServerFirewallRule</span><span class="sxs-lookup"><span data-stu-id="ec8ae-156">New-AzSqlServerFirewallRule</span></span>](./New-AzSqlServerFirewallRule.md)

[<span data-ttu-id="ec8ae-157">SQL Datenbankdokumentation</span><span class="sxs-lookup"><span data-stu-id="ec8ae-157">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
