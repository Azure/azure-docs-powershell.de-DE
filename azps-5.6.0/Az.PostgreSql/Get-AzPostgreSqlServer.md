---
external help file: ''
Module Name: Az.PostgreSql
online version: https://docs.microsoft.com/powershell/module/az.postgresql/get-azpostgresqlserver
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PostgreSql/help/Get-AzPostgreSqlServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PostgreSql/help/Get-AzPostgreSqlServer.md
ms.openlocfilehash: 718443cc31972f1d1d53a5b5802dc50c1ac31df0
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101933776"
---
# <span data-ttu-id="c4d4d-101">Get-AzPostgreSqlServer</span><span class="sxs-lookup"><span data-stu-id="c4d4d-101">Get-AzPostgreSqlServer</span></span>

## <span data-ttu-id="c4d4d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c4d4d-102">SYNOPSIS</span></span>
<span data-ttu-id="c4d4d-103">Ruft Informationen zu einem Server ab.</span><span class="sxs-lookup"><span data-stu-id="c4d4d-103">Gets information about a server.</span></span>

## <span data-ttu-id="c4d4d-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="c4d4d-104">SYNTAX</span></span>

### <span data-ttu-id="c4d4d-105">List1 (Standard)</span><span class="sxs-lookup"><span data-stu-id="c4d4d-105">List1 (Default)</span></span>
```
Get-AzPostgreSqlServer [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="c4d4d-106">Erhalten</span><span class="sxs-lookup"><span data-stu-id="c4d4d-106">Get</span></span>
```
Get-AzPostgreSqlServer -Name <String> -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="c4d4d-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="c4d4d-107">GetViaIdentity</span></span>
```
Get-AzPostgreSqlServer -InputObject <IPostgreSqlIdentity> [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="c4d4d-108">Liste</span><span class="sxs-lookup"><span data-stu-id="c4d4d-108">List</span></span>
```
Get-AzPostgreSqlServer -ResourceGroupName <String> [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

## <span data-ttu-id="c4d4d-109">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="c4d4d-109">DESCRIPTION</span></span>
<span data-ttu-id="c4d4d-110">Ruft Informationen zu einem Server ab.</span><span class="sxs-lookup"><span data-stu-id="c4d4d-110">Gets information about a server.</span></span>

## <span data-ttu-id="c4d4d-111">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="c4d4d-111">EXAMPLES</span></span>

### <span data-ttu-id="c4d4d-112">Beispiel 1: PostgreSql-Server mit Standardkontext erhalten</span><span class="sxs-lookup"><span data-stu-id="c4d4d-112">Example 1: Get PostgreSql server with default context</span></span>
```powershell
PS C:\> Get-AzPostgreSqlServer

Name                        Location AdministratorLogin Version StorageProfileStorageMb SkuName   SkuTier        SslEnforcement
----                        -------- ------------------ ------- ----------------------- -------   -------        --------------
postgresqltestserver        eastus   pwsh               9.6     5120                    GP_Gen5_4 GeneralPurpose Enabled
```

<span data-ttu-id="c4d4d-113">Dieses Cmdlet ruft den PostgreSql-Server mit dem Standardkontext ab.</span><span class="sxs-lookup"><span data-stu-id="c4d4d-113">This cmdlet gets PostgreSql server with default context.</span></span>

### <span data-ttu-id="c4d4d-114">Beispiel 2: Erhalten von PostgreSql-Server nach Ressourcengruppe und Servername</span><span class="sxs-lookup"><span data-stu-id="c4d4d-114">Example 2: Get PostgreSql server by resource group and server name</span></span>
```powershell
PS C:\> Get-AzPostgreSqlServer -ResourceGroupName PostgreSqlTestRG -Name PostgreSqlTestServer

Name                 Location AdministratorLogin Version StorageProfileStorageMb SkuName   SkuTier        SslEnforcement
----                 -------- ------------------ ------- ----------------------- -------   -------        --------------
postgresqltestserver eastus   pwsh               9.6     5120                    GP_Gen5_4 GeneralPurpose Enabled
```

<span data-ttu-id="c4d4d-115">Dieses Cmdlet ruft den PostgreSql-Server nach Ressourcengruppe und Servernamen ab.</span><span class="sxs-lookup"><span data-stu-id="c4d4d-115">This cmdlet gets PostgreSql server by resource group and server name.</span></span>

### <span data-ttu-id="c4d4d-116">Beispiel 3: Listet alle PostgreSql-Server in einer angegebenen Ressourcengruppe auf.</span><span class="sxs-lookup"><span data-stu-id="c4d4d-116">Example 3: Lists all the PostgreSql servers in specified resource group</span></span>
```powershell
PS C:\> Get-AzPostgreSqlServer -ResourceGroupName PostgreSqlTestRG

Name                        Location AdministratorLogin Version StorageProfileStorageMb SkuName   SkuTier        SslEnforcement
----                        -------- ------------------ ------- ----------------------- -------   -------        --------------
postgresqltestserver        eastus   pwsh               9.6     5120                    GP_Gen5_4 GeneralPurpose Enabled
```

<span data-ttu-id="c4d4d-117">In diesem Cmdlet werden alle PostgreSql-Server in der angegebenen Ressourcengruppe aufgeführt.</span><span class="sxs-lookup"><span data-stu-id="c4d4d-117">This cmdlet lists all the PostgreSql servers in specified resource group.</span></span>

### <span data-ttu-id="c4d4d-118">Beispiel 4: Holen Sie sich den PostgreSql-Server nach Identität</span><span class="sxs-lookup"><span data-stu-id="c4d4d-118">Example 4: Get PostgreSql server by identity</span></span>
```powershell
PS C:\> $ID = "/subscriptions/<SubscriptionId>/resourceGroups/PostgreSqlTestRG/providers/Microsoft.DBforPostgreSQL/servers/postgresqltestserver"
PS C:\> Get-AzPostgreSqlServer -InputObject $ID

Name                 Location AdministratorLogin Version StorageProfileStorageMb SkuName   SkuTier        SslEnforcement
----                 -------- ------------------ ------- ----------------------- -------   -------        --------------
postgresqltestserver eastus   pwsh               9.6     5120                    GP_Gen5_4 GeneralPurpose Enabled
```

<span data-ttu-id="c4d4d-119">Diese Cmdletlisten erhalten den PostgreSql-Server nach Identität.</span><span class="sxs-lookup"><span data-stu-id="c4d4d-119">This cmdlet lists gets PostgreSql server by identity.</span></span>

## <span data-ttu-id="c4d4d-120">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="c4d4d-120">PARAMETERS</span></span>

### <span data-ttu-id="c4d4d-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c4d4d-121">-DefaultProfile</span></span>
<span data-ttu-id="c4d4d-122">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="c4d4d-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c4d4d-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="c4d4d-123">-InputObject</span></span>
<span data-ttu-id="c4d4d-124">Identitätsparameter Zum Erstellen lesen Sie den Abschnitt NOTIZEN für INPUTOBJECT-Eigenschaften, und erstellen Sie eine Hashtabelle.</span><span class="sxs-lookup"><span data-stu-id="c4d4d-124">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="c4d4d-125">-Name</span><span class="sxs-lookup"><span data-stu-id="c4d4d-125">-Name</span></span>
<span data-ttu-id="c4d4d-126">Der Name des Servers.</span><span class="sxs-lookup"><span data-stu-id="c4d4d-126">The name of the server.</span></span>

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

### <span data-ttu-id="c4d4d-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c4d4d-127">-ResourceGroupName</span></span>
<span data-ttu-id="c4d4d-128">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="c4d4d-128">The name of the resource group.</span></span>
<span data-ttu-id="c4d4d-129">Der Name ist groß- und kleinschreibungsunabhängiger.</span><span class="sxs-lookup"><span data-stu-id="c4d4d-129">The name is case insensitive.</span></span>

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

### <span data-ttu-id="c4d4d-130">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="c4d4d-130">-SubscriptionId</span></span>
<span data-ttu-id="c4d4d-131">Die ID des Zielabonnements.</span><span class="sxs-lookup"><span data-stu-id="c4d4d-131">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="c4d4d-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c4d4d-132">CommonParameters</span></span>
<span data-ttu-id="c4d4d-133">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c4d4d-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c4d4d-134">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="c4d4d-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c4d4d-135">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="c4d4d-135">INPUTS</span></span>

### <span data-ttu-id="c4d4d-136">Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Models.IPostgreSqlIdentity</span><span class="sxs-lookup"><span data-stu-id="c4d4d-136">Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Models.IPostgreSqlIdentity</span></span>

## <span data-ttu-id="c4d4d-137">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="c4d4d-137">OUTPUTS</span></span>

### <span data-ttu-id="c4d4d-138">Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Models.Api20171201.IServer</span><span class="sxs-lookup"><span data-stu-id="c4d4d-138">Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Models.Api20171201.IServer</span></span>

## <span data-ttu-id="c4d4d-139">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="c4d4d-139">NOTES</span></span>

<span data-ttu-id="c4d4d-140">ALIASE</span><span class="sxs-lookup"><span data-stu-id="c4d4d-140">ALIASES</span></span>

<span data-ttu-id="c4d4d-141">KOMPLEXE PARAMETEREIGENSCHAFTEN</span><span class="sxs-lookup"><span data-stu-id="c4d4d-141">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="c4d4d-142">Um die unten beschriebenen Parameter zu erstellen, erstellen Sie eine Hashtabelle, die die entsprechenden Eigenschaften enthält.</span><span class="sxs-lookup"><span data-stu-id="c4d4d-142">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="c4d4d-143">Informationen zu Hashtabellen finden Sie unter Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="c4d4d-143">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="c4d4d-144">INPUTOBJECT <IPostgreSqlIdentity> : Identitätsparameter</span><span class="sxs-lookup"><span data-stu-id="c4d4d-144">INPUTOBJECT <IPostgreSqlIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="c4d4d-145">`[ConfigurationName <String>]`: Der Name der Serverkonfiguration.</span><span class="sxs-lookup"><span data-stu-id="c4d4d-145">`[ConfigurationName <String>]`: The name of the server configuration.</span></span>
  - <span data-ttu-id="c4d4d-146">`[DatabaseName <String>]`: Der Name der Datenbank.</span><span class="sxs-lookup"><span data-stu-id="c4d4d-146">`[DatabaseName <String>]`: The name of the database.</span></span>
  - <span data-ttu-id="c4d4d-147">`[FirewallRuleName <String>]`: Der Name der Serverfirewallregel.</span><span class="sxs-lookup"><span data-stu-id="c4d4d-147">`[FirewallRuleName <String>]`: The name of the server firewall rule.</span></span>
  - <span data-ttu-id="c4d4d-148">`[Id <String>]`: Ressourcenidentitätspfad</span><span class="sxs-lookup"><span data-stu-id="c4d4d-148">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="c4d4d-149">`[LocationName <String>]`: Der Name des Speicherorts.</span><span class="sxs-lookup"><span data-stu-id="c4d4d-149">`[LocationName <String>]`: The name of the location.</span></span>
  - <span data-ttu-id="c4d4d-150">`[ResourceGroupName <String>]`: Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="c4d4d-150">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="c4d4d-151">Der Name ist groß- und kleinschreibungsunabhängiger.</span><span class="sxs-lookup"><span data-stu-id="c4d4d-151">The name is case insensitive.</span></span>
  - <span data-ttu-id="c4d4d-152">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: Der Name der Sicherheitsbenachrichtigungsrichtlinie.</span><span class="sxs-lookup"><span data-stu-id="c4d4d-152">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: The name of the security alert policy.</span></span>
  - <span data-ttu-id="c4d4d-153">`[ServerName <String>]`: Der Name des Servers.</span><span class="sxs-lookup"><span data-stu-id="c4d4d-153">`[ServerName <String>]`: The name of the server.</span></span>
  - <span data-ttu-id="c4d4d-154">`[SubscriptionId <String>]`: Die ID des Zielabonnements.</span><span class="sxs-lookup"><span data-stu-id="c4d4d-154">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="c4d4d-155">`[VirtualNetworkRuleName <String>]`: Der Name der Regel für das virtuelle Netzwerk.</span><span class="sxs-lookup"><span data-stu-id="c4d4d-155">`[VirtualNetworkRuleName <String>]`: The name of the virtual network rule.</span></span>

## <span data-ttu-id="c4d4d-156">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="c4d4d-156">RELATED LINKS</span></span>

