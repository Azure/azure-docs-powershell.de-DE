---
external help file: ''
Module Name: Az.MySql
online version: https://docs.microsoft.com/en-us/powershell/module/az.mysql/test-azmysqlflexibleserverconnect
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MySql/help/Test-AzMySqlFlexibleServerConnect.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MySql/help/Test-AzMySqlFlexibleServerConnect.md
ms.openlocfilehash: ccb22d41ec1a4f2f2bceb711a09f7448015f9f38
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100161260"
---
# <span data-ttu-id="025bf-101">Test-AzMySqlFlexibleServerConnect</span><span class="sxs-lookup"><span data-stu-id="025bf-101">Test-AzMySqlFlexibleServerConnect</span></span>

## <span data-ttu-id="025bf-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="025bf-102">SYNOPSIS</span></span>
<span data-ttu-id="025bf-103">Testen der Verbindung mit dem Datenbankserver</span><span class="sxs-lookup"><span data-stu-id="025bf-103">Test out the connection to the database server</span></span>

## <span data-ttu-id="025bf-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="025bf-104">SYNTAX</span></span>

### <span data-ttu-id="025bf-105">Test (Standard)</span><span class="sxs-lookup"><span data-stu-id="025bf-105">Test (Default)</span></span>
```
Test-AzMySqlFlexibleServerConnect -Name <String> -ResourceGroupName <String>
 -AdministratorLoginPassword <SecureString> [-DatabaseName <String>] [-AdministratorUserName <String>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="025bf-106">TestAndQuery</span><span class="sxs-lookup"><span data-stu-id="025bf-106">TestAndQuery</span></span>
```
Test-AzMySqlFlexibleServerConnect -Name <String> -QueryText <String> -ResourceGroupName <String>
 -AdministratorLoginPassword <SecureString> [-DatabaseName <String>] [-AdministratorUserName <String>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="025bf-107">TestViaIdentity</span><span class="sxs-lookup"><span data-stu-id="025bf-107">TestViaIdentity</span></span>
```
Test-AzMySqlFlexibleServerConnect -AdministratorLoginPassword <SecureString> -InputObject <IMySqlIdentity>
 [-DatabaseName <String>] [-AdministratorUserName <String>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="025bf-108">TestViaIdentityAndQuery</span><span class="sxs-lookup"><span data-stu-id="025bf-108">TestViaIdentityAndQuery</span></span>
```
Test-AzMySqlFlexibleServerConnect -QueryText <String> -AdministratorLoginPassword <SecureString>
 -InputObject <IMySqlIdentity> [-DatabaseName <String>] [-AdministratorUserName <String>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="025bf-109">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="025bf-109">DESCRIPTION</span></span>
<span data-ttu-id="025bf-110">Testen der Verbindung mit dem Datenbankserver</span><span class="sxs-lookup"><span data-stu-id="025bf-110">Test out the connection to the database server</span></span>

## <span data-ttu-id="025bf-111">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="025bf-111">EXAMPLES</span></span>

### <span data-ttu-id="025bf-112">Beispiel 1: Testen der Verbindung nach Name</span><span class="sxs-lookup"><span data-stu-id="025bf-112">Example 1: Test connection by name</span></span>
```powershell
PS C:\> Get-AzMySqlFlexibleServerConnect -ResourceGroupName PowershellMySqlTest -Name mysql-test -AdministratorLoginPassword $password

The connection testing to mysql-test.database.azure.com was successful!
```

<span data-ttu-id="025bf-113">Testen der Verbindung durch die Ressourcengruppe und den Servernamen</span><span class="sxs-lookup"><span data-stu-id="025bf-113">Test connection by the resource group and the server name</span></span>

### <span data-ttu-id="025bf-114">Beispiel 2: Testen der Verbindung nach Identität</span><span class="sxs-lookup"><span data-stu-id="025bf-114">Example 2: Test connection by identity</span></span>
```powershell
PS C:\> Get-AzMySqlFlexibleServer -ResourceGroupName PowershellMySqlTest -ServerName mysql-test | Get-AzMySqlFlexibleServerConnect -AdministratorLoginPassword $password

The connection testing to mysql-test.database.azure.com was successful!
```

<span data-ttu-id="025bf-115">Testen der Verbindung durch die Identität</span><span class="sxs-lookup"><span data-stu-id="025bf-115">Test connection by the identity</span></span>

### <span data-ttu-id="025bf-116">Beispiel 3: Testabfrage nach Name</span><span class="sxs-lookup"><span data-stu-id="025bf-116">Example 3: Test query by name</span></span>
```powershell
PS C:\> Get-AzMySqlFlexibleServerConnect -ResourceGroupName PowershellMySqlTest -Name mysql-test -AdministratorLoginPassword $password -Query "SELECT * FROM test"

col
-----
1
2
3
```

<span data-ttu-id="025bf-117">Testen einer Abfrage nach der Ressourcengruppe und dem Servernamen</span><span class="sxs-lookup"><span data-stu-id="025bf-117">Test a query by the resource group and the server name</span></span>

### <span data-ttu-id="025bf-118">Beispiel 4: Testen der Verbindung nach Identität</span><span class="sxs-lookup"><span data-stu-id="025bf-118">Example 4: Test connection by identity</span></span>
```powershell
PS C:\> Get-AzMySqlFlexibleServer -ResourceGroupName PowershellMySqlTest -ServerName mysql-test | Get-AzMySqlFlexibleServerConnect -Query "SELECT * FROM test" -AdministratorLoginPassword $password

col
-----
1
2
3
```

<span data-ttu-id="025bf-119">Testen einer Abfrage nach der Identität</span><span class="sxs-lookup"><span data-stu-id="025bf-119">Test a query by the identity</span></span>

## <span data-ttu-id="025bf-120">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="025bf-120">PARAMETERS</span></span>

### <span data-ttu-id="025bf-121">-AdministratorLoginPassword</span><span class="sxs-lookup"><span data-stu-id="025bf-121">-AdministratorLoginPassword</span></span>
<span data-ttu-id="025bf-122">Das Kennwort des Administrators.</span><span class="sxs-lookup"><span data-stu-id="025bf-122">The password of the administrator.</span></span>
<span data-ttu-id="025bf-123">Mindestens 8 Zeichen und maximal 128 Zeichen.</span><span class="sxs-lookup"><span data-stu-id="025bf-123">Minimum 8 characters and maximum 128 characters.</span></span>
<span data-ttu-id="025bf-124">Das Kennwort muss Zeichen aus drei der folgenden Kategorien enthalten: englische Großbuchstaben, englische Kleinbuchstaben, Zahlen und nicht alphanumerische Zeichen.</span><span class="sxs-lookup"><span data-stu-id="025bf-124">Password must contain characters from three of the following categories: English uppercase letters, English lowercase letters, numbers, and non-alphanumeric characters.</span></span>

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

### <span data-ttu-id="025bf-125">-AdministratorUserName</span><span class="sxs-lookup"><span data-stu-id="025bf-125">-AdministratorUserName</span></span>
<span data-ttu-id="025bf-126">Administratorbenutzername für den Server.</span><span class="sxs-lookup"><span data-stu-id="025bf-126">Administrator username for the server.</span></span>
<span data-ttu-id="025bf-127">Nach dem Festlegen kann sie nicht mehr geändert werden.</span><span class="sxs-lookup"><span data-stu-id="025bf-127">Once set, it cannot be changed.</span></span>

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

### <span data-ttu-id="025bf-128">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="025bf-128">-DatabaseName</span></span>
<span data-ttu-id="025bf-129">Der Name der zu verbindende Datenbank.</span><span class="sxs-lookup"><span data-stu-id="025bf-129">The database name to connect.</span></span>

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

### <span data-ttu-id="025bf-130">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="025bf-130">-DefaultProfile</span></span>
<span data-ttu-id="025bf-131">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="025bf-131">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="025bf-132">-InputObject</span><span class="sxs-lookup"><span data-stu-id="025bf-132">-InputObject</span></span>
<span data-ttu-id="025bf-133">Der Server, auf dem die Verbindung hergestellt werden soll.</span><span class="sxs-lookup"><span data-stu-id="025bf-133">The server to connect.</span></span>
<span data-ttu-id="025bf-134">Informationen zum Erstellen finden Sie im Abschnitt NOTES zu #A0 und zum Erstellen einer Hashtabelle.</span><span class="sxs-lookup"><span data-stu-id="025bf-134">To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.IMySqlIdentity
Parameter Sets: TestViaIdentity, TestViaIdentityAndQuery
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="025bf-135">-Name</span><span class="sxs-lookup"><span data-stu-id="025bf-135">-Name</span></span>
<span data-ttu-id="025bf-136">Der Name des Servers, auf den die Verbindung hergestellt werden soll.</span><span class="sxs-lookup"><span data-stu-id="025bf-136">The name of the server to connect.</span></span>

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

### <span data-ttu-id="025bf-137">-QueryText</span><span class="sxs-lookup"><span data-stu-id="025bf-137">-QueryText</span></span>
<span data-ttu-id="025bf-138">Die Abfrage für die zu testde Datenbank</span><span class="sxs-lookup"><span data-stu-id="025bf-138">The query for the database to test</span></span>

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

### <span data-ttu-id="025bf-139">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="025bf-139">-ResourceGroupName</span></span>
<span data-ttu-id="025bf-140">Der Name der Ressourcengruppe, die die Ressource enthält. Sie können diesen Wert über die Azure Resource Manager-API oder das Portal abrufen.</span><span class="sxs-lookup"><span data-stu-id="025bf-140">The name of the resource group that contains the resource, You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

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

### <span data-ttu-id="025bf-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="025bf-141">CommonParameters</span></span>
<span data-ttu-id="025bf-142">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="025bf-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="025bf-143">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="025bf-143">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="025bf-144">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="025bf-144">INPUTS</span></span>

### <span data-ttu-id="025bf-145">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.IMySqlIdentity</span><span class="sxs-lookup"><span data-stu-id="025bf-145">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.IMySqlIdentity</span></span>

## <span data-ttu-id="025bf-146">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="025bf-146">OUTPUTS</span></span>

### <span data-ttu-id="025bf-147">System.String</span><span class="sxs-lookup"><span data-stu-id="025bf-147">System.String</span></span>

## <span data-ttu-id="025bf-148">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="025bf-148">NOTES</span></span>

<span data-ttu-id="025bf-149">ALIASE</span><span class="sxs-lookup"><span data-stu-id="025bf-149">ALIASES</span></span>

<span data-ttu-id="025bf-150">KOMPLEXE PARAMETEREIGENSCHAFTEN</span><span class="sxs-lookup"><span data-stu-id="025bf-150">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="025bf-151">Erstellen Sie zum Erstellen der unten beschriebenen Parameter eine Hashtabelle mit den entsprechenden Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="025bf-151">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="025bf-152">Um Informationen zu Hashtabellen zu erhalten, führen Sie Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="025bf-152">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="025bf-153">INPUTOBJECT <IMySqlIdentity> : Der Server, auf dem eine Verbindung hergestellt werden soll.</span><span class="sxs-lookup"><span data-stu-id="025bf-153">INPUTOBJECT <IMySqlIdentity>: The server to connect.</span></span>
  - <span data-ttu-id="025bf-154">`[ConfigurationName <String>]`: Der Name der Serverkonfiguration.</span><span class="sxs-lookup"><span data-stu-id="025bf-154">`[ConfigurationName <String>]`: The name of the server configuration.</span></span>
  - <span data-ttu-id="025bf-155">`[DatabaseName <String>]`: Der Name der Datenbank.</span><span class="sxs-lookup"><span data-stu-id="025bf-155">`[DatabaseName <String>]`: The name of the database.</span></span>
  - <span data-ttu-id="025bf-156">`[FirewallRuleName <String>]`: Der Name der Serverfirewallregel.</span><span class="sxs-lookup"><span data-stu-id="025bf-156">`[FirewallRuleName <String>]`: The name of the server firewall rule.</span></span>
  - <span data-ttu-id="025bf-157">`[Id <String>]`: Ressourcenidentitätspfad</span><span class="sxs-lookup"><span data-stu-id="025bf-157">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="025bf-158">`[KeyName <String>]`: Der Name des Serverschlüssels.</span><span class="sxs-lookup"><span data-stu-id="025bf-158">`[KeyName <String>]`: The name of the server key.</span></span>
  - <span data-ttu-id="025bf-159">`[LocationName <String>]`: Der Name des Speicherorts.</span><span class="sxs-lookup"><span data-stu-id="025bf-159">`[LocationName <String>]`: The name of the location.</span></span>
  - <span data-ttu-id="025bf-160">`[ResourceGroupName <String>]`: Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="025bf-160">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="025bf-161">Beim Namen wird die Groß-/Kleinschreibung nicht beachtet.</span><span class="sxs-lookup"><span data-stu-id="025bf-161">The name is case insensitive.</span></span>
  - <span data-ttu-id="025bf-162">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: Der Name der Sicherheitswarnungsrichtlinie.</span><span class="sxs-lookup"><span data-stu-id="025bf-162">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: The name of the security alert policy.</span></span>
  - <span data-ttu-id="025bf-163">`[ServerName <String>]`: Der Name des Servers.</span><span class="sxs-lookup"><span data-stu-id="025bf-163">`[ServerName <String>]`: The name of the server.</span></span>
  - <span data-ttu-id="025bf-164">`[SubscriptionId <String>]`: Die ID des Zielabonnements.</span><span class="sxs-lookup"><span data-stu-id="025bf-164">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="025bf-165">`[VirtualNetworkRuleName <String>]`: Der Name der Regel für das virtuelle Netzwerk.</span><span class="sxs-lookup"><span data-stu-id="025bf-165">`[VirtualNetworkRuleName <String>]`: The name of the virtual network rule.</span></span>

## <span data-ttu-id="025bf-166">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="025bf-166">RELATED LINKS</span></span>

