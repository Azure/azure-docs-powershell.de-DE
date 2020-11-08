---
external help file: ''
Module Name: Az.PostgreSql
online version: https://docs.microsoft.com/en-us/powershell/module/az.postgresql/get-azpostgresqlserver
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PostgreSql/help/Get-AzPostgreSqlServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PostgreSql/help/Get-AzPostgreSqlServer.md
ms.openlocfilehash: 71fb10b0aeed85a716a834b42b1bdae3e5f7b270
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94008986"
---
# <span data-ttu-id="788d9-101">Get-AzPostgreSqlServer</span><span class="sxs-lookup"><span data-stu-id="788d9-101">Get-AzPostgreSqlServer</span></span>

## <span data-ttu-id="788d9-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="788d9-102">SYNOPSIS</span></span>
<span data-ttu-id="788d9-103">Ruft Informationen zu einem Server ab.</span><span class="sxs-lookup"><span data-stu-id="788d9-103">Gets information about a server.</span></span>

## <span data-ttu-id="788d9-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="788d9-104">SYNTAX</span></span>

### <span data-ttu-id="788d9-105">List1 (Standard)</span><span class="sxs-lookup"><span data-stu-id="788d9-105">List1 (Default)</span></span>
```
Get-AzPostgreSqlServer [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="788d9-106">Erhalten</span><span class="sxs-lookup"><span data-stu-id="788d9-106">Get</span></span>
```
Get-AzPostgreSqlServer -Name <String> -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="788d9-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="788d9-107">GetViaIdentity</span></span>
```
Get-AzPostgreSqlServer -InputObject <IPostgreSqlIdentity> [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="788d9-108">Liste</span><span class="sxs-lookup"><span data-stu-id="788d9-108">List</span></span>
```
Get-AzPostgreSqlServer -ResourceGroupName <String> [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

## <span data-ttu-id="788d9-109">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="788d9-109">DESCRIPTION</span></span>
<span data-ttu-id="788d9-110">Ruft Informationen zu einem Server ab.</span><span class="sxs-lookup"><span data-stu-id="788d9-110">Gets information about a server.</span></span>

## <span data-ttu-id="788d9-111">Beispiele</span><span class="sxs-lookup"><span data-stu-id="788d9-111">EXAMPLES</span></span>

### <span data-ttu-id="788d9-112">Beispiel 1: Abrufen des PostgreSQL-Servers mit dem Standardkontext</span><span class="sxs-lookup"><span data-stu-id="788d9-112">Example 1: Get PostgreSql server with default context</span></span>
```powershell
PS C:\> Get-AzPostgreSqlServer

Name                        Location AdministratorLogin Version StorageProfileStorageMb SkuName   SkuTier        SslEnforcement
----                        -------- ------------------ ------- ----------------------- -------   -------        --------------
postgresqltestserver        eastus   pwsh               9.6     5120                    GP_Gen5_4 GeneralPurpose Enabled
```

<span data-ttu-id="788d9-113">Dieses Cmdlet ruft den PostgreSQL-Server mit dem Standardkontext ab.</span><span class="sxs-lookup"><span data-stu-id="788d9-113">This cmdlet gets PostgreSql server with default context.</span></span>

### <span data-ttu-id="788d9-114">Beispiel 2: Abrufen des PostgreSQL-Servers nach Ressourcengruppe und Servername</span><span class="sxs-lookup"><span data-stu-id="788d9-114">Example 2: Get PostgreSql server by resource group and server name</span></span>
```powershell
PS C:\> Get-AzPostgreSqlServer -ResourceGroupName PostgreSqlTestRG -Name PostgreSqlTestServer

Name                 Location AdministratorLogin Version StorageProfileStorageMb SkuName   SkuTier        SslEnforcement
----                 -------- ------------------ ------- ----------------------- -------   -------        --------------
postgresqltestserver eastus   pwsh               9.6     5120                    GP_Gen5_4 GeneralPurpose Enabled
```

<span data-ttu-id="788d9-115">Dieses Cmdlet ruft den PostgreSQL-Server nach Ressourcengruppe und Servername ab.</span><span class="sxs-lookup"><span data-stu-id="788d9-115">This cmdlet gets PostgreSql server by resource group and server name.</span></span>

### <span data-ttu-id="788d9-116">Beispiel 3: Listet alle PostgreSQL-Server in der angegebenen Ressourcengruppe auf</span><span class="sxs-lookup"><span data-stu-id="788d9-116">Example 3: Lists all the PostgreSql servers in specified resource group</span></span>
```powershell
PS C:\> Get-AzPostgreSqlServer -ResourceGroupName PostgreSqlTestRG

Name                        Location AdministratorLogin Version StorageProfileStorageMb SkuName   SkuTier        SslEnforcement
----                        -------- ------------------ ------- ----------------------- -------   -------        --------------
postgresqltestserver        eastus   pwsh               9.6     5120                    GP_Gen5_4 GeneralPurpose Enabled
```

<span data-ttu-id="788d9-117">Dieses Cmdlet listet alle PostgreSQL-Server in der angegebenen Ressourcengruppe auf.</span><span class="sxs-lookup"><span data-stu-id="788d9-117">This cmdlet lists all the PostgreSql servers in specified resource group.</span></span>

### <span data-ttu-id="788d9-118">Beispiel 4: Abrufen des PostgreSQL-Servers nach Identität</span><span class="sxs-lookup"><span data-stu-id="788d9-118">Example 4: Get PostgreSql server by identity</span></span>
```powershell
PS C:\> $ID = "/subscriptions/<SubscriptionId>/resourceGroups/PostgreSqlTestRG/providers/Microsoft.DBforPostgreSQL/servers/postgresqltestserver"
PS C:\> Get-AzPostgreSqlServer -InputObject $ID

Name                 Location AdministratorLogin Version StorageProfileStorageMb SkuName   SkuTier        SslEnforcement
----                 -------- ------------------ ------- ----------------------- -------   -------        --------------
postgresqltestserver eastus   pwsh               9.6     5120                    GP_Gen5_4 GeneralPurpose Enabled
```

<span data-ttu-id="788d9-119">In dieser Cmdlet-Liste wird der PostgreSQL-Server nach Identität abgerufen.</span><span class="sxs-lookup"><span data-stu-id="788d9-119">This cmdlet lists gets PostgreSql server by identity.</span></span>

## <span data-ttu-id="788d9-120">Parameter</span><span class="sxs-lookup"><span data-stu-id="788d9-120">PARAMETERS</span></span>

### <span data-ttu-id="788d9-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="788d9-121">-DefaultProfile</span></span>
<span data-ttu-id="788d9-122">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="788d9-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="788d9-123">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="788d9-123">-InputObject</span></span>
<span data-ttu-id="788d9-124">Zu Erstell-Parameter des Parameters, lesen Sie den Abschnitt "Notizen" für Inputobject-Eigenschaften, und erstellen Sie eine Hashtabelle.</span><span class="sxs-lookup"><span data-stu-id="788d9-124">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Models.IPostgreSqlIdentity
Parameter Sets: GetViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="788d9-125">-Name</span><span class="sxs-lookup"><span data-stu-id="788d9-125">-Name</span></span>
<span data-ttu-id="788d9-126">Der Name des Servers.</span><span class="sxs-lookup"><span data-stu-id="788d9-126">The name of the server.</span></span>

```yaml
Type: System.String
Parameter Sets: Get
Aliases: ServerName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="788d9-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="788d9-127">-ResourceGroupName</span></span>
<span data-ttu-id="788d9-128">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="788d9-128">The name of the resource group.</span></span>
<span data-ttu-id="788d9-129">Bei dem Namen wird die Groß-/Kleinschreibung nicht berücksichtigt.</span><span class="sxs-lookup"><span data-stu-id="788d9-129">The name is case insensitive.</span></span>

```yaml
Type: System.String
Parameter Sets: Get, List
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="788d9-130">-Abonnement-Nr</span><span class="sxs-lookup"><span data-stu-id="788d9-130">-SubscriptionId</span></span>
<span data-ttu-id="788d9-131">Die ID des zielabonnements.</span><span class="sxs-lookup"><span data-stu-id="788d9-131">The ID of the target subscription.</span></span>

```yaml
Type: System.String[]
Parameter Sets: Get, List, List1
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="788d9-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="788d9-132">CommonParameters</span></span>
<span data-ttu-id="788d9-133">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="788d9-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="788d9-134">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="788d9-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="788d9-135">Eingaben</span><span class="sxs-lookup"><span data-stu-id="788d9-135">INPUTS</span></span>

### <span data-ttu-id="788d9-136">Microsoft. Azure. PowerShell. Cmdlets. PostgreSQL. Models. IPostgreSqlIdentity</span><span class="sxs-lookup"><span data-stu-id="788d9-136">Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Models.IPostgreSqlIdentity</span></span>

## <span data-ttu-id="788d9-137">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="788d9-137">OUTPUTS</span></span>

### <span data-ttu-id="788d9-138">Microsoft. Azure. PowerShell. Cmdlets. PostgreSQL. Models. Api20171201. IServer</span><span class="sxs-lookup"><span data-stu-id="788d9-138">Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Models.Api20171201.IServer</span></span>

## <span data-ttu-id="788d9-139">Notizen</span><span class="sxs-lookup"><span data-stu-id="788d9-139">NOTES</span></span>

<span data-ttu-id="788d9-140">Aliase</span><span class="sxs-lookup"><span data-stu-id="788d9-140">ALIASES</span></span>

<span data-ttu-id="788d9-141">komplexe Parameter Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="788d9-141">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="788d9-142">Wenn Sie die unten beschriebenen Parameter erstellen möchten, erstellen Sie eine Hashtabelle mit den entsprechenden Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="788d9-142">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="788d9-143">Wenn Sie Informationen zu Hashtabellen erhalten, führen Sie Get-Help about_Hash_Tables aus.</span><span class="sxs-lookup"><span data-stu-id="788d9-143">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="788d9-144">Inputobject <IPostgreSqlIdentity> : Identity-Parameter</span><span class="sxs-lookup"><span data-stu-id="788d9-144">INPUTOBJECT <IPostgreSqlIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="788d9-145">`[ConfigurationName <String>]`: Der Name der Serverkonfiguration.</span><span class="sxs-lookup"><span data-stu-id="788d9-145">`[ConfigurationName <String>]`: The name of the server configuration.</span></span>
  - <span data-ttu-id="788d9-146">`[DatabaseName <String>]`: Der Name der Datenbank.</span><span class="sxs-lookup"><span data-stu-id="788d9-146">`[DatabaseName <String>]`: The name of the database.</span></span>
  - <span data-ttu-id="788d9-147">`[FirewallRuleName <String>]`: Der Name der Server Firewall-Regel.</span><span class="sxs-lookup"><span data-stu-id="788d9-147">`[FirewallRuleName <String>]`: The name of the server firewall rule.</span></span>
  - <span data-ttu-id="788d9-148">`[Id <String>]`: Ressourcen Identitäts Pfad</span><span class="sxs-lookup"><span data-stu-id="788d9-148">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="788d9-149">`[LocationName <String>]`: Der Name des Standorts.</span><span class="sxs-lookup"><span data-stu-id="788d9-149">`[LocationName <String>]`: The name of the location.</span></span>
  - <span data-ttu-id="788d9-150">`[ResourceGroupName <String>]`: Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="788d9-150">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="788d9-151">Bei dem Namen wird die Groß-/Kleinschreibung nicht berücksichtigt.</span><span class="sxs-lookup"><span data-stu-id="788d9-151">The name is case insensitive.</span></span>
  - <span data-ttu-id="788d9-152">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: Der Name der Sicherheits Warnungs Richtlinie.</span><span class="sxs-lookup"><span data-stu-id="788d9-152">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: The name of the security alert policy.</span></span>
  - <span data-ttu-id="788d9-153">`[ServerName <String>]`: Der Name des Servers.</span><span class="sxs-lookup"><span data-stu-id="788d9-153">`[ServerName <String>]`: The name of the server.</span></span>
  - <span data-ttu-id="788d9-154">`[SubscriptionId <String>]`: Die ID des zielabonnements.</span><span class="sxs-lookup"><span data-stu-id="788d9-154">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="788d9-155">`[VirtualNetworkRuleName <String>]`: Der Name der Regel für das virtuelle Netzwerk.</span><span class="sxs-lookup"><span data-stu-id="788d9-155">`[VirtualNetworkRuleName <String>]`: The name of the virtual network rule.</span></span>

## <span data-ttu-id="788d9-156">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="788d9-156">RELATED LINKS</span></span>

