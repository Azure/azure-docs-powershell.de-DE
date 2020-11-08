---
external help file: ''
Module Name: Az.MySql
online version: https://docs.microsoft.com/en-us/powershell/module/az.mysql/get-azmysqlserver
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MySql/help/Get-AzMySqlServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MySql/help/Get-AzMySqlServer.md
ms.openlocfilehash: e2187c95237cdb89915c47fc7089fd5f9d38cff1
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94173680"
---
# <span data-ttu-id="0cce6-101">Get-AzMySqlServer</span><span class="sxs-lookup"><span data-stu-id="0cce6-101">Get-AzMySqlServer</span></span>

## <span data-ttu-id="0cce6-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="0cce6-102">SYNOPSIS</span></span>
<span data-ttu-id="0cce6-103">Ruft Informationen zu einem Server ab.</span><span class="sxs-lookup"><span data-stu-id="0cce6-103">Gets information about a server.</span></span>

## <span data-ttu-id="0cce6-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="0cce6-104">SYNTAX</span></span>

### <span data-ttu-id="0cce6-105">List1 (Standard)</span><span class="sxs-lookup"><span data-stu-id="0cce6-105">List1 (Default)</span></span>
```
Get-AzMySqlServer [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="0cce6-106">Erhalten</span><span class="sxs-lookup"><span data-stu-id="0cce6-106">Get</span></span>
```
Get-AzMySqlServer -Name <String> -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="0cce6-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="0cce6-107">GetViaIdentity</span></span>
```
Get-AzMySqlServer -InputObject <IMySqlIdentity> [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="0cce6-108">Liste</span><span class="sxs-lookup"><span data-stu-id="0cce6-108">List</span></span>
```
Get-AzMySqlServer -ResourceGroupName <String> [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

## <span data-ttu-id="0cce6-109">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="0cce6-109">DESCRIPTION</span></span>
<span data-ttu-id="0cce6-110">Ruft Informationen zu einem Server ab.</span><span class="sxs-lookup"><span data-stu-id="0cce6-110">Gets information about a server.</span></span>

## <span data-ttu-id="0cce6-111">Beispiele</span><span class="sxs-lookup"><span data-stu-id="0cce6-111">EXAMPLES</span></span>

### <span data-ttu-id="0cce6-112">Beispiel 1: Abrufen des MySQL-Servers mit dem Standardkontext</span><span class="sxs-lookup"><span data-stu-id="0cce6-112">Example 1: Get MySql server with default context</span></span>
```powershell
PS C:\> Get-AzMySqlServer

Name          Location AdministratorLogin Version StorageProfileStorageMb SkuName   SkuTier        SslEnforcement
----          -------- ------------------ ------- ----------------------- -------   -------        --------------
mysql-test-11 eastus   mysql_test         5.7     5120                    GP_Gen5_4 GeneralPurpose Enabled
```

<span data-ttu-id="0cce6-113">Dieses Cmdlet ruft den MySQL-Server mit dem Standardkontext ab.</span><span class="sxs-lookup"><span data-stu-id="0cce6-113">This cmdlet gets MySql server with default context.</span></span>

### <span data-ttu-id="0cce6-114">Beispiel 2: Abrufen des MySQL-Servers nach Ressourcengruppe und Servername</span><span class="sxs-lookup"><span data-stu-id="0cce6-114">Example 2: Get MySql server by resource group and server name</span></span>
```powershell
PS C:\> Get-AzMySqlServer -ResourceGroupName PowershellMySqlTest -Name mysql-test

Name          Location AdministratorLogin Version StorageProfileStorageMb SkuName   SkuTier        SslEnforcement
----          -------- ------------------ ------- ----------------------- -------   -------        --------------
mysql-test    eastus   mysql_test         5.7     5120                    GP_Gen5_4 GeneralPurpose Enabled
```

<span data-ttu-id="0cce6-115">Dieses Cmdlet ruft den MySQL-Server nach Ressourcengruppe und Servername ab.</span><span class="sxs-lookup"><span data-stu-id="0cce6-115">This cmdlet gets MySql server by resource group and server name.</span></span>

### <span data-ttu-id="0cce6-116">Beispiel 3: Listet alle MySQL-Server in der angegebenen Ressourcengruppe auf</span><span class="sxs-lookup"><span data-stu-id="0cce6-116">Example 3: Lists all the MySql servers in specified resource group</span></span>
```powershell
PS C:\> Get-AzMySqlServer -ResourceGroupName PowershellMySqlTest

Name          Location AdministratorLogin Version StorageProfileStorageMb SkuName   SkuTier        SslEnforcement
----          -------- ------------------ ------- ----------------------- -------   -------        ------------
mysql-test    eastus   mysql_test         5.7     5120                    GP_Gen5_4 GeneralPurpose Enabled
```

<span data-ttu-id="0cce6-117">Dieses Cmdlet listet alle MySQL-Server in der angegebenen Ressourcengruppe auf.</span><span class="sxs-lookup"><span data-stu-id="0cce6-117">This cmdlet lists all the MySql servers in specified resource group.</span></span>

### <span data-ttu-id="0cce6-118">Beispiel 4: Abrufen von MySQL Server nach Identität</span><span class="sxs-lookup"><span data-stu-id="0cce6-118">Example 4: Get MySql server by identity</span></span>
```powershell
PS C:\> $ID = "/subscriptions/<SubscriptionId>/resourceGroups/PowershellMySqlTest/providers/Microsoft.DBforMySQL/servers/mysql-test"
PS C:\> Get-AzMySqlServer -InputObject $ID

Name          Location AdministratorLogin Version StorageProfileStorageMb SkuName   SkuTier        SslEnforcement
----          -------- ------------------ ------- ----------------------- -------   -------        ------------
mysql-test    eastus   mysql_test         5.7     5120                    GP_Gen5_4 GeneralPurpose Enabled
```

<span data-ttu-id="0cce6-119">In dieser Cmdlet-Liste wird der MySQL-Server nach Identität abgerufen.</span><span class="sxs-lookup"><span data-stu-id="0cce6-119">This cmdlet lists gets MySql server by identity.</span></span>

## <span data-ttu-id="0cce6-120">Parameter</span><span class="sxs-lookup"><span data-stu-id="0cce6-120">PARAMETERS</span></span>

### <span data-ttu-id="0cce6-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0cce6-121">-DefaultProfile</span></span>
<span data-ttu-id="0cce6-122">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="0cce6-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0cce6-123">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="0cce6-123">-InputObject</span></span>
<span data-ttu-id="0cce6-124">Zu Erstell-Parameter des Parameters, lesen Sie den Abschnitt "Notizen" für Inputobject-Eigenschaften, und erstellen Sie eine Hashtabelle.</span><span class="sxs-lookup"><span data-stu-id="0cce6-124">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.IMySqlIdentity
Parameter Sets: GetViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="0cce6-125">-Name</span><span class="sxs-lookup"><span data-stu-id="0cce6-125">-Name</span></span>
<span data-ttu-id="0cce6-126">Der Name des Servers.</span><span class="sxs-lookup"><span data-stu-id="0cce6-126">The name of the server.</span></span>

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

### <span data-ttu-id="0cce6-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0cce6-127">-ResourceGroupName</span></span>
<span data-ttu-id="0cce6-128">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="0cce6-128">The name of the resource group.</span></span>
<span data-ttu-id="0cce6-129">Bei dem Namen wird die Groß-/Kleinschreibung nicht berücksichtigt.</span><span class="sxs-lookup"><span data-stu-id="0cce6-129">The name is case insensitive.</span></span>

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

### <span data-ttu-id="0cce6-130">-Abonnement-Nr</span><span class="sxs-lookup"><span data-stu-id="0cce6-130">-SubscriptionId</span></span>
<span data-ttu-id="0cce6-131">Die ID des zielabonnements.</span><span class="sxs-lookup"><span data-stu-id="0cce6-131">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="0cce6-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0cce6-132">CommonParameters</span></span>
<span data-ttu-id="0cce6-133">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0cce6-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0cce6-134">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="0cce6-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0cce6-135">Eingaben</span><span class="sxs-lookup"><span data-stu-id="0cce6-135">INPUTS</span></span>

### <span data-ttu-id="0cce6-136">Microsoft. Azure. PowerShell. Cmdlets. MySQL. Models. IMySqlIdentity</span><span class="sxs-lookup"><span data-stu-id="0cce6-136">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.IMySqlIdentity</span></span>

## <span data-ttu-id="0cce6-137">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="0cce6-137">OUTPUTS</span></span>

### <span data-ttu-id="0cce6-138">Microsoft. Azure. PowerShell. Cmdlets. MySQL. Models. Api20171201. IServer</span><span class="sxs-lookup"><span data-stu-id="0cce6-138">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.Api20171201.IServer</span></span>

## <span data-ttu-id="0cce6-139">Notizen</span><span class="sxs-lookup"><span data-stu-id="0cce6-139">NOTES</span></span>

<span data-ttu-id="0cce6-140">Aliase</span><span class="sxs-lookup"><span data-stu-id="0cce6-140">ALIASES</span></span>

<span data-ttu-id="0cce6-141">komplexe Parameter Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="0cce6-141">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="0cce6-142">Wenn Sie die unten beschriebenen Parameter erstellen möchten, erstellen Sie eine Hashtabelle mit den entsprechenden Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="0cce6-142">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="0cce6-143">Wenn Sie Informationen zu Hashtabellen erhalten, führen Sie Get-Help about_Hash_Tables aus.</span><span class="sxs-lookup"><span data-stu-id="0cce6-143">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="0cce6-144">Inputobject <IMySqlIdentity> : Identity-Parameter</span><span class="sxs-lookup"><span data-stu-id="0cce6-144">INPUTOBJECT <IMySqlIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="0cce6-145">`[ConfigurationName <String>]`: Der Name der Serverkonfiguration.</span><span class="sxs-lookup"><span data-stu-id="0cce6-145">`[ConfigurationName <String>]`: The name of the server configuration.</span></span>
  - <span data-ttu-id="0cce6-146">`[DatabaseName <String>]`: Der Name der Datenbank.</span><span class="sxs-lookup"><span data-stu-id="0cce6-146">`[DatabaseName <String>]`: The name of the database.</span></span>
  - <span data-ttu-id="0cce6-147">`[FirewallRuleName <String>]`: Der Name der Server Firewall-Regel.</span><span class="sxs-lookup"><span data-stu-id="0cce6-147">`[FirewallRuleName <String>]`: The name of the server firewall rule.</span></span>
  - <span data-ttu-id="0cce6-148">`[Id <String>]`: Ressourcen Identitäts Pfad</span><span class="sxs-lookup"><span data-stu-id="0cce6-148">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="0cce6-149">`[LocationName <String>]`: Der Name des Standorts.</span><span class="sxs-lookup"><span data-stu-id="0cce6-149">`[LocationName <String>]`: The name of the location.</span></span>
  - <span data-ttu-id="0cce6-150">`[ResourceGroupName <String>]`: Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="0cce6-150">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="0cce6-151">Bei dem Namen wird die Groß-/Kleinschreibung nicht berücksichtigt.</span><span class="sxs-lookup"><span data-stu-id="0cce6-151">The name is case insensitive.</span></span>
  - <span data-ttu-id="0cce6-152">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: Der Name der Sicherheits Warnungs Richtlinie.</span><span class="sxs-lookup"><span data-stu-id="0cce6-152">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: The name of the security alert policy.</span></span>
  - <span data-ttu-id="0cce6-153">`[ServerName <String>]`: Der Name des Servers.</span><span class="sxs-lookup"><span data-stu-id="0cce6-153">`[ServerName <String>]`: The name of the server.</span></span>
  - <span data-ttu-id="0cce6-154">`[SubscriptionId <String>]`: Die ID des zielabonnements.</span><span class="sxs-lookup"><span data-stu-id="0cce6-154">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="0cce6-155">`[VirtualNetworkRuleName <String>]`: Der Name der Regel für das virtuelle Netzwerk.</span><span class="sxs-lookup"><span data-stu-id="0cce6-155">`[VirtualNetworkRuleName <String>]`: The name of the virtual network rule.</span></span>

## <span data-ttu-id="0cce6-156">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="0cce6-156">RELATED LINKS</span></span>

