---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: FAAF458C-1662-4130-9A16-0514B714D11D
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/set-azsqlserver
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlServer.md
ms.openlocfilehash: f408edfa0bcdff88fe7577a7cdb6549dcd722dc2
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/21/2020
ms.locfileid: "93845323"
---
# <span data-ttu-id="eb16c-101">Set-AzSqlServer</span><span class="sxs-lookup"><span data-stu-id="eb16c-101">Set-AzSqlServer</span></span>

## <span data-ttu-id="eb16c-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="eb16c-102">SYNOPSIS</span></span>
<span data-ttu-id="eb16c-103">Ändert die Eigenschaften eines SQL-Datenbankservers.</span><span class="sxs-lookup"><span data-stu-id="eb16c-103">Modifies properties of a SQL Database server.</span></span>

## <span data-ttu-id="eb16c-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="eb16c-104">SYNTAX</span></span>

```
Set-AzSqlServer [-ServerName] <String> [-SqlAdministratorPassword <SecureString>] [-Tags <Hashtable>]
 [-ServerVersion <String>] [-AssignIdentity] [-Force] [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-MinimalTlsVersion <String>] [-PublicNetworkAccess <String>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="eb16c-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="eb16c-105">DESCRIPTION</span></span>
<span data-ttu-id="eb16c-106">Das Cmdlet " **Satz-AzSqlServer** " ändert die Eigenschaften eines Azure SQL-Datenbankservers.</span><span class="sxs-lookup"><span data-stu-id="eb16c-106">The **Set-AzSqlServer** cmdlet modifies properties of an Azure SQL Database server.</span></span>

## <span data-ttu-id="eb16c-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="eb16c-107">EXAMPLES</span></span>

### <span data-ttu-id="eb16c-108">Beispiel 1: Zurücksetzen des Administratorkennworts</span><span class="sxs-lookup"><span data-stu-id="eb16c-108">Example 1: Reset the administrator password</span></span>
```
PS C:\>$ServerPassword = "newpassword"
PS C:\> $SecureString = ConvertTo-SecureString $ServerPassword -AsPlainText -Force
PS C:\> Set-AzSqlServer -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -SqlAdministratorPassword $secureString
ResourceGroupName        : ResourceGroup01
ServerName               : Server01
Location                 : Australia East
SqlAdministratorLogin    : adminLogin
SqlAdministratorPassword :
ServerVersion            : 12.0
Tags                     :
Identity                 :
FullyQualifiedDomainName : server01.database.windows.net
```

<span data-ttu-id="eb16c-109">Mit diesem Befehl wird das Administratorkennwort auf dem AzureSQL-Server mit dem Namen Server01 zurückgesetzt.</span><span class="sxs-lookup"><span data-stu-id="eb16c-109">This command resets the administrator password on the AzureSQL Server named server01.</span></span>

## <span data-ttu-id="eb16c-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="eb16c-110">PARAMETERS</span></span>

### <span data-ttu-id="eb16c-111">-AssignIdentity</span><span class="sxs-lookup"><span data-stu-id="eb16c-111">-AssignIdentity</span></span>
<span data-ttu-id="eb16c-112">Sie können eine Azure Active Directory-Identität für diesen Server für die Verwendung mit Schlüssel Verwaltungsdiensten wie Azure keyvault generieren und zuweisen.</span><span class="sxs-lookup"><span data-stu-id="eb16c-112">Generate and assign an Azure Active Directory Identity for this server for use with key management services like Azure KeyVault.</span></span>

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

### <span data-ttu-id="eb16c-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="eb16c-113">-DefaultProfile</span></span>
<span data-ttu-id="eb16c-114">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="eb16c-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="eb16c-115">-Force</span><span class="sxs-lookup"><span data-stu-id="eb16c-115">-Force</span></span>
<span data-ttu-id="eb16c-116">Erzwingt, dass der Befehl ausgeführt wird, ohne die Bestätigung des Benutzers zu fordern.</span><span class="sxs-lookup"><span data-stu-id="eb16c-116">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="eb16c-117">-PublicNetworkAccess</span><span class="sxs-lookup"><span data-stu-id="eb16c-117">-PublicNetworkAccess</span></span>
<span data-ttu-id="eb16c-118">Akzeptiert ein Flag, aktiviert/deaktiviert, um anzugeben, ob der Zugriff auf den öffentlichen Netzwerkserver zulässig ist oder nicht.</span><span class="sxs-lookup"><span data-stu-id="eb16c-118">Takes a flag, enabled/disabled, to specify whether public network access to server is allowed or not.</span></span>
<span data-ttu-id="eb16c-119">Wenn diese Option deaktiviert ist, können nur Verbindungen, die über private links erfolgen, auf diesen Server zugreifen.</span><span class="sxs-lookup"><span data-stu-id="eb16c-119">When disabled, only connections made through Private Links can reach this server.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="eb16c-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="eb16c-120">-ResourceGroupName</span></span>
<span data-ttu-id="eb16c-121">Gibt den Namen der Ressourcengruppe an, der der Server zugewiesen ist.</span><span class="sxs-lookup"><span data-stu-id="eb16c-121">Specifies the name of the resource group to which the server is assigned.</span></span>

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

### <span data-ttu-id="eb16c-122">-Servername</span><span class="sxs-lookup"><span data-stu-id="eb16c-122">-ServerName</span></span>
<span data-ttu-id="eb16c-123">Gibt den Namen des Servers an, der vom Cmdlet geändert wird.</span><span class="sxs-lookup"><span data-stu-id="eb16c-123">Specifies the name of the server that this cmdlet modifies.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="eb16c-124">-Server Version vom</span><span class="sxs-lookup"><span data-stu-id="eb16c-124">-ServerVersion</span></span>
<span data-ttu-id="eb16c-125">Gibt die Version an, für die dieses Cmdlet den Server ändert.</span><span class="sxs-lookup"><span data-stu-id="eb16c-125">Specifies the version to which this cmdlet changes the server.</span></span> <span data-ttu-id="eb16c-126">Die zulässigen Werte für diesen Parameter lauten: 2,0 und 12,0.</span><span class="sxs-lookup"><span data-stu-id="eb16c-126">The acceptable values for this parameter are: 2.0 and 12.0.</span></span>

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

### <span data-ttu-id="eb16c-127">-SqlAdministratorPassword</span><span class="sxs-lookup"><span data-stu-id="eb16c-127">-SqlAdministratorPassword</span></span>
<span data-ttu-id="eb16c-128">Gibt ein neues Kennwort als **SecureString** für den Datenbankserver-Administrator an.</span><span class="sxs-lookup"><span data-stu-id="eb16c-128">Specifies a new password, as a **SecureString** , for the database server administrator.</span></span> <span data-ttu-id="eb16c-129">Verwenden Sie das Get-Credential-Cmdlet, um eine **SecureString** -Anwendung zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="eb16c-129">To obtain a **SecureString** , use the Get-Credential cmdlet.</span></span> <span data-ttu-id="eb16c-130">Wenn Sie weitere Informationen wünschen, geben Sie `Get-Help
ConvertTo-SecureString` .</span><span class="sxs-lookup"><span data-stu-id="eb16c-130">For more information, type `Get-Help
ConvertTo-SecureString`.</span></span>

```yaml
Type: System.Security.SecureString
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="eb16c-131">-MinimalTlsVersion</span><span class="sxs-lookup"><span data-stu-id="eb16c-131">-MinimalTlsVersion</span></span>
<span data-ttu-id="eb16c-132">Die minimale TLS-Version, die für SQL Server erzwungen werden soll</span><span class="sxs-lookup"><span data-stu-id="eb16c-132">The minimal TLS version to enforce for Sql Server</span></span>

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

### <span data-ttu-id="eb16c-133">-Tags</span><span class="sxs-lookup"><span data-stu-id="eb16c-133">-Tags</span></span>
<span data-ttu-id="eb16c-134">Gibt ein Wörterbuch mit Tags an, die dieses Cmdlet dem Server anordnet.</span><span class="sxs-lookup"><span data-stu-id="eb16c-134">Specifies a dictionary of tags that this cmdlet associates with the server.</span></span> <span data-ttu-id="eb16c-135">Schlüssel-Wert-Paare in Form einer Hashtabelle, die als Tags auf dem Server definiert ist.</span><span class="sxs-lookup"><span data-stu-id="eb16c-135">Key-value pairs in the form of a hash table set as tags on the server.</span></span> <span data-ttu-id="eb16c-136">Beispiel: @ {Key0 = "value0"; key1 = $NULL; key2 = "Value2"}</span><span class="sxs-lookup"><span data-stu-id="eb16c-136">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="eb16c-137">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="eb16c-137">-Confirm</span></span>
<span data-ttu-id="eb16c-138">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="eb16c-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="eb16c-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="eb16c-139">-WhatIf</span></span>
<span data-ttu-id="eb16c-140">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="eb16c-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="eb16c-141">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="eb16c-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="eb16c-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="eb16c-142">CommonParameters</span></span>
<span data-ttu-id="eb16c-143">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="eb16c-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="eb16c-144">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="eb16c-144">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="eb16c-145">Eingaben</span><span class="sxs-lookup"><span data-stu-id="eb16c-145">INPUTS</span></span>

### <span data-ttu-id="eb16c-146">System. String</span><span class="sxs-lookup"><span data-stu-id="eb16c-146">System.String</span></span>

## <span data-ttu-id="eb16c-147">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="eb16c-147">OUTPUTS</span></span>

### <span data-ttu-id="eb16c-148">Microsoft. Azure. Commands. SQL. Server. Model. AzureSqlServerModel</span><span class="sxs-lookup"><span data-stu-id="eb16c-148">Microsoft.Azure.Commands.Sql.Server.Model.AzureSqlServerModel</span></span>

## <span data-ttu-id="eb16c-149">Notizen</span><span class="sxs-lookup"><span data-stu-id="eb16c-149">NOTES</span></span>

## <span data-ttu-id="eb16c-150">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="eb16c-150">RELATED LINKS</span></span>

[<span data-ttu-id="eb16c-151">SQL-Datenbank-Dokumentation</span><span class="sxs-lookup"><span data-stu-id="eb16c-151">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
