---
external help file: ''
Module Name: Az.PostgreSql
online version: https://docs.microsoft.com/en-us/powershell/module/az.postgresql/test-azpostgresqlflexibleserverconnect
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PostgreSql/help/Test-AzPostgreSqlFlexibleServerConnect.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PostgreSql/help/Test-AzPostgreSqlFlexibleServerConnect.md
ms.openlocfilehash: 1cbc4b8274a619514268e8412f7f9123a5e9e58a
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100169417"
---
# <span data-ttu-id="27434-101">Test-AzPostgreSqlFlexibleServerConnect</span><span class="sxs-lookup"><span data-stu-id="27434-101">Test-AzPostgreSqlFlexibleServerConnect</span></span>

## <span data-ttu-id="27434-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="27434-102">SYNOPSIS</span></span>
<span data-ttu-id="27434-103">Testen der Verbindung mit dem Datenbankserver</span><span class="sxs-lookup"><span data-stu-id="27434-103">Test out the connection to the database server</span></span>

## <span data-ttu-id="27434-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="27434-104">SYNTAX</span></span>

### <span data-ttu-id="27434-105">Test (Standard)</span><span class="sxs-lookup"><span data-stu-id="27434-105">Test (Default)</span></span>
```
Test-AzPostgreSqlFlexibleServerConnect -Name <String> -ResourceGroupName <String>
 -AdministratorLoginPassword <SecureString> [-DatabaseName <String>] [-AdministratorUserName <String>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="27434-106">TestAndQuery</span><span class="sxs-lookup"><span data-stu-id="27434-106">TestAndQuery</span></span>
```
Test-AzPostgreSqlFlexibleServerConnect -Name <String> -QueryText <String> -ResourceGroupName <String>
 -AdministratorLoginPassword <SecureString> [-DatabaseName <String>] [-AdministratorUserName <String>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="27434-107">TestViaIdentity</span><span class="sxs-lookup"><span data-stu-id="27434-107">TestViaIdentity</span></span>
```
Test-AzPostgreSqlFlexibleServerConnect -AdministratorLoginPassword <SecureString>
 -InputObject <IPostgreSqlIdentity> [-DatabaseName <String>] [-AdministratorUserName <String>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="27434-108">TestViaIdentityAndQuery</span><span class="sxs-lookup"><span data-stu-id="27434-108">TestViaIdentityAndQuery</span></span>
```
Test-AzPostgreSqlFlexibleServerConnect -QueryText <String> -AdministratorLoginPassword <SecureString>
 -InputObject <IPostgreSqlIdentity> [-DatabaseName <String>] [-AdministratorUserName <String>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="27434-109">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="27434-109">DESCRIPTION</span></span>
<span data-ttu-id="27434-110">Testen der Verbindung mit dem Datenbankserver</span><span class="sxs-lookup"><span data-stu-id="27434-110">Test out the connection to the database server</span></span>

## <span data-ttu-id="27434-111">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="27434-111">EXAMPLES</span></span>

### <span data-ttu-id="27434-112">Beispiel 1: Testen der Verbindung nach Name</span><span class="sxs-lookup"><span data-stu-id="27434-112">Example 1: Test connection by name</span></span>
```powershell
PS C:\> Get-AzPostgreSqlFlexibleServerConnect -ResourceGroupName PowershellPostgreSqlTest -Name postgresql-test -AdministratorLoginPassword $password

The connection testing to postgresql-test.database.azure.com was successful!
```

<span data-ttu-id="27434-113">Testverbindung durch die Ressourcengruppe und den Servernamen</span><span class="sxs-lookup"><span data-stu-id="27434-113">Test connection by the resource group and the server name</span></span>

### <span data-ttu-id="27434-114">Beispiel 2: Testen der Verbindung nach Identität</span><span class="sxs-lookup"><span data-stu-id="27434-114">Example 2: Test connection by identity</span></span>
```powershell
PS C:\> Get-AzPostgreSqlFlexibleServer -ResourceGroupName PowershellPostgreSqlTest -ServerName postgresql-test | Get-AzPostgreSqlFlexibleServerConnect -AdministratorLoginPassword $password

The connection testing to postgresql-test.database.azure.com was successful!
```

<span data-ttu-id="27434-115">Testen der Verbindung durch die Identität</span><span class="sxs-lookup"><span data-stu-id="27434-115">Test connection by the identity</span></span>

### <span data-ttu-id="27434-116">Beispiel 3: Testabfrage nach Name</span><span class="sxs-lookup"><span data-stu-id="27434-116">Example 3: Test query by name</span></span>
```powershell
PS C:\> Get-AzPostgreSqlFlexibleServerConnect -ResourceGroupName PowershellPostgreSqlTest -Name postgresql-test -AdministratorLoginPassword $password -Query "SELECT * FROM test"

col
-----
1
2
3
```

<span data-ttu-id="27434-117">Testen einer Abfrage nach der Ressourcengruppe und dem Servernamen</span><span class="sxs-lookup"><span data-stu-id="27434-117">Test a query by the resource group and the server name</span></span>

### <span data-ttu-id="27434-118">Beispiel 4: Testen der Verbindung nach Identität</span><span class="sxs-lookup"><span data-stu-id="27434-118">Example 4: Test connection by identity</span></span>
```powershell
PS C:\> Get-AzPostgreSqlFlexibleServer -ResourceGroupName PowershellPostgreSqlTest -ServerName postgresql-test | Get-AzPostgreSqlFlexibleServerConnect -Query "SELECT * FROM test" -AdministratorLoginPassword $password

col
-----
1
2
3
```

<span data-ttu-id="27434-119">Testen einer Abfrage nach der Identität</span><span class="sxs-lookup"><span data-stu-id="27434-119">Test a query by the identity</span></span>

## <span data-ttu-id="27434-120">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="27434-120">PARAMETERS</span></span>

### <span data-ttu-id="27434-121">-AdministratorLoginPassword</span><span class="sxs-lookup"><span data-stu-id="27434-121">-AdministratorLoginPassword</span></span>
<span data-ttu-id="27434-122">Das Kennwort des Administrators.</span><span class="sxs-lookup"><span data-stu-id="27434-122">The password of the administrator.</span></span>
<span data-ttu-id="27434-123">Mindestens 8 Zeichen und maximal 128 Zeichen.</span><span class="sxs-lookup"><span data-stu-id="27434-123">Minimum 8 characters and maximum 128 characters.</span></span>
<span data-ttu-id="27434-124">Das Kennwort muss Zeichen aus drei der folgenden Kategorien enthalten: englische Großbuchstaben, englische Kleinbuchstaben, Zahlen und nicht alphanumerische Zeichen.</span><span class="sxs-lookup"><span data-stu-id="27434-124">Password must contain characters from three of the following categories: English uppercase letters, English lowercase letters, numbers, and non-alphanumeric characters.</span></span>

```yaml
Type: System.Security.SecureString
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="27434-125">-AdministratorUserName</span><span class="sxs-lookup"><span data-stu-id="27434-125">-AdministratorUserName</span></span>
<span data-ttu-id="27434-126">Administratorbenutzername für den Server.</span><span class="sxs-lookup"><span data-stu-id="27434-126">Administrator username for the server.</span></span>
<span data-ttu-id="27434-127">Nach dem Festlegen kann sie nicht mehr geändert werden.</span><span class="sxs-lookup"><span data-stu-id="27434-127">Once set, it cannot be changed.</span></span>

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

### <span data-ttu-id="27434-128">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="27434-128">-DatabaseName</span></span>
<span data-ttu-id="27434-129">Der Name der zu verbindende Datenbank.</span><span class="sxs-lookup"><span data-stu-id="27434-129">The database name to connect.</span></span>

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

### <span data-ttu-id="27434-130">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="27434-130">-DefaultProfile</span></span>
<span data-ttu-id="27434-131">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="27434-131">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: System.Management.Automation.PSObject
Parameter Sets: (All)
Aliases: AzureRMContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="27434-132">-InputObject</span><span class="sxs-lookup"><span data-stu-id="27434-132">-InputObject</span></span>
<span data-ttu-id="27434-133">Der Server, auf dem die Verbindung hergestellt werden soll.</span><span class="sxs-lookup"><span data-stu-id="27434-133">The server to connect.</span></span>
<span data-ttu-id="27434-134">Informationen zum Erstellen finden Sie im Abschnitt NOTES zu #A0 und zum Erstellen einer Hashtabelle.</span><span class="sxs-lookup"><span data-stu-id="27434-134">To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Models.IPostgreSqlIdentity
Parameter Sets: TestViaIdentity, TestViaIdentityAndQuery
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="27434-135">-Name</span><span class="sxs-lookup"><span data-stu-id="27434-135">-Name</span></span>
<span data-ttu-id="27434-136">Der Name des Servers, auf den die Verbindung hergestellt werden soll.</span><span class="sxs-lookup"><span data-stu-id="27434-136">The name of the server to connect.</span></span>

```yaml
Type: System.String
Parameter Sets: Test, TestAndQuery
Aliases: ServerName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="27434-137">-QueryText</span><span class="sxs-lookup"><span data-stu-id="27434-137">-QueryText</span></span>
<span data-ttu-id="27434-138">Die Abfrage für die zu testde Datenbank</span><span class="sxs-lookup"><span data-stu-id="27434-138">The query for the database to test</span></span>

```yaml
Type: System.String
Parameter Sets: TestAndQuery, TestViaIdentityAndQuery
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="27434-139">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="27434-139">-ResourceGroupName</span></span>
<span data-ttu-id="27434-140">Der Name der Ressourcengruppe, die die Ressource enthält. Sie können diesen Wert über die Azure Resource Manager-API oder das Portal abrufen.</span><span class="sxs-lookup"><span data-stu-id="27434-140">The name of the resource group that contains the resource, You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

```yaml
Type: System.String
Parameter Sets: Test, TestAndQuery
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="27434-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="27434-141">CommonParameters</span></span>
<span data-ttu-id="27434-142">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="27434-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="27434-143">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="27434-143">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="27434-144">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="27434-144">INPUTS</span></span>

### <span data-ttu-id="27434-145">Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Models.IPostgreSqlIdentity</span><span class="sxs-lookup"><span data-stu-id="27434-145">Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Models.IPostgreSqlIdentity</span></span>

## <span data-ttu-id="27434-146">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="27434-146">OUTPUTS</span></span>

### <span data-ttu-id="27434-147">System.String</span><span class="sxs-lookup"><span data-stu-id="27434-147">System.String</span></span>

## <span data-ttu-id="27434-148">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="27434-148">NOTES</span></span>

<span data-ttu-id="27434-149">ALIASE</span><span class="sxs-lookup"><span data-stu-id="27434-149">ALIASES</span></span>

<span data-ttu-id="27434-150">KOMPLEXE PARAMETEREIGENSCHAFTEN</span><span class="sxs-lookup"><span data-stu-id="27434-150">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="27434-151">Erstellen Sie zum Erstellen der unten beschriebenen Parameter eine Hashtabelle mit den entsprechenden Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="27434-151">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="27434-152">Um Informationen zu Hashtabellen zu erhalten, führen Sie Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="27434-152">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="27434-153">INPUTOBJECT <IPostgreSqlIdentity> : Der Server, auf dem eine Verbindung hergestellt werden soll.</span><span class="sxs-lookup"><span data-stu-id="27434-153">INPUTOBJECT <IPostgreSqlIdentity>: The server to connect.</span></span>
  - <span data-ttu-id="27434-154">`[ConfigurationName <String>]`: Der Name der Serverkonfiguration.</span><span class="sxs-lookup"><span data-stu-id="27434-154">`[ConfigurationName <String>]`: The name of the server configuration.</span></span>
  - <span data-ttu-id="27434-155">`[DatabaseName <String>]`: Der Name der Datenbank.</span><span class="sxs-lookup"><span data-stu-id="27434-155">`[DatabaseName <String>]`: The name of the database.</span></span>
  - <span data-ttu-id="27434-156">`[FirewallRuleName <String>]`: Der Name der Serverfirewallregel.</span><span class="sxs-lookup"><span data-stu-id="27434-156">`[FirewallRuleName <String>]`: The name of the server firewall rule.</span></span>
  - <span data-ttu-id="27434-157">`[Id <String>]`: Ressourcenidentitätspfad</span><span class="sxs-lookup"><span data-stu-id="27434-157">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="27434-158">`[LocationName <String>]`: Der Name des Speicherorts.</span><span class="sxs-lookup"><span data-stu-id="27434-158">`[LocationName <String>]`: The name of the location.</span></span>
  - <span data-ttu-id="27434-159">`[ResourceGroupName <String>]`: Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="27434-159">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="27434-160">Beim Namen wird die Groß-/Kleinschreibung nicht beachtet.</span><span class="sxs-lookup"><span data-stu-id="27434-160">The name is case insensitive.</span></span>
  - <span data-ttu-id="27434-161">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: Der Name der Sicherheitswarnungsrichtlinie.</span><span class="sxs-lookup"><span data-stu-id="27434-161">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: The name of the security alert policy.</span></span>
  - <span data-ttu-id="27434-162">`[ServerName <String>]`: Der Name des Servers.</span><span class="sxs-lookup"><span data-stu-id="27434-162">`[ServerName <String>]`: The name of the server.</span></span>
  - <span data-ttu-id="27434-163">`[SubscriptionId <String>]`: Die ID des Zielabonnements.</span><span class="sxs-lookup"><span data-stu-id="27434-163">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="27434-164">`[VirtualNetworkRuleName <String>]`: Der Name der Regel für das virtuelle Netzwerk.</span><span class="sxs-lookup"><span data-stu-id="27434-164">`[VirtualNetworkRuleName <String>]`: The name of the virtual network rule.</span></span>

## <span data-ttu-id="27434-165">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="27434-165">RELATED LINKS</span></span>

