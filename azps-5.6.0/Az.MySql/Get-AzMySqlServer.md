---
external help file: ''
Module Name: Az.MySql
online version: https://docs.microsoft.com/powershell/module/az.mysql/get-azmysqlserver
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MySql/help/Get-AzMySqlServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MySql/help/Get-AzMySqlServer.md
ms.openlocfilehash: 7a9ef90da8861da8ae530d3a05dae4bbacd62898
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101918771"
---
# <span data-ttu-id="3c482-101">Get-AzMySqlServer</span><span class="sxs-lookup"><span data-stu-id="3c482-101">Get-AzMySqlServer</span></span>

## <span data-ttu-id="3c482-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3c482-102">SYNOPSIS</span></span>
<span data-ttu-id="3c482-103">Ruft Informationen zu einem Server ab.</span><span class="sxs-lookup"><span data-stu-id="3c482-103">Gets information about a server.</span></span>

## <span data-ttu-id="3c482-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="3c482-104">SYNTAX</span></span>

### <span data-ttu-id="3c482-105">List1 (Standard)</span><span class="sxs-lookup"><span data-stu-id="3c482-105">List1 (Default)</span></span>
```
Get-AzMySqlServer [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="3c482-106">Erhalten</span><span class="sxs-lookup"><span data-stu-id="3c482-106">Get</span></span>
```
Get-AzMySqlServer -Name <String> -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="3c482-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="3c482-107">GetViaIdentity</span></span>
```
Get-AzMySqlServer -InputObject <IMySqlIdentity> [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="3c482-108">Liste</span><span class="sxs-lookup"><span data-stu-id="3c482-108">List</span></span>
```
Get-AzMySqlServer -ResourceGroupName <String> [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

## <span data-ttu-id="3c482-109">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="3c482-109">DESCRIPTION</span></span>
<span data-ttu-id="3c482-110">Ruft Informationen zu einem Server ab.</span><span class="sxs-lookup"><span data-stu-id="3c482-110">Gets information about a server.</span></span>

## <span data-ttu-id="3c482-111">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="3c482-111">EXAMPLES</span></span>

### <span data-ttu-id="3c482-112">Beispiel 1: Get MySql server with default context</span><span class="sxs-lookup"><span data-stu-id="3c482-112">Example 1: Get MySql server with default context</span></span>
```powershell
PS C:\> Get-AzMySqlServer

Name          Location AdministratorLogin Version StorageProfileStorageMb SkuName   SkuTier        SslEnforcement
----          -------- ------------------ ------- ----------------------- -------   -------        --------------
mysql-test-11 eastus   mysql_test         5.7     5120                    GP_Gen5_4 GeneralPurpose Enabled
```

<span data-ttu-id="3c482-113">Dieses Cmdlet ruft den MySql-Server mit dem Standardkontext ab.</span><span class="sxs-lookup"><span data-stu-id="3c482-113">This cmdlet gets MySql server with default context.</span></span>

### <span data-ttu-id="3c482-114">Beispiel 2: Get MySql server by resource group and server name</span><span class="sxs-lookup"><span data-stu-id="3c482-114">Example 2: Get MySql server by resource group and server name</span></span>
```powershell
PS C:\> Get-AzMySqlServer -ResourceGroupName PowershellMySqlTest -Name mysql-test

Name          Location AdministratorLogin Version StorageProfileStorageMb SkuName   SkuTier        SslEnforcement
----          -------- ------------------ ------- ----------------------- -------   -------        --------------
mysql-test    eastus   mysql_test         5.7     5120                    GP_Gen5_4 GeneralPurpose Enabled
```

<span data-ttu-id="3c482-115">Dieses Cmdlet ruft den MySql-Server nach Ressourcengruppe und Servernamen ab.</span><span class="sxs-lookup"><span data-stu-id="3c482-115">This cmdlet gets MySql server by resource group and server name.</span></span>

### <span data-ttu-id="3c482-116">Beispiel 3: Listet alle MySql-Server in einer angegebenen Ressourcengruppe auf.</span><span class="sxs-lookup"><span data-stu-id="3c482-116">Example 3: Lists all the MySql servers in specified resource group</span></span>
```powershell
PS C:\> Get-AzMySqlServer -ResourceGroupName PowershellMySqlTest

Name          Location AdministratorLogin Version StorageProfileStorageMb SkuName   SkuTier        SslEnforcement
----          -------- ------------------ ------- ----------------------- -------   -------        ------------
mysql-test    eastus   mysql_test         5.7     5120                    GP_Gen5_4 GeneralPurpose Enabled
```

<span data-ttu-id="3c482-117">In diesem Cmdlet werden alle MySql-Server in der angegebenen Ressourcengruppe aufgeführt.</span><span class="sxs-lookup"><span data-stu-id="3c482-117">This cmdlet lists all the MySql servers in specified resource group.</span></span>

### <span data-ttu-id="3c482-118">Beispiel 4: Holen Sie sich den MySql-Server nach Identität</span><span class="sxs-lookup"><span data-stu-id="3c482-118">Example 4: Get MySql server by identity</span></span>
```powershell
PS C:\> $ID = "/subscriptions/<SubscriptionId>/resourceGroups/PowershellMySqlTest/providers/Microsoft.DBforMySQL/servers/mysql-test"
PS C:\> Get-AzMySqlServer -InputObject $ID

Name          Location AdministratorLogin Version StorageProfileStorageMb SkuName   SkuTier        SslEnforcement
----          -------- ------------------ ------- ----------------------- -------   -------        ------------
mysql-test    eastus   mysql_test         5.7     5120                    GP_Gen5_4 GeneralPurpose Enabled
```

<span data-ttu-id="3c482-119">Diese Cmdletlisten ruft den MySql-Server nach Identität ab.</span><span class="sxs-lookup"><span data-stu-id="3c482-119">This cmdlet lists gets MySql server by identity.</span></span>

## <span data-ttu-id="3c482-120">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="3c482-120">PARAMETERS</span></span>

### <span data-ttu-id="3c482-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3c482-121">-DefaultProfile</span></span>
<span data-ttu-id="3c482-122">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="3c482-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3c482-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="3c482-123">-InputObject</span></span>
<span data-ttu-id="3c482-124">Identitätsparameter Zum Erstellen lesen Sie den Abschnitt NOTIZEN für INPUTOBJECT-Eigenschaften, und erstellen Sie eine Hashtabelle.</span><span class="sxs-lookup"><span data-stu-id="3c482-124">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="3c482-125">-Name</span><span class="sxs-lookup"><span data-stu-id="3c482-125">-Name</span></span>
<span data-ttu-id="3c482-126">Der Name des Servers.</span><span class="sxs-lookup"><span data-stu-id="3c482-126">The name of the server.</span></span>

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

### <span data-ttu-id="3c482-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3c482-127">-ResourceGroupName</span></span>
<span data-ttu-id="3c482-128">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="3c482-128">The name of the resource group.</span></span>
<span data-ttu-id="3c482-129">Der Name ist groß- und kleinschreibungsunabhängiger.</span><span class="sxs-lookup"><span data-stu-id="3c482-129">The name is case insensitive.</span></span>

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

### <span data-ttu-id="3c482-130">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="3c482-130">-SubscriptionId</span></span>
<span data-ttu-id="3c482-131">Die ID des Zielabonnements.</span><span class="sxs-lookup"><span data-stu-id="3c482-131">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="3c482-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3c482-132">CommonParameters</span></span>
<span data-ttu-id="3c482-133">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3c482-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3c482-134">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="3c482-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3c482-135">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="3c482-135">INPUTS</span></span>

### <span data-ttu-id="3c482-136">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.IMySqlIdentity</span><span class="sxs-lookup"><span data-stu-id="3c482-136">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.IMySqlIdentity</span></span>

## <span data-ttu-id="3c482-137">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="3c482-137">OUTPUTS</span></span>

### <span data-ttu-id="3c482-138">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.Api20171201.IServer</span><span class="sxs-lookup"><span data-stu-id="3c482-138">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.Api20171201.IServer</span></span>

## <span data-ttu-id="3c482-139">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="3c482-139">NOTES</span></span>

<span data-ttu-id="3c482-140">ALIASE</span><span class="sxs-lookup"><span data-stu-id="3c482-140">ALIASES</span></span>

<span data-ttu-id="3c482-141">KOMPLEXE PARAMETEREIGENSCHAFTEN</span><span class="sxs-lookup"><span data-stu-id="3c482-141">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="3c482-142">Um die unten beschriebenen Parameter zu erstellen, erstellen Sie eine Hashtabelle, die die entsprechenden Eigenschaften enthält.</span><span class="sxs-lookup"><span data-stu-id="3c482-142">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="3c482-143">Informationen zu Hashtabellen finden Sie unter Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="3c482-143">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="3c482-144">INPUTOBJECT <IMySqlIdentity> : Identitätsparameter</span><span class="sxs-lookup"><span data-stu-id="3c482-144">INPUTOBJECT <IMySqlIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="3c482-145">`[ConfigurationName <String>]`: Der Name der Serverkonfiguration.</span><span class="sxs-lookup"><span data-stu-id="3c482-145">`[ConfigurationName <String>]`: The name of the server configuration.</span></span>
  - <span data-ttu-id="3c482-146">`[DatabaseName <String>]`: Der Name der Datenbank.</span><span class="sxs-lookup"><span data-stu-id="3c482-146">`[DatabaseName <String>]`: The name of the database.</span></span>
  - <span data-ttu-id="3c482-147">`[FirewallRuleName <String>]`: Der Name der Serverfirewallregel.</span><span class="sxs-lookup"><span data-stu-id="3c482-147">`[FirewallRuleName <String>]`: The name of the server firewall rule.</span></span>
  - <span data-ttu-id="3c482-148">`[Id <String>]`: Ressourcenidentitätspfad</span><span class="sxs-lookup"><span data-stu-id="3c482-148">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="3c482-149">`[KeyName <String>]`: Der Name des Serverschlüssels.</span><span class="sxs-lookup"><span data-stu-id="3c482-149">`[KeyName <String>]`: The name of the server key.</span></span>
  - <span data-ttu-id="3c482-150">`[LocationName <String>]`: Der Name des Speicherorts.</span><span class="sxs-lookup"><span data-stu-id="3c482-150">`[LocationName <String>]`: The name of the location.</span></span>
  - <span data-ttu-id="3c482-151">`[ResourceGroupName <String>]`: Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="3c482-151">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="3c482-152">Der Name ist groß- und kleinschreibungsunabhängiger.</span><span class="sxs-lookup"><span data-stu-id="3c482-152">The name is case insensitive.</span></span>
  - <span data-ttu-id="3c482-153">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: Der Name der Sicherheitsbenachrichtigungsrichtlinie.</span><span class="sxs-lookup"><span data-stu-id="3c482-153">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: The name of the security alert policy.</span></span>
  - <span data-ttu-id="3c482-154">`[ServerName <String>]`: Der Name des Servers.</span><span class="sxs-lookup"><span data-stu-id="3c482-154">`[ServerName <String>]`: The name of the server.</span></span>
  - <span data-ttu-id="3c482-155">`[SubscriptionId <String>]`: Die ID des Zielabonnements.</span><span class="sxs-lookup"><span data-stu-id="3c482-155">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="3c482-156">`[VirtualNetworkRuleName <String>]`: Der Name der Regel für das virtuelle Netzwerk.</span><span class="sxs-lookup"><span data-stu-id="3c482-156">`[VirtualNetworkRuleName <String>]`: The name of the virtual network rule.</span></span>

## <span data-ttu-id="3c482-157">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="3c482-157">RELATED LINKS</span></span>

