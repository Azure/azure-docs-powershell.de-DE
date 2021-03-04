---
external help file: ''
Module Name: Az.PostgreSql
online version: https://docs.microsoft.com/powershell/module/az.postgresql/test-azpostgresqlflexibleserverconnect
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PostgreSql/help/Test-AzPostgreSqlFlexibleServerConnect.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PostgreSql/help/Test-AzPostgreSqlFlexibleServerConnect.md
ms.openlocfilehash: 1e49f5937196a402e051d28665614befbf6eb04c
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101919395"
---
# <span data-ttu-id="cc9ee-101">Test-AzPostgreSqlFlexibleServerConnect</span><span class="sxs-lookup"><span data-stu-id="cc9ee-101">Test-AzPostgreSqlFlexibleServerConnect</span></span>

## <span data-ttu-id="cc9ee-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="cc9ee-102">SYNOPSIS</span></span>
<span data-ttu-id="cc9ee-103">Testen der Verbindung mit dem Datenbankserver</span><span class="sxs-lookup"><span data-stu-id="cc9ee-103">Test out the connection to the database server</span></span>

## <span data-ttu-id="cc9ee-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="cc9ee-104">SYNTAX</span></span>

### <span data-ttu-id="cc9ee-105">Test (Standard)</span><span class="sxs-lookup"><span data-stu-id="cc9ee-105">Test (Default)</span></span>
```
Test-AzPostgreSqlFlexibleServerConnect -Name <String> -ResourceGroupName <String>
 -AdministratorLoginPassword <SecureString> [-DatabaseName <String>] [-AdministratorUserName <String>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="cc9ee-106">TestAndQuery</span><span class="sxs-lookup"><span data-stu-id="cc9ee-106">TestAndQuery</span></span>
```
Test-AzPostgreSqlFlexibleServerConnect -Name <String> -QueryText <String> -ResourceGroupName <String>
 -AdministratorLoginPassword <SecureString> [-DatabaseName <String>] [-AdministratorUserName <String>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="cc9ee-107">TestViaIdentity</span><span class="sxs-lookup"><span data-stu-id="cc9ee-107">TestViaIdentity</span></span>
```
Test-AzPostgreSqlFlexibleServerConnect -AdministratorLoginPassword <SecureString>
 -InputObject <IPostgreSqlIdentity> [-DatabaseName <String>] [-AdministratorUserName <String>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="cc9ee-108">TestViaIdentityAndQuery</span><span class="sxs-lookup"><span data-stu-id="cc9ee-108">TestViaIdentityAndQuery</span></span>
```
Test-AzPostgreSqlFlexibleServerConnect -QueryText <String> -AdministratorLoginPassword <SecureString>
 -InputObject <IPostgreSqlIdentity> [-DatabaseName <String>] [-AdministratorUserName <String>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="cc9ee-109">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="cc9ee-109">DESCRIPTION</span></span>
<span data-ttu-id="cc9ee-110">Testen der Verbindung mit dem Datenbankserver</span><span class="sxs-lookup"><span data-stu-id="cc9ee-110">Test out the connection to the database server</span></span>

## <span data-ttu-id="cc9ee-111">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="cc9ee-111">EXAMPLES</span></span>

### <span data-ttu-id="cc9ee-112">Beispiel 1: Testen der Verbindung nach Name</span><span class="sxs-lookup"><span data-stu-id="cc9ee-112">Example 1: Test connection by name</span></span>
```powershell
PS C:\> Get-AzPostgreSqlFlexibleServerConnect -ResourceGroupName PowershellPostgreSqlTest -Name postgresql-test -AdministratorLoginPassword $password

The connection testing to postgresql-test.database.azure.com was successful!
```

<span data-ttu-id="cc9ee-113">Testen der Verbindung durch die Ressourcengruppe und den Servernamen</span><span class="sxs-lookup"><span data-stu-id="cc9ee-113">Test connection by the resource group and the server name</span></span>

### <span data-ttu-id="cc9ee-114">Beispiel 2: Testen der Verbindung nach Identität</span><span class="sxs-lookup"><span data-stu-id="cc9ee-114">Example 2: Test connection by identity</span></span>
```powershell
PS C:\> Get-AzPostgreSqlFlexibleServer -ResourceGroupName PowershellPostgreSqlTest -ServerName postgresql-test | Get-AzPostgreSqlFlexibleServerConnect -AdministratorLoginPassword $password

The connection testing to postgresql-test.database.azure.com was successful!
```

<span data-ttu-id="cc9ee-115">Testen der Verbindung nach der Identität</span><span class="sxs-lookup"><span data-stu-id="cc9ee-115">Test connection by the identity</span></span>

### <span data-ttu-id="cc9ee-116">Beispiel 3: Testabfrage nach Name</span><span class="sxs-lookup"><span data-stu-id="cc9ee-116">Example 3: Test query by name</span></span>
```powershell
PS C:\> Get-AzPostgreSqlFlexibleServerConnect -ResourceGroupName PowershellPostgreSqlTest -Name postgresql-test -AdministratorLoginPassword $password -Query "SELECT * FROM test"

col
-----
1
2
3
```

<span data-ttu-id="cc9ee-117">Testen einer Abfrage nach der Ressourcengruppe und dem Servernamen</span><span class="sxs-lookup"><span data-stu-id="cc9ee-117">Test a query by the resource group and the server name</span></span>

### <span data-ttu-id="cc9ee-118">Beispiel 4: Testen der Verbindung nach Identität</span><span class="sxs-lookup"><span data-stu-id="cc9ee-118">Example 4: Test connection by identity</span></span>
```powershell
PS C:\> Get-AzPostgreSqlFlexibleServer -ResourceGroupName PowershellPostgreSqlTest -ServerName postgresql-test | Get-AzPostgreSqlFlexibleServerConnect -Query "SELECT * FROM test" -AdministratorLoginPassword $password

col
-----
1
2
3
```

<span data-ttu-id="cc9ee-119">Testen einer Abfrage nach der Identität</span><span class="sxs-lookup"><span data-stu-id="cc9ee-119">Test a query by the identity</span></span>

## <span data-ttu-id="cc9ee-120">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="cc9ee-120">PARAMETERS</span></span>

### <span data-ttu-id="cc9ee-121">-AdministratorLoginPassword</span><span class="sxs-lookup"><span data-stu-id="cc9ee-121">-AdministratorLoginPassword</span></span>
<span data-ttu-id="cc9ee-122">Das Kennwort des Administrators.</span><span class="sxs-lookup"><span data-stu-id="cc9ee-122">The password of the administrator.</span></span>
<span data-ttu-id="cc9ee-123">Mindestens 8 Zeichen und maximal 128 Zeichen.</span><span class="sxs-lookup"><span data-stu-id="cc9ee-123">Minimum 8 characters and maximum 128 characters.</span></span>
<span data-ttu-id="cc9ee-124">Das Kennwort muss Zeichen aus drei der folgenden Kategorien enthalten: englische Großbuchstaben, englische Kleinbuchstaben, Zahlen und nicht alphanumerische Zeichen.</span><span class="sxs-lookup"><span data-stu-id="cc9ee-124">Password must contain characters from three of the following categories: English uppercase letters, English lowercase letters, numbers, and non-alphanumeric characters.</span></span>

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

### <span data-ttu-id="cc9ee-125">-AdministratorUserName</span><span class="sxs-lookup"><span data-stu-id="cc9ee-125">-AdministratorUserName</span></span>
<span data-ttu-id="cc9ee-126">Administratorname für den Server.</span><span class="sxs-lookup"><span data-stu-id="cc9ee-126">Administrator username for the server.</span></span>
<span data-ttu-id="cc9ee-127">Nachdem sie festgelegt wurde, kann sie nicht mehr geändert werden.</span><span class="sxs-lookup"><span data-stu-id="cc9ee-127">Once set, it cannot be changed.</span></span>

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

### <span data-ttu-id="cc9ee-128">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="cc9ee-128">-DatabaseName</span></span>
<span data-ttu-id="cc9ee-129">Der Datenbankname, mit dem eine Verbindung hergestellt werden soll.</span><span class="sxs-lookup"><span data-stu-id="cc9ee-129">The database name to connect.</span></span>

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

### <span data-ttu-id="cc9ee-130">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cc9ee-130">-DefaultProfile</span></span>
<span data-ttu-id="cc9ee-131">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="cc9ee-131">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="cc9ee-132">-InputObject</span><span class="sxs-lookup"><span data-stu-id="cc9ee-132">-InputObject</span></span>
<span data-ttu-id="cc9ee-133">Der Server, der eine Verbindung herstellen soll.</span><span class="sxs-lookup"><span data-stu-id="cc9ee-133">The server to connect.</span></span>
<span data-ttu-id="cc9ee-134">Informationen zum Erstellen finden Sie im Abschnitt NOTIZEN zu INPUTOBJECT-Eigenschaften, und erstellen Sie eine Hashtabelle.</span><span class="sxs-lookup"><span data-stu-id="cc9ee-134">To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="cc9ee-135">-Name</span><span class="sxs-lookup"><span data-stu-id="cc9ee-135">-Name</span></span>
<span data-ttu-id="cc9ee-136">Der Name des Servers, der eine Verbindung herstellen soll.</span><span class="sxs-lookup"><span data-stu-id="cc9ee-136">The name of the server to connect.</span></span>

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

### <span data-ttu-id="cc9ee-137">-QueryText</span><span class="sxs-lookup"><span data-stu-id="cc9ee-137">-QueryText</span></span>
<span data-ttu-id="cc9ee-138">Die Abfrage für die zu testende Datenbank</span><span class="sxs-lookup"><span data-stu-id="cc9ee-138">The query for the database to test</span></span>

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

### <span data-ttu-id="cc9ee-139">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cc9ee-139">-ResourceGroupName</span></span>
<span data-ttu-id="cc9ee-140">Der Name der Ressourcengruppe, die die Ressource enthält. Sie können diesen Wert über die Azure Resource Manager-API oder das Portal abrufen.</span><span class="sxs-lookup"><span data-stu-id="cc9ee-140">The name of the resource group that contains the resource, You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

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

### <span data-ttu-id="cc9ee-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cc9ee-141">CommonParameters</span></span>
<span data-ttu-id="cc9ee-142">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cc9ee-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cc9ee-143">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="cc9ee-143">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cc9ee-144">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="cc9ee-144">INPUTS</span></span>

### <span data-ttu-id="cc9ee-145">Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Models.IPostgreSqlIdentity</span><span class="sxs-lookup"><span data-stu-id="cc9ee-145">Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Models.IPostgreSqlIdentity</span></span>

## <span data-ttu-id="cc9ee-146">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="cc9ee-146">OUTPUTS</span></span>

### <span data-ttu-id="cc9ee-147">System.String</span><span class="sxs-lookup"><span data-stu-id="cc9ee-147">System.String</span></span>

## <span data-ttu-id="cc9ee-148">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="cc9ee-148">NOTES</span></span>

<span data-ttu-id="cc9ee-149">ALIASE</span><span class="sxs-lookup"><span data-stu-id="cc9ee-149">ALIASES</span></span>

<span data-ttu-id="cc9ee-150">KOMPLEXE PARAMETEREIGENSCHAFTEN</span><span class="sxs-lookup"><span data-stu-id="cc9ee-150">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="cc9ee-151">Um die unten beschriebenen Parameter zu erstellen, erstellen Sie eine Hashtabelle, die die entsprechenden Eigenschaften enthält.</span><span class="sxs-lookup"><span data-stu-id="cc9ee-151">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="cc9ee-152">Informationen zu Hashtabellen finden Sie unter Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="cc9ee-152">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="cc9ee-153">INPUTOBJECT <IPostgreSqlIdentity> : Der Server, der eine Verbindung herstellen soll.</span><span class="sxs-lookup"><span data-stu-id="cc9ee-153">INPUTOBJECT <IPostgreSqlIdentity>: The server to connect.</span></span>
  - <span data-ttu-id="cc9ee-154">`[ConfigurationName <String>]`: Der Name der Serverkonfiguration.</span><span class="sxs-lookup"><span data-stu-id="cc9ee-154">`[ConfigurationName <String>]`: The name of the server configuration.</span></span>
  - <span data-ttu-id="cc9ee-155">`[DatabaseName <String>]`: Der Name der Datenbank.</span><span class="sxs-lookup"><span data-stu-id="cc9ee-155">`[DatabaseName <String>]`: The name of the database.</span></span>
  - <span data-ttu-id="cc9ee-156">`[FirewallRuleName <String>]`: Der Name der Serverfirewallregel.</span><span class="sxs-lookup"><span data-stu-id="cc9ee-156">`[FirewallRuleName <String>]`: The name of the server firewall rule.</span></span>
  - <span data-ttu-id="cc9ee-157">`[Id <String>]`: Ressourcenidentitätspfad</span><span class="sxs-lookup"><span data-stu-id="cc9ee-157">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="cc9ee-158">`[LocationName <String>]`: Der Name des Speicherorts.</span><span class="sxs-lookup"><span data-stu-id="cc9ee-158">`[LocationName <String>]`: The name of the location.</span></span>
  - <span data-ttu-id="cc9ee-159">`[ResourceGroupName <String>]`: Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="cc9ee-159">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="cc9ee-160">Der Name ist groß- und kleinschreibungsunabhängiger.</span><span class="sxs-lookup"><span data-stu-id="cc9ee-160">The name is case insensitive.</span></span>
  - <span data-ttu-id="cc9ee-161">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: Der Name der Sicherheitsbenachrichtigungsrichtlinie.</span><span class="sxs-lookup"><span data-stu-id="cc9ee-161">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: The name of the security alert policy.</span></span>
  - <span data-ttu-id="cc9ee-162">`[ServerName <String>]`: Der Name des Servers.</span><span class="sxs-lookup"><span data-stu-id="cc9ee-162">`[ServerName <String>]`: The name of the server.</span></span>
  - <span data-ttu-id="cc9ee-163">`[SubscriptionId <String>]`: Die ID des Zielabonnements.</span><span class="sxs-lookup"><span data-stu-id="cc9ee-163">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="cc9ee-164">`[VirtualNetworkRuleName <String>]`: Der Name der Regel für das virtuelle Netzwerk.</span><span class="sxs-lookup"><span data-stu-id="cc9ee-164">`[VirtualNetworkRuleName <String>]`: The name of the virtual network rule.</span></span>

## <span data-ttu-id="cc9ee-165">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="cc9ee-165">RELATED LINKS</span></span>

